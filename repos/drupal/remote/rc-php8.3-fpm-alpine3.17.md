## `drupal:rc-php8.3-fpm-alpine3.17`

```console
$ docker pull drupal@sha256:4b13d098cd26c85da28e3f3140273182f279adfbb5f7d9f2699d390b69288652
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `drupal:rc-php8.3-fpm-alpine3.17` - linux; amd64

```console
$ docker pull drupal@sha256:bcd95da801a4714eefa683aedce24fe1afeb40a28b69d881a8968d61c9ca3ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52893553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ffb0a72d5deee91e7a43f921c100697a072cdf205b816096b1756a24d97e47`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Thu, 30 Nov 2023 23:44:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 30 Nov 2023 23:44:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 30 Nov 2023 23:44:05 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 30 Nov 2023 23:44:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 30 Nov 2023 23:44:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 30 Nov 2023 23:44:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 30 Nov 2023 23:44:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 30 Nov 2023 23:44:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 30 Nov 2023 23:44:06 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 30 Nov 2023 23:44:06 GMT
ENV PHP_VERSION=8.3.0
# Thu, 30 Nov 2023 23:44:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Thu, 30 Nov 2023 23:44:06 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Thu, 30 Nov 2023 23:44:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 30 Nov 2023 23:44:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 30 Nov 2023 23:51:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 30 Nov 2023 23:51:34 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 30 Nov 2023 23:51:35 GMT
RUN docker-php-ext-enable sodium
# Thu, 30 Nov 2023 23:51:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 30 Nov 2023 23:51:36 GMT
WORKDIR /var/www/html
# Thu, 30 Nov 2023 23:51:36 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 30 Nov 2023 23:51:36 GMT
STOPSIGNAL SIGQUIT
# Thu, 30 Nov 2023 23:51:36 GMT
EXPOSE 9000
# Thu, 30 Nov 2023 23:51:36 GMT
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
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b247515625fa62cbad8d65cc266af9543840a38f229e9442b2944001963f22bf`  
		Last Modified: Fri, 01 Dec 2023 00:43:34 GMT  
		Size: 1.9 MB (1918200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2e9fba79c42503c63db971b002c3140e17f01e70c115971879dafff3f91f56`  
		Last Modified: Fri, 01 Dec 2023 00:43:33 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70db101bade6cf80bb8fdb2aea594b74557f6498ed68147b041ebfc7d961c6ef`  
		Last Modified: Fri, 01 Dec 2023 00:43:33 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411662ef0505b88cd067fb97a87cd04fb74274fa475354c497cb95b507b99ace`  
		Last Modified: Fri, 01 Dec 2023 00:43:32 GMT  
		Size: 12.5 MB (12451821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127a0d7f809c3fcf7028bcf7b3b526e18157ac1791543bae533d120a93ba15ac`  
		Last Modified: Fri, 01 Dec 2023 00:43:31 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad50bc887d9c84b95faddec348c9a661860587c695744174053b8395728e54da`  
		Last Modified: Fri, 01 Dec 2023 00:43:57 GMT  
		Size: 13.0 MB (13005556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b07deefe63a06f9aaea82e1c8f92f9227e5a30778e353bff746945cdcdcda29`  
		Last Modified: Fri, 01 Dec 2023 00:43:55 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f118ffb4844fe3c99f87bc21df68e02a363f361ba7db230af40287abe49c778`  
		Last Modified: Fri, 01 Dec 2023 00:43:55 GMT  
		Size: 19.0 KB (18982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fbcdfed541e9c5ea4b1e26aaa0d8b926d0baff0746d7e628ae4a6ae3d02cb86`  
		Last Modified: Fri, 01 Dec 2023 00:43:55 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c0ae3b73bbc50025c0fe7bbaa1ac74d72d0044a53962007daf3190af77dc0e`  
		Last Modified: Mon, 11 Dec 2023 19:13:43 GMT  
		Size: 2.2 MB (2211166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6da313c406b03f0410e6913749185fab6cb700566582b224932f41341aa6b25`  
		Last Modified: Mon, 11 Dec 2023 19:13:42 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89e768ba07dcbf9a378bd1c5240ec8c2ff9c2d0882046cc3b02b37a1e12ce4a`  
		Last Modified: Mon, 11 Dec 2023 19:13:43 GMT  
		Size: 705.2 KB (705208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c2bef281038d4bdf9412b19ac7b33b4780e96534f458b6d8fd641a5ff974ff`  
		Last Modified: Mon, 11 Dec 2023 19:13:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4603c0d068246da291933deaf8af4f5cbcce8c66e3de2184119f386862481c00`  
		Last Modified: Mon, 11 Dec 2023 19:13:44 GMT  
		Size: 19.2 MB (19189214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-fpm-alpine3.17` - unknown; unknown

```console
$ docker pull drupal@sha256:d63cbc1d0517040995ec6919e0fe46b73bc8f2914ac209e47061083b3229aadb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.1 KB (315120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38c5f4a49e058417d08daacd67bb4d59723017b4737084f31462e7d3c8140e73`

```dockerfile
```

-	Layers:
	-	`sha256:623f64e7bf67f47ade0b0bb80a2f3f602b7df2294dbf5df4f77b2d6da7fd7c2f`  
		Last Modified: Mon, 11 Dec 2023 19:13:42 GMT  
		Size: 280.9 KB (280913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05410305388ecbcc51e334b2e45e24be51bdb0c8917d45bf48d3fd64881a16ba`  
		Last Modified: Mon, 11 Dec 2023 19:13:42 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-fpm-alpine3.17` - linux; arm variant v6

```console
$ docker pull drupal@sha256:5ee4faf943eb53fed32c6224536c9c2a2c357fb9ee5ccaa69c6cfbf5595ed0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50882703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90e376c2df6e4d7318ee6472bdcfb4e31c4995c08163d9c544e9fdd3e4c8e65`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:21 GMT
ADD file:90d3bdc6a557ead63796de0110e2fda87e65aa091070cbae612dfb2126568253 in / 
# Thu, 30 Nov 2023 22:49:21 GMT
CMD ["/bin/sh"]
# Thu, 30 Nov 2023 23:26:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 30 Nov 2023 23:26:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 30 Nov 2023 23:26:44 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 30 Nov 2023 23:26:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 30 Nov 2023 23:26:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 30 Nov 2023 23:26:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 30 Nov 2023 23:26:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 30 Nov 2023 23:26:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 30 Nov 2023 23:26:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 30 Nov 2023 23:26:45 GMT
ENV PHP_VERSION=8.3.0
# Thu, 30 Nov 2023 23:26:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Thu, 30 Nov 2023 23:26:45 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Thu, 30 Nov 2023 23:26:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 30 Nov 2023 23:26:52 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 30 Nov 2023 23:34:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 30 Nov 2023 23:34:30 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 30 Nov 2023 23:34:31 GMT
RUN docker-php-ext-enable sodium
# Thu, 30 Nov 2023 23:34:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 30 Nov 2023 23:34:31 GMT
WORKDIR /var/www/html
# Thu, 30 Nov 2023 23:34:32 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 30 Nov 2023 23:34:32 GMT
STOPSIGNAL SIGQUIT
# Thu, 30 Nov 2023 23:34:32 GMT
EXPOSE 9000
# Thu, 30 Nov 2023 23:34:32 GMT
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
	-	`sha256:f0440ff44d712e5fc701b84856116589b428157893ac461b633b1ab30b627eed`  
		Last Modified: Thu, 30 Nov 2023 22:49:52 GMT  
		Size: 3.1 MB (3113003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ea589cfbf153b254cdbbe3b864a1b7361db98d12af5fc8a386a4cc35784e0c`  
		Last Modified: Fri, 01 Dec 2023 00:16:32 GMT  
		Size: 1.9 MB (1901973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e61b9a7d18c8b206dfb5aee1618943ed51f3b10f9f0ba21e7b24afd46b9295`  
		Last Modified: Fri, 01 Dec 2023 00:16:32 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e43df84dfc0b8697a4c91ce52973ee988ec182eaa89d4bfd36124f353a5e5ba3`  
		Last Modified: Fri, 01 Dec 2023 00:16:32 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908b8cfafc247a8db433f2e1b0f759edacaf80110ea4ea3a86bb154dc2454e6e`  
		Last Modified: Fri, 01 Dec 2023 00:16:30 GMT  
		Size: 12.5 MB (12451811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9687d14f96ea438ef8419d7e74dcfdaa9365a80f66c54908cf4a1f600e6900d9`  
		Last Modified: Fri, 01 Dec 2023 00:16:30 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef5860245087878bcf90c21e551abbb436789ae77003ae957800a3f3e0f3491`  
		Last Modified: Fri, 01 Dec 2023 00:16:56 GMT  
		Size: 11.8 MB (11807179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba7148600b2d61a39af2d7df537c753605b4db0ddc3020856b4fad59120de87`  
		Last Modified: Fri, 01 Dec 2023 00:16:54 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b1efada63e250062a4b2aee61ad948693220c67c30e52ee2a331873a4e57aa8`  
		Last Modified: Fri, 01 Dec 2023 00:16:53 GMT  
		Size: 18.8 KB (18763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9288a7577ada8a0bd0901cbdd45659e96f8b1650f19504c339e020a66e5f78`  
		Last Modified: Fri, 01 Dec 2023 00:16:54 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a7a1b42765e47315fafb49369d6fd0000e8585c37885eea07fb4e56d1b8c0fd`  
		Last Modified: Mon, 11 Dec 2023 20:25:58 GMT  
		Size: 1.7 MB (1681509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd655ca5b8805b5f808b60575e72d9ececca4d11a6ddabe1d3b8dd9daa972ac`  
		Last Modified: Mon, 11 Dec 2023 20:25:57 GMT  
		Size: 312.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d01617a897ad314578326af0f54affec02878612279e817e295b7a7c10636c`  
		Last Modified: Mon, 11 Dec 2023 20:25:58 GMT  
		Size: 705.2 KB (705207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87db72d317f0aca9188389d281a11384b1dab936b50f0356945c152a83b3a49`  
		Last Modified: Mon, 11 Dec 2023 20:25:57 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0ec9ed37ef8a43eb99f6c368b19c9001f79a0b5c4039b3a7ac52cff93c2f1a`  
		Last Modified: Mon, 11 Dec 2023 20:26:05 GMT  
		Size: 19.2 MB (19189182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:rc-php8.3-fpm-alpine3.17` - linux; arm variant v7

```console
$ docker pull drupal@sha256:cb6bcf921fcfc99521c839a6f8afc3d53273def0a2321206c3b43c72e657f3de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49648380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a16a05b47319bc55378e5b59072a0ebba4d294e8f738b3ee953fa9849f65bd1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:34 GMT
ADD file:02a6ccbee2a71a547141a8480f3a3912c7bb0934df31124f4a4720204d326698 in / 
# Thu, 30 Nov 2023 22:49:34 GMT
CMD ["/bin/sh"]
# Thu, 30 Nov 2023 23:06:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 30 Nov 2023 23:06:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 30 Nov 2023 23:06:50 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 30 Nov 2023 23:06:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 30 Nov 2023 23:06:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 30 Nov 2023 23:06:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 30 Nov 2023 23:06:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 30 Nov 2023 23:06:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 30 Nov 2023 23:06:51 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 30 Nov 2023 23:06:51 GMT
ENV PHP_VERSION=8.3.0
# Thu, 30 Nov 2023 23:06:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Thu, 30 Nov 2023 23:06:51 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Thu, 30 Nov 2023 23:07:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 30 Nov 2023 23:07:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 30 Nov 2023 23:12:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 30 Nov 2023 23:12:37 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 30 Nov 2023 23:12:38 GMT
RUN docker-php-ext-enable sodium
# Thu, 30 Nov 2023 23:12:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 30 Nov 2023 23:12:38 GMT
WORKDIR /var/www/html
# Thu, 30 Nov 2023 23:12:39 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 30 Nov 2023 23:12:39 GMT
STOPSIGNAL SIGQUIT
# Thu, 30 Nov 2023 23:12:39 GMT
EXPOSE 9000
# Thu, 30 Nov 2023 23:12:39 GMT
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
	-	`sha256:d4ee79c42f17f258e1c67dc32e0776c934799d208cd0a9b6264f65d60f1a26fc`  
		Last Modified: Thu, 30 Nov 2023 22:50:08 GMT  
		Size: 2.9 MB (2869713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1f6a0f0c871bb0bdf558a5c951f8b9b39e3951c1295c36a2a80498cbd73aff`  
		Last Modified: Thu, 30 Nov 2023 23:59:31 GMT  
		Size: 1.8 MB (1751708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85150459f6b67a25c1e5439d10879cd97a5db2564f354dfd90eb4a85ca0eae5b`  
		Last Modified: Thu, 30 Nov 2023 23:59:30 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d843ac528c37f9c4509e60245b64e4ddc00982ba1f5d7ae08681c17e3d9470`  
		Last Modified: Thu, 30 Nov 2023 23:59:30 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d29def7c3904c004ae8f5b2ba673993d0823e9074ac6a33302f41a9c685dd47`  
		Last Modified: Thu, 30 Nov 2023 23:59:30 GMT  
		Size: 12.5 MB (12451800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db570319a20f7df433ffeaad3dad432d96f583d8cc39457a25c35ea95293170d`  
		Last Modified: Thu, 30 Nov 2023 23:59:28 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e9e4ca1caffe3e4180bc910910fd5e636b993cdfb4a31e0f1c7a9cc17ac6e9`  
		Last Modified: Thu, 30 Nov 2023 23:59:54 GMT  
		Size: 11.1 MB (11099389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f78acc8ea3154c5838ca145ec024e74df50af519be3bf3b96737deed3d45d2`  
		Last Modified: Thu, 30 Nov 2023 23:59:52 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90e8fc9094bcd0b8153682a47af5eadb0c593045e3f195a178aa2bdd7687f81`  
		Last Modified: Thu, 30 Nov 2023 23:59:52 GMT  
		Size: 18.8 KB (18770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e488ad00372b048b389d208346d3efa12f1ec1e53f11bb49120044fd12eb7c5a`  
		Last Modified: Thu, 30 Nov 2023 23:59:52 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73cd190bf1565c7b72cfb83f369d4246d426fab333ee8ed6cec885537472f62c`  
		Last Modified: Tue, 05 Dec 2023 02:19:06 GMT  
		Size: 1.5 MB (1548980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383a13e125c56c21b1215138fc5866012da9e6251236d5fe475e6f072a4c9645`  
		Last Modified: Tue, 05 Dec 2023 02:19:06 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd839511608154bad68be13dae44c1940d86d9cac6f1bc4274126b1c0139f39`  
		Last Modified: Tue, 05 Dec 2023 02:19:07 GMT  
		Size: 705.0 KB (705002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c85e24e3d0bb2be21d7d5bb42a5b54035f7af33582ad6f8968697081695df0`  
		Last Modified: Tue, 05 Dec 2023 02:19:06 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ce4d3dd703786739149559774d8751db1d250d0b01eda4648bd5d5771b2587`  
		Last Modified: Tue, 05 Dec 2023 02:19:08 GMT  
		Size: 19.2 MB (19188947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-fpm-alpine3.17` - unknown; unknown

```console
$ docker pull drupal@sha256:9faf7d13acf2f8e75a6a54185a22eb1dd6c66920039dca9b5f47603b0c0d8673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 KB (310580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24768cad0f85e27e75e0b41d79b5a3e0626333452cafc8c4ef6a8d7f0d36e471`

```dockerfile
```

-	Layers:
	-	`sha256:76bc47178e8e1d076251dd0e1ea14bc59aab9f20cb412c120c68e8ef9ff31722`  
		Last Modified: Tue, 05 Dec 2023 02:19:04 GMT  
		Size: 278.5 KB (278543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f993b4304a7213dd352814c17198b318d21e2a4b47f05c4b52b80ce950cd355b`  
		Last Modified: Tue, 05 Dec 2023 02:19:04 GMT  
		Size: 32.0 KB (32037 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-fpm-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:06d06607fb7eeddd4c88ad169ffc079b26d9941fbad6e8e9ddb3ee92f0b23514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (52995414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e50ced7e60afc5a94e63afb68c26bc2e0e86074f4ed8b07d2c7e7c45233abd`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:07 GMT
ADD file:e5c66967d6570e36da50c9d42dd8f8f55e6c6a65b92c79601ea9e750c076fa2a in / 
# Thu, 30 Nov 2023 23:11:07 GMT
CMD ["/bin/sh"]
# Thu, 30 Nov 2023 23:40:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 30 Nov 2023 23:40:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 30 Nov 2023 23:40:54 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 30 Nov 2023 23:40:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 30 Nov 2023 23:40:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 30 Nov 2023 23:40:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 30 Nov 2023 23:40:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 30 Nov 2023 23:40:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 30 Nov 2023 23:40:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 30 Nov 2023 23:40:55 GMT
ENV PHP_VERSION=8.3.0
# Thu, 30 Nov 2023 23:40:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Thu, 30 Nov 2023 23:40:55 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Thu, 30 Nov 2023 23:41:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 30 Nov 2023 23:41:02 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 30 Nov 2023 23:48:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 30 Nov 2023 23:48:55 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 30 Nov 2023 23:48:56 GMT
RUN docker-php-ext-enable sodium
# Thu, 30 Nov 2023 23:48:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 30 Nov 2023 23:48:56 GMT
WORKDIR /var/www/html
# Thu, 30 Nov 2023 23:48:57 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 30 Nov 2023 23:48:57 GMT
STOPSIGNAL SIGQUIT
# Thu, 30 Nov 2023 23:48:57 GMT
EXPOSE 9000
# Thu, 30 Nov 2023 23:48:57 GMT
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
	-	`sha256:b8180c93b172865af87a7c0e7e3c8bcb139e0d0c92e19c96467ff2cd4c8919ad`  
		Last Modified: Thu, 30 Nov 2023 23:11:45 GMT  
		Size: 3.3 MB (3258348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68106053112d5e6ec79f202c661246c75fcb6cd6fc87e7889731a30c11ba9cc2`  
		Last Modified: Fri, 01 Dec 2023 00:41:30 GMT  
		Size: 1.9 MB (1909305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185ba080aadee17b1bef7a3e0b10d9d40cd743b52620bfce05cd8825094b33ee`  
		Last Modified: Fri, 01 Dec 2023 00:41:29 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be83bc201e8a1bb055e184f413076cd0d92dab89af679e3fcfc353c80ce98cd4`  
		Last Modified: Fri, 01 Dec 2023 00:41:28 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025b26ca4d94f52533bb92e16ee3ae30da9471d75e41414ade451d57640db298`  
		Last Modified: Fri, 01 Dec 2023 00:41:27 GMT  
		Size: 12.5 MB (12451814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1158a3ed4606d574532652a7038890e031624fb73363b305630a867091790578`  
		Last Modified: Fri, 01 Dec 2023 00:41:27 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1743356b9173c90c4863b3b484d26246a2376e29fd4c7d5c5649c8a696843c9e`  
		Last Modified: Fri, 01 Dec 2023 00:41:53 GMT  
		Size: 13.0 MB (12999233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9e2733a71c022b1212b7680d063751729ebf36d3709465338eaf17ac51183d`  
		Last Modified: Fri, 01 Dec 2023 00:41:51 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed3acc2574845e06ab2ed3b9d530dcf274988a343ebdb7cac623641d3cab078`  
		Last Modified: Fri, 01 Dec 2023 00:41:51 GMT  
		Size: 18.8 KB (18781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6ce18901fdcfd383bbc5352075ce87b1371119bacc6cdaba0e92fe87ad5b6b`  
		Last Modified: Fri, 01 Dec 2023 00:41:51 GMT  
		Size: 9.2 KB (9175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3eaa2f279755312023bdb2e021b1b0e7b89d74a6d55a5093d46e60a10ba8da0`  
		Last Modified: Tue, 05 Dec 2023 02:25:34 GMT  
		Size: 2.4 MB (2449839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7496562c7660e6547f04c4bcf0247ac5d57f35d27cb51e0ab0380e42828aa69c`  
		Last Modified: Tue, 05 Dec 2023 02:25:34 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0a434a3ebb18231b332044fa8b7c73bb9652dfa98655afff2d6e16de8237d6`  
		Last Modified: Tue, 05 Dec 2023 02:25:34 GMT  
		Size: 705.0 KB (705001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d05252f88da8f95a6dae36454a7ad06d7fab3e580d7c8f3945a042f97a758c4`  
		Last Modified: Tue, 05 Dec 2023 02:25:34 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838b09dac76814ea5b937a31ae505d80b92953a69cdbf10e32c61b294fb5decb`  
		Last Modified: Tue, 05 Dec 2023 02:25:36 GMT  
		Size: 19.2 MB (19189024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-fpm-alpine3.17` - unknown; unknown

```console
$ docker pull drupal@sha256:4f5b41cd77ceb18a5432d2d4ae4ccc106d3f0ceb651af3e5a2a2d6a1ebbc24ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 KB (310466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33dc50eaef08e0f0d62ba85e132eb08de07e459111680ca0115ec2d987c67c4a`

```dockerfile
```

-	Layers:
	-	`sha256:df6e18935d84bfb49559e57c51d84a4d5b3fbf38fd4a9db4a62065f3aa0e0101`  
		Last Modified: Tue, 05 Dec 2023 02:25:32 GMT  
		Size: 278.5 KB (278524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b6665919a32181083d40ff0da108e1aecb9ddd6e277bb6d008cf369992eb1b9`  
		Last Modified: Tue, 05 Dec 2023 02:25:32 GMT  
		Size: 31.9 KB (31942 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-fpm-alpine3.17` - linux; 386

```console
$ docker pull drupal@sha256:7665af25c3512d3192e5572be0ec441506c85e2b9b054901ff5bd360412ffb73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53410319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3155ca9efa33f90773506c54428e5d8c73e6b56ef4e4e62f9227a5f6bc9b0822`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 01 Dec 2023 02:03:50 GMT
ADD file:4ad1e09b0030ebbf09adcc7c616502a079dc61aff7c6edce2f2ea248cd85b2df in / 
# Fri, 01 Dec 2023 02:03:50 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 02:25:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 01 Dec 2023 02:25:30 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 01 Dec 2023 02:25:31 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 01 Dec 2023 02:25:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 01 Dec 2023 02:25:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 01 Dec 2023 02:25:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 01 Dec 2023 02:25:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 01 Dec 2023 02:25:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 01 Dec 2023 02:25:32 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 01 Dec 2023 02:25:32 GMT
ENV PHP_VERSION=8.3.0
# Fri, 01 Dec 2023 02:25:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Fri, 01 Dec 2023 02:25:33 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Fri, 01 Dec 2023 02:25:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 01 Dec 2023 02:25:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 01 Dec 2023 02:38:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 01 Dec 2023 02:38:53 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 01 Dec 2023 02:38:54 GMT
RUN docker-php-ext-enable sodium
# Fri, 01 Dec 2023 02:38:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 01 Dec 2023 02:38:54 GMT
WORKDIR /var/www/html
# Fri, 01 Dec 2023 02:38:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 01 Dec 2023 02:38:55 GMT
STOPSIGNAL SIGQUIT
# Fri, 01 Dec 2023 02:38:55 GMT
EXPOSE 9000
# Fri, 01 Dec 2023 02:38:55 GMT
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
	-	`sha256:7583c43471b6e056e4cc98119de7f0921ba6ad8cd2645554165c3d9869b344dc`  
		Last Modified: Fri, 01 Dec 2023 02:04:31 GMT  
		Size: 3.4 MB (3414867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c6e64fa2e7ce24846f1f3eabcf60ebc0a9b410169ff76807f242270bc8fe1e`  
		Last Modified: Fri, 01 Dec 2023 04:08:43 GMT  
		Size: 2.0 MB (2035893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c455b231d21569e78e813936eb90e308ad3b6f91462b220c5b0f85547170abe`  
		Last Modified: Fri, 01 Dec 2023 04:08:42 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f684db43ddc9653c5aa5696b3d65429f1a8fdaf1b49711b0aec1281b6e9f4045`  
		Last Modified: Fri, 01 Dec 2023 04:08:42 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d6071bb1edecdef72d0345a7f08afef1ee9beb50246b2b954e99b6a3fdd307`  
		Last Modified: Fri, 01 Dec 2023 04:08:42 GMT  
		Size: 12.5 MB (12451815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df6152e4877dba54edaa9e2cfc0f82c2c1bfa784a9296dcb2f2a61dbb21f42a`  
		Last Modified: Fri, 01 Dec 2023 04:08:40 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe0d760a2cff90a3b96d75d701e662ce08dedf87d040a0a84f1f9540f989077`  
		Last Modified: Fri, 01 Dec 2023 04:09:12 GMT  
		Size: 13.3 MB (13289395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f58b9fdeab567b92b7390db2b22c323c0533ef882f10d17a051cbed38c7eef`  
		Last Modified: Fri, 01 Dec 2023 04:09:08 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c715a8e286975435489bfdc3032c1f57188daec3cff750d4f66c25bddfc276`  
		Last Modified: Fri, 01 Dec 2023 04:09:08 GMT  
		Size: 19.0 KB (18967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e85f1277bd82bbe6ea2e89eaea918e39412ab388f2d56498c005fdfc330794`  
		Last Modified: Fri, 01 Dec 2023 04:09:08 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2814e9fc30d2e4c2d4aacc1e63c96a3eda74d1914bbba10aab0ed82188b9ec5`  
		Last Modified: Tue, 05 Dec 2023 02:11:45 GMT  
		Size: 2.3 MB (2291279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f6d4a598a653f27315d951c14d1f494629e240b2a8982c6bdf3aa82ad553bc`  
		Last Modified: Tue, 05 Dec 2023 02:11:45 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3411b3b5827741acf21bd55fa88fca4d23f87fafabfc36417c67e0b25d81131`  
		Last Modified: Tue, 05 Dec 2023 02:11:46 GMT  
		Size: 705.0 KB (705006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c4d8153326f4eb15cdecce60bfd6c6a7735fc3e1578f313284c1abbd7fbbba`  
		Last Modified: Tue, 05 Dec 2023 02:11:43 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594fef3f415009d648c5cde491eea5e88c6ad6fe87f47e8483f9a6fb8733e2e1`  
		Last Modified: Tue, 05 Dec 2023 02:11:47 GMT  
		Size: 19.2 MB (19189022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-fpm-alpine3.17` - unknown; unknown

```console
$ docker pull drupal@sha256:1e6b32d82efd892f164e37229c87bed51e5bab35d9f05e84fed54737d8665d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 KB (33959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a214c973fb92c2673c35cb5ac4bf35ebeab97b3854305b7f1b45248d24bd4d71`

```dockerfile
```

-	Layers:
	-	`sha256:397bfc08958a2485cf9b7427f63d86a09ddaa29c412aeb887bc8ee72794cb138`  
		Last Modified: Tue, 05 Dec 2023 02:11:44 GMT  
		Size: 34.0 KB (33959 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-fpm-alpine3.17` - linux; ppc64le

```console
$ docker pull drupal@sha256:5b0328e4ddece65bddf7c638c434fdbaa27b729259744a67ad8c89bccd57beda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53133177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942e66dda7c51d41c8bee466d7656d08c954c79d303d1568c0d16285ff863761`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:15 GMT
ADD file:e3eb0ea4f652282ad08228d0d146f33998b9e93641756d780ac0205aa828c070 in / 
# Thu, 30 Nov 2023 23:19:17 GMT
CMD ["/bin/sh"]
# Thu, 30 Nov 2023 23:49:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 30 Nov 2023 23:50:08 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 30 Nov 2023 23:50:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 30 Nov 2023 23:50:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 30 Nov 2023 23:50:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 30 Nov 2023 23:50:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 30 Nov 2023 23:50:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 30 Nov 2023 23:50:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 30 Nov 2023 23:50:43 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 30 Nov 2023 23:50:45 GMT
ENV PHP_VERSION=8.3.0
# Thu, 30 Nov 2023 23:50:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Thu, 30 Nov 2023 23:50:50 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Thu, 30 Nov 2023 23:51:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 30 Nov 2023 23:51:04 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 30 Nov 2023 23:57:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 30 Nov 2023 23:57:50 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 30 Nov 2023 23:57:53 GMT
RUN docker-php-ext-enable sodium
# Thu, 30 Nov 2023 23:57:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 30 Nov 2023 23:57:58 GMT
WORKDIR /var/www/html
# Thu, 30 Nov 2023 23:58:07 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 30 Nov 2023 23:58:13 GMT
STOPSIGNAL SIGQUIT
# Thu, 30 Nov 2023 23:58:21 GMT
EXPOSE 9000
# Thu, 30 Nov 2023 23:58:23 GMT
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
	-	`sha256:c7d387f1f267ea360529df8d70b246f949e1afdb2317cdf84b028cda80a093d1`  
		Last Modified: Thu, 30 Nov 2023 23:20:17 GMT  
		Size: 3.4 MB (3391875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ceb4c7b64262166f66523ca8c83c91b6da0614cb21371e65abf05102263fff`  
		Last Modified: Fri, 01 Dec 2023 00:54:45 GMT  
		Size: 2.0 MB (1998656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc525a33d25691b980d49952089166e8be23cadce70b49e20fc15824ac97a3c`  
		Last Modified: Fri, 01 Dec 2023 00:54:44 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de94418ef0aa2483746b9ea3edbceb1016d94721c0b52d61813e29ce4803347`  
		Last Modified: Fri, 01 Dec 2023 00:54:44 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43106109fad105c39aa187e833877716cd8010eb197d422e83499d051b024c7c`  
		Last Modified: Fri, 01 Dec 2023 00:54:45 GMT  
		Size: 12.5 MB (12451810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b69f065da09649cdf04589189c66afb1825292a68746a6ebe019066cf5b8ed`  
		Last Modified: Fri, 01 Dec 2023 00:54:42 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb5ae1d2312bd68c006a289bb54467e010479ad041d77af9ffd738463d568c7`  
		Last Modified: Fri, 01 Dec 2023 00:55:14 GMT  
		Size: 13.4 MB (13430208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2249150a8c41302a91c0e11b289598e76b53235e57e795e52aff792c8cec6dc`  
		Last Modified: Fri, 01 Dec 2023 00:55:11 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11d292fa97e4ccd0fd6375355cdf4726c6016c9d3b1844a976bee3a634cb9d9`  
		Last Modified: Fri, 01 Dec 2023 00:55:11 GMT  
		Size: 18.8 KB (18778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cc1842ff660cd958ce1ab4a99a8f29efcd0e46774ef4f74e13fbe1c4ffbdb0`  
		Last Modified: Fri, 01 Dec 2023 00:55:11 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787adeb951091d65ea0b0971baa7ead62154aac5381006c01a64c9c33074bafa`  
		Last Modified: Tue, 05 Dec 2023 02:25:08 GMT  
		Size: 1.9 MB (1933343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766e406b56f97628af653db288e54de36f45e2db55e7ab9bb2c3e06342a899ae`  
		Last Modified: Tue, 05 Dec 2023 02:25:08 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1155f660b2f78eb2d04812092c5c6dd786e8631ba8761529af31859cf4d432a`  
		Last Modified: Mon, 11 Dec 2023 19:46:04 GMT  
		Size: 705.2 KB (705211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc834394b9ba2bd9873bb32324ff7cc876c9ca7986fe601bde88988f67c12d46`  
		Last Modified: Mon, 11 Dec 2023 19:46:03 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bad83ae1a6a1cc429cd9f91a4700dbf1b4c80b2ca7fe4edc06dcd46c9e1c0d6`  
		Last Modified: Mon, 11 Dec 2023 19:46:05 GMT  
		Size: 19.2 MB (19189219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-fpm-alpine3.17` - unknown; unknown

```console
$ docker pull drupal@sha256:7a29aa14bcccc95651e353d34996ef6a9629994e0314c1603b7951df39f2ef7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.2 KB (307182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:311539d0d5bb2c327dc1bafe51daa90fcc2a733386cb4d3c78e527577eb9ba62`

```dockerfile
```

-	Layers:
	-	`sha256:62a75bb4da96363cb5e7e0bbabd440bcd8651f126a3f7acb914719fce35a9bbf`  
		Last Modified: Mon, 11 Dec 2023 19:46:03 GMT  
		Size: 276.8 KB (276833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:134e4a60c03c06e44085fdeffa61ea3d048dd97a3febc304f79a9638cf28fe8e`  
		Last Modified: Mon, 11 Dec 2023 19:46:03 GMT  
		Size: 30.3 KB (30349 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-fpm-alpine3.17` - linux; s390x

```console
$ docker pull drupal@sha256:93a38d0128d90cc151e18a69bac8d7748a1bceddb2bb8159ce3983f1146365e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51453624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c3091a04fd529271e948df1f337287b8e37d9e6b362c7f7f2fe192a672d2ea`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:16 GMT
ADD file:bf416048d22b9a0deecb508385355d79b8d5d12b655c600dbdc0948f7dcbb2c2 in / 
# Thu, 30 Nov 2023 22:42:17 GMT
CMD ["/bin/sh"]
# Thu, 30 Nov 2023 22:54:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 30 Nov 2023 22:54:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 30 Nov 2023 22:54:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 30 Nov 2023 22:54:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 30 Nov 2023 22:54:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 30 Nov 2023 22:54:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 30 Nov 2023 22:54:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 30 Nov 2023 22:54:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 30 Nov 2023 22:54:49 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 30 Nov 2023 22:54:49 GMT
ENV PHP_VERSION=8.3.0
# Thu, 30 Nov 2023 22:54:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Thu, 30 Nov 2023 22:54:50 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Thu, 30 Nov 2023 22:54:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 30 Nov 2023 22:54:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 30 Nov 2023 23:02:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 30 Nov 2023 23:02:16 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 30 Nov 2023 23:02:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 30 Nov 2023 23:02:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 30 Nov 2023 23:02:17 GMT
WORKDIR /var/www/html
# Thu, 30 Nov 2023 23:02:18 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 30 Nov 2023 23:02:18 GMT
STOPSIGNAL SIGQUIT
# Thu, 30 Nov 2023 23:02:18 GMT
EXPOSE 9000
# Thu, 30 Nov 2023 23:02:18 GMT
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
	-	`sha256:7e9e7e53b618240d2e82e8cab6b677eab6786c4210dcc2b1a35bfd4cb492757e`  
		Last Modified: Thu, 30 Nov 2023 22:43:01 GMT  
		Size: 3.2 MB (3176332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a3268774e162b6964ffb61f07fe9761c7d943847826e9dbd6fb625468538ee`  
		Last Modified: Thu, 30 Nov 2023 23:48:25 GMT  
		Size: 2.0 MB (1966784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c778d6a13e3508dc643652a983ba137d6f1d69850fd2ef95d6d15514d8de79c6`  
		Last Modified: Thu, 30 Nov 2023 23:48:24 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824c797ef6ef25f9cce2db361f266d645e4f518370eb0716b1a021622882f198`  
		Last Modified: Thu, 30 Nov 2023 23:48:24 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591b6cbde5c421c1399830d85d1b99e4c72b32e454ec35e4f53df4c70ee13587`  
		Last Modified: Thu, 30 Nov 2023 23:48:23 GMT  
		Size: 12.5 MB (12451829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107f9fe31c778a4da98d0c2b9c7d02fffddee01f241eaa14bf3b0a5a4ac29550`  
		Last Modified: Thu, 30 Nov 2023 23:48:22 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71dd82838fb07b0a059f0464885bff68443b6339850797211b63e5239c8b2d5`  
		Last Modified: Thu, 30 Nov 2023 23:48:43 GMT  
		Size: 12.1 MB (12118167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094ff1fe7bf8f28965831efc5b09a0a23165258868434e1e6ef97fd4ac48c854`  
		Last Modified: Thu, 30 Nov 2023 23:48:41 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb28691e615e5a19b9307be167182f75f1b2cdd0e50a3240f297f483bb19989`  
		Last Modified: Thu, 30 Nov 2023 23:48:41 GMT  
		Size: 18.8 KB (18801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84debbead97dd432e4b14d5285b5347dd90d6e542b78ebc5a7c796188d12dd52`  
		Last Modified: Thu, 30 Nov 2023 23:48:41 GMT  
		Size: 9.2 KB (9175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8c970e67b3d2b03ce3b54a6aeb4258a1dbd10795d53d74fcdb290dc9a6456b`  
		Last Modified: Tue, 05 Dec 2023 02:27:09 GMT  
		Size: 1.8 MB (1813231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f081096b1b0bf1a57415833332d87226c1c0dff756e8880e494529ea6a4d1379`  
		Last Modified: Tue, 05 Dec 2023 02:27:08 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f8b5094a8cb359a4b78f04158250b4772aff12d91db1810855ec70342744f9`  
		Last Modified: Mon, 11 Dec 2023 20:14:29 GMT  
		Size: 705.2 KB (705211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc636f5c853a10853bcde42972a0e1ea2a631aeb43041514200cad16e98a0c24`  
		Last Modified: Mon, 11 Dec 2023 20:14:29 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1acc7330800b97d6e458b5755aa252465eb0561cad23f294ee81c04401b5f1a`  
		Last Modified: Mon, 11 Dec 2023 20:14:30 GMT  
		Size: 19.2 MB (19189194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-fpm-alpine3.17` - unknown; unknown

```console
$ docker pull drupal@sha256:1e8e6f5734cc4e19edc9fa987e5a3c46800c15c863607cedb498614e38a8eb92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 KB (307115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9892ee99dcddd83ca0945bf5000a2a40dff60734b83c6828c6a320139af33a3a`

```dockerfile
```

-	Layers:
	-	`sha256:c78bcef2b0f9e2fe92bd3fe0b33b6422de717b606696e5285a7093501bbcf0cb`  
		Last Modified: Mon, 11 Dec 2023 20:14:29 GMT  
		Size: 276.8 KB (276805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e65a538ff140018b3e0d6cfba3715e0acc35d8f0654877c082ba682a3a9d086`  
		Last Modified: Mon, 11 Dec 2023 20:14:29 GMT  
		Size: 30.3 KB (30310 bytes)  
		MIME: application/vnd.in-toto+json
