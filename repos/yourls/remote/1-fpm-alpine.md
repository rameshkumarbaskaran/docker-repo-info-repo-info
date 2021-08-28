## `yourls:1-fpm-alpine`

```console
$ docker pull yourls@sha256:0bd578149c6b6b2cd813017f00269f26e659c15879baf16968f68f168f421a6c
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

### `yourls:1-fpm-alpine` - linux; amd64

```console
$ docker pull yourls@sha256:a96d7f221edb31b6f8b326b0f008612513c425ab3117933c5efc820d6fb4ee44
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34110547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d664f1b2a80db71ff0c5575cf0eae73421fd11b99efcce34bcea1461a29e1861`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 21:00:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 21:00:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 21:00:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 21:00:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 21:00:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 21:12:06 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 27 Aug 2021 21:12:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 21:12:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 21:12:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 21:33:53 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 27 Aug 2021 21:33:53 GMT
ENV PHP_VERSION=8.0.10
# Fri, 27 Aug 2021 21:33:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.10.tar.xz.asc
# Fri, 27 Aug 2021 21:33:53 GMT
ENV PHP_SHA256=66dc4d1bc86d9c1bc255b51b79d337ed1a7a035cf71230daabbf9a4ca35795eb
# Fri, 27 Aug 2021 21:34:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 27 Aug 2021 21:34:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Aug 2021 21:41:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Aug 2021 21:41:16 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 27 Aug 2021 21:41:18 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Aug 2021 21:41:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Aug 2021 21:41:18 GMT
WORKDIR /var/www/html
# Fri, 27 Aug 2021 21:41:19 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 27 Aug 2021 21:41:19 GMT
STOPSIGNAL SIGQUIT
# Fri, 27 Aug 2021 21:41:19 GMT
EXPOSE 9000
# Fri, 27 Aug 2021 21:41:20 GMT
CMD ["php-fpm"]
# Sat, 28 Aug 2021 02:30:25 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Sat, 28 Aug 2021 02:30:25 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 28 Aug 2021 02:30:27 GMT
RUN apk add --no-cache bash
# Sat, 28 Aug 2021 02:30:27 GMT
ENV YOURLS_VERSION=1.8.1
# Sat, 28 Aug 2021 02:30:27 GMT
ENV YOURLS_SHA256=92b0666af3e3ad4a783e78cba93687e9a24acf216606a6d457819c5d36d2cfe4
# Sat, 28 Aug 2021 02:30:29 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Sat, 28 Aug 2021 02:30:29 GMT
COPY file:7bfc5a435dd9f76b0c1d23545b13f25bad15f4271d687c1a76bb5d10a41af1eb in /usr/local/bin/ 
# Sat, 28 Aug 2021 02:30:29 GMT
COPY file:0bcfdfe0566007e7477c55552a1341b82b958e95879a5314f411d2188da2429e in /usr/src/yourls/user/ 
# Sat, 28 Aug 2021 02:30:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Aug 2021 02:30:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153eea49496a46a69cf5f48803e9014824a6be1d3e04f9ee47cd3f395aba6d76`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 1.7 MB (1707843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11efd0df1fcb3f56e825ef3449f199b261f44e0130a10cb77fcf78339cb88173`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f3214c344df86e90fe2ae24d643d9dbc5dcfd6f229f4ee58f7c60c6f0cc895`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca3b156c422290e21480aba21414cdd28483d5dad9427df72d911dc79d0f99a`  
		Last Modified: Fri, 27 Aug 2021 22:43:29 GMT  
		Size: 10.7 MB (10722808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a82b29ca7841e4f869ad49ed2830595c69e5424d419fc603676d2f8eac2bc0`  
		Last Modified: Fri, 27 Aug 2021 22:43:26 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2009e000d9090805fd5d7046f821bc7a4dabbef12bf8468bc2ced38bbc6360`  
		Last Modified: Fri, 27 Aug 2021 22:43:29 GMT  
		Size: 15.1 MB (15082473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b96d2564500849cefb0d6f052fada5294521f8f1f7131587bfbebf4b705ed07`  
		Last Modified: Fri, 27 Aug 2021 22:43:26 GMT  
		Size: 2.3 KB (2263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f280c14bdb5b6903fa52cf29a5ff7fcccdb43d16c856e2128be4b4d703d74ad`  
		Last Modified: Fri, 27 Aug 2021 22:43:26 GMT  
		Size: 17.8 KB (17792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91356e6001923ea92c8eac82094f3dff308d05b81363fb945d1c00f200f68b3c`  
		Last Modified: Fri, 27 Aug 2021 22:43:26 GMT  
		Size: 8.6 KB (8570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5419b7e308df024e8dc156ee2ff21a169ceaa472b59e61ed41b76b9990bf08c`  
		Last Modified: Sat, 28 Aug 2021 02:31:01 GMT  
		Size: 711.1 KB (711056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1187ede8dce99504cfbd83d4c67d34d4c97b67e430e3446c2fbc36c268c7418`  
		Last Modified: Sat, 28 Aug 2021 02:30:58 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9353d9a91f8d946c349820330b58917c7dadcdf6177ee9a59cc068c30cd8bba4`  
		Last Modified: Sat, 28 Aug 2021 02:30:58 GMT  
		Size: 465.6 KB (465563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:631fb627c80949f8b385be15fad443a6aa45eecfc62e2fa2934a1c3b4dade265`  
		Last Modified: Sat, 28 Aug 2021 02:30:58 GMT  
		Size: 2.6 MB (2572158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdfb794dd131d139d4a10b5ead378bbcb5a65237bc65a974614a3ad13a268921`  
		Last Modified: Sat, 28 Aug 2021 02:30:58 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd7aee36893fa9d956f9bfef4a171e133e87c0b9db3aa6110695b94c1cc05f0`  
		Last Modified: Sat, 28 Aug 2021 02:30:58 GMT  
		Size: 2.0 KB (2041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm-alpine` - linux; arm variant v6

```console
$ docker pull yourls@sha256:833464a04503d89f256a7644a0ae154b7178b644926b343e92bf037c74e95a02
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32180668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e066b3dce50fe3d0a6e0ce1e63d9a92a13edad4875082b3a8fef7f3129d3d839`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 20:48:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 20:48:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 20:48:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 20:48:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 20:48:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 20:53:20 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 27 Aug 2021 20:53:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 20:53:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 20:53:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 21:03:54 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 27 Aug 2021 21:03:55 GMT
ENV PHP_VERSION=8.0.10
# Fri, 27 Aug 2021 21:03:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.10.tar.xz.asc
# Fri, 27 Aug 2021 21:03:55 GMT
ENV PHP_SHA256=66dc4d1bc86d9c1bc255b51b79d337ed1a7a035cf71230daabbf9a4ca35795eb
# Fri, 27 Aug 2021 21:04:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 27 Aug 2021 21:04:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Aug 2021 21:08:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Aug 2021 21:08:39 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 27 Aug 2021 21:08:41 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Aug 2021 21:08:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Aug 2021 21:08:42 GMT
WORKDIR /var/www/html
# Fri, 27 Aug 2021 21:08:44 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 27 Aug 2021 21:08:44 GMT
STOPSIGNAL SIGQUIT
# Fri, 27 Aug 2021 21:08:45 GMT
EXPOSE 9000
# Fri, 27 Aug 2021 21:08:45 GMT
CMD ["php-fpm"]
# Sat, 28 Aug 2021 01:43:25 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Sat, 28 Aug 2021 01:43:27 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 28 Aug 2021 01:43:29 GMT
RUN apk add --no-cache bash
# Sat, 28 Aug 2021 01:43:30 GMT
ENV YOURLS_VERSION=1.8.1
# Sat, 28 Aug 2021 01:43:30 GMT
ENV YOURLS_SHA256=92b0666af3e3ad4a783e78cba93687e9a24acf216606a6d457819c5d36d2cfe4
# Sat, 28 Aug 2021 01:43:33 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Sat, 28 Aug 2021 01:43:34 GMT
COPY file:7bfc5a435dd9f76b0c1d23545b13f25bad15f4271d687c1a76bb5d10a41af1eb in /usr/local/bin/ 
# Sat, 28 Aug 2021 01:43:35 GMT
COPY file:0bcfdfe0566007e7477c55552a1341b82b958e95879a5314f411d2188da2429e in /usr/src/yourls/user/ 
# Sat, 28 Aug 2021 01:43:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Aug 2021 01:43:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05720bf4927bb754d842782fff2d045d42b804759e30b8312cbf75272e200af`  
		Last Modified: Fri, 27 Aug 2021 21:55:19 GMT  
		Size: 1.7 MB (1696736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9951b98a5bb83a868efe164832e7d1a35e9a078a82219f95634454a864a332`  
		Last Modified: Fri, 27 Aug 2021 21:55:18 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6baa29c72aee654b7205fcfbde95333a6e9a5dfadc1a99d94e64c957f543ac`  
		Last Modified: Fri, 27 Aug 2021 21:55:18 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7782128efb22de8c009fb611ff2a882e179d7c920e400bb46eedee9b376177af`  
		Last Modified: Fri, 27 Aug 2021 21:58:13 GMT  
		Size: 10.7 MB (10722822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f768871d9f3b7a2e4dd4f5f40c76804c9d60be941d3528e7f301794911e817ed`  
		Last Modified: Fri, 27 Aug 2021 21:58:09 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78aa3af1d3d2cc2abfb828b05b88257d8c247b1babd2a4d9ca375959d58d8c9b`  
		Last Modified: Fri, 27 Aug 2021 21:58:19 GMT  
		Size: 13.7 MB (13713193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b218ec210bebdfbb6b1df39af6a2f62e301fa23b4eecfb8edff3ab1ceda4f14e`  
		Last Modified: Fri, 27 Aug 2021 21:58:08 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8b5b624f5b2f4d8704a78e97d283d4c24e0709b7b9b55ab3e7272dd520240d`  
		Last Modified: Fri, 27 Aug 2021 21:58:08 GMT  
		Size: 17.8 KB (17812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb01d3044874a53745331feef3483abe6819998c2c8a339093996cda0f4f70a`  
		Last Modified: Fri, 27 Aug 2021 21:58:09 GMT  
		Size: 8.6 KB (8571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f16560a89ea4b3f233b581581efae60d46e5d47840cc172ee80dc0f6b5fb267`  
		Last Modified: Sat, 28 Aug 2021 01:44:09 GMT  
		Size: 359.8 KB (359839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c9caf7038a0967f4045987b358d137d9e6f214950240e66b7b391b1f295e64`  
		Last Modified: Sat, 28 Aug 2021 01:44:07 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5943f70e36819ec843d04caa8ec640f9e78cdbf9ed856934d70389f4ff6357`  
		Last Modified: Sat, 28 Aug 2021 01:44:07 GMT  
		Size: 454.2 KB (454249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a409bf9d242466f4dfdd3213e3db523414d1e83fbb401a19297fec18f91a79`  
		Last Modified: Sat, 28 Aug 2021 01:44:09 GMT  
		Size: 2.6 MB (2572154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d476b86073e5805ab0940740b20b87d8fcd573ec62a91f4cb4c0d8e636c36b9`  
		Last Modified: Sat, 28 Aug 2021 01:44:07 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f31f7f966c743e1a5b84ae3afccfac847c09256a63016a5b204e39d61bc632d`  
		Last Modified: Sat, 28 Aug 2021 01:44:07 GMT  
		Size: 2.0 KB (2039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm-alpine` - linux; arm variant v7

```console
$ docker pull yourls@sha256:19a6d1588b91b434037bda53776e45d0a7075c71547c854ab1a91cd65c0124d4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32213786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c743e507953cc9792654e523bfd1b521297f766b1c27ff6cc87b6a4e44e4dba8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Aug 2021 17:57:32 GMT
ADD file:3a35ff3ac0d80289d419a4d6d8319610c38e1936d296addafb9aaf506946230f in / 
# Fri, 06 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 20:54:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Aug 2021 20:54:19 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 06 Aug 2021 20:54:20 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Aug 2021 20:54:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Aug 2021 20:54:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 06 Aug 2021 20:58:58 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 06 Aug 2021 20:58:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 20:58:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 20:58:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Aug 2021 21:10:01 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 26 Aug 2021 23:21:12 GMT
ENV PHP_VERSION=8.0.10
# Thu, 26 Aug 2021 23:21:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.10.tar.xz.asc
# Thu, 26 Aug 2021 23:21:13 GMT
ENV PHP_SHA256=66dc4d1bc86d9c1bc255b51b79d337ed1a7a035cf71230daabbf9a4ca35795eb
# Thu, 26 Aug 2021 23:21:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Aug 2021 23:21:28 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Aug 2021 23:25:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 26 Aug 2021 23:25:43 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Thu, 26 Aug 2021 23:25:46 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Aug 2021 23:25:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Aug 2021 23:25:47 GMT
WORKDIR /var/www/html
# Thu, 26 Aug 2021 23:25:49 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 26 Aug 2021 23:25:49 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Aug 2021 23:25:50 GMT
EXPOSE 9000
# Thu, 26 Aug 2021 23:25:50 GMT
CMD ["php-fpm"]
# Fri, 27 Aug 2021 10:59:49 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Fri, 27 Aug 2021 10:59:51 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 27 Aug 2021 10:59:53 GMT
RUN apk add --no-cache bash
# Fri, 27 Aug 2021 10:59:54 GMT
ENV YOURLS_VERSION=1.8.1
# Fri, 27 Aug 2021 10:59:54 GMT
ENV YOURLS_SHA256=92b0666af3e3ad4a783e78cba93687e9a24acf216606a6d457819c5d36d2cfe4
# Fri, 27 Aug 2021 10:59:58 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 27 Aug 2021 10:59:59 GMT
COPY file:7bfc5a435dd9f76b0c1d23545b13f25bad15f4271d687c1a76bb5d10a41af1eb in /usr/local/bin/ 
# Fri, 27 Aug 2021 10:59:59 GMT
COPY file:0bcfdfe0566007e7477c55552a1341b82b958e95879a5314f411d2188da2429e in /usr/src/yourls/user/ 
# Fri, 27 Aug 2021 11:00:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Aug 2021 11:00:00 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4ee0caa23b369b04827640a4be298bf4ff7bacd030c77e915f5d7fb8f987594a`  
		Last Modified: Fri, 06 Aug 2021 17:58:57 GMT  
		Size: 2.4 MB (2429359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60e2d83b5c992b22cef3665b0ab131088923cffff86634ff4237393a231b13d`  
		Last Modified: Fri, 06 Aug 2021 22:04:23 GMT  
		Size: 1.6 MB (1564630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d851eb12a849920c3886c6a5cc4c6ff6340be6574eae5478f604b4428ab1dc3`  
		Last Modified: Fri, 06 Aug 2021 22:04:22 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7635ae9ae7b01f3f897bee725eb55f2ee4ea71056d85205467700b3d753efc`  
		Last Modified: Fri, 06 Aug 2021 22:04:22 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0fda02651f5e453d45eb45729d259cd03db6a9488a0ff720b7f6f1d0e20b76`  
		Last Modified: Fri, 27 Aug 2021 02:30:15 GMT  
		Size: 10.7 MB (10722816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0fbd129723acb534ea646173575be2513cb8875b47fa3ae87a3a35eb3f0da2`  
		Last Modified: Fri, 27 Aug 2021 02:30:10 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66759d16d0a0ea087b661b719cbad223bf47060a18f46802862424dd170d906c`  
		Last Modified: Fri, 27 Aug 2021 02:30:19 GMT  
		Size: 14.1 MB (14142034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc540cb69b76a91dd0a023d137ab7f9ef4e6cf4d8d58c7f374c32cfbc7705b71`  
		Last Modified: Fri, 27 Aug 2021 02:30:10 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48890522ff5afce8f01aeb5432172d5c332d9fdf4e3746903980c80658918c2`  
		Last Modified: Fri, 27 Aug 2021 02:30:10 GMT  
		Size: 17.8 KB (17839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5de227160695233429bfa13e08c2bc42a0260105380dd939019f4caf6d54d1d`  
		Last Modified: Fri, 27 Aug 2021 02:30:10 GMT  
		Size: 8.6 KB (8570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b861c0a696d740968a65109d6ab99971e4a4769d9e0d2f8c40f297b02d6e66b`  
		Last Modified: Fri, 27 Aug 2021 11:02:34 GMT  
		Size: 333.7 KB (333729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9aaf06abdf0bd2c0106405bf86df8af268c8192fc3a206a27b4ac927f43562`  
		Last Modified: Fri, 27 Aug 2021 11:02:32 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79874898b30c76e126e95dd3a518f6119d5b61f459cb087e57dcd8ef6f0ed524`  
		Last Modified: Fri, 27 Aug 2021 11:02:32 GMT  
		Size: 414.8 KB (414809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb9959a029bbcc05c79d5cef62924373e15f03295946c9299f1a96dcabf3fa9`  
		Last Modified: Fri, 27 Aug 2021 11:02:34 GMT  
		Size: 2.6 MB (2572156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fa92177a9eefd9b2ff1c72b72bf98a8d633c33d5d136a2dc1ee8a423110b16`  
		Last Modified: Fri, 27 Aug 2021 11:02:32 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67525b7712bcc6d2bf16f2d1e586d6369262925bb219f218cf360bab8fa74f14`  
		Last Modified: Fri, 27 Aug 2021 11:02:32 GMT  
		Size: 2.0 KB (2042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:fdced666bbb9ed1f203b8003a681b6c59b8e0fc4fab2131de12f750373cbb22b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34588884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88dc0ae11b999056a38a8693b8d7484b01686ffa5495d6f5b8e42ad980bd8c3f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Aug 2021 17:39:26 GMT
ADD file:1a8fd1066485e1261462e689c1a072f010c1d3be904b73ef2b84128fac652951 in / 
# Fri, 06 Aug 2021 17:39:27 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 22:13:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Aug 2021 22:13:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 06 Aug 2021 22:13:46 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Aug 2021 22:13:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Aug 2021 22:13:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 06 Aug 2021 22:21:12 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 06 Aug 2021 22:21:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 22:21:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 22:21:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Aug 2021 22:34:42 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 27 Aug 2021 00:19:33 GMT
ENV PHP_VERSION=8.0.10
# Fri, 27 Aug 2021 00:19:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.10.tar.xz.asc
# Fri, 27 Aug 2021 00:19:33 GMT
ENV PHP_SHA256=66dc4d1bc86d9c1bc255b51b79d337ed1a7a035cf71230daabbf9a4ca35795eb
# Fri, 27 Aug 2021 00:19:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 27 Aug 2021 00:19:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Aug 2021 00:24:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Aug 2021 00:24:30 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 27 Aug 2021 00:24:31 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Aug 2021 00:24:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Aug 2021 00:24:32 GMT
WORKDIR /var/www/html
# Fri, 27 Aug 2021 00:24:32 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 27 Aug 2021 00:24:32 GMT
STOPSIGNAL SIGQUIT
# Fri, 27 Aug 2021 00:24:33 GMT
EXPOSE 9000
# Fri, 27 Aug 2021 00:24:33 GMT
CMD ["php-fpm"]
# Fri, 27 Aug 2021 04:56:50 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Fri, 27 Aug 2021 04:56:51 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 27 Aug 2021 04:56:53 GMT
RUN apk add --no-cache bash
# Fri, 27 Aug 2021 04:56:53 GMT
ENV YOURLS_VERSION=1.8.1
# Fri, 27 Aug 2021 04:56:53 GMT
ENV YOURLS_SHA256=92b0666af3e3ad4a783e78cba93687e9a24acf216606a6d457819c5d36d2cfe4
# Fri, 27 Aug 2021 04:56:54 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 27 Aug 2021 04:56:54 GMT
COPY file:7bfc5a435dd9f76b0c1d23545b13f25bad15f4271d687c1a76bb5d10a41af1eb in /usr/local/bin/ 
# Fri, 27 Aug 2021 04:56:54 GMT
COPY file:0bcfdfe0566007e7477c55552a1341b82b958e95879a5314f411d2188da2429e in /usr/src/yourls/user/ 
# Fri, 27 Aug 2021 04:56:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Aug 2021 04:56:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:fd3acdcea5682abced546ec19fb6ebee725c5184e5d91614c469c0a79e67f2d0`  
		Last Modified: Fri, 06 Aug 2021 17:40:12 GMT  
		Size: 2.7 MB (2710613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e75c04557b83c6887fa33eb52320a5c1afed1d1b8299d3accdf27cea6b5860`  
		Last Modified: Fri, 06 Aug 2021 23:19:35 GMT  
		Size: 1.7 MB (1710420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6439bb8bd6ba02680eef64ad51b996399f05a740cd7ab8e62834b24527f60c`  
		Last Modified: Fri, 06 Aug 2021 23:19:35 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d61d6c7061c67dabfce2227dc9665b59eb7c43fd2f927c11e7c76446b50fed3`  
		Last Modified: Fri, 06 Aug 2021 23:19:35 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8869871e3a4f623c33497c5c93a9803ae5d14804d38d1b433fca72d44f5f269`  
		Last Modified: Fri, 27 Aug 2021 02:46:22 GMT  
		Size: 10.7 MB (10722817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbc3e119bb6796df36d2aa3ac161891039537062a9072bd91c132340d9df26e`  
		Last Modified: Fri, 27 Aug 2021 02:46:18 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2e97ca7815508aca03a65d11d93033ecb6abab40d873332491684c9699b286`  
		Last Modified: Fri, 27 Aug 2021 02:46:21 GMT  
		Size: 16.0 MB (15995022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8c2fe629348bb073ef656c6fcd42d5119335d9adc1d19b7ad5815bfd3ec6a0`  
		Last Modified: Fri, 27 Aug 2021 02:46:18 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832b396f98cfb79b4b1f95731d69c482ff72bdf60518b8836b8e7c65da121351`  
		Last Modified: Fri, 27 Aug 2021 02:46:18 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb66bf1e406a8e6fe6ccbde3e3d93450fd7874123a4355cb37eb4a7c8171de45`  
		Last Modified: Fri, 27 Aug 2021 02:46:18 GMT  
		Size: 8.6 KB (8571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f461955d04c2dba539b554947ba559d1e384d9e60ef3a2d127690026e7b14128`  
		Last Modified: Fri, 27 Aug 2021 04:58:50 GMT  
		Size: 369.6 KB (369645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a906623ec486c33af89bece97772fa96be6d3aa12566e413ca6be7dd745587bb`  
		Last Modified: Fri, 27 Aug 2021 04:58:47 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f42218798544693fa3f5cfd6f18edb17584547c249c95e61fa7a1f798e0b0fd1`  
		Last Modified: Fri, 27 Aug 2021 04:58:46 GMT  
		Size: 474.0 KB (473951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5406a9d5960cc0dbc63756d5f0e70938791a837963dce1d9add0a68fecd507b`  
		Last Modified: Fri, 27 Aug 2021 04:58:47 GMT  
		Size: 2.6 MB (2572157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4cefd6bcd1558402a67c3c31db3c9a66fe3c84f31c1d57376e2f596899f2f29`  
		Last Modified: Fri, 27 Aug 2021 04:58:46 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21325059eda6be30c52d81969459b10a764cbd8c300aae209e764120b608582`  
		Last Modified: Fri, 27 Aug 2021 04:58:46 GMT  
		Size: 2.0 KB (2035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm-alpine` - linux; 386

```console
$ docker pull yourls@sha256:03fcfb24a27f3338636df18a1c158cc1f03dc2742fb1e4ca76b2c22796f14417
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34592640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e06064a3271c357d3d720f826630b86cb2660442a2224c34b6cbc1ad4c176bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 27 Aug 2021 17:38:29 GMT
ADD file:42a7bc5a08b546b47049dd0f89ae4e7a8c86342f87000f39ade3ff52916a6c2e in / 
# Fri, 27 Aug 2021 17:38:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 19:59:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 19:59:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 19:59:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 19:59:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 19:59:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 20:10:36 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 27 Aug 2021 20:10:37 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 20:10:37 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 20:10:37 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 20:29:52 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 27 Aug 2021 20:29:52 GMT
ENV PHP_VERSION=8.0.10
# Fri, 27 Aug 2021 20:29:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.10.tar.xz.asc
# Fri, 27 Aug 2021 20:29:52 GMT
ENV PHP_SHA256=66dc4d1bc86d9c1bc255b51b79d337ed1a7a035cf71230daabbf9a4ca35795eb
# Fri, 27 Aug 2021 20:29:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 27 Aug 2021 20:30:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Aug 2021 20:37:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Aug 2021 20:37:19 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 27 Aug 2021 20:37:20 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Aug 2021 20:37:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Aug 2021 20:37:21 GMT
WORKDIR /var/www/html
# Fri, 27 Aug 2021 20:37:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 27 Aug 2021 20:37:22 GMT
STOPSIGNAL SIGQUIT
# Fri, 27 Aug 2021 20:37:22 GMT
EXPOSE 9000
# Fri, 27 Aug 2021 20:37:22 GMT
CMD ["php-fpm"]
# Sat, 28 Aug 2021 02:31:01 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Sat, 28 Aug 2021 02:31:02 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 28 Aug 2021 02:31:03 GMT
RUN apk add --no-cache bash
# Sat, 28 Aug 2021 02:31:04 GMT
ENV YOURLS_VERSION=1.8.1
# Sat, 28 Aug 2021 02:31:04 GMT
ENV YOURLS_SHA256=92b0666af3e3ad4a783e78cba93687e9a24acf216606a6d457819c5d36d2cfe4
# Sat, 28 Aug 2021 02:31:06 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Sat, 28 Aug 2021 02:31:06 GMT
COPY file:7bfc5a435dd9f76b0c1d23545b13f25bad15f4271d687c1a76bb5d10a41af1eb in /usr/local/bin/ 
# Sat, 28 Aug 2021 02:31:06 GMT
COPY file:0bcfdfe0566007e7477c55552a1341b82b958e95879a5314f411d2188da2429e in /usr/src/yourls/user/ 
# Sat, 28 Aug 2021 02:31:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Aug 2021 02:31:07 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b11ae9fc5d8a106cfed3a6f6c75e5b5b5797c566fac4411622b4055df6541286`  
		Last Modified: Fri, 27 Aug 2021 17:39:18 GMT  
		Size: 2.8 MB (2822857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa6b193871895593dd2e9300b768212b024272930161ab8524f40a5735edd63`  
		Last Modified: Fri, 27 Aug 2021 21:44:10 GMT  
		Size: 1.8 MB (1805371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f324621ef2d45fa9d97583b1efc3fb241066b4dbf696e2dd38327a90d1e6813`  
		Last Modified: Fri, 27 Aug 2021 21:44:09 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d22e796392b3e282fea08fa6cb0da352053587b646a938425cb7c4171bf25a2`  
		Last Modified: Fri, 27 Aug 2021 21:44:09 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1f0691b35abc3e1cc0a213f15db883a1934075fe48465c1b96a18f72d39dd7`  
		Last Modified: Fri, 27 Aug 2021 21:48:09 GMT  
		Size: 10.7 MB (10722798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3f90f20de6e799b57fb3490bcee5db23cbf37ce1479f0856171f38597e839c`  
		Last Modified: Fri, 27 Aug 2021 21:48:05 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc166f47eddc24897eae8f431522de273f8bc62f88565ccd6defd1276fc54adb`  
		Last Modified: Fri, 27 Aug 2021 21:48:10 GMT  
		Size: 15.4 MB (15428112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4bfb05604335668ab061d83b90fb7fefbb43a939e2b6e1a1911f57ed336cede`  
		Last Modified: Fri, 27 Aug 2021 21:48:05 GMT  
		Size: 2.3 KB (2269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072c39e7c5738ea8f19930d2c98a7a91c1666468b5be8618e6db3ea5fd7e66aa`  
		Last Modified: Fri, 27 Aug 2021 21:48:05 GMT  
		Size: 17.8 KB (17794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e14b0de3b7bd0bda154b235d679b4ee43957d5971cf4a561e4a3ec52a88eec`  
		Last Modified: Fri, 27 Aug 2021 21:48:05 GMT  
		Size: 8.6 KB (8570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea5718c0425bfb8ca1cef95aa9d06d77be99cb092343ca47ebf73cb30551756`  
		Last Modified: Sat, 28 Aug 2021 02:32:11 GMT  
		Size: 705.5 KB (705482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b72baa40255376e3d9620c6a647d6c4888b51b4336f88bc704330821bcd9540`  
		Last Modified: Sat, 28 Aug 2021 02:32:08 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caa238435ad6e8215f5c964180db41b4f4e6befc23edb6a54dbe2152d765a89`  
		Last Modified: Sat, 28 Aug 2021 02:32:09 GMT  
		Size: 501.7 KB (501658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b214ceb6856e973d112f17a8fe521a6389de623ed9315c487ebf84c49daf17f4`  
		Last Modified: Sat, 28 Aug 2021 02:32:09 GMT  
		Size: 2.6 MB (2572155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba560311877f8c8f8ce5f230d0140927ab2ca32255ebe661bd5ceb66bc936f6e`  
		Last Modified: Sat, 28 Aug 2021 02:32:08 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb44d519289070854fbab6667dd948ef4b28d5e33a89d7713babb945453175ff`  
		Last Modified: Sat, 28 Aug 2021 02:32:08 GMT  
		Size: 2.0 KB (2038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm-alpine` - linux; ppc64le

```console
$ docker pull yourls@sha256:27ccc450b0eb63f3726ae8765695e24b593769f26a6d590b0271d26264cf4cca
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36200698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa730fcc53e2ce7e07bed977f4c0810db8c16c93c5107c94691e80163c8d7df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Aug 2021 18:28:28 GMT
ADD file:40f3b617d7ff269d92f0ffcf8aad561b5f2c0626ef519a7f584f1ba0182b3188 in / 
# Fri, 06 Aug 2021 18:28:35 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 23:16:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Aug 2021 23:17:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 06 Aug 2021 23:17:20 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Aug 2021 23:17:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Aug 2021 23:17:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 06 Aug 2021 23:23:44 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 06 Aug 2021 23:23:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 23:23:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 23:23:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Aug 2021 23:37:32 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 27 Aug 2021 03:04:39 GMT
ENV PHP_VERSION=8.0.10
# Fri, 27 Aug 2021 03:04:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.10.tar.xz.asc
# Fri, 27 Aug 2021 03:05:05 GMT
ENV PHP_SHA256=66dc4d1bc86d9c1bc255b51b79d337ed1a7a035cf71230daabbf9a4ca35795eb
# Fri, 27 Aug 2021 03:05:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 27 Aug 2021 03:05:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Aug 2021 03:10:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Aug 2021 03:10:57 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 27 Aug 2021 03:11:08 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Aug 2021 03:11:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Aug 2021 03:11:20 GMT
WORKDIR /var/www/html
# Fri, 27 Aug 2021 03:11:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 27 Aug 2021 03:11:46 GMT
STOPSIGNAL SIGQUIT
# Fri, 27 Aug 2021 03:11:57 GMT
EXPOSE 9000
# Fri, 27 Aug 2021 03:12:03 GMT
CMD ["php-fpm"]
# Fri, 27 Aug 2021 19:16:29 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Fri, 27 Aug 2021 19:16:43 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 27 Aug 2021 19:16:58 GMT
RUN apk add --no-cache bash
# Fri, 27 Aug 2021 19:17:04 GMT
ENV YOURLS_VERSION=1.8.1
# Fri, 27 Aug 2021 19:17:08 GMT
ENV YOURLS_SHA256=92b0666af3e3ad4a783e78cba93687e9a24acf216606a6d457819c5d36d2cfe4
# Fri, 27 Aug 2021 19:17:21 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 27 Aug 2021 19:17:22 GMT
COPY file:7bfc5a435dd9f76b0c1d23545b13f25bad15f4271d687c1a76bb5d10a41af1eb in /usr/local/bin/ 
# Fri, 27 Aug 2021 19:17:24 GMT
COPY file:0bcfdfe0566007e7477c55552a1341b82b958e95879a5314f411d2188da2429e in /usr/src/yourls/user/ 
# Fri, 27 Aug 2021 19:17:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Aug 2021 19:17:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:0ff902055236f70c4694c806877243e1dd52c513825a2a3ecc7eba8f5202acc8`  
		Last Modified: Fri, 06 Aug 2021 18:29:33 GMT  
		Size: 2.8 MB (2811152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6ff25f38da82eae5b2405214e57c7c39a03ddb9e5eb9d04b31edf4dcc07669`  
		Last Modified: Sat, 07 Aug 2021 00:29:55 GMT  
		Size: 1.8 MB (1753673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af333e5ee6f8ffe8b982f0c46d826dbc17bbc35803e4c60443beea3af1ab1bc`  
		Last Modified: Sat, 07 Aug 2021 00:29:54 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c80d5e8e81136737bd0d714e4bbecc9480689bf7e1faf489f1ad332150d992`  
		Last Modified: Sat, 07 Aug 2021 00:29:54 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76b7dcc586028933e6c31f68a97265aee453d1241fdfcbcc545f4e30e322fd5`  
		Last Modified: Fri, 27 Aug 2021 07:55:02 GMT  
		Size: 10.7 MB (10722820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659e9ca6bef6767736c8b8e402df2321067a797e296064674d49b524d40e4fd2`  
		Last Modified: Fri, 27 Aug 2021 07:54:57 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28cd322056cd935aa45f71880c0a0014353c60d4b10ab7c7742663c5ae119188`  
		Last Modified: Fri, 27 Aug 2021 07:55:10 GMT  
		Size: 17.4 MB (17354011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8bbfb712b4a06ebb92b5aae1cb9b5d8e5e9c7d53066b788f9e4254a9f9f4412`  
		Last Modified: Fri, 27 Aug 2021 07:54:57 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2506b36282aa8eae613537a0fd8baf95f98cf032594b424a17d475d8d127222e`  
		Last Modified: Fri, 27 Aug 2021 07:54:57 GMT  
		Size: 17.8 KB (17848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fddca9f0567fd79e0452ff7680683bed8485cd95cac98e0c01b0ca66fff00def`  
		Last Modified: Fri, 27 Aug 2021 07:54:57 GMT  
		Size: 8.6 KB (8571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b4c61788b1c867e9f4ac728c563697c18d72b230a2c397a328e5b0aab9775ae`  
		Last Modified: Fri, 27 Aug 2021 19:19:27 GMT  
		Size: 422.9 KB (422908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd24d475aa6b6ef83f757f9184bec3328dcfa98ad212e79e012ddbdb0ca2142`  
		Last Modified: Fri, 27 Aug 2021 19:19:22 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1a757113c7fc8f65c5d9def549c43a0ce3adb1ceeeb67fd584e14083661447`  
		Last Modified: Fri, 27 Aug 2021 19:19:23 GMT  
		Size: 529.7 KB (529705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b28cfbd5ea1deb6bbc45e44a7ead696bb25dc97863ad0250f9deebd6d298c7`  
		Last Modified: Fri, 27 Aug 2021 19:19:23 GMT  
		Size: 2.6 MB (2572156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4318ce38871a0cbd47c6e63e896bc9cf4f0ac5fa511a25048df12ffbf3d30d86`  
		Last Modified: Fri, 27 Aug 2021 19:19:22 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfb1f4dad6ef891aed8fbca8bcb9086e90ad1351b50e5cdc3d4a717137497c9`  
		Last Modified: Fri, 27 Aug 2021 19:19:23 GMT  
		Size: 2.0 KB (2044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm-alpine` - linux; s390x

```console
$ docker pull yourls@sha256:3748bcde65a5f83f4ef1fcd8573734d4d1879d8b7cee80e71cee41e169b43f76
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34006097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67069ada0da52391e8f5829c9c971cb8f3eda7c81e83ebbd121771a7c69c0709`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Aug 2021 17:41:30 GMT
ADD file:bdf19d63e9f8600d2fbe02435279b8df06fbcb5105e6b8eea778d8ef928e219a in / 
# Fri, 06 Aug 2021 17:41:31 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:04:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Aug 2021 19:04:44 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 06 Aug 2021 19:04:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Aug 2021 19:04:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Aug 2021 19:04:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 06 Aug 2021 19:08:03 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 06 Aug 2021 19:08:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 19:08:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 19:08:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Aug 2021 19:15:41 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 26 Aug 2021 20:47:38 GMT
ENV PHP_VERSION=8.0.10
# Thu, 26 Aug 2021 20:47:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.10.tar.xz.asc
# Thu, 26 Aug 2021 20:47:39 GMT
ENV PHP_SHA256=66dc4d1bc86d9c1bc255b51b79d337ed1a7a035cf71230daabbf9a4ca35795eb
# Thu, 26 Aug 2021 20:47:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Aug 2021 20:47:51 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Aug 2021 20:53:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 26 Aug 2021 20:53:33 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Thu, 26 Aug 2021 20:53:35 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Aug 2021 20:53:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Aug 2021 20:53:37 GMT
WORKDIR /var/www/html
# Thu, 26 Aug 2021 20:53:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 26 Aug 2021 20:53:39 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Aug 2021 20:53:40 GMT
EXPOSE 9000
# Thu, 26 Aug 2021 20:53:41 GMT
CMD ["php-fpm"]
# Fri, 27 Aug 2021 05:38:38 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Fri, 27 Aug 2021 05:38:39 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 27 Aug 2021 05:38:41 GMT
RUN apk add --no-cache bash
# Fri, 27 Aug 2021 05:38:42 GMT
ENV YOURLS_VERSION=1.8.1
# Fri, 27 Aug 2021 05:38:42 GMT
ENV YOURLS_SHA256=92b0666af3e3ad4a783e78cba93687e9a24acf216606a6d457819c5d36d2cfe4
# Fri, 27 Aug 2021 05:38:44 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 27 Aug 2021 05:38:45 GMT
COPY file:7bfc5a435dd9f76b0c1d23545b13f25bad15f4271d687c1a76bb5d10a41af1eb in /usr/local/bin/ 
# Fri, 27 Aug 2021 05:38:45 GMT
COPY file:0bcfdfe0566007e7477c55552a1341b82b958e95879a5314f411d2188da2429e in /usr/src/yourls/user/ 
# Fri, 27 Aug 2021 05:38:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Aug 2021 05:38:45 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:625f57562315453466f73bc9d8c96e678f8d4ea436b462d06c60fb217c6b3d38`  
		Last Modified: Fri, 06 Aug 2021 17:42:42 GMT  
		Size: 2.6 MB (2602036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2568987867095245025c394f06456a47a6c8bdaa6c96639c49ddb43f6bff047`  
		Last Modified: Fri, 20 Aug 2021 19:50:42 GMT  
		Size: 1.8 MB (1768133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd26dcb760c8a12fd1e292df471c9fde4aba0c4c70b845397a1dfe2e434b942b`  
		Last Modified: Fri, 20 Aug 2021 19:50:41 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba8a5b372f3024025b5c742c3ac12e1b59f6c09600dbc45c2ce807f5dfa3935`  
		Last Modified: Fri, 20 Aug 2021 19:50:41 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0dd5240e3926bc4376a4abeb1cd5614d69fb5f13d64d638ba929d9a5e7a2b8`  
		Last Modified: Fri, 27 Aug 2021 00:18:11 GMT  
		Size: 10.7 MB (10722821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b124272020843e82da131abfd0dbf0d982333664a33041bdf0abc5dd4b210d39`  
		Last Modified: Fri, 27 Aug 2021 00:18:09 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9e89a6d464e909f61c7dbfd616992727196b36e6302bdd1365990ef59cfafb`  
		Last Modified: Fri, 27 Aug 2021 00:18:11 GMT  
		Size: 15.4 MB (15448127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6820b556b48a57108dfcdaa7cb35e692a919f71ec59c79a6a9fa9d6266140b9`  
		Last Modified: Fri, 27 Aug 2021 00:18:09 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061e9c7fdda62e0c2671d0846ffdf6ac0ccfca89a00c7089fae0562df07a652e`  
		Last Modified: Fri, 27 Aug 2021 00:18:09 GMT  
		Size: 17.9 KB (17863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458465d852d65120354bbfb87a991595dfe75e8eefaa77d2770b58dadeec225e`  
		Last Modified: Fri, 27 Aug 2021 00:18:09 GMT  
		Size: 8.6 KB (8572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62860f86326e8db56eae86a498f3a17d1d1d6a7ee2177552c9008ebe2d53e6e`  
		Last Modified: Fri, 27 Aug 2021 05:40:17 GMT  
		Size: 375.8 KB (375774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f9a34d99159348bcdf69bac66ae13f394c3100c23723e7cbdfa2b861be3836`  
		Last Modified: Fri, 27 Aug 2021 05:40:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c5467377e56068a1a340d32fc9a818ffedff9ccf9f93e9318726bd7a733a14`  
		Last Modified: Fri, 27 Aug 2021 05:40:15 GMT  
		Size: 482.8 KB (482774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29009017b8eeebf115b2ab6f9392120ee8efdf5a3ee787a09860222586217e80`  
		Last Modified: Fri, 27 Aug 2021 05:40:15 GMT  
		Size: 2.6 MB (2572161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1074aaff1e9a1af63ee48657776b748152ecc65963e80c65a9d6f9f1247ff96`  
		Last Modified: Fri, 27 Aug 2021 05:40:15 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e14314c51ccb727d80bda343a6bcf67d94e0ae3f33411a99d3abb2f389faebe2`  
		Last Modified: Fri, 27 Aug 2021 05:40:15 GMT  
		Size: 2.0 KB (2037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
