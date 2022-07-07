## `wordpress:beta-6.0.1-php8.1-fpm-alpine`

```console
$ docker pull wordpress@sha256:0a38927f99a2d0d3dfb06bdb2d8733205b3b7dd3b3135eda8defd2459d2155e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm variant v6

### `wordpress:beta-6.0.1-php8.1-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:b42eefdd0674f139c9536c191e0674a508dd0092632b73663c54c37b8bbd4af7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97298982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a298747f4015b4ce36e1f26ce9e286542f40314b24e8ec5e92f84bbccef84a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 23 May 2022 19:49:32 GMT
ADD file:f7cee617575b5e5a7672d298a519bb8d8b5098efb90aa2a5d7b0510003457d52 in / 
# Mon, 23 May 2022 19:49:33 GMT
CMD ["/bin/sh"]
# Wed, 25 May 2022 21:50:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 25 May 2022 21:50:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 25 May 2022 21:50:08 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 25 May 2022 21:50:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 May 2022 21:50:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 25 May 2022 21:50:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 May 2022 21:50:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 May 2022 21:50:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 May 2022 21:50:12 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 07 Jul 2022 21:24:18 GMT
ENV PHP_VERSION=8.1.8
# Thu, 07 Jul 2022 21:24:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.8.tar.xz.asc
# Thu, 07 Jul 2022 21:24:19 GMT
ENV PHP_SHA256=04c065515bc347bc68e0bb1ac7182669a98a731e4a17727e5731650ad3d8de4c
# Thu, 07 Jul 2022 21:24:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 07 Jul 2022 21:24:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 07 Jul 2022 21:35:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 07 Jul 2022 21:35:32 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 07 Jul 2022 21:35:34 GMT
RUN docker-php-ext-enable sodium
# Thu, 07 Jul 2022 21:35:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 Jul 2022 21:35:35 GMT
WORKDIR /var/www/html
# Thu, 07 Jul 2022 21:35:37 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 07 Jul 2022 21:35:37 GMT
STOPSIGNAL SIGQUIT
# Thu, 07 Jul 2022 21:35:38 GMT
EXPOSE 9000
# Thu, 07 Jul 2022 21:35:38 GMT
CMD ["php-fpm"]
# Thu, 07 Jul 2022 22:57:52 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	;
# Thu, 07 Jul 2022 23:00:18 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Thu, 07 Jul 2022 23:00:21 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 07 Jul 2022 23:00:23 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 07 Jul 2022 23:08:33 GMT
RUN set -eux; 	version='6.0.1-RC1'; 	sha1='37b555bc69bb4b15d079a0b597059fce5a16efd4'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 777 wp-content
# Thu, 07 Jul 2022 23:08:35 GMT
VOLUME [/var/www/html]
# Thu, 07 Jul 2022 23:08:35 GMT
COPY --chown=www-data:www-datafile:f95ddeaad9b50ddddf288560052a9de4f33fa6297ea70870e396f6d99c482b7a in /usr/src/wordpress/ 
# Thu, 07 Jul 2022 23:08:36 GMT
COPY file:5be6bcc31206cb827f037769d89fd092037ed61a1e10d6cae7939a37055beb4c in /usr/local/bin/ 
# Thu, 07 Jul 2022 23:08:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Jul 2022 23:08:37 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:79a25ccaf940855872635c06e7614d9b27dd38ffb5a8adfdb9274dfdc0ea0d87`  
		Last Modified: Mon, 23 May 2022 19:08:47 GMT  
		Size: 2.6 MB (2606142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e7eae6d0293087d982d321125f6f132894675f6acb732427528058758d6ae3`  
		Last Modified: Wed, 25 May 2022 22:46:23 GMT  
		Size: 1.7 MB (1693282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad96c7e3fdd13c53c906a10fab89b0dc599bf1746acd163f9648f8f9ec949de`  
		Last Modified: Wed, 25 May 2022 22:46:21 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1acccbd45290b92307c479937198ace1c187e0fd49d5e1ea72c1f5d7d5e1705`  
		Last Modified: Wed, 25 May 2022 22:46:21 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa00277edf5af3bcea93a4e3e4aacf25d2b1f5c8c59a3493210c18e151ae238`  
		Last Modified: Thu, 07 Jul 2022 22:45:35 GMT  
		Size: 11.7 MB (11742258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f810c126b632d8fed8b53948cabb27aaa89fcdb205656dd28d53119f2ab4c55`  
		Last Modified: Thu, 07 Jul 2022 22:45:32 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f944ac94cedabc74dfef3835d0ded54570b50b1b2cff60cc46c01c031050983a`  
		Last Modified: Thu, 07 Jul 2022 22:46:57 GMT  
		Size: 12.8 MB (12835332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688488581fceb7a77e3a5b91ecee5eb523e69b82642251048a37e67ba397b01f`  
		Last Modified: Thu, 07 Jul 2022 22:46:52 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d429d69e5fdea51028b3ade6bd9d003b0ebd5e2e903c4bc403de13048c8ca1`  
		Last Modified: Thu, 07 Jul 2022 22:46:51 GMT  
		Size: 18.4 KB (18448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf602d736125daddc5df68c8070619ae7975f939f22283790b578bd02548099`  
		Last Modified: Thu, 07 Jul 2022 22:46:52 GMT  
		Size: 8.6 KB (8619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa00c9f204b41f2d08b4b409bb91a95403bc78241de8f6e1219943ba2cc88a8a`  
		Last Modified: Thu, 07 Jul 2022 23:14:04 GMT  
		Size: 43.3 MB (43268661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78f83e6a8f284bc84cac0bb945a978d0eb64aa7aa26471cc3dc53d524c61d26`  
		Last Modified: Thu, 07 Jul 2022 23:13:39 GMT  
		Size: 4.1 MB (4057457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b608b37e14590998b91b961cf5a738e6fbd7c3437b60488c85a2fc57e6383a`  
		Last Modified: Thu, 07 Jul 2022 23:13:34 GMT  
		Size: 65.6 KB (65569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892792e7636639fd54e1207d05ece9d1df6ad6185036b601f28fc0db00bda21a`  
		Last Modified: Thu, 07 Jul 2022 23:13:35 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d285e901dae033da444fa91c7586d586f8e6de7e90bc0905c9e3796091144f1`  
		Last Modified: Thu, 07 Jul 2022 23:17:29 GMT  
		Size: 21.0 MB (20994284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e6069d6db3dd0d85ede797202af5a79974bee799c1d695b3bf72df9193efac`  
		Last Modified: Thu, 07 Jul 2022 23:17:13 GMT  
		Size: 2.3 KB (2341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d7fa3dc1988e5d1381d05b7b70e3d3612b86854e335bb5551ddb79ede61e6e`  
		Last Modified: Thu, 07 Jul 2022 23:17:13 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
