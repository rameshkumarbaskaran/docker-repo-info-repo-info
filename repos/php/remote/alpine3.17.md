## `php:alpine3.17`

```console
$ docker pull php@sha256:adf662c8faff8798ac76e30e5cf9bfc2cd5a595e68395dc088b9cd1472948621
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

### `php:alpine3.17` - linux; amd64

```console
$ docker pull php@sha256:322cf41cacb3e13d0a16f842219d9b412e6933663ed6f9efefd3257cfc89643d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34086699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83b404a99bac563ac8f064e0240152cec8562a4c81a994d75ea66cd38fe31a6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 22 Nov 2022 22:19:28 GMT
ADD file:587cae71969871d3c6456d844a8795df9b64b12c710c275295a1182b46f630e7 in / 
# Tue, 22 Nov 2022 22:19:29 GMT
CMD ["/bin/sh"]
# Wed, 30 Nov 2022 21:39:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 30 Nov 2022 21:39:10 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 30 Nov 2022 21:39:10 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 30 Nov 2022 21:39:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 30 Nov 2022 21:39:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 30 Nov 2022 21:39:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 30 Nov 2022 21:39:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 30 Nov 2022 21:39:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 30 Nov 2022 21:39:12 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 08 Dec 2022 20:00:07 GMT
ENV PHP_VERSION=8.2.0
# Thu, 08 Dec 2022 20:00:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.0.tar.xz.asc
# Thu, 08 Dec 2022 20:00:07 GMT
ENV PHP_SHA256=6ea4c2dfb532950fd712aa2a08c1412a6a81cd1334dd0b0bf88a8e44c2b3a943
# Thu, 08 Dec 2022 20:00:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 08 Dec 2022 20:00:15 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 08 Dec 2022 20:03:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 08 Dec 2022 20:03:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 08 Dec 2022 20:03:54 GMT
RUN docker-php-ext-enable sodium
# Thu, 08 Dec 2022 20:03:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 Dec 2022 20:03:54 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:c158987b05517b6f2c5913f3acef1f2182a32345a304fe357e3ace5fadcad715`  
		Last Modified: Tue, 22 Nov 2022 22:19:52 GMT  
		Size: 3.4 MB (3370706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b6029f6920d234861e6cee7ca87a1840de19c6049c86038f1fb9432e32ea6d`  
		Last Modified: Wed, 30 Nov 2022 22:06:19 GMT  
		Size: 1.9 MB (1864199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55761811b31b62dd8f7c87e712cac077dacc6a20312b0e2a382c9bdb8315777c`  
		Last Modified: Wed, 30 Nov 2022 22:06:19 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750fd99fe831a06b99ef6e82d1c1be04f9bf478c24ea2d52d63ac918c90df13`  
		Last Modified: Wed, 30 Nov 2022 22:06:19 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922c6c40febb16b54f8910bf1c45d60099f645e84afde597c7d39f96f9bd1ec4`  
		Last Modified: Thu, 08 Dec 2022 20:31:40 GMT  
		Size: 11.9 MB (11940895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02e22042c3b569d97ae70d00803c6112e3afacb7b20668463d6ff4dd5445994`  
		Last Modified: Thu, 08 Dec 2022 20:31:39 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f194fa5612abe7b2ee88fae5264f7b220b7d40151f1875d23679b790d32244`  
		Last Modified: Thu, 08 Dec 2022 20:31:42 GMT  
		Size: 16.9 MB (16887424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f70f6f3726f1a5727d9c63832c1f7e164862204dc58bbcd1a78ffba5a75c4a`  
		Last Modified: Thu, 08 Dec 2022 20:31:39 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3076216702727dbcf8042587729f21caa6f159451347e492dfd75b20bf615af5`  
		Last Modified: Thu, 08 Dec 2022 20:31:39 GMT  
		Size: 19.0 KB (19004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:alpine3.17` - linux; arm variant v6

```console
$ docker pull php@sha256:37dd9cd9f05c986c046b517d44bc616e5a4c1d88ac1dd308f4f674bfabd461e7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32295912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3822ca773d7f3df53916ad3a0245d612ef3fe4c3eba5887ad22116a0f1a7b98d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 22 Nov 2022 22:55:46 GMT
ADD file:132c76d7f7dae2f51f589ee460f1870a2cec6e9dc7ff8e38e88fcee2cfbe70da in / 
# Tue, 22 Nov 2022 22:55:46 GMT
CMD ["/bin/sh"]
# Wed, 30 Nov 2022 21:31:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 30 Nov 2022 21:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 30 Nov 2022 21:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 30 Nov 2022 21:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 30 Nov 2022 21:31:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 30 Nov 2022 21:31:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 30 Nov 2022 21:31:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 30 Nov 2022 21:31:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 30 Nov 2022 21:31:04 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 08 Dec 2022 18:52:34 GMT
ENV PHP_VERSION=8.2.0
# Thu, 08 Dec 2022 18:52:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.0.tar.xz.asc
# Thu, 08 Dec 2022 18:52:34 GMT
ENV PHP_SHA256=6ea4c2dfb532950fd712aa2a08c1412a6a81cd1334dd0b0bf88a8e44c2b3a943
# Thu, 08 Dec 2022 18:52:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 08 Dec 2022 18:52:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 08 Dec 2022 18:55:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 08 Dec 2022 18:55:49 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 08 Dec 2022 18:55:50 GMT
RUN docker-php-ext-enable sodium
# Thu, 08 Dec 2022 18:55:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 Dec 2022 18:55:50 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:c2eb4db52fbe1266a78d8c185d33544a2916faa7d82fb5f50909fe233e0579da`  
		Last Modified: Tue, 22 Nov 2022 22:56:39 GMT  
		Size: 3.1 MB (3107138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519fe767bb0c7928a1dbb3eed5885ac27b686566653a40e08b8377c7efeb5965`  
		Last Modified: Wed, 30 Nov 2022 22:00:41 GMT  
		Size: 1.8 MB (1848421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d73d4fd50e3aae901afb655f4fb90048c5f350001b4d52bb8d1bc50424c93a`  
		Last Modified: Wed, 30 Nov 2022 22:00:41 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c342b7908a6480c9e4c98966c37148ce29d0f29d1ceabe2775acbbf4e4dd0698`  
		Last Modified: Wed, 30 Nov 2022 22:00:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0243115affd6a1d29f7c5f33a52b99af343aca9a83157e92f97be02335e795e`  
		Last Modified: Thu, 08 Dec 2022 19:23:33 GMT  
		Size: 11.9 MB (11940853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f810ffe674b44dc199c0ed6372180967330c0215ffec7292dbeea0c7e99be91`  
		Last Modified: Thu, 08 Dec 2022 19:23:31 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a332fc5db093c7b96daa70eead0907ecb17bdeb991ec53aebeb291d2644fee`  
		Last Modified: Thu, 08 Dec 2022 19:23:35 GMT  
		Size: 15.4 MB (15376336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042fe5f658b27caa759cc327c929da3309b19d245a07ba43596c2b215dfcbcd7`  
		Last Modified: Thu, 08 Dec 2022 19:23:31 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d47ce873c3209fc4a25797af2614728677c9ab7356faab4137bff24e5efc4eb`  
		Last Modified: Thu, 08 Dec 2022 19:23:32 GMT  
		Size: 18.8 KB (18768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:alpine3.17` - linux; arm variant v7

```console
$ docker pull php@sha256:230cef9ddec5638a32a1fbc62321b70ddb49a2f51cdf67069b5f3d457058acb1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30938027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c128761e9f6f0babf0a112880f830689cf3c59552d3fbda20840b53f821d4a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 22 Nov 2022 22:57:20 GMT
ADD file:080010d9005e8e0dae3e98c7f9afff3e3a40ed32579ca01946efc6ede8316bad in / 
# Tue, 22 Nov 2022 22:57:20 GMT
CMD ["/bin/sh"]
# Wed, 30 Nov 2022 21:47:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 30 Nov 2022 21:47:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 30 Nov 2022 21:47:29 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 30 Nov 2022 21:47:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 30 Nov 2022 21:47:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 30 Nov 2022 21:47:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 30 Nov 2022 21:47:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 30 Nov 2022 21:47:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 30 Nov 2022 21:47:30 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 08 Dec 2022 19:36:18 GMT
ENV PHP_VERSION=8.2.0
# Thu, 08 Dec 2022 19:36:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.0.tar.xz.asc
# Thu, 08 Dec 2022 19:36:19 GMT
ENV PHP_SHA256=6ea4c2dfb532950fd712aa2a08c1412a6a81cd1334dd0b0bf88a8e44c2b3a943
# Thu, 08 Dec 2022 19:36:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 08 Dec 2022 19:36:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 08 Dec 2022 19:39:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 08 Dec 2022 19:39:24 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 08 Dec 2022 19:39:25 GMT
RUN docker-php-ext-enable sodium
# Thu, 08 Dec 2022 19:39:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 Dec 2022 19:39:26 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:cb2ec849933dd31db64abae3fdcb6923c490d9795577bee1ee1be04eab0376ee`  
		Last Modified: Tue, 22 Nov 2022 22:58:12 GMT  
		Size: 2.9 MB (2865346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca108fdbcd11a67cf41e6ad58105ac2d95dffcd2febfae5df098b1577776e2b4`  
		Last Modified: Wed, 30 Nov 2022 22:22:22 GMT  
		Size: 1.7 MB (1703388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a3c36f0f232387119c44145dd35f68a589d293ea19f9fbff2f5dabfba05b7c`  
		Last Modified: Wed, 30 Nov 2022 22:22:21 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92740214b90b0b116f7b164af3e785bb3999df1307a4eac482afb0eedbf3904b`  
		Last Modified: Wed, 30 Nov 2022 22:22:21 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c164cfa716c8c30836bfc040bc9714ca8944322bfa826d7ebaf65a60871f652`  
		Last Modified: Thu, 08 Dec 2022 20:12:54 GMT  
		Size: 11.9 MB (11940852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0b07285068598969f77ccfd077d898c473ade4ff59dde1f0cb7d15b463e7c4`  
		Last Modified: Thu, 08 Dec 2022 20:12:52 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06bbf09e23ec01b5f3e5a644cb1840e669d3c5efbb0f2d463a83d191a1560dd6`  
		Last Modified: Thu, 08 Dec 2022 20:12:55 GMT  
		Size: 14.4 MB (14405254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1608c9a201433df854906c340b2b405c86aa0b5f0b4e550d7fa82edd0fba71f7`  
		Last Modified: Thu, 08 Dec 2022 20:12:52 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5e44e6245e8352bf9f7085dca46e6db741fecdfc7acf05c617d612f9da14ea`  
		Last Modified: Thu, 08 Dec 2022 20:12:53 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:alpine3.17` - linux; arm64 variant v8

```console
$ docker pull php@sha256:83276eb1eeddf4b7dcc6ca044c36d33e022009955f87bffe9067a3bdae2702c9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33866084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1934ed9186997079790f0fa147dbc0453aacdf34f99ce14db394410846e32c4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 22 Nov 2022 22:39:21 GMT
ADD file:685b5edadf1d5bf0aeb2aec35f810d83876e6d2ea0903b213f75a9c5f0dc5901 in / 
# Tue, 22 Nov 2022 22:39:21 GMT
CMD ["/bin/sh"]
# Wed, 30 Nov 2022 21:03:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 30 Nov 2022 21:03:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 30 Nov 2022 21:03:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 30 Nov 2022 21:03:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 30 Nov 2022 21:03:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 30 Nov 2022 21:03:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 30 Nov 2022 21:03:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 30 Nov 2022 21:03:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 30 Nov 2022 21:03:17 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 08 Dec 2022 19:15:51 GMT
ENV PHP_VERSION=8.2.0
# Thu, 08 Dec 2022 19:15:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.0.tar.xz.asc
# Thu, 08 Dec 2022 19:15:51 GMT
ENV PHP_SHA256=6ea4c2dfb532950fd712aa2a08c1412a6a81cd1334dd0b0bf88a8e44c2b3a943
# Thu, 08 Dec 2022 19:15:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 08 Dec 2022 19:15:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 08 Dec 2022 19:19:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 08 Dec 2022 19:19:28 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 08 Dec 2022 19:19:29 GMT
RUN docker-php-ext-enable sodium
# Thu, 08 Dec 2022 19:19:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 Dec 2022 19:19:29 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:261da4162673b93e5c0e7700a3718d40bcc086dbf24b1ec9b54bca0b82300626`  
		Last Modified: Tue, 22 Nov 2022 22:39:45 GMT  
		Size: 3.3 MB (3259190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd5030e0243953a5dc6a26415ada440038b253ef4560edd576a683164696fa9`  
		Last Modified: Wed, 30 Nov 2022 21:30:42 GMT  
		Size: 1.9 MB (1855650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0610361d296c40b235c4e28b9de89b2c1b01a138ea0571a3f566a92befab06`  
		Last Modified: Wed, 30 Nov 2022 21:30:42 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7fe1fcb7369b3185e4af858150e5942b7629718ae79fb697218cb0ab696b3f`  
		Last Modified: Wed, 30 Nov 2022 21:30:42 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f275d3acf8d2cda4abd76488818c815de25ebebe6533ec20fd80db3757986c42`  
		Last Modified: Thu, 08 Dec 2022 19:46:30 GMT  
		Size: 11.9 MB (11940882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a232b155932886c09c173557c8ea89983cee2e8313359b362cd793c49df305`  
		Last Modified: Thu, 08 Dec 2022 19:46:29 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff775680cb1876e313f7db414ce5ab56015c3e621dabde22380105dbdce02e94`  
		Last Modified: Thu, 08 Dec 2022 19:46:31 GMT  
		Size: 16.8 MB (16787097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef2d0dc546e3471b1b3254357fe35272ac287129138e9e16e513468262cb416`  
		Last Modified: Thu, 08 Dec 2022 19:46:29 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3269d9e0bbd83886c5a842f97b72152deb45e5371672fbd724b6b9c616d9fe17`  
		Last Modified: Thu, 08 Dec 2022 19:46:29 GMT  
		Size: 18.8 KB (18792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:alpine3.17` - linux; 386

```console
$ docker pull php@sha256:6950fb75881ea8dd03cf7e4f7ad4b2e7d73c60a24750f1c9e633a1d0279bd4e1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34619818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51bafa86c9613a3e9ca762293fc9da3db503639c248ffd1f3b1612d28961028f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 22 Nov 2022 22:38:24 GMT
ADD file:f2fbc3153694110f7004f005c4e18435b171ed44a3b35498a1b4916ef1e9af43 in / 
# Tue, 22 Nov 2022 22:38:25 GMT
CMD ["/bin/sh"]
# Wed, 30 Nov 2022 21:07:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 30 Nov 2022 21:07:37 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 30 Nov 2022 21:07:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 30 Nov 2022 21:07:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 30 Nov 2022 21:07:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 30 Nov 2022 21:07:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 30 Nov 2022 21:07:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 30 Nov 2022 21:07:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 30 Nov 2022 21:07:44 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 08 Dec 2022 19:12:57 GMT
ENV PHP_VERSION=8.2.0
# Thu, 08 Dec 2022 19:12:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.0.tar.xz.asc
# Thu, 08 Dec 2022 19:12:59 GMT
ENV PHP_SHA256=6ea4c2dfb532950fd712aa2a08c1412a6a81cd1334dd0b0bf88a8e44c2b3a943
# Thu, 08 Dec 2022 19:13:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 08 Dec 2022 19:13:08 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 08 Dec 2022 19:16:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 08 Dec 2022 19:16:22 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 08 Dec 2022 19:16:22 GMT
RUN docker-php-ext-enable sodium
# Thu, 08 Dec 2022 19:16:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 Dec 2022 19:16:24 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:3cc7ae06783159e8c992cfb745833f904e836c74a7704b7a90b4b45a598f878c`  
		Last Modified: Tue, 22 Nov 2022 22:39:08 GMT  
		Size: 3.4 MB (3408493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1915555ddacfd8951122a364c8e9629d63703005ba29cd220a628087a4564dd6`  
		Last Modified: Wed, 30 Nov 2022 21:37:44 GMT  
		Size: 2.0 MB (1970983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c764cb50f35c195b5559104acb5bb5c203ad771c1de6c4dfe9f876b73d885cb`  
		Last Modified: Wed, 30 Nov 2022 21:37:44 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26e72bb2c33f6f2a2dfb7dfe3d1921113cae9107fcf7c76998dc5899bb773ee`  
		Last Modified: Wed, 30 Nov 2022 21:37:44 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fedf136ae6ec79e2de5c78a023edfa45a099938827d481475c1171ed12f2b738`  
		Last Modified: Thu, 08 Dec 2022 19:48:45 GMT  
		Size: 11.9 MB (11940745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06815b929e65c865e85c12c2d8177103e02f051d3dd96c3e2e106f8b93a9364`  
		Last Modified: Thu, 08 Dec 2022 19:48:44 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febdf3314b0ca0fe80badb6003f7b059527b27c92237a2314e1eb98deb040a0e`  
		Last Modified: Thu, 08 Dec 2022 19:48:47 GMT  
		Size: 17.3 MB (17276288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fecafbfb7afbf6fe2ce0d148aeda889dc3c51e53873111aaa15dac001bd77e7`  
		Last Modified: Thu, 08 Dec 2022 19:48:44 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075a8c49ff0305cd2579496e6c711d73397b2a9fd86ba98b788ba7538e0c8f3c`  
		Last Modified: Thu, 08 Dec 2022 19:48:44 GMT  
		Size: 18.9 KB (18908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:alpine3.17` - linux; ppc64le

```console
$ docker pull php@sha256:c5738e475e21e7733a24a370b318bf3a12bf57fa51fc69a89e68dfdd41a287f5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (34958488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed42323947ad4599b31b671d76f091a44cbdde40696087a6b6882782a4f6cd90`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 23 Nov 2022 00:18:18 GMT
ADD file:a8e68f93c597f70ce637ef578c72c9b41b4b8d80b552b8e5570d4efcc1d02ff5 in / 
# Wed, 23 Nov 2022 00:18:18 GMT
CMD ["/bin/sh"]
# Wed, 30 Nov 2022 21:38:37 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 30 Nov 2022 21:38:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 30 Nov 2022 21:38:42 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 30 Nov 2022 21:38:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 30 Nov 2022 21:38:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 30 Nov 2022 21:38:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 30 Nov 2022 21:38:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 30 Nov 2022 21:38:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 30 Nov 2022 21:38:44 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 08 Dec 2022 19:44:23 GMT
ENV PHP_VERSION=8.2.0
# Thu, 08 Dec 2022 19:44:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.0.tar.xz.asc
# Thu, 08 Dec 2022 19:44:23 GMT
ENV PHP_SHA256=6ea4c2dfb532950fd712aa2a08c1412a6a81cd1334dd0b0bf88a8e44c2b3a943
# Thu, 08 Dec 2022 19:44:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 08 Dec 2022 19:44:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 08 Dec 2022 19:48:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 08 Dec 2022 19:48:19 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 08 Dec 2022 19:48:21 GMT
RUN docker-php-ext-enable sodium
# Thu, 08 Dec 2022 19:48:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 Dec 2022 19:48:21 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:69314845b945e4b33e4ee552d0e4156645f71c81b6cb71108c1e32e139aec052`  
		Last Modified: Wed, 23 Nov 2022 00:19:02 GMT  
		Size: 3.4 MB (3384500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb0b5b6ebfcb59d7bb376eda2a3a450213bafa678bcca93b0af952b4d0c1c18`  
		Last Modified: Wed, 30 Nov 2022 22:10:33 GMT  
		Size: 1.9 MB (1938378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed945cdf32e78d05dd306e297a89c2b21ac37e2c170d24aa2f5194ea02358fb`  
		Last Modified: Wed, 30 Nov 2022 22:10:32 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bed7d0ee32d4b74590d0ef4b007add6ad78f90481324806ba82f06942037372`  
		Last Modified: Wed, 30 Nov 2022 22:10:32 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f402bf141face7ef3b7659b512a98b4d51fbf683708e1938c0204e7e4ab9f4af`  
		Last Modified: Thu, 08 Dec 2022 20:22:39 GMT  
		Size: 11.9 MB (11940878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c079a126881e128b6f5b4cd6e04bbd5685cd8d423228cc13ee34d0a38745611`  
		Last Modified: Thu, 08 Dec 2022 20:22:37 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e072bb08df2b2308fcd4f4601ec4f90d7d870874ee374b48fef44a5869b9c4`  
		Last Modified: Thu, 08 Dec 2022 20:22:45 GMT  
		Size: 17.7 MB (17671472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2857d67c5cb0f0f25d40621f2ae03577b029c0ba096a4b0bf99b0cf9e20e87c`  
		Last Modified: Thu, 08 Dec 2022 20:22:38 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4809514f9adf953aec12aa23645475f288de1361f49088349ff46e1d179b00c9`  
		Last Modified: Thu, 08 Dec 2022 20:22:38 GMT  
		Size: 18.8 KB (18785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:alpine3.17` - linux; s390x

```console
$ docker pull php@sha256:44f4071f68d8da2ed8555aaf67a21bbac35635c8fff7b929b8dee2317b6663cc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32779339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478b59104f22af2eca0ac2be762cc66368096b8cfbc59a8615c6fc53b58a9dfa`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 22 Nov 2022 22:47:02 GMT
ADD file:d8cbd162b64e4b7a8b83086be37ef5ee69e955ac955ebbe59e70c6be2a2d1a9f in / 
# Tue, 22 Nov 2022 22:47:03 GMT
CMD ["/bin/sh"]
# Wed, 30 Nov 2022 20:56:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 30 Nov 2022 20:56:11 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 30 Nov 2022 20:56:11 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 30 Nov 2022 20:56:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 30 Nov 2022 20:56:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 30 Nov 2022 20:56:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 30 Nov 2022 20:56:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 30 Nov 2022 20:56:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 30 Nov 2022 20:56:12 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 08 Dec 2022 19:15:18 GMT
ENV PHP_VERSION=8.2.0
# Thu, 08 Dec 2022 19:15:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.0.tar.xz.asc
# Thu, 08 Dec 2022 19:15:19 GMT
ENV PHP_SHA256=6ea4c2dfb532950fd712aa2a08c1412a6a81cd1334dd0b0bf88a8e44c2b3a943
# Thu, 08 Dec 2022 19:15:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 08 Dec 2022 19:15:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 08 Dec 2022 19:20:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 08 Dec 2022 19:20:55 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 08 Dec 2022 19:20:57 GMT
RUN docker-php-ext-enable sodium
# Thu, 08 Dec 2022 19:20:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 Dec 2022 19:20:59 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:844b8973ca9523380e35625da9a5fd2d50338c403129146541e13d0722c056f7`  
		Last Modified: Tue, 22 Nov 2022 22:47:59 GMT  
		Size: 3.2 MB (3170814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6609bd910046178bd3eac570c2c1fc59cad29fb887adaab5d6693e71d47026`  
		Last Modified: Wed, 30 Nov 2022 21:21:53 GMT  
		Size: 1.9 MB (1910084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc11912a116f8a8ce368f5345478751ea66ff55a5b6f480e750cb6e236b8691`  
		Last Modified: Wed, 30 Nov 2022 21:21:53 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c64f2471f65bf6185d022a4d96096ed5e3f00c2a9697e44113bd0c8728997e1`  
		Last Modified: Wed, 30 Nov 2022 21:21:53 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345b79c586b0369c1126a0123feac5d70fe9e0344ac2ab6557dc3e37f94f73d9`  
		Last Modified: Thu, 08 Dec 2022 20:02:26 GMT  
		Size: 11.9 MB (11940898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd640d606e6dcb8e464070ac28c7fea05bf52b2c855d35b81843182fc0873a54`  
		Last Modified: Thu, 08 Dec 2022 20:02:25 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6beaa55c75c56b18065a3b5f4a399438e50560ad461697412ed112c639c63180`  
		Last Modified: Thu, 08 Dec 2022 20:02:27 GMT  
		Size: 15.7 MB (15734261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a7908ca1c8c13175dd25ad9361435c48020054dcd7cbc3ce6533b6cd7c6802`  
		Last Modified: Thu, 08 Dec 2022 20:02:25 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc63197d27e43afe7191a45fc528fecf318b873134ef39b77ccb6ca41684572b`  
		Last Modified: Thu, 08 Dec 2022 20:02:25 GMT  
		Size: 18.8 KB (18805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
