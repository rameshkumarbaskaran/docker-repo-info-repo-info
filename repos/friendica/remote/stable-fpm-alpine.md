## `friendica:stable-fpm-alpine`

```console
$ docker pull friendica@sha256:9437a76813083e45ba5f05c34a5e5258802bfc891a04b2994e95e5a4c7b78ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `friendica:stable-fpm-alpine` - linux; amd64

```console
$ docker pull friendica@sha256:5ba9c0b2dfd6325577d14e50050e9230c19220e0bbd7ba85db695db8498a7ad7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106879319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670e5954c956edf13d1cdf77a24e4abe4d7de80f42a02d97a83ed3a63cf8fd04`
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
# Sat, 18 Jan 2020 03:40:28 GMT
ENV PHP_VERSION=7.3.13
# Sat, 18 Jan 2020 03:40:28 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.13.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.13.tar.xz.asc/from/this/mirror
# Sat, 18 Jan 2020 03:40:29 GMT
ENV PHP_SHA256=57ac55fe442d2da650abeb9e6fa161bd3a98ba6528c029f076f8bba43dd5c228 PHP_MD5=
# Sat, 18 Jan 2020 03:40:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 18 Jan 2020 03:40:31 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 18 Jan 2020 03:45:44 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Sat, 18 Jan 2020 03:45:44 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Sat, 18 Jan 2020 03:45:45 GMT
RUN docker-php-ext-enable sodium
# Sat, 18 Jan 2020 03:45:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 18 Jan 2020 03:45:46 GMT
WORKDIR /var/www/html
# Sat, 18 Jan 2020 03:45:46 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Sat, 18 Jan 2020 03:45:46 GMT
STOPSIGNAL SIGQUIT
# Sat, 18 Jan 2020 03:45:47 GMT
EXPOSE 9000
# Sat, 18 Jan 2020 03:45:47 GMT
CMD ["php-fpm"]
# Sat, 18 Jan 2020 05:21:56 GMT
RUN set -ex;     apk add --no-cache         rsync         git         ssmtp         shadow;
# Sat, 18 Jan 2020 05:24:26 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mysql-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev     ;         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;         docker-php-ext-install -j "$(nproc)"        pdo_mysql        gd        zip        opcache        pcntl        ldap     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.1.1;     pecl install imagick-3.4.4;         docker-php-ext-enable     	apcu         memcached         redis         imagick     ;         runDeps="$(       scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions           | tr ',' '\n'           | sort -u           | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps;
# Sat, 18 Jan 2020 05:24:27 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Sat, 18 Jan 2020 05:24:27 GMT
VOLUME [/var/www/html]
# Sat, 18 Jan 2020 05:24:28 GMT
ENV FRIENDICA_VERSION=2019.12
# Sat, 18 Jan 2020 05:24:28 GMT
ENV FRIENDICA_ADDONS=2019.12
# Sat, 18 Jan 2020 05:24:48 GMT
RUN set -ex;     curl -fsSL -o friendica.tar.gz         "https://github.com/friendica/friendica/archive/${FRIENDICA_VERSION}.tar.gz";     tar -xzf friendica.tar.gz -C /usr/src/;     rm friendica.tar.gz;     mv -f /usr/src/friendica-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;     curl -fsSL -o friendica_addons.tar.gz         "https://github.com/friendica/friendica-addons/archive/${FRIENDICA_ADDONS}.tar.gz";     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica_addons.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica_addons.tar.gz;     /usr/src/friendica/bin/composer.phar install --no-dev -d /usr/src/friendica;
# Sat, 18 Jan 2020 05:24:49 GMT
COPY multi:0a5bdeeeece27826a5344be9215b3de17c80ece34c27fd9cf4c61a0c7e730616 in / 
# Sat, 18 Jan 2020 05:24:49 GMT
COPY multi:ccf608c3083a2548ed80248e6308632e395ce7dfbcb83d73bfba22293ecd8ffd in /usr/src/friendica/config/ 
# Sat, 18 Jan 2020 05:24:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 18 Jan 2020 05:24:49 GMT
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
	-	`sha256:95d062b61344d183d57cd61c6f5977fe44c943543373b7e4b00a7bfb93747649`  
		Last Modified: Sat, 18 Jan 2020 04:10:33 GMT  
		Size: 12.1 MB (12121661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b294e5746a7783e6dce563ee899ee4ba356e19138cece30851b6164df5ed6116`  
		Last Modified: Sat, 18 Jan 2020 04:10:30 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51c6b4a18496adeb1d87f0bf1ad95d86a14d2bb770b917deb3e76b33075faec`  
		Last Modified: Sat, 18 Jan 2020 04:10:33 GMT  
		Size: 14.9 MB (14894909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:277c385c86cfc0cddfb686d2eacfccb06fa76658c631b038d552bb235d811c88`  
		Last Modified: Sat, 18 Jan 2020 04:10:31 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:569d023f896549d009c7c1e489bf68f28c9de5bbaa67ebbe75a701a526ba6b24`  
		Last Modified: Sat, 18 Jan 2020 04:10:30 GMT  
		Size: 72.9 KB (72924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e55056f435969e1593a43ec31b6389526d84f15638605b07bc339c3f0431b02`  
		Last Modified: Sat, 18 Jan 2020 04:10:31 GMT  
		Size: 8.4 KB (8412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2293ff1b84adcc01dbc1e2807e2be12843171fad658af252ee0bfeb9601b6cbd`  
		Last Modified: Sat, 18 Jan 2020 05:25:16 GMT  
		Size: 9.0 MB (8969206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bcd4df43ec4589172b86d342ff8916a1a9cbc3d8f37f9c35faabac0aa43664d`  
		Last Modified: Sat, 18 Jan 2020 05:25:14 GMT  
		Size: 9.1 MB (9103849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe33b6e347886f396ff22700c99937bfc5fb547c64f6375aec9fdf511caf5ef4`  
		Last Modified: Sat, 18 Jan 2020 05:25:12 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55772e5d66e030e817769a5e4880e3056b4372aeedc297c98bec8719a3bde61c`  
		Last Modified: Sat, 18 Jan 2020 05:25:21 GMT  
		Size: 57.5 MB (57542793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb756e5019b672ce166a82bddd980904dd4a773fa3fd36cab2500a793dfef363`  
		Last Modified: Sat, 18 Jan 2020 05:25:12 GMT  
		Size: 2.2 KB (2179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d3c0f52debd4b904b1465450120ad5dd136ad4d7714fee3643424951084c42`  
		Last Modified: Sat, 18 Jan 2020 05:25:12 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:stable-fpm-alpine` - linux; arm variant v6

```console
$ docker pull friendica@sha256:621da8df69a7111501d3becf8cd382b0ca9b7407d5d4cf34f5953de402bd629f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.1 MB (106075363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44bf32c97fd8730fb6762f4edd6670fee23a52f8eefa8eb86c68c301bc9edea9`
-	Entrypoint: `["\/entrypoint.sh"]`
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
# Thu, 26 Dec 2019 22:39:08 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 26 Dec 2019 22:39:09 GMT
ENV PHP_VERSION=7.3.13
# Thu, 26 Dec 2019 22:39:09 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.13.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.13.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 22:39:09 GMT
ENV PHP_SHA256=57ac55fe442d2da650abeb9e6fa161bd3a98ba6528c029f076f8bba43dd5c228 PHP_MD5=
# Thu, 26 Dec 2019 22:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 22:39:14 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:42:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 22:42:58 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:43:01 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 22:43:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 22:43:02 GMT
WORKDIR /var/www/html
# Thu, 26 Dec 2019 22:43:04 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 26 Dec 2019 22:43:05 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Dec 2019 22:43:06 GMT
EXPOSE 9000
# Thu, 26 Dec 2019 22:43:06 GMT
CMD ["php-fpm"]
# Wed, 08 Jan 2020 22:31:27 GMT
RUN set -ex;     apk add --no-cache         rsync         git         ssmtp         shadow;
# Wed, 08 Jan 2020 22:34:33 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mysql-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev     ;         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;         docker-php-ext-install -j "$(nproc)"        pdo_mysql        gd        zip        opcache        pcntl        ldap     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.1.1;     pecl install imagick-3.4.4;         docker-php-ext-enable     	apcu         memcached         redis         imagick     ;         runDeps="$(       scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions           | tr ',' '\n'           | sort -u           | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps;
# Wed, 08 Jan 2020 22:34:36 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Wed, 08 Jan 2020 22:34:37 GMT
VOLUME [/var/www/html]
# Wed, 08 Jan 2020 22:34:38 GMT
ENV FRIENDICA_VERSION=2019.12
# Wed, 08 Jan 2020 22:34:39 GMT
ENV FRIENDICA_ADDONS=2019.12
# Wed, 08 Jan 2020 22:35:20 GMT
RUN set -ex;     curl -fsSL -o friendica.tar.gz         "https://github.com/friendica/friendica/archive/${FRIENDICA_VERSION}.tar.gz";     tar -xzf friendica.tar.gz -C /usr/src/;     rm friendica.tar.gz;     mv -f /usr/src/friendica-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;     curl -fsSL -o friendica_addons.tar.gz         "https://github.com/friendica/friendica-addons/archive/${FRIENDICA_ADDONS}.tar.gz";     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica_addons.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica_addons.tar.gz;     /usr/src/friendica/bin/composer.phar install --no-dev -d /usr/src/friendica;
# Wed, 08 Jan 2020 22:35:27 GMT
COPY multi:0a5bdeeeece27826a5344be9215b3de17c80ece34c27fd9cf4c61a0c7e730616 in / 
# Wed, 08 Jan 2020 22:35:28 GMT
COPY multi:ccf608c3083a2548ed80248e6308632e395ce7dfbcb83d73bfba22293ecd8ffd in /usr/src/friendica/config/ 
# Wed, 08 Jan 2020 22:35:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Jan 2020 22:35:32 GMT
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
	-	`sha256:822bbc45dff492b6c052ad119ad0350233c90fa29197ed8b0a54945cee35a899`  
		Last Modified: Thu, 26 Dec 2019 23:04:07 GMT  
		Size: 12.1 MB (12121719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e5026165f976c2821328a93e56dddbe5aea743378241f25c5aebeeebda1168`  
		Last Modified: Thu, 26 Dec 2019 23:04:04 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd3d3c9364e9b0c06395b5e04343bda785b4bc94828dea37e9b37e15c68fc78`  
		Last Modified: Thu, 26 Dec 2019 23:04:09 GMT  
		Size: 15.2 MB (15221237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041ee0a31f0c641afa47ce974ac0109709bc4b1f7493c9ea74b13912d6da1814`  
		Last Modified: Thu, 26 Dec 2019 23:04:04 GMT  
		Size: 2.2 KB (2219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4217df8989c3f1484c5b29036a740e7dbbd1bc71c6952bccbe58ff94034f1e4`  
		Last Modified: Thu, 26 Dec 2019 23:04:04 GMT  
		Size: 72.5 KB (72461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7566e62c743c61e8e3719a912f8b11f13ac7ed372f35ccf487c05baca234b6`  
		Last Modified: Thu, 26 Dec 2019 23:04:04 GMT  
		Size: 8.4 KB (8412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20cd293bc0cd18b084fe7cdce5d0e01d889ef8f8fa1876f20626487a4dea80dc`  
		Last Modified: Wed, 08 Jan 2020 22:36:11 GMT  
		Size: 8.5 MB (8513238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a41274a861a53ccbb8025a684b3fb0d3b96f05355b716f2764b0e0de89927d`  
		Last Modified: Wed, 08 Jan 2020 22:36:09 GMT  
		Size: 8.7 MB (8654334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45409468e9f29a253c4e32348a8253a21d88d6abbc01ef7a6bd3faab31f63ca`  
		Last Modified: Wed, 08 Jan 2020 22:36:06 GMT  
		Size: 577.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd44238e12c151b97963dca91cb3b03ea21b9d18922b577873945cfbcce82d9c`  
		Last Modified: Wed, 08 Jan 2020 22:36:23 GMT  
		Size: 57.5 MB (57542726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4689fcfd9d1bc89cf5b057a1c7237c34aeff67274584d1817472fbf7ff16373`  
		Last Modified: Wed, 08 Jan 2020 22:36:06 GMT  
		Size: 2.2 KB (2180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fee1d50038280cb063d15095aab571af087cfb200d7c6e22f76f0995b9ca273`  
		Last Modified: Wed, 08 Jan 2020 22:36:06 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:stable-fpm-alpine` - linux; arm variant v7

```console
$ docker pull friendica@sha256:9d3ef8724f84eeb5aecab12967bb734e431c6de82dd2d1bf70d61a64231c31b8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103520900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e91180b657dc412b0ae2b971f88d27258fda8a30f2560d02b941adb8a1a833`
-	Entrypoint: `["\/entrypoint.sh"]`
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
# Thu, 26 Dec 2019 21:40:56 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 26 Dec 2019 21:40:57 GMT
ENV PHP_VERSION=7.3.13
# Thu, 26 Dec 2019 21:40:57 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.13.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.13.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 21:40:58 GMT
ENV PHP_SHA256=57ac55fe442d2da650abeb9e6fa161bd3a98ba6528c029f076f8bba43dd5c228 PHP_MD5=
# Thu, 26 Dec 2019 21:41:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 21:41:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:43:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 21:43:39 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:43:45 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 21:43:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 21:43:48 GMT
WORKDIR /var/www/html
# Thu, 26 Dec 2019 21:43:50 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 26 Dec 2019 21:43:50 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Dec 2019 21:43:51 GMT
EXPOSE 9000
# Thu, 26 Dec 2019 21:43:52 GMT
CMD ["php-fpm"]
# Wed, 08 Jan 2020 22:44:19 GMT
RUN set -ex;     apk add --no-cache         rsync         git         ssmtp         shadow;
# Wed, 08 Jan 2020 22:47:09 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mysql-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev     ;         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;         docker-php-ext-install -j "$(nproc)"        pdo_mysql        gd        zip        opcache        pcntl        ldap     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.1.1;     pecl install imagick-3.4.4;         docker-php-ext-enable     	apcu         memcached         redis         imagick     ;         runDeps="$(       scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions           | tr ',' '\n'           | sort -u           | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps;
# Wed, 08 Jan 2020 22:47:11 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Wed, 08 Jan 2020 22:47:12 GMT
VOLUME [/var/www/html]
# Wed, 08 Jan 2020 22:47:12 GMT
ENV FRIENDICA_VERSION=2019.12
# Wed, 08 Jan 2020 22:47:13 GMT
ENV FRIENDICA_ADDONS=2019.12
# Wed, 08 Jan 2020 22:47:42 GMT
RUN set -ex;     curl -fsSL -o friendica.tar.gz         "https://github.com/friendica/friendica/archive/${FRIENDICA_VERSION}.tar.gz";     tar -xzf friendica.tar.gz -C /usr/src/;     rm friendica.tar.gz;     mv -f /usr/src/friendica-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;     curl -fsSL -o friendica_addons.tar.gz         "https://github.com/friendica/friendica-addons/archive/${FRIENDICA_ADDONS}.tar.gz";     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica_addons.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica_addons.tar.gz;     /usr/src/friendica/bin/composer.phar install --no-dev -d /usr/src/friendica;
# Wed, 08 Jan 2020 22:47:45 GMT
COPY multi:0a5bdeeeece27826a5344be9215b3de17c80ece34c27fd9cf4c61a0c7e730616 in / 
# Wed, 08 Jan 2020 22:47:47 GMT
COPY multi:ccf608c3083a2548ed80248e6308632e395ce7dfbcb83d73bfba22293ecd8ffd in /usr/src/friendica/config/ 
# Wed, 08 Jan 2020 22:47:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Jan 2020 22:47:49 GMT
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
	-	`sha256:2a9dff75b303d2f139474aebe1810bee376ea846a85f9bfedf5f2a57bad8dba8`  
		Last Modified: Thu, 26 Dec 2019 22:03:04 GMT  
		Size: 12.1 MB (12121713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f71b053328be84d647891df2e4c6a7496db3e7e9ef3aa709d533dd680dd10e`  
		Last Modified: Thu, 26 Dec 2019 22:03:00 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35abe73774e859ec10a03e76cbc5e99f4a3303bd60c1a296e212bc774a568ac2`  
		Last Modified: Thu, 26 Dec 2019 22:03:07 GMT  
		Size: 14.3 MB (14279420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b14efcf7568c047a6acc52671b73678f065c47d9fea733bb7cfee97e978fb7`  
		Last Modified: Thu, 26 Dec 2019 22:03:00 GMT  
		Size: 2.2 KB (2218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9382f28f181081769da69757371eab051ab23a48834fd4480efe02777444ef38`  
		Last Modified: Thu, 26 Dec 2019 22:03:00 GMT  
		Size: 72.5 KB (72452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375e23786c22b0569638da70c5c0948d1976b106aa59e5b26cd835f47ae9dd3c`  
		Last Modified: Thu, 26 Dec 2019 22:03:01 GMT  
		Size: 8.4 KB (8412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed758cb8d16cf11893cbcdbb5805e879b41aa76ef3075473f877cd7a4248256`  
		Last Modified: Wed, 08 Jan 2020 22:49:48 GMT  
		Size: 7.7 MB (7658918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a66a815a139954a669d9470a333e711f1b4d6a355204ed07f4ea7e9db25cc2`  
		Last Modified: Wed, 08 Jan 2020 22:49:47 GMT  
		Size: 8.2 MB (8185025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2472f5ee72df32b335d9ff9d6eac496fff7c36e9cd11d2af8fa89c1fff4adae7`  
		Last Modified: Wed, 08 Jan 2020 22:49:44 GMT  
		Size: 574.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63bde58f87b0970bf2a16fd57d41476f220565ea9c143683778deda2e38ff00`  
		Last Modified: Wed, 08 Jan 2020 22:50:00 GMT  
		Size: 57.5 MB (57542842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7edecc0331e2ec8367bce67bd648eb32fd83760912195463b3598e2f206213c2`  
		Last Modified: Wed, 08 Jan 2020 22:49:44 GMT  
		Size: 2.2 KB (2180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb18bbc5285bb9728b4c26d7bc5ab566e4edf9d05e53be74019104f99e7744fe`  
		Last Modified: Wed, 08 Jan 2020 22:49:44 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:stable-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:eff5c2d4ca96b9bf165011b80ffff7028fa925d6497386bb05d41c2402d875ea
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.1 MB (108053514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1564065f5bb131c90bb209b318ed8da2dfadb6a317de861593f846642ab576c`
-	Entrypoint: `["\/entrypoint.sh"]`
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
# Thu, 26 Dec 2019 22:26:00 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 26 Dec 2019 22:26:01 GMT
ENV PHP_VERSION=7.3.13
# Thu, 26 Dec 2019 22:26:01 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.13.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.13.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 22:26:02 GMT
ENV PHP_SHA256=57ac55fe442d2da650abeb9e6fa161bd3a98ba6528c029f076f8bba43dd5c228 PHP_MD5=
# Thu, 26 Dec 2019 22:26:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 22:26:07 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:29:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 22:29:56 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:29:59 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 22:30:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 22:30:01 GMT
WORKDIR /var/www/html
# Thu, 26 Dec 2019 22:30:02 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 26 Dec 2019 22:30:03 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Dec 2019 22:30:04 GMT
EXPOSE 9000
# Thu, 26 Dec 2019 22:30:05 GMT
CMD ["php-fpm"]
# Wed, 08 Jan 2020 22:53:13 GMT
RUN set -ex;     apk add --no-cache         rsync         git         ssmtp         shadow;
# Wed, 08 Jan 2020 22:56:30 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mysql-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev     ;         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;         docker-php-ext-install -j "$(nproc)"        pdo_mysql        gd        zip        opcache        pcntl        ldap     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.1.1;     pecl install imagick-3.4.4;         docker-php-ext-enable     	apcu         memcached         redis         imagick     ;         runDeps="$(       scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions           | tr ',' '\n'           | sort -u           | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps;
# Wed, 08 Jan 2020 22:56:37 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Wed, 08 Jan 2020 22:56:39 GMT
VOLUME [/var/www/html]
# Wed, 08 Jan 2020 22:56:42 GMT
ENV FRIENDICA_VERSION=2019.12
# Wed, 08 Jan 2020 22:56:44 GMT
ENV FRIENDICA_ADDONS=2019.12
# Wed, 08 Jan 2020 22:57:17 GMT
RUN set -ex;     curl -fsSL -o friendica.tar.gz         "https://github.com/friendica/friendica/archive/${FRIENDICA_VERSION}.tar.gz";     tar -xzf friendica.tar.gz -C /usr/src/;     rm friendica.tar.gz;     mv -f /usr/src/friendica-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;     curl -fsSL -o friendica_addons.tar.gz         "https://github.com/friendica/friendica-addons/archive/${FRIENDICA_ADDONS}.tar.gz";     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica_addons.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica_addons.tar.gz;     /usr/src/friendica/bin/composer.phar install --no-dev -d /usr/src/friendica;
# Wed, 08 Jan 2020 22:57:22 GMT
COPY multi:0a5bdeeeece27826a5344be9215b3de17c80ece34c27fd9cf4c61a0c7e730616 in / 
# Wed, 08 Jan 2020 22:57:25 GMT
COPY multi:ccf608c3083a2548ed80248e6308632e395ce7dfbcb83d73bfba22293ecd8ffd in /usr/src/friendica/config/ 
# Wed, 08 Jan 2020 22:57:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Jan 2020 22:57:29 GMT
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
	-	`sha256:1c5a5a78fde8390078f1f9d24a63235881517f5be598ad5eb88a30fc9e69ea04`  
		Last Modified: Thu, 26 Dec 2019 22:50:26 GMT  
		Size: 12.1 MB (12121703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b550413e662c74aedd8a52db71b91a28beb4efe286da2df89a433b49dfcb8dba`  
		Last Modified: Thu, 26 Dec 2019 22:50:23 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e4ba5f126f14f5dee0fe9f65f122fcc514a1e2c312c29b700c5d7742ac803a`  
		Last Modified: Thu, 26 Dec 2019 22:50:28 GMT  
		Size: 16.1 MB (16113917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251ef297ec93f8024bc967bacee6278179d7c152aac78f3028cf634e5af9e169`  
		Last Modified: Thu, 26 Dec 2019 22:50:24 GMT  
		Size: 2.2 KB (2218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942b906bfae5d3692c622caae61a135e05e056273455a38c5ccef0dd9bea70b4`  
		Last Modified: Thu, 26 Dec 2019 22:50:23 GMT  
		Size: 72.5 KB (72458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846c216d0bca80e1622c10735097fccd32893da0836aa594cce6eed966a23fd8`  
		Last Modified: Thu, 26 Dec 2019 22:50:23 GMT  
		Size: 8.4 KB (8413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c242978cb354be000e1ef2de0d518af583707ffacc807f6886d4a44a51c7b5`  
		Last Modified: Wed, 08 Jan 2020 22:59:32 GMT  
		Size: 9.2 MB (9159740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6039405487e3a3964e2badea1a979120ddf6b1b74cbec6a7f8d643124328f72a`  
		Last Modified: Wed, 08 Jan 2020 22:59:30 GMT  
		Size: 8.9 MB (8947807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638b5a59825b81d9d15eefc7eefbac42d75988d5f7b3c9b01e7280ef4719b234`  
		Last Modified: Wed, 08 Jan 2020 22:59:27 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cae37baca3db4e5b33aa87669560b8bf747a6915c42aab134ec2c11bdc280d0`  
		Last Modified: Wed, 08 Jan 2020 22:59:43 GMT  
		Size: 57.5 MB (57542774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc48f32ffc470ffa431965a9e231c04f28c17e92d2a6acc367e2fa4677ff10cc`  
		Last Modified: Wed, 08 Jan 2020 22:59:27 GMT  
		Size: 2.2 KB (2180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:058d9589ee4ea58f6bd044d71a45d0f7c204e13e6ac08713fe3d46fcafe4db29`  
		Last Modified: Wed, 08 Jan 2020 22:59:27 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:stable-fpm-alpine` - linux; 386

```console
$ docker pull friendica@sha256:bf11f9f1a5da2598e4d25bf263083c190df82e6c283efd779bdc08f234fc812b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110250538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:239375d35bc6bed409f9161afaeae9ebf1acfca0279a54ce5f30e988c0c40cf0`
-	Entrypoint: `["\/entrypoint.sh"]`
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
# Thu, 26 Dec 2019 23:13:09 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 26 Dec 2019 23:13:10 GMT
ENV PHP_VERSION=7.3.13
# Thu, 26 Dec 2019 23:13:10 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.13.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.13.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 23:13:11 GMT
ENV PHP_SHA256=57ac55fe442d2da650abeb9e6fa161bd3a98ba6528c029f076f8bba43dd5c228 PHP_MD5=
# Thu, 26 Dec 2019 23:13:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 23:13:15 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 23:20:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 23:20:27 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 26 Dec 2019 23:20:28 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 23:20:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 23:20:28 GMT
WORKDIR /var/www/html
# Thu, 26 Dec 2019 23:20:29 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 26 Dec 2019 23:20:29 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Dec 2019 23:20:30 GMT
EXPOSE 9000
# Thu, 26 Dec 2019 23:20:30 GMT
CMD ["php-fpm"]
# Wed, 08 Jan 2020 22:46:31 GMT
RUN set -ex;     apk add --no-cache         rsync         git         ssmtp         shadow;
# Wed, 08 Jan 2020 22:48:20 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mysql-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev     ;         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;         docker-php-ext-install -j "$(nproc)"        pdo_mysql        gd        zip        opcache        pcntl        ldap     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.1.1;     pecl install imagick-3.4.4;         docker-php-ext-enable     	apcu         memcached         redis         imagick     ;         runDeps="$(       scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions           | tr ',' '\n'           | sort -u           | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps;
# Wed, 08 Jan 2020 22:48:21 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Wed, 08 Jan 2020 22:48:21 GMT
VOLUME [/var/www/html]
# Wed, 08 Jan 2020 22:48:21 GMT
ENV FRIENDICA_VERSION=2019.12
# Wed, 08 Jan 2020 22:48:21 GMT
ENV FRIENDICA_ADDONS=2019.12
# Wed, 08 Jan 2020 22:48:38 GMT
RUN set -ex;     curl -fsSL -o friendica.tar.gz         "https://github.com/friendica/friendica/archive/${FRIENDICA_VERSION}.tar.gz";     tar -xzf friendica.tar.gz -C /usr/src/;     rm friendica.tar.gz;     mv -f /usr/src/friendica-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;     curl -fsSL -o friendica_addons.tar.gz         "https://github.com/friendica/friendica-addons/archive/${FRIENDICA_ADDONS}.tar.gz";     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica_addons.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica_addons.tar.gz;     /usr/src/friendica/bin/composer.phar install --no-dev -d /usr/src/friendica;
# Wed, 08 Jan 2020 22:48:38 GMT
COPY multi:0a5bdeeeece27826a5344be9215b3de17c80ece34c27fd9cf4c61a0c7e730616 in / 
# Wed, 08 Jan 2020 22:48:39 GMT
COPY multi:ccf608c3083a2548ed80248e6308632e395ce7dfbcb83d73bfba22293ecd8ffd in /usr/src/friendica/config/ 
# Wed, 08 Jan 2020 22:48:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Jan 2020 22:48:39 GMT
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
	-	`sha256:4655ca26de12857144e36bafcc406d32bc786a3685b725b321ecd0c3a54baee1`  
		Last Modified: Fri, 27 Dec 2019 00:01:52 GMT  
		Size: 12.1 MB (12121706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7404f4aa8e85701473b69aed6ec05202da440d53e87d85f836bc1981a47412df`  
		Last Modified: Fri, 27 Dec 2019 00:01:48 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25effbd8e8870a709534475245b8229d82149896d4ced778b78d7cc6b1e65dcc`  
		Last Modified: Fri, 27 Dec 2019 00:01:56 GMT  
		Size: 16.9 MB (16876469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c333d6b516eb5e2c7378a5c7d733955a17f86fb869c798b991da898bd1f1dcf8`  
		Last Modified: Fri, 27 Dec 2019 00:01:48 GMT  
		Size: 2.2 KB (2219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c52a3416cc32e240769dfb78a9c02cfb5d2cb7ab66906f0dafb16f804799a7`  
		Last Modified: Fri, 27 Dec 2019 00:01:48 GMT  
		Size: 72.1 KB (72110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81e191cae1cc98ea5c223660cd55cd73a7042dea2ff95fcebbd9471a69529ee`  
		Last Modified: Fri, 27 Dec 2019 00:01:48 GMT  
		Size: 8.4 KB (8412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ffa719a81aabf580bb49e39816684300b513b4242263a6387107c93bfc7f9d`  
		Last Modified: Wed, 08 Jan 2020 22:49:50 GMT  
		Size: 10.0 MB (9994701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f207367b426551e708abbb8a04063f93e21bcd983c577a9f33a5f40256b6ef`  
		Last Modified: Wed, 08 Jan 2020 22:49:49 GMT  
		Size: 9.4 MB (9368502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab63c06e0626b12c983316d285a0946ec8e3140a253c0ec49d04c3a58224eea`  
		Last Modified: Wed, 08 Jan 2020 22:49:46 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf80d3d6c4ffe073daea5ded100ec6a100bdba703e56b6ff231965e68c299b1a`  
		Last Modified: Wed, 08 Jan 2020 22:49:58 GMT  
		Size: 57.5 MB (57542900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882ac65d76015fbdbb9ded8a28eaa812b0cb03a0e05207b89bc7c2cb29443031`  
		Last Modified: Wed, 08 Jan 2020 22:49:46 GMT  
		Size: 2.2 KB (2180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afddf771f234eabc430cbd65672522ac881f9633b10e7cb423027844cbc5037b`  
		Last Modified: Wed, 08 Jan 2020 22:49:46 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:stable-fpm-alpine` - linux; ppc64le

```console
$ docker pull friendica@sha256:4162fb5045e234c8eeb8ec516602077cba1b9ffcfbcc84784102044a750575cf
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110573928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c1fecbe6bbe994866434db3965fdac92d4bb5b870415f3a077b480569262dd`
-	Entrypoint: `["\/entrypoint.sh"]`
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
# Thu, 26 Dec 2019 22:44:44 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 26 Dec 2019 22:44:47 GMT
ENV PHP_VERSION=7.3.13
# Thu, 26 Dec 2019 22:44:49 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.13.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.13.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 22:44:51 GMT
ENV PHP_SHA256=57ac55fe442d2da650abeb9e6fa161bd3a98ba6528c029f076f8bba43dd5c228 PHP_MD5=
# Thu, 26 Dec 2019 22:45:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 22:45:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:49:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 22:49:07 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:49:13 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 22:49:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 22:49:16 GMT
WORKDIR /var/www/html
# Thu, 26 Dec 2019 22:49:21 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 26 Dec 2019 22:49:22 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Dec 2019 22:49:24 GMT
EXPOSE 9000
# Thu, 26 Dec 2019 22:49:26 GMT
CMD ["php-fpm"]
# Wed, 08 Jan 2020 22:57:59 GMT
RUN set -ex;     apk add --no-cache         rsync         git         ssmtp         shadow;
# Wed, 08 Jan 2020 23:00:37 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mysql-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev     ;         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;         docker-php-ext-install -j "$(nproc)"        pdo_mysql        gd        zip        opcache        pcntl        ldap     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.1.1;     pecl install imagick-3.4.4;         docker-php-ext-enable     	apcu         memcached         redis         imagick     ;         runDeps="$(       scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions           | tr ',' '\n'           | sort -u           | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps;
# Wed, 08 Jan 2020 23:00:57 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Wed, 08 Jan 2020 23:01:05 GMT
VOLUME [/var/www/html]
# Wed, 08 Jan 2020 23:01:11 GMT
ENV FRIENDICA_VERSION=2019.12
# Wed, 08 Jan 2020 23:01:17 GMT
ENV FRIENDICA_ADDONS=2019.12
# Wed, 08 Jan 2020 23:02:05 GMT
RUN set -ex;     curl -fsSL -o friendica.tar.gz         "https://github.com/friendica/friendica/archive/${FRIENDICA_VERSION}.tar.gz";     tar -xzf friendica.tar.gz -C /usr/src/;     rm friendica.tar.gz;     mv -f /usr/src/friendica-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;     curl -fsSL -o friendica_addons.tar.gz         "https://github.com/friendica/friendica-addons/archive/${FRIENDICA_ADDONS}.tar.gz";     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica_addons.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica_addons.tar.gz;     /usr/src/friendica/bin/composer.phar install --no-dev -d /usr/src/friendica;
# Wed, 08 Jan 2020 23:02:11 GMT
COPY multi:0a5bdeeeece27826a5344be9215b3de17c80ece34c27fd9cf4c61a0c7e730616 in / 
# Wed, 08 Jan 2020 23:02:14 GMT
COPY multi:ccf608c3083a2548ed80248e6308632e395ce7dfbcb83d73bfba22293ecd8ffd in /usr/src/friendica/config/ 
# Wed, 08 Jan 2020 23:02:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Jan 2020 23:02:25 GMT
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
	-	`sha256:ec6660869077b31c1e35e85c4c3e86572130963f93d6aebbe2e0468cb9120274`  
		Last Modified: Thu, 26 Dec 2019 23:15:58 GMT  
		Size: 12.1 MB (12121734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76831a171d8801ba298157b55260ad2c6ef7b37920eac6c73365465a8aafb286`  
		Last Modified: Thu, 26 Dec 2019 23:15:52 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cfeef1a5e7b9b4a0fc99f64e650c6a0833ae8064bc185fb02f4306286e6d0b6`  
		Last Modified: Thu, 26 Dec 2019 23:16:01 GMT  
		Size: 17.4 MB (17446773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8209e344ca6c63901d38e722f528af487a2a69d661904f5f10cea21ee41f12e7`  
		Last Modified: Thu, 26 Dec 2019 23:15:53 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160dbc2dadb854d40eb2ef3a50b3ce4b380e6e79779e41b496f16bb75c3030f8`  
		Last Modified: Thu, 26 Dec 2019 23:15:52 GMT  
		Size: 72.8 KB (72798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6786f5af509d3ae068b9cc8d7c99ac85aa57c1da9296d19c6ae57dcdb0c0fbf3`  
		Last Modified: Thu, 26 Dec 2019 23:15:52 GMT  
		Size: 8.4 KB (8411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6cc6f4a7be50190b52a0b455ec629011d2ec77c8d43b098bf6369322640207`  
		Last Modified: Wed, 08 Jan 2020 23:06:11 GMT  
		Size: 9.7 MB (9709667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31c13877e7e174b4c19e5d75421439e0c098632483beee70c83d8caa1923c95`  
		Last Modified: Wed, 08 Jan 2020 23:06:06 GMT  
		Size: 9.4 MB (9449136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6673c5a47f4a29095ff3da7962940cda15495ee2267eade18f2b980b33e42f19`  
		Last Modified: Wed, 08 Jan 2020 23:06:05 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a09966bc7978dcea34636836293a59ad9e519bddf15ba768ada0875ed83379b`  
		Last Modified: Wed, 08 Jan 2020 23:06:15 GMT  
		Size: 57.5 MB (57542868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce9b6c977fcb63746d164d6e8a9ded2e4a4b7c7926e4a50ce681fae9f3bc86a`  
		Last Modified: Wed, 08 Jan 2020 23:06:05 GMT  
		Size: 2.2 KB (2180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3af9ee715c1dfc5d95aa1429500e98996135745a16ec43797a6b669909497e`  
		Last Modified: Wed, 08 Jan 2020 23:06:05 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
