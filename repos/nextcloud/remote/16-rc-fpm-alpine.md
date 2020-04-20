## `nextcloud:16-rc-fpm-alpine`

```console
$ docker pull nextcloud@sha256:75b0aad44efbd1caec48e2b7b9fe7c3e547eabe55a2046ba152ab4459d5bf1cd
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

### `nextcloud:16-rc-fpm-alpine` - linux; amd64

```console
$ docker pull nextcloud@sha256:5569c7b561d29b53f54f4be03126aeab595bef26bb42da01984d8b1202f36658
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125898856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f21b07f378b8554d3abf1a5cdb12c2ed2813ab595d7426fbb4355cb92bf1e34`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:18:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 18 Jan 2020 03:18:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 18 Jan 2020 03:18:29 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 18 Jan 2020 03:18:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 18 Jan 2020 03:18:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 18 Jan 2020 03:23:43 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 18 Jan 2020 03:23:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:23:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:23:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:40:28 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 20 Feb 2020 23:45:16 GMT
ENV PHP_VERSION=7.3.15
# Thu, 20 Feb 2020 23:45:16 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.15.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.15.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 23:45:16 GMT
ENV PHP_SHA256=de7ae7cf3d1dbb2824975b26b32991dac2b732886ec22075b8c53b261b018166 PHP_MD5=
# Thu, 20 Feb 2020 23:45:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Feb 2020 23:45:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 23:53:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 23:53:31 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 20 Feb 2020 23:53:33 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 23:53:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 23:53:33 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 23:53:35 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 20 Feb 2020 23:53:35 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Feb 2020 23:53:35 GMT
EXPOSE 9000
# Thu, 20 Feb 2020 23:53:35 GMT
CMD ["php-fpm"]
# Fri, 21 Feb 2020 05:21:01 GMT
RUN set -ex;         apk add --no-cache         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/15 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 21 Feb 2020 05:23:28 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         icu-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libpng-dev         libmemcached-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev         imagemagick-dev         libwebp-dev         gmp-dev     ;         docker-php-ext-configure gd --with-freetype-dir=/usr --with-png-dir=/usr --with-jpeg-dir=/usr --with-webp-dir=/usr;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-4.3.0;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --virtual .nextcloud-phpext-rundeps $runDeps;     apk del .build-deps
# Fri, 21 Feb 2020 05:23:29 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 21 Feb 2020 05:23:29 GMT
VOLUME [/var/www/html]
# Tue, 10 Mar 2020 00:39:30 GMT
ENV NEXTCLOUD_VERSION=16.0.9RC2
# Tue, 10 Mar 2020 00:39:48 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/prereleases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/prereleases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm -r "$GNUPGHOME" nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del .fetch-deps
# Tue, 10 Mar 2020 00:39:49 GMT
COPY multi:4c0d5f2638534e3802f1f41694007dfeea41bc4977afff5103eb396d3c7ab26b in / 
# Tue, 10 Mar 2020 00:39:49 GMT
COPY multi:07fbadbda22b19b1f9b8cfc5e833b697afbaa1e602ffea77b26286f5899f86d6 in /usr/src/nextcloud/config/ 
# Tue, 10 Mar 2020 00:39:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 10 Mar 2020 00:39:50 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c0a1817becf025301783a94fa11de700972e7d7c117ca7e45d080db0ec1a11`  
		Last Modified: Sat, 18 Jan 2020 04:09:35 GMT  
		Size: 1.4 MB (1354634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd5b3ea1fc31791c18f464b5b95dd3d9b8ff97aef4b64e0202f3da7f5550e80`  
		Last Modified: Sat, 18 Jan 2020 04:09:35 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db87396003bdeb76e6e367a5ae26be9642a89986dcda71b3491412c579cb6859`  
		Last Modified: Sat, 18 Jan 2020 04:09:35 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09a455666b3c26ab0e931207aa730d446e80c0a98a10ba411bd9aef2142d6b9`  
		Last Modified: Fri, 21 Feb 2020 02:32:07 GMT  
		Size: 12.1 MB (12131097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a989a7fc7b60166ec2cb9b1d45bde2be6ec4e3579395718c12d2dbd05a0981`  
		Last Modified: Fri, 21 Feb 2020 02:32:05 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b308a8c0d759c0e45a1b6fa290961911f84a02dd2ac90777b7f43ce69c31fa`  
		Last Modified: Fri, 21 Feb 2020 02:32:09 GMT  
		Size: 14.9 MB (14896617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352857664b099deb3d47d0aa1763e71736a7af26cd7d5da5087ceea451a9de5c`  
		Last Modified: Fri, 21 Feb 2020 02:32:05 GMT  
		Size: 2.2 KB (2214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299d966decb7882ffdf473f77aa5ca0138a01a72caf0cbab6b9306a30155328e`  
		Last Modified: Fri, 21 Feb 2020 02:32:05 GMT  
		Size: 72.9 KB (72932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50ac619e43d6d98e0be7867edcfaf2a263e21524e7b8b7fe0b953a04cbe5df2`  
		Last Modified: Fri, 21 Feb 2020 02:32:05 GMT  
		Size: 8.4 KB (8412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed41b3b29c7b615387861430ce772f2ec691b6d3fda4e4ac77c733ac97dca971`  
		Last Modified: Fri, 21 Feb 2020 05:41:09 GMT  
		Size: 315.8 KB (315809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8040ff23eef5e3f15ed1eff9775a852b6c5498b3cef82599252443cfa5efdc1f`  
		Last Modified: Fri, 21 Feb 2020 05:41:14 GMT  
		Size: 25.7 MB (25654415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db8540d8d98b0abf1e103ee217767f71bdf36e9f11c4aed4fb7a1a059def7cb5`  
		Last Modified: Fri, 21 Feb 2020 05:41:08 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e9e789e831f68ffd8c74f6c0dfc5d0e5a9642843017da3341fc928563b2c47`  
		Last Modified: Tue, 10 Mar 2020 00:45:48 GMT  
		Size: 68.7 MB (68654040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c897c79f8065e439c845c08575e2546846d54b0f0e8795f2af6d6407514409c3`  
		Last Modified: Tue, 10 Mar 2020 00:45:36 GMT  
		Size: 2.2 KB (2161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1cf56d36178f817cb12ec7367c65aed1a7c0cacb642fefefbf69feac4abf56`  
		Last Modified: Tue, 10 Mar 2020 00:45:36 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:16-rc-fpm-alpine` - linux; arm variant v6

```console
$ docker pull nextcloud@sha256:9c474b420459f1802bbe6a2f31f27f25ebf0a8e0905e809cd2413785596129cf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123839578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c30aaea8a4026d16fca8f44f149876e82d7c14e58bf96988ac00fd7349eb43a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 02:16:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 24 Mar 2020 02:16:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 24 Mar 2020 02:16:47 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 24 Mar 2020 02:16:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Mar 2020 02:16:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 24 Mar 2020 02:21:00 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Tue, 24 Mar 2020 02:21:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Mar 2020 02:21:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Apr 2020 07:54:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Apr 2020 08:19:55 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 17 Apr 2020 08:19:56 GMT
ENV PHP_VERSION=7.3.17
# Fri, 17 Apr 2020 08:19:58 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.17.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.17.tar.xz.asc/from/this/mirror
# Fri, 17 Apr 2020 08:19:59 GMT
ENV PHP_SHA256=6a30304c27f7e7a94538f5ffec599f600ee93aedbbecad8aa4f8bec539b10ad8 PHP_MD5=
# Fri, 17 Apr 2020 08:20:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 17 Apr 2020 08:20:05 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 17 Apr 2020 08:24:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 17 Apr 2020 08:24:41 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 17 Apr 2020 08:24:44 GMT
RUN docker-php-ext-enable sodium
# Fri, 17 Apr 2020 08:24:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Apr 2020 08:24:46 GMT
WORKDIR /var/www/html
# Fri, 17 Apr 2020 08:24:49 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 17 Apr 2020 08:24:50 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Apr 2020 08:24:51 GMT
EXPOSE 9000
# Fri, 17 Apr 2020 08:24:52 GMT
CMD ["php-fpm"]
# Fri, 17 Apr 2020 10:01:58 GMT
RUN set -ex;         apk add --no-cache         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/15 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 17 Apr 2020 10:06:03 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         icu-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libpng-dev         libmemcached-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev         imagemagick-dev         libwebp-dev         gmp-dev     ;         docker-php-ext-configure gd --with-freetype-dir=/usr --with-png-dir=/usr --with-jpeg-dir=/usr --with-webp-dir=/usr;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-4.3.0;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --virtual .nextcloud-phpext-rundeps $runDeps;     apk del .build-deps
# Fri, 17 Apr 2020 10:06:08 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 17 Apr 2020 10:06:09 GMT
VOLUME [/var/www/html]
# Mon, 20 Apr 2020 16:49:40 GMT
ENV NEXTCLOUD_VERSION=16.0.10RC1
# Mon, 20 Apr 2020 16:50:21 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/prereleases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/prereleases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm -r "$GNUPGHOME" nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del .fetch-deps
# Mon, 20 Apr 2020 16:50:24 GMT
COPY multi:57de70033920dd582f0dbb812d28f0cfdcf6a102d5b4374faf9435d87a0a7585 in / 
# Mon, 20 Apr 2020 16:50:27 GMT
COPY multi:965c5cb843579fcde0cf3c9edb975639cbd2d55de5f645b1061d46855979394d in /usr/src/nextcloud/config/ 
# Mon, 20 Apr 2020 16:50:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Apr 2020 16:50:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ea08e138832a1357c5a2058da55929de016d0715372ec90df8716d8f08e8aa`  
		Last Modified: Tue, 24 Mar 2020 02:56:26 GMT  
		Size: 1.3 MB (1321096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6155177d2f4f58391e952733581935ca259371ca891a8e72311ff15a4b0caaf9`  
		Last Modified: Tue, 24 Mar 2020 02:56:26 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64588fb2e6842997faa53e9e5d4ec63be60ac226be4ae2eb5a97bff62263b14e`  
		Last Modified: Tue, 24 Mar 2020 02:56:25 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1e22c941fed10dda4f6e3c4f8b6e9d55e29ce45080418fb347f08d0c2f6112`  
		Last Modified: Fri, 17 Apr 2020 09:10:03 GMT  
		Size: 12.1 MB (12135772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc4d76aee69a60b1cfbb344726523fabe9ff89c78450425d89ece7b716adaef`  
		Last Modified: Fri, 17 Apr 2020 09:09:58 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eaddbf34589de5e574d16732b3f7a3814d7eaaaa20759685eebea1ce9cb4cac`  
		Last Modified: Fri, 17 Apr 2020 09:10:03 GMT  
		Size: 13.4 MB (13404311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d60fc00584a963b5e68f6bbb66592f5e4700fbf9072aa1037e54b0d8b2bea9`  
		Last Modified: Fri, 17 Apr 2020 09:09:58 GMT  
		Size: 2.2 KB (2214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ba9f57ea34cd1c5056f766f92c0bcf8927a9bead599b9ca33ce1cca78c91c8`  
		Last Modified: Fri, 17 Apr 2020 09:09:59 GMT  
		Size: 17.1 KB (17060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d7e18de761d3f9a690a2e1e346d20e6a6378e74b75290b43cbb44106edb585`  
		Last Modified: Fri, 17 Apr 2020 09:09:58 GMT  
		Size: 8.4 KB (8412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:058f4ddd1529f5636df6245857b6603848434b8d718ab5b26a90ba862b2a9673`  
		Last Modified: Fri, 17 Apr 2020 10:21:47 GMT  
		Size: 268.8 KB (268776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0c41c9ae2bf6057a147de931d81fb36316e5d83a65e3bf653646efcf46c3ab`  
		Last Modified: Fri, 17 Apr 2020 10:21:53 GMT  
		Size: 24.8 MB (24779900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9c7eee6de7d99841449d75114383a7d7c050512dbb2d9000284d067a95600e`  
		Last Modified: Fri, 17 Apr 2020 10:21:45 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c867a979aa8e66f7ac22ed0b44498a8eafa5a60d32a30b9b63b6aa43fbc34aa`  
		Last Modified: Mon, 20 Apr 2020 16:55:19 GMT  
		Size: 69.3 MB (69276989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef2807bd732f3d843c3a4c5638f2c70b23542f64f1f4f07f88d03d06b93471e`  
		Last Modified: Mon, 20 Apr 2020 16:54:58 GMT  
		Size: 2.6 KB (2553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f18645c4925c5b44a713c415880a9f11ac2ebf1b5293aa7a404fbf9abf6718`  
		Last Modified: Mon, 20 Apr 2020 16:54:59 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:16-rc-fpm-alpine` - linux; arm variant v7

```console
$ docker pull nextcloud@sha256:60ed27c28f0dce11ab861380aef074538f7fde3b3da867e94c4cb99509aad120
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (122007029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc848d745a6c0f0c819546c802ed1d7afe020f210b575e0a1a6b7ebe8de39f8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 01:36:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 24 Mar 2020 01:36:37 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 24 Mar 2020 01:36:39 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 24 Mar 2020 01:36:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Mar 2020 01:36:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 24 Mar 2020 01:39:39 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Tue, 24 Mar 2020 01:39:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Mar 2020 01:39:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Apr 2020 12:34:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Apr 2020 13:25:55 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 17 Apr 2020 13:25:56 GMT
ENV PHP_VERSION=7.3.17
# Fri, 17 Apr 2020 13:25:57 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.17.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.17.tar.xz.asc/from/this/mirror
# Fri, 17 Apr 2020 13:25:57 GMT
ENV PHP_SHA256=6a30304c27f7e7a94538f5ffec599f600ee93aedbbecad8aa4f8bec539b10ad8 PHP_MD5=
# Fri, 17 Apr 2020 13:26:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 17 Apr 2020 13:26:02 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 17 Apr 2020 13:28:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 17 Apr 2020 13:28:35 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 17 Apr 2020 13:28:37 GMT
RUN docker-php-ext-enable sodium
# Fri, 17 Apr 2020 13:28:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Apr 2020 13:28:39 GMT
WORKDIR /var/www/html
# Fri, 17 Apr 2020 13:28:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 17 Apr 2020 13:28:42 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Apr 2020 13:28:43 GMT
EXPOSE 9000
# Fri, 17 Apr 2020 13:28:43 GMT
CMD ["php-fpm"]
# Fri, 17 Apr 2020 15:33:08 GMT
RUN set -ex;         apk add --no-cache         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/15 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 17 Apr 2020 15:36:08 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         icu-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libpng-dev         libmemcached-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev         imagemagick-dev         libwebp-dev         gmp-dev     ;         docker-php-ext-configure gd --with-freetype-dir=/usr --with-png-dir=/usr --with-jpeg-dir=/usr --with-webp-dir=/usr;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-4.3.0;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --virtual .nextcloud-phpext-rundeps $runDeps;     apk del .build-deps
# Fri, 17 Apr 2020 15:36:11 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 17 Apr 2020 15:36:11 GMT
VOLUME [/var/www/html]
# Mon, 20 Apr 2020 17:06:02 GMT
ENV NEXTCLOUD_VERSION=16.0.10RC1
# Mon, 20 Apr 2020 17:07:07 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/prereleases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/prereleases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm -r "$GNUPGHOME" nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del .fetch-deps
# Mon, 20 Apr 2020 17:07:13 GMT
COPY multi:57de70033920dd582f0dbb812d28f0cfdcf6a102d5b4374faf9435d87a0a7585 in / 
# Mon, 20 Apr 2020 17:07:15 GMT
COPY multi:965c5cb843579fcde0cf3c9edb975639cbd2d55de5f645b1061d46855979394d in /usr/src/nextcloud/config/ 
# Mon, 20 Apr 2020 17:07:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Apr 2020 17:07:16 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221e0c8c991c3fdd8db1ec76c1a911aa0f946325ec2cf15d22a25693accc6edc`  
		Last Modified: Tue, 24 Mar 2020 02:07:16 GMT  
		Size: 1.2 MB (1227325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edeaee6722c9e078934e8f34fe0dc55d3f3c28d742e92ce6b3e86775beaeeb44`  
		Last Modified: Tue, 24 Mar 2020 02:07:16 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84528978bcc1c0fe1d795bbe412f0a4123fa9119c11c98cd9b1ab8c5db8203f0`  
		Last Modified: Tue, 24 Mar 2020 02:07:16 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb81d8a30d73db2e0c1b432b2857034607feb17929c39f8af2012f19e9334592`  
		Last Modified: Fri, 17 Apr 2020 14:42:29 GMT  
		Size: 12.1 MB (12135773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42cb4d19c6ac5828a78fb9798dfed0d22345644a23ee148aa4480743a66e4d9a`  
		Last Modified: Fri, 17 Apr 2020 14:42:25 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cbee0e07f0fbca5c1bd473fbcf9f8864b9ccc2de0a7c2191d2975d6039d5b0`  
		Last Modified: Fri, 17 Apr 2020 14:42:29 GMT  
		Size: 12.5 MB (12535660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c3e81e0f9856075f1fe9b48afff5843fcfa23fea819c7abd55853d6ac8dc5a`  
		Last Modified: Fri, 17 Apr 2020 14:42:25 GMT  
		Size: 2.2 KB (2218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4f0d806a3a251c829de8e63467122a9398d95066140c1c4a98faa69b1ce365`  
		Last Modified: Fri, 17 Apr 2020 14:42:26 GMT  
		Size: 17.0 KB (17046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd18261c5d1edf031ec19003d0026497670ebac38d0647160caeb9fed2987af1`  
		Last Modified: Fri, 17 Apr 2020 14:42:25 GMT  
		Size: 8.4 KB (8414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666a1050d46f2556ce6aad37c95ab12e2ac759db6c0b9cfa6bae0bb6245d1e5f`  
		Last Modified: Fri, 17 Apr 2020 16:23:24 GMT  
		Size: 243.3 KB (243340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265a5cf3599ba26ecd34c21c0e16bdb2f12001affd4b4e877d7125bfedf74e8f`  
		Last Modified: Fri, 17 Apr 2020 16:23:29 GMT  
		Size: 24.1 MB (24133324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9f2db8b38fcd53a5ee7d35eebfd916deca5257a9c74a013f1d7b40bef9fbe0`  
		Last Modified: Fri, 17 Apr 2020 16:23:22 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2a600dd6e4bb96f461b624fe8612c1de7762951c1eb90021aadd799d2e3e57`  
		Last Modified: Mon, 20 Apr 2020 17:25:45 GMT  
		Size: 69.3 MB (69276965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a019b71496bb19f9f3691f6d0c32ef1b2968b1d0a54ec8db829a748fd1697482`  
		Last Modified: Mon, 20 Apr 2020 17:25:21 GMT  
		Size: 2.6 KB (2554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d219e68e39514c3d2df2260a1dace5669a4603bfd27d2de5bbd07a0ff893d0b`  
		Last Modified: Mon, 20 Apr 2020 17:25:21 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:16-rc-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull nextcloud@sha256:432cec7f3cc5a470a7c7fc7163f3ad4dcf3c5941e33d93b841944d0616c4276b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125370260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dfa447d8f138b5a0a4afbc782a9ab57dff579e6bb350edb663881a5f14eb0da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 00:27:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 24 Mar 2020 00:27:19 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 24 Mar 2020 00:27:21 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 24 Mar 2020 00:27:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Mar 2020 00:27:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 24 Mar 2020 00:31:20 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Tue, 24 Mar 2020 00:31:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Mar 2020 00:31:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Apr 2020 13:23:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Apr 2020 14:22:17 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 17 Apr 2020 14:22:19 GMT
ENV PHP_VERSION=7.3.17
# Fri, 17 Apr 2020 14:22:20 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.17.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.17.tar.xz.asc/from/this/mirror
# Fri, 17 Apr 2020 14:22:21 GMT
ENV PHP_SHA256=6a30304c27f7e7a94538f5ffec599f600ee93aedbbecad8aa4f8bec539b10ad8 PHP_MD5=
# Fri, 17 Apr 2020 14:22:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 17 Apr 2020 14:22:26 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 17 Apr 2020 14:25:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 17 Apr 2020 14:25:20 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 17 Apr 2020 14:25:23 GMT
RUN docker-php-ext-enable sodium
# Fri, 17 Apr 2020 14:25:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Apr 2020 14:25:24 GMT
WORKDIR /var/www/html
# Fri, 17 Apr 2020 14:25:26 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 17 Apr 2020 14:25:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Apr 2020 14:25:29 GMT
EXPOSE 9000
# Fri, 17 Apr 2020 14:25:31 GMT
CMD ["php-fpm"]
# Fri, 17 Apr 2020 16:40:38 GMT
RUN set -ex;         apk add --no-cache         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/15 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 17 Apr 2020 16:44:14 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         icu-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libpng-dev         libmemcached-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev         imagemagick-dev         libwebp-dev         gmp-dev     ;         docker-php-ext-configure gd --with-freetype-dir=/usr --with-png-dir=/usr --with-jpeg-dir=/usr --with-webp-dir=/usr;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-4.3.0;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --virtual .nextcloud-phpext-rundeps $runDeps;     apk del .build-deps
# Fri, 17 Apr 2020 16:44:19 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 17 Apr 2020 16:44:20 GMT
VOLUME [/var/www/html]
# Mon, 20 Apr 2020 16:42:28 GMT
ENV NEXTCLOUD_VERSION=16.0.10RC1
# Mon, 20 Apr 2020 16:43:25 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/prereleases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/prereleases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm -r "$GNUPGHOME" nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del .fetch-deps
# Mon, 20 Apr 2020 16:43:29 GMT
COPY multi:57de70033920dd582f0dbb812d28f0cfdcf6a102d5b4374faf9435d87a0a7585 in / 
# Mon, 20 Apr 2020 16:43:30 GMT
COPY multi:965c5cb843579fcde0cf3c9edb975639cbd2d55de5f645b1061d46855979394d in /usr/src/nextcloud/config/ 
# Mon, 20 Apr 2020 16:43:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Apr 2020 16:43:31 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee501176ea6c9d16dc12649d7c62f4b6466cc96eaf80bfcea3aa261a052ec099`  
		Last Modified: Tue, 24 Mar 2020 01:03:05 GMT  
		Size: 1.4 MB (1359430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e876007701d95df62eb874f76916e4d139709812e5e0be471c4107729808d6af`  
		Last Modified: Tue, 24 Mar 2020 01:03:04 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ed02bd016dcfb57e62d938f46a81237af426353ef7df647b64c3b3a93276a7`  
		Last Modified: Tue, 24 Mar 2020 01:03:04 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3813b0ac87515d0051ca369cc988483868501b4d19041459b3e276a526eb8536`  
		Last Modified: Fri, 17 Apr 2020 15:42:44 GMT  
		Size: 12.1 MB (12135762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e00f280ba95882e54d409c323493a27cb7225922c91e4397edf25e7808cb66`  
		Last Modified: Fri, 17 Apr 2020 15:42:40 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:300d45b409e7b094f301f528f7166c1de6937225e079b305d55f5355b5d678df`  
		Last Modified: Fri, 17 Apr 2020 15:42:45 GMT  
		Size: 14.2 MB (14169365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf451511d09b5194f6014d6ab4a5ef80bda7ea36780cae5e69e6171815487e7`  
		Last Modified: Fri, 17 Apr 2020 15:42:40 GMT  
		Size: 2.2 KB (2213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e3714cdc083f7168b6061ca7a33ea9b8f96a2a7b8541f049824873631238623`  
		Last Modified: Fri, 17 Apr 2020 15:42:40 GMT  
		Size: 17.0 KB (17043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729594a93af8c507c7ee7526096dca5b0184e555e91a06288982b2337e9f80b7`  
		Last Modified: Fri, 17 Apr 2020 15:42:40 GMT  
		Size: 8.4 KB (8409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd004f362194fafd0c7672f00e56692cf2f8c7621a7bc6862bc6490751a24c16`  
		Last Modified: Fri, 17 Apr 2020 17:30:54 GMT  
		Size: 269.2 KB (269193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af26f8533c938df3bdce63fea9712707024af5649fc1b5e1efcf461953f621b3`  
		Last Modified: Fri, 17 Apr 2020 17:31:00 GMT  
		Size: 25.4 MB (25402260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c90ab350594aa2bfdf237f531ff7c64e8e77189c9911c8d628d98ec7fb955a`  
		Last Modified: Fri, 17 Apr 2020 17:30:52 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a746a53cbc403a484543296db270f9383452c9ee699182c6601bc20012f8efae`  
		Last Modified: Mon, 20 Apr 2020 17:01:16 GMT  
		Size: 69.3 MB (69276974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f659f97c5733219f487dc14e69c63e682da831cabeb825d93d07f9abd1a89591`  
		Last Modified: Mon, 20 Apr 2020 17:00:58 GMT  
		Size: 2.6 KB (2553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b1b713d71c38ac3dec4ae2f79577706b12ef41bea118fee3448097a1595cf4`  
		Last Modified: Mon, 20 Apr 2020 17:00:58 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:16-rc-fpm-alpine` - linux; 386

```console
$ docker pull nextcloud@sha256:57f1f821e79ccff0743ff7fce3a0947b4925e6712619aa5208f7381017003e4e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126824969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869bae5d44c7cddeec703236fdef2765a8fa76da04272f14f46349bd5e6eec9e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 23 Mar 2020 21:38:28 GMT
ADD file:99c8234abafd4fa915c0b826eb0e3be0e6aaa7c1e33cb1214ef71a99e9c02e06 in / 
# Mon, 23 Mar 2020 21:38:28 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 02:43:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 24 Mar 2020 02:43:35 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 24 Mar 2020 02:43:36 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 24 Mar 2020 02:43:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Mar 2020 02:43:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 24 Mar 2020 02:51:22 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Tue, 24 Mar 2020 02:51:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Mar 2020 02:51:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Apr 2020 08:09:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Apr 2020 09:36:40 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 17 Apr 2020 09:36:40 GMT
ENV PHP_VERSION=7.3.17
# Fri, 17 Apr 2020 09:36:41 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.17.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.17.tar.xz.asc/from/this/mirror
# Fri, 17 Apr 2020 09:36:41 GMT
ENV PHP_SHA256=6a30304c27f7e7a94538f5ffec599f600ee93aedbbecad8aa4f8bec539b10ad8 PHP_MD5=
# Fri, 17 Apr 2020 09:36:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 17 Apr 2020 09:36:44 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 17 Apr 2020 09:43:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 17 Apr 2020 09:43:21 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 17 Apr 2020 09:43:22 GMT
RUN docker-php-ext-enable sodium
# Fri, 17 Apr 2020 09:43:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Apr 2020 09:43:23 GMT
WORKDIR /var/www/html
# Fri, 17 Apr 2020 09:43:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 17 Apr 2020 09:43:24 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Apr 2020 09:43:24 GMT
EXPOSE 9000
# Fri, 17 Apr 2020 09:43:24 GMT
CMD ["php-fpm"]
# Fri, 17 Apr 2020 14:16:04 GMT
RUN set -ex;         apk add --no-cache         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/15 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 17 Apr 2020 14:19:13 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         icu-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libpng-dev         libmemcached-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev         imagemagick-dev         libwebp-dev         gmp-dev     ;         docker-php-ext-configure gd --with-freetype-dir=/usr --with-png-dir=/usr --with-jpeg-dir=/usr --with-webp-dir=/usr;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-4.3.0;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --virtual .nextcloud-phpext-rundeps $runDeps;     apk del .build-deps
# Fri, 17 Apr 2020 14:19:14 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 17 Apr 2020 14:19:14 GMT
VOLUME [/var/www/html]
# Mon, 20 Apr 2020 16:39:28 GMT
ENV NEXTCLOUD_VERSION=16.0.10RC1
# Mon, 20 Apr 2020 16:39:53 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/prereleases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/prereleases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm -r "$GNUPGHOME" nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del .fetch-deps
# Mon, 20 Apr 2020 16:39:53 GMT
COPY multi:57de70033920dd582f0dbb812d28f0cfdcf6a102d5b4374faf9435d87a0a7585 in / 
# Mon, 20 Apr 2020 16:39:54 GMT
COPY multi:965c5cb843579fcde0cf3c9edb975639cbd2d55de5f645b1061d46855979394d in /usr/src/nextcloud/config/ 
# Mon, 20 Apr 2020 16:39:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Apr 2020 16:39:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:43f6a4398e1c9e860dfb5c93d7049ab9eedf814513bd6d07e06077c560303c7a`  
		Last Modified: Mon, 23 Mar 2020 21:38:48 GMT  
		Size: 2.8 MB (2806122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8addccc9b68d6aad59a5f93e0ca1813c5d09a0c7943108d860d8c29f6bebdb5`  
		Last Modified: Tue, 24 Mar 2020 04:03:48 GMT  
		Size: 1.5 MB (1452601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb273244de1495dfb0044080245a9fa0c6f3d8a2ab5f30610237d9a76e66cd4`  
		Last Modified: Tue, 24 Mar 2020 04:03:47 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d6dffa3f09145ac45428f87b062a4603137dadcaa84454812f81f70b71ea07`  
		Last Modified: Tue, 24 Mar 2020 04:03:47 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a9f21a31999d51b3656143e27734240a2b4126bd650d12d178be79a8bef7332`  
		Last Modified: Fri, 17 Apr 2020 11:57:05 GMT  
		Size: 12.1 MB (12135763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a411623dba30045feedada8b5808030c8a4cce685b4869ab2635ef8ec63f63`  
		Last Modified: Fri, 17 Apr 2020 11:57:01 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ebbebfe6d9779e9a617985de74ed35b8320e6c35fa2a7ddb67bd6b529a0a01a`  
		Last Modified: Fri, 17 Apr 2020 11:57:10 GMT  
		Size: 14.8 MB (14819149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8499086693ca3698c3f608ea40dea6057e9bf860c9f6a21f8f7b85370aa38f`  
		Last Modified: Fri, 17 Apr 2020 11:57:01 GMT  
		Size: 2.2 KB (2214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:313541c3610fa348606e5de3af4a8bc7acb6a13fb58fa5261dd07f58a2cf1be6`  
		Last Modified: Fri, 17 Apr 2020 11:57:01 GMT  
		Size: 17.1 KB (17055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbcd0e7b63262da33e48c7d6283f11c44f2bcbf1582ffc8d21584152fa65b2ce`  
		Last Modified: Fri, 17 Apr 2020 11:57:01 GMT  
		Size: 8.4 KB (8413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304a56722bb6ebbf5b449267346d2cc0026ab0f039fe2a5aa5e2c52274d77c6a`  
		Last Modified: Fri, 17 Apr 2020 14:46:21 GMT  
		Size: 277.0 KB (277035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95986205ca06006ced946e39adc8244582f42ae02f2835e59171f43eaca59e10`  
		Last Modified: Fri, 17 Apr 2020 14:46:27 GMT  
		Size: 26.0 MB (26022962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f8eb1a084c1ec33f85bb426fbbeb7ca6ec888bd7a69f8b230d1c30b5b94d2d`  
		Last Modified: Fri, 17 Apr 2020 14:46:19 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11c778040d320d6b6d1e736e9fd5656e0fbfb752a1c7624a5ebcd5e5e10a04b`  
		Last Modified: Mon, 20 Apr 2020 16:50:35 GMT  
		Size: 69.3 MB (69277288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22271fbdbce3b3e7db2f331ddefabd5637f151cee60ffbe3bcaf6de77fcfa026`  
		Last Modified: Mon, 20 Apr 2020 16:50:18 GMT  
		Size: 2.6 KB (2551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060bdbb06fadbf4973280f0fd40d974f3a3e898438e39f3b48acb5f95af74641`  
		Last Modified: Mon, 20 Apr 2020 16:50:18 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:16-rc-fpm-alpine` - linux; ppc64le

```console
$ docker pull nextcloud@sha256:08a9c2b717e09b228ef2d1e513060bb93198a86192cf62106af71c13ec569d55
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127448701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd8facd345387224c1016a52476cc5f1d434df4920fae0a1d0e6b03ec12f00d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 18 Jan 2020 02:20:41 GMT
ADD file:32ddb3d5255071cca51573ceee2464dd5a87c8d1cce514ae965b6e824d9ef24b in / 
# Sat, 18 Jan 2020 02:20:45 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:24:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 18 Jan 2020 03:24:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 18 Jan 2020 03:24:20 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 18 Jan 2020 03:24:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 18 Jan 2020 03:24:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 18 Jan 2020 03:29:11 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 18 Jan 2020 03:29:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:29:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:29:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:44:39 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 20 Feb 2020 23:32:51 GMT
ENV PHP_VERSION=7.3.15
# Thu, 20 Feb 2020 23:32:56 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.15.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.15.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 23:32:58 GMT
ENV PHP_SHA256=de7ae7cf3d1dbb2824975b26b32991dac2b732886ec22075b8c53b261b018166 PHP_MD5=
# Thu, 20 Feb 2020 23:33:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Feb 2020 23:33:14 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 23:37:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 23:37:24 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 20 Feb 2020 23:37:34 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 23:37:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 23:37:43 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 23:37:49 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 20 Feb 2020 23:37:52 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Feb 2020 23:37:54 GMT
EXPOSE 9000
# Thu, 20 Feb 2020 23:37:56 GMT
CMD ["php-fpm"]
# Fri, 21 Feb 2020 05:33:32 GMT
RUN set -ex;         apk add --no-cache         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/15 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 21 Feb 2020 05:36:17 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         icu-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libpng-dev         libmemcached-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev         imagemagick-dev         libwebp-dev         gmp-dev     ;         docker-php-ext-configure gd --with-freetype-dir=/usr --with-png-dir=/usr --with-jpeg-dir=/usr --with-webp-dir=/usr;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-4.3.0;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --virtual .nextcloud-phpext-rundeps $runDeps;     apk del .build-deps
# Fri, 21 Feb 2020 05:36:27 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 21 Feb 2020 05:36:29 GMT
VOLUME [/var/www/html]
# Tue, 10 Mar 2020 00:52:54 GMT
ENV NEXTCLOUD_VERSION=16.0.9RC2
# Tue, 10 Mar 2020 00:54:30 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/prereleases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/prereleases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm -r "$GNUPGHOME" nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del .fetch-deps
# Tue, 10 Mar 2020 00:54:33 GMT
COPY multi:4c0d5f2638534e3802f1f41694007dfeea41bc4977afff5103eb396d3c7ab26b in / 
# Tue, 10 Mar 2020 00:54:35 GMT
COPY multi:07fbadbda22b19b1f9b8cfc5e833b697afbaa1e602ffea77b26286f5899f86d6 in /usr/src/nextcloud/config/ 
# Tue, 10 Mar 2020 00:54:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 10 Mar 2020 00:54:45 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:cd95c8a93e39dcaa0634a65d5b86a88bcd5c3092adb1f96504a7030faa165123`  
		Last Modified: Sat, 18 Jan 2020 02:21:25 GMT  
		Size: 2.8 MB (2822125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eccdcd97be351ef8da754f6efea3745b7060b1fe92ab96e4b8f5ff85b6322da9`  
		Last Modified: Sat, 18 Jan 2020 04:12:49 GMT  
		Size: 1.4 MB (1397881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea78a138902aeee431e9b31b236dfea5d4f95a1e155aada946ca57f6650a4da9`  
		Last Modified: Sat, 18 Jan 2020 04:12:49 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda899b5dd7be53564e6266c17b869d98468c50bc887279c51acacfa831de39f`  
		Last Modified: Sat, 18 Jan 2020 04:12:49 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1775719ce1987b3e74bb726563ad1142557efde7e2ece216f5f611a41b8932`  
		Last Modified: Fri, 21 Feb 2020 01:46:40 GMT  
		Size: 12.1 MB (12131117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75fa22675f5682529e1aa1345c5e5bcbbc9580dfaefe26e4892f93b7494901b`  
		Last Modified: Fri, 21 Feb 2020 01:46:35 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce0c911f9e9989f53f34b0a44403e57188888a94a99653898b2761a509c8ccc`  
		Last Modified: Fri, 21 Feb 2020 01:46:40 GMT  
		Size: 15.9 MB (15914637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc21471de95a95d2f73dedd73f6c54fb75bbcd63448412e15252844689060bc`  
		Last Modified: Fri, 21 Feb 2020 01:46:36 GMT  
		Size: 2.2 KB (2217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e6379540f5bbf58cd0788233a0ecbb1912f02646b3accdbfe9cda9b380e64e`  
		Last Modified: Fri, 21 Feb 2020 01:46:36 GMT  
		Size: 72.8 KB (72789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da52ff22f56b499ccb06bcc130b81e63edde35898738738ac0217bde5b8a1b44`  
		Last Modified: Fri, 21 Feb 2020 01:46:37 GMT  
		Size: 8.4 KB (8413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a0cb5dca0945e079afcec0b39568556a312b564fa907068b3cabe19bf85dd3`  
		Last Modified: Fri, 21 Feb 2020 06:57:00 GMT  
		Size: 331.1 KB (331109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a71b7b867313288e6e99517bba4911071767f27444f8d2b812d4d71042cd071`  
		Last Modified: Fri, 21 Feb 2020 06:57:10 GMT  
		Size: 26.1 MB (26109554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33eea45bad467ab98295308cd6ec3af20f189d30f80f2ceb2f378353a108074`  
		Last Modified: Fri, 21 Feb 2020 06:56:56 GMT  
		Size: 525.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:316e15d29c0dd7b7e9cfe41ae4eb6a0e6b717d7e1a1a0fb9ae72b622c96bc39b`  
		Last Modified: Tue, 10 Mar 2020 01:36:58 GMT  
		Size: 68.7 MB (68653027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cfeab100fda37c117ccb2f068f30808789ffb2ed2a28486e7aaa1ce9fee0ab4`  
		Last Modified: Tue, 10 Mar 2020 01:31:22 GMT  
		Size: 2.2 KB (2161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf10dc7c14a828b13ef525fd370a1f0b94979b18d40e74b80329d6aca62cbaf`  
		Last Modified: Tue, 10 Mar 2020 01:31:22 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:16-rc-fpm-alpine` - linux; s390x

```console
$ docker pull nextcloud@sha256:2fcce9323fefd4469f03355cf7c0b891e126c04ab821af6e65b47461497a370e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.1 MB (125095957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35aeca4b508bffac11f870e589528e39d039ca5e177d8530ef686e6866dddc2e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 23 Mar 2020 21:41:34 GMT
ADD file:b6d4ad8fd0ec7f66e6d54b8cd8937ba7821b44096806af78692b4cab6d087a9c in / 
# Mon, 23 Mar 2020 21:41:34 GMT
CMD ["/bin/sh"]
# Thu, 09 Apr 2020 21:33:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 09 Apr 2020 21:33:10 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 09 Apr 2020 21:33:11 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 09 Apr 2020 21:33:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Apr 2020 21:33:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 10 Apr 2020 19:15:05 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 10 Apr 2020 19:15:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Apr 2020 19:15:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Apr 2020 08:41:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Apr 2020 09:22:24 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 17 Apr 2020 09:22:25 GMT
ENV PHP_VERSION=7.3.17
# Fri, 17 Apr 2020 09:22:25 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.17.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.17.tar.xz.asc/from/this/mirror
# Fri, 17 Apr 2020 09:22:26 GMT
ENV PHP_SHA256=6a30304c27f7e7a94538f5ffec599f600ee93aedbbecad8aa4f8bec539b10ad8 PHP_MD5=
# Fri, 17 Apr 2020 09:22:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 17 Apr 2020 09:22:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 17 Apr 2020 09:27:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 17 Apr 2020 09:27:33 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 17 Apr 2020 09:27:35 GMT
RUN docker-php-ext-enable sodium
# Fri, 17 Apr 2020 09:27:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Apr 2020 09:27:37 GMT
WORKDIR /var/www/html
# Fri, 17 Apr 2020 09:27:39 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 17 Apr 2020 09:27:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Apr 2020 09:27:40 GMT
EXPOSE 9000
# Fri, 17 Apr 2020 09:27:41 GMT
CMD ["php-fpm"]
# Fri, 17 Apr 2020 11:55:18 GMT
RUN set -ex;         apk add --no-cache         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/15 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 17 Apr 2020 11:56:30 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         icu-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libpng-dev         libmemcached-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev         imagemagick-dev         libwebp-dev         gmp-dev     ;         docker-php-ext-configure gd --with-freetype-dir=/usr --with-png-dir=/usr --with-jpeg-dir=/usr --with-webp-dir=/usr;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-4.3.0;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --virtual .nextcloud-phpext-rundeps $runDeps;     apk del .build-deps
# Fri, 17 Apr 2020 11:56:32 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 17 Apr 2020 11:56:32 GMT
VOLUME [/var/www/html]
# Mon, 20 Apr 2020 16:42:20 GMT
ENV NEXTCLOUD_VERSION=16.0.10RC1
# Mon, 20 Apr 2020 16:42:39 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/prereleases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/prereleases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm -r "$GNUPGHOME" nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del .fetch-deps
# Mon, 20 Apr 2020 16:42:44 GMT
COPY multi:57de70033920dd582f0dbb812d28f0cfdcf6a102d5b4374faf9435d87a0a7585 in / 
# Mon, 20 Apr 2020 16:42:45 GMT
COPY multi:965c5cb843579fcde0cf3c9edb975639cbd2d55de5f645b1061d46855979394d in /usr/src/nextcloud/config/ 
# Mon, 20 Apr 2020 16:42:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Apr 2020 16:42:45 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ca1c6795bfb97df28a926fd646127ba4944b69beb1cea7b00d62787b8b3c0108`  
		Last Modified: Mon, 23 Mar 2020 21:41:56 GMT  
		Size: 2.6 MB (2582073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad3b53ba6c7f5ff683ae6afa31df6374faa3c07822f066af26578dd2c918e37`  
		Last Modified: Fri, 10 Apr 2020 21:46:58 GMT  
		Size: 1.4 MB (1396295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfd25bc04177b98b92121b955a3ae61d15d399f38ca2104da4b71fc9d04e4a9`  
		Last Modified: Fri, 10 Apr 2020 21:46:57 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:338a05df156f3e56a8e489253e860451d64f871e71549ca9fffa31d161963f93`  
		Last Modified: Fri, 10 Apr 2020 21:46:55 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b3c78d55eff5fcf04c6b5cdeb4d5159a6b24ae1e4c838a39234f564535f76f`  
		Last Modified: Fri, 17 Apr 2020 10:31:45 GMT  
		Size: 12.1 MB (12135771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92cf07b365ba2b68e3dccb5b8d013fb453d9dc6e6162284a447d9759ecf9411`  
		Last Modified: Fri, 17 Apr 2020 10:31:42 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3c227cfbc2d71f5860485f96b68f78092323c2dc77ec621a0e0e5f1f24f2d7`  
		Last Modified: Fri, 17 Apr 2020 10:31:51 GMT  
		Size: 13.8 MB (13757160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1deab12e457643a2b798f3ef435bac7f46d646d1e683789829537a740a5a2813`  
		Last Modified: Fri, 17 Apr 2020 10:31:58 GMT  
		Size: 2.2 KB (2219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2d41f5c5391be1aa9f06c1bac02bb932ba1b922a36a3ceacf2d03257a20bc9`  
		Last Modified: Fri, 17 Apr 2020 10:31:42 GMT  
		Size: 17.0 KB (17035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b755481ec229ed5c02564f242aca8e9a8a2bb0d5e652da92f839ebdfc0ea9f`  
		Last Modified: Fri, 17 Apr 2020 10:31:42 GMT  
		Size: 8.4 KB (8413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed571f1f2cb56a800a138381b394e01c9415865aac0a2e411bc259ad56efba7`  
		Last Modified: Fri, 17 Apr 2020 12:25:49 GMT  
		Size: 272.0 KB (271956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d539604401033a91c9c0bd443d206a4cae2cc983573f53636ed4b72e4cd825`  
		Last Modified: Fri, 17 Apr 2020 12:25:52 GMT  
		Size: 25.6 MB (25641552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d52ef5421fd4c9b1f75191a696a79eddba268c111008d775c02acfef8e55a54`  
		Last Modified: Fri, 17 Apr 2020 12:25:47 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42ea69eba820703a9694746a242dd97d00e8bc6955da8a0efbf9295659b23f0`  
		Last Modified: Mon, 20 Apr 2020 16:52:41 GMT  
		Size: 69.3 MB (69277011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70b4ca97ed47a762608ad870ac7bd8bd5d1246372dd2e118007e501ae04c5f2`  
		Last Modified: Mon, 20 Apr 2020 16:52:47 GMT  
		Size: 2.6 KB (2553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7023bfe19007b354dc46c4686f02444942d7fc0d419eb5c4be116bb84c3c31f2`  
		Last Modified: Mon, 20 Apr 2020 16:52:49 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
