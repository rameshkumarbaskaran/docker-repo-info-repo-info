<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `adminer`

-	[`adminer:4`](#adminer4)
-	[`adminer:4-fastcgi`](#adminer4-fastcgi)
-	[`adminer:4-standalone`](#adminer4-standalone)
-	[`adminer:4.8.0`](#adminer480)
-	[`adminer:4.8.0-fastcgi`](#adminer480-fastcgi)
-	[`adminer:4.8.0-standalone`](#adminer480-standalone)
-	[`adminer:fastcgi`](#adminerfastcgi)
-	[`adminer:latest`](#adminerlatest)
-	[`adminer:standalone`](#adminerstandalone)

## `adminer:4`

```console
$ docker pull adminer@sha256:1ee6ed00d1169a14a1030a1d44a5ab1724392c115d296d98f0a0e8700628deeb
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

### `adminer:4` - linux; amd64

```console
$ docker pull adminer@sha256:d7cbbb92e43f7d55027a58bd115d9425548325f3754cb705b03368243b3930d3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.6 MB (33625851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d5528d5e4b1e1e879cf6d3b49b09245873a231a6054521f40a538633893e3d`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 03:21:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 06 Mar 2021 03:21:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 06 Mar 2021 03:21:31 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 06 Mar 2021 03:21:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 06 Mar 2021 03:21:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 06 Mar 2021 03:21:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 03:21:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 03:21:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 06 Mar 2021 04:18:25 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Sat, 06 Mar 2021 04:18:25 GMT
ENV PHP_VERSION=7.4.16
# Sat, 06 Mar 2021 04:18:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Sat, 06 Mar 2021 04:18:26 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Sat, 06 Mar 2021 04:18:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 06 Mar 2021 04:18:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Mar 2021 04:25:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Mar 2021 04:25:46 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Sat, 06 Mar 2021 04:25:48 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Mar 2021 04:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Mar 2021 04:25:49 GMT
CMD ["php" "-a"]
# Sat, 06 Mar 2021 08:51:16 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 06 Mar 2021 08:51:16 GMT
STOPSIGNAL SIGINT
# Sat, 06 Mar 2021 08:51:17 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 06 Mar 2021 08:51:17 GMT
WORKDIR /var/www/html
# Sat, 06 Mar 2021 08:51:43 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 06 Mar 2021 08:51:43 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Sat, 06 Mar 2021 08:51:43 GMT
ENV ADMINER_VERSION=4.8.0
# Sat, 06 Mar 2021 08:51:44 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Sat, 06 Mar 2021 08:51:44 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Sat, 06 Mar 2021 08:51:46 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 06 Mar 2021 08:51:46 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 06 Mar 2021 08:51:46 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 06 Mar 2021 08:51:46 GMT
USER adminer
# Sat, 06 Mar 2021 08:51:46 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 06 Mar 2021 08:51:47 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743181516422399af3888ad5df44c6f711f992b2f86288db9e191ae13de99fa0`  
		Last Modified: Sat, 06 Mar 2021 06:31:08 GMT  
		Size: 1.7 MB (1694870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c307b60e377a3903f74fd9cde3ad69f754071faac36f81ca74e1aa9eabe4851`  
		Last Modified: Sat, 06 Mar 2021 06:31:08 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d5b43308915ce3198dec1c19aa88719afacff02c85660a952982856a0bcc9c`  
		Last Modified: Sat, 06 Mar 2021 06:31:08 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4848a1e010e4e0cda8de291fa6ed2f3efecf20d7343a69cec21878885828d2d`  
		Last Modified: Sat, 06 Mar 2021 06:35:54 GMT  
		Size: 10.4 MB (10354097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8e88ab7b4e15d3c4d8d099845669643447a702d27188138ed20f8c14879cde`  
		Last Modified: Sat, 06 Mar 2021 06:35:54 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c6688ec4022c9042fad0bff0a5aaa03cd55628577fe71a419761ca5478392c`  
		Last Modified: Sat, 06 Mar 2021 06:35:56 GMT  
		Size: 14.3 MB (14253596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b401e642cd6c785a0ede5899c8a1fb93770d6eaf04a0a5faeb0183ad5c21f3`  
		Last Modified: Sat, 06 Mar 2021 06:35:54 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4aa45ba156c9e4af51f7b2a5eec317be47eca6ba8e9bb8fc368488ea41c11c`  
		Last Modified: Sat, 06 Mar 2021 06:35:54 GMT  
		Size: 17.5 KB (17518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b686977c50b0410c0084a21bef42aae47c53441ee7defe7b25bcad585a19999`  
		Last Modified: Sat, 06 Mar 2021 08:52:42 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf15bf71cdf8a60508b2773274a23124c80de6ad9611b97bd532869bdce6929`  
		Last Modified: Sat, 06 Mar 2021 08:52:38 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7855e8a455940ec1b6c2e7a9d42e3a94e92b3f7dd253bfdefd2ef4f0b272a242`  
		Last Modified: Sat, 06 Mar 2021 08:52:40 GMT  
		Size: 3.9 MB (3903349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff73275236b8945efe2dadf9b67d73cc5c24fb699f0e3265cbdb3445bdabcba`  
		Last Modified: Sat, 06 Mar 2021 08:52:38 GMT  
		Size: 1.5 KB (1471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64cfef0d91dbc6948021e94ae4407132c018d08d4446215342ad7e0447e33383`  
		Last Modified: Sat, 06 Mar 2021 08:52:39 GMT  
		Size: 582.8 KB (582798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7097b3e809e2d58f970ecec3070fa3db82d914e74c47172eb2c2800e051290`  
		Last Modified: Sat, 06 Mar 2021 08:52:39 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; arm variant v6

```console
$ docker pull adminer@sha256:67ecf13bed27733de831bad0889ec483ede8530402c3c46011d2334e4a991c25
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32352290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4b093e53cd99d8904355485561c5dd006e3077e79bf2eaba849078b7c8ff3b`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:17:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Feb 2021 22:17:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 17 Feb 2021 22:17:15 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Feb 2021 22:17:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Feb 2021 22:17:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Feb 2021 22:17:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:17:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:17:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Feb 2021 22:24:49 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:22:42 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:22:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:22:48 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:22:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:23:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:26:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:26:24 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:26:28 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:26:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:26:30 GMT
CMD ["php" "-a"]
# Fri, 05 Mar 2021 01:28:12 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 01:28:12 GMT
STOPSIGNAL SIGINT
# Fri, 05 Mar 2021 01:28:15 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 01:28:15 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 01:29:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 01:29:05 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 01:29:06 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 01:29:07 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 01:29:08 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 01:29:11 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 01:29:11 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:29:12 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 01:29:13 GMT
USER adminer
# Fri, 05 Mar 2021 01:29:13 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 05 Mar 2021 01:29:14 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a33e390360f607fe5a7fe0a0203b7347693b0d8cab270352594a3700e1a1d0`  
		Last Modified: Wed, 17 Feb 2021 22:57:10 GMT  
		Size: 1.7 MB (1684729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d1bbb88bd210deaf33702df9d6fa7f35e72f23dfbb55196147ab537320e9f3`  
		Last Modified: Wed, 17 Feb 2021 22:57:09 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b99fbc527c373db47c36282e5bbd82010870902db2af45982bbb8d700375a32`  
		Last Modified: Wed, 17 Feb 2021 22:57:09 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37a52f8d6a0669099c893e2b3e9ce5d8862eed5489a15f8dafd39f664233b7c`  
		Last Modified: Fri, 05 Mar 2021 00:53:01 GMT  
		Size: 10.4 MB (10354085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e31438bda764d2d788352c3dbdc563f97c840ce2736c283190e590e11a4641`  
		Last Modified: Fri, 05 Mar 2021 00:52:59 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615508ce208f1bfacc67745161a522490ffde3254a7e5b88e2a75704a178b65d`  
		Last Modified: Fri, 05 Mar 2021 00:53:05 GMT  
		Size: 13.5 MB (13479609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49bab722652cd2c45df88dee34d635b0c4824fd1885e9cdb6fa1ad1c707b24d`  
		Last Modified: Fri, 05 Mar 2021 00:52:59 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b5e7fa68211b0722b528ee1f7b5f413c32b3581eec56fc37d056cf1e44d45f`  
		Last Modified: Fri, 05 Mar 2021 00:52:59 GMT  
		Size: 17.6 KB (17574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a863fe1948ed188002b2c53e19c1c4f06aa611913e9aee2e6d37a4b38892fa27`  
		Last Modified: Fri, 05 Mar 2021 01:31:18 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e5d7f207dfb0131e75fb5675de4013a21ec2a9965b6a5f2974a09de577b376`  
		Last Modified: Fri, 05 Mar 2021 01:31:15 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613aba5afd5742d6a2f8c093d4d9e2e3eef9f92d01853c139b3f7690a577fd1d`  
		Last Modified: Fri, 05 Mar 2021 01:31:16 GMT  
		Size: 3.6 MB (3603470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ea9f569f958143bd38a220ee729c6ef6f85c122fe3f42b2a761b57e39df3e9`  
		Last Modified: Fri, 05 Mar 2021 01:31:15 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e6944e336be980c37b3af333b01dab0f1b3db12af184e3cc0ed1d4a326a6ab`  
		Last Modified: Fri, 05 Mar 2021 01:31:15 GMT  
		Size: 582.8 KB (582808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4644911e6f4e52234e1b7b359c25f4998c5be8fe108e2f0b54e5cfd721d2d9`  
		Last Modified: Fri, 05 Mar 2021 01:31:15 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; arm variant v7

```console
$ docker pull adminer@sha256:3c5fe027a505612b8c787c41923bc81f01eba12776b7827fb8de3b48fadd12ff
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31126385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7625601231cbbafd93c468bb5506f91c320be7c6640088ec3203f7b61bcae845`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:56:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Feb 2021 22:57:00 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 17 Feb 2021 22:57:04 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Feb 2021 22:57:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Feb 2021 22:57:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Feb 2021 22:57:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:57:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:57:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Feb 2021 23:07:25 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:51:51 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:51:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:51:52 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:51:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:51:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:54:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:54:56 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:55:00 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:55:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:55:01 GMT
CMD ["php" "-a"]
# Fri, 05 Mar 2021 03:16:34 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 03:16:35 GMT
STOPSIGNAL SIGINT
# Fri, 05 Mar 2021 03:16:37 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 03:16:37 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 03:17:32 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 03:17:34 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 03:17:35 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 03:17:36 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 03:17:36 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 03:17:39 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 03:17:40 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 03:17:41 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 03:17:42 GMT
USER adminer
# Fri, 05 Mar 2021 03:17:42 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 05 Mar 2021 03:17:43 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf491575714634902d01e3e48f3b92702cb2e4c42056aa5421058d2a2cbfd9f6`  
		Last Modified: Wed, 17 Feb 2021 23:33:58 GMT  
		Size: 1.6 MB (1555125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8ae33f1196d3a62a9383b30d3fd81dd4be1bcf1a99a3d928f585b0d85c5408`  
		Last Modified: Wed, 17 Feb 2021 23:33:58 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16bd16ac2dc3896b7ddf5e8e50bafcc3990d8313dc26634a51beafc97cc6374`  
		Last Modified: Wed, 17 Feb 2021 23:33:58 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224ef988837049de958e2e9476510f82fe8e42270706a0671a5a463f6ae97dc2`  
		Last Modified: Fri, 05 Mar 2021 01:20:19 GMT  
		Size: 10.4 MB (10354091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9e75985cf89dec0ed12206b36f371ffbda22ccf6cdbccf5d19345e62db2c14`  
		Last Modified: Fri, 05 Mar 2021 01:20:16 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3067a7094a3949ddb39a5787e92b263164d2eb287f0d508c0497dc270667f7a2`  
		Last Modified: Fri, 05 Mar 2021 01:20:19 GMT  
		Size: 12.6 MB (12608573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e967fccc5675136a3112da05f19624319efe2274faf250ffc942f8df1727990b`  
		Last Modified: Fri, 05 Mar 2021 01:20:15 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bee2c4ad784aa0aa254a050c45062e42eae3e6414649f1e7372db7fe0845817`  
		Last Modified: Fri, 05 Mar 2021 01:20:15 GMT  
		Size: 17.6 KB (17556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd957d7c1659b87bbacdaaa44de1493cd86ce1058104890fa7f886c244af7e2`  
		Last Modified: Fri, 05 Mar 2021 03:19:23 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a9b53808941e232e796f0fce8be1b1a2bdab2ab0d1227f671cdc2e6d8acecd`  
		Last Modified: Fri, 05 Mar 2021 03:19:21 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b983fd5f2f41ac862e588d3c7cb994ae11a6d4dfd1273298d35ff8fcdc87e72`  
		Last Modified: Fri, 05 Mar 2021 03:19:21 GMT  
		Size: 3.6 MB (3576366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957ff1dc0df9c3cd0fa022e0ae444a04b77d5b488a38dcba9673c2f3dfb07f8d`  
		Last Modified: Fri, 05 Mar 2021 03:19:21 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d418e42a87cf9ea044ec23d04a0b56e7f7b51dbab5639eb0e1c16248b88575`  
		Last Modified: Fri, 05 Mar 2021 03:19:21 GMT  
		Size: 582.8 KB (582806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1688bcdb1a112479d4950eae42069fa29ff4e81e587b2387362b4a6cc0fbe2`  
		Last Modified: Fri, 05 Mar 2021 03:19:21 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:7991be9e1a1ee3f2c5d374475d3746026dd7ca64a60167a65551567d7cfccf43
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33506242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11682bbe518b1faa63b82b75d246e7c35612d6d253da8f2011c0539c5b07f5cc`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 23:42:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Feb 2021 23:42:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 17 Feb 2021 23:42:38 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Feb 2021 23:42:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Feb 2021 23:42:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Feb 2021 23:42:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 23:42:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 23:42:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Feb 2021 23:53:01 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:37:35 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:37:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:37:38 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:37:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:37:47 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:42:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:42:39 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:42:44 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:42:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:42:47 GMT
CMD ["php" "-a"]
# Fri, 05 Mar 2021 02:04:43 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 02:04:44 GMT
STOPSIGNAL SIGINT
# Fri, 05 Mar 2021 02:04:48 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 02:04:50 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 02:05:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 02:05:56 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 02:05:57 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 02:05:57 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 02:05:58 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 02:06:02 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 02:06:03 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 02:06:04 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 02:06:05 GMT
USER adminer
# Fri, 05 Mar 2021 02:06:06 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 05 Mar 2021 02:06:06 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4b642bcaaef409203aaedc803835562ee86d3ea457bf4ccdd22e5d7b2367f1`  
		Last Modified: Thu, 18 Feb 2021 00:23:35 GMT  
		Size: 1.7 MB (1694455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ea39643e14bb66b107bb23b02b8c7a193ed89d38f4ae52b1decbe763fb0db9`  
		Last Modified: Thu, 18 Feb 2021 00:23:34 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3455119714d8ce066305d3b121e103a3cf690db26bb556906ba67e7a7c1f559`  
		Last Modified: Thu, 18 Feb 2021 00:23:34 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a68a1ddf490519ddbcd4f75589909c8d4703a6b902bae2a7319905984b7547`  
		Last Modified: Fri, 05 Mar 2021 01:13:32 GMT  
		Size: 10.4 MB (10354115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1754592c0391f5b7b27cf3c7110b1e2a917ebb769b0ceaf9bfdfd0181cc6cb`  
		Last Modified: Fri, 05 Mar 2021 01:13:30 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a402e34d4d52011f5ecf29a826d7fd94dc474fdf156b70d506d3deaeb2a4d3b`  
		Last Modified: Fri, 05 Mar 2021 01:13:34 GMT  
		Size: 14.3 MB (14263146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1702d0137849d4baf63d0536ee9f8391c72c295a46613ed43c270f3cc81a90`  
		Last Modified: Fri, 05 Mar 2021 01:13:31 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ebe5152320826ffaea66119f3e759ce05ed98bb09a201643ee6674cbd9685e`  
		Last Modified: Fri, 05 Mar 2021 01:13:31 GMT  
		Size: 17.6 KB (17574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a42655d4ea3811b755ccede7be6704d6e30a4e912c6ec284807f25e1874c11`  
		Last Modified: Fri, 05 Mar 2021 02:08:13 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36983a97af0e64abf039823af9b57936cc5add643fab48f1d64ca7fbeb076a02`  
		Last Modified: Fri, 05 Mar 2021 02:08:11 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23c53be365e785ad30481daf9c58f08857ca80fc5fc681e12655557a14f7093`  
		Last Modified: Fri, 05 Mar 2021 02:08:12 GMT  
		Size: 3.9 MB (3874584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d698ddfcb363647524ac96d6fe45138e9aa228c8662ec68d2c877a5862a6257`  
		Last Modified: Fri, 05 Mar 2021 02:08:11 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e7497f33585536dba243eedb8aea95c51b88677f674845065a15d776a0e7c78`  
		Last Modified: Fri, 05 Mar 2021 02:08:12 GMT  
		Size: 582.8 KB (582809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041eab10d184403fbf0b2a94255c47e5618bc99fd708586209ad66d02a41c86b`  
		Last Modified: Fri, 05 Mar 2021 02:08:11 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; 386

```console
$ docker pull adminer@sha256:3c12e8f857cf7b920500273d347a57b13be7f75bc361cd49631704781e87dafe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34214715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8de5231523b1be5d66db42c66ace28ceef73e37457dc22956bd36744ea35592f`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 02:13:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 06 Mar 2021 02:13:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 06 Mar 2021 02:13:32 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 06 Mar 2021 02:13:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 06 Mar 2021 02:13:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 06 Mar 2021 02:13:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 02:13:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 02:13:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 06 Mar 2021 02:59:52 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Sat, 06 Mar 2021 02:59:52 GMT
ENV PHP_VERSION=7.4.16
# Sat, 06 Mar 2021 02:59:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Sat, 06 Mar 2021 02:59:53 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Sat, 06 Mar 2021 03:00:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 06 Mar 2021 03:00:19 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Mar 2021 03:08:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Mar 2021 03:08:56 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Sat, 06 Mar 2021 03:08:58 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Mar 2021 03:08:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Mar 2021 03:08:58 GMT
CMD ["php" "-a"]
# Sat, 06 Mar 2021 08:16:03 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 06 Mar 2021 08:16:03 GMT
STOPSIGNAL SIGINT
# Sat, 06 Mar 2021 08:16:04 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 06 Mar 2021 08:16:04 GMT
WORKDIR /var/www/html
# Sat, 06 Mar 2021 08:16:34 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 06 Mar 2021 08:16:34 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Sat, 06 Mar 2021 08:16:34 GMT
ENV ADMINER_VERSION=4.8.0
# Sat, 06 Mar 2021 08:16:34 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Sat, 06 Mar 2021 08:16:35 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Sat, 06 Mar 2021 08:16:37 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 06 Mar 2021 08:16:38 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 06 Mar 2021 08:16:38 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 06 Mar 2021 08:16:38 GMT
USER adminer
# Sat, 06 Mar 2021 08:16:38 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 06 Mar 2021 08:16:38 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d779edf81d3549de0c570804cffa8279f4a980d3fed1292285070f24a1b00f`  
		Last Modified: Sat, 06 Mar 2021 05:47:24 GMT  
		Size: 1.8 MB (1793700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce9d30537e4bf7ab9ad24ea334671e794e0830680c386cf4b36dbba54dd40c5`  
		Last Modified: Sat, 06 Mar 2021 05:47:23 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f119038c35efd6cc0b1a27c432b2fc338da413650c224359556d95e0bf8214`  
		Last Modified: Sat, 06 Mar 2021 05:47:23 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:125aeed6c18a6c28cf608d3c3cd80094c61ed4f9023855f9c3ac4993f1542907`  
		Last Modified: Sat, 06 Mar 2021 05:53:56 GMT  
		Size: 10.4 MB (10354073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05563330040dc337869b22ab8c267fc06fa14139a5f270679e69ba3a718896b5`  
		Last Modified: Sat, 06 Mar 2021 05:53:53 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567f9a9d037948e123fbbec64dfb76f7cca9d30cd3e5526abc597b65fd39656b`  
		Last Modified: Sat, 06 Mar 2021 05:54:00 GMT  
		Size: 14.6 MB (14630287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28b3a57348334ee91df9b04ec97e570fcff52d0a9fa3e3ec3247823d80a437d`  
		Last Modified: Sat, 06 Mar 2021 05:53:53 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0621d49125fecbf6f64ac583fbf7c76034bc51eed48c69516922c398d93a6c`  
		Last Modified: Sat, 06 Mar 2021 05:53:54 GMT  
		Size: 17.5 KB (17501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c703587ef05b977c127d751c1c78fa472b5ddb67b5ac217ac20ea90cd8855c`  
		Last Modified: Sat, 06 Mar 2021 08:17:58 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e848e2757b70b020801c677c59e10e8709f14f3f76f32d2b1be5f95679f4f6c5`  
		Last Modified: Sat, 06 Mar 2021 08:17:54 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f2ac401974d5ea19f7f375960da2a7a6c77f23dab4135c4bd95c4dc64f9d02`  
		Last Modified: Sat, 06 Mar 2021 08:17:55 GMT  
		Size: 4.0 MB (4010207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cb78f666be732b2b10b604df1cb578ad8ccca1445c29fd5bab4ba346f29247`  
		Last Modified: Sat, 06 Mar 2021 08:17:54 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980181a00a928280cf2288da2498d06c9203508ce40aa0aed05b1a2be94ae1ce`  
		Last Modified: Sat, 06 Mar 2021 08:17:54 GMT  
		Size: 582.8 KB (582807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0865a1f7fbcf5062e0b5b2fc87b6ea55d2e4c094297f6139e110bbc7a1c9794`  
		Last Modified: Sat, 06 Mar 2021 08:17:54 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; ppc64le

```console
$ docker pull adminer@sha256:f8ed36e984e53d541d8f690681208acc65c3b6e90ac3830c51e821eeb7b24951
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (34960311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0819898f5e08afcbb1041ea1c325869490d997fe19fcaa3e93b720312272db4`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 21:17:29 GMT
ADD file:28f4377c61c0f8eb43a6b36e6a24ef5893f51d405d25b62e364988223537ae0b in / 
# Wed, 17 Feb 2021 21:17:37 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 00:23:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Feb 2021 00:24:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 18 Feb 2021 00:24:44 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 18 Feb 2021 00:24:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Feb 2021 00:25:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 18 Feb 2021 00:25:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:25:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:25:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Feb 2021 00:40:47 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 01:05:36 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 01:05:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 01:05:52 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 01:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 01:06:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:11:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 01:11:19 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:11:29 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 01:11:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 01:11:46 GMT
CMD ["php" "-a"]
# Fri, 05 Mar 2021 02:08:50 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 02:09:05 GMT
STOPSIGNAL SIGINT
# Fri, 05 Mar 2021 02:09:23 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 02:09:30 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 02:10:27 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 02:10:29 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 02:10:33 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 02:10:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 02:10:56 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 02:11:23 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 02:11:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 02:11:34 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 02:11:42 GMT
USER adminer
# Fri, 05 Mar 2021 02:11:57 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 05 Mar 2021 02:12:05 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:cb672e0375a8f9bb3d33049ceb372ffa49b959bfc84fe6f72bfb97b682a608c8`  
		Last Modified: Wed, 17 Feb 2021 21:18:10 GMT  
		Size: 2.8 MB (2813081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebfde0ed2b25fdf7a28b46b01e73c7891af78bd260ce9c5f46f33a0fd4bba5a`  
		Last Modified: Thu, 18 Feb 2021 01:25:11 GMT  
		Size: 1.7 MB (1741666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c587bda2cf37683b8f80371450083e1533df270a51cbe196c845e7ab52f8943`  
		Last Modified: Thu, 18 Feb 2021 01:25:09 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2faee0918d4167a0323dba5b4244442a3d6cd88d5eacd4a560b72f056274a4`  
		Last Modified: Thu, 18 Feb 2021 01:25:10 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791bb958f337b6cf4b2ea90cf5ac9fcb4612738a152ac4a09a69335da096e59b`  
		Last Modified: Fri, 05 Mar 2021 01:49:57 GMT  
		Size: 10.4 MB (10354080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86e997f6d103c9c5f8aa990ba021777b0a7b8073db6c1aa66166630ac5fb896`  
		Last Modified: Fri, 05 Mar 2021 01:49:55 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97cf656907ab8d840227fdc0e36c17cac097192e975dbb19d8fbc99f3ddde66`  
		Last Modified: Fri, 05 Mar 2021 01:49:59 GMT  
		Size: 15.5 MB (15524632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953ac22358c5b3a72272c4db94f387dafe749dccc315fe715fd54646a7e67fa1`  
		Last Modified: Fri, 05 Mar 2021 01:49:55 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5274e31720b346823b92235766eace03c5b3ca24d9af8910eb3c00a29bc1f48e`  
		Last Modified: Fri, 05 Mar 2021 01:49:56 GMT  
		Size: 17.6 KB (17566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae1914ed9afaacdd2822f6ce3b21c1ba2cfc67fb0a0fc37105941301dde3979`  
		Last Modified: Fri, 05 Mar 2021 02:15:07 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097959a8b93e17b2458e2add93679e6bc07debf1b8ed2e8e39ebdb005d0de353`  
		Last Modified: Fri, 05 Mar 2021 02:15:03 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08378c640496a604d70139ba5075c5cd2fe90d0786621bc4396e7cee75634053`  
		Last Modified: Fri, 05 Mar 2021 02:15:05 GMT  
		Size: 3.9 MB (3918494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4eee7fd3e560e705de2352e9453419f436960844b5ddfda9986cedb09cd6bde`  
		Last Modified: Fri, 05 Mar 2021 02:15:03 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435b254436c62649064c5af03dfecbb978ff36ac4740efbc8a476f538850455e`  
		Last Modified: Fri, 05 Mar 2021 02:15:03 GMT  
		Size: 582.8 KB (582810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38c8209ca8c0d5b2b2b2baae2f460323d08fc90ce007eabd250244bc371189b`  
		Last Modified: Fri, 05 Mar 2021 02:15:05 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; s390x

```console
$ docker pull adminer@sha256:9035a1407febca18c25bbc2820e9ac6a09281165f387df8d135066d3bcad2d14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32764749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ff9987904c7594d2e9098e19fcc387f22c02e45e942703bd6f07ac77ebbe58`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 00:40:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Feb 2021 00:40:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 18 Feb 2021 00:40:31 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 18 Feb 2021 00:40:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Feb 2021 00:40:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 18 Feb 2021 00:40:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:40:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:40:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Feb 2021 00:51:38 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:17:53 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:17:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:17:54 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:17:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:17:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:21:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:21:14 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:21:14 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:21:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:21:15 GMT
CMD ["php" "-a"]
# Fri, 05 Mar 2021 01:35:01 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 01:35:02 GMT
STOPSIGNAL SIGINT
# Fri, 05 Mar 2021 01:35:03 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 01:35:03 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 01:35:28 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 01:35:28 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 01:35:28 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 01:35:29 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 01:35:29 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 01:35:30 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 01:35:30 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:35:31 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 01:35:31 GMT
USER adminer
# Fri, 05 Mar 2021 01:35:31 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 05 Mar 2021 01:35:31 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2eaf748a32e76be0f1aa6246cb11c8aa5022aa834df364bb87f581198e6376`  
		Last Modified: Thu, 18 Feb 2021 01:26:48 GMT  
		Size: 1.8 MB (1756400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5716be54c61b8e2a38b4d6a0cbece88801726747842f6bd1a50aaf4e8442013f`  
		Last Modified: Thu, 18 Feb 2021 01:26:48 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6aa66a8dad4ec1443c27324fc452b05c4299dbffefcebee55700880033b3ff7`  
		Last Modified: Thu, 18 Feb 2021 01:26:47 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8b7b210cf7a350eb620b3574b19324168c8c4833e0cfe3d634398782f48175`  
		Last Modified: Fri, 05 Mar 2021 00:51:36 GMT  
		Size: 10.4 MB (10354085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a066cfbe30cd983f5ffef2df9d50618ade23fe99302b69e012774b2269585d1`  
		Last Modified: Fri, 05 Mar 2021 00:51:35 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9401205bc3eb7297f85c414b790172be23d1c4ab061aee72eaeb28b69132c073`  
		Last Modified: Fri, 05 Mar 2021 00:51:38 GMT  
		Size: 13.9 MB (13860060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afee2a631a7b79b3c487a3ef4500ea44fa978bd6464fe317d1a65d4b104f7309`  
		Last Modified: Fri, 05 Mar 2021 00:51:35 GMT  
		Size: 2.3 KB (2261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0499fd075a9fd055ca563a90fb4b2aaac9056a65b191d7db41c37188db098cf1`  
		Last Modified: Fri, 05 Mar 2021 00:51:35 GMT  
		Size: 17.6 KB (17566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b53123be7d4a2e60f8c580951db7f413a3fddabf032b97cc4e1715defe06aa`  
		Last Modified: Fri, 05 Mar 2021 01:36:37 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aab483619f81007684651c4b32aae7e47300c44374d5a2e165bfee97c9a5ed8`  
		Last Modified: Fri, 05 Mar 2021 01:36:35 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21994edf819ad8eed5eea7af018652abc984e3d7f67f6dd34ead1779f80b961c`  
		Last Modified: Fri, 05 Mar 2021 01:36:35 GMT  
		Size: 3.6 MB (3583473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39598f68be044d39764fd4f2c72cccb6ff39c29081b324413fb9af80f22c6b6`  
		Last Modified: Fri, 05 Mar 2021 01:36:35 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6988f4418691c53ad239170a2ec56313d0be5ebf6636151c2ab31dee05fd76`  
		Last Modified: Fri, 05 Mar 2021 01:36:35 GMT  
		Size: 582.8 KB (582811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f94af1afe9ebb57211f0f17af8d7edc0ccf29b7fe0f188bae543435432d960`  
		Last Modified: Fri, 05 Mar 2021 01:36:35 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4-fastcgi`

```console
$ docker pull adminer@sha256:ddbc8ec701aaf2deafbf06f680f3a1d2cd9b1fffb94d27c1f4395ad50008d9de
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

### `adminer:4-fastcgi` - linux; amd64

```console
$ docker pull adminer@sha256:bc5ef236fdce0cdf13798c6ce77033b0c9b0946a2b1e93de5e6f43a64b82d004
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33700229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7d4c6e1f2444f36f3d32007c33a6c9cd065f53a81670922522b88fa93450db`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 03:21:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 06 Mar 2021 03:21:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 06 Mar 2021 03:21:31 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 06 Mar 2021 03:21:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 06 Mar 2021 03:21:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 06 Mar 2021 03:31:10 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 06 Mar 2021 03:31:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 03:31:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 03:31:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 06 Mar 2021 04:25:55 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Sat, 06 Mar 2021 04:25:55 GMT
ENV PHP_VERSION=7.4.16
# Sat, 06 Mar 2021 04:25:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Sat, 06 Mar 2021 04:25:56 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Sat, 06 Mar 2021 04:26:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 06 Mar 2021 04:26:02 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Mar 2021 04:33:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Mar 2021 04:33:18 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Sat, 06 Mar 2021 04:33:20 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Mar 2021 04:33:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Mar 2021 04:33:21 GMT
WORKDIR /var/www/html
# Sat, 06 Mar 2021 04:33:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Sat, 06 Mar 2021 04:33:23 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 04:33:23 GMT
EXPOSE 9000
# Sat, 06 Mar 2021 04:33:23 GMT
CMD ["php-fpm"]
# Sat, 06 Mar 2021 08:51:52 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 06 Mar 2021 08:51:53 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 06 Mar 2021 08:52:18 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 06 Mar 2021 08:52:18 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Sat, 06 Mar 2021 08:52:18 GMT
ENV ADMINER_VERSION=4.8.0
# Sat, 06 Mar 2021 08:52:19 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Sat, 06 Mar 2021 08:52:19 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Sat, 06 Mar 2021 08:52:20 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 06 Mar 2021 08:52:21 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 06 Mar 2021 08:52:21 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 06 Mar 2021 08:52:21 GMT
USER adminer
# Sat, 06 Mar 2021 08:52:21 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743181516422399af3888ad5df44c6f711f992b2f86288db9e191ae13de99fa0`  
		Last Modified: Sat, 06 Mar 2021 06:31:08 GMT  
		Size: 1.7 MB (1694870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c307b60e377a3903f74fd9cde3ad69f754071faac36f81ca74e1aa9eabe4851`  
		Last Modified: Sat, 06 Mar 2021 06:31:08 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d5b43308915ce3198dec1c19aa88719afacff02c85660a952982856a0bcc9c`  
		Last Modified: Sat, 06 Mar 2021 06:31:08 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9d5f24e6dd6af8f23f239240af8081c566914e78925b8646ee59d456477a1b`  
		Last Modified: Sat, 06 Mar 2021 06:36:44 GMT  
		Size: 10.4 MB (10354098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfaad94f9a19bca51025c93a5b36fbf3c4e2636a37ecf935233cff9afc27f94`  
		Last Modified: Sat, 06 Mar 2021 06:36:41 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3507948cfcd59468730f9f8ae89b321891415ae8f7c98d96b4662c057f5af471`  
		Last Modified: Sat, 06 Mar 2021 06:36:44 GMT  
		Size: 14.3 MB (14319531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f880a2fb467d3c5d725b4ef31da9c50bcd19a9171455db7a0d4a80a9f80395e`  
		Last Modified: Sat, 06 Mar 2021 06:36:40 GMT  
		Size: 2.3 KB (2265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56deb6830b6ed046fb324d5539b34742ee0aa32484cf961c9fbd5c47aca9a930`  
		Last Modified: Sat, 06 Mar 2021 06:36:41 GMT  
		Size: 17.5 KB (17521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a194189cbad21888697c3cee4fca8f4d5ac096f5ac1eb2981e77d310fa63d6f`  
		Last Modified: Sat, 06 Mar 2021 06:36:40 GMT  
		Size: 8.4 KB (8448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d93b56dad37e253e7efcccf4f4bc0c55f1093fe4a3ee4743ae53353d77a4fb`  
		Last Modified: Sat, 06 Mar 2021 08:53:09 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238c4c0f49a87323787cdbdc3bd37ed5b43bd67fd3d903a5efc67f049bde2cb0`  
		Last Modified: Sat, 06 Mar 2021 08:53:07 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ed295294c14844d5fa520952a46cc832ea9192ab54ceebcd9da78c2b835dd3`  
		Last Modified: Sat, 06 Mar 2021 08:53:07 GMT  
		Size: 3.9 MB (3903344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285104d31a4786a761bed245e8a819ffccb92919702026f95ab8874eaeb112a0`  
		Last Modified: Sat, 06 Mar 2021 08:53:07 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ef4cb5580635a144f2bbf3d755884632850d26926d5b90840cbab8b1642886`  
		Last Modified: Sat, 06 Mar 2021 08:53:08 GMT  
		Size: 582.8 KB (582795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f853ae8f0e76e3efc1e422db5915507f4f50c611294e9c5492f775bd0ecb1f`  
		Last Modified: Sat, 06 Mar 2021 08:53:07 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm variant v6

```console
$ docker pull adminer@sha256:2c93d2f0b02908d29d3e3a4228ab25c9c86b812331b270e390a62a9680ff1433
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32424063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f018255660e0906d91baef706cff1811a4410856b0a37263b715383bb70fdcdc`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:17:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Feb 2021 22:17:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 17 Feb 2021 22:17:15 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Feb 2021 22:17:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Feb 2021 22:17:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Feb 2021 22:20:46 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Wed, 17 Feb 2021 22:20:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:20:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:20:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Feb 2021 22:28:41 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:26:48 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:26:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:26:54 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:27:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:27:04 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:30:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:30:26 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:30:30 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:30:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:30:35 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 00:30:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 05 Mar 2021 00:30:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Mar 2021 00:30:42 GMT
EXPOSE 9000
# Fri, 05 Mar 2021 00:30:43 GMT
CMD ["php-fpm"]
# Fri, 05 Mar 2021 01:29:31 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 01:29:34 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 01:30:26 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 01:30:28 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 01:30:32 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 01:30:33 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 01:30:34 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 01:30:38 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 01:30:40 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:30:41 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 01:30:42 GMT
USER adminer
# Fri, 05 Mar 2021 01:30:43 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a33e390360f607fe5a7fe0a0203b7347693b0d8cab270352594a3700e1a1d0`  
		Last Modified: Wed, 17 Feb 2021 22:57:10 GMT  
		Size: 1.7 MB (1684729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d1bbb88bd210deaf33702df9d6fa7f35e72f23dfbb55196147ab537320e9f3`  
		Last Modified: Wed, 17 Feb 2021 22:57:09 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b99fbc527c373db47c36282e5bbd82010870902db2af45982bbb8d700375a32`  
		Last Modified: Wed, 17 Feb 2021 22:57:09 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a4e6f92ba693a7496c53317c79fb8823ac45b33556818a381ca1acb347a311`  
		Last Modified: Fri, 05 Mar 2021 00:53:29 GMT  
		Size: 10.4 MB (10354080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64bd603e34a5bf0fa1834fd5ce8641cedb22c0847f3169c9e72e354c86124cf5`  
		Last Modified: Fri, 05 Mar 2021 00:53:26 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5a57e3834bdaac522a5cdd7b4b6477988fcf852a76cc708026ebebdf3418d8`  
		Last Modified: Fri, 05 Mar 2021 00:53:31 GMT  
		Size: 13.5 MB (13542966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f30d0b9ee8eeabfe33c8ea2c2fcafd27e5f80bcffda325ebb1846975ef034a6`  
		Last Modified: Fri, 05 Mar 2021 00:53:26 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b17255c3c925daf160f37347c78fc54f36e044e2bfd7a8e3bffe95da9645f246`  
		Last Modified: Fri, 05 Mar 2021 00:53:26 GMT  
		Size: 17.6 KB (17565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85523748d905c5ced6faebb10205d1f7d78ae3e4869ede5793c7166ed9f77aff`  
		Last Modified: Fri, 05 Mar 2021 00:53:26 GMT  
		Size: 8.4 KB (8439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1712caab329d945c3f088703ff9c4deec4090358774a7db47f0b7b99c15e87c5`  
		Last Modified: Fri, 05 Mar 2021 01:31:31 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a5a4bdd0e396fbf2a64b84a39e11daf996231c4892713b67a32e9322c81803`  
		Last Modified: Fri, 05 Mar 2021 01:31:31 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9de2c7ce4296df3731f81d52dcc5b36bd803852f0e238ca129824dc7cc262fc`  
		Last Modified: Fri, 05 Mar 2021 01:31:30 GMT  
		Size: 3.6 MB (3603477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797df658ad578348afe4e024e48bbce535519997fa3519bfaf6f43f9a3fbe08b`  
		Last Modified: Fri, 05 Mar 2021 01:31:29 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63a45dd2ec611bee4416bdce98f4eff41d3463dd6d6609a205a19133a310515`  
		Last Modified: Fri, 05 Mar 2021 01:31:30 GMT  
		Size: 582.8 KB (582797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4e6e8ef666b79da7372c6c2125bbf4aa29676e7bdafca00830339affbf7107`  
		Last Modified: Fri, 05 Mar 2021 01:31:30 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:76344293a9cba5c4d934e1de727cfbbad24ec801c6738f8053de6f20f4042dd4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31197081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e91dadff87355741ea5395e5e6d3093bb426a290226eb1bb4da419f1036038`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:56:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Feb 2021 22:57:00 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 17 Feb 2021 22:57:04 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Feb 2021 22:57:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Feb 2021 22:57:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Feb 2021 23:02:51 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Wed, 17 Feb 2021 23:02:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 23:02:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 23:02:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Feb 2021 23:10:45 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:55:10 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:55:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:55:11 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:55:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:55:19 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:58:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:58:21 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:58:25 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:58:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:58:27 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 00:58:29 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 05 Mar 2021 00:58:30 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Mar 2021 00:58:31 GMT
EXPOSE 9000
# Fri, 05 Mar 2021 00:58:31 GMT
CMD ["php-fpm"]
# Fri, 05 Mar 2021 03:17:52 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 03:17:55 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 03:18:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 03:18:46 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 03:18:47 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 03:18:48 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 03:18:49 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 03:18:53 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 03:18:53 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 03:18:54 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 03:18:55 GMT
USER adminer
# Fri, 05 Mar 2021 03:18:56 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf491575714634902d01e3e48f3b92702cb2e4c42056aa5421058d2a2cbfd9f6`  
		Last Modified: Wed, 17 Feb 2021 23:33:58 GMT  
		Size: 1.6 MB (1555125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8ae33f1196d3a62a9383b30d3fd81dd4be1bcf1a99a3d928f585b0d85c5408`  
		Last Modified: Wed, 17 Feb 2021 23:33:58 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16bd16ac2dc3896b7ddf5e8e50bafcc3990d8313dc26634a51beafc97cc6374`  
		Last Modified: Wed, 17 Feb 2021 23:33:58 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d01524e4fc3d179f93abe7a61fc071ecdf6c581f749d96a60690840a8fa15a`  
		Last Modified: Fri, 05 Mar 2021 01:20:43 GMT  
		Size: 10.4 MB (10354089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada63173b828bcc3b5e7d7d61a96a1a4f0a3af46ad66848c75181167c6302b6c`  
		Last Modified: Fri, 05 Mar 2021 01:20:40 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a644dd136e4a568009bc8751ede1d9017381190dc8660db4a7c91ad4bbe6cd`  
		Last Modified: Fri, 05 Mar 2021 01:20:45 GMT  
		Size: 12.7 MB (12670824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a36409e92a747f08911634d5cad27605075c881509247a1abea57e68679210`  
		Last Modified: Fri, 05 Mar 2021 01:20:40 GMT  
		Size: 2.3 KB (2263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6111685ad3b47ae7d882febd0446f781cf086d73c476fd00e53527166c5fa7`  
		Last Modified: Fri, 05 Mar 2021 01:20:40 GMT  
		Size: 17.6 KB (17565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b43d0062c0be09cf3da7b8d797ec945fa4a15872201297c8fc68c7c7fb5c0e`  
		Last Modified: Fri, 05 Mar 2021 01:20:40 GMT  
		Size: 8.4 KB (8441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce8f178b810d2b0b4986e7a6068e8e0a703cb9601aee7af7f6235398197d74c`  
		Last Modified: Fri, 05 Mar 2021 03:19:38 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b2f6c2d0c7d9165289f4145f9fb2d5bd3622112bcb40a5555d56f3358b9705`  
		Last Modified: Fri, 05 Mar 2021 03:19:36 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a09c36d006daa2967af8b26e2157350bb5c39f1101544c40298a9879857f951`  
		Last Modified: Fri, 05 Mar 2021 03:19:36 GMT  
		Size: 3.6 MB (3576364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e5deca6d2f48ec567fff9f38134e4504ee858f1a6de2b415ff6f147b559865`  
		Last Modified: Fri, 05 Mar 2021 03:19:36 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c078244c143c12118d608de1dacae67d924b37e40fa5ff5e1626d7603db96c77`  
		Last Modified: Fri, 05 Mar 2021 03:19:36 GMT  
		Size: 582.8 KB (582808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399c2c8d9bb3754b99dd4e63d7f86d9a17b1ba333afbcdd1a91323827dbf6c19`  
		Last Modified: Fri, 05 Mar 2021 03:19:36 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:9d290c8427c90264c046b18b2dad85bf1ab72b9636a299fdcdb70e725b73cf37
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.6 MB (33587124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fda254daa0110b7ed8e11936831a70eb476e6bac9d0f864a167cc3ca89cc570`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 23:42:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Feb 2021 23:42:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 17 Feb 2021 23:42:38 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Feb 2021 23:42:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Feb 2021 23:42:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Feb 2021 23:47:35 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Wed, 17 Feb 2021 23:47:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 23:47:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 23:47:37 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Feb 2021 23:57:44 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:42:58 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:43:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:43:01 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:43:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:43:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:47:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:47:53 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:47:56 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:47:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:47:58 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 00:48:00 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 05 Mar 2021 00:48:00 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Mar 2021 00:48:01 GMT
EXPOSE 9000
# Fri, 05 Mar 2021 00:48:02 GMT
CMD ["php-fpm"]
# Fri, 05 Mar 2021 02:06:30 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 02:06:33 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 02:07:32 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 02:07:34 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 02:07:35 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 02:07:37 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 02:07:38 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 02:07:42 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 02:07:43 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 02:07:44 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 02:07:46 GMT
USER adminer
# Fri, 05 Mar 2021 02:07:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4b642bcaaef409203aaedc803835562ee86d3ea457bf4ccdd22e5d7b2367f1`  
		Last Modified: Thu, 18 Feb 2021 00:23:35 GMT  
		Size: 1.7 MB (1694455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ea39643e14bb66b107bb23b02b8c7a193ed89d38f4ae52b1decbe763fb0db9`  
		Last Modified: Thu, 18 Feb 2021 00:23:34 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3455119714d8ce066305d3b121e103a3cf690db26bb556906ba67e7a7c1f559`  
		Last Modified: Thu, 18 Feb 2021 00:23:34 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5fb9efa5fb7c6758d0c1ef8f8dec26c072a0b3db105d3bc1072051a584a31e`  
		Last Modified: Fri, 05 Mar 2021 01:14:03 GMT  
		Size: 10.4 MB (10354114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b86fa187c3fdc5dc79bdeb0cc5299859c0c0095b732f4ee415c0bb12daa215b`  
		Last Modified: Fri, 05 Mar 2021 01:14:00 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12f3432275b2be2dd42ee1df485264de064473b2c82feda5bf9c9d20b5b271b`  
		Last Modified: Fri, 05 Mar 2021 01:14:04 GMT  
		Size: 14.3 MB (14335600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c51b3d598680e53ab4687fb42e8f593583f31bd96bddf4f4a3260e7ce39978`  
		Last Modified: Fri, 05 Mar 2021 01:14:00 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f84e9090c4bc7becc3688c7892a83e9851718fc9492734a99d408a8f37e5940`  
		Last Modified: Fri, 05 Mar 2021 01:14:00 GMT  
		Size: 17.6 KB (17578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6e5a4c4a59a3a7880ef2d31091da082e89c8a5d36fe48cc0e6d2a869a4c015`  
		Last Modified: Fri, 05 Mar 2021 01:14:00 GMT  
		Size: 8.4 KB (8443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c96f48785c9c98e7112aba8a63a131c4068630fb03bf917709cbf26dcde0f6`  
		Last Modified: Fri, 05 Mar 2021 02:08:29 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68227b3239ccce99fdd4b5f144a2966beb055b69b3cd677b07dc854149769ed7`  
		Last Modified: Fri, 05 Mar 2021 02:08:28 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ee8c6445369dac5a5c0a1eebb4a5de36d9b41daa6842a89ffd90533c70d115`  
		Last Modified: Fri, 05 Mar 2021 02:08:28 GMT  
		Size: 3.9 MB (3874581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd6128ec00cfc5bafbcbb5cd0958f7c6bb1789fdd6d9f462f7bdfb945d25051`  
		Last Modified: Fri, 05 Mar 2021 02:08:27 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e85b4b40588c16a96e7bd4ebc9bda548027f1d29a882087ca1873edbe5c6a3e`  
		Last Modified: Fri, 05 Mar 2021 02:08:28 GMT  
		Size: 582.8 KB (582807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52d3bffbd635505b2a6fe9733d78a3056c37f05d763c518a0cfbb0e62ae6fa8`  
		Last Modified: Fri, 05 Mar 2021 02:08:28 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:26d15f54137462efdfea2e074d6e3aab1a83d2e91bfb268a77550109c29e494e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34296076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f79ec5602cf1203e859966ea84f6f0af410574c66ff1695966634f7fa99a0602`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 02:13:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 06 Mar 2021 02:13:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 06 Mar 2021 02:13:32 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 06 Mar 2021 02:13:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 06 Mar 2021 02:13:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 06 Mar 2021 02:20:59 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 06 Mar 2021 02:20:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 02:20:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 02:21:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 06 Mar 2021 03:09:15 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Sat, 06 Mar 2021 03:09:15 GMT
ENV PHP_VERSION=7.4.16
# Sat, 06 Mar 2021 03:09:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Sat, 06 Mar 2021 03:09:16 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Sat, 06 Mar 2021 03:09:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 06 Mar 2021 03:09:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Mar 2021 03:18:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Mar 2021 03:18:11 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Sat, 06 Mar 2021 03:18:13 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Mar 2021 03:18:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Mar 2021 03:18:14 GMT
WORKDIR /var/www/html
# Sat, 06 Mar 2021 03:18:15 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Sat, 06 Mar 2021 03:18:15 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 03:18:16 GMT
EXPOSE 9000
# Sat, 06 Mar 2021 03:18:16 GMT
CMD ["php-fpm"]
# Sat, 06 Mar 2021 08:16:46 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 06 Mar 2021 08:16:47 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 06 Mar 2021 08:17:17 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 06 Mar 2021 08:17:17 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Sat, 06 Mar 2021 08:17:18 GMT
ENV ADMINER_VERSION=4.8.0
# Sat, 06 Mar 2021 08:17:18 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Sat, 06 Mar 2021 08:17:18 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Sat, 06 Mar 2021 08:17:20 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 06 Mar 2021 08:17:20 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 06 Mar 2021 08:17:20 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 06 Mar 2021 08:17:21 GMT
USER adminer
# Sat, 06 Mar 2021 08:17:21 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d779edf81d3549de0c570804cffa8279f4a980d3fed1292285070f24a1b00f`  
		Last Modified: Sat, 06 Mar 2021 05:47:24 GMT  
		Size: 1.8 MB (1793700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce9d30537e4bf7ab9ad24ea334671e794e0830680c386cf4b36dbba54dd40c5`  
		Last Modified: Sat, 06 Mar 2021 05:47:23 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f119038c35efd6cc0b1a27c432b2fc338da413650c224359556d95e0bf8214`  
		Last Modified: Sat, 06 Mar 2021 05:47:23 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5397827f225e72f10184ff09624c35bf31a5231897f53e91ca07da5f62e873dc`  
		Last Modified: Sat, 06 Mar 2021 05:54:56 GMT  
		Size: 10.4 MB (10354073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8309650059a0810adb36671135e0f311a358f75fb9dd4d4de7e8ca2e03df4ecd`  
		Last Modified: Sat, 06 Mar 2021 05:54:52 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8ec289fc161bd97f4660f6a9b0102128d91f8545b7a66236470e13f99820a6`  
		Last Modified: Sat, 06 Mar 2021 05:54:56 GMT  
		Size: 14.7 MB (14703205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df93dca921888af6f7dd240ba41be2492ce1b35f2a7691841b7453de8097cba`  
		Last Modified: Sat, 06 Mar 2021 05:54:52 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a789e9947572f56584832fc18a9febda69c07a7fd803f86bb47b8b76048e0d`  
		Last Modified: Sat, 06 Mar 2021 05:54:52 GMT  
		Size: 17.5 KB (17499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7a016c5403915747cc20016342dd4a30b61cf26f6ecfbf3db8dc913816ba0d`  
		Last Modified: Sat, 06 Mar 2021 05:54:52 GMT  
		Size: 8.4 KB (8443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20574028b280be669aaf096c2a36ea615748c8d8947b537fed28011a1bba827`  
		Last Modified: Sat, 06 Mar 2021 08:18:31 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcffc992f5c3c59e7de4cf88a6b3a2bcea4814b1479dd0fd6533b32693a2337`  
		Last Modified: Sat, 06 Mar 2021 08:18:28 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d41c527ce013e3f17159bc459ca0d55a95da81bcc5e14571bbe997c5156b6e0`  
		Last Modified: Sat, 06 Mar 2021 08:18:30 GMT  
		Size: 4.0 MB (4010213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad6f6db03a695dc6910470b21945bc6f75b04d9f24622618a244bced44e9a04`  
		Last Modified: Sat, 06 Mar 2021 08:18:29 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde165942766dd540d19ff22ecd092d80baff426cd360af35eb0fb5ef30b2dac`  
		Last Modified: Sat, 06 Mar 2021 08:18:29 GMT  
		Size: 582.8 KB (582800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a269b82e491105b4090cf94096e9ce312f49c2e7c64fc59ce8fca97a0048d95`  
		Last Modified: Sat, 06 Mar 2021 08:18:28 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:60214217e7c6d9d5d171f4a2f5b8e64a7616f02249811ff70fc139b463c8c1a6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (35045727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195aaf01b7fc54d33fea092504c0b5d14247b799d81fbb46ce985ef115ac65c8`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 17 Feb 2021 21:17:29 GMT
ADD file:28f4377c61c0f8eb43a6b36e6a24ef5893f51d405d25b62e364988223537ae0b in / 
# Wed, 17 Feb 2021 21:17:37 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 00:23:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Feb 2021 00:24:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 18 Feb 2021 00:24:44 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 18 Feb 2021 00:24:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Feb 2021 00:25:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 18 Feb 2021 00:32:20 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 18 Feb 2021 00:32:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:32:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:32:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Feb 2021 00:47:19 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 01:12:05 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 01:12:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 01:12:14 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 01:12:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 01:12:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:17:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 01:17:41 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:17:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 01:17:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 01:18:00 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 01:18:13 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 05 Mar 2021 01:18:18 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Mar 2021 01:18:22 GMT
EXPOSE 9000
# Fri, 05 Mar 2021 01:18:25 GMT
CMD ["php-fpm"]
# Fri, 05 Mar 2021 02:12:29 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 02:12:47 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 02:13:39 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 02:13:41 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 02:13:45 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 02:13:50 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 02:13:54 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 02:14:11 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 02:14:12 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 02:14:17 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 02:14:23 GMT
USER adminer
# Fri, 05 Mar 2021 02:14:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:cb672e0375a8f9bb3d33049ceb372ffa49b959bfc84fe6f72bfb97b682a608c8`  
		Last Modified: Wed, 17 Feb 2021 21:18:10 GMT  
		Size: 2.8 MB (2813081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebfde0ed2b25fdf7a28b46b01e73c7891af78bd260ce9c5f46f33a0fd4bba5a`  
		Last Modified: Thu, 18 Feb 2021 01:25:11 GMT  
		Size: 1.7 MB (1741666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c587bda2cf37683b8f80371450083e1533df270a51cbe196c845e7ab52f8943`  
		Last Modified: Thu, 18 Feb 2021 01:25:09 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2faee0918d4167a0323dba5b4244442a3d6cd88d5eacd4a560b72f056274a4`  
		Last Modified: Thu, 18 Feb 2021 01:25:10 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50832ff8121fa6dabe4fef261cdf442de13beba3eba5b02edc01bb52575f604`  
		Last Modified: Fri, 05 Mar 2021 01:50:47 GMT  
		Size: 10.4 MB (10354080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492225a51fbf5c42138184c0b8f334e0c03349c39df922382ab84510b28fa495`  
		Last Modified: Fri, 05 Mar 2021 01:50:40 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e38b008adbe62b7a3a5140dedb456e37ae0f03fe3970c9f2386f7b294c13c3`  
		Last Modified: Fri, 05 Mar 2021 01:50:44 GMT  
		Size: 15.6 MB (15601592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac2e3566364c50161e37f74f62cc1631496ad06e929b660adcd70dd66254b3d`  
		Last Modified: Fri, 05 Mar 2021 01:50:40 GMT  
		Size: 2.3 KB (2265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48abd24364092c58878a940181d9510d843d157a2e6649ea9fe3f8452341d5e0`  
		Last Modified: Fri, 05 Mar 2021 01:50:40 GMT  
		Size: 17.6 KB (17568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c82139d7ee7be2c8e6f6313bad71cc515fcb36b36f9db46406380c839a21ff`  
		Last Modified: Fri, 05 Mar 2021 01:50:40 GMT  
		Size: 8.4 KB (8445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb87a4b5911ea0082c17ed927c804ab2ef1074f3e4a232baee3c7aa0d53f2001`  
		Last Modified: Fri, 05 Mar 2021 02:15:36 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:867bbe031ef2fdc9b041f464c092ae860709ae7089ad3bf2d020ca9a5685adb9`  
		Last Modified: Fri, 05 Mar 2021 02:15:33 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1352d4abeeccc4cdec18fe083cca986917a96a75c051377c6e6f60df25b8b7`  
		Last Modified: Fri, 05 Mar 2021 02:15:35 GMT  
		Size: 3.9 MB (3918505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf3106a1ac6be7ebc6cac6752295d88ad3e0b6dde2a752abbcf19665597f91d`  
		Last Modified: Fri, 05 Mar 2021 02:15:32 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7e5c63ff249b14ce430b50a9d068fd75bd570c8e3dda8a120527bbeb589643`  
		Last Modified: Fri, 05 Mar 2021 02:15:32 GMT  
		Size: 582.8 KB (582811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5372a8bc61644fe0469438556e96846b6dd32a217c62c627af9666e934dc59d0`  
		Last Modified: Fri, 05 Mar 2021 02:15:34 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:172c17539eec169a1efbc7bdb5582b0c6d68a767c96c91534eaa512ea11f1a54
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32837225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e84b58503996daca80603c6caf456f29c872d2fbcedc12f3883b3ff932310f5`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 00:40:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Feb 2021 00:40:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 18 Feb 2021 00:40:31 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 18 Feb 2021 00:40:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Feb 2021 00:40:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 18 Feb 2021 00:46:04 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 18 Feb 2021 00:46:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:46:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:46:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Feb 2021 00:56:47 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:21:28 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:21:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:21:28 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:21:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:21:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:24:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:24:36 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:24:37 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:24:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:24:37 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 00:24:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 05 Mar 2021 00:24:38 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Mar 2021 00:24:38 GMT
EXPOSE 9000
# Fri, 05 Mar 2021 00:24:38 GMT
CMD ["php-fpm"]
# Fri, 05 Mar 2021 01:35:37 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 01:35:38 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 01:36:11 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 01:36:11 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 01:36:12 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 01:36:12 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 01:36:13 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 01:36:14 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 01:36:14 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:36:15 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 01:36:15 GMT
USER adminer
# Fri, 05 Mar 2021 01:36:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2eaf748a32e76be0f1aa6246cb11c8aa5022aa834df364bb87f581198e6376`  
		Last Modified: Thu, 18 Feb 2021 01:26:48 GMT  
		Size: 1.8 MB (1756400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5716be54c61b8e2a38b4d6a0cbece88801726747842f6bd1a50aaf4e8442013f`  
		Last Modified: Thu, 18 Feb 2021 01:26:48 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6aa66a8dad4ec1443c27324fc452b05c4299dbffefcebee55700880033b3ff7`  
		Last Modified: Thu, 18 Feb 2021 01:26:47 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ec6de43c42608abedaf0d1351eac485f25cf6ea8189784c33b0bd55cf4c8de`  
		Last Modified: Fri, 05 Mar 2021 00:51:59 GMT  
		Size: 10.4 MB (10354080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7f932c8c75e84329764906d4a66784a32d6eebc1e0bf7b70c2e6608e3fbf9b`  
		Last Modified: Fri, 05 Mar 2021 00:51:56 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94d974f2d24d19a056887cdf386d4e9505e841d3a06c71f3ffa4eda14b55cd5`  
		Last Modified: Fri, 05 Mar 2021 00:51:59 GMT  
		Size: 13.9 MB (13924090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69925775200e946533560678d8a38f9ae9c806a7f163e84949bcbcb5b90adcf5`  
		Last Modified: Fri, 05 Mar 2021 00:51:56 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e58476f31db9ac4d71c9e0ea37118bbbd9193cc0b3aea7cc05bab5c83ddff8`  
		Last Modified: Fri, 05 Mar 2021 00:51:56 GMT  
		Size: 17.6 KB (17562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c27cda61463930e8e9c42f8de03c8a59af15035338f16a147b75cfff1adc6bb`  
		Last Modified: Fri, 05 Mar 2021 00:51:56 GMT  
		Size: 8.4 KB (8445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536690e7823ee104420228155dfb821af13a367f39347bb42c6536a406b031c2`  
		Last Modified: Fri, 05 Mar 2021 01:36:49 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f87e2102e12d1ceefff1f2490100e7e4a089955c1ec33e2d52db85d8706f9c`  
		Last Modified: Fri, 05 Mar 2021 01:36:47 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180b148ebd9e445d7b63cfd748624466a392b06d40e4980de5a006e90fe54def`  
		Last Modified: Fri, 05 Mar 2021 01:36:48 GMT  
		Size: 3.6 MB (3583484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95fc51e3df0e6750051bc696529caddc5ee514b5c8d0515a39eee82a06e9739a`  
		Last Modified: Fri, 05 Mar 2021 01:36:47 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5435da686f45a2ef26c52cb075980530af7e8ef76884a406b5a0e9b3068a28`  
		Last Modified: Fri, 05 Mar 2021 01:36:47 GMT  
		Size: 582.8 KB (582804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472506157be8ba02f17eab06907cba644d1ead543ffe97be2a01f98d2a45ad45`  
		Last Modified: Fri, 05 Mar 2021 01:36:47 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4-standalone`

```console
$ docker pull adminer@sha256:1ee6ed00d1169a14a1030a1d44a5ab1724392c115d296d98f0a0e8700628deeb
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

### `adminer:4-standalone` - linux; amd64

```console
$ docker pull adminer@sha256:d7cbbb92e43f7d55027a58bd115d9425548325f3754cb705b03368243b3930d3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.6 MB (33625851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d5528d5e4b1e1e879cf6d3b49b09245873a231a6054521f40a538633893e3d`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 03:21:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 06 Mar 2021 03:21:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 06 Mar 2021 03:21:31 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 06 Mar 2021 03:21:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 06 Mar 2021 03:21:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 06 Mar 2021 03:21:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 03:21:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 03:21:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 06 Mar 2021 04:18:25 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Sat, 06 Mar 2021 04:18:25 GMT
ENV PHP_VERSION=7.4.16
# Sat, 06 Mar 2021 04:18:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Sat, 06 Mar 2021 04:18:26 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Sat, 06 Mar 2021 04:18:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 06 Mar 2021 04:18:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Mar 2021 04:25:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Mar 2021 04:25:46 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Sat, 06 Mar 2021 04:25:48 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Mar 2021 04:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Mar 2021 04:25:49 GMT
CMD ["php" "-a"]
# Sat, 06 Mar 2021 08:51:16 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 06 Mar 2021 08:51:16 GMT
STOPSIGNAL SIGINT
# Sat, 06 Mar 2021 08:51:17 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 06 Mar 2021 08:51:17 GMT
WORKDIR /var/www/html
# Sat, 06 Mar 2021 08:51:43 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 06 Mar 2021 08:51:43 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Sat, 06 Mar 2021 08:51:43 GMT
ENV ADMINER_VERSION=4.8.0
# Sat, 06 Mar 2021 08:51:44 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Sat, 06 Mar 2021 08:51:44 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Sat, 06 Mar 2021 08:51:46 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 06 Mar 2021 08:51:46 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 06 Mar 2021 08:51:46 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 06 Mar 2021 08:51:46 GMT
USER adminer
# Sat, 06 Mar 2021 08:51:46 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 06 Mar 2021 08:51:47 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743181516422399af3888ad5df44c6f711f992b2f86288db9e191ae13de99fa0`  
		Last Modified: Sat, 06 Mar 2021 06:31:08 GMT  
		Size: 1.7 MB (1694870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c307b60e377a3903f74fd9cde3ad69f754071faac36f81ca74e1aa9eabe4851`  
		Last Modified: Sat, 06 Mar 2021 06:31:08 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d5b43308915ce3198dec1c19aa88719afacff02c85660a952982856a0bcc9c`  
		Last Modified: Sat, 06 Mar 2021 06:31:08 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4848a1e010e4e0cda8de291fa6ed2f3efecf20d7343a69cec21878885828d2d`  
		Last Modified: Sat, 06 Mar 2021 06:35:54 GMT  
		Size: 10.4 MB (10354097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8e88ab7b4e15d3c4d8d099845669643447a702d27188138ed20f8c14879cde`  
		Last Modified: Sat, 06 Mar 2021 06:35:54 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c6688ec4022c9042fad0bff0a5aaa03cd55628577fe71a419761ca5478392c`  
		Last Modified: Sat, 06 Mar 2021 06:35:56 GMT  
		Size: 14.3 MB (14253596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b401e642cd6c785a0ede5899c8a1fb93770d6eaf04a0a5faeb0183ad5c21f3`  
		Last Modified: Sat, 06 Mar 2021 06:35:54 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4aa45ba156c9e4af51f7b2a5eec317be47eca6ba8e9bb8fc368488ea41c11c`  
		Last Modified: Sat, 06 Mar 2021 06:35:54 GMT  
		Size: 17.5 KB (17518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b686977c50b0410c0084a21bef42aae47c53441ee7defe7b25bcad585a19999`  
		Last Modified: Sat, 06 Mar 2021 08:52:42 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf15bf71cdf8a60508b2773274a23124c80de6ad9611b97bd532869bdce6929`  
		Last Modified: Sat, 06 Mar 2021 08:52:38 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7855e8a455940ec1b6c2e7a9d42e3a94e92b3f7dd253bfdefd2ef4f0b272a242`  
		Last Modified: Sat, 06 Mar 2021 08:52:40 GMT  
		Size: 3.9 MB (3903349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff73275236b8945efe2dadf9b67d73cc5c24fb699f0e3265cbdb3445bdabcba`  
		Last Modified: Sat, 06 Mar 2021 08:52:38 GMT  
		Size: 1.5 KB (1471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64cfef0d91dbc6948021e94ae4407132c018d08d4446215342ad7e0447e33383`  
		Last Modified: Sat, 06 Mar 2021 08:52:39 GMT  
		Size: 582.8 KB (582798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7097b3e809e2d58f970ecec3070fa3db82d914e74c47172eb2c2800e051290`  
		Last Modified: Sat, 06 Mar 2021 08:52:39 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm variant v6

```console
$ docker pull adminer@sha256:67ecf13bed27733de831bad0889ec483ede8530402c3c46011d2334e4a991c25
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32352290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4b093e53cd99d8904355485561c5dd006e3077e79bf2eaba849078b7c8ff3b`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:17:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Feb 2021 22:17:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 17 Feb 2021 22:17:15 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Feb 2021 22:17:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Feb 2021 22:17:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Feb 2021 22:17:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:17:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:17:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Feb 2021 22:24:49 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:22:42 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:22:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:22:48 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:22:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:23:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:26:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:26:24 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:26:28 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:26:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:26:30 GMT
CMD ["php" "-a"]
# Fri, 05 Mar 2021 01:28:12 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 01:28:12 GMT
STOPSIGNAL SIGINT
# Fri, 05 Mar 2021 01:28:15 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 01:28:15 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 01:29:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 01:29:05 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 01:29:06 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 01:29:07 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 01:29:08 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 01:29:11 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 01:29:11 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:29:12 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 01:29:13 GMT
USER adminer
# Fri, 05 Mar 2021 01:29:13 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 05 Mar 2021 01:29:14 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a33e390360f607fe5a7fe0a0203b7347693b0d8cab270352594a3700e1a1d0`  
		Last Modified: Wed, 17 Feb 2021 22:57:10 GMT  
		Size: 1.7 MB (1684729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d1bbb88bd210deaf33702df9d6fa7f35e72f23dfbb55196147ab537320e9f3`  
		Last Modified: Wed, 17 Feb 2021 22:57:09 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b99fbc527c373db47c36282e5bbd82010870902db2af45982bbb8d700375a32`  
		Last Modified: Wed, 17 Feb 2021 22:57:09 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37a52f8d6a0669099c893e2b3e9ce5d8862eed5489a15f8dafd39f664233b7c`  
		Last Modified: Fri, 05 Mar 2021 00:53:01 GMT  
		Size: 10.4 MB (10354085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e31438bda764d2d788352c3dbdc563f97c840ce2736c283190e590e11a4641`  
		Last Modified: Fri, 05 Mar 2021 00:52:59 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615508ce208f1bfacc67745161a522490ffde3254a7e5b88e2a75704a178b65d`  
		Last Modified: Fri, 05 Mar 2021 00:53:05 GMT  
		Size: 13.5 MB (13479609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49bab722652cd2c45df88dee34d635b0c4824fd1885e9cdb6fa1ad1c707b24d`  
		Last Modified: Fri, 05 Mar 2021 00:52:59 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b5e7fa68211b0722b528ee1f7b5f413c32b3581eec56fc37d056cf1e44d45f`  
		Last Modified: Fri, 05 Mar 2021 00:52:59 GMT  
		Size: 17.6 KB (17574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a863fe1948ed188002b2c53e19c1c4f06aa611913e9aee2e6d37a4b38892fa27`  
		Last Modified: Fri, 05 Mar 2021 01:31:18 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e5d7f207dfb0131e75fb5675de4013a21ec2a9965b6a5f2974a09de577b376`  
		Last Modified: Fri, 05 Mar 2021 01:31:15 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613aba5afd5742d6a2f8c093d4d9e2e3eef9f92d01853c139b3f7690a577fd1d`  
		Last Modified: Fri, 05 Mar 2021 01:31:16 GMT  
		Size: 3.6 MB (3603470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ea9f569f958143bd38a220ee729c6ef6f85c122fe3f42b2a761b57e39df3e9`  
		Last Modified: Fri, 05 Mar 2021 01:31:15 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e6944e336be980c37b3af333b01dab0f1b3db12af184e3cc0ed1d4a326a6ab`  
		Last Modified: Fri, 05 Mar 2021 01:31:15 GMT  
		Size: 582.8 KB (582808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4644911e6f4e52234e1b7b359c25f4998c5be8fe108e2f0b54e5cfd721d2d9`  
		Last Modified: Fri, 05 Mar 2021 01:31:15 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:3c5fe027a505612b8c787c41923bc81f01eba12776b7827fb8de3b48fadd12ff
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31126385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7625601231cbbafd93c468bb5506f91c320be7c6640088ec3203f7b61bcae845`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:56:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Feb 2021 22:57:00 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 17 Feb 2021 22:57:04 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Feb 2021 22:57:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Feb 2021 22:57:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Feb 2021 22:57:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:57:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:57:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Feb 2021 23:07:25 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:51:51 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:51:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:51:52 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:51:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:51:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:54:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:54:56 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:55:00 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:55:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:55:01 GMT
CMD ["php" "-a"]
# Fri, 05 Mar 2021 03:16:34 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 03:16:35 GMT
STOPSIGNAL SIGINT
# Fri, 05 Mar 2021 03:16:37 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 03:16:37 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 03:17:32 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 03:17:34 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 03:17:35 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 03:17:36 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 03:17:36 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 03:17:39 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 03:17:40 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 03:17:41 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 03:17:42 GMT
USER adminer
# Fri, 05 Mar 2021 03:17:42 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 05 Mar 2021 03:17:43 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf491575714634902d01e3e48f3b92702cb2e4c42056aa5421058d2a2cbfd9f6`  
		Last Modified: Wed, 17 Feb 2021 23:33:58 GMT  
		Size: 1.6 MB (1555125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8ae33f1196d3a62a9383b30d3fd81dd4be1bcf1a99a3d928f585b0d85c5408`  
		Last Modified: Wed, 17 Feb 2021 23:33:58 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16bd16ac2dc3896b7ddf5e8e50bafcc3990d8313dc26634a51beafc97cc6374`  
		Last Modified: Wed, 17 Feb 2021 23:33:58 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224ef988837049de958e2e9476510f82fe8e42270706a0671a5a463f6ae97dc2`  
		Last Modified: Fri, 05 Mar 2021 01:20:19 GMT  
		Size: 10.4 MB (10354091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9e75985cf89dec0ed12206b36f371ffbda22ccf6cdbccf5d19345e62db2c14`  
		Last Modified: Fri, 05 Mar 2021 01:20:16 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3067a7094a3949ddb39a5787e92b263164d2eb287f0d508c0497dc270667f7a2`  
		Last Modified: Fri, 05 Mar 2021 01:20:19 GMT  
		Size: 12.6 MB (12608573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e967fccc5675136a3112da05f19624319efe2274faf250ffc942f8df1727990b`  
		Last Modified: Fri, 05 Mar 2021 01:20:15 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bee2c4ad784aa0aa254a050c45062e42eae3e6414649f1e7372db7fe0845817`  
		Last Modified: Fri, 05 Mar 2021 01:20:15 GMT  
		Size: 17.6 KB (17556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd957d7c1659b87bbacdaaa44de1493cd86ce1058104890fa7f886c244af7e2`  
		Last Modified: Fri, 05 Mar 2021 03:19:23 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a9b53808941e232e796f0fce8be1b1a2bdab2ab0d1227f671cdc2e6d8acecd`  
		Last Modified: Fri, 05 Mar 2021 03:19:21 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b983fd5f2f41ac862e588d3c7cb994ae11a6d4dfd1273298d35ff8fcdc87e72`  
		Last Modified: Fri, 05 Mar 2021 03:19:21 GMT  
		Size: 3.6 MB (3576366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957ff1dc0df9c3cd0fa022e0ae444a04b77d5b488a38dcba9673c2f3dfb07f8d`  
		Last Modified: Fri, 05 Mar 2021 03:19:21 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d418e42a87cf9ea044ec23d04a0b56e7f7b51dbab5639eb0e1c16248b88575`  
		Last Modified: Fri, 05 Mar 2021 03:19:21 GMT  
		Size: 582.8 KB (582806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1688bcdb1a112479d4950eae42069fa29ff4e81e587b2387362b4a6cc0fbe2`  
		Last Modified: Fri, 05 Mar 2021 03:19:21 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:7991be9e1a1ee3f2c5d374475d3746026dd7ca64a60167a65551567d7cfccf43
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33506242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11682bbe518b1faa63b82b75d246e7c35612d6d253da8f2011c0539c5b07f5cc`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 23:42:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Feb 2021 23:42:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 17 Feb 2021 23:42:38 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Feb 2021 23:42:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Feb 2021 23:42:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Feb 2021 23:42:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 23:42:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 23:42:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Feb 2021 23:53:01 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:37:35 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:37:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:37:38 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:37:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:37:47 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:42:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:42:39 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:42:44 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:42:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:42:47 GMT
CMD ["php" "-a"]
# Fri, 05 Mar 2021 02:04:43 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 02:04:44 GMT
STOPSIGNAL SIGINT
# Fri, 05 Mar 2021 02:04:48 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 02:04:50 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 02:05:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 02:05:56 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 02:05:57 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 02:05:57 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 02:05:58 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 02:06:02 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 02:06:03 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 02:06:04 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 02:06:05 GMT
USER adminer
# Fri, 05 Mar 2021 02:06:06 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 05 Mar 2021 02:06:06 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4b642bcaaef409203aaedc803835562ee86d3ea457bf4ccdd22e5d7b2367f1`  
		Last Modified: Thu, 18 Feb 2021 00:23:35 GMT  
		Size: 1.7 MB (1694455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ea39643e14bb66b107bb23b02b8c7a193ed89d38f4ae52b1decbe763fb0db9`  
		Last Modified: Thu, 18 Feb 2021 00:23:34 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3455119714d8ce066305d3b121e103a3cf690db26bb556906ba67e7a7c1f559`  
		Last Modified: Thu, 18 Feb 2021 00:23:34 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a68a1ddf490519ddbcd4f75589909c8d4703a6b902bae2a7319905984b7547`  
		Last Modified: Fri, 05 Mar 2021 01:13:32 GMT  
		Size: 10.4 MB (10354115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1754592c0391f5b7b27cf3c7110b1e2a917ebb769b0ceaf9bfdfd0181cc6cb`  
		Last Modified: Fri, 05 Mar 2021 01:13:30 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a402e34d4d52011f5ecf29a826d7fd94dc474fdf156b70d506d3deaeb2a4d3b`  
		Last Modified: Fri, 05 Mar 2021 01:13:34 GMT  
		Size: 14.3 MB (14263146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1702d0137849d4baf63d0536ee9f8391c72c295a46613ed43c270f3cc81a90`  
		Last Modified: Fri, 05 Mar 2021 01:13:31 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ebe5152320826ffaea66119f3e759ce05ed98bb09a201643ee6674cbd9685e`  
		Last Modified: Fri, 05 Mar 2021 01:13:31 GMT  
		Size: 17.6 KB (17574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a42655d4ea3811b755ccede7be6704d6e30a4e912c6ec284807f25e1874c11`  
		Last Modified: Fri, 05 Mar 2021 02:08:13 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36983a97af0e64abf039823af9b57936cc5add643fab48f1d64ca7fbeb076a02`  
		Last Modified: Fri, 05 Mar 2021 02:08:11 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23c53be365e785ad30481daf9c58f08857ca80fc5fc681e12655557a14f7093`  
		Last Modified: Fri, 05 Mar 2021 02:08:12 GMT  
		Size: 3.9 MB (3874584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d698ddfcb363647524ac96d6fe45138e9aa228c8662ec68d2c877a5862a6257`  
		Last Modified: Fri, 05 Mar 2021 02:08:11 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e7497f33585536dba243eedb8aea95c51b88677f674845065a15d776a0e7c78`  
		Last Modified: Fri, 05 Mar 2021 02:08:12 GMT  
		Size: 582.8 KB (582809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041eab10d184403fbf0b2a94255c47e5618bc99fd708586209ad66d02a41c86b`  
		Last Modified: Fri, 05 Mar 2021 02:08:11 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; 386

```console
$ docker pull adminer@sha256:3c12e8f857cf7b920500273d347a57b13be7f75bc361cd49631704781e87dafe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34214715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8de5231523b1be5d66db42c66ace28ceef73e37457dc22956bd36744ea35592f`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 02:13:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 06 Mar 2021 02:13:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 06 Mar 2021 02:13:32 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 06 Mar 2021 02:13:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 06 Mar 2021 02:13:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 06 Mar 2021 02:13:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 02:13:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 02:13:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 06 Mar 2021 02:59:52 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Sat, 06 Mar 2021 02:59:52 GMT
ENV PHP_VERSION=7.4.16
# Sat, 06 Mar 2021 02:59:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Sat, 06 Mar 2021 02:59:53 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Sat, 06 Mar 2021 03:00:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 06 Mar 2021 03:00:19 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Mar 2021 03:08:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Mar 2021 03:08:56 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Sat, 06 Mar 2021 03:08:58 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Mar 2021 03:08:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Mar 2021 03:08:58 GMT
CMD ["php" "-a"]
# Sat, 06 Mar 2021 08:16:03 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 06 Mar 2021 08:16:03 GMT
STOPSIGNAL SIGINT
# Sat, 06 Mar 2021 08:16:04 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 06 Mar 2021 08:16:04 GMT
WORKDIR /var/www/html
# Sat, 06 Mar 2021 08:16:34 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 06 Mar 2021 08:16:34 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Sat, 06 Mar 2021 08:16:34 GMT
ENV ADMINER_VERSION=4.8.0
# Sat, 06 Mar 2021 08:16:34 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Sat, 06 Mar 2021 08:16:35 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Sat, 06 Mar 2021 08:16:37 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 06 Mar 2021 08:16:38 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 06 Mar 2021 08:16:38 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 06 Mar 2021 08:16:38 GMT
USER adminer
# Sat, 06 Mar 2021 08:16:38 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 06 Mar 2021 08:16:38 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d779edf81d3549de0c570804cffa8279f4a980d3fed1292285070f24a1b00f`  
		Last Modified: Sat, 06 Mar 2021 05:47:24 GMT  
		Size: 1.8 MB (1793700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce9d30537e4bf7ab9ad24ea334671e794e0830680c386cf4b36dbba54dd40c5`  
		Last Modified: Sat, 06 Mar 2021 05:47:23 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f119038c35efd6cc0b1a27c432b2fc338da413650c224359556d95e0bf8214`  
		Last Modified: Sat, 06 Mar 2021 05:47:23 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:125aeed6c18a6c28cf608d3c3cd80094c61ed4f9023855f9c3ac4993f1542907`  
		Last Modified: Sat, 06 Mar 2021 05:53:56 GMT  
		Size: 10.4 MB (10354073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05563330040dc337869b22ab8c267fc06fa14139a5f270679e69ba3a718896b5`  
		Last Modified: Sat, 06 Mar 2021 05:53:53 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567f9a9d037948e123fbbec64dfb76f7cca9d30cd3e5526abc597b65fd39656b`  
		Last Modified: Sat, 06 Mar 2021 05:54:00 GMT  
		Size: 14.6 MB (14630287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28b3a57348334ee91df9b04ec97e570fcff52d0a9fa3e3ec3247823d80a437d`  
		Last Modified: Sat, 06 Mar 2021 05:53:53 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0621d49125fecbf6f64ac583fbf7c76034bc51eed48c69516922c398d93a6c`  
		Last Modified: Sat, 06 Mar 2021 05:53:54 GMT  
		Size: 17.5 KB (17501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c703587ef05b977c127d751c1c78fa472b5ddb67b5ac217ac20ea90cd8855c`  
		Last Modified: Sat, 06 Mar 2021 08:17:58 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e848e2757b70b020801c677c59e10e8709f14f3f76f32d2b1be5f95679f4f6c5`  
		Last Modified: Sat, 06 Mar 2021 08:17:54 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f2ac401974d5ea19f7f375960da2a7a6c77f23dab4135c4bd95c4dc64f9d02`  
		Last Modified: Sat, 06 Mar 2021 08:17:55 GMT  
		Size: 4.0 MB (4010207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cb78f666be732b2b10b604df1cb578ad8ccca1445c29fd5bab4ba346f29247`  
		Last Modified: Sat, 06 Mar 2021 08:17:54 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980181a00a928280cf2288da2498d06c9203508ce40aa0aed05b1a2be94ae1ce`  
		Last Modified: Sat, 06 Mar 2021 08:17:54 GMT  
		Size: 582.8 KB (582807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0865a1f7fbcf5062e0b5b2fc87b6ea55d2e4c094297f6139e110bbc7a1c9794`  
		Last Modified: Sat, 06 Mar 2021 08:17:54 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:f8ed36e984e53d541d8f690681208acc65c3b6e90ac3830c51e821eeb7b24951
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (34960311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0819898f5e08afcbb1041ea1c325869490d997fe19fcaa3e93b720312272db4`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 21:17:29 GMT
ADD file:28f4377c61c0f8eb43a6b36e6a24ef5893f51d405d25b62e364988223537ae0b in / 
# Wed, 17 Feb 2021 21:17:37 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 00:23:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Feb 2021 00:24:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 18 Feb 2021 00:24:44 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 18 Feb 2021 00:24:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Feb 2021 00:25:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 18 Feb 2021 00:25:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:25:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:25:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Feb 2021 00:40:47 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 01:05:36 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 01:05:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 01:05:52 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 01:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 01:06:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:11:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 01:11:19 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:11:29 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 01:11:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 01:11:46 GMT
CMD ["php" "-a"]
# Fri, 05 Mar 2021 02:08:50 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 02:09:05 GMT
STOPSIGNAL SIGINT
# Fri, 05 Mar 2021 02:09:23 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 02:09:30 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 02:10:27 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 02:10:29 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 02:10:33 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 02:10:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 02:10:56 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 02:11:23 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 02:11:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 02:11:34 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 02:11:42 GMT
USER adminer
# Fri, 05 Mar 2021 02:11:57 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 05 Mar 2021 02:12:05 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:cb672e0375a8f9bb3d33049ceb372ffa49b959bfc84fe6f72bfb97b682a608c8`  
		Last Modified: Wed, 17 Feb 2021 21:18:10 GMT  
		Size: 2.8 MB (2813081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebfde0ed2b25fdf7a28b46b01e73c7891af78bd260ce9c5f46f33a0fd4bba5a`  
		Last Modified: Thu, 18 Feb 2021 01:25:11 GMT  
		Size: 1.7 MB (1741666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c587bda2cf37683b8f80371450083e1533df270a51cbe196c845e7ab52f8943`  
		Last Modified: Thu, 18 Feb 2021 01:25:09 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2faee0918d4167a0323dba5b4244442a3d6cd88d5eacd4a560b72f056274a4`  
		Last Modified: Thu, 18 Feb 2021 01:25:10 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791bb958f337b6cf4b2ea90cf5ac9fcb4612738a152ac4a09a69335da096e59b`  
		Last Modified: Fri, 05 Mar 2021 01:49:57 GMT  
		Size: 10.4 MB (10354080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86e997f6d103c9c5f8aa990ba021777b0a7b8073db6c1aa66166630ac5fb896`  
		Last Modified: Fri, 05 Mar 2021 01:49:55 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97cf656907ab8d840227fdc0e36c17cac097192e975dbb19d8fbc99f3ddde66`  
		Last Modified: Fri, 05 Mar 2021 01:49:59 GMT  
		Size: 15.5 MB (15524632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953ac22358c5b3a72272c4db94f387dafe749dccc315fe715fd54646a7e67fa1`  
		Last Modified: Fri, 05 Mar 2021 01:49:55 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5274e31720b346823b92235766eace03c5b3ca24d9af8910eb3c00a29bc1f48e`  
		Last Modified: Fri, 05 Mar 2021 01:49:56 GMT  
		Size: 17.6 KB (17566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae1914ed9afaacdd2822f6ce3b21c1ba2cfc67fb0a0fc37105941301dde3979`  
		Last Modified: Fri, 05 Mar 2021 02:15:07 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097959a8b93e17b2458e2add93679e6bc07debf1b8ed2e8e39ebdb005d0de353`  
		Last Modified: Fri, 05 Mar 2021 02:15:03 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08378c640496a604d70139ba5075c5cd2fe90d0786621bc4396e7cee75634053`  
		Last Modified: Fri, 05 Mar 2021 02:15:05 GMT  
		Size: 3.9 MB (3918494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4eee7fd3e560e705de2352e9453419f436960844b5ddfda9986cedb09cd6bde`  
		Last Modified: Fri, 05 Mar 2021 02:15:03 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435b254436c62649064c5af03dfecbb978ff36ac4740efbc8a476f538850455e`  
		Last Modified: Fri, 05 Mar 2021 02:15:03 GMT  
		Size: 582.8 KB (582810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38c8209ca8c0d5b2b2b2baae2f460323d08fc90ce007eabd250244bc371189b`  
		Last Modified: Fri, 05 Mar 2021 02:15:05 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; s390x

```console
$ docker pull adminer@sha256:9035a1407febca18c25bbc2820e9ac6a09281165f387df8d135066d3bcad2d14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32764749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ff9987904c7594d2e9098e19fcc387f22c02e45e942703bd6f07ac77ebbe58`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 00:40:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Feb 2021 00:40:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 18 Feb 2021 00:40:31 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 18 Feb 2021 00:40:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Feb 2021 00:40:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 18 Feb 2021 00:40:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:40:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:40:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Feb 2021 00:51:38 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:17:53 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:17:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:17:54 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:17:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:17:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:21:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:21:14 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:21:14 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:21:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:21:15 GMT
CMD ["php" "-a"]
# Fri, 05 Mar 2021 01:35:01 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 01:35:02 GMT
STOPSIGNAL SIGINT
# Fri, 05 Mar 2021 01:35:03 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 01:35:03 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 01:35:28 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 01:35:28 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 01:35:28 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 01:35:29 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 01:35:29 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 01:35:30 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 01:35:30 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:35:31 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 01:35:31 GMT
USER adminer
# Fri, 05 Mar 2021 01:35:31 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 05 Mar 2021 01:35:31 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2eaf748a32e76be0f1aa6246cb11c8aa5022aa834df364bb87f581198e6376`  
		Last Modified: Thu, 18 Feb 2021 01:26:48 GMT  
		Size: 1.8 MB (1756400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5716be54c61b8e2a38b4d6a0cbece88801726747842f6bd1a50aaf4e8442013f`  
		Last Modified: Thu, 18 Feb 2021 01:26:48 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6aa66a8dad4ec1443c27324fc452b05c4299dbffefcebee55700880033b3ff7`  
		Last Modified: Thu, 18 Feb 2021 01:26:47 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8b7b210cf7a350eb620b3574b19324168c8c4833e0cfe3d634398782f48175`  
		Last Modified: Fri, 05 Mar 2021 00:51:36 GMT  
		Size: 10.4 MB (10354085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a066cfbe30cd983f5ffef2df9d50618ade23fe99302b69e012774b2269585d1`  
		Last Modified: Fri, 05 Mar 2021 00:51:35 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9401205bc3eb7297f85c414b790172be23d1c4ab061aee72eaeb28b69132c073`  
		Last Modified: Fri, 05 Mar 2021 00:51:38 GMT  
		Size: 13.9 MB (13860060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afee2a631a7b79b3c487a3ef4500ea44fa978bd6464fe317d1a65d4b104f7309`  
		Last Modified: Fri, 05 Mar 2021 00:51:35 GMT  
		Size: 2.3 KB (2261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0499fd075a9fd055ca563a90fb4b2aaac9056a65b191d7db41c37188db098cf1`  
		Last Modified: Fri, 05 Mar 2021 00:51:35 GMT  
		Size: 17.6 KB (17566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b53123be7d4a2e60f8c580951db7f413a3fddabf032b97cc4e1715defe06aa`  
		Last Modified: Fri, 05 Mar 2021 01:36:37 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aab483619f81007684651c4b32aae7e47300c44374d5a2e165bfee97c9a5ed8`  
		Last Modified: Fri, 05 Mar 2021 01:36:35 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21994edf819ad8eed5eea7af018652abc984e3d7f67f6dd34ead1779f80b961c`  
		Last Modified: Fri, 05 Mar 2021 01:36:35 GMT  
		Size: 3.6 MB (3583473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39598f68be044d39764fd4f2c72cccb6ff39c29081b324413fb9af80f22c6b6`  
		Last Modified: Fri, 05 Mar 2021 01:36:35 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6988f4418691c53ad239170a2ec56313d0be5ebf6636151c2ab31dee05fd76`  
		Last Modified: Fri, 05 Mar 2021 01:36:35 GMT  
		Size: 582.8 KB (582811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f94af1afe9ebb57211f0f17af8d7edc0ccf29b7fe0f188bae543435432d960`  
		Last Modified: Fri, 05 Mar 2021 01:36:35 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.8.0`

```console
$ docker pull adminer@sha256:1ee6ed00d1169a14a1030a1d44a5ab1724392c115d296d98f0a0e8700628deeb
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

### `adminer:4.8.0` - linux; amd64

```console
$ docker pull adminer@sha256:d7cbbb92e43f7d55027a58bd115d9425548325f3754cb705b03368243b3930d3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.6 MB (33625851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d5528d5e4b1e1e879cf6d3b49b09245873a231a6054521f40a538633893e3d`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 03:21:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 06 Mar 2021 03:21:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 06 Mar 2021 03:21:31 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 06 Mar 2021 03:21:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 06 Mar 2021 03:21:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 06 Mar 2021 03:21:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 03:21:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 03:21:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 06 Mar 2021 04:18:25 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Sat, 06 Mar 2021 04:18:25 GMT
ENV PHP_VERSION=7.4.16
# Sat, 06 Mar 2021 04:18:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Sat, 06 Mar 2021 04:18:26 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Sat, 06 Mar 2021 04:18:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 06 Mar 2021 04:18:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Mar 2021 04:25:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Mar 2021 04:25:46 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Sat, 06 Mar 2021 04:25:48 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Mar 2021 04:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Mar 2021 04:25:49 GMT
CMD ["php" "-a"]
# Sat, 06 Mar 2021 08:51:16 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 06 Mar 2021 08:51:16 GMT
STOPSIGNAL SIGINT
# Sat, 06 Mar 2021 08:51:17 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 06 Mar 2021 08:51:17 GMT
WORKDIR /var/www/html
# Sat, 06 Mar 2021 08:51:43 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 06 Mar 2021 08:51:43 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Sat, 06 Mar 2021 08:51:43 GMT
ENV ADMINER_VERSION=4.8.0
# Sat, 06 Mar 2021 08:51:44 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Sat, 06 Mar 2021 08:51:44 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Sat, 06 Mar 2021 08:51:46 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 06 Mar 2021 08:51:46 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 06 Mar 2021 08:51:46 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 06 Mar 2021 08:51:46 GMT
USER adminer
# Sat, 06 Mar 2021 08:51:46 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 06 Mar 2021 08:51:47 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743181516422399af3888ad5df44c6f711f992b2f86288db9e191ae13de99fa0`  
		Last Modified: Sat, 06 Mar 2021 06:31:08 GMT  
		Size: 1.7 MB (1694870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c307b60e377a3903f74fd9cde3ad69f754071faac36f81ca74e1aa9eabe4851`  
		Last Modified: Sat, 06 Mar 2021 06:31:08 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d5b43308915ce3198dec1c19aa88719afacff02c85660a952982856a0bcc9c`  
		Last Modified: Sat, 06 Mar 2021 06:31:08 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4848a1e010e4e0cda8de291fa6ed2f3efecf20d7343a69cec21878885828d2d`  
		Last Modified: Sat, 06 Mar 2021 06:35:54 GMT  
		Size: 10.4 MB (10354097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8e88ab7b4e15d3c4d8d099845669643447a702d27188138ed20f8c14879cde`  
		Last Modified: Sat, 06 Mar 2021 06:35:54 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c6688ec4022c9042fad0bff0a5aaa03cd55628577fe71a419761ca5478392c`  
		Last Modified: Sat, 06 Mar 2021 06:35:56 GMT  
		Size: 14.3 MB (14253596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b401e642cd6c785a0ede5899c8a1fb93770d6eaf04a0a5faeb0183ad5c21f3`  
		Last Modified: Sat, 06 Mar 2021 06:35:54 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4aa45ba156c9e4af51f7b2a5eec317be47eca6ba8e9bb8fc368488ea41c11c`  
		Last Modified: Sat, 06 Mar 2021 06:35:54 GMT  
		Size: 17.5 KB (17518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b686977c50b0410c0084a21bef42aae47c53441ee7defe7b25bcad585a19999`  
		Last Modified: Sat, 06 Mar 2021 08:52:42 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf15bf71cdf8a60508b2773274a23124c80de6ad9611b97bd532869bdce6929`  
		Last Modified: Sat, 06 Mar 2021 08:52:38 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7855e8a455940ec1b6c2e7a9d42e3a94e92b3f7dd253bfdefd2ef4f0b272a242`  
		Last Modified: Sat, 06 Mar 2021 08:52:40 GMT  
		Size: 3.9 MB (3903349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff73275236b8945efe2dadf9b67d73cc5c24fb699f0e3265cbdb3445bdabcba`  
		Last Modified: Sat, 06 Mar 2021 08:52:38 GMT  
		Size: 1.5 KB (1471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64cfef0d91dbc6948021e94ae4407132c018d08d4446215342ad7e0447e33383`  
		Last Modified: Sat, 06 Mar 2021 08:52:39 GMT  
		Size: 582.8 KB (582798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7097b3e809e2d58f970ecec3070fa3db82d914e74c47172eb2c2800e051290`  
		Last Modified: Sat, 06 Mar 2021 08:52:39 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.0` - linux; arm variant v6

```console
$ docker pull adminer@sha256:67ecf13bed27733de831bad0889ec483ede8530402c3c46011d2334e4a991c25
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32352290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4b093e53cd99d8904355485561c5dd006e3077e79bf2eaba849078b7c8ff3b`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:17:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Feb 2021 22:17:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 17 Feb 2021 22:17:15 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Feb 2021 22:17:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Feb 2021 22:17:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Feb 2021 22:17:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:17:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:17:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Feb 2021 22:24:49 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:22:42 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:22:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:22:48 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:22:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:23:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:26:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:26:24 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:26:28 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:26:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:26:30 GMT
CMD ["php" "-a"]
# Fri, 05 Mar 2021 01:28:12 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 01:28:12 GMT
STOPSIGNAL SIGINT
# Fri, 05 Mar 2021 01:28:15 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 01:28:15 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 01:29:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 01:29:05 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 01:29:06 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 01:29:07 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 01:29:08 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 01:29:11 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 01:29:11 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:29:12 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 01:29:13 GMT
USER adminer
# Fri, 05 Mar 2021 01:29:13 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 05 Mar 2021 01:29:14 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a33e390360f607fe5a7fe0a0203b7347693b0d8cab270352594a3700e1a1d0`  
		Last Modified: Wed, 17 Feb 2021 22:57:10 GMT  
		Size: 1.7 MB (1684729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d1bbb88bd210deaf33702df9d6fa7f35e72f23dfbb55196147ab537320e9f3`  
		Last Modified: Wed, 17 Feb 2021 22:57:09 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b99fbc527c373db47c36282e5bbd82010870902db2af45982bbb8d700375a32`  
		Last Modified: Wed, 17 Feb 2021 22:57:09 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37a52f8d6a0669099c893e2b3e9ce5d8862eed5489a15f8dafd39f664233b7c`  
		Last Modified: Fri, 05 Mar 2021 00:53:01 GMT  
		Size: 10.4 MB (10354085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e31438bda764d2d788352c3dbdc563f97c840ce2736c283190e590e11a4641`  
		Last Modified: Fri, 05 Mar 2021 00:52:59 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615508ce208f1bfacc67745161a522490ffde3254a7e5b88e2a75704a178b65d`  
		Last Modified: Fri, 05 Mar 2021 00:53:05 GMT  
		Size: 13.5 MB (13479609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49bab722652cd2c45df88dee34d635b0c4824fd1885e9cdb6fa1ad1c707b24d`  
		Last Modified: Fri, 05 Mar 2021 00:52:59 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b5e7fa68211b0722b528ee1f7b5f413c32b3581eec56fc37d056cf1e44d45f`  
		Last Modified: Fri, 05 Mar 2021 00:52:59 GMT  
		Size: 17.6 KB (17574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a863fe1948ed188002b2c53e19c1c4f06aa611913e9aee2e6d37a4b38892fa27`  
		Last Modified: Fri, 05 Mar 2021 01:31:18 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e5d7f207dfb0131e75fb5675de4013a21ec2a9965b6a5f2974a09de577b376`  
		Last Modified: Fri, 05 Mar 2021 01:31:15 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613aba5afd5742d6a2f8c093d4d9e2e3eef9f92d01853c139b3f7690a577fd1d`  
		Last Modified: Fri, 05 Mar 2021 01:31:16 GMT  
		Size: 3.6 MB (3603470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ea9f569f958143bd38a220ee729c6ef6f85c122fe3f42b2a761b57e39df3e9`  
		Last Modified: Fri, 05 Mar 2021 01:31:15 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e6944e336be980c37b3af333b01dab0f1b3db12af184e3cc0ed1d4a326a6ab`  
		Last Modified: Fri, 05 Mar 2021 01:31:15 GMT  
		Size: 582.8 KB (582808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4644911e6f4e52234e1b7b359c25f4998c5be8fe108e2f0b54e5cfd721d2d9`  
		Last Modified: Fri, 05 Mar 2021 01:31:15 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.0` - linux; arm variant v7

```console
$ docker pull adminer@sha256:3c5fe027a505612b8c787c41923bc81f01eba12776b7827fb8de3b48fadd12ff
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31126385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7625601231cbbafd93c468bb5506f91c320be7c6640088ec3203f7b61bcae845`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:56:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Feb 2021 22:57:00 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 17 Feb 2021 22:57:04 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Feb 2021 22:57:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Feb 2021 22:57:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Feb 2021 22:57:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:57:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:57:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Feb 2021 23:07:25 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:51:51 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:51:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:51:52 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:51:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:51:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:54:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:54:56 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:55:00 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:55:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:55:01 GMT
CMD ["php" "-a"]
# Fri, 05 Mar 2021 03:16:34 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 03:16:35 GMT
STOPSIGNAL SIGINT
# Fri, 05 Mar 2021 03:16:37 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 03:16:37 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 03:17:32 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 03:17:34 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 03:17:35 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 03:17:36 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 03:17:36 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 03:17:39 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 03:17:40 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 03:17:41 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 03:17:42 GMT
USER adminer
# Fri, 05 Mar 2021 03:17:42 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 05 Mar 2021 03:17:43 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf491575714634902d01e3e48f3b92702cb2e4c42056aa5421058d2a2cbfd9f6`  
		Last Modified: Wed, 17 Feb 2021 23:33:58 GMT  
		Size: 1.6 MB (1555125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8ae33f1196d3a62a9383b30d3fd81dd4be1bcf1a99a3d928f585b0d85c5408`  
		Last Modified: Wed, 17 Feb 2021 23:33:58 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16bd16ac2dc3896b7ddf5e8e50bafcc3990d8313dc26634a51beafc97cc6374`  
		Last Modified: Wed, 17 Feb 2021 23:33:58 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224ef988837049de958e2e9476510f82fe8e42270706a0671a5a463f6ae97dc2`  
		Last Modified: Fri, 05 Mar 2021 01:20:19 GMT  
		Size: 10.4 MB (10354091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9e75985cf89dec0ed12206b36f371ffbda22ccf6cdbccf5d19345e62db2c14`  
		Last Modified: Fri, 05 Mar 2021 01:20:16 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3067a7094a3949ddb39a5787e92b263164d2eb287f0d508c0497dc270667f7a2`  
		Last Modified: Fri, 05 Mar 2021 01:20:19 GMT  
		Size: 12.6 MB (12608573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e967fccc5675136a3112da05f19624319efe2274faf250ffc942f8df1727990b`  
		Last Modified: Fri, 05 Mar 2021 01:20:15 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bee2c4ad784aa0aa254a050c45062e42eae3e6414649f1e7372db7fe0845817`  
		Last Modified: Fri, 05 Mar 2021 01:20:15 GMT  
		Size: 17.6 KB (17556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd957d7c1659b87bbacdaaa44de1493cd86ce1058104890fa7f886c244af7e2`  
		Last Modified: Fri, 05 Mar 2021 03:19:23 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a9b53808941e232e796f0fce8be1b1a2bdab2ab0d1227f671cdc2e6d8acecd`  
		Last Modified: Fri, 05 Mar 2021 03:19:21 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b983fd5f2f41ac862e588d3c7cb994ae11a6d4dfd1273298d35ff8fcdc87e72`  
		Last Modified: Fri, 05 Mar 2021 03:19:21 GMT  
		Size: 3.6 MB (3576366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957ff1dc0df9c3cd0fa022e0ae444a04b77d5b488a38dcba9673c2f3dfb07f8d`  
		Last Modified: Fri, 05 Mar 2021 03:19:21 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d418e42a87cf9ea044ec23d04a0b56e7f7b51dbab5639eb0e1c16248b88575`  
		Last Modified: Fri, 05 Mar 2021 03:19:21 GMT  
		Size: 582.8 KB (582806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1688bcdb1a112479d4950eae42069fa29ff4e81e587b2387362b4a6cc0fbe2`  
		Last Modified: Fri, 05 Mar 2021 03:19:21 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.0` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:7991be9e1a1ee3f2c5d374475d3746026dd7ca64a60167a65551567d7cfccf43
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33506242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11682bbe518b1faa63b82b75d246e7c35612d6d253da8f2011c0539c5b07f5cc`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 23:42:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Feb 2021 23:42:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 17 Feb 2021 23:42:38 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Feb 2021 23:42:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Feb 2021 23:42:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Feb 2021 23:42:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 23:42:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 23:42:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Feb 2021 23:53:01 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:37:35 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:37:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:37:38 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:37:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:37:47 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:42:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:42:39 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:42:44 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:42:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:42:47 GMT
CMD ["php" "-a"]
# Fri, 05 Mar 2021 02:04:43 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 02:04:44 GMT
STOPSIGNAL SIGINT
# Fri, 05 Mar 2021 02:04:48 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 02:04:50 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 02:05:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 02:05:56 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 02:05:57 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 02:05:57 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 02:05:58 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 02:06:02 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 02:06:03 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 02:06:04 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 02:06:05 GMT
USER adminer
# Fri, 05 Mar 2021 02:06:06 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 05 Mar 2021 02:06:06 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4b642bcaaef409203aaedc803835562ee86d3ea457bf4ccdd22e5d7b2367f1`  
		Last Modified: Thu, 18 Feb 2021 00:23:35 GMT  
		Size: 1.7 MB (1694455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ea39643e14bb66b107bb23b02b8c7a193ed89d38f4ae52b1decbe763fb0db9`  
		Last Modified: Thu, 18 Feb 2021 00:23:34 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3455119714d8ce066305d3b121e103a3cf690db26bb556906ba67e7a7c1f559`  
		Last Modified: Thu, 18 Feb 2021 00:23:34 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a68a1ddf490519ddbcd4f75589909c8d4703a6b902bae2a7319905984b7547`  
		Last Modified: Fri, 05 Mar 2021 01:13:32 GMT  
		Size: 10.4 MB (10354115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1754592c0391f5b7b27cf3c7110b1e2a917ebb769b0ceaf9bfdfd0181cc6cb`  
		Last Modified: Fri, 05 Mar 2021 01:13:30 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a402e34d4d52011f5ecf29a826d7fd94dc474fdf156b70d506d3deaeb2a4d3b`  
		Last Modified: Fri, 05 Mar 2021 01:13:34 GMT  
		Size: 14.3 MB (14263146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1702d0137849d4baf63d0536ee9f8391c72c295a46613ed43c270f3cc81a90`  
		Last Modified: Fri, 05 Mar 2021 01:13:31 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ebe5152320826ffaea66119f3e759ce05ed98bb09a201643ee6674cbd9685e`  
		Last Modified: Fri, 05 Mar 2021 01:13:31 GMT  
		Size: 17.6 KB (17574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a42655d4ea3811b755ccede7be6704d6e30a4e912c6ec284807f25e1874c11`  
		Last Modified: Fri, 05 Mar 2021 02:08:13 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36983a97af0e64abf039823af9b57936cc5add643fab48f1d64ca7fbeb076a02`  
		Last Modified: Fri, 05 Mar 2021 02:08:11 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23c53be365e785ad30481daf9c58f08857ca80fc5fc681e12655557a14f7093`  
		Last Modified: Fri, 05 Mar 2021 02:08:12 GMT  
		Size: 3.9 MB (3874584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d698ddfcb363647524ac96d6fe45138e9aa228c8662ec68d2c877a5862a6257`  
		Last Modified: Fri, 05 Mar 2021 02:08:11 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e7497f33585536dba243eedb8aea95c51b88677f674845065a15d776a0e7c78`  
		Last Modified: Fri, 05 Mar 2021 02:08:12 GMT  
		Size: 582.8 KB (582809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041eab10d184403fbf0b2a94255c47e5618bc99fd708586209ad66d02a41c86b`  
		Last Modified: Fri, 05 Mar 2021 02:08:11 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.0` - linux; 386

```console
$ docker pull adminer@sha256:3c12e8f857cf7b920500273d347a57b13be7f75bc361cd49631704781e87dafe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34214715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8de5231523b1be5d66db42c66ace28ceef73e37457dc22956bd36744ea35592f`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 02:13:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 06 Mar 2021 02:13:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 06 Mar 2021 02:13:32 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 06 Mar 2021 02:13:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 06 Mar 2021 02:13:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 06 Mar 2021 02:13:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 02:13:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 02:13:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 06 Mar 2021 02:59:52 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Sat, 06 Mar 2021 02:59:52 GMT
ENV PHP_VERSION=7.4.16
# Sat, 06 Mar 2021 02:59:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Sat, 06 Mar 2021 02:59:53 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Sat, 06 Mar 2021 03:00:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 06 Mar 2021 03:00:19 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Mar 2021 03:08:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Mar 2021 03:08:56 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Sat, 06 Mar 2021 03:08:58 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Mar 2021 03:08:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Mar 2021 03:08:58 GMT
CMD ["php" "-a"]
# Sat, 06 Mar 2021 08:16:03 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 06 Mar 2021 08:16:03 GMT
STOPSIGNAL SIGINT
# Sat, 06 Mar 2021 08:16:04 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 06 Mar 2021 08:16:04 GMT
WORKDIR /var/www/html
# Sat, 06 Mar 2021 08:16:34 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 06 Mar 2021 08:16:34 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Sat, 06 Mar 2021 08:16:34 GMT
ENV ADMINER_VERSION=4.8.0
# Sat, 06 Mar 2021 08:16:34 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Sat, 06 Mar 2021 08:16:35 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Sat, 06 Mar 2021 08:16:37 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 06 Mar 2021 08:16:38 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 06 Mar 2021 08:16:38 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 06 Mar 2021 08:16:38 GMT
USER adminer
# Sat, 06 Mar 2021 08:16:38 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 06 Mar 2021 08:16:38 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d779edf81d3549de0c570804cffa8279f4a980d3fed1292285070f24a1b00f`  
		Last Modified: Sat, 06 Mar 2021 05:47:24 GMT  
		Size: 1.8 MB (1793700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce9d30537e4bf7ab9ad24ea334671e794e0830680c386cf4b36dbba54dd40c5`  
		Last Modified: Sat, 06 Mar 2021 05:47:23 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f119038c35efd6cc0b1a27c432b2fc338da413650c224359556d95e0bf8214`  
		Last Modified: Sat, 06 Mar 2021 05:47:23 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:125aeed6c18a6c28cf608d3c3cd80094c61ed4f9023855f9c3ac4993f1542907`  
		Last Modified: Sat, 06 Mar 2021 05:53:56 GMT  
		Size: 10.4 MB (10354073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05563330040dc337869b22ab8c267fc06fa14139a5f270679e69ba3a718896b5`  
		Last Modified: Sat, 06 Mar 2021 05:53:53 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567f9a9d037948e123fbbec64dfb76f7cca9d30cd3e5526abc597b65fd39656b`  
		Last Modified: Sat, 06 Mar 2021 05:54:00 GMT  
		Size: 14.6 MB (14630287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28b3a57348334ee91df9b04ec97e570fcff52d0a9fa3e3ec3247823d80a437d`  
		Last Modified: Sat, 06 Mar 2021 05:53:53 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0621d49125fecbf6f64ac583fbf7c76034bc51eed48c69516922c398d93a6c`  
		Last Modified: Sat, 06 Mar 2021 05:53:54 GMT  
		Size: 17.5 KB (17501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c703587ef05b977c127d751c1c78fa472b5ddb67b5ac217ac20ea90cd8855c`  
		Last Modified: Sat, 06 Mar 2021 08:17:58 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e848e2757b70b020801c677c59e10e8709f14f3f76f32d2b1be5f95679f4f6c5`  
		Last Modified: Sat, 06 Mar 2021 08:17:54 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f2ac401974d5ea19f7f375960da2a7a6c77f23dab4135c4bd95c4dc64f9d02`  
		Last Modified: Sat, 06 Mar 2021 08:17:55 GMT  
		Size: 4.0 MB (4010207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cb78f666be732b2b10b604df1cb578ad8ccca1445c29fd5bab4ba346f29247`  
		Last Modified: Sat, 06 Mar 2021 08:17:54 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980181a00a928280cf2288da2498d06c9203508ce40aa0aed05b1a2be94ae1ce`  
		Last Modified: Sat, 06 Mar 2021 08:17:54 GMT  
		Size: 582.8 KB (582807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0865a1f7fbcf5062e0b5b2fc87b6ea55d2e4c094297f6139e110bbc7a1c9794`  
		Last Modified: Sat, 06 Mar 2021 08:17:54 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.0` - linux; ppc64le

```console
$ docker pull adminer@sha256:f8ed36e984e53d541d8f690681208acc65c3b6e90ac3830c51e821eeb7b24951
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (34960311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0819898f5e08afcbb1041ea1c325869490d997fe19fcaa3e93b720312272db4`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 21:17:29 GMT
ADD file:28f4377c61c0f8eb43a6b36e6a24ef5893f51d405d25b62e364988223537ae0b in / 
# Wed, 17 Feb 2021 21:17:37 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 00:23:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Feb 2021 00:24:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 18 Feb 2021 00:24:44 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 18 Feb 2021 00:24:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Feb 2021 00:25:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 18 Feb 2021 00:25:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:25:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:25:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Feb 2021 00:40:47 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 01:05:36 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 01:05:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 01:05:52 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 01:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 01:06:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:11:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 01:11:19 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:11:29 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 01:11:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 01:11:46 GMT
CMD ["php" "-a"]
# Fri, 05 Mar 2021 02:08:50 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 02:09:05 GMT
STOPSIGNAL SIGINT
# Fri, 05 Mar 2021 02:09:23 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 02:09:30 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 02:10:27 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 02:10:29 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 02:10:33 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 02:10:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 02:10:56 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 02:11:23 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 02:11:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 02:11:34 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 02:11:42 GMT
USER adminer
# Fri, 05 Mar 2021 02:11:57 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 05 Mar 2021 02:12:05 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:cb672e0375a8f9bb3d33049ceb372ffa49b959bfc84fe6f72bfb97b682a608c8`  
		Last Modified: Wed, 17 Feb 2021 21:18:10 GMT  
		Size: 2.8 MB (2813081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebfde0ed2b25fdf7a28b46b01e73c7891af78bd260ce9c5f46f33a0fd4bba5a`  
		Last Modified: Thu, 18 Feb 2021 01:25:11 GMT  
		Size: 1.7 MB (1741666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c587bda2cf37683b8f80371450083e1533df270a51cbe196c845e7ab52f8943`  
		Last Modified: Thu, 18 Feb 2021 01:25:09 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2faee0918d4167a0323dba5b4244442a3d6cd88d5eacd4a560b72f056274a4`  
		Last Modified: Thu, 18 Feb 2021 01:25:10 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791bb958f337b6cf4b2ea90cf5ac9fcb4612738a152ac4a09a69335da096e59b`  
		Last Modified: Fri, 05 Mar 2021 01:49:57 GMT  
		Size: 10.4 MB (10354080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86e997f6d103c9c5f8aa990ba021777b0a7b8073db6c1aa66166630ac5fb896`  
		Last Modified: Fri, 05 Mar 2021 01:49:55 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97cf656907ab8d840227fdc0e36c17cac097192e975dbb19d8fbc99f3ddde66`  
		Last Modified: Fri, 05 Mar 2021 01:49:59 GMT  
		Size: 15.5 MB (15524632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953ac22358c5b3a72272c4db94f387dafe749dccc315fe715fd54646a7e67fa1`  
		Last Modified: Fri, 05 Mar 2021 01:49:55 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5274e31720b346823b92235766eace03c5b3ca24d9af8910eb3c00a29bc1f48e`  
		Last Modified: Fri, 05 Mar 2021 01:49:56 GMT  
		Size: 17.6 KB (17566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae1914ed9afaacdd2822f6ce3b21c1ba2cfc67fb0a0fc37105941301dde3979`  
		Last Modified: Fri, 05 Mar 2021 02:15:07 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097959a8b93e17b2458e2add93679e6bc07debf1b8ed2e8e39ebdb005d0de353`  
		Last Modified: Fri, 05 Mar 2021 02:15:03 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08378c640496a604d70139ba5075c5cd2fe90d0786621bc4396e7cee75634053`  
		Last Modified: Fri, 05 Mar 2021 02:15:05 GMT  
		Size: 3.9 MB (3918494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4eee7fd3e560e705de2352e9453419f436960844b5ddfda9986cedb09cd6bde`  
		Last Modified: Fri, 05 Mar 2021 02:15:03 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435b254436c62649064c5af03dfecbb978ff36ac4740efbc8a476f538850455e`  
		Last Modified: Fri, 05 Mar 2021 02:15:03 GMT  
		Size: 582.8 KB (582810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38c8209ca8c0d5b2b2b2baae2f460323d08fc90ce007eabd250244bc371189b`  
		Last Modified: Fri, 05 Mar 2021 02:15:05 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.0` - linux; s390x

```console
$ docker pull adminer@sha256:9035a1407febca18c25bbc2820e9ac6a09281165f387df8d135066d3bcad2d14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32764749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ff9987904c7594d2e9098e19fcc387f22c02e45e942703bd6f07ac77ebbe58`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 00:40:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Feb 2021 00:40:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 18 Feb 2021 00:40:31 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 18 Feb 2021 00:40:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Feb 2021 00:40:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 18 Feb 2021 00:40:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:40:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:40:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Feb 2021 00:51:38 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:17:53 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:17:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:17:54 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:17:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:17:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:21:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:21:14 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:21:14 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:21:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:21:15 GMT
CMD ["php" "-a"]
# Fri, 05 Mar 2021 01:35:01 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 01:35:02 GMT
STOPSIGNAL SIGINT
# Fri, 05 Mar 2021 01:35:03 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 01:35:03 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 01:35:28 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 01:35:28 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 01:35:28 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 01:35:29 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 01:35:29 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 01:35:30 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 01:35:30 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:35:31 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 01:35:31 GMT
USER adminer
# Fri, 05 Mar 2021 01:35:31 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 05 Mar 2021 01:35:31 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2eaf748a32e76be0f1aa6246cb11c8aa5022aa834df364bb87f581198e6376`  
		Last Modified: Thu, 18 Feb 2021 01:26:48 GMT  
		Size: 1.8 MB (1756400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5716be54c61b8e2a38b4d6a0cbece88801726747842f6bd1a50aaf4e8442013f`  
		Last Modified: Thu, 18 Feb 2021 01:26:48 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6aa66a8dad4ec1443c27324fc452b05c4299dbffefcebee55700880033b3ff7`  
		Last Modified: Thu, 18 Feb 2021 01:26:47 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8b7b210cf7a350eb620b3574b19324168c8c4833e0cfe3d634398782f48175`  
		Last Modified: Fri, 05 Mar 2021 00:51:36 GMT  
		Size: 10.4 MB (10354085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a066cfbe30cd983f5ffef2df9d50618ade23fe99302b69e012774b2269585d1`  
		Last Modified: Fri, 05 Mar 2021 00:51:35 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9401205bc3eb7297f85c414b790172be23d1c4ab061aee72eaeb28b69132c073`  
		Last Modified: Fri, 05 Mar 2021 00:51:38 GMT  
		Size: 13.9 MB (13860060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afee2a631a7b79b3c487a3ef4500ea44fa978bd6464fe317d1a65d4b104f7309`  
		Last Modified: Fri, 05 Mar 2021 00:51:35 GMT  
		Size: 2.3 KB (2261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0499fd075a9fd055ca563a90fb4b2aaac9056a65b191d7db41c37188db098cf1`  
		Last Modified: Fri, 05 Mar 2021 00:51:35 GMT  
		Size: 17.6 KB (17566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b53123be7d4a2e60f8c580951db7f413a3fddabf032b97cc4e1715defe06aa`  
		Last Modified: Fri, 05 Mar 2021 01:36:37 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aab483619f81007684651c4b32aae7e47300c44374d5a2e165bfee97c9a5ed8`  
		Last Modified: Fri, 05 Mar 2021 01:36:35 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21994edf819ad8eed5eea7af018652abc984e3d7f67f6dd34ead1779f80b961c`  
		Last Modified: Fri, 05 Mar 2021 01:36:35 GMT  
		Size: 3.6 MB (3583473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39598f68be044d39764fd4f2c72cccb6ff39c29081b324413fb9af80f22c6b6`  
		Last Modified: Fri, 05 Mar 2021 01:36:35 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6988f4418691c53ad239170a2ec56313d0be5ebf6636151c2ab31dee05fd76`  
		Last Modified: Fri, 05 Mar 2021 01:36:35 GMT  
		Size: 582.8 KB (582811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f94af1afe9ebb57211f0f17af8d7edc0ccf29b7fe0f188bae543435432d960`  
		Last Modified: Fri, 05 Mar 2021 01:36:35 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.8.0-fastcgi`

```console
$ docker pull adminer@sha256:ddbc8ec701aaf2deafbf06f680f3a1d2cd9b1fffb94d27c1f4395ad50008d9de
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

### `adminer:4.8.0-fastcgi` - linux; amd64

```console
$ docker pull adminer@sha256:bc5ef236fdce0cdf13798c6ce77033b0c9b0946a2b1e93de5e6f43a64b82d004
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33700229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7d4c6e1f2444f36f3d32007c33a6c9cd065f53a81670922522b88fa93450db`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 03:21:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 06 Mar 2021 03:21:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 06 Mar 2021 03:21:31 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 06 Mar 2021 03:21:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 06 Mar 2021 03:21:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 06 Mar 2021 03:31:10 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 06 Mar 2021 03:31:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 03:31:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 03:31:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 06 Mar 2021 04:25:55 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Sat, 06 Mar 2021 04:25:55 GMT
ENV PHP_VERSION=7.4.16
# Sat, 06 Mar 2021 04:25:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Sat, 06 Mar 2021 04:25:56 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Sat, 06 Mar 2021 04:26:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 06 Mar 2021 04:26:02 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Mar 2021 04:33:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Mar 2021 04:33:18 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Sat, 06 Mar 2021 04:33:20 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Mar 2021 04:33:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Mar 2021 04:33:21 GMT
WORKDIR /var/www/html
# Sat, 06 Mar 2021 04:33:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Sat, 06 Mar 2021 04:33:23 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 04:33:23 GMT
EXPOSE 9000
# Sat, 06 Mar 2021 04:33:23 GMT
CMD ["php-fpm"]
# Sat, 06 Mar 2021 08:51:52 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 06 Mar 2021 08:51:53 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 06 Mar 2021 08:52:18 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 06 Mar 2021 08:52:18 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Sat, 06 Mar 2021 08:52:18 GMT
ENV ADMINER_VERSION=4.8.0
# Sat, 06 Mar 2021 08:52:19 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Sat, 06 Mar 2021 08:52:19 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Sat, 06 Mar 2021 08:52:20 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 06 Mar 2021 08:52:21 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 06 Mar 2021 08:52:21 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 06 Mar 2021 08:52:21 GMT
USER adminer
# Sat, 06 Mar 2021 08:52:21 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743181516422399af3888ad5df44c6f711f992b2f86288db9e191ae13de99fa0`  
		Last Modified: Sat, 06 Mar 2021 06:31:08 GMT  
		Size: 1.7 MB (1694870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c307b60e377a3903f74fd9cde3ad69f754071faac36f81ca74e1aa9eabe4851`  
		Last Modified: Sat, 06 Mar 2021 06:31:08 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d5b43308915ce3198dec1c19aa88719afacff02c85660a952982856a0bcc9c`  
		Last Modified: Sat, 06 Mar 2021 06:31:08 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9d5f24e6dd6af8f23f239240af8081c566914e78925b8646ee59d456477a1b`  
		Last Modified: Sat, 06 Mar 2021 06:36:44 GMT  
		Size: 10.4 MB (10354098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfaad94f9a19bca51025c93a5b36fbf3c4e2636a37ecf935233cff9afc27f94`  
		Last Modified: Sat, 06 Mar 2021 06:36:41 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3507948cfcd59468730f9f8ae89b321891415ae8f7c98d96b4662c057f5af471`  
		Last Modified: Sat, 06 Mar 2021 06:36:44 GMT  
		Size: 14.3 MB (14319531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f880a2fb467d3c5d725b4ef31da9c50bcd19a9171455db7a0d4a80a9f80395e`  
		Last Modified: Sat, 06 Mar 2021 06:36:40 GMT  
		Size: 2.3 KB (2265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56deb6830b6ed046fb324d5539b34742ee0aa32484cf961c9fbd5c47aca9a930`  
		Last Modified: Sat, 06 Mar 2021 06:36:41 GMT  
		Size: 17.5 KB (17521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a194189cbad21888697c3cee4fca8f4d5ac096f5ac1eb2981e77d310fa63d6f`  
		Last Modified: Sat, 06 Mar 2021 06:36:40 GMT  
		Size: 8.4 KB (8448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d93b56dad37e253e7efcccf4f4bc0c55f1093fe4a3ee4743ae53353d77a4fb`  
		Last Modified: Sat, 06 Mar 2021 08:53:09 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238c4c0f49a87323787cdbdc3bd37ed5b43bd67fd3d903a5efc67f049bde2cb0`  
		Last Modified: Sat, 06 Mar 2021 08:53:07 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ed295294c14844d5fa520952a46cc832ea9192ab54ceebcd9da78c2b835dd3`  
		Last Modified: Sat, 06 Mar 2021 08:53:07 GMT  
		Size: 3.9 MB (3903344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285104d31a4786a761bed245e8a819ffccb92919702026f95ab8874eaeb112a0`  
		Last Modified: Sat, 06 Mar 2021 08:53:07 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ef4cb5580635a144f2bbf3d755884632850d26926d5b90840cbab8b1642886`  
		Last Modified: Sat, 06 Mar 2021 08:53:08 GMT  
		Size: 582.8 KB (582795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f853ae8f0e76e3efc1e422db5915507f4f50c611294e9c5492f775bd0ecb1f`  
		Last Modified: Sat, 06 Mar 2021 08:53:07 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.0-fastcgi` - linux; arm variant v6

```console
$ docker pull adminer@sha256:2c93d2f0b02908d29d3e3a4228ab25c9c86b812331b270e390a62a9680ff1433
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32424063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f018255660e0906d91baef706cff1811a4410856b0a37263b715383bb70fdcdc`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:17:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Feb 2021 22:17:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 17 Feb 2021 22:17:15 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Feb 2021 22:17:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Feb 2021 22:17:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Feb 2021 22:20:46 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Wed, 17 Feb 2021 22:20:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:20:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:20:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Feb 2021 22:28:41 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:26:48 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:26:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:26:54 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:27:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:27:04 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:30:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:30:26 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:30:30 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:30:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:30:35 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 00:30:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 05 Mar 2021 00:30:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Mar 2021 00:30:42 GMT
EXPOSE 9000
# Fri, 05 Mar 2021 00:30:43 GMT
CMD ["php-fpm"]
# Fri, 05 Mar 2021 01:29:31 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 01:29:34 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 01:30:26 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 01:30:28 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 01:30:32 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 01:30:33 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 01:30:34 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 01:30:38 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 01:30:40 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:30:41 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 01:30:42 GMT
USER adminer
# Fri, 05 Mar 2021 01:30:43 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a33e390360f607fe5a7fe0a0203b7347693b0d8cab270352594a3700e1a1d0`  
		Last Modified: Wed, 17 Feb 2021 22:57:10 GMT  
		Size: 1.7 MB (1684729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d1bbb88bd210deaf33702df9d6fa7f35e72f23dfbb55196147ab537320e9f3`  
		Last Modified: Wed, 17 Feb 2021 22:57:09 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b99fbc527c373db47c36282e5bbd82010870902db2af45982bbb8d700375a32`  
		Last Modified: Wed, 17 Feb 2021 22:57:09 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a4e6f92ba693a7496c53317c79fb8823ac45b33556818a381ca1acb347a311`  
		Last Modified: Fri, 05 Mar 2021 00:53:29 GMT  
		Size: 10.4 MB (10354080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64bd603e34a5bf0fa1834fd5ce8641cedb22c0847f3169c9e72e354c86124cf5`  
		Last Modified: Fri, 05 Mar 2021 00:53:26 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5a57e3834bdaac522a5cdd7b4b6477988fcf852a76cc708026ebebdf3418d8`  
		Last Modified: Fri, 05 Mar 2021 00:53:31 GMT  
		Size: 13.5 MB (13542966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f30d0b9ee8eeabfe33c8ea2c2fcafd27e5f80bcffda325ebb1846975ef034a6`  
		Last Modified: Fri, 05 Mar 2021 00:53:26 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b17255c3c925daf160f37347c78fc54f36e044e2bfd7a8e3bffe95da9645f246`  
		Last Modified: Fri, 05 Mar 2021 00:53:26 GMT  
		Size: 17.6 KB (17565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85523748d905c5ced6faebb10205d1f7d78ae3e4869ede5793c7166ed9f77aff`  
		Last Modified: Fri, 05 Mar 2021 00:53:26 GMT  
		Size: 8.4 KB (8439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1712caab329d945c3f088703ff9c4deec4090358774a7db47f0b7b99c15e87c5`  
		Last Modified: Fri, 05 Mar 2021 01:31:31 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a5a4bdd0e396fbf2a64b84a39e11daf996231c4892713b67a32e9322c81803`  
		Last Modified: Fri, 05 Mar 2021 01:31:31 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9de2c7ce4296df3731f81d52dcc5b36bd803852f0e238ca129824dc7cc262fc`  
		Last Modified: Fri, 05 Mar 2021 01:31:30 GMT  
		Size: 3.6 MB (3603477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797df658ad578348afe4e024e48bbce535519997fa3519bfaf6f43f9a3fbe08b`  
		Last Modified: Fri, 05 Mar 2021 01:31:29 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63a45dd2ec611bee4416bdce98f4eff41d3463dd6d6609a205a19133a310515`  
		Last Modified: Fri, 05 Mar 2021 01:31:30 GMT  
		Size: 582.8 KB (582797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4e6e8ef666b79da7372c6c2125bbf4aa29676e7bdafca00830339affbf7107`  
		Last Modified: Fri, 05 Mar 2021 01:31:30 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.0-fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:76344293a9cba5c4d934e1de727cfbbad24ec801c6738f8053de6f20f4042dd4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31197081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e91dadff87355741ea5395e5e6d3093bb426a290226eb1bb4da419f1036038`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:56:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Feb 2021 22:57:00 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 17 Feb 2021 22:57:04 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Feb 2021 22:57:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Feb 2021 22:57:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Feb 2021 23:02:51 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Wed, 17 Feb 2021 23:02:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 23:02:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 23:02:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Feb 2021 23:10:45 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:55:10 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:55:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:55:11 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:55:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:55:19 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:58:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:58:21 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:58:25 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:58:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:58:27 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 00:58:29 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 05 Mar 2021 00:58:30 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Mar 2021 00:58:31 GMT
EXPOSE 9000
# Fri, 05 Mar 2021 00:58:31 GMT
CMD ["php-fpm"]
# Fri, 05 Mar 2021 03:17:52 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 03:17:55 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 03:18:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 03:18:46 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 03:18:47 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 03:18:48 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 03:18:49 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 03:18:53 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 03:18:53 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 03:18:54 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 03:18:55 GMT
USER adminer
# Fri, 05 Mar 2021 03:18:56 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf491575714634902d01e3e48f3b92702cb2e4c42056aa5421058d2a2cbfd9f6`  
		Last Modified: Wed, 17 Feb 2021 23:33:58 GMT  
		Size: 1.6 MB (1555125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8ae33f1196d3a62a9383b30d3fd81dd4be1bcf1a99a3d928f585b0d85c5408`  
		Last Modified: Wed, 17 Feb 2021 23:33:58 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16bd16ac2dc3896b7ddf5e8e50bafcc3990d8313dc26634a51beafc97cc6374`  
		Last Modified: Wed, 17 Feb 2021 23:33:58 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d01524e4fc3d179f93abe7a61fc071ecdf6c581f749d96a60690840a8fa15a`  
		Last Modified: Fri, 05 Mar 2021 01:20:43 GMT  
		Size: 10.4 MB (10354089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada63173b828bcc3b5e7d7d61a96a1a4f0a3af46ad66848c75181167c6302b6c`  
		Last Modified: Fri, 05 Mar 2021 01:20:40 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a644dd136e4a568009bc8751ede1d9017381190dc8660db4a7c91ad4bbe6cd`  
		Last Modified: Fri, 05 Mar 2021 01:20:45 GMT  
		Size: 12.7 MB (12670824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a36409e92a747f08911634d5cad27605075c881509247a1abea57e68679210`  
		Last Modified: Fri, 05 Mar 2021 01:20:40 GMT  
		Size: 2.3 KB (2263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6111685ad3b47ae7d882febd0446f781cf086d73c476fd00e53527166c5fa7`  
		Last Modified: Fri, 05 Mar 2021 01:20:40 GMT  
		Size: 17.6 KB (17565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b43d0062c0be09cf3da7b8d797ec945fa4a15872201297c8fc68c7c7fb5c0e`  
		Last Modified: Fri, 05 Mar 2021 01:20:40 GMT  
		Size: 8.4 KB (8441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce8f178b810d2b0b4986e7a6068e8e0a703cb9601aee7af7f6235398197d74c`  
		Last Modified: Fri, 05 Mar 2021 03:19:38 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b2f6c2d0c7d9165289f4145f9fb2d5bd3622112bcb40a5555d56f3358b9705`  
		Last Modified: Fri, 05 Mar 2021 03:19:36 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a09c36d006daa2967af8b26e2157350bb5c39f1101544c40298a9879857f951`  
		Last Modified: Fri, 05 Mar 2021 03:19:36 GMT  
		Size: 3.6 MB (3576364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e5deca6d2f48ec567fff9f38134e4504ee858f1a6de2b415ff6f147b559865`  
		Last Modified: Fri, 05 Mar 2021 03:19:36 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c078244c143c12118d608de1dacae67d924b37e40fa5ff5e1626d7603db96c77`  
		Last Modified: Fri, 05 Mar 2021 03:19:36 GMT  
		Size: 582.8 KB (582808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399c2c8d9bb3754b99dd4e63d7f86d9a17b1ba333afbcdd1a91323827dbf6c19`  
		Last Modified: Fri, 05 Mar 2021 03:19:36 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.0-fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:9d290c8427c90264c046b18b2dad85bf1ab72b9636a299fdcdb70e725b73cf37
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.6 MB (33587124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fda254daa0110b7ed8e11936831a70eb476e6bac9d0f864a167cc3ca89cc570`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 23:42:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Feb 2021 23:42:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 17 Feb 2021 23:42:38 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Feb 2021 23:42:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Feb 2021 23:42:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Feb 2021 23:47:35 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Wed, 17 Feb 2021 23:47:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 23:47:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 23:47:37 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Feb 2021 23:57:44 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:42:58 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:43:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:43:01 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:43:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:43:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:47:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:47:53 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:47:56 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:47:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:47:58 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 00:48:00 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 05 Mar 2021 00:48:00 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Mar 2021 00:48:01 GMT
EXPOSE 9000
# Fri, 05 Mar 2021 00:48:02 GMT
CMD ["php-fpm"]
# Fri, 05 Mar 2021 02:06:30 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 02:06:33 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 02:07:32 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 02:07:34 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 02:07:35 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 02:07:37 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 02:07:38 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 02:07:42 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 02:07:43 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 02:07:44 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 02:07:46 GMT
USER adminer
# Fri, 05 Mar 2021 02:07:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4b642bcaaef409203aaedc803835562ee86d3ea457bf4ccdd22e5d7b2367f1`  
		Last Modified: Thu, 18 Feb 2021 00:23:35 GMT  
		Size: 1.7 MB (1694455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ea39643e14bb66b107bb23b02b8c7a193ed89d38f4ae52b1decbe763fb0db9`  
		Last Modified: Thu, 18 Feb 2021 00:23:34 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3455119714d8ce066305d3b121e103a3cf690db26bb556906ba67e7a7c1f559`  
		Last Modified: Thu, 18 Feb 2021 00:23:34 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5fb9efa5fb7c6758d0c1ef8f8dec26c072a0b3db105d3bc1072051a584a31e`  
		Last Modified: Fri, 05 Mar 2021 01:14:03 GMT  
		Size: 10.4 MB (10354114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b86fa187c3fdc5dc79bdeb0cc5299859c0c0095b732f4ee415c0bb12daa215b`  
		Last Modified: Fri, 05 Mar 2021 01:14:00 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12f3432275b2be2dd42ee1df485264de064473b2c82feda5bf9c9d20b5b271b`  
		Last Modified: Fri, 05 Mar 2021 01:14:04 GMT  
		Size: 14.3 MB (14335600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c51b3d598680e53ab4687fb42e8f593583f31bd96bddf4f4a3260e7ce39978`  
		Last Modified: Fri, 05 Mar 2021 01:14:00 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f84e9090c4bc7becc3688c7892a83e9851718fc9492734a99d408a8f37e5940`  
		Last Modified: Fri, 05 Mar 2021 01:14:00 GMT  
		Size: 17.6 KB (17578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6e5a4c4a59a3a7880ef2d31091da082e89c8a5d36fe48cc0e6d2a869a4c015`  
		Last Modified: Fri, 05 Mar 2021 01:14:00 GMT  
		Size: 8.4 KB (8443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c96f48785c9c98e7112aba8a63a131c4068630fb03bf917709cbf26dcde0f6`  
		Last Modified: Fri, 05 Mar 2021 02:08:29 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68227b3239ccce99fdd4b5f144a2966beb055b69b3cd677b07dc854149769ed7`  
		Last Modified: Fri, 05 Mar 2021 02:08:28 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ee8c6445369dac5a5c0a1eebb4a5de36d9b41daa6842a89ffd90533c70d115`  
		Last Modified: Fri, 05 Mar 2021 02:08:28 GMT  
		Size: 3.9 MB (3874581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd6128ec00cfc5bafbcbb5cd0958f7c6bb1789fdd6d9f462f7bdfb945d25051`  
		Last Modified: Fri, 05 Mar 2021 02:08:27 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e85b4b40588c16a96e7bd4ebc9bda548027f1d29a882087ca1873edbe5c6a3e`  
		Last Modified: Fri, 05 Mar 2021 02:08:28 GMT  
		Size: 582.8 KB (582807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52d3bffbd635505b2a6fe9733d78a3056c37f05d763c518a0cfbb0e62ae6fa8`  
		Last Modified: Fri, 05 Mar 2021 02:08:28 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.0-fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:26d15f54137462efdfea2e074d6e3aab1a83d2e91bfb268a77550109c29e494e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34296076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f79ec5602cf1203e859966ea84f6f0af410574c66ff1695966634f7fa99a0602`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 02:13:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 06 Mar 2021 02:13:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 06 Mar 2021 02:13:32 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 06 Mar 2021 02:13:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 06 Mar 2021 02:13:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 06 Mar 2021 02:20:59 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 06 Mar 2021 02:20:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 02:20:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 02:21:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 06 Mar 2021 03:09:15 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Sat, 06 Mar 2021 03:09:15 GMT
ENV PHP_VERSION=7.4.16
# Sat, 06 Mar 2021 03:09:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Sat, 06 Mar 2021 03:09:16 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Sat, 06 Mar 2021 03:09:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 06 Mar 2021 03:09:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Mar 2021 03:18:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Mar 2021 03:18:11 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Sat, 06 Mar 2021 03:18:13 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Mar 2021 03:18:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Mar 2021 03:18:14 GMT
WORKDIR /var/www/html
# Sat, 06 Mar 2021 03:18:15 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Sat, 06 Mar 2021 03:18:15 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 03:18:16 GMT
EXPOSE 9000
# Sat, 06 Mar 2021 03:18:16 GMT
CMD ["php-fpm"]
# Sat, 06 Mar 2021 08:16:46 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 06 Mar 2021 08:16:47 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 06 Mar 2021 08:17:17 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 06 Mar 2021 08:17:17 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Sat, 06 Mar 2021 08:17:18 GMT
ENV ADMINER_VERSION=4.8.0
# Sat, 06 Mar 2021 08:17:18 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Sat, 06 Mar 2021 08:17:18 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Sat, 06 Mar 2021 08:17:20 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 06 Mar 2021 08:17:20 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 06 Mar 2021 08:17:20 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 06 Mar 2021 08:17:21 GMT
USER adminer
# Sat, 06 Mar 2021 08:17:21 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d779edf81d3549de0c570804cffa8279f4a980d3fed1292285070f24a1b00f`  
		Last Modified: Sat, 06 Mar 2021 05:47:24 GMT  
		Size: 1.8 MB (1793700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce9d30537e4bf7ab9ad24ea334671e794e0830680c386cf4b36dbba54dd40c5`  
		Last Modified: Sat, 06 Mar 2021 05:47:23 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f119038c35efd6cc0b1a27c432b2fc338da413650c224359556d95e0bf8214`  
		Last Modified: Sat, 06 Mar 2021 05:47:23 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5397827f225e72f10184ff09624c35bf31a5231897f53e91ca07da5f62e873dc`  
		Last Modified: Sat, 06 Mar 2021 05:54:56 GMT  
		Size: 10.4 MB (10354073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8309650059a0810adb36671135e0f311a358f75fb9dd4d4de7e8ca2e03df4ecd`  
		Last Modified: Sat, 06 Mar 2021 05:54:52 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8ec289fc161bd97f4660f6a9b0102128d91f8545b7a66236470e13f99820a6`  
		Last Modified: Sat, 06 Mar 2021 05:54:56 GMT  
		Size: 14.7 MB (14703205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df93dca921888af6f7dd240ba41be2492ce1b35f2a7691841b7453de8097cba`  
		Last Modified: Sat, 06 Mar 2021 05:54:52 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a789e9947572f56584832fc18a9febda69c07a7fd803f86bb47b8b76048e0d`  
		Last Modified: Sat, 06 Mar 2021 05:54:52 GMT  
		Size: 17.5 KB (17499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7a016c5403915747cc20016342dd4a30b61cf26f6ecfbf3db8dc913816ba0d`  
		Last Modified: Sat, 06 Mar 2021 05:54:52 GMT  
		Size: 8.4 KB (8443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20574028b280be669aaf096c2a36ea615748c8d8947b537fed28011a1bba827`  
		Last Modified: Sat, 06 Mar 2021 08:18:31 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcffc992f5c3c59e7de4cf88a6b3a2bcea4814b1479dd0fd6533b32693a2337`  
		Last Modified: Sat, 06 Mar 2021 08:18:28 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d41c527ce013e3f17159bc459ca0d55a95da81bcc5e14571bbe997c5156b6e0`  
		Last Modified: Sat, 06 Mar 2021 08:18:30 GMT  
		Size: 4.0 MB (4010213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad6f6db03a695dc6910470b21945bc6f75b04d9f24622618a244bced44e9a04`  
		Last Modified: Sat, 06 Mar 2021 08:18:29 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde165942766dd540d19ff22ecd092d80baff426cd360af35eb0fb5ef30b2dac`  
		Last Modified: Sat, 06 Mar 2021 08:18:29 GMT  
		Size: 582.8 KB (582800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a269b82e491105b4090cf94096e9ce312f49c2e7c64fc59ce8fca97a0048d95`  
		Last Modified: Sat, 06 Mar 2021 08:18:28 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.0-fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:60214217e7c6d9d5d171f4a2f5b8e64a7616f02249811ff70fc139b463c8c1a6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (35045727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195aaf01b7fc54d33fea092504c0b5d14247b799d81fbb46ce985ef115ac65c8`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 17 Feb 2021 21:17:29 GMT
ADD file:28f4377c61c0f8eb43a6b36e6a24ef5893f51d405d25b62e364988223537ae0b in / 
# Wed, 17 Feb 2021 21:17:37 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 00:23:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Feb 2021 00:24:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 18 Feb 2021 00:24:44 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 18 Feb 2021 00:24:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Feb 2021 00:25:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 18 Feb 2021 00:32:20 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 18 Feb 2021 00:32:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:32:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:32:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Feb 2021 00:47:19 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 01:12:05 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 01:12:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 01:12:14 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 01:12:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 01:12:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:17:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 01:17:41 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:17:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 01:17:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 01:18:00 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 01:18:13 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 05 Mar 2021 01:18:18 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Mar 2021 01:18:22 GMT
EXPOSE 9000
# Fri, 05 Mar 2021 01:18:25 GMT
CMD ["php-fpm"]
# Fri, 05 Mar 2021 02:12:29 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 02:12:47 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 02:13:39 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 02:13:41 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 02:13:45 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 02:13:50 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 02:13:54 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 02:14:11 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 02:14:12 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 02:14:17 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 02:14:23 GMT
USER adminer
# Fri, 05 Mar 2021 02:14:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:cb672e0375a8f9bb3d33049ceb372ffa49b959bfc84fe6f72bfb97b682a608c8`  
		Last Modified: Wed, 17 Feb 2021 21:18:10 GMT  
		Size: 2.8 MB (2813081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebfde0ed2b25fdf7a28b46b01e73c7891af78bd260ce9c5f46f33a0fd4bba5a`  
		Last Modified: Thu, 18 Feb 2021 01:25:11 GMT  
		Size: 1.7 MB (1741666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c587bda2cf37683b8f80371450083e1533df270a51cbe196c845e7ab52f8943`  
		Last Modified: Thu, 18 Feb 2021 01:25:09 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2faee0918d4167a0323dba5b4244442a3d6cd88d5eacd4a560b72f056274a4`  
		Last Modified: Thu, 18 Feb 2021 01:25:10 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50832ff8121fa6dabe4fef261cdf442de13beba3eba5b02edc01bb52575f604`  
		Last Modified: Fri, 05 Mar 2021 01:50:47 GMT  
		Size: 10.4 MB (10354080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492225a51fbf5c42138184c0b8f334e0c03349c39df922382ab84510b28fa495`  
		Last Modified: Fri, 05 Mar 2021 01:50:40 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e38b008adbe62b7a3a5140dedb456e37ae0f03fe3970c9f2386f7b294c13c3`  
		Last Modified: Fri, 05 Mar 2021 01:50:44 GMT  
		Size: 15.6 MB (15601592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac2e3566364c50161e37f74f62cc1631496ad06e929b660adcd70dd66254b3d`  
		Last Modified: Fri, 05 Mar 2021 01:50:40 GMT  
		Size: 2.3 KB (2265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48abd24364092c58878a940181d9510d843d157a2e6649ea9fe3f8452341d5e0`  
		Last Modified: Fri, 05 Mar 2021 01:50:40 GMT  
		Size: 17.6 KB (17568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c82139d7ee7be2c8e6f6313bad71cc515fcb36b36f9db46406380c839a21ff`  
		Last Modified: Fri, 05 Mar 2021 01:50:40 GMT  
		Size: 8.4 KB (8445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb87a4b5911ea0082c17ed927c804ab2ef1074f3e4a232baee3c7aa0d53f2001`  
		Last Modified: Fri, 05 Mar 2021 02:15:36 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:867bbe031ef2fdc9b041f464c092ae860709ae7089ad3bf2d020ca9a5685adb9`  
		Last Modified: Fri, 05 Mar 2021 02:15:33 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1352d4abeeccc4cdec18fe083cca986917a96a75c051377c6e6f60df25b8b7`  
		Last Modified: Fri, 05 Mar 2021 02:15:35 GMT  
		Size: 3.9 MB (3918505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf3106a1ac6be7ebc6cac6752295d88ad3e0b6dde2a752abbcf19665597f91d`  
		Last Modified: Fri, 05 Mar 2021 02:15:32 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7e5c63ff249b14ce430b50a9d068fd75bd570c8e3dda8a120527bbeb589643`  
		Last Modified: Fri, 05 Mar 2021 02:15:32 GMT  
		Size: 582.8 KB (582811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5372a8bc61644fe0469438556e96846b6dd32a217c62c627af9666e934dc59d0`  
		Last Modified: Fri, 05 Mar 2021 02:15:34 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.0-fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:172c17539eec169a1efbc7bdb5582b0c6d68a767c96c91534eaa512ea11f1a54
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32837225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e84b58503996daca80603c6caf456f29c872d2fbcedc12f3883b3ff932310f5`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 00:40:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Feb 2021 00:40:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 18 Feb 2021 00:40:31 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 18 Feb 2021 00:40:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Feb 2021 00:40:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 18 Feb 2021 00:46:04 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 18 Feb 2021 00:46:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:46:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:46:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Feb 2021 00:56:47 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:21:28 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:21:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:21:28 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:21:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:21:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:24:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:24:36 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:24:37 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:24:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:24:37 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 00:24:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 05 Mar 2021 00:24:38 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Mar 2021 00:24:38 GMT
EXPOSE 9000
# Fri, 05 Mar 2021 00:24:38 GMT
CMD ["php-fpm"]
# Fri, 05 Mar 2021 01:35:37 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 01:35:38 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 01:36:11 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 01:36:11 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 01:36:12 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 01:36:12 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 01:36:13 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 01:36:14 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 01:36:14 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:36:15 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 01:36:15 GMT
USER adminer
# Fri, 05 Mar 2021 01:36:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2eaf748a32e76be0f1aa6246cb11c8aa5022aa834df364bb87f581198e6376`  
		Last Modified: Thu, 18 Feb 2021 01:26:48 GMT  
		Size: 1.8 MB (1756400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5716be54c61b8e2a38b4d6a0cbece88801726747842f6bd1a50aaf4e8442013f`  
		Last Modified: Thu, 18 Feb 2021 01:26:48 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6aa66a8dad4ec1443c27324fc452b05c4299dbffefcebee55700880033b3ff7`  
		Last Modified: Thu, 18 Feb 2021 01:26:47 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ec6de43c42608abedaf0d1351eac485f25cf6ea8189784c33b0bd55cf4c8de`  
		Last Modified: Fri, 05 Mar 2021 00:51:59 GMT  
		Size: 10.4 MB (10354080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7f932c8c75e84329764906d4a66784a32d6eebc1e0bf7b70c2e6608e3fbf9b`  
		Last Modified: Fri, 05 Mar 2021 00:51:56 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94d974f2d24d19a056887cdf386d4e9505e841d3a06c71f3ffa4eda14b55cd5`  
		Last Modified: Fri, 05 Mar 2021 00:51:59 GMT  
		Size: 13.9 MB (13924090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69925775200e946533560678d8a38f9ae9c806a7f163e84949bcbcb5b90adcf5`  
		Last Modified: Fri, 05 Mar 2021 00:51:56 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e58476f31db9ac4d71c9e0ea37118bbbd9193cc0b3aea7cc05bab5c83ddff8`  
		Last Modified: Fri, 05 Mar 2021 00:51:56 GMT  
		Size: 17.6 KB (17562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c27cda61463930e8e9c42f8de03c8a59af15035338f16a147b75cfff1adc6bb`  
		Last Modified: Fri, 05 Mar 2021 00:51:56 GMT  
		Size: 8.4 KB (8445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536690e7823ee104420228155dfb821af13a367f39347bb42c6536a406b031c2`  
		Last Modified: Fri, 05 Mar 2021 01:36:49 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f87e2102e12d1ceefff1f2490100e7e4a089955c1ec33e2d52db85d8706f9c`  
		Last Modified: Fri, 05 Mar 2021 01:36:47 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180b148ebd9e445d7b63cfd748624466a392b06d40e4980de5a006e90fe54def`  
		Last Modified: Fri, 05 Mar 2021 01:36:48 GMT  
		Size: 3.6 MB (3583484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95fc51e3df0e6750051bc696529caddc5ee514b5c8d0515a39eee82a06e9739a`  
		Last Modified: Fri, 05 Mar 2021 01:36:47 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5435da686f45a2ef26c52cb075980530af7e8ef76884a406b5a0e9b3068a28`  
		Last Modified: Fri, 05 Mar 2021 01:36:47 GMT  
		Size: 582.8 KB (582804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472506157be8ba02f17eab06907cba644d1ead543ffe97be2a01f98d2a45ad45`  
		Last Modified: Fri, 05 Mar 2021 01:36:47 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.8.0-standalone`

```console
$ docker pull adminer@sha256:1ee6ed00d1169a14a1030a1d44a5ab1724392c115d296d98f0a0e8700628deeb
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

### `adminer:4.8.0-standalone` - linux; amd64

```console
$ docker pull adminer@sha256:d7cbbb92e43f7d55027a58bd115d9425548325f3754cb705b03368243b3930d3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.6 MB (33625851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d5528d5e4b1e1e879cf6d3b49b09245873a231a6054521f40a538633893e3d`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 03:21:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 06 Mar 2021 03:21:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 06 Mar 2021 03:21:31 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 06 Mar 2021 03:21:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 06 Mar 2021 03:21:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 06 Mar 2021 03:21:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 03:21:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 03:21:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 06 Mar 2021 04:18:25 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Sat, 06 Mar 2021 04:18:25 GMT
ENV PHP_VERSION=7.4.16
# Sat, 06 Mar 2021 04:18:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Sat, 06 Mar 2021 04:18:26 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Sat, 06 Mar 2021 04:18:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 06 Mar 2021 04:18:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Mar 2021 04:25:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Mar 2021 04:25:46 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Sat, 06 Mar 2021 04:25:48 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Mar 2021 04:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Mar 2021 04:25:49 GMT
CMD ["php" "-a"]
# Sat, 06 Mar 2021 08:51:16 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 06 Mar 2021 08:51:16 GMT
STOPSIGNAL SIGINT
# Sat, 06 Mar 2021 08:51:17 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 06 Mar 2021 08:51:17 GMT
WORKDIR /var/www/html
# Sat, 06 Mar 2021 08:51:43 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 06 Mar 2021 08:51:43 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Sat, 06 Mar 2021 08:51:43 GMT
ENV ADMINER_VERSION=4.8.0
# Sat, 06 Mar 2021 08:51:44 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Sat, 06 Mar 2021 08:51:44 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Sat, 06 Mar 2021 08:51:46 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 06 Mar 2021 08:51:46 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 06 Mar 2021 08:51:46 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 06 Mar 2021 08:51:46 GMT
USER adminer
# Sat, 06 Mar 2021 08:51:46 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 06 Mar 2021 08:51:47 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743181516422399af3888ad5df44c6f711f992b2f86288db9e191ae13de99fa0`  
		Last Modified: Sat, 06 Mar 2021 06:31:08 GMT  
		Size: 1.7 MB (1694870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c307b60e377a3903f74fd9cde3ad69f754071faac36f81ca74e1aa9eabe4851`  
		Last Modified: Sat, 06 Mar 2021 06:31:08 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d5b43308915ce3198dec1c19aa88719afacff02c85660a952982856a0bcc9c`  
		Last Modified: Sat, 06 Mar 2021 06:31:08 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4848a1e010e4e0cda8de291fa6ed2f3efecf20d7343a69cec21878885828d2d`  
		Last Modified: Sat, 06 Mar 2021 06:35:54 GMT  
		Size: 10.4 MB (10354097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8e88ab7b4e15d3c4d8d099845669643447a702d27188138ed20f8c14879cde`  
		Last Modified: Sat, 06 Mar 2021 06:35:54 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c6688ec4022c9042fad0bff0a5aaa03cd55628577fe71a419761ca5478392c`  
		Last Modified: Sat, 06 Mar 2021 06:35:56 GMT  
		Size: 14.3 MB (14253596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b401e642cd6c785a0ede5899c8a1fb93770d6eaf04a0a5faeb0183ad5c21f3`  
		Last Modified: Sat, 06 Mar 2021 06:35:54 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4aa45ba156c9e4af51f7b2a5eec317be47eca6ba8e9bb8fc368488ea41c11c`  
		Last Modified: Sat, 06 Mar 2021 06:35:54 GMT  
		Size: 17.5 KB (17518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b686977c50b0410c0084a21bef42aae47c53441ee7defe7b25bcad585a19999`  
		Last Modified: Sat, 06 Mar 2021 08:52:42 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf15bf71cdf8a60508b2773274a23124c80de6ad9611b97bd532869bdce6929`  
		Last Modified: Sat, 06 Mar 2021 08:52:38 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7855e8a455940ec1b6c2e7a9d42e3a94e92b3f7dd253bfdefd2ef4f0b272a242`  
		Last Modified: Sat, 06 Mar 2021 08:52:40 GMT  
		Size: 3.9 MB (3903349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff73275236b8945efe2dadf9b67d73cc5c24fb699f0e3265cbdb3445bdabcba`  
		Last Modified: Sat, 06 Mar 2021 08:52:38 GMT  
		Size: 1.5 KB (1471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64cfef0d91dbc6948021e94ae4407132c018d08d4446215342ad7e0447e33383`  
		Last Modified: Sat, 06 Mar 2021 08:52:39 GMT  
		Size: 582.8 KB (582798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7097b3e809e2d58f970ecec3070fa3db82d914e74c47172eb2c2800e051290`  
		Last Modified: Sat, 06 Mar 2021 08:52:39 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.0-standalone` - linux; arm variant v6

```console
$ docker pull adminer@sha256:67ecf13bed27733de831bad0889ec483ede8530402c3c46011d2334e4a991c25
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32352290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4b093e53cd99d8904355485561c5dd006e3077e79bf2eaba849078b7c8ff3b`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:17:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Feb 2021 22:17:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 17 Feb 2021 22:17:15 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Feb 2021 22:17:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Feb 2021 22:17:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Feb 2021 22:17:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:17:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:17:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Feb 2021 22:24:49 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:22:42 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:22:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:22:48 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:22:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:23:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:26:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:26:24 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:26:28 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:26:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:26:30 GMT
CMD ["php" "-a"]
# Fri, 05 Mar 2021 01:28:12 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 01:28:12 GMT
STOPSIGNAL SIGINT
# Fri, 05 Mar 2021 01:28:15 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 01:28:15 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 01:29:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 01:29:05 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 01:29:06 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 01:29:07 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 01:29:08 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 01:29:11 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 01:29:11 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:29:12 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 01:29:13 GMT
USER adminer
# Fri, 05 Mar 2021 01:29:13 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 05 Mar 2021 01:29:14 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a33e390360f607fe5a7fe0a0203b7347693b0d8cab270352594a3700e1a1d0`  
		Last Modified: Wed, 17 Feb 2021 22:57:10 GMT  
		Size: 1.7 MB (1684729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d1bbb88bd210deaf33702df9d6fa7f35e72f23dfbb55196147ab537320e9f3`  
		Last Modified: Wed, 17 Feb 2021 22:57:09 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b99fbc527c373db47c36282e5bbd82010870902db2af45982bbb8d700375a32`  
		Last Modified: Wed, 17 Feb 2021 22:57:09 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37a52f8d6a0669099c893e2b3e9ce5d8862eed5489a15f8dafd39f664233b7c`  
		Last Modified: Fri, 05 Mar 2021 00:53:01 GMT  
		Size: 10.4 MB (10354085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e31438bda764d2d788352c3dbdc563f97c840ce2736c283190e590e11a4641`  
		Last Modified: Fri, 05 Mar 2021 00:52:59 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615508ce208f1bfacc67745161a522490ffde3254a7e5b88e2a75704a178b65d`  
		Last Modified: Fri, 05 Mar 2021 00:53:05 GMT  
		Size: 13.5 MB (13479609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49bab722652cd2c45df88dee34d635b0c4824fd1885e9cdb6fa1ad1c707b24d`  
		Last Modified: Fri, 05 Mar 2021 00:52:59 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b5e7fa68211b0722b528ee1f7b5f413c32b3581eec56fc37d056cf1e44d45f`  
		Last Modified: Fri, 05 Mar 2021 00:52:59 GMT  
		Size: 17.6 KB (17574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a863fe1948ed188002b2c53e19c1c4f06aa611913e9aee2e6d37a4b38892fa27`  
		Last Modified: Fri, 05 Mar 2021 01:31:18 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e5d7f207dfb0131e75fb5675de4013a21ec2a9965b6a5f2974a09de577b376`  
		Last Modified: Fri, 05 Mar 2021 01:31:15 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613aba5afd5742d6a2f8c093d4d9e2e3eef9f92d01853c139b3f7690a577fd1d`  
		Last Modified: Fri, 05 Mar 2021 01:31:16 GMT  
		Size: 3.6 MB (3603470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ea9f569f958143bd38a220ee729c6ef6f85c122fe3f42b2a761b57e39df3e9`  
		Last Modified: Fri, 05 Mar 2021 01:31:15 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e6944e336be980c37b3af333b01dab0f1b3db12af184e3cc0ed1d4a326a6ab`  
		Last Modified: Fri, 05 Mar 2021 01:31:15 GMT  
		Size: 582.8 KB (582808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4644911e6f4e52234e1b7b359c25f4998c5be8fe108e2f0b54e5cfd721d2d9`  
		Last Modified: Fri, 05 Mar 2021 01:31:15 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.0-standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:3c5fe027a505612b8c787c41923bc81f01eba12776b7827fb8de3b48fadd12ff
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31126385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7625601231cbbafd93c468bb5506f91c320be7c6640088ec3203f7b61bcae845`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:56:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Feb 2021 22:57:00 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 17 Feb 2021 22:57:04 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Feb 2021 22:57:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Feb 2021 22:57:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Feb 2021 22:57:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:57:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:57:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Feb 2021 23:07:25 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:51:51 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:51:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:51:52 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:51:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:51:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:54:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:54:56 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:55:00 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:55:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:55:01 GMT
CMD ["php" "-a"]
# Fri, 05 Mar 2021 03:16:34 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 03:16:35 GMT
STOPSIGNAL SIGINT
# Fri, 05 Mar 2021 03:16:37 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 03:16:37 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 03:17:32 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 03:17:34 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 03:17:35 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 03:17:36 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 03:17:36 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 03:17:39 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 03:17:40 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 03:17:41 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 03:17:42 GMT
USER adminer
# Fri, 05 Mar 2021 03:17:42 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 05 Mar 2021 03:17:43 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf491575714634902d01e3e48f3b92702cb2e4c42056aa5421058d2a2cbfd9f6`  
		Last Modified: Wed, 17 Feb 2021 23:33:58 GMT  
		Size: 1.6 MB (1555125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8ae33f1196d3a62a9383b30d3fd81dd4be1bcf1a99a3d928f585b0d85c5408`  
		Last Modified: Wed, 17 Feb 2021 23:33:58 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16bd16ac2dc3896b7ddf5e8e50bafcc3990d8313dc26634a51beafc97cc6374`  
		Last Modified: Wed, 17 Feb 2021 23:33:58 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224ef988837049de958e2e9476510f82fe8e42270706a0671a5a463f6ae97dc2`  
		Last Modified: Fri, 05 Mar 2021 01:20:19 GMT  
		Size: 10.4 MB (10354091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9e75985cf89dec0ed12206b36f371ffbda22ccf6cdbccf5d19345e62db2c14`  
		Last Modified: Fri, 05 Mar 2021 01:20:16 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3067a7094a3949ddb39a5787e92b263164d2eb287f0d508c0497dc270667f7a2`  
		Last Modified: Fri, 05 Mar 2021 01:20:19 GMT  
		Size: 12.6 MB (12608573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e967fccc5675136a3112da05f19624319efe2274faf250ffc942f8df1727990b`  
		Last Modified: Fri, 05 Mar 2021 01:20:15 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bee2c4ad784aa0aa254a050c45062e42eae3e6414649f1e7372db7fe0845817`  
		Last Modified: Fri, 05 Mar 2021 01:20:15 GMT  
		Size: 17.6 KB (17556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd957d7c1659b87bbacdaaa44de1493cd86ce1058104890fa7f886c244af7e2`  
		Last Modified: Fri, 05 Mar 2021 03:19:23 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a9b53808941e232e796f0fce8be1b1a2bdab2ab0d1227f671cdc2e6d8acecd`  
		Last Modified: Fri, 05 Mar 2021 03:19:21 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b983fd5f2f41ac862e588d3c7cb994ae11a6d4dfd1273298d35ff8fcdc87e72`  
		Last Modified: Fri, 05 Mar 2021 03:19:21 GMT  
		Size: 3.6 MB (3576366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957ff1dc0df9c3cd0fa022e0ae444a04b77d5b488a38dcba9673c2f3dfb07f8d`  
		Last Modified: Fri, 05 Mar 2021 03:19:21 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d418e42a87cf9ea044ec23d04a0b56e7f7b51dbab5639eb0e1c16248b88575`  
		Last Modified: Fri, 05 Mar 2021 03:19:21 GMT  
		Size: 582.8 KB (582806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1688bcdb1a112479d4950eae42069fa29ff4e81e587b2387362b4a6cc0fbe2`  
		Last Modified: Fri, 05 Mar 2021 03:19:21 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.0-standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:7991be9e1a1ee3f2c5d374475d3746026dd7ca64a60167a65551567d7cfccf43
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33506242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11682bbe518b1faa63b82b75d246e7c35612d6d253da8f2011c0539c5b07f5cc`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 23:42:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Feb 2021 23:42:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 17 Feb 2021 23:42:38 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Feb 2021 23:42:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Feb 2021 23:42:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Feb 2021 23:42:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 23:42:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 23:42:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Feb 2021 23:53:01 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:37:35 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:37:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:37:38 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:37:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:37:47 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:42:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:42:39 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:42:44 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:42:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:42:47 GMT
CMD ["php" "-a"]
# Fri, 05 Mar 2021 02:04:43 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 02:04:44 GMT
STOPSIGNAL SIGINT
# Fri, 05 Mar 2021 02:04:48 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 02:04:50 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 02:05:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 02:05:56 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 02:05:57 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 02:05:57 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 02:05:58 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 02:06:02 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 02:06:03 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 02:06:04 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 02:06:05 GMT
USER adminer
# Fri, 05 Mar 2021 02:06:06 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 05 Mar 2021 02:06:06 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4b642bcaaef409203aaedc803835562ee86d3ea457bf4ccdd22e5d7b2367f1`  
		Last Modified: Thu, 18 Feb 2021 00:23:35 GMT  
		Size: 1.7 MB (1694455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ea39643e14bb66b107bb23b02b8c7a193ed89d38f4ae52b1decbe763fb0db9`  
		Last Modified: Thu, 18 Feb 2021 00:23:34 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3455119714d8ce066305d3b121e103a3cf690db26bb556906ba67e7a7c1f559`  
		Last Modified: Thu, 18 Feb 2021 00:23:34 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a68a1ddf490519ddbcd4f75589909c8d4703a6b902bae2a7319905984b7547`  
		Last Modified: Fri, 05 Mar 2021 01:13:32 GMT  
		Size: 10.4 MB (10354115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1754592c0391f5b7b27cf3c7110b1e2a917ebb769b0ceaf9bfdfd0181cc6cb`  
		Last Modified: Fri, 05 Mar 2021 01:13:30 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a402e34d4d52011f5ecf29a826d7fd94dc474fdf156b70d506d3deaeb2a4d3b`  
		Last Modified: Fri, 05 Mar 2021 01:13:34 GMT  
		Size: 14.3 MB (14263146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1702d0137849d4baf63d0536ee9f8391c72c295a46613ed43c270f3cc81a90`  
		Last Modified: Fri, 05 Mar 2021 01:13:31 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ebe5152320826ffaea66119f3e759ce05ed98bb09a201643ee6674cbd9685e`  
		Last Modified: Fri, 05 Mar 2021 01:13:31 GMT  
		Size: 17.6 KB (17574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a42655d4ea3811b755ccede7be6704d6e30a4e912c6ec284807f25e1874c11`  
		Last Modified: Fri, 05 Mar 2021 02:08:13 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36983a97af0e64abf039823af9b57936cc5add643fab48f1d64ca7fbeb076a02`  
		Last Modified: Fri, 05 Mar 2021 02:08:11 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23c53be365e785ad30481daf9c58f08857ca80fc5fc681e12655557a14f7093`  
		Last Modified: Fri, 05 Mar 2021 02:08:12 GMT  
		Size: 3.9 MB (3874584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d698ddfcb363647524ac96d6fe45138e9aa228c8662ec68d2c877a5862a6257`  
		Last Modified: Fri, 05 Mar 2021 02:08:11 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e7497f33585536dba243eedb8aea95c51b88677f674845065a15d776a0e7c78`  
		Last Modified: Fri, 05 Mar 2021 02:08:12 GMT  
		Size: 582.8 KB (582809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041eab10d184403fbf0b2a94255c47e5618bc99fd708586209ad66d02a41c86b`  
		Last Modified: Fri, 05 Mar 2021 02:08:11 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.0-standalone` - linux; 386

```console
$ docker pull adminer@sha256:3c12e8f857cf7b920500273d347a57b13be7f75bc361cd49631704781e87dafe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34214715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8de5231523b1be5d66db42c66ace28ceef73e37457dc22956bd36744ea35592f`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 02:13:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 06 Mar 2021 02:13:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 06 Mar 2021 02:13:32 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 06 Mar 2021 02:13:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 06 Mar 2021 02:13:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 06 Mar 2021 02:13:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 02:13:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 02:13:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 06 Mar 2021 02:59:52 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Sat, 06 Mar 2021 02:59:52 GMT
ENV PHP_VERSION=7.4.16
# Sat, 06 Mar 2021 02:59:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Sat, 06 Mar 2021 02:59:53 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Sat, 06 Mar 2021 03:00:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 06 Mar 2021 03:00:19 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Mar 2021 03:08:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Mar 2021 03:08:56 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Sat, 06 Mar 2021 03:08:58 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Mar 2021 03:08:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Mar 2021 03:08:58 GMT
CMD ["php" "-a"]
# Sat, 06 Mar 2021 08:16:03 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 06 Mar 2021 08:16:03 GMT
STOPSIGNAL SIGINT
# Sat, 06 Mar 2021 08:16:04 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 06 Mar 2021 08:16:04 GMT
WORKDIR /var/www/html
# Sat, 06 Mar 2021 08:16:34 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 06 Mar 2021 08:16:34 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Sat, 06 Mar 2021 08:16:34 GMT
ENV ADMINER_VERSION=4.8.0
# Sat, 06 Mar 2021 08:16:34 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Sat, 06 Mar 2021 08:16:35 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Sat, 06 Mar 2021 08:16:37 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 06 Mar 2021 08:16:38 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 06 Mar 2021 08:16:38 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 06 Mar 2021 08:16:38 GMT
USER adminer
# Sat, 06 Mar 2021 08:16:38 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 06 Mar 2021 08:16:38 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d779edf81d3549de0c570804cffa8279f4a980d3fed1292285070f24a1b00f`  
		Last Modified: Sat, 06 Mar 2021 05:47:24 GMT  
		Size: 1.8 MB (1793700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce9d30537e4bf7ab9ad24ea334671e794e0830680c386cf4b36dbba54dd40c5`  
		Last Modified: Sat, 06 Mar 2021 05:47:23 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f119038c35efd6cc0b1a27c432b2fc338da413650c224359556d95e0bf8214`  
		Last Modified: Sat, 06 Mar 2021 05:47:23 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:125aeed6c18a6c28cf608d3c3cd80094c61ed4f9023855f9c3ac4993f1542907`  
		Last Modified: Sat, 06 Mar 2021 05:53:56 GMT  
		Size: 10.4 MB (10354073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05563330040dc337869b22ab8c267fc06fa14139a5f270679e69ba3a718896b5`  
		Last Modified: Sat, 06 Mar 2021 05:53:53 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567f9a9d037948e123fbbec64dfb76f7cca9d30cd3e5526abc597b65fd39656b`  
		Last Modified: Sat, 06 Mar 2021 05:54:00 GMT  
		Size: 14.6 MB (14630287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28b3a57348334ee91df9b04ec97e570fcff52d0a9fa3e3ec3247823d80a437d`  
		Last Modified: Sat, 06 Mar 2021 05:53:53 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0621d49125fecbf6f64ac583fbf7c76034bc51eed48c69516922c398d93a6c`  
		Last Modified: Sat, 06 Mar 2021 05:53:54 GMT  
		Size: 17.5 KB (17501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c703587ef05b977c127d751c1c78fa472b5ddb67b5ac217ac20ea90cd8855c`  
		Last Modified: Sat, 06 Mar 2021 08:17:58 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e848e2757b70b020801c677c59e10e8709f14f3f76f32d2b1be5f95679f4f6c5`  
		Last Modified: Sat, 06 Mar 2021 08:17:54 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f2ac401974d5ea19f7f375960da2a7a6c77f23dab4135c4bd95c4dc64f9d02`  
		Last Modified: Sat, 06 Mar 2021 08:17:55 GMT  
		Size: 4.0 MB (4010207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cb78f666be732b2b10b604df1cb578ad8ccca1445c29fd5bab4ba346f29247`  
		Last Modified: Sat, 06 Mar 2021 08:17:54 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980181a00a928280cf2288da2498d06c9203508ce40aa0aed05b1a2be94ae1ce`  
		Last Modified: Sat, 06 Mar 2021 08:17:54 GMT  
		Size: 582.8 KB (582807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0865a1f7fbcf5062e0b5b2fc87b6ea55d2e4c094297f6139e110bbc7a1c9794`  
		Last Modified: Sat, 06 Mar 2021 08:17:54 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.0-standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:f8ed36e984e53d541d8f690681208acc65c3b6e90ac3830c51e821eeb7b24951
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (34960311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0819898f5e08afcbb1041ea1c325869490d997fe19fcaa3e93b720312272db4`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 21:17:29 GMT
ADD file:28f4377c61c0f8eb43a6b36e6a24ef5893f51d405d25b62e364988223537ae0b in / 
# Wed, 17 Feb 2021 21:17:37 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 00:23:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Feb 2021 00:24:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 18 Feb 2021 00:24:44 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 18 Feb 2021 00:24:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Feb 2021 00:25:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 18 Feb 2021 00:25:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:25:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:25:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Feb 2021 00:40:47 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 01:05:36 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 01:05:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 01:05:52 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 01:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 01:06:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:11:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 01:11:19 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:11:29 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 01:11:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 01:11:46 GMT
CMD ["php" "-a"]
# Fri, 05 Mar 2021 02:08:50 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 02:09:05 GMT
STOPSIGNAL SIGINT
# Fri, 05 Mar 2021 02:09:23 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 02:09:30 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 02:10:27 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 02:10:29 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 02:10:33 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 02:10:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 02:10:56 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 02:11:23 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 02:11:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 02:11:34 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 02:11:42 GMT
USER adminer
# Fri, 05 Mar 2021 02:11:57 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 05 Mar 2021 02:12:05 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:cb672e0375a8f9bb3d33049ceb372ffa49b959bfc84fe6f72bfb97b682a608c8`  
		Last Modified: Wed, 17 Feb 2021 21:18:10 GMT  
		Size: 2.8 MB (2813081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebfde0ed2b25fdf7a28b46b01e73c7891af78bd260ce9c5f46f33a0fd4bba5a`  
		Last Modified: Thu, 18 Feb 2021 01:25:11 GMT  
		Size: 1.7 MB (1741666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c587bda2cf37683b8f80371450083e1533df270a51cbe196c845e7ab52f8943`  
		Last Modified: Thu, 18 Feb 2021 01:25:09 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2faee0918d4167a0323dba5b4244442a3d6cd88d5eacd4a560b72f056274a4`  
		Last Modified: Thu, 18 Feb 2021 01:25:10 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791bb958f337b6cf4b2ea90cf5ac9fcb4612738a152ac4a09a69335da096e59b`  
		Last Modified: Fri, 05 Mar 2021 01:49:57 GMT  
		Size: 10.4 MB (10354080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86e997f6d103c9c5f8aa990ba021777b0a7b8073db6c1aa66166630ac5fb896`  
		Last Modified: Fri, 05 Mar 2021 01:49:55 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97cf656907ab8d840227fdc0e36c17cac097192e975dbb19d8fbc99f3ddde66`  
		Last Modified: Fri, 05 Mar 2021 01:49:59 GMT  
		Size: 15.5 MB (15524632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953ac22358c5b3a72272c4db94f387dafe749dccc315fe715fd54646a7e67fa1`  
		Last Modified: Fri, 05 Mar 2021 01:49:55 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5274e31720b346823b92235766eace03c5b3ca24d9af8910eb3c00a29bc1f48e`  
		Last Modified: Fri, 05 Mar 2021 01:49:56 GMT  
		Size: 17.6 KB (17566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae1914ed9afaacdd2822f6ce3b21c1ba2cfc67fb0a0fc37105941301dde3979`  
		Last Modified: Fri, 05 Mar 2021 02:15:07 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097959a8b93e17b2458e2add93679e6bc07debf1b8ed2e8e39ebdb005d0de353`  
		Last Modified: Fri, 05 Mar 2021 02:15:03 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08378c640496a604d70139ba5075c5cd2fe90d0786621bc4396e7cee75634053`  
		Last Modified: Fri, 05 Mar 2021 02:15:05 GMT  
		Size: 3.9 MB (3918494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4eee7fd3e560e705de2352e9453419f436960844b5ddfda9986cedb09cd6bde`  
		Last Modified: Fri, 05 Mar 2021 02:15:03 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435b254436c62649064c5af03dfecbb978ff36ac4740efbc8a476f538850455e`  
		Last Modified: Fri, 05 Mar 2021 02:15:03 GMT  
		Size: 582.8 KB (582810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38c8209ca8c0d5b2b2b2baae2f460323d08fc90ce007eabd250244bc371189b`  
		Last Modified: Fri, 05 Mar 2021 02:15:05 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.0-standalone` - linux; s390x

```console
$ docker pull adminer@sha256:9035a1407febca18c25bbc2820e9ac6a09281165f387df8d135066d3bcad2d14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32764749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ff9987904c7594d2e9098e19fcc387f22c02e45e942703bd6f07ac77ebbe58`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 00:40:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Feb 2021 00:40:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 18 Feb 2021 00:40:31 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 18 Feb 2021 00:40:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Feb 2021 00:40:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 18 Feb 2021 00:40:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:40:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:40:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Feb 2021 00:51:38 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:17:53 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:17:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:17:54 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:17:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:17:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:21:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:21:14 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:21:14 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:21:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:21:15 GMT
CMD ["php" "-a"]
# Fri, 05 Mar 2021 01:35:01 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 01:35:02 GMT
STOPSIGNAL SIGINT
# Fri, 05 Mar 2021 01:35:03 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 01:35:03 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 01:35:28 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 01:35:28 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 01:35:28 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 01:35:29 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 01:35:29 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 01:35:30 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 01:35:30 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:35:31 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 01:35:31 GMT
USER adminer
# Fri, 05 Mar 2021 01:35:31 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 05 Mar 2021 01:35:31 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2eaf748a32e76be0f1aa6246cb11c8aa5022aa834df364bb87f581198e6376`  
		Last Modified: Thu, 18 Feb 2021 01:26:48 GMT  
		Size: 1.8 MB (1756400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5716be54c61b8e2a38b4d6a0cbece88801726747842f6bd1a50aaf4e8442013f`  
		Last Modified: Thu, 18 Feb 2021 01:26:48 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6aa66a8dad4ec1443c27324fc452b05c4299dbffefcebee55700880033b3ff7`  
		Last Modified: Thu, 18 Feb 2021 01:26:47 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8b7b210cf7a350eb620b3574b19324168c8c4833e0cfe3d634398782f48175`  
		Last Modified: Fri, 05 Mar 2021 00:51:36 GMT  
		Size: 10.4 MB (10354085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a066cfbe30cd983f5ffef2df9d50618ade23fe99302b69e012774b2269585d1`  
		Last Modified: Fri, 05 Mar 2021 00:51:35 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9401205bc3eb7297f85c414b790172be23d1c4ab061aee72eaeb28b69132c073`  
		Last Modified: Fri, 05 Mar 2021 00:51:38 GMT  
		Size: 13.9 MB (13860060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afee2a631a7b79b3c487a3ef4500ea44fa978bd6464fe317d1a65d4b104f7309`  
		Last Modified: Fri, 05 Mar 2021 00:51:35 GMT  
		Size: 2.3 KB (2261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0499fd075a9fd055ca563a90fb4b2aaac9056a65b191d7db41c37188db098cf1`  
		Last Modified: Fri, 05 Mar 2021 00:51:35 GMT  
		Size: 17.6 KB (17566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b53123be7d4a2e60f8c580951db7f413a3fddabf032b97cc4e1715defe06aa`  
		Last Modified: Fri, 05 Mar 2021 01:36:37 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aab483619f81007684651c4b32aae7e47300c44374d5a2e165bfee97c9a5ed8`  
		Last Modified: Fri, 05 Mar 2021 01:36:35 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21994edf819ad8eed5eea7af018652abc984e3d7f67f6dd34ead1779f80b961c`  
		Last Modified: Fri, 05 Mar 2021 01:36:35 GMT  
		Size: 3.6 MB (3583473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39598f68be044d39764fd4f2c72cccb6ff39c29081b324413fb9af80f22c6b6`  
		Last Modified: Fri, 05 Mar 2021 01:36:35 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6988f4418691c53ad239170a2ec56313d0be5ebf6636151c2ab31dee05fd76`  
		Last Modified: Fri, 05 Mar 2021 01:36:35 GMT  
		Size: 582.8 KB (582811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f94af1afe9ebb57211f0f17af8d7edc0ccf29b7fe0f188bae543435432d960`  
		Last Modified: Fri, 05 Mar 2021 01:36:35 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:fastcgi`

```console
$ docker pull adminer@sha256:ddbc8ec701aaf2deafbf06f680f3a1d2cd9b1fffb94d27c1f4395ad50008d9de
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

### `adminer:fastcgi` - linux; amd64

```console
$ docker pull adminer@sha256:bc5ef236fdce0cdf13798c6ce77033b0c9b0946a2b1e93de5e6f43a64b82d004
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33700229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7d4c6e1f2444f36f3d32007c33a6c9cd065f53a81670922522b88fa93450db`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 03:21:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 06 Mar 2021 03:21:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 06 Mar 2021 03:21:31 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 06 Mar 2021 03:21:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 06 Mar 2021 03:21:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 06 Mar 2021 03:31:10 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 06 Mar 2021 03:31:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 03:31:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 03:31:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 06 Mar 2021 04:25:55 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Sat, 06 Mar 2021 04:25:55 GMT
ENV PHP_VERSION=7.4.16
# Sat, 06 Mar 2021 04:25:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Sat, 06 Mar 2021 04:25:56 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Sat, 06 Mar 2021 04:26:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 06 Mar 2021 04:26:02 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Mar 2021 04:33:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Mar 2021 04:33:18 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Sat, 06 Mar 2021 04:33:20 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Mar 2021 04:33:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Mar 2021 04:33:21 GMT
WORKDIR /var/www/html
# Sat, 06 Mar 2021 04:33:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Sat, 06 Mar 2021 04:33:23 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 04:33:23 GMT
EXPOSE 9000
# Sat, 06 Mar 2021 04:33:23 GMT
CMD ["php-fpm"]
# Sat, 06 Mar 2021 08:51:52 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 06 Mar 2021 08:51:53 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 06 Mar 2021 08:52:18 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 06 Mar 2021 08:52:18 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Sat, 06 Mar 2021 08:52:18 GMT
ENV ADMINER_VERSION=4.8.0
# Sat, 06 Mar 2021 08:52:19 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Sat, 06 Mar 2021 08:52:19 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Sat, 06 Mar 2021 08:52:20 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 06 Mar 2021 08:52:21 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 06 Mar 2021 08:52:21 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 06 Mar 2021 08:52:21 GMT
USER adminer
# Sat, 06 Mar 2021 08:52:21 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743181516422399af3888ad5df44c6f711f992b2f86288db9e191ae13de99fa0`  
		Last Modified: Sat, 06 Mar 2021 06:31:08 GMT  
		Size: 1.7 MB (1694870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c307b60e377a3903f74fd9cde3ad69f754071faac36f81ca74e1aa9eabe4851`  
		Last Modified: Sat, 06 Mar 2021 06:31:08 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d5b43308915ce3198dec1c19aa88719afacff02c85660a952982856a0bcc9c`  
		Last Modified: Sat, 06 Mar 2021 06:31:08 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9d5f24e6dd6af8f23f239240af8081c566914e78925b8646ee59d456477a1b`  
		Last Modified: Sat, 06 Mar 2021 06:36:44 GMT  
		Size: 10.4 MB (10354098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfaad94f9a19bca51025c93a5b36fbf3c4e2636a37ecf935233cff9afc27f94`  
		Last Modified: Sat, 06 Mar 2021 06:36:41 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3507948cfcd59468730f9f8ae89b321891415ae8f7c98d96b4662c057f5af471`  
		Last Modified: Sat, 06 Mar 2021 06:36:44 GMT  
		Size: 14.3 MB (14319531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f880a2fb467d3c5d725b4ef31da9c50bcd19a9171455db7a0d4a80a9f80395e`  
		Last Modified: Sat, 06 Mar 2021 06:36:40 GMT  
		Size: 2.3 KB (2265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56deb6830b6ed046fb324d5539b34742ee0aa32484cf961c9fbd5c47aca9a930`  
		Last Modified: Sat, 06 Mar 2021 06:36:41 GMT  
		Size: 17.5 KB (17521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a194189cbad21888697c3cee4fca8f4d5ac096f5ac1eb2981e77d310fa63d6f`  
		Last Modified: Sat, 06 Mar 2021 06:36:40 GMT  
		Size: 8.4 KB (8448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d93b56dad37e253e7efcccf4f4bc0c55f1093fe4a3ee4743ae53353d77a4fb`  
		Last Modified: Sat, 06 Mar 2021 08:53:09 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238c4c0f49a87323787cdbdc3bd37ed5b43bd67fd3d903a5efc67f049bde2cb0`  
		Last Modified: Sat, 06 Mar 2021 08:53:07 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ed295294c14844d5fa520952a46cc832ea9192ab54ceebcd9da78c2b835dd3`  
		Last Modified: Sat, 06 Mar 2021 08:53:07 GMT  
		Size: 3.9 MB (3903344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285104d31a4786a761bed245e8a819ffccb92919702026f95ab8874eaeb112a0`  
		Last Modified: Sat, 06 Mar 2021 08:53:07 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ef4cb5580635a144f2bbf3d755884632850d26926d5b90840cbab8b1642886`  
		Last Modified: Sat, 06 Mar 2021 08:53:08 GMT  
		Size: 582.8 KB (582795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f853ae8f0e76e3efc1e422db5915507f4f50c611294e9c5492f775bd0ecb1f`  
		Last Modified: Sat, 06 Mar 2021 08:53:07 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; arm variant v6

```console
$ docker pull adminer@sha256:2c93d2f0b02908d29d3e3a4228ab25c9c86b812331b270e390a62a9680ff1433
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32424063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f018255660e0906d91baef706cff1811a4410856b0a37263b715383bb70fdcdc`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:17:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Feb 2021 22:17:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 17 Feb 2021 22:17:15 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Feb 2021 22:17:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Feb 2021 22:17:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Feb 2021 22:20:46 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Wed, 17 Feb 2021 22:20:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:20:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:20:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Feb 2021 22:28:41 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:26:48 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:26:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:26:54 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:27:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:27:04 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:30:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:30:26 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:30:30 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:30:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:30:35 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 00:30:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 05 Mar 2021 00:30:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Mar 2021 00:30:42 GMT
EXPOSE 9000
# Fri, 05 Mar 2021 00:30:43 GMT
CMD ["php-fpm"]
# Fri, 05 Mar 2021 01:29:31 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 01:29:34 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 01:30:26 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 01:30:28 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 01:30:32 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 01:30:33 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 01:30:34 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 01:30:38 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 01:30:40 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:30:41 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 01:30:42 GMT
USER adminer
# Fri, 05 Mar 2021 01:30:43 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a33e390360f607fe5a7fe0a0203b7347693b0d8cab270352594a3700e1a1d0`  
		Last Modified: Wed, 17 Feb 2021 22:57:10 GMT  
		Size: 1.7 MB (1684729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d1bbb88bd210deaf33702df9d6fa7f35e72f23dfbb55196147ab537320e9f3`  
		Last Modified: Wed, 17 Feb 2021 22:57:09 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b99fbc527c373db47c36282e5bbd82010870902db2af45982bbb8d700375a32`  
		Last Modified: Wed, 17 Feb 2021 22:57:09 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a4e6f92ba693a7496c53317c79fb8823ac45b33556818a381ca1acb347a311`  
		Last Modified: Fri, 05 Mar 2021 00:53:29 GMT  
		Size: 10.4 MB (10354080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64bd603e34a5bf0fa1834fd5ce8641cedb22c0847f3169c9e72e354c86124cf5`  
		Last Modified: Fri, 05 Mar 2021 00:53:26 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5a57e3834bdaac522a5cdd7b4b6477988fcf852a76cc708026ebebdf3418d8`  
		Last Modified: Fri, 05 Mar 2021 00:53:31 GMT  
		Size: 13.5 MB (13542966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f30d0b9ee8eeabfe33c8ea2c2fcafd27e5f80bcffda325ebb1846975ef034a6`  
		Last Modified: Fri, 05 Mar 2021 00:53:26 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b17255c3c925daf160f37347c78fc54f36e044e2bfd7a8e3bffe95da9645f246`  
		Last Modified: Fri, 05 Mar 2021 00:53:26 GMT  
		Size: 17.6 KB (17565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85523748d905c5ced6faebb10205d1f7d78ae3e4869ede5793c7166ed9f77aff`  
		Last Modified: Fri, 05 Mar 2021 00:53:26 GMT  
		Size: 8.4 KB (8439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1712caab329d945c3f088703ff9c4deec4090358774a7db47f0b7b99c15e87c5`  
		Last Modified: Fri, 05 Mar 2021 01:31:31 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a5a4bdd0e396fbf2a64b84a39e11daf996231c4892713b67a32e9322c81803`  
		Last Modified: Fri, 05 Mar 2021 01:31:31 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9de2c7ce4296df3731f81d52dcc5b36bd803852f0e238ca129824dc7cc262fc`  
		Last Modified: Fri, 05 Mar 2021 01:31:30 GMT  
		Size: 3.6 MB (3603477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797df658ad578348afe4e024e48bbce535519997fa3519bfaf6f43f9a3fbe08b`  
		Last Modified: Fri, 05 Mar 2021 01:31:29 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63a45dd2ec611bee4416bdce98f4eff41d3463dd6d6609a205a19133a310515`  
		Last Modified: Fri, 05 Mar 2021 01:31:30 GMT  
		Size: 582.8 KB (582797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4e6e8ef666b79da7372c6c2125bbf4aa29676e7bdafca00830339affbf7107`  
		Last Modified: Fri, 05 Mar 2021 01:31:30 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:76344293a9cba5c4d934e1de727cfbbad24ec801c6738f8053de6f20f4042dd4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31197081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e91dadff87355741ea5395e5e6d3093bb426a290226eb1bb4da419f1036038`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:56:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Feb 2021 22:57:00 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 17 Feb 2021 22:57:04 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Feb 2021 22:57:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Feb 2021 22:57:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Feb 2021 23:02:51 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Wed, 17 Feb 2021 23:02:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 23:02:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 23:02:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Feb 2021 23:10:45 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:55:10 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:55:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:55:11 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:55:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:55:19 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:58:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:58:21 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:58:25 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:58:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:58:27 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 00:58:29 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 05 Mar 2021 00:58:30 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Mar 2021 00:58:31 GMT
EXPOSE 9000
# Fri, 05 Mar 2021 00:58:31 GMT
CMD ["php-fpm"]
# Fri, 05 Mar 2021 03:17:52 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 03:17:55 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 03:18:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 03:18:46 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 03:18:47 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 03:18:48 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 03:18:49 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 03:18:53 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 03:18:53 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 03:18:54 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 03:18:55 GMT
USER adminer
# Fri, 05 Mar 2021 03:18:56 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf491575714634902d01e3e48f3b92702cb2e4c42056aa5421058d2a2cbfd9f6`  
		Last Modified: Wed, 17 Feb 2021 23:33:58 GMT  
		Size: 1.6 MB (1555125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8ae33f1196d3a62a9383b30d3fd81dd4be1bcf1a99a3d928f585b0d85c5408`  
		Last Modified: Wed, 17 Feb 2021 23:33:58 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16bd16ac2dc3896b7ddf5e8e50bafcc3990d8313dc26634a51beafc97cc6374`  
		Last Modified: Wed, 17 Feb 2021 23:33:58 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d01524e4fc3d179f93abe7a61fc071ecdf6c581f749d96a60690840a8fa15a`  
		Last Modified: Fri, 05 Mar 2021 01:20:43 GMT  
		Size: 10.4 MB (10354089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada63173b828bcc3b5e7d7d61a96a1a4f0a3af46ad66848c75181167c6302b6c`  
		Last Modified: Fri, 05 Mar 2021 01:20:40 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a644dd136e4a568009bc8751ede1d9017381190dc8660db4a7c91ad4bbe6cd`  
		Last Modified: Fri, 05 Mar 2021 01:20:45 GMT  
		Size: 12.7 MB (12670824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a36409e92a747f08911634d5cad27605075c881509247a1abea57e68679210`  
		Last Modified: Fri, 05 Mar 2021 01:20:40 GMT  
		Size: 2.3 KB (2263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6111685ad3b47ae7d882febd0446f781cf086d73c476fd00e53527166c5fa7`  
		Last Modified: Fri, 05 Mar 2021 01:20:40 GMT  
		Size: 17.6 KB (17565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b43d0062c0be09cf3da7b8d797ec945fa4a15872201297c8fc68c7c7fb5c0e`  
		Last Modified: Fri, 05 Mar 2021 01:20:40 GMT  
		Size: 8.4 KB (8441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce8f178b810d2b0b4986e7a6068e8e0a703cb9601aee7af7f6235398197d74c`  
		Last Modified: Fri, 05 Mar 2021 03:19:38 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b2f6c2d0c7d9165289f4145f9fb2d5bd3622112bcb40a5555d56f3358b9705`  
		Last Modified: Fri, 05 Mar 2021 03:19:36 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a09c36d006daa2967af8b26e2157350bb5c39f1101544c40298a9879857f951`  
		Last Modified: Fri, 05 Mar 2021 03:19:36 GMT  
		Size: 3.6 MB (3576364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e5deca6d2f48ec567fff9f38134e4504ee858f1a6de2b415ff6f147b559865`  
		Last Modified: Fri, 05 Mar 2021 03:19:36 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c078244c143c12118d608de1dacae67d924b37e40fa5ff5e1626d7603db96c77`  
		Last Modified: Fri, 05 Mar 2021 03:19:36 GMT  
		Size: 582.8 KB (582808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399c2c8d9bb3754b99dd4e63d7f86d9a17b1ba333afbcdd1a91323827dbf6c19`  
		Last Modified: Fri, 05 Mar 2021 03:19:36 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:9d290c8427c90264c046b18b2dad85bf1ab72b9636a299fdcdb70e725b73cf37
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.6 MB (33587124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fda254daa0110b7ed8e11936831a70eb476e6bac9d0f864a167cc3ca89cc570`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 23:42:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Feb 2021 23:42:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 17 Feb 2021 23:42:38 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Feb 2021 23:42:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Feb 2021 23:42:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Feb 2021 23:47:35 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Wed, 17 Feb 2021 23:47:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 23:47:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 23:47:37 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Feb 2021 23:57:44 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:42:58 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:43:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:43:01 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:43:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:43:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:47:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:47:53 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:47:56 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:47:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:47:58 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 00:48:00 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 05 Mar 2021 00:48:00 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Mar 2021 00:48:01 GMT
EXPOSE 9000
# Fri, 05 Mar 2021 00:48:02 GMT
CMD ["php-fpm"]
# Fri, 05 Mar 2021 02:06:30 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 02:06:33 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 02:07:32 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 02:07:34 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 02:07:35 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 02:07:37 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 02:07:38 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 02:07:42 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 02:07:43 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 02:07:44 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 02:07:46 GMT
USER adminer
# Fri, 05 Mar 2021 02:07:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4b642bcaaef409203aaedc803835562ee86d3ea457bf4ccdd22e5d7b2367f1`  
		Last Modified: Thu, 18 Feb 2021 00:23:35 GMT  
		Size: 1.7 MB (1694455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ea39643e14bb66b107bb23b02b8c7a193ed89d38f4ae52b1decbe763fb0db9`  
		Last Modified: Thu, 18 Feb 2021 00:23:34 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3455119714d8ce066305d3b121e103a3cf690db26bb556906ba67e7a7c1f559`  
		Last Modified: Thu, 18 Feb 2021 00:23:34 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5fb9efa5fb7c6758d0c1ef8f8dec26c072a0b3db105d3bc1072051a584a31e`  
		Last Modified: Fri, 05 Mar 2021 01:14:03 GMT  
		Size: 10.4 MB (10354114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b86fa187c3fdc5dc79bdeb0cc5299859c0c0095b732f4ee415c0bb12daa215b`  
		Last Modified: Fri, 05 Mar 2021 01:14:00 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12f3432275b2be2dd42ee1df485264de064473b2c82feda5bf9c9d20b5b271b`  
		Last Modified: Fri, 05 Mar 2021 01:14:04 GMT  
		Size: 14.3 MB (14335600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c51b3d598680e53ab4687fb42e8f593583f31bd96bddf4f4a3260e7ce39978`  
		Last Modified: Fri, 05 Mar 2021 01:14:00 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f84e9090c4bc7becc3688c7892a83e9851718fc9492734a99d408a8f37e5940`  
		Last Modified: Fri, 05 Mar 2021 01:14:00 GMT  
		Size: 17.6 KB (17578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6e5a4c4a59a3a7880ef2d31091da082e89c8a5d36fe48cc0e6d2a869a4c015`  
		Last Modified: Fri, 05 Mar 2021 01:14:00 GMT  
		Size: 8.4 KB (8443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c96f48785c9c98e7112aba8a63a131c4068630fb03bf917709cbf26dcde0f6`  
		Last Modified: Fri, 05 Mar 2021 02:08:29 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68227b3239ccce99fdd4b5f144a2966beb055b69b3cd677b07dc854149769ed7`  
		Last Modified: Fri, 05 Mar 2021 02:08:28 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ee8c6445369dac5a5c0a1eebb4a5de36d9b41daa6842a89ffd90533c70d115`  
		Last Modified: Fri, 05 Mar 2021 02:08:28 GMT  
		Size: 3.9 MB (3874581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd6128ec00cfc5bafbcbb5cd0958f7c6bb1789fdd6d9f462f7bdfb945d25051`  
		Last Modified: Fri, 05 Mar 2021 02:08:27 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e85b4b40588c16a96e7bd4ebc9bda548027f1d29a882087ca1873edbe5c6a3e`  
		Last Modified: Fri, 05 Mar 2021 02:08:28 GMT  
		Size: 582.8 KB (582807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52d3bffbd635505b2a6fe9733d78a3056c37f05d763c518a0cfbb0e62ae6fa8`  
		Last Modified: Fri, 05 Mar 2021 02:08:28 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:26d15f54137462efdfea2e074d6e3aab1a83d2e91bfb268a77550109c29e494e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34296076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f79ec5602cf1203e859966ea84f6f0af410574c66ff1695966634f7fa99a0602`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 02:13:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 06 Mar 2021 02:13:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 06 Mar 2021 02:13:32 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 06 Mar 2021 02:13:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 06 Mar 2021 02:13:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 06 Mar 2021 02:20:59 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 06 Mar 2021 02:20:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 02:20:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 02:21:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 06 Mar 2021 03:09:15 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Sat, 06 Mar 2021 03:09:15 GMT
ENV PHP_VERSION=7.4.16
# Sat, 06 Mar 2021 03:09:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Sat, 06 Mar 2021 03:09:16 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Sat, 06 Mar 2021 03:09:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 06 Mar 2021 03:09:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Mar 2021 03:18:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Mar 2021 03:18:11 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Sat, 06 Mar 2021 03:18:13 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Mar 2021 03:18:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Mar 2021 03:18:14 GMT
WORKDIR /var/www/html
# Sat, 06 Mar 2021 03:18:15 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Sat, 06 Mar 2021 03:18:15 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 03:18:16 GMT
EXPOSE 9000
# Sat, 06 Mar 2021 03:18:16 GMT
CMD ["php-fpm"]
# Sat, 06 Mar 2021 08:16:46 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 06 Mar 2021 08:16:47 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 06 Mar 2021 08:17:17 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 06 Mar 2021 08:17:17 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Sat, 06 Mar 2021 08:17:18 GMT
ENV ADMINER_VERSION=4.8.0
# Sat, 06 Mar 2021 08:17:18 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Sat, 06 Mar 2021 08:17:18 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Sat, 06 Mar 2021 08:17:20 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 06 Mar 2021 08:17:20 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 06 Mar 2021 08:17:20 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 06 Mar 2021 08:17:21 GMT
USER adminer
# Sat, 06 Mar 2021 08:17:21 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d779edf81d3549de0c570804cffa8279f4a980d3fed1292285070f24a1b00f`  
		Last Modified: Sat, 06 Mar 2021 05:47:24 GMT  
		Size: 1.8 MB (1793700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce9d30537e4bf7ab9ad24ea334671e794e0830680c386cf4b36dbba54dd40c5`  
		Last Modified: Sat, 06 Mar 2021 05:47:23 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f119038c35efd6cc0b1a27c432b2fc338da413650c224359556d95e0bf8214`  
		Last Modified: Sat, 06 Mar 2021 05:47:23 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5397827f225e72f10184ff09624c35bf31a5231897f53e91ca07da5f62e873dc`  
		Last Modified: Sat, 06 Mar 2021 05:54:56 GMT  
		Size: 10.4 MB (10354073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8309650059a0810adb36671135e0f311a358f75fb9dd4d4de7e8ca2e03df4ecd`  
		Last Modified: Sat, 06 Mar 2021 05:54:52 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8ec289fc161bd97f4660f6a9b0102128d91f8545b7a66236470e13f99820a6`  
		Last Modified: Sat, 06 Mar 2021 05:54:56 GMT  
		Size: 14.7 MB (14703205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df93dca921888af6f7dd240ba41be2492ce1b35f2a7691841b7453de8097cba`  
		Last Modified: Sat, 06 Mar 2021 05:54:52 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a789e9947572f56584832fc18a9febda69c07a7fd803f86bb47b8b76048e0d`  
		Last Modified: Sat, 06 Mar 2021 05:54:52 GMT  
		Size: 17.5 KB (17499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7a016c5403915747cc20016342dd4a30b61cf26f6ecfbf3db8dc913816ba0d`  
		Last Modified: Sat, 06 Mar 2021 05:54:52 GMT  
		Size: 8.4 KB (8443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20574028b280be669aaf096c2a36ea615748c8d8947b537fed28011a1bba827`  
		Last Modified: Sat, 06 Mar 2021 08:18:31 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcffc992f5c3c59e7de4cf88a6b3a2bcea4814b1479dd0fd6533b32693a2337`  
		Last Modified: Sat, 06 Mar 2021 08:18:28 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d41c527ce013e3f17159bc459ca0d55a95da81bcc5e14571bbe997c5156b6e0`  
		Last Modified: Sat, 06 Mar 2021 08:18:30 GMT  
		Size: 4.0 MB (4010213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad6f6db03a695dc6910470b21945bc6f75b04d9f24622618a244bced44e9a04`  
		Last Modified: Sat, 06 Mar 2021 08:18:29 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde165942766dd540d19ff22ecd092d80baff426cd360af35eb0fb5ef30b2dac`  
		Last Modified: Sat, 06 Mar 2021 08:18:29 GMT  
		Size: 582.8 KB (582800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a269b82e491105b4090cf94096e9ce312f49c2e7c64fc59ce8fca97a0048d95`  
		Last Modified: Sat, 06 Mar 2021 08:18:28 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:60214217e7c6d9d5d171f4a2f5b8e64a7616f02249811ff70fc139b463c8c1a6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (35045727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195aaf01b7fc54d33fea092504c0b5d14247b799d81fbb46ce985ef115ac65c8`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 17 Feb 2021 21:17:29 GMT
ADD file:28f4377c61c0f8eb43a6b36e6a24ef5893f51d405d25b62e364988223537ae0b in / 
# Wed, 17 Feb 2021 21:17:37 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 00:23:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Feb 2021 00:24:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 18 Feb 2021 00:24:44 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 18 Feb 2021 00:24:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Feb 2021 00:25:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 18 Feb 2021 00:32:20 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 18 Feb 2021 00:32:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:32:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:32:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Feb 2021 00:47:19 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 01:12:05 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 01:12:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 01:12:14 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 01:12:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 01:12:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:17:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 01:17:41 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:17:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 01:17:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 01:18:00 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 01:18:13 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 05 Mar 2021 01:18:18 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Mar 2021 01:18:22 GMT
EXPOSE 9000
# Fri, 05 Mar 2021 01:18:25 GMT
CMD ["php-fpm"]
# Fri, 05 Mar 2021 02:12:29 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 02:12:47 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 02:13:39 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 02:13:41 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 02:13:45 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 02:13:50 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 02:13:54 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 02:14:11 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 02:14:12 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 02:14:17 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 02:14:23 GMT
USER adminer
# Fri, 05 Mar 2021 02:14:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:cb672e0375a8f9bb3d33049ceb372ffa49b959bfc84fe6f72bfb97b682a608c8`  
		Last Modified: Wed, 17 Feb 2021 21:18:10 GMT  
		Size: 2.8 MB (2813081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebfde0ed2b25fdf7a28b46b01e73c7891af78bd260ce9c5f46f33a0fd4bba5a`  
		Last Modified: Thu, 18 Feb 2021 01:25:11 GMT  
		Size: 1.7 MB (1741666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c587bda2cf37683b8f80371450083e1533df270a51cbe196c845e7ab52f8943`  
		Last Modified: Thu, 18 Feb 2021 01:25:09 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2faee0918d4167a0323dba5b4244442a3d6cd88d5eacd4a560b72f056274a4`  
		Last Modified: Thu, 18 Feb 2021 01:25:10 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50832ff8121fa6dabe4fef261cdf442de13beba3eba5b02edc01bb52575f604`  
		Last Modified: Fri, 05 Mar 2021 01:50:47 GMT  
		Size: 10.4 MB (10354080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492225a51fbf5c42138184c0b8f334e0c03349c39df922382ab84510b28fa495`  
		Last Modified: Fri, 05 Mar 2021 01:50:40 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e38b008adbe62b7a3a5140dedb456e37ae0f03fe3970c9f2386f7b294c13c3`  
		Last Modified: Fri, 05 Mar 2021 01:50:44 GMT  
		Size: 15.6 MB (15601592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac2e3566364c50161e37f74f62cc1631496ad06e929b660adcd70dd66254b3d`  
		Last Modified: Fri, 05 Mar 2021 01:50:40 GMT  
		Size: 2.3 KB (2265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48abd24364092c58878a940181d9510d843d157a2e6649ea9fe3f8452341d5e0`  
		Last Modified: Fri, 05 Mar 2021 01:50:40 GMT  
		Size: 17.6 KB (17568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c82139d7ee7be2c8e6f6313bad71cc515fcb36b36f9db46406380c839a21ff`  
		Last Modified: Fri, 05 Mar 2021 01:50:40 GMT  
		Size: 8.4 KB (8445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb87a4b5911ea0082c17ed927c804ab2ef1074f3e4a232baee3c7aa0d53f2001`  
		Last Modified: Fri, 05 Mar 2021 02:15:36 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:867bbe031ef2fdc9b041f464c092ae860709ae7089ad3bf2d020ca9a5685adb9`  
		Last Modified: Fri, 05 Mar 2021 02:15:33 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1352d4abeeccc4cdec18fe083cca986917a96a75c051377c6e6f60df25b8b7`  
		Last Modified: Fri, 05 Mar 2021 02:15:35 GMT  
		Size: 3.9 MB (3918505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf3106a1ac6be7ebc6cac6752295d88ad3e0b6dde2a752abbcf19665597f91d`  
		Last Modified: Fri, 05 Mar 2021 02:15:32 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7e5c63ff249b14ce430b50a9d068fd75bd570c8e3dda8a120527bbeb589643`  
		Last Modified: Fri, 05 Mar 2021 02:15:32 GMT  
		Size: 582.8 KB (582811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5372a8bc61644fe0469438556e96846b6dd32a217c62c627af9666e934dc59d0`  
		Last Modified: Fri, 05 Mar 2021 02:15:34 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:172c17539eec169a1efbc7bdb5582b0c6d68a767c96c91534eaa512ea11f1a54
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32837225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e84b58503996daca80603c6caf456f29c872d2fbcedc12f3883b3ff932310f5`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 00:40:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Feb 2021 00:40:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 18 Feb 2021 00:40:31 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 18 Feb 2021 00:40:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Feb 2021 00:40:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 18 Feb 2021 00:46:04 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 18 Feb 2021 00:46:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:46:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:46:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Feb 2021 00:56:47 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:21:28 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:21:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:21:28 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:21:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:21:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:24:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:24:36 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:24:37 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:24:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:24:37 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 00:24:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 05 Mar 2021 00:24:38 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Mar 2021 00:24:38 GMT
EXPOSE 9000
# Fri, 05 Mar 2021 00:24:38 GMT
CMD ["php-fpm"]
# Fri, 05 Mar 2021 01:35:37 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 01:35:38 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 01:36:11 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 01:36:11 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 01:36:12 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 01:36:12 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 01:36:13 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 01:36:14 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 01:36:14 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:36:15 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 01:36:15 GMT
USER adminer
# Fri, 05 Mar 2021 01:36:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2eaf748a32e76be0f1aa6246cb11c8aa5022aa834df364bb87f581198e6376`  
		Last Modified: Thu, 18 Feb 2021 01:26:48 GMT  
		Size: 1.8 MB (1756400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5716be54c61b8e2a38b4d6a0cbece88801726747842f6bd1a50aaf4e8442013f`  
		Last Modified: Thu, 18 Feb 2021 01:26:48 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6aa66a8dad4ec1443c27324fc452b05c4299dbffefcebee55700880033b3ff7`  
		Last Modified: Thu, 18 Feb 2021 01:26:47 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ec6de43c42608abedaf0d1351eac485f25cf6ea8189784c33b0bd55cf4c8de`  
		Last Modified: Fri, 05 Mar 2021 00:51:59 GMT  
		Size: 10.4 MB (10354080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7f932c8c75e84329764906d4a66784a32d6eebc1e0bf7b70c2e6608e3fbf9b`  
		Last Modified: Fri, 05 Mar 2021 00:51:56 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94d974f2d24d19a056887cdf386d4e9505e841d3a06c71f3ffa4eda14b55cd5`  
		Last Modified: Fri, 05 Mar 2021 00:51:59 GMT  
		Size: 13.9 MB (13924090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69925775200e946533560678d8a38f9ae9c806a7f163e84949bcbcb5b90adcf5`  
		Last Modified: Fri, 05 Mar 2021 00:51:56 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e58476f31db9ac4d71c9e0ea37118bbbd9193cc0b3aea7cc05bab5c83ddff8`  
		Last Modified: Fri, 05 Mar 2021 00:51:56 GMT  
		Size: 17.6 KB (17562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c27cda61463930e8e9c42f8de03c8a59af15035338f16a147b75cfff1adc6bb`  
		Last Modified: Fri, 05 Mar 2021 00:51:56 GMT  
		Size: 8.4 KB (8445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536690e7823ee104420228155dfb821af13a367f39347bb42c6536a406b031c2`  
		Last Modified: Fri, 05 Mar 2021 01:36:49 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f87e2102e12d1ceefff1f2490100e7e4a089955c1ec33e2d52db85d8706f9c`  
		Last Modified: Fri, 05 Mar 2021 01:36:47 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180b148ebd9e445d7b63cfd748624466a392b06d40e4980de5a006e90fe54def`  
		Last Modified: Fri, 05 Mar 2021 01:36:48 GMT  
		Size: 3.6 MB (3583484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95fc51e3df0e6750051bc696529caddc5ee514b5c8d0515a39eee82a06e9739a`  
		Last Modified: Fri, 05 Mar 2021 01:36:47 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5435da686f45a2ef26c52cb075980530af7e8ef76884a406b5a0e9b3068a28`  
		Last Modified: Fri, 05 Mar 2021 01:36:47 GMT  
		Size: 582.8 KB (582804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472506157be8ba02f17eab06907cba644d1ead543ffe97be2a01f98d2a45ad45`  
		Last Modified: Fri, 05 Mar 2021 01:36:47 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:latest`

```console
$ docker pull adminer@sha256:1ee6ed00d1169a14a1030a1d44a5ab1724392c115d296d98f0a0e8700628deeb
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

### `adminer:latest` - linux; amd64

```console
$ docker pull adminer@sha256:d7cbbb92e43f7d55027a58bd115d9425548325f3754cb705b03368243b3930d3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.6 MB (33625851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d5528d5e4b1e1e879cf6d3b49b09245873a231a6054521f40a538633893e3d`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 03:21:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 06 Mar 2021 03:21:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 06 Mar 2021 03:21:31 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 06 Mar 2021 03:21:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 06 Mar 2021 03:21:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 06 Mar 2021 03:21:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 03:21:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 03:21:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 06 Mar 2021 04:18:25 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Sat, 06 Mar 2021 04:18:25 GMT
ENV PHP_VERSION=7.4.16
# Sat, 06 Mar 2021 04:18:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Sat, 06 Mar 2021 04:18:26 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Sat, 06 Mar 2021 04:18:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 06 Mar 2021 04:18:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Mar 2021 04:25:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Mar 2021 04:25:46 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Sat, 06 Mar 2021 04:25:48 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Mar 2021 04:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Mar 2021 04:25:49 GMT
CMD ["php" "-a"]
# Sat, 06 Mar 2021 08:51:16 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 06 Mar 2021 08:51:16 GMT
STOPSIGNAL SIGINT
# Sat, 06 Mar 2021 08:51:17 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 06 Mar 2021 08:51:17 GMT
WORKDIR /var/www/html
# Sat, 06 Mar 2021 08:51:43 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 06 Mar 2021 08:51:43 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Sat, 06 Mar 2021 08:51:43 GMT
ENV ADMINER_VERSION=4.8.0
# Sat, 06 Mar 2021 08:51:44 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Sat, 06 Mar 2021 08:51:44 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Sat, 06 Mar 2021 08:51:46 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 06 Mar 2021 08:51:46 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 06 Mar 2021 08:51:46 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 06 Mar 2021 08:51:46 GMT
USER adminer
# Sat, 06 Mar 2021 08:51:46 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 06 Mar 2021 08:51:47 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743181516422399af3888ad5df44c6f711f992b2f86288db9e191ae13de99fa0`  
		Last Modified: Sat, 06 Mar 2021 06:31:08 GMT  
		Size: 1.7 MB (1694870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c307b60e377a3903f74fd9cde3ad69f754071faac36f81ca74e1aa9eabe4851`  
		Last Modified: Sat, 06 Mar 2021 06:31:08 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d5b43308915ce3198dec1c19aa88719afacff02c85660a952982856a0bcc9c`  
		Last Modified: Sat, 06 Mar 2021 06:31:08 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4848a1e010e4e0cda8de291fa6ed2f3efecf20d7343a69cec21878885828d2d`  
		Last Modified: Sat, 06 Mar 2021 06:35:54 GMT  
		Size: 10.4 MB (10354097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8e88ab7b4e15d3c4d8d099845669643447a702d27188138ed20f8c14879cde`  
		Last Modified: Sat, 06 Mar 2021 06:35:54 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c6688ec4022c9042fad0bff0a5aaa03cd55628577fe71a419761ca5478392c`  
		Last Modified: Sat, 06 Mar 2021 06:35:56 GMT  
		Size: 14.3 MB (14253596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b401e642cd6c785a0ede5899c8a1fb93770d6eaf04a0a5faeb0183ad5c21f3`  
		Last Modified: Sat, 06 Mar 2021 06:35:54 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4aa45ba156c9e4af51f7b2a5eec317be47eca6ba8e9bb8fc368488ea41c11c`  
		Last Modified: Sat, 06 Mar 2021 06:35:54 GMT  
		Size: 17.5 KB (17518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b686977c50b0410c0084a21bef42aae47c53441ee7defe7b25bcad585a19999`  
		Last Modified: Sat, 06 Mar 2021 08:52:42 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf15bf71cdf8a60508b2773274a23124c80de6ad9611b97bd532869bdce6929`  
		Last Modified: Sat, 06 Mar 2021 08:52:38 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7855e8a455940ec1b6c2e7a9d42e3a94e92b3f7dd253bfdefd2ef4f0b272a242`  
		Last Modified: Sat, 06 Mar 2021 08:52:40 GMT  
		Size: 3.9 MB (3903349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff73275236b8945efe2dadf9b67d73cc5c24fb699f0e3265cbdb3445bdabcba`  
		Last Modified: Sat, 06 Mar 2021 08:52:38 GMT  
		Size: 1.5 KB (1471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64cfef0d91dbc6948021e94ae4407132c018d08d4446215342ad7e0447e33383`  
		Last Modified: Sat, 06 Mar 2021 08:52:39 GMT  
		Size: 582.8 KB (582798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7097b3e809e2d58f970ecec3070fa3db82d914e74c47172eb2c2800e051290`  
		Last Modified: Sat, 06 Mar 2021 08:52:39 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm variant v6

```console
$ docker pull adminer@sha256:67ecf13bed27733de831bad0889ec483ede8530402c3c46011d2334e4a991c25
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32352290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4b093e53cd99d8904355485561c5dd006e3077e79bf2eaba849078b7c8ff3b`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:17:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Feb 2021 22:17:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 17 Feb 2021 22:17:15 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Feb 2021 22:17:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Feb 2021 22:17:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Feb 2021 22:17:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:17:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:17:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Feb 2021 22:24:49 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:22:42 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:22:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:22:48 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:22:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:23:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:26:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:26:24 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:26:28 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:26:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:26:30 GMT
CMD ["php" "-a"]
# Fri, 05 Mar 2021 01:28:12 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 01:28:12 GMT
STOPSIGNAL SIGINT
# Fri, 05 Mar 2021 01:28:15 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 01:28:15 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 01:29:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 01:29:05 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 01:29:06 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 01:29:07 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 01:29:08 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 01:29:11 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 01:29:11 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:29:12 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 01:29:13 GMT
USER adminer
# Fri, 05 Mar 2021 01:29:13 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 05 Mar 2021 01:29:14 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a33e390360f607fe5a7fe0a0203b7347693b0d8cab270352594a3700e1a1d0`  
		Last Modified: Wed, 17 Feb 2021 22:57:10 GMT  
		Size: 1.7 MB (1684729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d1bbb88bd210deaf33702df9d6fa7f35e72f23dfbb55196147ab537320e9f3`  
		Last Modified: Wed, 17 Feb 2021 22:57:09 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b99fbc527c373db47c36282e5bbd82010870902db2af45982bbb8d700375a32`  
		Last Modified: Wed, 17 Feb 2021 22:57:09 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37a52f8d6a0669099c893e2b3e9ce5d8862eed5489a15f8dafd39f664233b7c`  
		Last Modified: Fri, 05 Mar 2021 00:53:01 GMT  
		Size: 10.4 MB (10354085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e31438bda764d2d788352c3dbdc563f97c840ce2736c283190e590e11a4641`  
		Last Modified: Fri, 05 Mar 2021 00:52:59 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615508ce208f1bfacc67745161a522490ffde3254a7e5b88e2a75704a178b65d`  
		Last Modified: Fri, 05 Mar 2021 00:53:05 GMT  
		Size: 13.5 MB (13479609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49bab722652cd2c45df88dee34d635b0c4824fd1885e9cdb6fa1ad1c707b24d`  
		Last Modified: Fri, 05 Mar 2021 00:52:59 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b5e7fa68211b0722b528ee1f7b5f413c32b3581eec56fc37d056cf1e44d45f`  
		Last Modified: Fri, 05 Mar 2021 00:52:59 GMT  
		Size: 17.6 KB (17574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a863fe1948ed188002b2c53e19c1c4f06aa611913e9aee2e6d37a4b38892fa27`  
		Last Modified: Fri, 05 Mar 2021 01:31:18 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e5d7f207dfb0131e75fb5675de4013a21ec2a9965b6a5f2974a09de577b376`  
		Last Modified: Fri, 05 Mar 2021 01:31:15 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613aba5afd5742d6a2f8c093d4d9e2e3eef9f92d01853c139b3f7690a577fd1d`  
		Last Modified: Fri, 05 Mar 2021 01:31:16 GMT  
		Size: 3.6 MB (3603470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ea9f569f958143bd38a220ee729c6ef6f85c122fe3f42b2a761b57e39df3e9`  
		Last Modified: Fri, 05 Mar 2021 01:31:15 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e6944e336be980c37b3af333b01dab0f1b3db12af184e3cc0ed1d4a326a6ab`  
		Last Modified: Fri, 05 Mar 2021 01:31:15 GMT  
		Size: 582.8 KB (582808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4644911e6f4e52234e1b7b359c25f4998c5be8fe108e2f0b54e5cfd721d2d9`  
		Last Modified: Fri, 05 Mar 2021 01:31:15 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm variant v7

```console
$ docker pull adminer@sha256:3c5fe027a505612b8c787c41923bc81f01eba12776b7827fb8de3b48fadd12ff
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31126385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7625601231cbbafd93c468bb5506f91c320be7c6640088ec3203f7b61bcae845`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:56:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Feb 2021 22:57:00 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 17 Feb 2021 22:57:04 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Feb 2021 22:57:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Feb 2021 22:57:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Feb 2021 22:57:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:57:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:57:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Feb 2021 23:07:25 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:51:51 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:51:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:51:52 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:51:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:51:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:54:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:54:56 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:55:00 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:55:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:55:01 GMT
CMD ["php" "-a"]
# Fri, 05 Mar 2021 03:16:34 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 03:16:35 GMT
STOPSIGNAL SIGINT
# Fri, 05 Mar 2021 03:16:37 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 03:16:37 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 03:17:32 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 03:17:34 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 03:17:35 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 03:17:36 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 03:17:36 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 03:17:39 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 03:17:40 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 03:17:41 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 03:17:42 GMT
USER adminer
# Fri, 05 Mar 2021 03:17:42 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 05 Mar 2021 03:17:43 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf491575714634902d01e3e48f3b92702cb2e4c42056aa5421058d2a2cbfd9f6`  
		Last Modified: Wed, 17 Feb 2021 23:33:58 GMT  
		Size: 1.6 MB (1555125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8ae33f1196d3a62a9383b30d3fd81dd4be1bcf1a99a3d928f585b0d85c5408`  
		Last Modified: Wed, 17 Feb 2021 23:33:58 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16bd16ac2dc3896b7ddf5e8e50bafcc3990d8313dc26634a51beafc97cc6374`  
		Last Modified: Wed, 17 Feb 2021 23:33:58 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224ef988837049de958e2e9476510f82fe8e42270706a0671a5a463f6ae97dc2`  
		Last Modified: Fri, 05 Mar 2021 01:20:19 GMT  
		Size: 10.4 MB (10354091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9e75985cf89dec0ed12206b36f371ffbda22ccf6cdbccf5d19345e62db2c14`  
		Last Modified: Fri, 05 Mar 2021 01:20:16 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3067a7094a3949ddb39a5787e92b263164d2eb287f0d508c0497dc270667f7a2`  
		Last Modified: Fri, 05 Mar 2021 01:20:19 GMT  
		Size: 12.6 MB (12608573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e967fccc5675136a3112da05f19624319efe2274faf250ffc942f8df1727990b`  
		Last Modified: Fri, 05 Mar 2021 01:20:15 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bee2c4ad784aa0aa254a050c45062e42eae3e6414649f1e7372db7fe0845817`  
		Last Modified: Fri, 05 Mar 2021 01:20:15 GMT  
		Size: 17.6 KB (17556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd957d7c1659b87bbacdaaa44de1493cd86ce1058104890fa7f886c244af7e2`  
		Last Modified: Fri, 05 Mar 2021 03:19:23 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a9b53808941e232e796f0fce8be1b1a2bdab2ab0d1227f671cdc2e6d8acecd`  
		Last Modified: Fri, 05 Mar 2021 03:19:21 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b983fd5f2f41ac862e588d3c7cb994ae11a6d4dfd1273298d35ff8fcdc87e72`  
		Last Modified: Fri, 05 Mar 2021 03:19:21 GMT  
		Size: 3.6 MB (3576366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957ff1dc0df9c3cd0fa022e0ae444a04b77d5b488a38dcba9673c2f3dfb07f8d`  
		Last Modified: Fri, 05 Mar 2021 03:19:21 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d418e42a87cf9ea044ec23d04a0b56e7f7b51dbab5639eb0e1c16248b88575`  
		Last Modified: Fri, 05 Mar 2021 03:19:21 GMT  
		Size: 582.8 KB (582806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1688bcdb1a112479d4950eae42069fa29ff4e81e587b2387362b4a6cc0fbe2`  
		Last Modified: Fri, 05 Mar 2021 03:19:21 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:7991be9e1a1ee3f2c5d374475d3746026dd7ca64a60167a65551567d7cfccf43
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33506242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11682bbe518b1faa63b82b75d246e7c35612d6d253da8f2011c0539c5b07f5cc`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 23:42:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Feb 2021 23:42:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 17 Feb 2021 23:42:38 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Feb 2021 23:42:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Feb 2021 23:42:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Feb 2021 23:42:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 23:42:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 23:42:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Feb 2021 23:53:01 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:37:35 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:37:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:37:38 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:37:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:37:47 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:42:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:42:39 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:42:44 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:42:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:42:47 GMT
CMD ["php" "-a"]
# Fri, 05 Mar 2021 02:04:43 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 02:04:44 GMT
STOPSIGNAL SIGINT
# Fri, 05 Mar 2021 02:04:48 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 02:04:50 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 02:05:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 02:05:56 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 02:05:57 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 02:05:57 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 02:05:58 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 02:06:02 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 02:06:03 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 02:06:04 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 02:06:05 GMT
USER adminer
# Fri, 05 Mar 2021 02:06:06 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 05 Mar 2021 02:06:06 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4b642bcaaef409203aaedc803835562ee86d3ea457bf4ccdd22e5d7b2367f1`  
		Last Modified: Thu, 18 Feb 2021 00:23:35 GMT  
		Size: 1.7 MB (1694455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ea39643e14bb66b107bb23b02b8c7a193ed89d38f4ae52b1decbe763fb0db9`  
		Last Modified: Thu, 18 Feb 2021 00:23:34 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3455119714d8ce066305d3b121e103a3cf690db26bb556906ba67e7a7c1f559`  
		Last Modified: Thu, 18 Feb 2021 00:23:34 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a68a1ddf490519ddbcd4f75589909c8d4703a6b902bae2a7319905984b7547`  
		Last Modified: Fri, 05 Mar 2021 01:13:32 GMT  
		Size: 10.4 MB (10354115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1754592c0391f5b7b27cf3c7110b1e2a917ebb769b0ceaf9bfdfd0181cc6cb`  
		Last Modified: Fri, 05 Mar 2021 01:13:30 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a402e34d4d52011f5ecf29a826d7fd94dc474fdf156b70d506d3deaeb2a4d3b`  
		Last Modified: Fri, 05 Mar 2021 01:13:34 GMT  
		Size: 14.3 MB (14263146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1702d0137849d4baf63d0536ee9f8391c72c295a46613ed43c270f3cc81a90`  
		Last Modified: Fri, 05 Mar 2021 01:13:31 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ebe5152320826ffaea66119f3e759ce05ed98bb09a201643ee6674cbd9685e`  
		Last Modified: Fri, 05 Mar 2021 01:13:31 GMT  
		Size: 17.6 KB (17574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a42655d4ea3811b755ccede7be6704d6e30a4e912c6ec284807f25e1874c11`  
		Last Modified: Fri, 05 Mar 2021 02:08:13 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36983a97af0e64abf039823af9b57936cc5add643fab48f1d64ca7fbeb076a02`  
		Last Modified: Fri, 05 Mar 2021 02:08:11 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23c53be365e785ad30481daf9c58f08857ca80fc5fc681e12655557a14f7093`  
		Last Modified: Fri, 05 Mar 2021 02:08:12 GMT  
		Size: 3.9 MB (3874584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d698ddfcb363647524ac96d6fe45138e9aa228c8662ec68d2c877a5862a6257`  
		Last Modified: Fri, 05 Mar 2021 02:08:11 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e7497f33585536dba243eedb8aea95c51b88677f674845065a15d776a0e7c78`  
		Last Modified: Fri, 05 Mar 2021 02:08:12 GMT  
		Size: 582.8 KB (582809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041eab10d184403fbf0b2a94255c47e5618bc99fd708586209ad66d02a41c86b`  
		Last Modified: Fri, 05 Mar 2021 02:08:11 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; 386

```console
$ docker pull adminer@sha256:3c12e8f857cf7b920500273d347a57b13be7f75bc361cd49631704781e87dafe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34214715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8de5231523b1be5d66db42c66ace28ceef73e37457dc22956bd36744ea35592f`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 02:13:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 06 Mar 2021 02:13:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 06 Mar 2021 02:13:32 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 06 Mar 2021 02:13:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 06 Mar 2021 02:13:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 06 Mar 2021 02:13:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 02:13:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 02:13:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 06 Mar 2021 02:59:52 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Sat, 06 Mar 2021 02:59:52 GMT
ENV PHP_VERSION=7.4.16
# Sat, 06 Mar 2021 02:59:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Sat, 06 Mar 2021 02:59:53 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Sat, 06 Mar 2021 03:00:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 06 Mar 2021 03:00:19 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Mar 2021 03:08:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Mar 2021 03:08:56 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Sat, 06 Mar 2021 03:08:58 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Mar 2021 03:08:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Mar 2021 03:08:58 GMT
CMD ["php" "-a"]
# Sat, 06 Mar 2021 08:16:03 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 06 Mar 2021 08:16:03 GMT
STOPSIGNAL SIGINT
# Sat, 06 Mar 2021 08:16:04 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 06 Mar 2021 08:16:04 GMT
WORKDIR /var/www/html
# Sat, 06 Mar 2021 08:16:34 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 06 Mar 2021 08:16:34 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Sat, 06 Mar 2021 08:16:34 GMT
ENV ADMINER_VERSION=4.8.0
# Sat, 06 Mar 2021 08:16:34 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Sat, 06 Mar 2021 08:16:35 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Sat, 06 Mar 2021 08:16:37 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 06 Mar 2021 08:16:38 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 06 Mar 2021 08:16:38 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 06 Mar 2021 08:16:38 GMT
USER adminer
# Sat, 06 Mar 2021 08:16:38 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 06 Mar 2021 08:16:38 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d779edf81d3549de0c570804cffa8279f4a980d3fed1292285070f24a1b00f`  
		Last Modified: Sat, 06 Mar 2021 05:47:24 GMT  
		Size: 1.8 MB (1793700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce9d30537e4bf7ab9ad24ea334671e794e0830680c386cf4b36dbba54dd40c5`  
		Last Modified: Sat, 06 Mar 2021 05:47:23 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f119038c35efd6cc0b1a27c432b2fc338da413650c224359556d95e0bf8214`  
		Last Modified: Sat, 06 Mar 2021 05:47:23 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:125aeed6c18a6c28cf608d3c3cd80094c61ed4f9023855f9c3ac4993f1542907`  
		Last Modified: Sat, 06 Mar 2021 05:53:56 GMT  
		Size: 10.4 MB (10354073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05563330040dc337869b22ab8c267fc06fa14139a5f270679e69ba3a718896b5`  
		Last Modified: Sat, 06 Mar 2021 05:53:53 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567f9a9d037948e123fbbec64dfb76f7cca9d30cd3e5526abc597b65fd39656b`  
		Last Modified: Sat, 06 Mar 2021 05:54:00 GMT  
		Size: 14.6 MB (14630287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28b3a57348334ee91df9b04ec97e570fcff52d0a9fa3e3ec3247823d80a437d`  
		Last Modified: Sat, 06 Mar 2021 05:53:53 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0621d49125fecbf6f64ac583fbf7c76034bc51eed48c69516922c398d93a6c`  
		Last Modified: Sat, 06 Mar 2021 05:53:54 GMT  
		Size: 17.5 KB (17501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c703587ef05b977c127d751c1c78fa472b5ddb67b5ac217ac20ea90cd8855c`  
		Last Modified: Sat, 06 Mar 2021 08:17:58 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e848e2757b70b020801c677c59e10e8709f14f3f76f32d2b1be5f95679f4f6c5`  
		Last Modified: Sat, 06 Mar 2021 08:17:54 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f2ac401974d5ea19f7f375960da2a7a6c77f23dab4135c4bd95c4dc64f9d02`  
		Last Modified: Sat, 06 Mar 2021 08:17:55 GMT  
		Size: 4.0 MB (4010207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cb78f666be732b2b10b604df1cb578ad8ccca1445c29fd5bab4ba346f29247`  
		Last Modified: Sat, 06 Mar 2021 08:17:54 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980181a00a928280cf2288da2498d06c9203508ce40aa0aed05b1a2be94ae1ce`  
		Last Modified: Sat, 06 Mar 2021 08:17:54 GMT  
		Size: 582.8 KB (582807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0865a1f7fbcf5062e0b5b2fc87b6ea55d2e4c094297f6139e110bbc7a1c9794`  
		Last Modified: Sat, 06 Mar 2021 08:17:54 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; ppc64le

```console
$ docker pull adminer@sha256:f8ed36e984e53d541d8f690681208acc65c3b6e90ac3830c51e821eeb7b24951
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (34960311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0819898f5e08afcbb1041ea1c325869490d997fe19fcaa3e93b720312272db4`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 21:17:29 GMT
ADD file:28f4377c61c0f8eb43a6b36e6a24ef5893f51d405d25b62e364988223537ae0b in / 
# Wed, 17 Feb 2021 21:17:37 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 00:23:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Feb 2021 00:24:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 18 Feb 2021 00:24:44 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 18 Feb 2021 00:24:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Feb 2021 00:25:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 18 Feb 2021 00:25:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:25:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:25:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Feb 2021 00:40:47 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 01:05:36 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 01:05:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 01:05:52 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 01:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 01:06:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:11:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 01:11:19 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:11:29 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 01:11:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 01:11:46 GMT
CMD ["php" "-a"]
# Fri, 05 Mar 2021 02:08:50 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 02:09:05 GMT
STOPSIGNAL SIGINT
# Fri, 05 Mar 2021 02:09:23 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 02:09:30 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 02:10:27 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 02:10:29 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 02:10:33 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 02:10:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 02:10:56 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 02:11:23 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 02:11:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 02:11:34 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 02:11:42 GMT
USER adminer
# Fri, 05 Mar 2021 02:11:57 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 05 Mar 2021 02:12:05 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:cb672e0375a8f9bb3d33049ceb372ffa49b959bfc84fe6f72bfb97b682a608c8`  
		Last Modified: Wed, 17 Feb 2021 21:18:10 GMT  
		Size: 2.8 MB (2813081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebfde0ed2b25fdf7a28b46b01e73c7891af78bd260ce9c5f46f33a0fd4bba5a`  
		Last Modified: Thu, 18 Feb 2021 01:25:11 GMT  
		Size: 1.7 MB (1741666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c587bda2cf37683b8f80371450083e1533df270a51cbe196c845e7ab52f8943`  
		Last Modified: Thu, 18 Feb 2021 01:25:09 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2faee0918d4167a0323dba5b4244442a3d6cd88d5eacd4a560b72f056274a4`  
		Last Modified: Thu, 18 Feb 2021 01:25:10 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791bb958f337b6cf4b2ea90cf5ac9fcb4612738a152ac4a09a69335da096e59b`  
		Last Modified: Fri, 05 Mar 2021 01:49:57 GMT  
		Size: 10.4 MB (10354080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86e997f6d103c9c5f8aa990ba021777b0a7b8073db6c1aa66166630ac5fb896`  
		Last Modified: Fri, 05 Mar 2021 01:49:55 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97cf656907ab8d840227fdc0e36c17cac097192e975dbb19d8fbc99f3ddde66`  
		Last Modified: Fri, 05 Mar 2021 01:49:59 GMT  
		Size: 15.5 MB (15524632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953ac22358c5b3a72272c4db94f387dafe749dccc315fe715fd54646a7e67fa1`  
		Last Modified: Fri, 05 Mar 2021 01:49:55 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5274e31720b346823b92235766eace03c5b3ca24d9af8910eb3c00a29bc1f48e`  
		Last Modified: Fri, 05 Mar 2021 01:49:56 GMT  
		Size: 17.6 KB (17566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae1914ed9afaacdd2822f6ce3b21c1ba2cfc67fb0a0fc37105941301dde3979`  
		Last Modified: Fri, 05 Mar 2021 02:15:07 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097959a8b93e17b2458e2add93679e6bc07debf1b8ed2e8e39ebdb005d0de353`  
		Last Modified: Fri, 05 Mar 2021 02:15:03 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08378c640496a604d70139ba5075c5cd2fe90d0786621bc4396e7cee75634053`  
		Last Modified: Fri, 05 Mar 2021 02:15:05 GMT  
		Size: 3.9 MB (3918494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4eee7fd3e560e705de2352e9453419f436960844b5ddfda9986cedb09cd6bde`  
		Last Modified: Fri, 05 Mar 2021 02:15:03 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435b254436c62649064c5af03dfecbb978ff36ac4740efbc8a476f538850455e`  
		Last Modified: Fri, 05 Mar 2021 02:15:03 GMT  
		Size: 582.8 KB (582810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38c8209ca8c0d5b2b2b2baae2f460323d08fc90ce007eabd250244bc371189b`  
		Last Modified: Fri, 05 Mar 2021 02:15:05 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; s390x

```console
$ docker pull adminer@sha256:9035a1407febca18c25bbc2820e9ac6a09281165f387df8d135066d3bcad2d14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32764749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ff9987904c7594d2e9098e19fcc387f22c02e45e942703bd6f07ac77ebbe58`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 00:40:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Feb 2021 00:40:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 18 Feb 2021 00:40:31 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 18 Feb 2021 00:40:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Feb 2021 00:40:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 18 Feb 2021 00:40:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:40:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:40:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Feb 2021 00:51:38 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:17:53 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:17:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:17:54 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:17:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:17:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:21:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:21:14 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:21:14 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:21:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:21:15 GMT
CMD ["php" "-a"]
# Fri, 05 Mar 2021 01:35:01 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 01:35:02 GMT
STOPSIGNAL SIGINT
# Fri, 05 Mar 2021 01:35:03 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 01:35:03 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 01:35:28 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 01:35:28 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 01:35:28 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 01:35:29 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 01:35:29 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 01:35:30 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 01:35:30 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:35:31 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 01:35:31 GMT
USER adminer
# Fri, 05 Mar 2021 01:35:31 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 05 Mar 2021 01:35:31 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2eaf748a32e76be0f1aa6246cb11c8aa5022aa834df364bb87f581198e6376`  
		Last Modified: Thu, 18 Feb 2021 01:26:48 GMT  
		Size: 1.8 MB (1756400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5716be54c61b8e2a38b4d6a0cbece88801726747842f6bd1a50aaf4e8442013f`  
		Last Modified: Thu, 18 Feb 2021 01:26:48 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6aa66a8dad4ec1443c27324fc452b05c4299dbffefcebee55700880033b3ff7`  
		Last Modified: Thu, 18 Feb 2021 01:26:47 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8b7b210cf7a350eb620b3574b19324168c8c4833e0cfe3d634398782f48175`  
		Last Modified: Fri, 05 Mar 2021 00:51:36 GMT  
		Size: 10.4 MB (10354085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a066cfbe30cd983f5ffef2df9d50618ade23fe99302b69e012774b2269585d1`  
		Last Modified: Fri, 05 Mar 2021 00:51:35 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9401205bc3eb7297f85c414b790172be23d1c4ab061aee72eaeb28b69132c073`  
		Last Modified: Fri, 05 Mar 2021 00:51:38 GMT  
		Size: 13.9 MB (13860060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afee2a631a7b79b3c487a3ef4500ea44fa978bd6464fe317d1a65d4b104f7309`  
		Last Modified: Fri, 05 Mar 2021 00:51:35 GMT  
		Size: 2.3 KB (2261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0499fd075a9fd055ca563a90fb4b2aaac9056a65b191d7db41c37188db098cf1`  
		Last Modified: Fri, 05 Mar 2021 00:51:35 GMT  
		Size: 17.6 KB (17566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b53123be7d4a2e60f8c580951db7f413a3fddabf032b97cc4e1715defe06aa`  
		Last Modified: Fri, 05 Mar 2021 01:36:37 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aab483619f81007684651c4b32aae7e47300c44374d5a2e165bfee97c9a5ed8`  
		Last Modified: Fri, 05 Mar 2021 01:36:35 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21994edf819ad8eed5eea7af018652abc984e3d7f67f6dd34ead1779f80b961c`  
		Last Modified: Fri, 05 Mar 2021 01:36:35 GMT  
		Size: 3.6 MB (3583473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39598f68be044d39764fd4f2c72cccb6ff39c29081b324413fb9af80f22c6b6`  
		Last Modified: Fri, 05 Mar 2021 01:36:35 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6988f4418691c53ad239170a2ec56313d0be5ebf6636151c2ab31dee05fd76`  
		Last Modified: Fri, 05 Mar 2021 01:36:35 GMT  
		Size: 582.8 KB (582811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f94af1afe9ebb57211f0f17af8d7edc0ccf29b7fe0f188bae543435432d960`  
		Last Modified: Fri, 05 Mar 2021 01:36:35 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:standalone`

```console
$ docker pull adminer@sha256:1ee6ed00d1169a14a1030a1d44a5ab1724392c115d296d98f0a0e8700628deeb
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

### `adminer:standalone` - linux; amd64

```console
$ docker pull adminer@sha256:d7cbbb92e43f7d55027a58bd115d9425548325f3754cb705b03368243b3930d3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.6 MB (33625851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d5528d5e4b1e1e879cf6d3b49b09245873a231a6054521f40a538633893e3d`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 03:21:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 06 Mar 2021 03:21:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 06 Mar 2021 03:21:31 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 06 Mar 2021 03:21:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 06 Mar 2021 03:21:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 06 Mar 2021 03:21:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 03:21:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 03:21:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 06 Mar 2021 04:18:25 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Sat, 06 Mar 2021 04:18:25 GMT
ENV PHP_VERSION=7.4.16
# Sat, 06 Mar 2021 04:18:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Sat, 06 Mar 2021 04:18:26 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Sat, 06 Mar 2021 04:18:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 06 Mar 2021 04:18:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Mar 2021 04:25:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Mar 2021 04:25:46 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Sat, 06 Mar 2021 04:25:48 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Mar 2021 04:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Mar 2021 04:25:49 GMT
CMD ["php" "-a"]
# Sat, 06 Mar 2021 08:51:16 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 06 Mar 2021 08:51:16 GMT
STOPSIGNAL SIGINT
# Sat, 06 Mar 2021 08:51:17 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 06 Mar 2021 08:51:17 GMT
WORKDIR /var/www/html
# Sat, 06 Mar 2021 08:51:43 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 06 Mar 2021 08:51:43 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Sat, 06 Mar 2021 08:51:43 GMT
ENV ADMINER_VERSION=4.8.0
# Sat, 06 Mar 2021 08:51:44 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Sat, 06 Mar 2021 08:51:44 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Sat, 06 Mar 2021 08:51:46 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 06 Mar 2021 08:51:46 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 06 Mar 2021 08:51:46 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 06 Mar 2021 08:51:46 GMT
USER adminer
# Sat, 06 Mar 2021 08:51:46 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 06 Mar 2021 08:51:47 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743181516422399af3888ad5df44c6f711f992b2f86288db9e191ae13de99fa0`  
		Last Modified: Sat, 06 Mar 2021 06:31:08 GMT  
		Size: 1.7 MB (1694870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c307b60e377a3903f74fd9cde3ad69f754071faac36f81ca74e1aa9eabe4851`  
		Last Modified: Sat, 06 Mar 2021 06:31:08 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d5b43308915ce3198dec1c19aa88719afacff02c85660a952982856a0bcc9c`  
		Last Modified: Sat, 06 Mar 2021 06:31:08 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4848a1e010e4e0cda8de291fa6ed2f3efecf20d7343a69cec21878885828d2d`  
		Last Modified: Sat, 06 Mar 2021 06:35:54 GMT  
		Size: 10.4 MB (10354097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8e88ab7b4e15d3c4d8d099845669643447a702d27188138ed20f8c14879cde`  
		Last Modified: Sat, 06 Mar 2021 06:35:54 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c6688ec4022c9042fad0bff0a5aaa03cd55628577fe71a419761ca5478392c`  
		Last Modified: Sat, 06 Mar 2021 06:35:56 GMT  
		Size: 14.3 MB (14253596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b401e642cd6c785a0ede5899c8a1fb93770d6eaf04a0a5faeb0183ad5c21f3`  
		Last Modified: Sat, 06 Mar 2021 06:35:54 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4aa45ba156c9e4af51f7b2a5eec317be47eca6ba8e9bb8fc368488ea41c11c`  
		Last Modified: Sat, 06 Mar 2021 06:35:54 GMT  
		Size: 17.5 KB (17518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b686977c50b0410c0084a21bef42aae47c53441ee7defe7b25bcad585a19999`  
		Last Modified: Sat, 06 Mar 2021 08:52:42 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf15bf71cdf8a60508b2773274a23124c80de6ad9611b97bd532869bdce6929`  
		Last Modified: Sat, 06 Mar 2021 08:52:38 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7855e8a455940ec1b6c2e7a9d42e3a94e92b3f7dd253bfdefd2ef4f0b272a242`  
		Last Modified: Sat, 06 Mar 2021 08:52:40 GMT  
		Size: 3.9 MB (3903349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff73275236b8945efe2dadf9b67d73cc5c24fb699f0e3265cbdb3445bdabcba`  
		Last Modified: Sat, 06 Mar 2021 08:52:38 GMT  
		Size: 1.5 KB (1471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64cfef0d91dbc6948021e94ae4407132c018d08d4446215342ad7e0447e33383`  
		Last Modified: Sat, 06 Mar 2021 08:52:39 GMT  
		Size: 582.8 KB (582798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7097b3e809e2d58f970ecec3070fa3db82d914e74c47172eb2c2800e051290`  
		Last Modified: Sat, 06 Mar 2021 08:52:39 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; arm variant v6

```console
$ docker pull adminer@sha256:67ecf13bed27733de831bad0889ec483ede8530402c3c46011d2334e4a991c25
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32352290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4b093e53cd99d8904355485561c5dd006e3077e79bf2eaba849078b7c8ff3b`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:17:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Feb 2021 22:17:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 17 Feb 2021 22:17:15 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Feb 2021 22:17:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Feb 2021 22:17:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Feb 2021 22:17:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:17:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:17:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Feb 2021 22:24:49 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:22:42 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:22:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:22:48 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:22:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:23:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:26:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:26:24 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:26:28 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:26:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:26:30 GMT
CMD ["php" "-a"]
# Fri, 05 Mar 2021 01:28:12 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 01:28:12 GMT
STOPSIGNAL SIGINT
# Fri, 05 Mar 2021 01:28:15 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 01:28:15 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 01:29:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 01:29:05 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 01:29:06 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 01:29:07 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 01:29:08 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 01:29:11 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 01:29:11 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:29:12 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 01:29:13 GMT
USER adminer
# Fri, 05 Mar 2021 01:29:13 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 05 Mar 2021 01:29:14 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a33e390360f607fe5a7fe0a0203b7347693b0d8cab270352594a3700e1a1d0`  
		Last Modified: Wed, 17 Feb 2021 22:57:10 GMT  
		Size: 1.7 MB (1684729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d1bbb88bd210deaf33702df9d6fa7f35e72f23dfbb55196147ab537320e9f3`  
		Last Modified: Wed, 17 Feb 2021 22:57:09 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b99fbc527c373db47c36282e5bbd82010870902db2af45982bbb8d700375a32`  
		Last Modified: Wed, 17 Feb 2021 22:57:09 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37a52f8d6a0669099c893e2b3e9ce5d8862eed5489a15f8dafd39f664233b7c`  
		Last Modified: Fri, 05 Mar 2021 00:53:01 GMT  
		Size: 10.4 MB (10354085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e31438bda764d2d788352c3dbdc563f97c840ce2736c283190e590e11a4641`  
		Last Modified: Fri, 05 Mar 2021 00:52:59 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615508ce208f1bfacc67745161a522490ffde3254a7e5b88e2a75704a178b65d`  
		Last Modified: Fri, 05 Mar 2021 00:53:05 GMT  
		Size: 13.5 MB (13479609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49bab722652cd2c45df88dee34d635b0c4824fd1885e9cdb6fa1ad1c707b24d`  
		Last Modified: Fri, 05 Mar 2021 00:52:59 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b5e7fa68211b0722b528ee1f7b5f413c32b3581eec56fc37d056cf1e44d45f`  
		Last Modified: Fri, 05 Mar 2021 00:52:59 GMT  
		Size: 17.6 KB (17574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a863fe1948ed188002b2c53e19c1c4f06aa611913e9aee2e6d37a4b38892fa27`  
		Last Modified: Fri, 05 Mar 2021 01:31:18 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e5d7f207dfb0131e75fb5675de4013a21ec2a9965b6a5f2974a09de577b376`  
		Last Modified: Fri, 05 Mar 2021 01:31:15 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613aba5afd5742d6a2f8c093d4d9e2e3eef9f92d01853c139b3f7690a577fd1d`  
		Last Modified: Fri, 05 Mar 2021 01:31:16 GMT  
		Size: 3.6 MB (3603470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ea9f569f958143bd38a220ee729c6ef6f85c122fe3f42b2a761b57e39df3e9`  
		Last Modified: Fri, 05 Mar 2021 01:31:15 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e6944e336be980c37b3af333b01dab0f1b3db12af184e3cc0ed1d4a326a6ab`  
		Last Modified: Fri, 05 Mar 2021 01:31:15 GMT  
		Size: 582.8 KB (582808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4644911e6f4e52234e1b7b359c25f4998c5be8fe108e2f0b54e5cfd721d2d9`  
		Last Modified: Fri, 05 Mar 2021 01:31:15 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:3c5fe027a505612b8c787c41923bc81f01eba12776b7827fb8de3b48fadd12ff
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31126385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7625601231cbbafd93c468bb5506f91c320be7c6640088ec3203f7b61bcae845`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:56:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Feb 2021 22:57:00 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 17 Feb 2021 22:57:04 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Feb 2021 22:57:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Feb 2021 22:57:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Feb 2021 22:57:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:57:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:57:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Feb 2021 23:07:25 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:51:51 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:51:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:51:52 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:51:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:51:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:54:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:54:56 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:55:00 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:55:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:55:01 GMT
CMD ["php" "-a"]
# Fri, 05 Mar 2021 03:16:34 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 03:16:35 GMT
STOPSIGNAL SIGINT
# Fri, 05 Mar 2021 03:16:37 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 03:16:37 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 03:17:32 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 03:17:34 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 03:17:35 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 03:17:36 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 03:17:36 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 03:17:39 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 03:17:40 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 03:17:41 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 03:17:42 GMT
USER adminer
# Fri, 05 Mar 2021 03:17:42 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 05 Mar 2021 03:17:43 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf491575714634902d01e3e48f3b92702cb2e4c42056aa5421058d2a2cbfd9f6`  
		Last Modified: Wed, 17 Feb 2021 23:33:58 GMT  
		Size: 1.6 MB (1555125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8ae33f1196d3a62a9383b30d3fd81dd4be1bcf1a99a3d928f585b0d85c5408`  
		Last Modified: Wed, 17 Feb 2021 23:33:58 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16bd16ac2dc3896b7ddf5e8e50bafcc3990d8313dc26634a51beafc97cc6374`  
		Last Modified: Wed, 17 Feb 2021 23:33:58 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224ef988837049de958e2e9476510f82fe8e42270706a0671a5a463f6ae97dc2`  
		Last Modified: Fri, 05 Mar 2021 01:20:19 GMT  
		Size: 10.4 MB (10354091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9e75985cf89dec0ed12206b36f371ffbda22ccf6cdbccf5d19345e62db2c14`  
		Last Modified: Fri, 05 Mar 2021 01:20:16 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3067a7094a3949ddb39a5787e92b263164d2eb287f0d508c0497dc270667f7a2`  
		Last Modified: Fri, 05 Mar 2021 01:20:19 GMT  
		Size: 12.6 MB (12608573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e967fccc5675136a3112da05f19624319efe2274faf250ffc942f8df1727990b`  
		Last Modified: Fri, 05 Mar 2021 01:20:15 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bee2c4ad784aa0aa254a050c45062e42eae3e6414649f1e7372db7fe0845817`  
		Last Modified: Fri, 05 Mar 2021 01:20:15 GMT  
		Size: 17.6 KB (17556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd957d7c1659b87bbacdaaa44de1493cd86ce1058104890fa7f886c244af7e2`  
		Last Modified: Fri, 05 Mar 2021 03:19:23 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a9b53808941e232e796f0fce8be1b1a2bdab2ab0d1227f671cdc2e6d8acecd`  
		Last Modified: Fri, 05 Mar 2021 03:19:21 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b983fd5f2f41ac862e588d3c7cb994ae11a6d4dfd1273298d35ff8fcdc87e72`  
		Last Modified: Fri, 05 Mar 2021 03:19:21 GMT  
		Size: 3.6 MB (3576366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957ff1dc0df9c3cd0fa022e0ae444a04b77d5b488a38dcba9673c2f3dfb07f8d`  
		Last Modified: Fri, 05 Mar 2021 03:19:21 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d418e42a87cf9ea044ec23d04a0b56e7f7b51dbab5639eb0e1c16248b88575`  
		Last Modified: Fri, 05 Mar 2021 03:19:21 GMT  
		Size: 582.8 KB (582806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1688bcdb1a112479d4950eae42069fa29ff4e81e587b2387362b4a6cc0fbe2`  
		Last Modified: Fri, 05 Mar 2021 03:19:21 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:7991be9e1a1ee3f2c5d374475d3746026dd7ca64a60167a65551567d7cfccf43
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33506242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11682bbe518b1faa63b82b75d246e7c35612d6d253da8f2011c0539c5b07f5cc`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 23:42:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Feb 2021 23:42:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 17 Feb 2021 23:42:38 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Feb 2021 23:42:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Feb 2021 23:42:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Feb 2021 23:42:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 23:42:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 23:42:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Feb 2021 23:53:01 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:37:35 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:37:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:37:38 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:37:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:37:47 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:42:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:42:39 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:42:44 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:42:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:42:47 GMT
CMD ["php" "-a"]
# Fri, 05 Mar 2021 02:04:43 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 02:04:44 GMT
STOPSIGNAL SIGINT
# Fri, 05 Mar 2021 02:04:48 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 02:04:50 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 02:05:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 02:05:56 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 02:05:57 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 02:05:57 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 02:05:58 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 02:06:02 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 02:06:03 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 02:06:04 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 02:06:05 GMT
USER adminer
# Fri, 05 Mar 2021 02:06:06 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 05 Mar 2021 02:06:06 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4b642bcaaef409203aaedc803835562ee86d3ea457bf4ccdd22e5d7b2367f1`  
		Last Modified: Thu, 18 Feb 2021 00:23:35 GMT  
		Size: 1.7 MB (1694455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ea39643e14bb66b107bb23b02b8c7a193ed89d38f4ae52b1decbe763fb0db9`  
		Last Modified: Thu, 18 Feb 2021 00:23:34 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3455119714d8ce066305d3b121e103a3cf690db26bb556906ba67e7a7c1f559`  
		Last Modified: Thu, 18 Feb 2021 00:23:34 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a68a1ddf490519ddbcd4f75589909c8d4703a6b902bae2a7319905984b7547`  
		Last Modified: Fri, 05 Mar 2021 01:13:32 GMT  
		Size: 10.4 MB (10354115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1754592c0391f5b7b27cf3c7110b1e2a917ebb769b0ceaf9bfdfd0181cc6cb`  
		Last Modified: Fri, 05 Mar 2021 01:13:30 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a402e34d4d52011f5ecf29a826d7fd94dc474fdf156b70d506d3deaeb2a4d3b`  
		Last Modified: Fri, 05 Mar 2021 01:13:34 GMT  
		Size: 14.3 MB (14263146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1702d0137849d4baf63d0536ee9f8391c72c295a46613ed43c270f3cc81a90`  
		Last Modified: Fri, 05 Mar 2021 01:13:31 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ebe5152320826ffaea66119f3e759ce05ed98bb09a201643ee6674cbd9685e`  
		Last Modified: Fri, 05 Mar 2021 01:13:31 GMT  
		Size: 17.6 KB (17574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a42655d4ea3811b755ccede7be6704d6e30a4e912c6ec284807f25e1874c11`  
		Last Modified: Fri, 05 Mar 2021 02:08:13 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36983a97af0e64abf039823af9b57936cc5add643fab48f1d64ca7fbeb076a02`  
		Last Modified: Fri, 05 Mar 2021 02:08:11 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23c53be365e785ad30481daf9c58f08857ca80fc5fc681e12655557a14f7093`  
		Last Modified: Fri, 05 Mar 2021 02:08:12 GMT  
		Size: 3.9 MB (3874584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d698ddfcb363647524ac96d6fe45138e9aa228c8662ec68d2c877a5862a6257`  
		Last Modified: Fri, 05 Mar 2021 02:08:11 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e7497f33585536dba243eedb8aea95c51b88677f674845065a15d776a0e7c78`  
		Last Modified: Fri, 05 Mar 2021 02:08:12 GMT  
		Size: 582.8 KB (582809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041eab10d184403fbf0b2a94255c47e5618bc99fd708586209ad66d02a41c86b`  
		Last Modified: Fri, 05 Mar 2021 02:08:11 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; 386

```console
$ docker pull adminer@sha256:3c12e8f857cf7b920500273d347a57b13be7f75bc361cd49631704781e87dafe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34214715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8de5231523b1be5d66db42c66ace28ceef73e37457dc22956bd36744ea35592f`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 02:13:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 06 Mar 2021 02:13:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 06 Mar 2021 02:13:32 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 06 Mar 2021 02:13:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 06 Mar 2021 02:13:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 06 Mar 2021 02:13:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 02:13:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 02:13:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 06 Mar 2021 02:59:52 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Sat, 06 Mar 2021 02:59:52 GMT
ENV PHP_VERSION=7.4.16
# Sat, 06 Mar 2021 02:59:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Sat, 06 Mar 2021 02:59:53 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Sat, 06 Mar 2021 03:00:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 06 Mar 2021 03:00:19 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Mar 2021 03:08:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Mar 2021 03:08:56 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Sat, 06 Mar 2021 03:08:58 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Mar 2021 03:08:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Mar 2021 03:08:58 GMT
CMD ["php" "-a"]
# Sat, 06 Mar 2021 08:16:03 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 06 Mar 2021 08:16:03 GMT
STOPSIGNAL SIGINT
# Sat, 06 Mar 2021 08:16:04 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 06 Mar 2021 08:16:04 GMT
WORKDIR /var/www/html
# Sat, 06 Mar 2021 08:16:34 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 06 Mar 2021 08:16:34 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Sat, 06 Mar 2021 08:16:34 GMT
ENV ADMINER_VERSION=4.8.0
# Sat, 06 Mar 2021 08:16:34 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Sat, 06 Mar 2021 08:16:35 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Sat, 06 Mar 2021 08:16:37 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 06 Mar 2021 08:16:38 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 06 Mar 2021 08:16:38 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 06 Mar 2021 08:16:38 GMT
USER adminer
# Sat, 06 Mar 2021 08:16:38 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 06 Mar 2021 08:16:38 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d779edf81d3549de0c570804cffa8279f4a980d3fed1292285070f24a1b00f`  
		Last Modified: Sat, 06 Mar 2021 05:47:24 GMT  
		Size: 1.8 MB (1793700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce9d30537e4bf7ab9ad24ea334671e794e0830680c386cf4b36dbba54dd40c5`  
		Last Modified: Sat, 06 Mar 2021 05:47:23 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f119038c35efd6cc0b1a27c432b2fc338da413650c224359556d95e0bf8214`  
		Last Modified: Sat, 06 Mar 2021 05:47:23 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:125aeed6c18a6c28cf608d3c3cd80094c61ed4f9023855f9c3ac4993f1542907`  
		Last Modified: Sat, 06 Mar 2021 05:53:56 GMT  
		Size: 10.4 MB (10354073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05563330040dc337869b22ab8c267fc06fa14139a5f270679e69ba3a718896b5`  
		Last Modified: Sat, 06 Mar 2021 05:53:53 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567f9a9d037948e123fbbec64dfb76f7cca9d30cd3e5526abc597b65fd39656b`  
		Last Modified: Sat, 06 Mar 2021 05:54:00 GMT  
		Size: 14.6 MB (14630287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28b3a57348334ee91df9b04ec97e570fcff52d0a9fa3e3ec3247823d80a437d`  
		Last Modified: Sat, 06 Mar 2021 05:53:53 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0621d49125fecbf6f64ac583fbf7c76034bc51eed48c69516922c398d93a6c`  
		Last Modified: Sat, 06 Mar 2021 05:53:54 GMT  
		Size: 17.5 KB (17501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c703587ef05b977c127d751c1c78fa472b5ddb67b5ac217ac20ea90cd8855c`  
		Last Modified: Sat, 06 Mar 2021 08:17:58 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e848e2757b70b020801c677c59e10e8709f14f3f76f32d2b1be5f95679f4f6c5`  
		Last Modified: Sat, 06 Mar 2021 08:17:54 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f2ac401974d5ea19f7f375960da2a7a6c77f23dab4135c4bd95c4dc64f9d02`  
		Last Modified: Sat, 06 Mar 2021 08:17:55 GMT  
		Size: 4.0 MB (4010207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cb78f666be732b2b10b604df1cb578ad8ccca1445c29fd5bab4ba346f29247`  
		Last Modified: Sat, 06 Mar 2021 08:17:54 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980181a00a928280cf2288da2498d06c9203508ce40aa0aed05b1a2be94ae1ce`  
		Last Modified: Sat, 06 Mar 2021 08:17:54 GMT  
		Size: 582.8 KB (582807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0865a1f7fbcf5062e0b5b2fc87b6ea55d2e4c094297f6139e110bbc7a1c9794`  
		Last Modified: Sat, 06 Mar 2021 08:17:54 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:f8ed36e984e53d541d8f690681208acc65c3b6e90ac3830c51e821eeb7b24951
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (34960311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0819898f5e08afcbb1041ea1c325869490d997fe19fcaa3e93b720312272db4`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 21:17:29 GMT
ADD file:28f4377c61c0f8eb43a6b36e6a24ef5893f51d405d25b62e364988223537ae0b in / 
# Wed, 17 Feb 2021 21:17:37 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 00:23:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Feb 2021 00:24:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 18 Feb 2021 00:24:44 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 18 Feb 2021 00:24:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Feb 2021 00:25:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 18 Feb 2021 00:25:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:25:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:25:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Feb 2021 00:40:47 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 01:05:36 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 01:05:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 01:05:52 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 01:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 01:06:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:11:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 01:11:19 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:11:29 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 01:11:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 01:11:46 GMT
CMD ["php" "-a"]
# Fri, 05 Mar 2021 02:08:50 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 02:09:05 GMT
STOPSIGNAL SIGINT
# Fri, 05 Mar 2021 02:09:23 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 02:09:30 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 02:10:27 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 02:10:29 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 02:10:33 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 02:10:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 02:10:56 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 02:11:23 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 02:11:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 02:11:34 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 02:11:42 GMT
USER adminer
# Fri, 05 Mar 2021 02:11:57 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 05 Mar 2021 02:12:05 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:cb672e0375a8f9bb3d33049ceb372ffa49b959bfc84fe6f72bfb97b682a608c8`  
		Last Modified: Wed, 17 Feb 2021 21:18:10 GMT  
		Size: 2.8 MB (2813081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebfde0ed2b25fdf7a28b46b01e73c7891af78bd260ce9c5f46f33a0fd4bba5a`  
		Last Modified: Thu, 18 Feb 2021 01:25:11 GMT  
		Size: 1.7 MB (1741666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c587bda2cf37683b8f80371450083e1533df270a51cbe196c845e7ab52f8943`  
		Last Modified: Thu, 18 Feb 2021 01:25:09 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2faee0918d4167a0323dba5b4244442a3d6cd88d5eacd4a560b72f056274a4`  
		Last Modified: Thu, 18 Feb 2021 01:25:10 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791bb958f337b6cf4b2ea90cf5ac9fcb4612738a152ac4a09a69335da096e59b`  
		Last Modified: Fri, 05 Mar 2021 01:49:57 GMT  
		Size: 10.4 MB (10354080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86e997f6d103c9c5f8aa990ba021777b0a7b8073db6c1aa66166630ac5fb896`  
		Last Modified: Fri, 05 Mar 2021 01:49:55 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97cf656907ab8d840227fdc0e36c17cac097192e975dbb19d8fbc99f3ddde66`  
		Last Modified: Fri, 05 Mar 2021 01:49:59 GMT  
		Size: 15.5 MB (15524632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953ac22358c5b3a72272c4db94f387dafe749dccc315fe715fd54646a7e67fa1`  
		Last Modified: Fri, 05 Mar 2021 01:49:55 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5274e31720b346823b92235766eace03c5b3ca24d9af8910eb3c00a29bc1f48e`  
		Last Modified: Fri, 05 Mar 2021 01:49:56 GMT  
		Size: 17.6 KB (17566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae1914ed9afaacdd2822f6ce3b21c1ba2cfc67fb0a0fc37105941301dde3979`  
		Last Modified: Fri, 05 Mar 2021 02:15:07 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097959a8b93e17b2458e2add93679e6bc07debf1b8ed2e8e39ebdb005d0de353`  
		Last Modified: Fri, 05 Mar 2021 02:15:03 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08378c640496a604d70139ba5075c5cd2fe90d0786621bc4396e7cee75634053`  
		Last Modified: Fri, 05 Mar 2021 02:15:05 GMT  
		Size: 3.9 MB (3918494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4eee7fd3e560e705de2352e9453419f436960844b5ddfda9986cedb09cd6bde`  
		Last Modified: Fri, 05 Mar 2021 02:15:03 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435b254436c62649064c5af03dfecbb978ff36ac4740efbc8a476f538850455e`  
		Last Modified: Fri, 05 Mar 2021 02:15:03 GMT  
		Size: 582.8 KB (582810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38c8209ca8c0d5b2b2b2baae2f460323d08fc90ce007eabd250244bc371189b`  
		Last Modified: Fri, 05 Mar 2021 02:15:05 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; s390x

```console
$ docker pull adminer@sha256:9035a1407febca18c25bbc2820e9ac6a09281165f387df8d135066d3bcad2d14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32764749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ff9987904c7594d2e9098e19fcc387f22c02e45e942703bd6f07ac77ebbe58`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 00:40:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Feb 2021 00:40:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 18 Feb 2021 00:40:31 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 18 Feb 2021 00:40:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Feb 2021 00:40:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 18 Feb 2021 00:40:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:40:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:40:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Feb 2021 00:51:38 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 05 Mar 2021 00:17:53 GMT
ENV PHP_VERSION=7.4.16
# Fri, 05 Mar 2021 00:17:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Fri, 05 Mar 2021 00:17:54 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Fri, 05 Mar 2021 00:17:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:17:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:21:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:21:14 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:21:14 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:21:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:21:15 GMT
CMD ["php" "-a"]
# Fri, 05 Mar 2021 01:35:01 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 05 Mar 2021 01:35:02 GMT
STOPSIGNAL SIGINT
# Fri, 05 Mar 2021 01:35:03 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 05 Mar 2021 01:35:03 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 01:35:28 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 05 Mar 2021 01:35:28 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 05 Mar 2021 01:35:28 GMT
ENV ADMINER_VERSION=4.8.0
# Fri, 05 Mar 2021 01:35:29 GMT
ENV ADMINER_DOWNLOAD_SHA256=e274268e0e0f2a6b8040c000a969889062904ae7a5ccbaf013dc890e12e32eaa
# Fri, 05 Mar 2021 01:35:29 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=55b52851faa5661667edb003b00cf520ebeb1e41cfcea4a7fc028ed0f55ff557
# Fri, 05 Mar 2021 01:35:30 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 05 Mar 2021 01:35:30 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:35:31 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 05 Mar 2021 01:35:31 GMT
USER adminer
# Fri, 05 Mar 2021 01:35:31 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 05 Mar 2021 01:35:31 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2eaf748a32e76be0f1aa6246cb11c8aa5022aa834df364bb87f581198e6376`  
		Last Modified: Thu, 18 Feb 2021 01:26:48 GMT  
		Size: 1.8 MB (1756400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5716be54c61b8e2a38b4d6a0cbece88801726747842f6bd1a50aaf4e8442013f`  
		Last Modified: Thu, 18 Feb 2021 01:26:48 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6aa66a8dad4ec1443c27324fc452b05c4299dbffefcebee55700880033b3ff7`  
		Last Modified: Thu, 18 Feb 2021 01:26:47 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8b7b210cf7a350eb620b3574b19324168c8c4833e0cfe3d634398782f48175`  
		Last Modified: Fri, 05 Mar 2021 00:51:36 GMT  
		Size: 10.4 MB (10354085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a066cfbe30cd983f5ffef2df9d50618ade23fe99302b69e012774b2269585d1`  
		Last Modified: Fri, 05 Mar 2021 00:51:35 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9401205bc3eb7297f85c414b790172be23d1c4ab061aee72eaeb28b69132c073`  
		Last Modified: Fri, 05 Mar 2021 00:51:38 GMT  
		Size: 13.9 MB (13860060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afee2a631a7b79b3c487a3ef4500ea44fa978bd6464fe317d1a65d4b104f7309`  
		Last Modified: Fri, 05 Mar 2021 00:51:35 GMT  
		Size: 2.3 KB (2261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0499fd075a9fd055ca563a90fb4b2aaac9056a65b191d7db41c37188db098cf1`  
		Last Modified: Fri, 05 Mar 2021 00:51:35 GMT  
		Size: 17.6 KB (17566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b53123be7d4a2e60f8c580951db7f413a3fddabf032b97cc4e1715defe06aa`  
		Last Modified: Fri, 05 Mar 2021 01:36:37 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aab483619f81007684651c4b32aae7e47300c44374d5a2e165bfee97c9a5ed8`  
		Last Modified: Fri, 05 Mar 2021 01:36:35 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21994edf819ad8eed5eea7af018652abc984e3d7f67f6dd34ead1779f80b961c`  
		Last Modified: Fri, 05 Mar 2021 01:36:35 GMT  
		Size: 3.6 MB (3583473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39598f68be044d39764fd4f2c72cccb6ff39c29081b324413fb9af80f22c6b6`  
		Last Modified: Fri, 05 Mar 2021 01:36:35 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6988f4418691c53ad239170a2ec56313d0be5ebf6636151c2ab31dee05fd76`  
		Last Modified: Fri, 05 Mar 2021 01:36:35 GMT  
		Size: 582.8 KB (582811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f94af1afe9ebb57211f0f17af8d7edc0ccf29b7fe0f188bae543435432d960`  
		Last Modified: Fri, 05 Mar 2021 01:36:35 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
