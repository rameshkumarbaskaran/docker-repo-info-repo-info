## `friendica:dev-fpm-alpine`

```console
$ docker pull friendica@sha256:19cd79beabe416b4c8ac380e8c81a986a8f25c52268138686eae03932f188f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `friendica:dev-fpm-alpine` - linux; amd64

```console
$ docker pull friendica@sha256:bd4c1faf38c389d20bb79af8215a92d36a7a43a565353d0b1bac8566ab2f0cdc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48831678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410895adc3f5651d7c9fbd76d0ff3ba95939671e22b6c96abc21221ab38b5e51`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 17:35:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 24 Apr 2020 17:35:50 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 24 Apr 2020 17:35:51 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 24 Apr 2020 17:35:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 24 Apr 2020 17:35:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 24 Apr 2020 17:41:08 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 24 Apr 2020 17:41:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Apr 2020 17:41:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Apr 2020 17:41:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 24 Apr 2020 18:13:46 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 15 May 2020 03:35:01 GMT
ENV PHP_VERSION=7.3.18
# Fri, 15 May 2020 03:35:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.18.tar.xz.asc
# Fri, 15 May 2020 03:35:02 GMT
ENV PHP_SHA256=7b3e2479a8d6fd7666dcdef8aec50d49c4599cc6ee86e48d41724cfd99cc9e58 PHP_MD5=
# Fri, 15 May 2020 03:35:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 May 2020 03:35:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 May 2020 03:43:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 02 Jun 2020 21:26:43 GMT
COPY multi:bd67471e0c4047be362a8a0e199558e6245207a6f70b72fdfe55aa2d2cae15e6 in /usr/local/bin/ 
# Tue, 02 Jun 2020 21:26:44 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jun 2020 21:26:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jun 2020 21:26:45 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 21:26:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 02 Jun 2020 21:26:46 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Jun 2020 21:26:46 GMT
EXPOSE 9000
# Tue, 02 Jun 2020 21:26:46 GMT
CMD ["php-fpm"]
# Tue, 02 Jun 2020 23:59:22 GMT
RUN set -ex;     apk add --no-cache         rsync         git         ssmtp         shadow         tini;
# Wed, 03 Jun 2020 00:00:58 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mysql-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev     ;         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;         docker-php-ext-install -j "$(nproc)"        pdo_mysql        gd        zip        opcache        pcntl        ldap     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.2.1;     pecl install imagick-3.4.4;         docker-php-ext-enable     	apcu         memcached         redis         imagick     ;         runDeps="$(       scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions           | tr ',' '\n'           | sort -u           | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps;
# Wed, 03 Jun 2020 00:00:59 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Wed, 03 Jun 2020 00:00:59 GMT
VOLUME [/var/www/html]
# Wed, 03 Jun 2020 00:01:52 GMT
ENV FRIENDICA_VERSION=2020.06-dev
# Wed, 03 Jun 2020 00:01:52 GMT
ENV FRIENDICA_ADDONS=2020.06-dev
# Wed, 03 Jun 2020 00:01:53 GMT
COPY multi:79c18253e95b11e5d803cb19685ac5cb4fcedfeda73215d7e2e3f89d93570667 in / 
# Wed, 03 Jun 2020 00:01:53 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Wed, 03 Jun 2020 00:01:53 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Wed, 03 Jun 2020 00:01:54 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc86e4cff5f320d778d7412cab415d31e8e986659b5e453545b0a7afe86d472`  
		Last Modified: Fri, 24 Apr 2020 19:16:17 GMT  
		Size: 1.4 MB (1355296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be142bd33f5003d85a3e056208af127ac6c5f627f263469134baafdd011ad59`  
		Last Modified: Fri, 24 Apr 2020 19:16:16 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8132c9e52be363f64724649f370635dd54cac7b8696c6365dd2011290afbc7c0`  
		Last Modified: Fri, 24 Apr 2020 19:16:16 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd3bab6dd2a627f22ce5c0fca8b69ce6e71690bd1d31c49c71c7d73594626a7`  
		Last Modified: Fri, 15 May 2020 06:22:51 GMT  
		Size: 12.1 MB (12135951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c6b59e65beb122382bd5ff2ebd5b1c28afad7e66ebc57ade90311ad3acf578`  
		Last Modified: Fri, 15 May 2020 06:22:49 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14653794c696348acbbddb2e05a0869f58a66a182eaac7a74b2c37115126e6b2`  
		Last Modified: Fri, 15 May 2020 06:22:54 GMT  
		Size: 14.4 MB (14443957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b71d6d2ee05bbde3840546c066c4dfd8decad1625534ba936ab11e7af43d303b`  
		Last Modified: Tue, 02 Jun 2020 21:31:56 GMT  
		Size: 2.3 KB (2278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecd1e4c035cb583c1eb0a7eb3ae8aad72d6a3a77c2fad5cdb7ca1a79ce7739ce`  
		Last Modified: Tue, 02 Jun 2020 21:31:56 GMT  
		Size: 16.9 KB (16922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748cbd71c007e409a5482b08a0eaaf6fb588b725aef5c441648a493fdabdd175`  
		Last Modified: Tue, 02 Jun 2020 21:31:57 GMT  
		Size: 8.4 KB (8420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e360be17f6168862add43a3b6c35e733f45b5d8977ba1dd1116bd5ef8e3dee`  
		Last Modified: Wed, 03 Jun 2020 00:02:40 GMT  
		Size: 8.9 MB (8943528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2dd1fb0b3286253bc877f7a22c1a0c0f7db7696788244ea23df38d6d355038`  
		Last Modified: Wed, 03 Jun 2020 00:02:40 GMT  
		Size: 9.1 MB (9105592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5946c7abe41c059f86122b28ab8e25e73372bfbbb0e7966f650dc1265315e4ef`  
		Last Modified: Wed, 03 Jun 2020 00:02:38 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a568eefe79b97a32464e634fcb5c820a606b004e499b70e3db461ba7336200c`  
		Last Modified: Wed, 03 Jun 2020 00:02:38 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2cd794a42a2b52e89d0a5aab765e944fb4773ed82567c10efebd0f8169004a`  
		Last Modified: Wed, 03 Jun 2020 00:02:38 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-fpm-alpine` - linux; arm variant v6

```console
$ docker pull friendica@sha256:3bb18e2b10bc73f5aea701825714bb4bef8b49449d52845f8b957b218f3df41f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47088394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38c8d614a4021bbafa4357890fb8035c87c1b023494b024cc4cd32c9480f3ac`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Thu, 11 Jun 2020 18:14:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 11 Jun 2020 18:14:50 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 11 Jun 2020 18:14:52 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 11 Jun 2020 18:14:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2020 18:14:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 11 Jun 2020 18:20:14 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 11 Jun 2020 18:20:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2020 18:20:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2020 18:20:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2020 18:49:43 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 11 Jun 2020 18:49:43 GMT
ENV PHP_VERSION=7.3.19
# Thu, 11 Jun 2020 18:49:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.19.tar.xz.asc
# Thu, 11 Jun 2020 18:49:45 GMT
ENV PHP_SHA256=6402faa19b1a8c4317c7612632bce985684a5bbae0980a5779a4019439882422 PHP_MD5=
# Thu, 11 Jun 2020 18:49:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 11 Jun 2020 18:49:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 Jun 2020 18:54:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 11 Jun 2020 18:54:07 GMT
COPY multi:bd67471e0c4047be362a8a0e199558e6245207a6f70b72fdfe55aa2d2cae15e6 in /usr/local/bin/ 
# Thu, 11 Jun 2020 18:54:16 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 Jun 2020 18:54:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2020 18:54:22 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2020 18:54:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 11 Jun 2020 18:54:28 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Jun 2020 18:54:29 GMT
EXPOSE 9000
# Thu, 11 Jun 2020 18:54:30 GMT
CMD ["php-fpm"]
# Thu, 11 Jun 2020 21:33:29 GMT
RUN set -ex;     apk add --no-cache         rsync         git         ssmtp         shadow         tini;
# Thu, 11 Jun 2020 21:36:35 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mysql-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev     ;         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;         docker-php-ext-install -j "$(nproc)"        pdo_mysql        gd        zip        opcache        pcntl        ldap     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.2.1;     pecl install imagick-3.4.4;         docker-php-ext-enable     	apcu         memcached         redis         imagick     ;         runDeps="$(       scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions           | tr ',' '\n'           | sort -u           | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps;
# Thu, 11 Jun 2020 21:36:37 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Thu, 11 Jun 2020 21:36:38 GMT
VOLUME [/var/www/html]
# Thu, 11 Jun 2020 21:37:34 GMT
ENV FRIENDICA_VERSION=2020.06-dev
# Thu, 11 Jun 2020 21:37:34 GMT
ENV FRIENDICA_ADDONS=2020.06-dev
# Thu, 11 Jun 2020 21:37:36 GMT
COPY multi:79c18253e95b11e5d803cb19685ac5cb4fcedfeda73215d7e2e3f89d93570667 in / 
# Thu, 11 Jun 2020 21:37:37 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Thu, 11 Jun 2020 21:37:38 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 11 Jun 2020 21:37:39 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72788d65e292354c2ce4b67441d334d0ba534db5ce71d5b8bf78011a256b566f`  
		Last Modified: Thu, 11 Jun 2020 19:29:37 GMT  
		Size: 1.3 MB (1310273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e32d62de43da999aca07cf15fdbe1cd6b03aebc88c15409c3463daadf13e01`  
		Last Modified: Thu, 11 Jun 2020 19:29:36 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6701e05673b745147608cd1b6eb47a3fbc35bcfd8a65bc536e5b9f919b3d0e77`  
		Last Modified: Thu, 11 Jun 2020 19:29:36 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfdc186cc7d770e1dd848851a0edff9f29b8420e3eeb8c514546179408d14151`  
		Last Modified: Thu, 11 Jun 2020 19:32:07 GMT  
		Size: 12.1 MB (12137446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b1b3d3cc42a10b3bff060659273f61f3fe0d488d5a404a55ff42987be08253`  
		Last Modified: Thu, 11 Jun 2020 19:32:04 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc41e8155088920616c5fb8c06c9a83f2974eada80f8a64b9ca6f08346c10af4`  
		Last Modified: Thu, 11 Jun 2020 19:32:07 GMT  
		Size: 13.4 MB (13434484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2511fede9502a3b1c902debe88037bb29f6fec4023e8503dfd0b3bd41272e46c`  
		Last Modified: Thu, 11 Jun 2020 19:32:04 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d79aaf1041cf052aea079eb6b10c184d0b024ecc2540a7db5e9d865f3742e54`  
		Last Modified: Thu, 11 Jun 2020 19:32:04 GMT  
		Size: 16.7 KB (16748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c25597fab65d3bd2eb61aa5be4865ed26fb4f33a23ab1d863360b5b0ca608d0`  
		Last Modified: Thu, 11 Jun 2020 19:32:04 GMT  
		Size: 8.4 KB (8416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcfb84b2ecc64c22dbc9b7c004b5471cd0b13a7f50982468819f7274551bfba`  
		Last Modified: Thu, 11 Jun 2020 21:37:52 GMT  
		Size: 8.6 MB (8615340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd784c2087e8489c50522aa87653bf64a7f39bffb17690c768de4e3f3ae2823`  
		Last Modified: Thu, 11 Jun 2020 21:37:52 GMT  
		Size: 9.0 MB (8953595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da7219ce491926f3b8424de2ae7d3bb52a7edd02e18f73fb46b3d92c2acf700`  
		Last Modified: Thu, 11 Jun 2020 21:37:49 GMT  
		Size: 575.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25d2985eec175a7eff9cb5a68cf39e10168d2dcc8d5f29caff4c5f6dbfefdeb`  
		Last Modified: Thu, 11 Jun 2020 21:37:49 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f01a5918687d55844f47a88b897d4d2fc786e8e88c599d49e981cf95c267a7`  
		Last Modified: Thu, 11 Jun 2020 21:37:49 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-fpm-alpine` - linux; arm variant v7

```console
$ docker pull friendica@sha256:dfb05a048d361c0883e976a4e802d7b16ca4934fea0065636ac4e12ab6b58168
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44172037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b18f09965c6f9dd4dde5f46d23ece9dd675be3e1ce307b350df7a07e5e666f`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 09:12:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 24 Apr 2020 09:12:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 24 Apr 2020 09:12:34 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 24 Apr 2020 09:12:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 24 Apr 2020 09:12:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 24 Apr 2020 09:15:20 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 24 Apr 2020 09:15:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Apr 2020 09:15:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Apr 2020 09:15:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 24 Apr 2020 10:06:01 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 14 May 2020 23:24:12 GMT
ENV PHP_VERSION=7.3.18
# Thu, 14 May 2020 23:24:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.18.tar.xz.asc
# Thu, 14 May 2020 23:24:14 GMT
ENV PHP_SHA256=7b3e2479a8d6fd7666dcdef8aec50d49c4599cc6ee86e48d41724cfd99cc9e58 PHP_MD5=
# Thu, 14 May 2020 23:24:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 14 May 2020 23:24:19 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 14 May 2020 23:26:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 02 Jun 2020 22:06:50 GMT
COPY multi:bd67471e0c4047be362a8a0e199558e6245207a6f70b72fdfe55aa2d2cae15e6 in /usr/local/bin/ 
# Tue, 02 Jun 2020 22:06:54 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jun 2020 22:06:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jun 2020 22:06:56 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 22:06:58 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 02 Jun 2020 22:06:59 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Jun 2020 22:07:00 GMT
EXPOSE 9000
# Tue, 02 Jun 2020 22:07:00 GMT
CMD ["php-fpm"]
# Tue, 02 Jun 2020 22:48:52 GMT
RUN set -ex;     apk add --no-cache         rsync         git         ssmtp         shadow         tini;
# Tue, 02 Jun 2020 22:51:50 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mysql-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev     ;         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;         docker-php-ext-install -j "$(nproc)"        pdo_mysql        gd        zip        opcache        pcntl        ldap     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.2.1;     pecl install imagick-3.4.4;         docker-php-ext-enable     	apcu         memcached         redis         imagick     ;         runDeps="$(       scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions           | tr ',' '\n'           | sort -u           | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps;
# Tue, 02 Jun 2020 22:51:54 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 02 Jun 2020 22:51:55 GMT
VOLUME [/var/www/html]
# Tue, 02 Jun 2020 22:53:28 GMT
ENV FRIENDICA_VERSION=2020.06-dev
# Tue, 02 Jun 2020 22:53:29 GMT
ENV FRIENDICA_ADDONS=2020.06-dev
# Tue, 02 Jun 2020 22:53:31 GMT
COPY multi:79c18253e95b11e5d803cb19685ac5cb4fcedfeda73215d7e2e3f89d93570667 in / 
# Tue, 02 Jun 2020 22:53:32 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Tue, 02 Jun 2020 22:53:34 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 02 Jun 2020 22:53:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39281f57fe7d3f99c4fe23af0e5eb45caa0646180d5ff71304d26ff35a0b9856`  
		Last Modified: Fri, 24 Apr 2020 11:16:34 GMT  
		Size: 1.2 MB (1227897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df36ec4ede8343ef6e75d1f33f8dbbe0ccdfa6522152dda7801db48b8a06b85`  
		Last Modified: Fri, 24 Apr 2020 11:16:33 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e16ed34ef7f3b453ef768e1198de2318c7d1cdd60f43223f1c53df2e82119e`  
		Last Modified: Fri, 24 Apr 2020 11:16:33 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daede5e8beaed5a4424f466fa6be0dd172c1e1799703833e8718b73456b1c069`  
		Last Modified: Fri, 15 May 2020 00:45:29 GMT  
		Size: 12.1 MB (12135965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bccfb83d9f4c3bdef45d87ad2ada282134dc7a08a5e08150d4b4280128336b5`  
		Last Modified: Fri, 15 May 2020 00:45:24 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff48b76d47020446d8a31191e67d0ad8bfad84c4c25604721d0a9fa89bd5ba76`  
		Last Modified: Fri, 15 May 2020 00:45:28 GMT  
		Size: 12.5 MB (12542253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7b4fe848868764f099e55bf1e399cdf83bad36d0b597b674ed62e46045162a`  
		Last Modified: Tue, 02 Jun 2020 22:16:58 GMT  
		Size: 2.3 KB (2278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f01907d1234beed2939a4c36e7979187a1de9571ab1023bbe52f7a325b55a4`  
		Last Modified: Tue, 02 Jun 2020 22:16:58 GMT  
		Size: 16.9 KB (16879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa9479dc904142f054826df0e0d05e5bcd1be6cae83b6f6e59d0293555008d3`  
		Last Modified: Tue, 02 Jun 2020 22:16:58 GMT  
		Size: 8.4 KB (8422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1050ef0c36f4e8c352d97c376cf7dcf9e47a1ac3063460c8d2d65ed8c6d5524`  
		Last Modified: Tue, 02 Jun 2020 22:54:12 GMT  
		Size: 7.6 MB (7622962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a90e96bdaa59593e78330bdfdfd53679599faba724a47ba095fa63ab84e60d7`  
		Last Modified: Tue, 02 Jun 2020 22:54:13 GMT  
		Size: 8.2 MB (8186780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc80b5b61054669aed446c18921f91d052bd1eb88344ff43cc521f5065258aa`  
		Last Modified: Tue, 02 Jun 2020 22:54:11 GMT  
		Size: 577.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e9ab392abd39acfa0109d0df73449870ba4e0a8c78966fc105c43ca35ab777`  
		Last Modified: Tue, 02 Jun 2020 22:54:11 GMT  
		Size: 2.9 KB (2850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03795d9d8f5cf333266e26536670ea39946832051aa9babd383e7d43db673a30`  
		Last Modified: Tue, 02 Jun 2020 22:54:11 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:a4d62e0f00616cb817486d5b319ed6a5eb29af28d6ce983373b4949740024bbd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48512285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13f1d8aa73563db10c38e6e565cc3b41569381201c268467c7e58f505512380`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:51:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 24 Apr 2020 12:51:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 24 Apr 2020 12:51:35 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 24 Apr 2020 12:51:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 24 Apr 2020 12:51:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 24 Apr 2020 12:55:36 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 24 Apr 2020 12:55:37 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Apr 2020 12:55:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Apr 2020 12:55:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 24 Apr 2020 13:20:12 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 15 May 2020 01:07:53 GMT
ENV PHP_VERSION=7.3.18
# Fri, 15 May 2020 01:07:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.18.tar.xz.asc
# Fri, 15 May 2020 01:07:55 GMT
ENV PHP_SHA256=7b3e2479a8d6fd7666dcdef8aec50d49c4599cc6ee86e48d41724cfd99cc9e58 PHP_MD5=
# Fri, 15 May 2020 01:07:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 May 2020 01:08:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 May 2020 01:10:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 02 Jun 2020 21:53:24 GMT
COPY multi:bd67471e0c4047be362a8a0e199558e6245207a6f70b72fdfe55aa2d2cae15e6 in /usr/local/bin/ 
# Tue, 02 Jun 2020 21:53:32 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jun 2020 21:53:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jun 2020 21:53:34 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 21:53:35 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 02 Jun 2020 21:53:36 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Jun 2020 21:53:37 GMT
EXPOSE 9000
# Tue, 02 Jun 2020 21:53:37 GMT
CMD ["php-fpm"]
# Tue, 02 Jun 2020 22:57:04 GMT
RUN set -ex;     apk add --no-cache         rsync         git         ssmtp         shadow         tini;
# Tue, 02 Jun 2020 23:00:03 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mysql-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev     ;         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;         docker-php-ext-install -j "$(nproc)"        pdo_mysql        gd        zip        opcache        pcntl        ldap     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.2.1;     pecl install imagick-3.4.4;         docker-php-ext-enable     	apcu         memcached         redis         imagick     ;         runDeps="$(       scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions           | tr ',' '\n'           | sort -u           | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps;
# Tue, 02 Jun 2020 23:00:06 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 02 Jun 2020 23:00:07 GMT
VOLUME [/var/www/html]
# Tue, 02 Jun 2020 23:01:32 GMT
ENV FRIENDICA_VERSION=2020.06-dev
# Tue, 02 Jun 2020 23:01:33 GMT
ENV FRIENDICA_ADDONS=2020.06-dev
# Tue, 02 Jun 2020 23:01:34 GMT
COPY multi:79c18253e95b11e5d803cb19685ac5cb4fcedfeda73215d7e2e3f89d93570667 in / 
# Tue, 02 Jun 2020 23:01:35 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Tue, 02 Jun 2020 23:01:36 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 02 Jun 2020 23:01:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8614da4aa8d46e10af7f7788136931561b8f1d1efe1a78311b26f5cf57506f`  
		Last Modified: Fri, 24 Apr 2020 14:02:47 GMT  
		Size: 1.4 MB (1359714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ececdba1264fbd4760d671f21f71713e4038fc665ad77ae891d54cc1d8db0cc3`  
		Last Modified: Fri, 24 Apr 2020 14:02:46 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab4eb699b8d1e5be3d1e82202067c943b8869558f71be0d2557563912b0f942`  
		Last Modified: Fri, 24 Apr 2020 14:02:47 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3d65bb7b2918ebf9f9a3d9a99a950f7e30cbdf915714bd4c1b1252c61076808`  
		Last Modified: Fri, 15 May 2020 02:30:38 GMT  
		Size: 12.1 MB (12135959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2887397ca89d88ad2684fc5a3583e3541c11c6e0c87c342d00dec4a7ad82465`  
		Last Modified: Fri, 15 May 2020 02:30:34 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9fae7ecae4bdd2bfdf0b70b2138cdccc4404abc9f4a16b2998116e99d965e85`  
		Last Modified: Fri, 15 May 2020 02:30:36 GMT  
		Size: 14.2 MB (14179596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ceb95f5ec97b36513d55dc1459df890c7e38553d4bfdfd307950011b0d7ad00`  
		Last Modified: Tue, 02 Jun 2020 22:06:00 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44384b852f36c0872be06e7c401590deb06832f79c006c6b6b2e667e255887ef`  
		Last Modified: Tue, 02 Jun 2020 22:06:00 GMT  
		Size: 16.9 KB (16916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8d40c0a78f177b54b73f9d51c26e4cdac19efe56fdf7d341491ac3e3bdaa89`  
		Last Modified: Tue, 02 Jun 2020 22:06:00 GMT  
		Size: 8.4 KB (8419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d7e7a51cd12bfd2025649c8cec5d650abdb25d30735b3c00a77338efbcf0fb`  
		Last Modified: Tue, 02 Jun 2020 23:02:22 GMT  
		Size: 9.1 MB (9128790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de73822e4a903437d35d4ab4d4938fca85e40728b9ae5e9abb4673124e216666`  
		Last Modified: Tue, 02 Jun 2020 23:02:22 GMT  
		Size: 8.9 MB (8949642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd30ca7616053c0d19b43d4fd448f3965fbe50b087b7b06833a16c0ff32da900`  
		Last Modified: Tue, 02 Jun 2020 23:02:20 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4111579798d592055f1b73074cc873e592ba9572d2817cb5cbf48da859601ed`  
		Last Modified: Tue, 02 Jun 2020 23:02:20 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460ed0ad159b710ef05db7ed163bf089f75bad07d363e6e24d8a794fd9cfad1f`  
		Last Modified: Tue, 02 Jun 2020 23:02:20 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-fpm-alpine` - linux; 386

```console
$ docker pull friendica@sha256:2467c47517369c3fc3bbce908eed368e1f94c36f3690507ec0dcfdf32a4df282
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50590291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb87980e126d0ba0ca5b323a26ab2c69dbf3ea51fdc2aa4cd4bc8bcf97b2156`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:04 GMT
ADD file:63bd8a316cba8c404cc2e32a5120406c24aee8db3224c469a6077b941d900863 in / 
# Thu, 23 Apr 2020 21:16:04 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 06:05:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 24 Apr 2020 06:05:46 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 24 Apr 2020 06:05:47 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 24 Apr 2020 06:05:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 24 Apr 2020 06:05:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 24 Apr 2020 06:11:34 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 24 Apr 2020 06:11:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Apr 2020 06:11:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Apr 2020 06:11:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 24 Apr 2020 06:47:03 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 15 May 2020 04:08:25 GMT
ENV PHP_VERSION=7.3.18
# Fri, 15 May 2020 04:08:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.18.tar.xz.asc
# Fri, 15 May 2020 04:08:26 GMT
ENV PHP_SHA256=7b3e2479a8d6fd7666dcdef8aec50d49c4599cc6ee86e48d41724cfd99cc9e58 PHP_MD5=
# Fri, 15 May 2020 04:08:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 May 2020 04:08:31 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 May 2020 04:18:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 02 Jun 2020 21:43:29 GMT
COPY multi:bd67471e0c4047be362a8a0e199558e6245207a6f70b72fdfe55aa2d2cae15e6 in /usr/local/bin/ 
# Tue, 02 Jun 2020 21:43:31 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jun 2020 21:43:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jun 2020 21:43:31 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 21:43:32 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 02 Jun 2020 21:43:32 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Jun 2020 21:43:32 GMT
EXPOSE 9000
# Tue, 02 Jun 2020 21:43:32 GMT
CMD ["php-fpm"]
# Tue, 02 Jun 2020 22:44:52 GMT
RUN set -ex;     apk add --no-cache         rsync         git         ssmtp         shadow         tini;
# Tue, 02 Jun 2020 22:46:56 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mysql-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev     ;         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;         docker-php-ext-install -j "$(nproc)"        pdo_mysql        gd        zip        opcache        pcntl        ldap     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.2.1;     pecl install imagick-3.4.4;         docker-php-ext-enable     	apcu         memcached         redis         imagick     ;         runDeps="$(       scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions           | tr ',' '\n'           | sort -u           | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps;
# Tue, 02 Jun 2020 22:46:57 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 02 Jun 2020 22:46:57 GMT
VOLUME [/var/www/html]
# Tue, 02 Jun 2020 22:47:50 GMT
ENV FRIENDICA_VERSION=2020.06-dev
# Tue, 02 Jun 2020 22:47:50 GMT
ENV FRIENDICA_ADDONS=2020.06-dev
# Tue, 02 Jun 2020 22:47:51 GMT
COPY multi:79c18253e95b11e5d803cb19685ac5cb4fcedfeda73215d7e2e3f89d93570667 in / 
# Tue, 02 Jun 2020 22:47:51 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Tue, 02 Jun 2020 22:47:51 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 02 Jun 2020 22:47:51 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2826c1e79865da7e0da0a993a2a38db61c3911e05b5df617439a86d4deac90fb`  
		Last Modified: Thu, 23 Apr 2020 21:16:32 GMT  
		Size: 2.8 MB (2808418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990138137e85533c48403b0cd1aee9ac6c5f3fc3be67a74a44a22f1a30e39af6`  
		Last Modified: Fri, 24 Apr 2020 07:59:39 GMT  
		Size: 1.5 MB (1453100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d973cd3524efeb6727b2144c33f96c71896f4ee22b1a55cc0c5aa5756f9b758`  
		Last Modified: Fri, 24 Apr 2020 07:59:37 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f386ab173ce6081c15380f99f906f8ea531e5748425804a21ebb0b5c433e6782`  
		Last Modified: Fri, 24 Apr 2020 07:59:38 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82977f578d166ae182063f6c434863475995613482abda41dcf69302e0ebc9af`  
		Last Modified: Fri, 15 May 2020 07:00:08 GMT  
		Size: 12.1 MB (12135962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae6cd5ba3555da6fbb9259b49f417355f3608bcf27963e8509ac8cac3724714`  
		Last Modified: Fri, 15 May 2020 07:00:03 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f149e523b49947dd815eb66a2f161ebdd7c8199da9f8e84cee71c8c46834687a`  
		Last Modified: Fri, 15 May 2020 07:00:12 GMT  
		Size: 14.8 MB (14821352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c0e56a3e32ca512f9ced53969ea323d402c02daf3b2c50bf6ae583124ca162`  
		Last Modified: Tue, 02 Jun 2020 21:48:56 GMT  
		Size: 2.3 KB (2275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80919c28c69f091a66e6c32703ff2042d6ce9978e941d6acb58c7ccfb9f9e1e7`  
		Last Modified: Tue, 02 Jun 2020 21:48:56 GMT  
		Size: 16.9 KB (16901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7861bf0e4d4d966463af35dc7412172492b00c42c374e21c2cdb71f06ecdc61`  
		Last Modified: Tue, 02 Jun 2020 21:48:56 GMT  
		Size: 8.4 KB (8411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb8c5015b33abeabb8d18b1d62a73279275d1fc7a7f8272c808bea940488fd0`  
		Last Modified: Tue, 02 Jun 2020 22:48:27 GMT  
		Size: 10.0 MB (9967086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961df71767bd2016723331d3bb8f536e895d2287a8ef1cca7f028b8d2e02d1cf`  
		Last Modified: Tue, 02 Jun 2020 22:48:26 GMT  
		Size: 9.4 MB (9370381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4236e0066cbaf5bfbbd0b4852c738daea051b75ec33ec9c55a769e3fa0ee3392`  
		Last Modified: Tue, 02 Jun 2020 22:48:23 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee260084219fced6e238e542c0c871daedbf191d8bf520d0a9a19c0efd464a5`  
		Last Modified: Tue, 02 Jun 2020 22:48:24 GMT  
		Size: 2.9 KB (2850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538ca4a40b4fcaba9b015f677d5db95de8ea6dfa21ca653208742b3a34fde0f2`  
		Last Modified: Tue, 02 Jun 2020 22:48:23 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-fpm-alpine` - linux; ppc64le

```console
$ docker pull friendica@sha256:39ff6c64f45b0dec799853a8207db5b0dfd669068c1e30c6295779342f423c00
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50989585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7f27aa358824801a57209800cfdd639fde4b2d4b91cdd99c63a4153665d446`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 07:11:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 24 Apr 2020 07:11:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 24 Apr 2020 07:12:07 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 24 Apr 2020 07:12:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 24 Apr 2020 07:12:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 24 Apr 2020 07:18:49 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 24 Apr 2020 07:18:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Apr 2020 07:18:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Apr 2020 07:18:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 24 Apr 2020 07:55:04 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Mon, 18 May 2020 10:03:52 GMT
ENV PHP_VERSION=7.3.18
# Mon, 18 May 2020 10:04:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.18.tar.xz.asc
# Mon, 18 May 2020 10:04:06 GMT
ENV PHP_SHA256=7b3e2479a8d6fd7666dcdef8aec50d49c4599cc6ee86e48d41724cfd99cc9e58 PHP_MD5=
# Mon, 18 May 2020 10:04:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Mon, 18 May 2020 10:04:30 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 18 May 2020 10:09:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 02 Jun 2020 21:28:52 GMT
COPY multi:bd67471e0c4047be362a8a0e199558e6245207a6f70b72fdfe55aa2d2cae15e6 in /usr/local/bin/ 
# Tue, 02 Jun 2020 21:28:57 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jun 2020 21:28:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jun 2020 21:29:01 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 21:29:06 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 02 Jun 2020 21:29:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Jun 2020 21:29:09 GMT
EXPOSE 9000
# Tue, 02 Jun 2020 21:29:11 GMT
CMD ["php-fpm"]
# Tue, 02 Jun 2020 22:31:39 GMT
RUN set -ex;     apk add --no-cache         rsync         git         ssmtp         shadow         tini;
# Tue, 02 Jun 2020 22:34:14 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mysql-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev     ;         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;         docker-php-ext-install -j "$(nproc)"        pdo_mysql        gd        zip        opcache        pcntl        ldap     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.2.1;     pecl install imagick-3.4.4;         docker-php-ext-enable     	apcu         memcached         redis         imagick     ;         runDeps="$(       scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions           | tr ',' '\n'           | sort -u           | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps;
# Tue, 02 Jun 2020 22:34:21 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 02 Jun 2020 22:34:25 GMT
VOLUME [/var/www/html]
# Tue, 02 Jun 2020 22:35:56 GMT
ENV FRIENDICA_VERSION=2020.06-dev
# Tue, 02 Jun 2020 22:35:57 GMT
ENV FRIENDICA_ADDONS=2020.06-dev
# Tue, 02 Jun 2020 22:36:00 GMT
COPY multi:79c18253e95b11e5d803cb19685ac5cb4fcedfeda73215d7e2e3f89d93570667 in / 
# Tue, 02 Jun 2020 22:36:00 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Tue, 02 Jun 2020 22:36:02 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 02 Jun 2020 22:36:04 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d52f33021895c8254527a626bd23b02f5ffb7cf7d498663099bfb52bc36cb4f`  
		Last Modified: Fri, 24 Apr 2020 08:53:41 GMT  
		Size: 1.4 MB (1398496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca0df5facaec815af37eabcf3f16b8d84fbf49322219c06e6d19e7067b54f86`  
		Last Modified: Fri, 24 Apr 2020 08:53:38 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eafa9bf45f1a09b417cf061af38e982c6a4e2c77a1f1f3c59b8587f215c9208`  
		Last Modified: Fri, 24 Apr 2020 08:53:37 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb2791ecf08083b2c56fb42d338e6e2acc9c075a68930d7d40c6ff860a02736`  
		Last Modified: Mon, 18 May 2020 12:25:42 GMT  
		Size: 12.1 MB (12135981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362a405ca1195dc1df8148b5865c0bf9413958b3797475b766ee87a5c7445c96`  
		Last Modified: Mon, 18 May 2020 12:25:32 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e3c67f84b1c47bbe2278c1881255065a223bab743e604a4b42b273f5db0627`  
		Last Modified: Mon, 18 May 2020 12:26:02 GMT  
		Size: 15.5 MB (15459242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c847b79f051e19334b9b35bb5337a59991733d670a056eeceb897716a819bcb3`  
		Last Modified: Tue, 02 Jun 2020 21:44:31 GMT  
		Size: 2.3 KB (2275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb95c798a25bd215f4405769e34d2b478c7796092a1762bf75b2cacd254399b`  
		Last Modified: Tue, 02 Jun 2020 21:44:32 GMT  
		Size: 16.9 KB (16885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4dfb97528e55dfb208c3da547e420354bb078671c3772fe9a8524cdccafbce8`  
		Last Modified: Tue, 02 Jun 2020 21:44:32 GMT  
		Size: 8.4 KB (8419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7c09f850a5115ea5db29fbd4c927d0445f03d3ecbf7bc1b0bc04360297137c`  
		Last Modified: Tue, 02 Jun 2020 22:37:04 GMT  
		Size: 9.7 MB (9684891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38a2230eb499191d9c44271a1ee0b9aa83a10eddfb43f11d594b3c5339f18a8`  
		Last Modified: Tue, 02 Jun 2020 22:37:04 GMT  
		Size: 9.5 MB (9454998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e651a550b8a436cc842586bdac5845374365a206fac95fdd052396f63b69c4f`  
		Last Modified: Tue, 02 Jun 2020 22:37:01 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53938be230e975760e980f6333b39f86a404482ff67e574446f98a528fb2618`  
		Last Modified: Tue, 02 Jun 2020 22:37:01 GMT  
		Size: 2.9 KB (2851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581004a90dc18dcc62bd1fd6d7e8cb886661dacfea15c9f273fa78f985580d29`  
		Last Modified: Tue, 02 Jun 2020 22:37:01 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
