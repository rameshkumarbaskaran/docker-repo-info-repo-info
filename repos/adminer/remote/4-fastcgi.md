## `adminer:4-fastcgi`

```console
$ docker pull adminer@sha256:630be280f30da089ad51aefc958c156910e6a149710c9da8c2d59a081891aaf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `adminer:4-fastcgi` - linux; amd64

```console
$ docker pull adminer@sha256:a6fba2c8b8b2aedcc7563a7be20fdba3bed2806ee4ca6bbad9bfe451a247943d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31106050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce28adb4fe140e43080c7537718777a7893665a109d343d278f2fb4b29a1ab10`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 20:38:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 21 Oct 2019 20:38:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Mon, 21 Oct 2019 20:38:10 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 21 Oct 2019 20:38:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 21 Oct 2019 20:38:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Mon, 21 Oct 2019 20:43:24 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 24 Oct 2019 01:15:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2019 01:15:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2019 01:15:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 24 Oct 2019 01:15:45 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Wed, 18 Dec 2019 22:44:39 GMT
ENV PHP_VERSION=7.4.1
# Wed, 18 Dec 2019 22:44:39 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Wed, 18 Dec 2019 22:44:39 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Wed, 18 Dec 2019 22:44:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 18 Dec 2019 22:44:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 18 Dec 2019 22:53:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Wed, 18 Dec 2019 22:53:32 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Wed, 18 Dec 2019 22:53:33 GMT
RUN docker-php-ext-enable sodium
# Wed, 18 Dec 2019 22:53:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 18 Dec 2019 22:53:33 GMT
WORKDIR /var/www/html
# Wed, 18 Dec 2019 22:53:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Wed, 18 Dec 2019 22:53:34 GMT
STOPSIGNAL SIGQUIT
# Wed, 18 Dec 2019 22:53:35 GMT
EXPOSE 9000
# Wed, 18 Dec 2019 22:53:35 GMT
CMD ["php-fpm"]
# Thu, 19 Dec 2019 05:36:17 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Thu, 19 Dec 2019 05:36:18 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 19 Dec 2019 05:36:19 GMT
RUN apk add --no-cache libpq
# Thu, 19 Dec 2019 05:36:36 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Thu, 19 Dec 2019 05:36:36 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Thu, 19 Dec 2019 05:36:36 GMT
ENV ADMINER_VERSION=4.7.5
# Thu, 19 Dec 2019 05:36:37 GMT
ENV ADMINER_DOWNLOAD_SHA256=857351da4d8963ad5621f1a696bd2396b3c28d7f41284ab741fed65dec95539c
# Thu, 19 Dec 2019 05:36:37 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=07f47b70560bb5eaeeb6ffc3d3b53f038e10ffe582e6e16cd218221365f19677
# Thu, 19 Dec 2019 05:36:38 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Thu, 19 Dec 2019 05:36:38 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 19 Dec 2019 05:36:38 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 19 Dec 2019 05:36:39 GMT
USER adminer
# Thu, 19 Dec 2019 05:36:39 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feea9773e4044a213a29aa77e99239ac5e8f7f56877eab4f96530221d1323dae`  
		Last Modified: Mon, 21 Oct 2019 21:44:19 GMT  
		Size: 1.3 MB (1342556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8ac5388d32433d5cbb16635a76d609f999bcb3ca7d1e5119e373f8da4de580`  
		Last Modified: Mon, 21 Oct 2019 21:44:19 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a226b9fe82df5bbc955b561faf3aa8df8a2faef7d2fd6cc00d95e855d4dd01`  
		Last Modified: Mon, 21 Oct 2019 21:44:18 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99401fd0ece70360f3ccecf44f844a5a0efdf32146d6c446970c26531752c341`  
		Last Modified: Thu, 19 Dec 2019 03:00:56 GMT  
		Size: 10.3 MB (10263900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de913d86f05a50a4c3f792243ec9f24779f57ce0e0238c053c4287d7880a5347`  
		Last Modified: Thu, 19 Dec 2019 03:00:53 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2b5a211ce6ec0d98a72f219b18530d5c25fafc0a7a9a21b7da0330bbbe5797`  
		Last Modified: Thu, 19 Dec 2019 03:01:00 GMT  
		Size: 14.7 MB (14660671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b33dbfafe9a898ff3a2b3e4e1a7af15b797a7c00dd874e9d3c827e395cd43b`  
		Last Modified: Thu, 19 Dec 2019 03:00:54 GMT  
		Size: 2.2 KB (2220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e0c9bf0c294f08a2cc44a9197f856fda455f40aa06c532cea2cb79d6877f77`  
		Last Modified: Thu, 19 Dec 2019 03:00:53 GMT  
		Size: 72.3 KB (72299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa5c4c9069b45e81276629ede436f3bf5cea9843721c563a1f72553b0d445ec`  
		Last Modified: Thu, 19 Dec 2019 03:00:54 GMT  
		Size: 8.4 KB (8409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b066b20593318b62a26b9637aa4ab4a2a37c8f397ee9fdba7e79e592e450402f`  
		Last Modified: Thu, 19 Dec 2019 05:37:01 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640b2caf715bb36f272914262e86e6181fa0510cc8236e55b5a5ff3cd535744d`  
		Last Modified: Thu, 19 Dec 2019 05:37:01 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc66e0562ddf1d4ba9dcaffa1afa1eae778de558f7674bc53c7473b63ac44f22`  
		Last Modified: Thu, 19 Dec 2019 05:37:00 GMT  
		Size: 1.3 MB (1267203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b877ea3f3b11a7225696f96d2c7247c2f8b714f79fc03f89f71bebc6b9431424`  
		Last Modified: Thu, 19 Dec 2019 05:37:00 GMT  
		Size: 125.7 KB (125656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014e55e883e88a5a8887682b5c9b8c76b00141600a698701ec3cb97da6380b0f`  
		Last Modified: Thu, 19 Dec 2019 05:37:00 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac91ac5b58c527badba4ad4c05ece7bc5954fe9e14a7dd195cc1dc23479603d`  
		Last Modified: Thu, 19 Dec 2019 05:37:00 GMT  
		Size: 570.4 KB (570381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f0eb5db857e60dc084fc2707add56ec223c18d1235477d69daf5a1635a8966d`  
		Last Modified: Thu, 19 Dec 2019 05:37:00 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm variant v6

```console
$ docker pull adminer@sha256:77cc97e832575b7c1f99abbe3d0f189dfd9e61a94c993bc0612a10f60e5db223
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31236686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd47698a9f94a455b8d6f314a9dc83be98fc0586326d85f664f3a7461a52b98`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 24 Dec 2019 18:49:41 GMT
ADD file:c4f944e24d0f2e758363506e8b98b3b53973ec18dd4dd23da3f09520ef22c65c in / 
# Tue, 24 Dec 2019 18:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 22:20:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 22:20:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 22:20:18 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 22:20:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 22:20:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 22:24:45 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 26 Dec 2019 22:24:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:24:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:24:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 22:24:48 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 22:24:49 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 22:24:50 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 22:24:51 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 22:24:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 22:24:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:29:19 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 22:29:23 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:29:35 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 22:29:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 22:29:40 GMT
WORKDIR /var/www/html
# Thu, 26 Dec 2019 22:29:46 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 26 Dec 2019 22:29:46 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Dec 2019 22:29:47 GMT
EXPOSE 9000
# Thu, 26 Dec 2019 22:29:48 GMT
CMD ["php-fpm"]
# Fri, 27 Dec 2019 01:10:39 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 27 Dec 2019 01:10:42 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 27 Dec 2019 01:10:45 GMT
RUN apk add --no-cache libpq
# Fri, 27 Dec 2019 01:11:24 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 27 Dec 2019 01:11:25 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 27 Dec 2019 01:11:26 GMT
ENV ADMINER_VERSION=4.7.5
# Fri, 27 Dec 2019 01:11:27 GMT
ENV ADMINER_DOWNLOAD_SHA256=857351da4d8963ad5621f1a696bd2396b3c28d7f41284ab741fed65dec95539c
# Fri, 27 Dec 2019 01:11:28 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=07f47b70560bb5eaeeb6ffc3d3b53f038e10ffe582e6e16cd218221365f19677
# Fri, 27 Dec 2019 01:11:31 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 27 Dec 2019 01:11:32 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 27 Dec 2019 01:11:33 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 27 Dec 2019 01:11:33 GMT
USER adminer
# Fri, 27 Dec 2019 01:11:34 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:546eec1e02ac5f4494868d8b22e8ced00773a2fba8e25b3edd30002889874299`  
		Last Modified: Tue, 24 Dec 2019 18:50:07 GMT  
		Size: 2.6 MB (2612021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f2222aeb0ea56ad08de7753e2ed3f6c40f7093cda7436e94583ce0f0922072`  
		Last Modified: Thu, 26 Dec 2019 23:02:36 GMT  
		Size: 1.3 MB (1321130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f893e696ec7590309f1a77539ce734af052f1aa42c48aaf6f478453dcd7eafa`  
		Last Modified: Thu, 26 Dec 2019 23:02:35 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ad230ebfba33233fbafdd19ca2939dfd20dffdc83636c23f9285017935fca9`  
		Last Modified: Thu, 26 Dec 2019 23:02:35 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab304e6f8d5ee14818b69d7f454b10bb1b58e96c4425b2df48f6a1901359e9e`  
		Last Modified: Thu, 26 Dec 2019 23:03:06 GMT  
		Size: 10.3 MB (10264410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e63b620269b288a2842d7b18a5890e19d00ddb60e7c9c00a11eeb546343285e`  
		Last Modified: Thu, 26 Dec 2019 23:03:04 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af1c46b0525e2c0094abcaccdaf30b05d418ad96c0a6bdc362a654bce76605c`  
		Last Modified: Thu, 26 Dec 2019 23:03:08 GMT  
		Size: 15.0 MB (15025066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa708d0c4c86408eb6d130d742667cdf0467ed3a036f58f1602842b9f30b72f`  
		Last Modified: Thu, 26 Dec 2019 23:03:03 GMT  
		Size: 2.2 KB (2220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fab8f904d3b232e05897d0a8b62c7467390a4b2acccf4415bead91a6ecf9ba0`  
		Last Modified: Thu, 26 Dec 2019 23:03:03 GMT  
		Size: 72.7 KB (72677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d29ba0a8fa2bf1b2ecfd2108f31f38bf4958b7dd36f312503cbbedcbd146012d`  
		Last Modified: Thu, 26 Dec 2019 23:03:03 GMT  
		Size: 8.4 KB (8412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd71418cc406d3e1c09c02597537252c189b945d82eaf5a7edefd4eb96c48463`  
		Last Modified: Fri, 27 Dec 2019 01:12:13 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40ad95bf8de58927184e9d49bab6b065bcecf60313ea921158b332c34d7a722`  
		Last Modified: Fri, 27 Dec 2019 01:12:13 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274167797df0d8caf3d1bd357b5d179cea3745623b45031be79401e9a90821f6`  
		Last Modified: Fri, 27 Dec 2019 01:12:10 GMT  
		Size: 1.2 MB (1234588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b8b3eb2bed2d02dd141630147a3e0ee0b22d8c1657de5c0045e5b13cf1231d`  
		Last Modified: Fri, 27 Dec 2019 01:12:10 GMT  
		Size: 120.0 KB (120030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939ad560f7b8af5440bfeea46135af8dcad429d1e6bc4738da6b46714d181b0c`  
		Last Modified: Fri, 27 Dec 2019 01:12:10 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:937bb5add534f40b1fec3b41e2a26daeb605a6a13b800103947a7d7e4334f3b5`  
		Last Modified: Fri, 27 Dec 2019 01:12:10 GMT  
		Size: 570.5 KB (570451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1619a39b7b252548309d44f94d6b37fc5ffceae08ce2cc79c1397d74df2119c1`  
		Last Modified: Fri, 27 Dec 2019 01:12:10 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:f2703cf92fbe8afae4cb14b41e393bb64bca9c908b6e7b95ca79cd319de00f69
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.9 MB (29905182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e992357d6ab475df064bd7ab36299a2c97f45f59d3b0be7c55186316eadc286`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 24 Dec 2019 18:59:09 GMT
ADD file:caf7ca25875eddd2bfa2d1e56663bb52d278a85f6ee1314f9ccf01dc4da8070a in / 
# Tue, 24 Dec 2019 18:59:10 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:28:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 21:28:59 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 21:29:01 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 21:29:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 21:29:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 21:31:46 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 26 Dec 2019 21:31:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 21:31:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 21:31:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 21:31:48 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 21:31:49 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 21:31:49 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 21:31:50 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 21:31:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 21:31:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:34:19 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 21:34:21 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:34:23 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 21:34:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 21:34:24 GMT
WORKDIR /var/www/html
# Thu, 26 Dec 2019 21:34:26 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 26 Dec 2019 21:34:26 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Dec 2019 21:34:27 GMT
EXPOSE 9000
# Thu, 26 Dec 2019 21:34:27 GMT
CMD ["php-fpm"]
# Thu, 26 Dec 2019 23:55:37 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Thu, 26 Dec 2019 23:55:38 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 26 Dec 2019 23:55:40 GMT
RUN apk add --no-cache libpq
# Thu, 26 Dec 2019 23:56:09 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Thu, 26 Dec 2019 23:56:09 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Thu, 26 Dec 2019 23:56:10 GMT
ENV ADMINER_VERSION=4.7.5
# Thu, 26 Dec 2019 23:56:11 GMT
ENV ADMINER_DOWNLOAD_SHA256=857351da4d8963ad5621f1a696bd2396b3c28d7f41284ab741fed65dec95539c
# Thu, 26 Dec 2019 23:56:12 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=07f47b70560bb5eaeeb6ffc3d3b53f038e10ffe582e6e16cd218221365f19677
# Thu, 26 Dec 2019 23:56:14 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Thu, 26 Dec 2019 23:56:15 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 26 Dec 2019 23:56:16 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 26 Dec 2019 23:56:16 GMT
USER adminer
# Thu, 26 Dec 2019 23:56:17 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3922e475e500b2739b5e74787fc80622853325822f71f8bd3de7e5b09654d60f`  
		Last Modified: Tue, 24 Dec 2019 18:59:33 GMT  
		Size: 2.4 MB (2416691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d850653ef66a74bc2f65e933df679895db53bc6e01d23076dbc532056eec8a7`  
		Last Modified: Thu, 26 Dec 2019 22:01:17 GMT  
		Size: 1.2 MB (1227347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed0b2f0bcd9c23ef1f79be9d752fea5f714457c75308002cf597d596e8b1c1a`  
		Last Modified: Thu, 26 Dec 2019 22:01:17 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77de73a7de2b81d6828d80578fc934edf55e039effcf2bb8555e6a0b5864080`  
		Last Modified: Thu, 26 Dec 2019 22:01:17 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c11d20d004d40b99d5194df6300e64226aa44c67452ecece47a184bbe8080a0`  
		Last Modified: Thu, 26 Dec 2019 22:01:52 GMT  
		Size: 10.3 MB (10264422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5460405b7323ea77ca7d7ad362ab4002b71737204bc819aa9cb7639a6a5511c`  
		Last Modified: Thu, 26 Dec 2019 22:01:49 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f931bf1ab6b00d5323feb85b158592d01c205ba7598375b5e25687a9e34ba27`  
		Last Modified: Thu, 26 Dec 2019 22:01:54 GMT  
		Size: 14.1 MB (14097660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ee7e2b5788a8ddf71c69f897be7155ae35a4e029addb9cb68b5e46cb66426d`  
		Last Modified: Thu, 26 Dec 2019 22:01:49 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9cbe15a8b4b41cc991f69471bf6f621a85758139eb5223c7581f426181b3b64`  
		Last Modified: Thu, 26 Dec 2019 22:01:49 GMT  
		Size: 72.7 KB (72675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e687de4d653c5a639b88a7f65e523c3fb81c66add44f474f84cf85f7772ad6`  
		Last Modified: Thu, 26 Dec 2019 22:01:49 GMT  
		Size: 8.4 KB (8410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c055d28bc5840f04a400fafb55f1ee49fb2ef4285a882beefb16f63a668bfdb8`  
		Last Modified: Thu, 26 Dec 2019 23:56:52 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b6ad6f596f2ae42406232d4c14216308901bf6502953d57161485ab0e19e2`  
		Last Modified: Thu, 26 Dec 2019 23:56:52 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c5f6e3ff4edf50028b2e6fec70191ded7efcf2b95b9ad21c71d83dc8f88f99`  
		Last Modified: Thu, 26 Dec 2019 23:56:50 GMT  
		Size: 1.1 MB (1124733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd571a10306ad93eee284565fde27d3c1f7aa0a5c1f2dc382e6c5851f47823d`  
		Last Modified: Thu, 26 Dec 2019 23:56:51 GMT  
		Size: 114.9 KB (114911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56b227b6b810ae706d407f7b12218f76d346ee6e75bb4ded7f4cbac0d0f07b0`  
		Last Modified: Thu, 26 Dec 2019 23:56:50 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18843fbdb73c5ffc9c508bb1e272fa0258fbec00c3fa9b43de50ca48f0b7214e`  
		Last Modified: Thu, 26 Dec 2019 23:56:50 GMT  
		Size: 570.4 KB (570439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35cb645bbc18deb730aba0ab04842a4f44ba3edd4345b3e1e32e06bdc5c3650`  
		Last Modified: Thu, 26 Dec 2019 23:56:50 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:cbcb81bb2c1d30f24a607b2bf00b5c5d3b956b402cc07e1e010c2820c6e92a22
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32352363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5597d49153c0c0dafdd44f5525ad7ebde05ad1474ef2c1a5d2ef0a45839f04`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 24 Dec 2019 20:26:15 GMT
ADD file:d6c3db0313ab0c6201770c7248d1bac964011a1c08f1a9b434442b7c21efef87 in / 
# Tue, 24 Dec 2019 20:26:24 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 22:08:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 22:08:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 22:08:31 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 22:08:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 22:08:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 22:12:44 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 26 Dec 2019 22:12:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:12:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:12:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 22:12:49 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 22:12:50 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 22:12:51 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 22:12:53 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 22:12:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 22:12:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:16:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 22:16:36 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:16:40 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 22:16:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 22:16:42 GMT
WORKDIR /var/www/html
# Thu, 26 Dec 2019 22:16:48 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 26 Dec 2019 22:16:50 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Dec 2019 22:16:53 GMT
EXPOSE 9000
# Thu, 26 Dec 2019 22:16:54 GMT
CMD ["php-fpm"]
# Fri, 27 Dec 2019 00:57:00 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 27 Dec 2019 00:57:03 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 27 Dec 2019 00:57:08 GMT
RUN apk add --no-cache libpq
# Fri, 27 Dec 2019 00:57:48 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 27 Dec 2019 00:57:49 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 27 Dec 2019 00:57:50 GMT
ENV ADMINER_VERSION=4.7.5
# Fri, 27 Dec 2019 00:57:51 GMT
ENV ADMINER_DOWNLOAD_SHA256=857351da4d8963ad5621f1a696bd2396b3c28d7f41284ab741fed65dec95539c
# Fri, 27 Dec 2019 00:57:52 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=07f47b70560bb5eaeeb6ffc3d3b53f038e10ffe582e6e16cd218221365f19677
# Fri, 27 Dec 2019 00:57:58 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 27 Dec 2019 00:58:00 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 27 Dec 2019 00:58:01 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 27 Dec 2019 00:58:02 GMT
USER adminer
# Fri, 27 Dec 2019 00:58:04 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:cde5963f3b93eec667cad527c99d80402a5a91a7a1381f7ffe562f215aec0c50`  
		Last Modified: Tue, 24 Dec 2019 20:26:52 GMT  
		Size: 2.7 MB (2719182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36763f956175b40d2a6ca97c274d362c9a0deb76d9b7eb62e95b8ca953bb1db2`  
		Last Modified: Thu, 26 Dec 2019 22:48:41 GMT  
		Size: 1.4 MB (1359427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01374ab459ad592d2c9b91efb836df933906c6cd8c63606db7f385c084fa04d2`  
		Last Modified: Thu, 26 Dec 2019 22:48:40 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34492236b9882b05dc402fe511c10ac8463554a1223a9bd10460daeab25a98f`  
		Last Modified: Thu, 26 Dec 2019 22:48:40 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474f7a80201cc20ec59956d6cce765403fc020c0a49cc5136121c969007aead9`  
		Last Modified: Thu, 26 Dec 2019 22:49:09 GMT  
		Size: 10.3 MB (10264410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0436e47a841764ed38f8d21fdff56f7eeafefead8fd2320cc30874e6afd6383c`  
		Last Modified: Thu, 26 Dec 2019 22:49:07 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2cf87914a703d60144402468705b60cce64c90bcb6c856f68f00abe6f6bf47`  
		Last Modified: Thu, 26 Dec 2019 22:49:12 GMT  
		Size: 15.9 MB (15926064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c8a34eb5e66734b19696479a74fb3f960337310b26e77f3469b853e7d4080a`  
		Last Modified: Thu, 26 Dec 2019 22:49:07 GMT  
		Size: 2.2 KB (2219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b367a830e57fb19825431ca9d2804a540ce4620c4c031862719d01bc5cb7f05`  
		Last Modified: Thu, 26 Dec 2019 22:49:07 GMT  
		Size: 72.7 KB (72676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae18949d5ff2fd5cbb53b1a02ecc0dd6e210b30168fc40fac6772af107423a5`  
		Last Modified: Thu, 26 Dec 2019 22:49:07 GMT  
		Size: 8.4 KB (8413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b9fb9df87907ca82383cc972ca5b20ef04dcc4178e5679b9d6de064ff1aae4`  
		Last Modified: Fri, 27 Dec 2019 00:58:50 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97667e1e1f5cb90cc6ff4ab6f60e768bc0d6e16270a3d2fc297e31ec020b6c5`  
		Last Modified: Fri, 27 Dec 2019 00:58:51 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d691b108e52397911ca62ec4a2892f0de69decfd35155598197645a5729f5e3c`  
		Last Modified: Fri, 27 Dec 2019 00:58:49 GMT  
		Size: 1.3 MB (1299230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11692c5de2fd1b72d0bbc12b54b2ee7b08888f78687cb97426aa0a50da520326`  
		Last Modified: Fri, 27 Dec 2019 00:58:49 GMT  
		Size: 124.6 KB (124608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738febf67e71b1f24fa82dc06fa5a4c34e83581303d1b7c0fd6a05ce43919c82`  
		Last Modified: Fri, 27 Dec 2019 00:58:49 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef827005ecd7bebe14f157c318f1e8091d887ce2e1cf2f28596c77c377ca0f51`  
		Last Modified: Fri, 27 Dec 2019 00:58:49 GMT  
		Size: 570.4 KB (570447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d965a77c84fa07252e8ebb8a121b6e75a88f9d642a65e8aaf0c230d398a5cb`  
		Last Modified: Fri, 27 Dec 2019 00:58:49 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:d5ab0a2f0ff99e230cccd6cb45b9deb6489fe8192846a579296ac150ec911f46
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33355319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd96f6c318e5dd0c4e4bc6110629741022f88595fe23420f2c0bd54d3234215b`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 24 Dec 2019 19:38:57 GMT
ADD file:d0127a9692e8445993a88163cb741dbb23fa25436dd65289e76b08484264b397 in / 
# Tue, 24 Dec 2019 19:38:57 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 22:36:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 22:36:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 22:36:14 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 22:36:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 22:36:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 22:46:02 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 26 Dec 2019 22:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 22:46:03 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 22:46:04 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 22:46:04 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 22:46:04 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 22:46:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 22:46:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:55:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 22:55:40 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:55:42 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 22:55:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 22:55:43 GMT
WORKDIR /var/www/html
# Thu, 26 Dec 2019 22:55:44 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 26 Dec 2019 22:55:44 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Dec 2019 22:55:45 GMT
EXPOSE 9000
# Thu, 26 Dec 2019 22:55:45 GMT
CMD ["php-fpm"]
# Fri, 27 Dec 2019 01:43:09 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 27 Dec 2019 01:43:10 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 27 Dec 2019 01:43:11 GMT
RUN apk add --no-cache libpq
# Fri, 27 Dec 2019 01:43:28 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 27 Dec 2019 01:43:28 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 27 Dec 2019 01:43:29 GMT
ENV ADMINER_VERSION=4.7.5
# Fri, 27 Dec 2019 01:43:29 GMT
ENV ADMINER_DOWNLOAD_SHA256=857351da4d8963ad5621f1a696bd2396b3c28d7f41284ab741fed65dec95539c
# Fri, 27 Dec 2019 01:43:29 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=07f47b70560bb5eaeeb6ffc3d3b53f038e10ffe582e6e16cd218221365f19677
# Fri, 27 Dec 2019 01:43:30 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 27 Dec 2019 01:43:31 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 27 Dec 2019 01:43:31 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 27 Dec 2019 01:43:31 GMT
USER adminer
# Fri, 27 Dec 2019 01:43:31 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:57bbc6f150623b3e4f01930af4ab2efa6ed5df02319341a08b1ce0bbd7e4afdf`  
		Last Modified: Tue, 24 Dec 2019 19:39:19 GMT  
		Size: 2.8 MB (2805146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db25e971d6f24055202f90f96d257a719817ad73623eaf02d98fb13c2dbe9a1b`  
		Last Modified: Fri, 27 Dec 2019 00:00:12 GMT  
		Size: 1.5 MB (1452611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ecdadbdbb91bc66f820e5b3077004286155b3e618cc444f493d7e73b400333`  
		Last Modified: Fri, 27 Dec 2019 00:00:12 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8331211b40f9489961b63904af5f93f96465efa4f5202ee08600fd1fe3caec6c`  
		Last Modified: Fri, 27 Dec 2019 00:00:11 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c898237da49a3335f6813cdfd073c2a4552a1fe075a2107438912f99a4bef13d`  
		Last Modified: Fri, 27 Dec 2019 00:00:34 GMT  
		Size: 10.3 MB (10264414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc30aec901261e4fd0bb030c7047f9a147a071d56a8beff7a51cce88efec310c`  
		Last Modified: Fri, 27 Dec 2019 00:00:31 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70031a3e4784b8eb4530e90ba8a8638a2251103e562d5d3a34b8c89f19c18995`  
		Last Modified: Fri, 27 Dec 2019 00:00:39 GMT  
		Size: 16.6 MB (16645879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3a84644960e8c3296b802ca166d6b1ee94931e3e5edb780eff374d1aefed88`  
		Last Modified: Fri, 27 Dec 2019 00:00:31 GMT  
		Size: 2.2 KB (2219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:089d11f253333704cdcaf8495f141b3c8884e887e0b7dfc0c8174b92636ed244`  
		Last Modified: Fri, 27 Dec 2019 00:00:31 GMT  
		Size: 72.3 KB (72339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b89d7c97ca63dbd49171bacd97acefdd2f60c6820db1c6d18589983e38333b0`  
		Last Modified: Fri, 27 Dec 2019 00:00:31 GMT  
		Size: 8.4 KB (8405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ea2dbbb5030cbad0c3e17805fd15329af2cbcba061a8c8e0ef08b16b18a503`  
		Last Modified: Fri, 27 Dec 2019 01:43:55 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a4841da56330354852a77712622640a383b049b336c77c2b7712a3fc9a4676`  
		Last Modified: Fri, 27 Dec 2019 01:43:55 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150dae6a7c76bf284adca6fe069498d8b3d1a2c2f7945e58b8bdaa1835f095af`  
		Last Modified: Fri, 27 Dec 2019 01:43:54 GMT  
		Size: 1.4 MB (1397656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa235ab6ffcc99d75227e6498d8c39622ea179d4e11c0336ede459f5e71bae9`  
		Last Modified: Fri, 27 Dec 2019 01:43:54 GMT  
		Size: 130.7 KB (130715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c53a485f5135790cb5edbaa48f963a0c54005c90b1db971aa6c79d3f11418c7`  
		Last Modified: Fri, 27 Dec 2019 01:43:54 GMT  
		Size: 1.5 KB (1470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea3b999e7281e94f7ee7f9dd0214bdb5203bdb81ce0336548cff88dc4715abc`  
		Last Modified: Fri, 27 Dec 2019 01:43:54 GMT  
		Size: 570.4 KB (570375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dca10af384876e3bdaa22dd3a935d55c2b60a4741df77b3fbd7ee6309b80949`  
		Last Modified: Fri, 27 Dec 2019 01:43:54 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:edb718195af6cd23b24e336835fdeeef4726ba9530d793b1cd5f64c07c79c864
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33779013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375c965f5a62780553c87dd30e0084b21ba51b4e456fd2291b7e8d9f07f9592a`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 24 Dec 2019 19:28:37 GMT
ADD file:4d85451a651e236d899cd849617594eb6babf24079f9b2269134ad06d89bdecc in / 
# Tue, 24 Dec 2019 19:28:38 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 22:21:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 22:21:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 22:21:14 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 22:21:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 22:21:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 22:28:02 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 26 Dec 2019 22:28:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:28:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:28:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 22:28:17 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 22:28:21 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 22:28:26 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 22:28:29 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 22:28:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 22:28:45 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:33:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 22:33:30 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:33:36 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 22:33:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 22:33:41 GMT
WORKDIR /var/www/html
# Thu, 26 Dec 2019 22:33:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 26 Dec 2019 22:33:47 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Dec 2019 22:33:49 GMT
EXPOSE 9000
# Thu, 26 Dec 2019 22:33:51 GMT
CMD ["php-fpm"]
# Fri, 27 Dec 2019 01:27:24 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 27 Dec 2019 01:27:29 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 27 Dec 2019 01:27:33 GMT
RUN apk add --no-cache libpq
# Fri, 27 Dec 2019 01:27:58 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 27 Dec 2019 01:27:59 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 27 Dec 2019 01:28:01 GMT
ENV ADMINER_VERSION=4.7.5
# Fri, 27 Dec 2019 01:28:03 GMT
ENV ADMINER_DOWNLOAD_SHA256=857351da4d8963ad5621f1a696bd2396b3c28d7f41284ab741fed65dec95539c
# Fri, 27 Dec 2019 01:28:05 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=07f47b70560bb5eaeeb6ffc3d3b53f038e10ffe582e6e16cd218221365f19677
# Fri, 27 Dec 2019 01:28:10 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 27 Dec 2019 01:28:11 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 27 Dec 2019 01:28:13 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 27 Dec 2019 01:28:14 GMT
USER adminer
# Fri, 27 Dec 2019 01:28:16 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a5dee701e1e87430161d8fce67e77ee5e132bdbafe165c52490a36df654c7660`  
		Last Modified: Tue, 24 Dec 2019 19:29:09 GMT  
		Size: 2.8 MB (2816482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5787caafdab36524ef14f193793a44b3b5f54da82c98e8152770c2868fd93b11`  
		Last Modified: Thu, 26 Dec 2019 23:13:04 GMT  
		Size: 1.4 MB (1397977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691639ddfd73c88dfeda1734ababccfaed311f9d747bf07d41c6e7fed2880baf`  
		Last Modified: Thu, 26 Dec 2019 23:13:03 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2a706347c576336f1e0145755e4fa707710b3f42dc7d18903fcee51bb72842`  
		Last Modified: Thu, 26 Dec 2019 23:13:02 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6265853e696169a34fbbea5b88ddb0984c7e5a3b82e277d5eb322b9549fc01`  
		Last Modified: Thu, 26 Dec 2019 23:14:01 GMT  
		Size: 10.3 MB (10264438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8fbe6cc840a0629d1c42e7961db868a757536b63a3911a986b03f08b5c0bee9`  
		Last Modified: Thu, 26 Dec 2019 23:13:56 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e1c51cf67fc2a96b322f860a81ecc0c8e83a4ee9c0a36f17cabaa89bae5150`  
		Last Modified: Thu, 26 Dec 2019 23:14:07 GMT  
		Size: 17.2 MB (17153993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77114ea50cd1d27fa7a2f49a2b1d30f57a67d9457fb679bc5577bb7d64661c6`  
		Last Modified: Thu, 26 Dec 2019 23:13:56 GMT  
		Size: 2.2 KB (2218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd9b53f7e638e15d075fffbcf0e5f96c75415c70a3a4c311eaeac82f80a86ac6`  
		Last Modified: Thu, 26 Dec 2019 23:13:56 GMT  
		Size: 73.0 KB (73014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e903c6f5ff4c873c3c58d4c1d993d14f5af469901a9bdb20cb4dec0ce0fa08`  
		Last Modified: Thu, 26 Dec 2019 23:13:56 GMT  
		Size: 8.4 KB (8410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2d6072b86cd32b875900471516245970b71dbdd6aa8cbfb0445c6f8e8a76a7`  
		Last Modified: Fri, 27 Dec 2019 01:29:22 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56da1647a67e908afad3d8848ed9860ec46e716bb57be44dd248fe8507352a1`  
		Last Modified: Fri, 27 Dec 2019 01:29:22 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6fec04281325b33caa11ae7e30c70a817f67b0e38058beb15214b6eab23f9a`  
		Last Modified: Fri, 27 Dec 2019 01:29:20 GMT  
		Size: 1.4 MB (1350646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9e9f4625db5b290e8b886809d9cffc2ad97f4fc517cc2bc844963e7da9e5e2`  
		Last Modified: Fri, 27 Dec 2019 01:29:19 GMT  
		Size: 135.7 KB (135709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78448fb55ff7a820e71e34aaf5476ff0e68fc7314a821c168183be1262a3370f`  
		Last Modified: Fri, 27 Dec 2019 01:29:19 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03abb5079c0b5586b560fafa6d8536c2871e0179a2f34912bfb03cd3bb6e190e`  
		Last Modified: Fri, 27 Dec 2019 01:29:19 GMT  
		Size: 570.4 KB (570445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa90b78bb1d2036c2bdd1ac0f1d9b10525fbc37d5741baaa0d1ca5f0ef23e449`  
		Last Modified: Fri, 27 Dec 2019 01:29:19 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
