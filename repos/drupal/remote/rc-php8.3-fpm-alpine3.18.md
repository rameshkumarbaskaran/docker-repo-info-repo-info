## `drupal:rc-php8.3-fpm-alpine3.18`

```console
$ docker pull drupal@sha256:88d4e01eab4ea361b1448e7eabf1becd305d36b3b2743b9737d070c6a1e41b73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `drupal:rc-php8.3-fpm-alpine3.18` - linux; amd64

```console
$ docker pull drupal@sha256:0e8b06886f1e0362888d09d04b0bcac933e93e00a27f6fec97b95a0746f09d42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53842876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583156aed0cf491e865cb0c5bb34dd368747fe3d6221a7a95da30685a7e39632`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Thu, 30 Nov 2023 23:32:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 05 Dec 2023 00:36:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 05 Dec 2023 00:36:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_VERSION=8.3.1
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.1.tar.xz.asc
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_SHA256=56445b1771b2ba5b7573453f9e8a9451e2d810b1741a352fa05259733b1e9758
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 05 Dec 2023 00:36:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 05 Dec 2023 00:36:09 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 05 Dec 2023 00:36:09 GMT
RUN docker-php-ext-enable sodium
# Tue, 05 Dec 2023 00:36:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 05 Dec 2023 00:36:09 GMT
WORKDIR /var/www/html
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 05 Dec 2023 00:36:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Dec 2023 00:36:09 GMT
EXPOSE 9000
# Tue, 05 Dec 2023 00:36:09 GMT
CMD ["php-fpm"]
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
ENV DRUPAL_VERSION=10.2.0-rc1
# Tue, 05 Dec 2023 00:36:09 GMT
WORKDIR /opt/drupal
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd7d9d0a8568ad67e56f7560786ec06ada3d1624401e0c09a19bac68d6852bf`  
		Last Modified: Tue, 12 Dec 2023 23:25:21 GMT  
		Size: 2.7 MB (2682507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba0fbf849ad16a6e44bd1d2f64aad25339ce479d893afe5a2e6ab1d5f32a8b8`  
		Last Modified: Tue, 12 Dec 2023 23:25:21 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37536836bf3207c08cde055f9b82489c03cdba8bf0195bcc3776a34fa0c4fc3`  
		Last Modified: Tue, 12 Dec 2023 23:25:20 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84feca336f0e93f9410db1f29b3b787e90b2b02ecb366b85e1de959e60ec4b52`  
		Last Modified: Thu, 28 Dec 2023 01:18:07 GMT  
		Size: 12.5 MB (12465365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95d40893fc95bcf2230be556c574c14cc96c071b3465114f742823992bdab1b`  
		Last Modified: Thu, 28 Dec 2023 01:18:06 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d626e66aef42dba4d48cad02da9608d525bcb0917f33152fc435baeeb0d0b7b`  
		Last Modified: Thu, 28 Dec 2023 01:18:33 GMT  
		Size: 12.9 MB (12923837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea596b088ebc70b0f58dd7a3d23108a2855ceed0962ac2d2fdb8fd293d275799`  
		Last Modified: Thu, 28 Dec 2023 01:18:31 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1af25291f02b36b9362705e4143d8414c29d6abb247d2bd0b540dd3726a8269`  
		Last Modified: Thu, 28 Dec 2023 01:18:30 GMT  
		Size: 18.9 KB (18947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6baf3a15e7c823c38c2a5c06e61733f6ba0df829d0feeb0365ee024206f44fa1`  
		Last Modified: Thu, 28 Dec 2023 01:18:30 GMT  
		Size: 9.2 KB (9175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d503e2c67bedc5e39bff8d94844961f7234514ef2779befa0f73908d25db1adc`  
		Last Modified: Thu, 28 Dec 2023 06:49:10 GMT  
		Size: 2.4 MB (2441483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71beee9854c62c368ef44e7aebef1271f44b66e3654d308540016b460ea86b24`  
		Last Modified: Thu, 28 Dec 2023 06:49:10 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cbf086f19c300831e180990bfa80df0cc8e58a8be8f5b6c0fa11d087f4478f`  
		Last Modified: Thu, 28 Dec 2023 06:49:10 GMT  
		Size: 705.2 KB (705206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7c619ae3e0d5074f9868a8ba706f1c194ecbe8186de9baf61d92ad47cd0f0c`  
		Last Modified: Thu, 28 Dec 2023 06:49:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112fa4a5d2bd9f71ff9fcbf93e7d30c3722dbb130c4711d143346231ec97a204`  
		Last Modified: Thu, 28 Dec 2023 06:49:12 GMT  
		Size: 19.2 MB (19189029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:f14b34a81e2283a1a1db1111cdfe386b2df333635a7190dc624c56f35458a446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 KB (317089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9403a68a9674411cdf8d8ebcccb7886d98d27428aebd2f4050aad3cc16bc3525`

```dockerfile
```

-	Layers:
	-	`sha256:79bda534a555ae13f4ea17712dc5038a6048cbfa6511464fe5b684a07019a8dc`  
		Last Modified: Thu, 28 Dec 2023 06:49:09 GMT  
		Size: 282.9 KB (282881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:001b6b16a49deebb54b0e4c4671b5175de24c9ca18a518af4eafb343fbcc147f`  
		Last Modified: Thu, 28 Dec 2023 06:49:09 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-fpm-alpine3.18` - linux; arm variant v6

```console
$ docker pull drupal@sha256:9f190f0ee6fefcf7b64cc4ccdf58678f321be09eef4bf4005e9bf15f92df5509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51913999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abee5f1593444602c336cc180d04b9c58a973dc076ad388fe2c46d0077f48a85`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Thu, 30 Nov 2023 23:15:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 05 Dec 2023 00:36:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 05 Dec 2023 00:36:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_VERSION=8.3.1
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.1.tar.xz.asc
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_SHA256=56445b1771b2ba5b7573453f9e8a9451e2d810b1741a352fa05259733b1e9758
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 05 Dec 2023 00:36:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 05 Dec 2023 00:36:09 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 05 Dec 2023 00:36:09 GMT
RUN docker-php-ext-enable sodium
# Tue, 05 Dec 2023 00:36:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 05 Dec 2023 00:36:09 GMT
WORKDIR /var/www/html
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 05 Dec 2023 00:36:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Dec 2023 00:36:09 GMT
EXPOSE 9000
# Tue, 05 Dec 2023 00:36:09 GMT
CMD ["php-fpm"]
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
ENV DRUPAL_VERSION=10.2.0-rc1
# Tue, 05 Dec 2023 00:36:09 GMT
WORKDIR /opt/drupal
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc4620463cb47a0b53bc40938dace7cd0a6449205a123affe87a8905f53fc67`  
		Last Modified: Tue, 12 Dec 2023 22:11:33 GMT  
		Size: 2.7 MB (2688484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf314afc65237389babea371465ce0680635f0af4c692c1e00e9b9324a94167`  
		Last Modified: Tue, 12 Dec 2023 22:11:32 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041da360c70d55e74ed9edc257854df4b289baf6d0097eb72943da34de87054a`  
		Last Modified: Tue, 12 Dec 2023 22:11:32 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13f8f532dfc841153b6b024dc293f00a1e9b729cd5b8f1d5de067c70f4f3064`  
		Last Modified: Thu, 28 Dec 2023 03:40:15 GMT  
		Size: 12.5 MB (12465360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd4c4490a13abb4cae5de41e04822b78f4619fdd0b582b4b752df77a80d8017`  
		Last Modified: Thu, 28 Dec 2023 03:40:14 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f18534ea6e8b097f93a34cf95e77bab7a319304bccb90633012d55d477382f`  
		Last Modified: Thu, 28 Dec 2023 03:40:43 GMT  
		Size: 11.8 MB (11828937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa9e601cf7915cfa361ae98f29656e24a7cdc2368542d8f4cf8332659638c8e`  
		Last Modified: Thu, 28 Dec 2023 03:40:40 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c4709c43437ea7f76a147e25b90d762df928967d14e03e341441b4ec71fd54`  
		Last Modified: Thu, 28 Dec 2023 03:40:40 GMT  
		Size: 18.8 KB (18779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e7f89f582029825e599ec0d2945745e066e7df20ade53a42a6e7610805947c`  
		Last Modified: Thu, 28 Dec 2023 03:40:40 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc06eb523d97f5eb8c96aa2f070dd05a562cf4a3ddeb72c1e839483f2b69ed40`  
		Last Modified: Sun, 31 Dec 2023 19:47:43 GMT  
		Size: 1.9 MB (1857256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8f0709ac9d3a193667f48058ac79ec5215a8ea4d5ec154e0dbccf2cfb30e02`  
		Last Modified: Sun, 31 Dec 2023 19:47:43 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103b03a7ecc2b5573c7184b1076be206dff7614306a211d9668a072286344aae`  
		Last Modified: Sun, 31 Dec 2023 19:47:44 GMT  
		Size: 705.2 KB (705205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13a8cca6e285aded26658f21c5a4d2c9e16678e16dfeec7da3c4d3792665886`  
		Last Modified: Sun, 31 Dec 2023 19:47:44 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782b3d5f625ef2fa012035de967d5c478fdd4e2a1f3e953db8e34e475ea9eff7`  
		Last Modified: Sun, 31 Dec 2023 19:47:45 GMT  
		Size: 19.2 MB (19189025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:1495fc90f144ce0408f6e256f489d7fd3dc43c00b0ba7caaf2389b0f00c5f6f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 KB (31824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d742346556948c98b8f39eaee23b9c7d3134f56dc89424679964d534b28367d6`

```dockerfile
```

-	Layers:
	-	`sha256:57b8ca6fbffa05bd70b5e50712241abce58cfad9be2d17d422fbef43293263ab`  
		Last Modified: Sun, 31 Dec 2023 19:47:42 GMT  
		Size: 31.8 KB (31824 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-fpm-alpine3.18` - linux; arm variant v7

```console
$ docker pull drupal@sha256:5bc76549e3340c8d6ebf241aa1ca31bd641ada8952ed14ac8be29c6a135d3220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50611396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b42dc5fc673b13505fe7754af2ea2135aaba4c1f9c27f24db8983ae216fc17`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Thu, 30 Nov 2023 22:58:53 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 05 Dec 2023 00:36:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 05 Dec 2023 00:36:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_VERSION=8.3.1
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.1.tar.xz.asc
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_SHA256=56445b1771b2ba5b7573453f9e8a9451e2d810b1741a352fa05259733b1e9758
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 05 Dec 2023 00:36:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 05 Dec 2023 00:36:09 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 05 Dec 2023 00:36:09 GMT
RUN docker-php-ext-enable sodium
# Tue, 05 Dec 2023 00:36:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 05 Dec 2023 00:36:09 GMT
WORKDIR /var/www/html
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 05 Dec 2023 00:36:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Dec 2023 00:36:09 GMT
EXPOSE 9000
# Tue, 05 Dec 2023 00:36:09 GMT
CMD ["php-fpm"]
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
ENV DRUPAL_VERSION=10.2.0-rc1
# Tue, 05 Dec 2023 00:36:09 GMT
WORKDIR /opt/drupal
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2952d7a17ff3c6e07d09737b9b4aa1666b8a80ce6376de09203883260011487b`  
		Last Modified: Tue, 12 Dec 2023 22:37:12 GMT  
		Size: 2.5 MB (2528496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860b046a1e57ad92d9b8a7b74d56a87953677b5cc11c995d1c7a2f8cf59b70ee`  
		Last Modified: Tue, 12 Dec 2023 22:37:11 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88aeb612e7437063efb5da34b46a1f5b3e345e92aab4681d6a3590d9d35f547`  
		Last Modified: Tue, 12 Dec 2023 22:37:11 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe35b9cca7be0d192ae0f5f755bd2de933942ebfecc88dace645877fe319ed57`  
		Last Modified: Thu, 28 Dec 2023 02:50:23 GMT  
		Size: 12.5 MB (12465376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ff1af493d85a4ba08f3c363c0fe0d5fa20c17f374625971bc3c9c52999e985`  
		Last Modified: Thu, 28 Dec 2023 02:50:22 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f15f4842151ae4b22b7265e8092f65fcc5638861585de01a6e333cec7058ac`  
		Last Modified: Thu, 28 Dec 2023 02:50:50 GMT  
		Size: 11.1 MB (11066132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36b7051b3cc4200507f8bc8a76e82c1ecfd0a5b8dd10a24df6e32dfdba9230c`  
		Last Modified: Thu, 28 Dec 2023 02:50:47 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1598d99920de85764a7cbdb906dac8fc45c31fa47f0949a8e3d20e544591ad72`  
		Last Modified: Thu, 28 Dec 2023 02:50:47 GMT  
		Size: 18.8 KB (18778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178160ba7441d72eecc8f769379889bdbacd4315dceb7007b42975138be03e82`  
		Last Modified: Thu, 28 Dec 2023 02:50:47 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff97c53215d96478f7faebfc3261eb8d10205be470ec9d70bf624f137b7a52f`  
		Last Modified: Thu, 28 Dec 2023 08:27:23 GMT  
		Size: 1.7 MB (1723490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7642112a00b7fd161d77a31f62330d7913c835719533126dea8c9a1c0e1e4b4c`  
		Last Modified: Thu, 28 Dec 2023 08:27:23 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ce81910d8da6ed5eabdbfeca9a933ab19e84a0b3d5272133268c60fb58a733`  
		Last Modified: Thu, 28 Dec 2023 08:27:23 GMT  
		Size: 705.2 KB (705205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d720937589815044fbcbd23391489e30d81a09652973465f4a1fb5e20038fb`  
		Last Modified: Thu, 28 Dec 2023 08:27:23 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5defb2dabfb063e7ecd23ddd9cb11ed2326544e0c3a3ffbf2b702625500321a3`  
		Last Modified: Thu, 28 Dec 2023 08:27:25 GMT  
		Size: 19.2 MB (19188835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:30adc3e38fa264a62adf782f33092dce396c21e7e98571da7d33020a6e0d1c5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.5 KB (312472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88de1be21c6b1a5ff85959e67e299ecc7c9869846e28659ff95e1c598b0c793`

```dockerfile
```

-	Layers:
	-	`sha256:ce1d7326bb2971ce656798f4b97c19b45d14b1893ebaa2d78e6e11d243508d3a`  
		Last Modified: Thu, 28 Dec 2023 08:27:21 GMT  
		Size: 280.4 KB (280433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93149b0675139098a0dfade93124b07d3585da4b6dbc0e72e3293deb4bc0006b`  
		Last Modified: Thu, 28 Dec 2023 08:27:21 GMT  
		Size: 32.0 KB (32039 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-fpm-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:da35dfa9b54b15a3bafa3426b70522756e6d19ffbcdad3a1f25050ac416111e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54152012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0f0a79c8880226a469ae73b6879538b537a239a285685a9008612066c884e2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Thu, 30 Nov 2023 23:28:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 05 Dec 2023 00:36:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 05 Dec 2023 00:36:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_VERSION=8.3.1
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.1.tar.xz.asc
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_SHA256=56445b1771b2ba5b7573453f9e8a9451e2d810b1741a352fa05259733b1e9758
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 05 Dec 2023 00:36:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 05 Dec 2023 00:36:09 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 05 Dec 2023 00:36:09 GMT
RUN docker-php-ext-enable sodium
# Tue, 05 Dec 2023 00:36:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 05 Dec 2023 00:36:09 GMT
WORKDIR /var/www/html
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 05 Dec 2023 00:36:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Dec 2023 00:36:09 GMT
EXPOSE 9000
# Tue, 05 Dec 2023 00:36:09 GMT
CMD ["php-fpm"]
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
ENV DRUPAL_VERSION=10.2.0-rc1
# Tue, 05 Dec 2023 00:36:09 GMT
WORKDIR /opt/drupal
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9493d390846313743a61bb9fd10069c0615ed8474da609a9a62ef2ae3a07d6`  
		Last Modified: Tue, 12 Dec 2023 23:01:30 GMT  
		Size: 2.7 MB (2721137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a094d8333de010a9ce81148984a52cc40090c05dbbf5caf82c5be8a98d8d7f`  
		Last Modified: Tue, 12 Dec 2023 23:01:28 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef6120775a4798753155fc2c5b38706e5d6351f725e1a504527d9ff5db74921`  
		Last Modified: Tue, 12 Dec 2023 23:01:28 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7ec156b16d518d136fcd316dee8fcf1952f7844da9684e112fbff2bbcb5f3f`  
		Last Modified: Thu, 28 Dec 2023 00:34:21 GMT  
		Size: 12.5 MB (12465355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7bc98c7451662127fd0738132416238b1826f0fd2f3f1e78db0d17fe4f6b87`  
		Last Modified: Thu, 28 Dec 2023 00:34:21 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f4024388e425a9b434eb6f23e45a1f3c10c26dcd4e3e778a2e241cb970454c`  
		Last Modified: Thu, 28 Dec 2023 00:34:46 GMT  
		Size: 13.0 MB (12993976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d601e216aafa1fb9f6a35af1a07894525b5b5a179dd79ae27eb225e8ffb06da`  
		Last Modified: Thu, 28 Dec 2023 00:34:44 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9d1db46904d468534edb6b7a80cf2a6af5cdff2cd82c06f70b557d01c4911e`  
		Last Modified: Thu, 28 Dec 2023 00:34:44 GMT  
		Size: 18.7 KB (18745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d57edeb81fd4d07bbe18f21dbfaafe916d51aa8cc74e11f893a3576447858c`  
		Last Modified: Thu, 28 Dec 2023 00:34:44 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16db4b73f25b9f4a0e14c38fe00baf05de84b206138055f3593e6965435a0a7`  
		Last Modified: Thu, 28 Dec 2023 05:30:09 GMT  
		Size: 2.7 MB (2711365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7a21506fb75e0f0e542c4cc05fad7637f426fbe86719c45aa9896b860f4e8b`  
		Last Modified: Thu, 28 Dec 2023 05:30:10 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c56242a90a9338c56f2e2e74f883d5f72a88fe7d11e369930082035da29a0dd`  
		Last Modified: Thu, 28 Dec 2023 05:30:10 GMT  
		Size: 705.2 KB (705209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17a7007e6c1f01410af269a8951885593107a6bdd1a6d789b348aba88e0dcee`  
		Last Modified: Thu, 28 Dec 2023 05:30:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53e71c2ac5ee15a9bcda2169e2d1a9e725658e384a52187af88e0e40627960b`  
		Last Modified: Thu, 28 Dec 2023 05:30:11 GMT  
		Size: 19.2 MB (19189113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:4a9c832a1843d22d13ccdf5ea06495a9f73b1c0230bbd33d1e9cc6a8f2f83843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 KB (310732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83b2caf35a31dc97e5d18bc6d884131de3107d2d33b756d9b53d9dd97fef07d`

```dockerfile
```

-	Layers:
	-	`sha256:6ec54681157649eb7f9f597941aa5997192907a49922d2295567d5df20e09e29`  
		Last Modified: Thu, 28 Dec 2023 07:20:41 GMT  
		Size: 280.4 KB (280414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e008aa52e9e778f4f0ed287bc77146276011f5714a75ba1e692f51618cab255`  
		Last Modified: Thu, 28 Dec 2023 07:20:41 GMT  
		Size: 30.3 KB (30318 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-fpm-alpine3.18` - linux; 386

```console
$ docker pull drupal@sha256:33f8d301ec82eb3f49563bc2d382b56c22cd909520cff2582401312478cd4da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53899211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924ae762beb99b5fde6e01f52405aabb4f3865790cdfd9537f9b76c220cb2c4c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 01 Dec 2023 02:03:44 GMT
ADD file:92902088cd15ed8f5dca2f7fc6570fb4e4824fac8b09e091c88e96bbd0ca814b in / 
# Fri, 01 Dec 2023 02:03:44 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 02:05:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 05 Dec 2023 00:36:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 05 Dec 2023 00:36:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_VERSION=8.3.1
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.1.tar.xz.asc
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_SHA256=56445b1771b2ba5b7573453f9e8a9451e2d810b1741a352fa05259733b1e9758
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 05 Dec 2023 00:36:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 05 Dec 2023 00:36:09 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 05 Dec 2023 00:36:09 GMT
RUN docker-php-ext-enable sodium
# Tue, 05 Dec 2023 00:36:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 05 Dec 2023 00:36:09 GMT
WORKDIR /var/www/html
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 05 Dec 2023 00:36:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Dec 2023 00:36:09 GMT
EXPOSE 9000
# Tue, 05 Dec 2023 00:36:09 GMT
CMD ["php-fpm"]
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
ENV DRUPAL_VERSION=10.2.0-rc1
# Tue, 05 Dec 2023 00:36:09 GMT
WORKDIR /opt/drupal
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:4966a8bd129b0a6adf93dc295a8fbe8f665d3194a684a5ce199c1c3596dbf3d9`  
		Last Modified: Fri, 01 Dec 2023 02:04:18 GMT  
		Size: 3.2 MB (3238831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a0db04108a3491da6930962cfddd8b7616fe0b734f222e1ae96b23bf4727c8`  
		Last Modified: Wed, 13 Dec 2023 00:35:28 GMT  
		Size: 2.7 MB (2727229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09ad542fe3d1d3c763ba1901995b27dad8eb44b5135977d67a171e85514bcb8`  
		Last Modified: Wed, 13 Dec 2023 00:35:27 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b16ecefd5db50b00edcce1cec58169026bac36c6e8cf30723f81c7c0fc7b1b3`  
		Last Modified: Wed, 13 Dec 2023 00:35:27 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e022bc8663018ee7c4f06161a3e0b5fe9f2cb10fac99e11ca8b8ecf566479118`  
		Last Modified: Thu, 28 Dec 2023 02:18:04 GMT  
		Size: 12.5 MB (12465360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fc343882b793acc2c55356ee4549035240ee17f0e4b0e2f902d1da29a09863`  
		Last Modified: Thu, 28 Dec 2023 02:18:04 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250c9b54a9dff5d7e97a1550d083a3a09c2b2313db3d748085092596c38942b2`  
		Last Modified: Thu, 28 Dec 2023 02:18:33 GMT  
		Size: 13.1 MB (13107239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be93536199ea784b6bc193635804e9304c75ee7edcd3f675cd5d6b445665f772`  
		Last Modified: Thu, 28 Dec 2023 02:18:30 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2e7bf3b92582e600d093505a52ed47c0050a34fa8797a35715621808559dba`  
		Last Modified: Thu, 28 Dec 2023 02:18:30 GMT  
		Size: 18.9 KB (18933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a5613b90314f7d815d61d4d3519ebddb799503692999fd42e58784f5e24d29`  
		Last Modified: Thu, 28 Dec 2023 02:18:30 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef81c541b549bbcec416d006fe05e955853b2d4fc530354b8d42f3b5de480fb3`  
		Last Modified: Thu, 28 Dec 2023 06:49:09 GMT  
		Size: 2.4 MB (2433258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdc5c8a7709eafc2f77f90f101cf8fb4c185d6b589f5b12287cd3b733ca8747`  
		Last Modified: Thu, 28 Dec 2023 06:49:09 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563bb01a060aad05c86110740dd3cb63dabf7da2eb9e3aa8e56432659f9fd641`  
		Last Modified: Thu, 28 Dec 2023 06:49:09 GMT  
		Size: 705.2 KB (705207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb34e63492c31e9baa6424b29255b454f9835da108f59d1206bc23b29dce393c`  
		Last Modified: Thu, 28 Dec 2023 06:49:09 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b3a405803bd882c916d1b06a4a48d02f73f7198d571d6ead5f29ca9f40e9a7`  
		Last Modified: Thu, 28 Dec 2023 06:49:11 GMT  
		Size: 19.2 MB (19189074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:4d8b03a1fbac4f1c47c5a861295093a94097901700f41239ab7579cb644e62d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.0 KB (317036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f01dd88b2d5bcfb4be59182439c4a96fe868ce924efc25ce05e6a852f60fe0`

```dockerfile
```

-	Layers:
	-	`sha256:752001d94648431492a2aa766b7ae7443088551c5363e14dab00c78d6257e614`  
		Last Modified: Thu, 28 Dec 2023 06:49:07 GMT  
		Size: 282.9 KB (282861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18c20ea0a1b27211520b4d4de3ce0cfbf71d90961c868bcda159f95a196da64b`  
		Last Modified: Thu, 28 Dec 2023 06:49:07 GMT  
		Size: 34.2 KB (34175 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-fpm-alpine3.18` - linux; ppc64le

```console
$ docker pull drupal@sha256:d7802e6567e31fc6f53a6410572dbec350318c24b006e0eedca1724139b6a58c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54112102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31d18fcf3e5643794c27dbcb4070e440e2891232bea6a4ce99be430c9a8f2177`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Thu, 30 Nov 2023 23:37:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 05 Dec 2023 00:36:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 05 Dec 2023 00:36:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_VERSION=8.3.1
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.1.tar.xz.asc
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_SHA256=56445b1771b2ba5b7573453f9e8a9451e2d810b1741a352fa05259733b1e9758
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 05 Dec 2023 00:36:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 05 Dec 2023 00:36:09 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 05 Dec 2023 00:36:09 GMT
RUN docker-php-ext-enable sodium
# Tue, 05 Dec 2023 00:36:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 05 Dec 2023 00:36:09 GMT
WORKDIR /var/www/html
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 05 Dec 2023 00:36:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Dec 2023 00:36:09 GMT
EXPOSE 9000
# Tue, 05 Dec 2023 00:36:09 GMT
CMD ["php-fpm"]
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
ENV DRUPAL_VERSION=10.2.0-rc1
# Tue, 05 Dec 2023 00:36:09 GMT
WORKDIR /opt/drupal
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ae471a7c4df6c524f1c2aea3fd05694ae08d09a91e2cfe13bfe016f043f841`  
		Last Modified: Tue, 12 Dec 2023 22:42:57 GMT  
		Size: 2.8 MB (2768111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e0edd009540eef1f3db13dcabb2a9555108334728d35cc262b72d194614c05`  
		Last Modified: Tue, 12 Dec 2023 22:42:56 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e3ae20a075c13074416585923c54fe9bd73fb76e5e7d29cf90c9601679edb3`  
		Last Modified: Tue, 12 Dec 2023 22:42:57 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5457b3f2731b7d2cfc710d3077d32ed5907c30913edd70ba03da11e8b18e6f76`  
		Last Modified: Thu, 28 Dec 2023 01:01:46 GMT  
		Size: 12.5 MB (12465343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a942e6da7561478672196249f46b06fc331485ea7cfbde4e91609ff95e3906`  
		Last Modified: Thu, 28 Dec 2023 01:01:45 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a004c1859ef03c52ff23cc3d13150f18b70b43db35bb3b3c410f6e244bfffd77`  
		Last Modified: Thu, 28 Dec 2023 01:02:17 GMT  
		Size: 13.3 MB (13344827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7283dcdd7f76222d1d948e5636294b218ce282c0774a896f1a81a61139033c`  
		Last Modified: Thu, 28 Dec 2023 01:02:14 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aeb74b00e6f91ea2463a6165fcb5cccfc97241e4af92b20b9a71c0230d96533`  
		Last Modified: Thu, 28 Dec 2023 01:02:14 GMT  
		Size: 18.7 KB (18734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00df963cafddedb07d64d970e6deda780357da974b54b846153b5ce6daeb29f`  
		Last Modified: Thu, 28 Dec 2023 01:02:14 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b040ca5714f46e8c161b792f80d44b28467a685a3dd89afb593b663fbb9ca48`  
		Last Modified: Thu, 28 Dec 2023 05:30:20 GMT  
		Size: 2.3 MB (2258363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755c9e3c7ec42aa1b1557ca8b413148ac89affae5cdbf9da037490da5405a5cd`  
		Last Modified: Thu, 28 Dec 2023 05:30:20 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946a8d222bbba2f6897e2e0869f2b7f934b54541aec0ab556bf8f0d5d26c5c20`  
		Last Modified: Thu, 28 Dec 2023 05:30:21 GMT  
		Size: 705.2 KB (705211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50dd8d74d7c1bbfd0a75c3163e152ec3df2caed44afb51a6d1dff78560f16d3b`  
		Last Modified: Thu, 28 Dec 2023 05:30:20 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32303c42106ebbb1bbf3eac1ad0be296ff6fed15bc5da4b892b1c3a8c47525d`  
		Last Modified: Thu, 28 Dec 2023 05:30:22 GMT  
		Size: 19.2 MB (19189105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:e77cf5ed6ab430cbc38cb73223bad0fb92a2007946ebc4922cf270fd0b2b22d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.1 KB (309147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4405b2c3c489d3ed4dd0d7f6ffeb4d9b4c47b42a7ba962f1ae0e2ed2d5c89404`

```dockerfile
```

-	Layers:
	-	`sha256:a36193e5eaac3983a8362d30a5900e647674fcdaf76fbbd8c393d3e9682501c5`  
		Last Modified: Thu, 28 Dec 2023 07:11:26 GMT  
		Size: 278.8 KB (278797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:117776c5c02a53378f2e72645cf1d9db05d831e224aeb632512663a44dc577b7`  
		Last Modified: Thu, 28 Dec 2023 07:11:26 GMT  
		Size: 30.4 KB (30350 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-fpm-alpine3.18` - linux; s390x

```console
$ docker pull drupal@sha256:bb76c7d81c8f1e4f60ff5d24d20538c1a2b65e66ba2524a95b97e4e0ca041399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52480303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea77a5d0fff8aae46840495635aa304920ed5c16c8bc3463a5e3d15a1ea1910`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Thu, 30 Nov 2023 22:45:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 05 Dec 2023 00:36:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 05 Dec 2023 00:36:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_VERSION=8.3.1
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.1.tar.xz.asc
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_SHA256=56445b1771b2ba5b7573453f9e8a9451e2d810b1741a352fa05259733b1e9758
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 05 Dec 2023 00:36:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 05 Dec 2023 00:36:09 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 05 Dec 2023 00:36:09 GMT
RUN docker-php-ext-enable sodium
# Tue, 05 Dec 2023 00:36:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 05 Dec 2023 00:36:09 GMT
WORKDIR /var/www/html
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 05 Dec 2023 00:36:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Dec 2023 00:36:09 GMT
EXPOSE 9000
# Tue, 05 Dec 2023 00:36:09 GMT
CMD ["php-fpm"]
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
ENV DRUPAL_VERSION=10.2.0-rc1
# Tue, 05 Dec 2023 00:36:09 GMT
WORKDIR /opt/drupal
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9d8a04e5ffd20d63f8efed3950a23dcb2ee8c86112d44078098827cc0a057c`  
		Last Modified: Tue, 12 Dec 2023 22:07:56 GMT  
		Size: 2.8 MB (2792794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc1eecd649c3114a4174ae109f3249b22dd301b21fff70ecf137592a983070c`  
		Last Modified: Tue, 12 Dec 2023 22:07:55 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4c869f81ed8d85aa688c56443814d8b1a0a9691bf3d2e9ce43691b73186c28`  
		Last Modified: Tue, 12 Dec 2023 22:07:55 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f920e896211f665d6e09da1eed1d5dcc1041523f031ecbd6b3e88ffcdf0f57`  
		Last Modified: Wed, 27 Dec 2023 23:42:22 GMT  
		Size: 12.5 MB (12465353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31696582b01a4f9b8164f0cac30a960a989ef3aede565cb552d3ef6a65d3870a`  
		Last Modified: Wed, 27 Dec 2023 23:42:22 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88c046fc40c3a218224287eb731b55276e9233e1108578c661b0ff99b4b2dd6`  
		Last Modified: Wed, 27 Dec 2023 23:42:38 GMT  
		Size: 12.1 MB (12077096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85bd838f47df07d5dcdfea87e32d0a68807d8fa2f8b5ddf8b8b3f549dee3db8`  
		Last Modified: Wed, 27 Dec 2023 23:42:36 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9eb5efae41334ac1ea1c7d7396e4b7c6793f44513bf908774f367208c4ef40`  
		Last Modified: Wed, 27 Dec 2023 23:42:36 GMT  
		Size: 18.8 KB (18775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d959da16c48c763ddfd313a0426eb96101f7127e62cb5a483eb5f3807323be`  
		Last Modified: Wed, 27 Dec 2023 23:42:36 GMT  
		Size: 9.2 KB (9174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62c979f5954bcd596e431e844a1b6cac250a0fd45ab71ba50d07bbb09affbac`  
		Last Modified: Thu, 28 Dec 2023 03:02:02 GMT  
		Size: 2.0 MB (2000431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565d27077473b0d908ac08ce4bbbc44481c34490ec9356d47baef5c0c0c14c83`  
		Last Modified: Thu, 28 Dec 2023 03:02:02 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb076b80cd00ee70695c7f9f55cadab478f08746e1e17e86b1beebc161716e5a`  
		Last Modified: Thu, 28 Dec 2023 03:02:02 GMT  
		Size: 705.2 KB (705206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ce9950f11c5ed3c02c062b1568a5ebab30c2f2630a9f9bd1447d593e802123`  
		Last Modified: Thu, 28 Dec 2023 03:02:03 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971771aa91d92016715eb5b9ac26503a81739835d5793c3dd31ba626e7abcb2a`  
		Last Modified: Thu, 28 Dec 2023 03:02:03 GMT  
		Size: 19.2 MB (19189119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:e65ffeec51bb60eeeb99f65276c6d575b3e63a76253bb81845bf090d2201cb10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 KB (310704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5943157b77b89273e755c166ee70b8a00434c2531c0ba7324a69dfb93e163017`

```dockerfile
```

-	Layers:
	-	`sha256:5608d8dacc5b461f81c45578c3dc4f43761ba6a930b61445e16c9014b6dcd99d`  
		Last Modified: Thu, 28 Dec 2023 03:02:01 GMT  
		Size: 278.8 KB (278769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd524220c60dd4d67735b521844a897ff85f51add340b4d9bb6721ed8756003d`  
		Last Modified: Thu, 28 Dec 2023 03:02:01 GMT  
		Size: 31.9 KB (31935 bytes)  
		MIME: application/vnd.in-toto+json
