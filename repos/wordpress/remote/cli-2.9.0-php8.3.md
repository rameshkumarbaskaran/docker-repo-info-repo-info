## `wordpress:cli-2.9.0-php8.3`

```console
$ docker pull wordpress@sha256:e47e0e38232d02b29e47fae58f4eb3158b7d49216e2b121bbfa963a138b6849d
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

### `wordpress:cli-2.9.0-php8.3` - linux; amd64

```console
$ docker pull wordpress@sha256:3a008aafccc6a8d2d7ec2b069722cb43b3569b61cd833f9f2f13d74a9284746e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67813869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e537e553696333a6dd824e8e392fe186ecca2bdecd6d2aab16a12dfe16c54d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Fri, 24 Nov 2023 12:37:46 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["/bin/sh"]
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 24 Nov 2023 12:37:46 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 24 Nov 2023 12:37:46 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_VERSION=8.3.1
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.1.tar.xz.asc
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_SHA256=56445b1771b2ba5b7573453f9e8a9451e2d810b1741a352fa05259733b1e9758
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Nov 2023 12:37:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 24 Nov 2023 12:37:46 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 24 Nov 2023 12:37:46 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Nov 2023 12:37:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["php" "-a"]
# Fri, 24 Nov 2023 12:37:46 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
WORKDIR /var/www/html
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_VERSION=2.9.0
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_SHA512=39fa365300ab45840e30cc344595bbd175c3558a4499679edd9f9e3a00a846e94179c29c80de3242f1c405f3623605605748d188d9bb98450d9377388f60f113
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
VOLUME [/var/www/html]
# Fri, 24 Nov 2023 12:37:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Nov 2023 12:37:46 GMT
USER www-data
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc99979baa6760dc40a927f812328a1431e3870d0f166b035365166ef2cf8d4`  
		Last Modified: Tue, 12 Dec 2023 23:24:24 GMT  
		Size: 2.8 MB (2755737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47536423e0797b82f7a737a4efeb29297c96a33e8662ddcd121d728a01eac477`  
		Last Modified: Tue, 12 Dec 2023 23:24:23 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be6d4fc569fcdbdb835c5ee3607367e6ba4779809c0fad97de75045144220f8`  
		Last Modified: Tue, 12 Dec 2023 23:24:23 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d66ed8a08e88da3eb191d4a92354afb44aa32afeb70a35f017bb21e4d476a42`  
		Last Modified: Thu, 28 Dec 2023 01:16:37 GMT  
		Size: 12.5 MB (12465566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c89438a3af7fa920ae38a4db8d3af3a75255d7fc2f3218abc7441df47dece1c`  
		Last Modified: Thu, 28 Dec 2023 01:16:36 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032cda9d3dcea536b0398720b48c829672073360aa49163574c082896af3b3c3`  
		Last Modified: Thu, 28 Dec 2023 01:16:39 GMT  
		Size: 17.2 MB (17241947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64252f72f3b7f569d0824c7e6e85c77f6996a2a23c1e0ac2eac4bc0bc2a71c20`  
		Last Modified: Thu, 28 Dec 2023 01:16:36 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b1388b45b1ff44be24bc5c4450ecf6731f698fd0189d6560a285728a0312a2`  
		Last Modified: Thu, 28 Dec 2023 01:16:37 GMT  
		Size: 19.3 KB (19293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74af768238ce093045859c5aa0a560484b6b7db7556c39528eed8f95cb87360`  
		Last Modified: Thu, 28 Dec 2023 02:50:31 GMT  
		Size: 20.5 MB (20498114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef409f9bc56c11f309588a89823b41a8b7d9f47b460fd0afd1890af59f86ff36`  
		Last Modified: Thu, 28 Dec 2023 02:50:32 GMT  
		Size: 9.9 MB (9897695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38a54684db54e2743caedb6fc67a9ba37642667bc6e880d536facd8ab380fb5`  
		Last Modified: Thu, 28 Dec 2023 02:50:32 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccac17d0fa5d63818b07283ecef28329872208bca9c14d2bcd0b45e286b3ae2`  
		Last Modified: Thu, 28 Dec 2023 02:50:32 GMT  
		Size: 1.5 MB (1521707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ecfb9cca293ba100c1ed2efaaa86bd8aea7f39bf161e29d45b83d9c6a3dfd0`  
		Last Modified: Thu, 28 Dec 2023 02:50:32 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.9.0-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:6a609042e850df646c8310da0ed1d89aeea1f7e6fcd7547d82b9d31a23987603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1217753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e969865f12a664c0726cabc34d57fa99ce9d971ff4a3a5e802713d822b46ef`

```dockerfile
```

-	Layers:
	-	`sha256:b3055ff77da38d19be74a0daf8790bd0bb39c7ad5e18eb117c59b4fefc7160c5`  
		Last Modified: Thu, 28 Dec 2023 02:50:31 GMT  
		Size: 1.2 MB (1175524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c45532299af17f150e4bb3711e749550b5306824707b3cbd01aedcf1caee750`  
		Last Modified: Thu, 28 Dec 2023 02:50:31 GMT  
		Size: 42.2 KB (42229 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.9.0-php8.3` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:0856f1dd8cc33d2be0539b62f0ed342636fe5108f141c14dae34bd424654fbd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64287230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1cbce82fe3f18e42d09c5e7a5ee4112e03acdadd7854467cf186787699b37b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Fri, 24 Nov 2023 12:37:46 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["/bin/sh"]
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 24 Nov 2023 12:37:46 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 24 Nov 2023 12:37:46 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_VERSION=8.3.1
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.1.tar.xz.asc
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_SHA256=56445b1771b2ba5b7573453f9e8a9451e2d810b1741a352fa05259733b1e9758
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Nov 2023 12:37:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 24 Nov 2023 12:37:46 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 24 Nov 2023 12:37:46 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Nov 2023 12:37:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["php" "-a"]
# Fri, 24 Nov 2023 12:37:46 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
WORKDIR /var/www/html
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_VERSION=2.9.0
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_SHA512=39fa365300ab45840e30cc344595bbd175c3558a4499679edd9f9e3a00a846e94179c29c80de3242f1c405f3623605605748d188d9bb98450d9377388f60f113
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
VOLUME [/var/www/html]
# Fri, 24 Nov 2023 12:37:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Nov 2023 12:37:46 GMT
USER www-data
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6157a5053a6ba5646a1361153760014335e77813c8792b60d226dedefbb229`  
		Last Modified: Tue, 12 Dec 2023 22:10:24 GMT  
		Size: 2.8 MB (2761045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2682a06d9f91bef66466bcb1b37715dc344282ac9f062ffff8405cf448d71f51`  
		Last Modified: Tue, 12 Dec 2023 22:10:23 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982a61382f7fcec3d428935d516ac99bf603d105e72ebe0c2952b860f329675f`  
		Last Modified: Tue, 12 Dec 2023 22:10:22 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46410971fbf15a0ea5f80deb04d24771da7314fe274870ab21a4517a5821c620`  
		Last Modified: Thu, 28 Dec 2023 03:38:42 GMT  
		Size: 12.5 MB (12465580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d4614c4bf98630e83e1df402eafbaeb878c332a0646470c9d18b2d95dd3f1a`  
		Last Modified: Thu, 28 Dec 2023 03:38:40 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e5fa771d8a9ce53f76eca0cef0c841165647fd9c13bf2352041ddc4bbf414a`  
		Last Modified: Thu, 28 Dec 2023 03:38:46 GMT  
		Size: 15.7 MB (15746387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fc5ffdb56fc05b7ea8025cd10994a2d95f6e8c4db376880ebf101c85f99aaa`  
		Last Modified: Thu, 28 Dec 2023 03:38:40 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee56d8823937abe60ab7a83d709a61b26cd0fde9ebf5a70cfda1664769064b8`  
		Last Modified: Thu, 28 Dec 2023 03:38:40 GMT  
		Size: 19.1 KB (19130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4c66e7444eb419acff2e59973443cded94e43ef36438a65c714722e566dce9`  
		Last Modified: Sun, 31 Dec 2023 13:31:49 GMT  
		Size: 19.4 MB (19445819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdcc87f44e3ced725b3192962f4ae67ee7e8e4167b12a94bb61e4736b71d81e`  
		Last Modified: Sun, 31 Dec 2023 13:31:50 GMT  
		Size: 9.2 MB (9157076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d24c57493feddf1aa3b101ce7d821da6d16e097aeae7aa01c5d03cdcbde67`  
		Last Modified: Sun, 31 Dec 2023 13:31:50 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c840b6dd954fd383418a629cff22d4c23f7eb4855957c84a17c728a79327790e`  
		Last Modified: Sun, 31 Dec 2023 13:31:50 GMT  
		Size: 1.5 MB (1521717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cba31d0974966a1b083077991416c3b4a500754a9416d1c9998a3cb762eff40`  
		Last Modified: Sun, 31 Dec 2023 13:31:51 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.9.0-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:613d70afdc06ff224c7a63f34a659bfca4268cef17284a889f937b340040bfc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 KB (42137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dcb0e0f325ad4dad626af016256539c94c3bc637d5c1f9a442792272b3dd741`

```dockerfile
```

-	Layers:
	-	`sha256:50b5e7313968d0f5557b3c44861eddf184941e68658a2e18041e9f67246febb3`  
		Last Modified: Sun, 31 Dec 2023 13:31:49 GMT  
		Size: 42.1 KB (42137 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.9.0-php8.3` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:fad2fae489e15932e146f5e6cc6e2fcb900162fe3236e0cad1bb05d7b20d18a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62051993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a5e5e849371f8dd3d745e0e86f890a3e661e28cdc674f0c63b779a8958ebeb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Fri, 24 Nov 2023 12:37:46 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["/bin/sh"]
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 24 Nov 2023 12:37:46 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 24 Nov 2023 12:37:46 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_VERSION=8.3.1
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.1.tar.xz.asc
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_SHA256=56445b1771b2ba5b7573453f9e8a9451e2d810b1741a352fa05259733b1e9758
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Nov 2023 12:37:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 24 Nov 2023 12:37:46 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 24 Nov 2023 12:37:46 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Nov 2023 12:37:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["php" "-a"]
# Fri, 24 Nov 2023 12:37:46 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
WORKDIR /var/www/html
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_VERSION=2.9.0
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_SHA512=39fa365300ab45840e30cc344595bbd175c3558a4499679edd9f9e3a00a846e94179c29c80de3242f1c405f3623605605748d188d9bb98450d9377388f60f113
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
VOLUME [/var/www/html]
# Fri, 24 Nov 2023 12:37:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Nov 2023 12:37:46 GMT
USER www-data
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fcdc554dd7b708317247ba5731b0d76bc06dc68a48af57f662820d33c665cc`  
		Last Modified: Tue, 12 Dec 2023 22:36:17 GMT  
		Size: 2.6 MB (2608664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4717604343f2899832c4417228ef3cdb02080f72378a4152eb72083f09c96e`  
		Last Modified: Tue, 12 Dec 2023 22:36:15 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0a6a05c32e2329e654bc633b417da36b7c74ed6bf626231bf0e900f912838e`  
		Last Modified: Tue, 12 Dec 2023 22:36:15 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6c4940542fd7f43df35b09df2c3a727ef3d43d4337c0aa0a2630982291809d`  
		Last Modified: Thu, 28 Dec 2023 02:48:47 GMT  
		Size: 12.5 MB (12465579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac59c3fff92938ba8e4e28febee8c5b665e9ff07b3a78657662562238689e7b`  
		Last Modified: Thu, 28 Dec 2023 02:48:46 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07bbcbdd7ebbc2e32c5d2096a350d8e7b04cdf4efccdf10c8626f21a6dee1a7`  
		Last Modified: Thu, 28 Dec 2023 02:48:50 GMT  
		Size: 14.7 MB (14739754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de506d0d6df0d727f0a6ac28d2e4cf2da017984468190a33e0f77a4167a3dde0`  
		Last Modified: Thu, 28 Dec 2023 02:48:45 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c55989c46ca51bbd84eeca9bdecfaf4144f387d719c62e75c99ece28d1aa5e9`  
		Last Modified: Thu, 28 Dec 2023 02:48:45 GMT  
		Size: 19.1 KB (19108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0226d31c281861bc60c0893440c215f86ca3a203789389de7c9b22eff2e6a518`  
		Last Modified: Thu, 28 Dec 2023 10:40:46 GMT  
		Size: 18.9 MB (18939079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e8a1b77745702e9d5016e057950480a6c2f8543ccb708535461a9c159c0a13`  
		Last Modified: Thu, 28 Dec 2023 10:40:47 GMT  
		Size: 8.8 MB (8834080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53cb8a32c43466cb132f33758fecaf3d383034eef13dd84e578c6e9953bd53ef`  
		Last Modified: Thu, 28 Dec 2023 10:40:46 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a13e69904c90f27003f4caa6cb424bf01e6adefb4e353ab39a4a8fbad54140`  
		Last Modified: Thu, 28 Dec 2023 10:40:47 GMT  
		Size: 1.5 MB (1521699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065170318a50c2e2e682b8bbd6006af6d0f48152b0adb89c0201ff8d21d7c5a6`  
		Last Modified: Thu, 28 Dec 2023 10:40:47 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.9.0-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:0eebbfa58772c2a44a2d1b02fa85c7f0e6c9a221572fd574266e3830d6b9024f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1217912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254c23344f9bda2f796eeecce7177a823afafd0a3c7647e3a63718cbb59b126e`

```dockerfile
```

-	Layers:
	-	`sha256:06ef78c62fece37beffa13753ac8e8906341820b3260e7164c95bc50bb841d26`  
		Last Modified: Thu, 28 Dec 2023 10:40:45 GMT  
		Size: 1.2 MB (1175560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a53b06eedb8b55f360cc309dec433dfa3dd5fbd9eb46e7c5d4bb0e5e83a9f0c`  
		Last Modified: Thu, 28 Dec 2023 10:40:45 GMT  
		Size: 42.4 KB (42352 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.9.0-php8.3` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:7abfec4c7bd7372ec08463b99d1c9c61199b8c1471f44c4bee9542ba71aad1f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67643063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f54568246b9852ad7b287746b509b04ed902756d6efa01e870c2c192f8ae073`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Fri, 24 Nov 2023 12:37:46 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["/bin/sh"]
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 24 Nov 2023 12:37:46 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 24 Nov 2023 12:37:46 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_VERSION=8.3.1
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.1.tar.xz.asc
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_SHA256=56445b1771b2ba5b7573453f9e8a9451e2d810b1741a352fa05259733b1e9758
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Nov 2023 12:37:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 24 Nov 2023 12:37:46 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 24 Nov 2023 12:37:46 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Nov 2023 12:37:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["php" "-a"]
# Fri, 24 Nov 2023 12:37:46 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
WORKDIR /var/www/html
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_VERSION=2.9.0
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_SHA512=39fa365300ab45840e30cc344595bbd175c3558a4499679edd9f9e3a00a846e94179c29c80de3242f1c405f3623605605748d188d9bb98450d9377388f60f113
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
VOLUME [/var/www/html]
# Fri, 24 Nov 2023 12:37:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Nov 2023 12:37:46 GMT
USER www-data
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a19b0853c69aaf4e0a33f42601f1bddea728304bef39e2fc08f66f3d518576`  
		Last Modified: Tue, 12 Dec 2023 23:00:29 GMT  
		Size: 2.8 MB (2810204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872ba87116831a71587816ab8564d1a2b7137e1163524eb7e5abf40966e6882c`  
		Last Modified: Tue, 12 Dec 2023 23:00:28 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a9508fcdd73dc8c678f841adc3269e9919da38f14917ddaa2162b636d4661c`  
		Last Modified: Tue, 12 Dec 2023 23:00:28 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def0554f9c72eaae677cdb5ee1323dac94b472cbca4b0601ea86130b1c163546`  
		Last Modified: Thu, 28 Dec 2023 00:32:52 GMT  
		Size: 12.5 MB (12465572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9019e34eb849acaf850d10f4075f93eeb506c919f80f4e5c39c2b2a15cae4773`  
		Last Modified: Thu, 28 Dec 2023 00:32:51 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed22edfdb10a36cd9b58e853dc177e6e9e106ad104ee5c6f3d3bbdc5c8dcd5b`  
		Last Modified: Thu, 28 Dec 2023 00:32:53 GMT  
		Size: 17.2 MB (17212001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa64ecb8fa41b54ab49204e2f9ef993e7bfb9fb9bd93838140b5f9ebe89f8d4d`  
		Last Modified: Thu, 28 Dec 2023 00:32:51 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0cfdabc37df1900b7881f01fed7201c95360c004bf90ebbad00ca372c2cbf57`  
		Last Modified: Thu, 28 Dec 2023 00:32:51 GMT  
		Size: 19.1 KB (19081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8224f4f82dc59c4b24127bb8363f1e807db5f55b5375623692b6287b7f03b70`  
		Last Modified: Thu, 28 Dec 2023 07:18:45 GMT  
		Size: 20.8 MB (20792336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c5f682193aa504ad71ab791c8c24f1ca0d74e8291283b2cf0f8e93cf9b1ad0`  
		Last Modified: Thu, 28 Dec 2023 07:18:46 GMT  
		Size: 9.5 MB (9469104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89eeb66f4bd25dd40aa76d6395f14f21e03a04908401afe40ce5f686b65cc361`  
		Last Modified: Thu, 28 Dec 2023 07:18:45 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6820071ea74498a9112005f6d59a47e2b533d4773ffa3ccd15bae71ec1605f6`  
		Last Modified: Thu, 28 Dec 2023 07:18:46 GMT  
		Size: 1.5 MB (1521636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0c157c8eeaa3caa0eae9401a3baf7765d19d783a0f214d9130e6dbbc78efe0`  
		Last Modified: Thu, 28 Dec 2023 07:18:47 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.9.0-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:f39ae8d9a1b48c1eebf8e5f774b8c79a242f176a494c893c31fc9d11cf3bc4e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1217775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f2cf52193f24dbff2b7ff3b7bd482f77ae3c65d3bb5d7e2166bddc6b4ec208c`

```dockerfile
```

-	Layers:
	-	`sha256:4250e050e269454eed123afd911d62f37daf7fb7811e9ff65f44353fd900b267`  
		Last Modified: Thu, 28 Dec 2023 07:18:45 GMT  
		Size: 1.2 MB (1175535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5c726a4075a98a7d388f8efcd41a112f8c86ef384ba1de4d2159c5a8a5f4704`  
		Last Modified: Thu, 28 Dec 2023 07:18:45 GMT  
		Size: 42.2 KB (42240 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.9.0-php8.3` - linux; 386

```console
$ docker pull wordpress@sha256:31ab4e1b70e67024dfbfe03111cf249731ef93307e2726491b832c54b15a609a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67925588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0245def0c7f147988efcffdb0677329373f2eea6fc930681dec64ce945d5ff3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Fri, 24 Nov 2023 12:37:46 GMT
ADD file:bd52540f209ba362654d795d7893669c819d35011a16f9f319301727a33b3bd9 in / 
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["/bin/sh"]
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 24 Nov 2023 12:37:46 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 24 Nov 2023 12:37:46 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_VERSION=8.3.1
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.1.tar.xz.asc
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_SHA256=56445b1771b2ba5b7573453f9e8a9451e2d810b1741a352fa05259733b1e9758
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Nov 2023 12:37:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 24 Nov 2023 12:37:46 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 24 Nov 2023 12:37:46 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Nov 2023 12:37:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["php" "-a"]
# Fri, 24 Nov 2023 12:37:46 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
WORKDIR /var/www/html
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_VERSION=2.9.0
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_SHA512=39fa365300ab45840e30cc344595bbd175c3558a4499679edd9f9e3a00a846e94179c29c80de3242f1c405f3623605605748d188d9bb98450d9377388f60f113
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
VOLUME [/var/www/html]
# Fri, 24 Nov 2023 12:37:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Nov 2023 12:37:46 GMT
USER www-data
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:9acd8b4c9d4385585f74dabb4bc6b3351888710ae37ec5dbd9ea950281b8f9bb`  
		Last Modified: Fri, 08 Dec 2023 01:38:43 GMT  
		Size: 3.2 MB (3244115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35c853c51aa63c9f21d6c91fa6948b8160ed6a90764a48e7b1891c38e016590`  
		Last Modified: Wed, 13 Dec 2023 00:34:22 GMT  
		Size: 2.8 MB (2820917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6af7fb9ea0ea850c653027fa7b1b18f1d4c405aade35df3c3ec2151bb8251f`  
		Last Modified: Wed, 13 Dec 2023 00:34:21 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9233674231d3f63e2099e1d4253bf67fd488ef3d4fcd72e3e741ffb7a41f385e`  
		Last Modified: Wed, 13 Dec 2023 00:34:20 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062d991a79d8baf3832da0dada4118aca16d685f39c582dd9f1c13be8872adf6`  
		Last Modified: Thu, 28 Dec 2023 02:16:22 GMT  
		Size: 12.5 MB (12465568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdccc64f3f0e267c36f0f474677b772b5b671944d0c7ce46b2eb39bc91b7141`  
		Last Modified: Thu, 28 Dec 2023 02:16:21 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412e46b7649c21f5bacb422ca6f89b57da6cf094daa587baa90055faa7475e38`  
		Last Modified: Thu, 28 Dec 2023 02:16:26 GMT  
		Size: 17.7 MB (17672674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78aa1ae3aca128a3a0b42bc849dd0cae59fb65c4a90ec2ed2d32b1d67f7f49b`  
		Last Modified: Thu, 28 Dec 2023 02:16:21 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f1d7dcb92a3d10f884e655d750cd26c36d5f0ea48f3fb83e371d8d1a96c363`  
		Last Modified: Thu, 28 Dec 2023 02:16:21 GMT  
		Size: 19.3 KB (19293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11154f9e7e976182e526cce8e7a92cc29b6309a32fb000975281cd33c586ac44`  
		Last Modified: Thu, 28 Dec 2023 06:51:33 GMT  
		Size: 20.2 MB (20159438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5428253567ffaf82816d850772b80d31d0690cd0504cb41c06f8642b35aabc9`  
		Last Modified: Thu, 28 Dec 2023 06:51:34 GMT  
		Size: 10.0 MB (10016565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e13b696623f080ab63892397a3db8196e3a2e1a58fdc882e5e8f07578f587c`  
		Last Modified: Thu, 28 Dec 2023 06:51:33 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7d4245d0a584ae8b1c89b6d7ef250cad1f1f7b3fffbc10a39ca5c11fc21bab`  
		Last Modified: Thu, 28 Dec 2023 06:51:35 GMT  
		Size: 1.5 MB (1521681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7afffdd9927b918cfac5e59acb2d0948f74a4ad21b6221cff1e7e65c08fee65`  
		Last Modified: Thu, 28 Dec 2023 06:51:34 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.9.0-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:6323cff878e469022c8c68ea41f3684acaafe5ce0323762f282937bb9be7b6c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1217695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7c308aedc1616fb64dfb6ca23cbec51b59b8c1dd06c2ac27b020b031a9cd34`

```dockerfile
```

-	Layers:
	-	`sha256:0b01aa817ac7519f48d2f49320f74f0902514dac01583784d4d1ae44c72e29bb`  
		Last Modified: Thu, 28 Dec 2023 06:51:32 GMT  
		Size: 1.2 MB (1175499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b0710c8472f740a763eebadd0191c268f089469eefde92427b65417ace0b03b`  
		Last Modified: Thu, 28 Dec 2023 06:51:32 GMT  
		Size: 42.2 KB (42196 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.9.0-php8.3` - linux; ppc64le

```console
$ docker pull wordpress@sha256:d89620e54798b0596c06423d241b8b22ddecfc91e4b454b79daaa6aed379ed7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69632480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa947e085e04a0557b71a10e9ce1e7e3116cb4d420b528f8adca3d25338a64a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Fri, 24 Nov 2023 12:37:46 GMT
ADD file:052421189f8d269382daaaa8beb63c687e4d8ca908c421abdce53bcc627a40b4 in / 
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["/bin/sh"]
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 24 Nov 2023 12:37:46 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 24 Nov 2023 12:37:46 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_VERSION=8.3.1
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.1.tar.xz.asc
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_SHA256=56445b1771b2ba5b7573453f9e8a9451e2d810b1741a352fa05259733b1e9758
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Nov 2023 12:37:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 24 Nov 2023 12:37:46 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 24 Nov 2023 12:37:46 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Nov 2023 12:37:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["php" "-a"]
# Fri, 24 Nov 2023 12:37:46 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
WORKDIR /var/www/html
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_VERSION=2.9.0
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_SHA512=39fa365300ab45840e30cc344595bbd175c3558a4499679edd9f9e3a00a846e94179c29c80de3242f1c405f3623605605748d188d9bb98450d9377388f60f113
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
VOLUME [/var/www/html]
# Fri, 24 Nov 2023 12:37:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Nov 2023 12:37:46 GMT
USER www-data
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:243ac51c334a47917a84be93e972ee6378987e9b3b917a5a8df29025e161c1f3`  
		Last Modified: Fri, 08 Dec 2023 01:23:14 GMT  
		Size: 3.4 MB (3358233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89935d2f947cbd3585545f82639d347027ef82fbbf413f8684101953ea74bd6`  
		Last Modified: Tue, 12 Dec 2023 22:41:51 GMT  
		Size: 2.8 MB (2838539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b208bea042d5cdcbe6436f88d2f7ea51b03a91df91ae099118f57b644b87bdb2`  
		Last Modified: Tue, 12 Dec 2023 22:41:50 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcb83a14858379fd485cb474c02417cd209b148b775365e9bae3ab90f5fe798`  
		Last Modified: Tue, 12 Dec 2023 22:41:50 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768bf5c3f1f20a2b5b1c1b941f51711a1f3fcd823d7c2b21749012338b7c5225`  
		Last Modified: Thu, 28 Dec 2023 01:00:00 GMT  
		Size: 12.5 MB (12465577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a921af2fb25a52cdd55f7f7ac0c8f0e9495847a7fb171a10f5df7168eb77bf`  
		Last Modified: Thu, 28 Dec 2023 00:59:59 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749b20d5212c5d7e7da7bf0b7246297f631bda917e8555a944438b7dd9a20cef`  
		Last Modified: Thu, 28 Dec 2023 01:00:03 GMT  
		Size: 18.1 MB (18116296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1aaa6291246b504beab5348aab711e81a792cbcf5f51b8316532575aee4dd0`  
		Last Modified: Thu, 28 Dec 2023 00:59:59 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa4e6bd635428b380aa075f2870700b2cec013307a245459a93e09813fb748a`  
		Last Modified: Thu, 28 Dec 2023 00:59:59 GMT  
		Size: 19.1 KB (19102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3487588deef3db39b2b1c127b87db103cd6358eddf83c2920d5ab66c44c439`  
		Last Modified: Thu, 28 Dec 2023 07:08:39 GMT  
		Size: 21.3 MB (21340773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de25a0ab7070628e958c45eb75f6b405d224a56e2fd04d1e0a93970eca03f0ef`  
		Last Modified: Thu, 28 Dec 2023 07:08:40 GMT  
		Size: 10.0 MB (9966926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991a8c59a2523b613026e3cafebc386332f874548033ae9cd315a54af0bce2ad`  
		Last Modified: Thu, 28 Dec 2023 07:08:39 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e417b816ac742108366880312cb5c8b60317aa42007c0eb19d997b4286e948`  
		Last Modified: Thu, 28 Dec 2023 07:08:40 GMT  
		Size: 1.5 MB (1521693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf35f4d25e6531667a637ec97314a5c0d556c00b814edc165422340d03ff1c46`  
		Last Modified: Thu, 28 Dec 2023 07:08:40 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.9.0-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:7b72cd56857a97e608b3f447a48b42fe7b943c4310cc8c10ff0da875e4a47f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1216198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b22bd684152c0f3c6e6ee5fc6118c93fb141bbb85e742853154a02aac8e795`

```dockerfile
```

-	Layers:
	-	`sha256:895ccada3a1a4a1597d08b90fe3f4388912cd432e15dd64cbe67f0c840a049a5`  
		Last Modified: Thu, 28 Dec 2023 07:08:38 GMT  
		Size: 1.2 MB (1173922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e80a466823965f5eadd736379ac6d80ecfa488ef4d4ec3004c8d689cbe94fa82`  
		Last Modified: Thu, 28 Dec 2023 07:08:38 GMT  
		Size: 42.3 KB (42276 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.9.0-php8.3` - linux; s390x

```console
$ docker pull wordpress@sha256:07123fb5400d6359c62af9f6f1a8cd621642d0b2849ccb6f554cdabff579b318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69524856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6230754cb5afbee1970325acdc7e9abbec63a916265debec4fd08f7053fd917d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Fri, 24 Nov 2023 12:37:46 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["/bin/sh"]
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 24 Nov 2023 12:37:46 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 24 Nov 2023 12:37:46 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_VERSION=8.3.1
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.1.tar.xz.asc
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_SHA256=56445b1771b2ba5b7573453f9e8a9451e2d810b1741a352fa05259733b1e9758
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Nov 2023 12:37:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 24 Nov 2023 12:37:46 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 24 Nov 2023 12:37:46 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Nov 2023 12:37:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["php" "-a"]
# Fri, 24 Nov 2023 12:37:46 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
WORKDIR /var/www/html
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_VERSION=2.9.0
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_SHA512=39fa365300ab45840e30cc344595bbd175c3558a4499679edd9f9e3a00a846e94179c29c80de3242f1c405f3623605605748d188d9bb98450d9377388f60f113
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
VOLUME [/var/www/html]
# Fri, 24 Nov 2023 12:37:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Nov 2023 12:37:46 GMT
USER www-data
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0180a7268e169fa6dd82fc04f9270dbd4fe716cf09b03fc82f84618025bad4`  
		Last Modified: Tue, 12 Dec 2023 22:07:16 GMT  
		Size: 2.9 MB (2937974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ecaefbf268f4b1e4d9f16c5d67523f3b76e72db0c3fc7a2f3fb6fd7fbdec547`  
		Last Modified: Tue, 12 Dec 2023 22:07:16 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f0d18e8f1067fcb105dea2ad180f140d138c6d99310025696d1aaa322017db`  
		Last Modified: Tue, 12 Dec 2023 22:07:16 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41026c09e77359ebd31b20412114dff6fce9d0b63711a64d0a7c33cfc438da72`  
		Last Modified: Wed, 27 Dec 2023 23:41:28 GMT  
		Size: 12.5 MB (12465585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d07321e9ae1a4a26a032a3b77240cff9122b408cd1d8a225b3adb29b5429248`  
		Last Modified: Wed, 27 Dec 2023 23:41:27 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021c834fe6a97e0814d9fb14ceaf9c9c088b0f12c9f1c4ab3ab4da0337702122`  
		Last Modified: Wed, 27 Dec 2023 23:41:30 GMT  
		Size: 17.0 MB (16995119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6561f9a0748bdb2571be6596801eeabd2b4f80e2c61ba32dbccaaa4d56f19387`  
		Last Modified: Wed, 27 Dec 2023 23:41:27 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332ae46e1cabf7c53bb32e0cd5fdbd878157b415b29c97f1f88a36cb3fe9f71a`  
		Last Modified: Wed, 27 Dec 2023 23:41:27 GMT  
		Size: 19.1 KB (19105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edf4639bee830137833bbe5161b4b8fb812fa927f67ab843b62941dc447b6cc`  
		Last Modified: Thu, 28 Dec 2023 03:59:46 GMT  
		Size: 22.4 MB (22407099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de9611995e8857b8441b77a63284eec5bcaf64e5e2e5ae492a9e9299086e423`  
		Last Modified: Thu, 28 Dec 2023 03:59:47 GMT  
		Size: 9.9 MB (9930595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17e86a825d5cd016dff5410cbd08b25cca4f9b1c08fafd1aa8e7fef17e0b131`  
		Last Modified: Thu, 28 Dec 2023 03:59:46 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d59fd4f9fae147e74f90381591790c82a61d79207df43ef0530e431bfc13c63`  
		Last Modified: Thu, 28 Dec 2023 03:59:47 GMT  
		Size: 1.5 MB (1521709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d129acf5e2e8b83aea8b30601b040234754ae6d63af82b101ce635eeeee97cb`  
		Last Modified: Thu, 28 Dec 2023 03:59:47 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.9.0-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:0a60d745bacde3405ce529a5e1e817ba60052b323af897157d753c538b6b7570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1216118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a7640fc516ef5254b049c446f857072a55f516ebff7081564d9cf74076a077b`

```dockerfile
```

-	Layers:
	-	`sha256:48dbc253d644c045a2ee5c7238eb50f42162b358fa3b6248af2b91c822bea07a`  
		Last Modified: Thu, 28 Dec 2023 03:59:46 GMT  
		Size: 1.2 MB (1173888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c87e2135b7262a6dbd15b3b4249028bb56179aecc186e6d7c4808e16ef3d82f`  
		Last Modified: Thu, 28 Dec 2023 03:59:46 GMT  
		Size: 42.2 KB (42230 bytes)  
		MIME: application/vnd.in-toto+json
