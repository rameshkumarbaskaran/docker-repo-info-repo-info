## `php:alpine3.16`

```console
$ docker pull php@sha256:f80f56b22ec4b8a7d87035417102cad9f53c30045f7cccabdeacf2c70e8489a4
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

### `php:alpine3.16` - linux; amd64

```console
$ docker pull php@sha256:5b33022be85d8c2e21e1de7014a21f4270da560b44c8276e0a65e179cbd465b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.6 MB (33552585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e76f082704950c4363e0fe6e6b0c22814f01480405b6cd157cc2a42f0d8dfb`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:36:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 12 Nov 2022 08:36:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 12 Nov 2022 08:36:57 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 12 Nov 2022 08:36:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 12 Nov 2022 08:36:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 12 Nov 2022 08:36:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 08:36:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 08:36:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 12 Nov 2022 08:36:58 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 08 Dec 2022 20:11:47 GMT
ENV PHP_VERSION=8.2.0
# Thu, 08 Dec 2022 20:11:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.0.tar.xz.asc
# Thu, 08 Dec 2022 20:11:47 GMT
ENV PHP_SHA256=6ea4c2dfb532950fd712aa2a08c1412a6a81cd1334dd0b0bf88a8e44c2b3a943
# Thu, 08 Dec 2022 20:11:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 08 Dec 2022 20:11:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 08 Dec 2022 20:15:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 08 Dec 2022 20:15:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 08 Dec 2022 20:15:54 GMT
RUN docker-php-ext-enable sodium
# Thu, 08 Dec 2022 20:15:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 Dec 2022 20:15:54 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b78b4fe0ca1ca5277d0b56997b3a74ac05ac52ff34cf9d5c6c063bd3feca07e`  
		Last Modified: Sat, 12 Nov 2022 09:30:31 GMT  
		Size: 1.7 MB (1721291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6040f2a28f7fd4288a87be2db7a8886104a1080402d0343e1c527c232d8963`  
		Last Modified: Sat, 12 Nov 2022 09:30:31 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2e66b89284d71ee13c90182fe35d46d2461573064ae7f020aa4c22c1235e2a`  
		Last Modified: Sat, 12 Nov 2022 09:30:31 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf66eb1b1eb46bc57249df883e96f1ee23f820097201b1bf0f940ad7816cc60`  
		Last Modified: Thu, 08 Dec 2022 20:33:10 GMT  
		Size: 11.9 MB (11940860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9af814762672ca92fd61ff5f940655a7c74507db4d3970582cdc33ecfe8093`  
		Last Modified: Thu, 08 Dec 2022 20:33:10 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286d6a7dc22edb4e41901006e607aa65f7a621016245c5ac84a1116ccf752b2d`  
		Last Modified: Thu, 08 Dec 2022 20:33:12 GMT  
		Size: 17.1 MB (17060787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4faf159ec2e065ffa086a8dc20b6931409a8e14ca08b839d30367881cfb9c5f`  
		Last Modified: Thu, 08 Dec 2022 20:33:09 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139c2e5d913644ed688ec2b7c20e1b15b28d65be31dbf4238fe5933fc66dc91a`  
		Last Modified: Thu, 08 Dec 2022 20:33:10 GMT  
		Size: 18.9 KB (18904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:alpine3.16` - linux; arm variant v6

```console
$ docker pull php@sha256:e8404b1a6bd5b5f82cce79c2cb42636b4ecc3c066dbcaa3e73006d6df6ac4ad7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32270994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c04433a8565304e6ad96e66154b36cb2df5a1d612cc692cb1c320983eb0b6d2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:54:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 12 Nov 2022 04:55:00 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 12 Nov 2022 04:55:01 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 12 Nov 2022 04:55:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 12 Nov 2022 04:55:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 12 Nov 2022 04:55:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 04:55:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 04:55:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 12 Nov 2022 04:55:02 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 06 Jan 2023 00:07:07 GMT
ENV PHP_VERSION=8.2.1
# Fri, 06 Jan 2023 00:07:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.1.tar.xz.asc
# Fri, 06 Jan 2023 00:07:07 GMT
ENV PHP_SHA256=650d3bd7a056cabf07f6a0f6f1dd8ba45cd369574bbeaa36de7d1ece212c17af
# Fri, 06 Jan 2023 00:07:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 06 Jan 2023 00:07:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:14:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Jan 2023 00:14:02 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:14:04 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Jan 2023 00:14:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Jan 2023 00:14:04 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:089b5ea696a25e03b2eaa2ba4c2d7ca2b161473cb9f1686ca8b9af4b714cc216`  
		Last Modified: Sat, 12 Nov 2022 05:51:25 GMT  
		Size: 1.7 MB (1708068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148c879de0e59a35d228a53d3c70813c09859b8647217f5bdf53e6b8058daa80`  
		Last Modified: Sat, 12 Nov 2022 05:51:24 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b9d16af9cd3acc95ea5a8da94a040a0f63b8af95a60a4ad30aaddbab836604`  
		Last Modified: Sat, 12 Nov 2022 05:51:24 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdae20e72eddcf9f2008cb181327c20256b2b6f3f5a489185e50c1b1d6441068`  
		Last Modified: Fri, 06 Jan 2023 01:22:35 GMT  
		Size: 12.1 MB (12052128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8439fbd3b23ff54fc00958bf2988e89a098bf7217b2b3db42a9450198bc00b3`  
		Last Modified: Fri, 06 Jan 2023 01:22:34 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21049a84abdd10cf40edc2b0e509a1fd9185f66f816e801602264c99e713c14c`  
		Last Modified: Fri, 06 Jan 2023 01:22:37 GMT  
		Size: 15.9 MB (15872534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ee735c47a89aaace710494cdddb69aa1555aa0a8d07d4d198e8487ed2867b3`  
		Last Modified: Fri, 06 Jan 2023 01:22:34 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8e285ada9cec7904e5f926b087bca49f6a63a52abb1bb8e00e0308851bc92a`  
		Last Modified: Fri, 06 Jan 2023 01:22:34 GMT  
		Size: 18.8 KB (18755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:alpine3.16` - linux; arm variant v7

```console
$ docker pull php@sha256:54384db8feca80ae08efdb35d0209dee2d7deb30c769b94154e19c731561ebda
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30909337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fe549dafa9005b762bdab21920d342ffa3a34b113c074610a03e455b6cee16`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Sat, 12 Nov 2022 03:57:24 GMT
ADD file:0b4a628f529226f5ec9d357ca63138bd2d22411a889c780ac8d395d761e07b2c in / 
# Sat, 12 Nov 2022 03:57:24 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:47:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 12 Nov 2022 05:47:35 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 12 Nov 2022 05:47:35 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 12 Nov 2022 05:47:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 12 Nov 2022 05:47:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 12 Nov 2022 05:47:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 05:47:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 05:47:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 12 Nov 2022 05:47:36 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 05 Jan 2023 23:29:50 GMT
ENV PHP_VERSION=8.2.1
# Thu, 05 Jan 2023 23:29:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.1.tar.xz.asc
# Thu, 05 Jan 2023 23:29:51 GMT
ENV PHP_SHA256=650d3bd7a056cabf07f6a0f6f1dd8ba45cd369574bbeaa36de7d1ece212c17af
# Thu, 05 Jan 2023 23:29:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 05 Jan 2023 23:29:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 05 Jan 2023 23:33:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 05 Jan 2023 23:33:06 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 05 Jan 2023 23:33:07 GMT
RUN docker-php-ext-enable sodium
# Thu, 05 Jan 2023 23:33:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Jan 2023 23:33:07 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:e44ba29d168a7f7c9e914f3724614df9e070aa6ef9b9ba5c9004db3c071f403a`  
		Last Modified: Sat, 12 Nov 2022 03:58:16 GMT  
		Size: 2.4 MB (2418788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525864ff6d6c3a1a9ca039e0999c8d05701858671326bac7253a25aa21de91b9`  
		Last Modified: Sat, 12 Nov 2022 06:53:18 GMT  
		Size: 1.6 MB (1575444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09a62104a768e3175677dcac32aa6ba859b0b7917b110ff8fdda7c64447d13f`  
		Last Modified: Sat, 12 Nov 2022 06:53:17 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd62154db22fa402fe200d63a35937ed4a35c102677a20c24eff0fca7ad7981d`  
		Last Modified: Sat, 12 Nov 2022 06:53:17 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64aef6ebf650b7253d8dde7d0d2b07bb1d0dff74b170223290dc5f0bafd30444`  
		Last Modified: Fri, 06 Jan 2023 01:45:00 GMT  
		Size: 12.1 MB (12052121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f4283655a51d9ef9dd78dfd1306cf718f8f35ae5a5fbcea32305ad9b07eee8`  
		Last Modified: Fri, 06 Jan 2023 01:44:59 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a91ecf3bfb62b2b9ba5921b75e7cdd1ea9067663f8e986f02da78d9ae53d1ab`  
		Last Modified: Fri, 06 Jan 2023 01:45:02 GMT  
		Size: 14.8 MB (14839847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc0c8b1398eb0988cb7573a80f4efadfecc852281bd11de9f743c5e71b0f231`  
		Last Modified: Fri, 06 Jan 2023 01:44:59 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccca0e38682274a30db350c4a3349ed7b3e226a76cfa20e975b13bbe438a6514`  
		Last Modified: Fri, 06 Jan 2023 01:44:59 GMT  
		Size: 18.7 KB (18739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:alpine3.16` - linux; arm64 variant v8

```console
$ docker pull php@sha256:45e0b99442ff7cf3dd15e0d0c92a901d64a07b395878c19d33b057a56cfa8b81
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33456677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d7eb263ab0f97b61802b1ede6da32f5a9a5c8a6707d11bfc06553741c57fe0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:37:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 12 Nov 2022 04:38:00 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 12 Nov 2022 04:38:00 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 12 Nov 2022 04:38:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 12 Nov 2022 04:38:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 12 Nov 2022 04:38:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 04:38:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 04:38:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 12 Nov 2022 04:38:01 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 08 Dec 2022 19:26:59 GMT
ENV PHP_VERSION=8.2.0
# Thu, 08 Dec 2022 19:26:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.0.tar.xz.asc
# Thu, 08 Dec 2022 19:26:59 GMT
ENV PHP_SHA256=6ea4c2dfb532950fd712aa2a08c1412a6a81cd1334dd0b0bf88a8e44c2b3a943
# Thu, 08 Dec 2022 19:27:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 08 Dec 2022 19:27:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 08 Dec 2022 19:30:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 08 Dec 2022 19:30:58 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 08 Dec 2022 19:30:59 GMT
RUN docker-php-ext-enable sodium
# Thu, 08 Dec 2022 19:30:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 Dec 2022 19:30:59 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d018a6b8f2b9d3c88bb51b66bb27c7840ca587dc27d7b18ed9d29271f7a801`  
		Last Modified: Sat, 12 Nov 2022 05:25:21 GMT  
		Size: 1.7 MB (1715697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd698c26bd17e47cae3e287202cee1112230b8c1e3b6eff40ab1c13d26737998`  
		Last Modified: Sat, 12 Nov 2022 05:25:21 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d804918576056f288bba1c63c140494fb4cfd8c845d79c029e38fba1f5665ee`  
		Last Modified: Sat, 12 Nov 2022 05:25:21 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db29c31a9ac855157a44d2fc46dc53c4cf5611637324c84d41d5ef26e5a065c5`  
		Last Modified: Thu, 08 Dec 2022 19:48:07 GMT  
		Size: 11.9 MB (11940873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:357917aa5b45ead2147f5a640adf7b77dc506b0d218ab5ebba26b680462c69da`  
		Last Modified: Thu, 08 Dec 2022 19:48:07 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2d8a2435120a65a6a67a1984a705eb78a91e19fe42e011b9f0d4c992d0cda25`  
		Last Modified: Thu, 08 Dec 2022 19:48:09 GMT  
		Size: 17.1 MB (17069169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3f02980385029679cfc964309d2aa546afd536f95ab7dccc4bd8076804fb2f`  
		Last Modified: Thu, 08 Dec 2022 19:48:07 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7587fb0f9532beff5033664897236eef45fbcead43f0a61e04ccee111376d74b`  
		Last Modified: Thu, 08 Dec 2022 19:48:07 GMT  
		Size: 18.7 KB (18709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:alpine3.16` - linux; 386

```console
$ docker pull php@sha256:d2df7b867c1a038b8673e5f2cd03fb8b39339a730860ffd9a7304e878f2cfd00
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34057227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18fc0cf4ed81d2ef01cfce0cf92935adb7565de78ed7c6a8ba71dee3932a39b0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Sat, 12 Nov 2022 03:38:23 GMT
ADD file:561637cbdd23fdd69f555dbc938902d79be2b123eb244d2cfd35b337878b63df in / 
# Sat, 12 Nov 2022 03:38:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:08:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 12 Nov 2022 08:08:30 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 12 Nov 2022 08:08:31 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 12 Nov 2022 08:08:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 12 Nov 2022 08:08:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 12 Nov 2022 08:08:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 08:08:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 08:08:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 12 Nov 2022 08:08:37 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 08 Dec 2022 19:23:35 GMT
ENV PHP_VERSION=8.2.0
# Thu, 08 Dec 2022 19:23:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.0.tar.xz.asc
# Thu, 08 Dec 2022 19:23:37 GMT
ENV PHP_SHA256=6ea4c2dfb532950fd712aa2a08c1412a6a81cd1334dd0b0bf88a8e44c2b3a943
# Thu, 08 Dec 2022 19:23:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 08 Dec 2022 19:23:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 08 Dec 2022 19:27:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 08 Dec 2022 19:27:44 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 08 Dec 2022 19:27:44 GMT
RUN docker-php-ext-enable sodium
# Thu, 08 Dec 2022 19:27:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 Dec 2022 19:27:46 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:0c10ccf9426f4a034c81b9e1a0fa81fc5cd957d8a4e0ea545ee33f4cd59f227b`  
		Last Modified: Sat, 12 Nov 2022 03:39:07 GMT  
		Size: 2.8 MB (2808348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529c1276f7fbbfab5754449ae3db2b4a04a98af1d706770d02ddb1654a806e5e`  
		Last Modified: Sat, 12 Nov 2022 09:10:33 GMT  
		Size: 1.8 MB (1820471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5a372dd65c07f12bc395d2ea0e1266225dc55c9a1673efe9894a022f00e41d`  
		Last Modified: Sat, 12 Nov 2022 09:10:32 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839f3c42dc99fde076c817b954f4cc26d21c68b993eedfc6e5a5428d4b49c393`  
		Last Modified: Sat, 12 Nov 2022 09:10:32 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c5e5b723e0112f5c5ccff4755ede88767e04d00438fe643696107941e52c64`  
		Last Modified: Thu, 08 Dec 2022 19:50:36 GMT  
		Size: 11.9 MB (11940624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b459d156d7712d2ccfb7c74b05bf9d5af67585e3906b449b1839e26d2a633c4c`  
		Last Modified: Thu, 08 Dec 2022 19:50:34 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cdfc4a5ca32676331eefd726df63cb98f99845cf1b3440d02b3b847840e06b8`  
		Last Modified: Thu, 08 Dec 2022 19:50:37 GMT  
		Size: 17.5 MB (17464570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0160b0872d92af92961b1dd8d91493d295cfec42e0803d93bcc5ca4b4ba886a`  
		Last Modified: Thu, 08 Dec 2022 19:50:34 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ee8b21720c713c40de3d7ccf4c62f2cc9795c494e10d443f6c3bba0f004fa9`  
		Last Modified: Thu, 08 Dec 2022 19:50:34 GMT  
		Size: 18.8 KB (18816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:alpine3.16` - linux; ppc64le

```console
$ docker pull php@sha256:71b8d30d597ad3bef9af65d5a64ebb7993d93e11ca7a14ebcaa0e907a77fd9e5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.9 MB (34860149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9832aba78a04ef18b6aa4ae4f03261018481148915848ccad620faaf67147d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Sat, 12 Nov 2022 04:16:30 GMT
ADD file:6f7965319fe0caaea57086835c0c2212284c6850f33e3c4d522c758e43acbc98 in / 
# Sat, 12 Nov 2022 04:16:31 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 07:14:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 12 Nov 2022 07:14:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 12 Nov 2022 07:14:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 12 Nov 2022 07:14:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 12 Nov 2022 07:14:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 12 Nov 2022 07:14:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 07:14:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 07:14:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 12 Nov 2022 07:14:35 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 05 Jan 2023 23:46:45 GMT
ENV PHP_VERSION=8.2.1
# Thu, 05 Jan 2023 23:46:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.1.tar.xz.asc
# Thu, 05 Jan 2023 23:46:46 GMT
ENV PHP_SHA256=650d3bd7a056cabf07f6a0f6f1dd8ba45cd369574bbeaa36de7d1ece212c17af
# Thu, 05 Jan 2023 23:46:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 05 Jan 2023 23:46:57 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 05 Jan 2023 23:52:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 05 Jan 2023 23:52:08 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 05 Jan 2023 23:52:09 GMT
RUN docker-php-ext-enable sodium
# Thu, 05 Jan 2023 23:52:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Jan 2023 23:52:10 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:5c3a6ece62351976dfb4b56dc417aebd2a7dbda14ebac2737edd2ab43883553f`  
		Last Modified: Sat, 12 Nov 2022 04:17:14 GMT  
		Size: 2.8 MB (2801551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194dd51b13c32835b9a76fe58f7580e66a1df8a2acea27095b556cf63b31a98`  
		Last Modified: Sat, 12 Nov 2022 08:27:35 GMT  
		Size: 1.8 MB (1772559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e966c695081973df431189ce4bf6ed44556dad53c642dfb26fa5c0df97e5a7`  
		Last Modified: Sat, 12 Nov 2022 08:27:35 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdd33a80e474697f7ae3aeeba872662ed64ab312628cb4eaf63bd9cefb1b5a3`  
		Last Modified: Sat, 12 Nov 2022 08:27:35 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f9e2b76cc410dce78a77dbe5768195af26e8fc500791158b4fca2f5cb2083e`  
		Last Modified: Fri, 06 Jan 2023 01:30:37 GMT  
		Size: 12.1 MB (12052146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f9e3ef32a2fadf9011561fa2177f0a37385414cc18f4982432496873ffdaf1`  
		Last Modified: Fri, 06 Jan 2023 01:30:36 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3279f253c1c7a1420ed43f63d13a9d2b486cbe49a97b652b5f822f0413356be`  
		Last Modified: Fri, 06 Jan 2023 01:30:42 GMT  
		Size: 18.2 MB (18210678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f245842c924f1ae1f43befb85760bc5487857067896eb31526bd6124c4bb18`  
		Last Modified: Fri, 06 Jan 2023 01:30:36 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da481ed30d6b8930d1a65e14c6c304b55a7a5d877f8b2d216797e1b06ef6714a`  
		Last Modified: Fri, 06 Jan 2023 01:30:36 GMT  
		Size: 18.7 KB (18744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:alpine3.16` - linux; s390x

```console
$ docker pull php@sha256:d1618123aef027f24695feade9469f70b3e1b7e0eb219cf350621f849eadc406
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32350983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d8f2d8c26c0d6ed15b7fc63474f1d60581f73446c47efa8e97a53d20dfd360`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Sat, 12 Nov 2022 03:42:05 GMT
ADD file:b78ae95cbacd853e398f187adaf3be51d9e301a66de8f7a4b6c60a9733075cb5 in / 
# Sat, 12 Nov 2022 03:42:06 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:31:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 12 Nov 2022 05:31:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 12 Nov 2022 05:31:46 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 12 Nov 2022 05:31:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 12 Nov 2022 05:31:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 12 Nov 2022 05:31:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 05:31:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 05:31:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 12 Nov 2022 05:31:49 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 08 Dec 2022 19:33:00 GMT
ENV PHP_VERSION=8.2.0
# Thu, 08 Dec 2022 19:33:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.0.tar.xz.asc
# Thu, 08 Dec 2022 19:33:01 GMT
ENV PHP_SHA256=6ea4c2dfb532950fd712aa2a08c1412a6a81cd1334dd0b0bf88a8e44c2b3a943
# Thu, 08 Dec 2022 19:33:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 08 Dec 2022 19:33:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 08 Dec 2022 19:39:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 08 Dec 2022 19:39:18 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 08 Dec 2022 19:39:21 GMT
RUN docker-php-ext-enable sodium
# Thu, 08 Dec 2022 19:39:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 Dec 2022 19:39:22 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:cff16a5ffe2df97bc1d10b021c5ceb98bdb36a18a1d70395590444ac204a9b2b`  
		Last Modified: Sat, 12 Nov 2022 03:43:06 GMT  
		Size: 2.6 MB (2591126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d900dcf97f987ab1cb475ea526ac6e9c9784703d1e1be1cd7ae1fb777a7d94`  
		Last Modified: Sat, 12 Nov 2022 06:29:44 GMT  
		Size: 1.8 MB (1776146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0442afc535a74897e967e16b9e816dd275e3f0af102e3215ad2e35350d268d`  
		Last Modified: Sat, 12 Nov 2022 06:29:44 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3645d9671ef8df3e3310d7ba31ed1e48aa39751f695906393ad5b64366d9f5ee`  
		Last Modified: Sat, 12 Nov 2022 06:29:44 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe7c524f95abec0a4a22d7543cb7985e8019321dcbd31c59a40b7d3cdf8dd3c`  
		Last Modified: Thu, 08 Dec 2022 20:03:57 GMT  
		Size: 11.9 MB (11940866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3634d8a6e99d38e121e1c70c028d235849db04a3abc6ba1048d966b05beed1e0`  
		Last Modified: Thu, 08 Dec 2022 20:03:56 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b635f300da649afe0c10d47a1f4160f41f023c85ee8c7f4b9825fb92a37b8a83`  
		Last Modified: Thu, 08 Dec 2022 20:03:59 GMT  
		Size: 16.0 MB (16019662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b4865d99ec53c2731aa124fe61d4ab8f9cff2a352479514100bd22d2481f8c`  
		Last Modified: Thu, 08 Dec 2022 20:03:57 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb62d80bc12169127666f81f0a5f505e3a98f000082b8eabfd0a934ead31ecf1`  
		Last Modified: Thu, 08 Dec 2022 20:03:56 GMT  
		Size: 18.7 KB (18707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
