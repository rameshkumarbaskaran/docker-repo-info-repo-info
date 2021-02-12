## `irssi:1-alpine`

```console
$ docker pull irssi@sha256:4c55efb401f0e61a9bf5b94d05813922d51c4bb2c3422fe70aa6c15007cd72f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `irssi:1-alpine` - linux; amd64

```console
$ docker pull irssi@sha256:6f155185a9910969212aaa20048910405c719366e2a96066a673d63f2ff8dfb9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18636192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5e01025e17df3698ef23de49fcab9568d7136952e0cca39cf883603971b272`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 28 Jan 2021 23:19:38 GMT
ADD file:0e2d487cd80773e947c8aae6daad3d565b7bb019a954af2b8bff188681c00d81 in / 
# Thu, 28 Jan 2021 23:19:38 GMT
CMD ["/bin/sh"]
# Fri, 12 Feb 2021 02:21:49 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Fri, 12 Feb 2021 02:21:49 GMT
ENV HOME=/home/user
# Fri, 12 Feb 2021 02:21:50 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Fri, 12 Feb 2021 02:21:50 GMT
ENV LANG=C.UTF-8
# Fri, 12 Feb 2021 02:21:50 GMT
ENV IRSSI_VERSION=1.2.2
# Fri, 12 Feb 2021 02:22:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		automake 		coreutils 		dpkg-dev dpkg 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		make 		ncurses-dev 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-true-color 		--with-bot 		--with-proxy 		--with-socks 	; 	make -j "$(nproc)"; 	make install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Fri, 12 Feb 2021 02:22:43 GMT
WORKDIR /home/user
# Fri, 12 Feb 2021 02:22:43 GMT
USER user
# Fri, 12 Feb 2021 02:22:44 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4c0d98bf9879488e0407f897d9dd4bf758555a78e39675e72b5124ccf12c2580`  
		Last Modified: Thu, 28 Jan 2021 23:20:08 GMT  
		Size: 2.8 MB (2811321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e9195ef07e8ce96840069ea52b95743ba4e95c933b6c5aafc91148fb4721f44`  
		Last Modified: Fri, 12 Feb 2021 02:23:03 GMT  
		Size: 9.5 MB (9546138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d8535849319e138c31afbe4b9cb3d1b7d68f972783f0eae615623b4f590261`  
		Last Modified: Fri, 12 Feb 2021 02:23:01 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5e2e93832b2db8f3b88719edc11ed0375635931b550d8be30680601dd4d2ef`  
		Last Modified: Fri, 12 Feb 2021 02:23:02 GMT  
		Size: 6.3 MB (6277489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:698e84cfae8986acac7e59843e695264d41f14def4b021734c103f0a92a0e069
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17380412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9e8c8a3db72b33c84df4161fe46bbf8c9378e8b424b689a285da48e2c0e608`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 28 Jan 2021 23:49:59 GMT
ADD file:c197324e4979e2a7b257ad683d20dd9cbdae525a076bd68fe6aa0e0b126875df in / 
# Thu, 28 Jan 2021 23:49:59 GMT
CMD ["/bin/sh"]
# Fri, 12 Feb 2021 01:54:42 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Fri, 12 Feb 2021 01:54:43 GMT
ENV HOME=/home/user
# Fri, 12 Feb 2021 01:54:45 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Fri, 12 Feb 2021 01:54:45 GMT
ENV LANG=C.UTF-8
# Fri, 12 Feb 2021 01:54:46 GMT
ENV IRSSI_VERSION=1.2.2
# Fri, 12 Feb 2021 01:55:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		automake 		coreutils 		dpkg-dev dpkg 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		make 		ncurses-dev 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-true-color 		--with-bot 		--with-proxy 		--with-socks 	; 	make -j "$(nproc)"; 	make install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Fri, 12 Feb 2021 01:55:33 GMT
WORKDIR /home/user
# Fri, 12 Feb 2021 01:55:34 GMT
USER user
# Fri, 12 Feb 2021 01:55:34 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a66f440da051140fefcb0a520bdeb69d763b1eb4fd1b2ed46b4c0a168e335108`  
		Last Modified: Thu, 28 Jan 2021 23:50:33 GMT  
		Size: 2.6 MB (2621759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12451b1bc4d5c62d33eef08cbcdefae0154eb47a002ac9794b7ef0ddeb5184c1`  
		Last Modified: Fri, 12 Feb 2021 01:55:53 GMT  
		Size: 8.8 MB (8779064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e8ca4053b93c992549af5d1f53bb609a7597028ae863fa2f2a59598a2d03d3`  
		Last Modified: Fri, 12 Feb 2021 01:55:49 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39bf2e55d75b67d6b2757768d5563dd901045093c88ec3a44b279d06c2d0c588`  
		Last Modified: Fri, 12 Feb 2021 01:55:51 GMT  
		Size: 6.0 MB (5978314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:d6ae62f0fb1fe35688f617e54fcd40ef3651107ee957c0ed867d3e930e466f92
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16826803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10355eb724bc2f005236178c2e9ad47a899c3ac11890e4ab2b58f586c746e16e`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 28 Jan 2021 23:58:03 GMT
ADD file:98a89b90a8b442eed5301790dd2bd3a27391c5e4426126eed9d1cf44e70f8857 in / 
# Thu, 28 Jan 2021 23:58:04 GMT
CMD ["/bin/sh"]
# Fri, 12 Feb 2021 02:02:20 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Fri, 12 Feb 2021 02:02:22 GMT
ENV HOME=/home/user
# Fri, 12 Feb 2021 02:02:23 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Fri, 12 Feb 2021 02:02:24 GMT
ENV LANG=C.UTF-8
# Fri, 12 Feb 2021 02:02:25 GMT
ENV IRSSI_VERSION=1.2.2
# Fri, 12 Feb 2021 02:03:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		automake 		coreutils 		dpkg-dev dpkg 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		make 		ncurses-dev 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-true-color 		--with-bot 		--with-proxy 		--with-socks 	; 	make -j "$(nproc)"; 	make install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Fri, 12 Feb 2021 02:03:10 GMT
WORKDIR /home/user
# Fri, 12 Feb 2021 02:03:11 GMT
USER user
# Fri, 12 Feb 2021 02:03:12 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9b1db703a337d301b1d50292acfbabd5fb3796511b962410c554420b85cd78dc`  
		Last Modified: Thu, 28 Jan 2021 23:58:38 GMT  
		Size: 2.4 MB (2423559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a720b45ecd098b693042f7458e1a870e1a7d3161e05dd3b730a75653d15eaa`  
		Last Modified: Fri, 12 Feb 2021 02:03:36 GMT  
		Size: 8.6 MB (8630419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7abea0ca0fe92746a60d6f2b791751a646a9766482fef45934dba57a70e9e4`  
		Last Modified: Fri, 12 Feb 2021 02:03:32 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6fa92e39aa3ecdc3f120c1de2a486a79fd715de8c9c10b1870b4e7ed61f7a0`  
		Last Modified: Fri, 12 Feb 2021 02:03:34 GMT  
		Size: 5.8 MB (5771554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:3b9041124ac4d90b6fca2a0b7e2394b45dbc395bad1dba33697706f602368083
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18483592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e478282eb524a3206e9cc38f551d08878bcec7cab3eaf0c0e26371dd284e40`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 28 Jan 2021 23:39:33 GMT
ADD file:fecabe41deaeb72acdd63023566d87ae48b013ef80c97fdd993b55d6c727da93 in / 
# Thu, 28 Jan 2021 23:39:34 GMT
CMD ["/bin/sh"]
# Fri, 12 Feb 2021 02:42:59 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Fri, 12 Feb 2021 02:43:01 GMT
ENV HOME=/home/user
# Fri, 12 Feb 2021 02:43:03 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Fri, 12 Feb 2021 02:43:04 GMT
ENV LANG=C.UTF-8
# Fri, 12 Feb 2021 02:43:05 GMT
ENV IRSSI_VERSION=1.2.2
# Fri, 12 Feb 2021 02:43:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		automake 		coreutils 		dpkg-dev dpkg 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		make 		ncurses-dev 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-true-color 		--with-bot 		--with-proxy 		--with-socks 	; 	make -j "$(nproc)"; 	make install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Fri, 12 Feb 2021 02:43:53 GMT
WORKDIR /home/user
# Fri, 12 Feb 2021 02:43:53 GMT
USER user
# Fri, 12 Feb 2021 02:43:54 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2914792bc417803b2106001990194cc00cdd4b6fd97cd21a368f26148bc8e722`  
		Last Modified: Thu, 28 Jan 2021 23:40:10 GMT  
		Size: 2.7 MB (2711261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1472be30a9c004f7572fa2ea158640b79968100f2315d8e360aa93af7e0ac6ec`  
		Last Modified: Fri, 12 Feb 2021 02:44:16 GMT  
		Size: 9.5 MB (9542244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be9ff8abf426fb845619acdb1a33f5eb5e350caa2cf190408b1ef8e0b24fc5c`  
		Last Modified: Fri, 12 Feb 2021 02:44:13 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:166c8668e79dc504a5684693fd3b134639984128b42a0773f2fa5cd9e232698a`  
		Last Modified: Fri, 12 Feb 2021 02:44:14 GMT  
		Size: 6.2 MB (6228816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1-alpine` - linux; 386

```console
$ docker pull irssi@sha256:3eb3e9d9632f9141e74c26a33e48d845c1c6d125db99aba5e822698f8f6bbc69
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17696674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5218d4e5fa8450c7411955b9ba93511e93b2eacc878b57a8159a04a169191fa7`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 28 Jan 2021 23:38:31 GMT
ADD file:c0e9ea135d66ad6504c77915a7a48b3bead60892d155d3258b746cb4945981c0 in / 
# Thu, 28 Jan 2021 23:38:31 GMT
CMD ["/bin/sh"]
# Fri, 12 Feb 2021 02:40:53 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Fri, 12 Feb 2021 02:40:53 GMT
ENV HOME=/home/user
# Fri, 12 Feb 2021 02:40:54 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Fri, 12 Feb 2021 02:40:54 GMT
ENV LANG=C.UTF-8
# Fri, 12 Feb 2021 02:40:54 GMT
ENV IRSSI_VERSION=1.2.2
# Fri, 12 Feb 2021 02:41:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		automake 		coreutils 		dpkg-dev dpkg 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		make 		ncurses-dev 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-true-color 		--with-bot 		--with-proxy 		--with-socks 	; 	make -j "$(nproc)"; 	make install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Fri, 12 Feb 2021 02:41:54 GMT
WORKDIR /home/user
# Fri, 12 Feb 2021 02:41:54 GMT
USER user
# Fri, 12 Feb 2021 02:41:54 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3fea00a81341ce917db671eb3ad24ef5750cb6928b7f760e3ce4dab619eeb1fa`  
		Last Modified: Thu, 28 Jan 2021 23:39:02 GMT  
		Size: 2.8 MB (2817627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e2567f275f1580b3a666d72f9fd68f0624463b51d3efb4d0ca32220140480f`  
		Last Modified: Fri, 12 Feb 2021 02:42:19 GMT  
		Size: 8.9 MB (8912699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cf744978f6b257e75f0d9f8d485cc009c002a68fbfd09d2c86682e295a55ca`  
		Last Modified: Fri, 12 Feb 2021 02:42:15 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c24e57c1812de51612f3a7d46b191b5335b7aa8c7453d615fc0aa626654737`  
		Last Modified: Fri, 12 Feb 2021 02:42:22 GMT  
		Size: 6.0 MB (5965103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:d311dab78fc85b3da27d037bd147a456f46668231c4e1638a68791a6583803e9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18936606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d89ab620811ed1d73742b91c14b60c97ba0792d521e62ac8c2e60362356a222`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 28 Jan 2021 23:55:50 GMT
ADD file:b14fd5f3f7fcd16e2b4ec6932d3e9c07c7400c577cee5fdcb88b0795a70a7bfb in / 
# Thu, 28 Jan 2021 23:55:52 GMT
CMD ["/bin/sh"]
# Fri, 12 Feb 2021 02:22:51 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Fri, 12 Feb 2021 02:22:57 GMT
ENV HOME=/home/user
# Fri, 12 Feb 2021 02:23:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Fri, 12 Feb 2021 02:23:20 GMT
ENV LANG=C.UTF-8
# Fri, 12 Feb 2021 02:23:28 GMT
ENV IRSSI_VERSION=1.2.2
# Fri, 12 Feb 2021 02:24:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		automake 		coreutils 		dpkg-dev dpkg 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		make 		ncurses-dev 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-true-color 		--with-bot 		--with-proxy 		--with-socks 	; 	make -j "$(nproc)"; 	make install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Fri, 12 Feb 2021 02:24:38 GMT
WORKDIR /home/user
# Fri, 12 Feb 2021 02:24:41 GMT
USER user
# Fri, 12 Feb 2021 02:24:47 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f3b94a1d8d591af02f1b419642bee91066ecbb9c65099d6903deed310fd1c2ff`  
		Last Modified: Thu, 28 Jan 2021 23:56:32 GMT  
		Size: 2.8 MB (2812517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1350879e766a79b2700ba308c8723d6062ba50e73770b955b3c7eaa85d71f0c4`  
		Last Modified: Fri, 12 Feb 2021 02:25:16 GMT  
		Size: 9.6 MB (9642136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d400834332386f797f1b7d0efbb74ccf52781cf43800e6d216531c559034030`  
		Last Modified: Fri, 12 Feb 2021 02:25:14 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8df220e5e651e0e7237d472b3e06378faf13942fc99a530aeaf5a827cec8d3`  
		Last Modified: Fri, 12 Feb 2021 02:25:15 GMT  
		Size: 6.5 MB (6480679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:1bd143b42adb04426f451e5b62935c167f03b48fcf438fb5f04e632418893b68
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18849294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f129f13349018ff90ba92a29a67d281d6fb481ba679ef5e8cf346213d430469`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 28 Jan 2021 23:41:35 GMT
ADD file:d97e6c37df0fb8306b072d9c0a32f68f5aff583ba849303926644deacfa25eb9 in / 
# Thu, 28 Jan 2021 23:41:36 GMT
CMD ["/bin/sh"]
# Fri, 12 Feb 2021 02:43:53 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Fri, 12 Feb 2021 02:43:54 GMT
ENV HOME=/home/user
# Fri, 12 Feb 2021 02:43:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Fri, 12 Feb 2021 02:43:55 GMT
ENV LANG=C.UTF-8
# Fri, 12 Feb 2021 02:43:55 GMT
ENV IRSSI_VERSION=1.2.2
# Fri, 12 Feb 2021 02:44:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		automake 		coreutils 		dpkg-dev dpkg 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		make 		ncurses-dev 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-true-color 		--with-bot 		--with-proxy 		--with-socks 	; 	make -j "$(nproc)"; 	make install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Fri, 12 Feb 2021 02:44:31 GMT
WORKDIR /home/user
# Fri, 12 Feb 2021 02:44:31 GMT
USER user
# Fri, 12 Feb 2021 02:44:31 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:43901f1af0ef9db6b0bf30ac6f6dacd78bf1ecfeb47ad0a93aa2370fa8e62407`  
		Last Modified: Thu, 28 Jan 2021 23:42:09 GMT  
		Size: 2.6 MB (2602059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6828360093815c1589a6af17651b459c37cfc47b9251cb9bf6c4274c6113954`  
		Last Modified: Fri, 12 Feb 2021 02:44:50 GMT  
		Size: 10.0 MB (9983480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cce6436611d96d1810fbfd666eb399c0f4ff5d46923c12fc0e95e3852f8a0b18`  
		Last Modified: Fri, 12 Feb 2021 02:44:49 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b12ed13d4cf5c3d7d9df02e897ffe39a45ead31fe6bc3860beab89444cd80b`  
		Last Modified: Fri, 12 Feb 2021 02:44:49 GMT  
		Size: 6.3 MB (6262484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
