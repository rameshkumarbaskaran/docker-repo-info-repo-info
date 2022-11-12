## `irssi:1-alpine`

```console
$ docker pull irssi@sha256:1c8992670520882aa3a4d4ae4a4385fde820cc026cfe57de91629cad9ec6e0e9
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
$ docker pull irssi@sha256:a138fb7c5a7f29b97595c3d1931ed165b004eb1ed20071f2216568b9516063c8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17471136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e788de2b86e371837a5e85fe4b38024c00678c723a9fb4310529c309ff1d4c32`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 22:46:20 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Thu, 06 Oct 2022 22:46:20 GMT
ENV HOME=/home/user
# Thu, 06 Oct 2022 22:46:21 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Thu, 06 Oct 2022 22:46:21 GMT
ENV LANG=C.UTF-8
# Mon, 31 Oct 2022 19:28:01 GMT
ENV IRSSI_VERSION=1.4.3
# Mon, 31 Oct 2022 19:28:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 31 Oct 2022 19:28:23 GMT
WORKDIR /home/user
# Mon, 31 Oct 2022 19:28:23 GMT
USER user
# Mon, 31 Oct 2022 19:28:23 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ff79af72bb12b49e71f6508ebe4aa9b7ba12e5c1c2037f0953067fcc50546d`  
		Last Modified: Thu, 06 Oct 2022 22:47:00 GMT  
		Size: 9.6 MB (9641364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11abf0b311aa35dce58e3aa729ed8b52ce47c211c776e639f37cd3e2ed7f41fd`  
		Last Modified: Thu, 06 Oct 2022 22:46:58 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a698d457dc10eb85ac57f79cf84d647959077776acd831b726973ad89b84b281`  
		Last Modified: Mon, 31 Oct 2022 19:28:56 GMT  
		Size: 5.0 MB (5022433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:ecc5f927cd20f5330db531743d004cb7099ecae61d09324a915d75d961032a81
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16401963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4554dafe8b24e9676c91549f8d437f0fcaa58fab6e376fba8917d2d04f1bb031`
-	Default Command: `["irssi"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:32:43 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Sat, 12 Nov 2022 04:32:43 GMT
ENV HOME=/home/user
# Sat, 12 Nov 2022 04:32:44 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Sat, 12 Nov 2022 04:32:44 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 04:32:44 GMT
ENV IRSSI_VERSION=1.4.3
# Sat, 12 Nov 2022 04:33:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Sat, 12 Nov 2022 04:33:06 GMT
WORKDIR /home/user
# Sat, 12 Nov 2022 04:33:06 GMT
USER user
# Sat, 12 Nov 2022 04:33:06 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5f135cffa9ea64772b3fc0464ebd47b24e26250a3c3ee5e42fbe21939ddb4d`  
		Last Modified: Sat, 12 Nov 2022 04:33:31 GMT  
		Size: 8.9 MB (8871396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226660f18be5a45f39079200003d496e45b9fbe6c74778e86beb3a4af5794bb1`  
		Last Modified: Sat, 12 Nov 2022 04:33:29 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b56de36739d5fc75692c7f843588862f83eed75ecfd3d2987818ab1f73b5e2`  
		Last Modified: Sat, 12 Nov 2022 04:33:30 GMT  
		Size: 4.9 MB (4914204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:7350968cbef0bd34629cfd329492b6b988af1d9cc45ba81637f32f96e3baeca8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15831159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63554d137896f0aa62a4f1d83e2bf5a88a13c92e5738da94976c71ff0957f0c1`
-	Default Command: `["irssi"]`

```dockerfile
# Sat, 12 Nov 2022 03:57:24 GMT
ADD file:0b4a628f529226f5ec9d357ca63138bd2d22411a889c780ac8d395d761e07b2c in / 
# Sat, 12 Nov 2022 03:57:24 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:50:31 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Sat, 12 Nov 2022 04:50:31 GMT
ENV HOME=/home/user
# Sat, 12 Nov 2022 04:50:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Sat, 12 Nov 2022 04:50:32 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 04:50:32 GMT
ENV IRSSI_VERSION=1.4.3
# Sat, 12 Nov 2022 04:50:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Sat, 12 Nov 2022 04:50:52 GMT
WORKDIR /home/user
# Sat, 12 Nov 2022 04:50:52 GMT
USER user
# Sat, 12 Nov 2022 04:50:52 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e44ba29d168a7f7c9e914f3724614df9e070aa6ef9b9ba5c9004db3c071f403a`  
		Last Modified: Sat, 12 Nov 2022 03:58:16 GMT  
		Size: 2.4 MB (2418788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0c59eea215ab5434ff08bbf56ca21875e09e56636bf26b6ef7f3628b433d72`  
		Last Modified: Sat, 12 Nov 2022 04:51:27 GMT  
		Size: 8.7 MB (8718211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b6b796de9465eb6db58061a60b92109ecc2e46627bfcebf39830ae9044ba0d`  
		Last Modified: Sat, 12 Nov 2022 04:51:25 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1beff4ffe11f80a05bb3b4691b7550bb1013c72d3764ff16375437a7fea6ed`  
		Last Modified: Sat, 12 Nov 2022 04:51:26 GMT  
		Size: 4.7 MB (4692901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0a3995c5d6da11692151b211500ab9a0f8849bce9b2949f176a76598972a2107
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19121465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df690d3b92a469a8d30921af1d7aa578138a2d885829ba157875904b34a35f02`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Thu, 10 Nov 2022 20:39:41 GMT
CMD ["/bin/sh"]
# Thu, 10 Nov 2022 21:44:20 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Thu, 10 Nov 2022 21:44:20 GMT
ENV HOME=/home/user
# Thu, 10 Nov 2022 21:44:21 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Thu, 10 Nov 2022 21:44:21 GMT
ENV LANG=C.UTF-8
# Thu, 10 Nov 2022 21:44:21 GMT
ENV IRSSI_VERSION=1.4.3
# Thu, 10 Nov 2022 21:44:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Thu, 10 Nov 2022 21:44:35 GMT
WORKDIR /home/user
# Thu, 10 Nov 2022 21:44:35 GMT
USER user
# Thu, 10 Nov 2022 21:44:35 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2507a840456a8ee30e0beabc3e0fd3340b042b0e078d3a8ec51cd66d03c4ae66`  
		Last Modified: Thu, 10 Nov 2022 21:44:55 GMT  
		Size: 9.6 MB (9623582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28552c93fd99f72724a9ee9c771082127246b2eb389069b484444fcdc8ebbfa2`  
		Last Modified: Thu, 10 Nov 2022 21:44:54 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be69c0427773c855e3c10bc29efec558598d8d4a51390f0881bcf3506b947b05`  
		Last Modified: Thu, 10 Nov 2022 21:44:54 GMT  
		Size: 6.8 MB (6788935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1-alpine` - linux; 386

```console
$ docker pull irssi@sha256:1c3f0f7f74a1c7a2d3f058cee1bd0ed3c3c8f10ab1b24951e9444e59c937ca48
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16911093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6c61e02f929ef713e587b403d9af3c3b707e569aebbc22ac932f9f818e6026`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:29:42 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Thu, 06 Oct 2022 20:29:43 GMT
ENV HOME=/home/user
# Thu, 06 Oct 2022 20:29:44 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Thu, 06 Oct 2022 20:29:45 GMT
ENV LANG=C.UTF-8
# Mon, 31 Oct 2022 19:39:22 GMT
ENV IRSSI_VERSION=1.4.3
# Mon, 31 Oct 2022 19:39:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 31 Oct 2022 19:39:44 GMT
WORKDIR /home/user
# Mon, 31 Oct 2022 19:39:45 GMT
USER user
# Mon, 31 Oct 2022 19:39:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6998e76f864cbaf06e7debbc8cc223f98c373cb95b806cfe44aca74812c27568`  
		Last Modified: Thu, 06 Oct 2022 20:30:40 GMT  
		Size: 9.0 MB (9003050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3b2d0f1f5305fc69e974d644c6d4eb9805269f1617bdb0f4f866bcce3d175e`  
		Last Modified: Thu, 06 Oct 2022 20:30:39 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c0fac54e9da775128723c744e0d0e07a343ff9c89bb65dc8252eea11653564`  
		Last Modified: Mon, 31 Oct 2022 19:40:32 GMT  
		Size: 5.1 MB (5099662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:5aefaa4807981c39268ea065d43d27dbc2aee4d7a61deab03508bb85b5e15281
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17652597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaeef271e1d8b48a38c45072075a8b4f5cb24e1bc70d3c09df9b3ccf08e5cf0f`
-	Default Command: `["irssi"]`

```dockerfile
# Sat, 12 Nov 2022 04:16:30 GMT
ADD file:6f7965319fe0caaea57086835c0c2212284c6850f33e3c4d522c758e43acbc98 in / 
# Sat, 12 Nov 2022 04:16:31 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:14:23 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Sat, 12 Nov 2022 05:14:24 GMT
ENV HOME=/home/user
# Sat, 12 Nov 2022 05:14:26 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Sat, 12 Nov 2022 05:14:26 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 05:14:27 GMT
ENV IRSSI_VERSION=1.4.3
# Sat, 12 Nov 2022 05:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Sat, 12 Nov 2022 05:14:55 GMT
WORKDIR /home/user
# Sat, 12 Nov 2022 05:14:56 GMT
USER user
# Sat, 12 Nov 2022 05:14:56 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5c3a6ece62351976dfb4b56dc417aebd2a7dbda14ebac2737edd2ab43883553f`  
		Last Modified: Sat, 12 Nov 2022 04:17:14 GMT  
		Size: 2.8 MB (2801551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308b2aae03f822a5d6e07ef807dee55cb4ddce272eaa1e19d755e3cadd32d2c8`  
		Last Modified: Sat, 12 Nov 2022 05:15:31 GMT  
		Size: 9.7 MB (9733979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1dcdba578ab0a07b7e7a763c869c8943a62397cc648aaf6b98a19c20d8f024`  
		Last Modified: Sat, 12 Nov 2022 05:15:28 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e7ed154f2df94832294cd3b1f2f674171b0785f756233ab3b5b3d31e65c93c`  
		Last Modified: Sat, 12 Nov 2022 05:15:29 GMT  
		Size: 5.1 MB (5115784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:e4eb7d05828c6196b6d7804b89a3fc23bbe6f2b71a94c6fd33828cdd14730792
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17701838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2983fc02ed7fba551695b8cee2736ae0f49a72b9cb7d979c91ee11b4449c6c49`
-	Default Command: `["irssi"]`

```dockerfile
# Sat, 12 Nov 2022 03:42:05 GMT
ADD file:b78ae95cbacd853e398f187adaf3be51d9e301a66de8f7a4b6c60a9733075cb5 in / 
# Sat, 12 Nov 2022 03:42:06 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:27:18 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Sat, 12 Nov 2022 05:27:19 GMT
ENV HOME=/home/user
# Sat, 12 Nov 2022 05:27:20 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Sat, 12 Nov 2022 05:27:20 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 05:27:20 GMT
ENV IRSSI_VERSION=1.4.3
# Sat, 12 Nov 2022 05:27:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Sat, 12 Nov 2022 05:27:48 GMT
WORKDIR /home/user
# Sat, 12 Nov 2022 05:27:48 GMT
USER user
# Sat, 12 Nov 2022 05:27:49 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cff16a5ffe2df97bc1d10b021c5ceb98bdb36a18a1d70395590444ac204a9b2b`  
		Last Modified: Sat, 12 Nov 2022 03:43:06 GMT  
		Size: 2.6 MB (2591126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d1ccff4022f2d17884620efdd1ceeabf75e0b076a47eabb657f35b66b4ccdd`  
		Last Modified: Sat, 12 Nov 2022 05:28:28 GMT  
		Size: 10.1 MB (10079024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac443591d55c542b71137136de959b450b5709fa34803912c66917447df14d4`  
		Last Modified: Sat, 12 Nov 2022 05:28:26 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36fe48acef9ac0082e1aef9b649360656c15818a75aea885876ed76f6878ba3f`  
		Last Modified: Sat, 12 Nov 2022 05:28:26 GMT  
		Size: 5.0 MB (5030405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
