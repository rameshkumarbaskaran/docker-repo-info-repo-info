## `drupal:7-fpm-alpine3.16`

```console
$ docker pull drupal@sha256:12685b592f7cbe62640c28eb98789ecbc8a9013c334c6b11bd95a914de988417
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

### `drupal:7-fpm-alpine3.16` - linux; amd64

```console
$ docker pull drupal@sha256:7dadb407b3db3dda4e238d6745059b961f22c6163e1f6b7db0ebb1b600503d38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34780147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6eedc1e4f2fbba85590731f324ba0da6a10b70956d3963ba1b58344274db13`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 07 Jun 2023 21:27:14 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Wed, 07 Jun 2023 21:27:14 GMT
CMD ["/bin/sh"]
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 07 Jun 2023 21:27:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 07 Jun 2023 21:27:14 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4 39B641343D8C104B2B146DC3F9C39DC0B9698544
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_VERSION=8.0.30
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.30.tar.xz.asc
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_SHA256=216ab305737a5d392107112d618a755dc5df42058226f1670e9db90e77d777d9
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 07 Jun 2023 21:27:14 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 07 Jun 2023 21:27:14 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 07 Jun 2023 21:27:14 GMT
RUN docker-php-ext-enable sodium
# Wed, 07 Jun 2023 21:27:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 07 Jun 2023 21:27:14 GMT
WORKDIR /var/www/html
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 07 Jun 2023 21:27:14 GMT
STOPSIGNAL SIGQUIT
# Wed, 07 Jun 2023 21:27:14 GMT
EXPOSE 9000
# Wed, 07 Jun 2023 21:27:14 GMT
CMD ["php-fpm"]
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 07 Jun 2023 21:27:14 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 07 Jun 2023 21:27:14 GMT
ENV DRUPAL_VERSION=7.98
# Wed, 07 Jun 2023 21:27:14 GMT
ENV DRUPAL_MD5=4139f0feecb44a53645242194809b73a
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5f9cde2c4dbdd3cc68566e25cc28c6c9e1188f0ced3f008877e603e234a79c`  
		Last Modified: Sat, 21 Oct 2023 06:34:02 GMT  
		Size: 3.3 MB (3257780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e748c1d059cf44a74f2135b9228b9e6408d56d95ee0f05ef1789d055637b6e0`  
		Last Modified: Sat, 21 Oct 2023 06:34:02 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a56f4c3c93a87a0c513d0d945d54cfc7a2761b204bef6c604d944c68e440567`  
		Last Modified: Sat, 21 Oct 2023 06:34:02 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be2c5ed3c4ab64c0c8586c9557c7fe1eeea9d9e470be69dcc220393e39ecfb7`  
		Last Modified: Sat, 21 Oct 2023 06:37:16 GMT  
		Size: 10.8 MB (10841083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142f0e40e9f47387d9aa822a9119bc21513c8fea0878993592073d0c89aeaf3b`  
		Last Modified: Sat, 21 Oct 2023 06:37:15 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a19c75621103be144be34499407f0e25071d63deb5b7c7ee90d10bdd7c9e895`  
		Last Modified: Sat, 21 Oct 2023 06:37:45 GMT  
		Size: 12.1 MB (12085333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4dc4942210169666837de6ecf48ee09b1daef4482613bac5c31e57f9a76546a`  
		Last Modified: Sat, 21 Oct 2023 06:37:43 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40affa1013c9759e226e74284003b2d604089fcd1a091da39d940ba8c98d211b`  
		Last Modified: Sat, 21 Oct 2023 06:37:43 GMT  
		Size: 18.7 KB (18684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c383bc84a52661f485d5b54236bc7a03d28a7b8916c80cda00bd73c95a8e913c`  
		Last Modified: Sat, 21 Oct 2023 06:37:43 GMT  
		Size: 8.7 KB (8713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7ed91f88f41e1b2cbf46f151dbda6e49ce2300fe1a495038312b17d3b15b8e`  
		Last Modified: Wed, 08 Nov 2023 20:27:44 GMT  
		Size: 2.3 MB (2345791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacf4f796aae9f3cf05f186de3fbb0a7f86085ea25026f642cdadebb31d6df41`  
		Last Modified: Wed, 08 Nov 2023 20:27:44 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79206b502d906832befc83ff69f7964251255dc2f02533617739ba4027de49da`  
		Last Modified: Wed, 08 Nov 2023 20:27:44 GMT  
		Size: 3.4 MB (3410296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-fpm-alpine3.16` - unknown; unknown

```console
$ docker pull drupal@sha256:f20758754f23d46366e6f5cd5a6a2e1816b6c9cf40d58fcff0943100443c4310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.1 KB (251113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7382bef27ebf2603bee9b6cf96374710cc08c5c1e2aab2304d80bff56a6c341`

```dockerfile
```

-	Layers:
	-	`sha256:929519fb964bfc132110d40bae03f39dfbcebcd524f603eaff0af2f9da892d16`  
		Last Modified: Wed, 08 Nov 2023 20:27:44 GMT  
		Size: 227.5 KB (227500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:863369c6dbae011c881e5cb57171cd735a2ef08bb9f835cd0b0c665f4fcc9bde`  
		Last Modified: Wed, 08 Nov 2023 20:27:44 GMT  
		Size: 23.6 KB (23613 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-fpm-alpine3.16` - linux; arm variant v6

```console
$ docker pull drupal@sha256:200f2b4f90c01cf9769ba9781d14304c6a0df68e75f386dd41a68a42a390afdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32727497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c612a6e94fd709b53375788f9f098770f4385250cfddc45afacf4efca6844883`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 07 Jun 2023 21:27:14 GMT
ADD file:321b24cc0fbd39caa2d7672a740d2cd2030ba99cab16f50c22db9955bd99350b in / 
# Wed, 07 Jun 2023 21:27:14 GMT
CMD ["/bin/sh"]
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 07 Jun 2023 21:27:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 07 Jun 2023 21:27:14 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4 39B641343D8C104B2B146DC3F9C39DC0B9698544
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_VERSION=8.0.30
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.30.tar.xz.asc
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_SHA256=216ab305737a5d392107112d618a755dc5df42058226f1670e9db90e77d777d9
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 07 Jun 2023 21:27:14 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 07 Jun 2023 21:27:14 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 07 Jun 2023 21:27:14 GMT
RUN docker-php-ext-enable sodium
# Wed, 07 Jun 2023 21:27:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 07 Jun 2023 21:27:14 GMT
WORKDIR /var/www/html
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 07 Jun 2023 21:27:14 GMT
STOPSIGNAL SIGQUIT
# Wed, 07 Jun 2023 21:27:14 GMT
EXPOSE 9000
# Wed, 07 Jun 2023 21:27:14 GMT
CMD ["php-fpm"]
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 07 Jun 2023 21:27:14 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 07 Jun 2023 21:27:14 GMT
ENV DRUPAL_VERSION=7.98
# Wed, 07 Jun 2023 21:27:14 GMT
ENV DRUPAL_MD5=4139f0feecb44a53645242194809b73a
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:dffa980f71c953938bb194a457aa62e7f1885137331eef8bf7f9403c075f711c`  
		Last Modified: Mon, 07 Aug 2023 19:50:02 GMT  
		Size: 2.6 MB (2615553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29c357d6784fdb079f1921858d3d0e364fa8658f83ba71728ec5fe9361cbc98`  
		Last Modified: Sat, 21 Oct 2023 03:28:43 GMT  
		Size: 3.0 MB (3004864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1dd5690b538865e1204da4d15c2d269732722a759c999e0eb71d997e0588d16`  
		Last Modified: Sat, 21 Oct 2023 03:28:42 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a60d00ef2f1db4050a540341e488d1a09d8d3590b688b273e25c4bb5e3ed67`  
		Last Modified: Sat, 21 Oct 2023 03:28:43 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088133a000518f8e0199e4328ea21068cbf75146981e2af5fd1bbd49b2c457ed`  
		Last Modified: Sat, 21 Oct 2023 03:31:44 GMT  
		Size: 10.8 MB (10841091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336a25a5af7846f8ab7f89f98d873a5e9afe066e322e804a15d1a72af4098899`  
		Last Modified: Sat, 21 Oct 2023 03:31:43 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9be9828e79c71b174ab290d0e29f0d93288b299137766827a2327f24fc9adae`  
		Last Modified: Sat, 21 Oct 2023 03:32:12 GMT  
		Size: 11.0 MB (10996271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5afe9550264897812fa33de89acbc4f0f367607d3dcf5d6a86eb1bb0bae35c9`  
		Last Modified: Sat, 21 Oct 2023 03:32:10 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f9fa7ce470404293b8ddef59f600a551985b465c6c38778603ea985e6fdbc31`  
		Last Modified: Sat, 21 Oct 2023 03:32:10 GMT  
		Size: 18.7 KB (18683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58976cfd1258c57207f41f80007f5811044690e5e4c01c02eceb8f229aaca902`  
		Last Modified: Sat, 21 Oct 2023 03:32:10 GMT  
		Size: 8.7 KB (8715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7947900f0cf277eebcb7198b250c1cb4b9da00e9a7f711fe064407360eab23`  
		Last Modified: Wed, 08 Nov 2023 20:37:23 GMT  
		Size: 1.8 MB (1827219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b35d8c90b8ae9560bc24d46ddd256faf9e7517b660b0012a6146d396e4173b1`  
		Last Modified: Wed, 08 Nov 2023 20:37:23 GMT  
		Size: 311.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6a7f92cf9a4518ab2fc839b8997d9850325ef5b06e3f5dac830655a7a4ebd8`  
		Last Modified: Wed, 08 Nov 2023 20:39:42 GMT  
		Size: 3.4 MB (3410317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:7-fpm-alpine3.16` - linux; arm variant v7

```console
$ docker pull drupal@sha256:ed4d536810588e4cf329d4050f7eb07a238c25158ad1b79afb32c6e48434c16a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 MB (31516155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a235c2f0518d37966d485a32810197af91e14b11f080d65a4bd6c34e92f6413`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 07 Jun 2023 21:27:14 GMT
ADD file:911497ffc967e53c16d8356f320bf61fe06b85fc3250b7c01183f7bcfbfef404 in / 
# Wed, 07 Jun 2023 21:27:14 GMT
CMD ["/bin/sh"]
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 07 Jun 2023 21:27:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 07 Jun 2023 21:27:14 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4 39B641343D8C104B2B146DC3F9C39DC0B9698544
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_VERSION=8.0.30
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.30.tar.xz.asc
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_SHA256=216ab305737a5d392107112d618a755dc5df42058226f1670e9db90e77d777d9
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 07 Jun 2023 21:27:14 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 07 Jun 2023 21:27:14 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 07 Jun 2023 21:27:14 GMT
RUN docker-php-ext-enable sodium
# Wed, 07 Jun 2023 21:27:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 07 Jun 2023 21:27:14 GMT
WORKDIR /var/www/html
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 07 Jun 2023 21:27:14 GMT
STOPSIGNAL SIGQUIT
# Wed, 07 Jun 2023 21:27:14 GMT
EXPOSE 9000
# Wed, 07 Jun 2023 21:27:14 GMT
CMD ["php-fpm"]
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 07 Jun 2023 21:27:14 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 07 Jun 2023 21:27:14 GMT
ENV DRUPAL_VERSION=7.98
# Wed, 07 Jun 2023 21:27:14 GMT
ENV DRUPAL_MD5=4139f0feecb44a53645242194809b73a
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:d27c9f7e5791cecbf0251c0e7638ad6fbd2b510f038f66cc06c933da98c75979`  
		Last Modified: Mon, 07 Aug 2023 19:58:18 GMT  
		Size: 2.4 MB (2419274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee28d7774c683e5fd44e8b5f395d15311d75b1cf5300040efac8c1a085da3d4a`  
		Last Modified: Sat, 21 Oct 2023 03:51:19 GMT  
		Size: 2.8 MB (2791922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a51f4b1ed371a17cb9c1f2e82837093fd51d9a2dd3f0e942cf9688f15da8fd6`  
		Last Modified: Sat, 21 Oct 2023 03:51:18 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ebc794bac90c8f790e8c5dad9fc57b1b79d9e58e02efe176e2ecdb10b511f2`  
		Last Modified: Sat, 21 Oct 2023 03:51:18 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c695bb1574ba1ff1645d8578822d2e3d2f837a45f8cc150a67fdffbcec32b93`  
		Last Modified: Sat, 21 Oct 2023 03:54:27 GMT  
		Size: 10.8 MB (10841077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb217111faca192bcffc9d5e109310ccf1ba2f83cb7b343eaf409ae58176403e`  
		Last Modified: Sat, 21 Oct 2023 03:54:26 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf20cfffe306c25cc306016ca339259bf959dc8e04bfb7dfbb17e44a2713012`  
		Last Modified: Sat, 21 Oct 2023 03:54:51 GMT  
		Size: 10.4 MB (10350156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593a395541ae95adb3f2e03b402a721103bdffd676b606d1e2129660342bd672`  
		Last Modified: Sat, 21 Oct 2023 03:54:49 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c7210a2e242f534c2fc26577eb08436124174fbebe4a6cc80dc7fa9e34eea7`  
		Last Modified: Sat, 21 Oct 2023 03:54:49 GMT  
		Size: 18.7 KB (18666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7baa4a188b711385b21d7117cb5f2bcd5489a8dc7d456f8120803b25681b2c6`  
		Last Modified: Sat, 21 Oct 2023 03:54:49 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5088a532d88805e3e97df66860385e85b2409c0c0a08d7ad876825265420fd`  
		Last Modified: Wed, 08 Nov 2023 21:15:41 GMT  
		Size: 1.7 MB (1671253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c127e0e9422cca8ad514025ff41f23027b2d92221e714a06e4cde6315c4b8843`  
		Last Modified: Wed, 08 Nov 2023 21:15:41 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5016c9bf8b1e1ee3569d7ea85a609e2d9dec8607c798c947995db96ff4b4c421`  
		Last Modified: Wed, 08 Nov 2023 21:34:05 GMT  
		Size: 3.4 MB (3410308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-fpm-alpine3.16` - unknown; unknown

```console
$ docker pull drupal@sha256:3f0073c1904366d0d1285d81c44d74a28289d4f12ed4e77a905a7a1b774dfd1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.6 KB (249620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53ef0873f4edbf8c3a3589bd95bdbdcb4e6a624ee9b27c54f3f351118b4b602`

```dockerfile
```

-	Layers:
	-	`sha256:15a15d28095ebef4507ae015db14eda9df39329eb2d8b7b8e12ca2d4f1fe9b71`  
		Last Modified: Wed, 08 Nov 2023 21:34:04 GMT  
		Size: 227.5 KB (227536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cdd99bbcbf6a84cf4c71e8f4c6b805319df5579eab137da0fc1fabbebe3324a`  
		Last Modified: Wed, 08 Nov 2023 21:34:04 GMT  
		Size: 22.1 KB (22084 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-fpm-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:c81a5a839ce0c4b9aff6a06197a454850206a7322a712e01676d9a23af14c93e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33660515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c6daa65737cc2af634627380029a70ee0aca09b273d0fd357efa037ab00f7e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 07 Jun 2023 21:27:14 GMT
ADD file:cf85500a1f5b87a88587b279c8b8018eebeb3092f402b7e2cc4ad3873e078580 in / 
# Wed, 07 Jun 2023 21:27:14 GMT
CMD ["/bin/sh"]
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 07 Jun 2023 21:27:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 07 Jun 2023 21:27:14 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4 39B641343D8C104B2B146DC3F9C39DC0B9698544
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_VERSION=8.0.30
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.30.tar.xz.asc
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_SHA256=216ab305737a5d392107112d618a755dc5df42058226f1670e9db90e77d777d9
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 07 Jun 2023 21:27:14 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 07 Jun 2023 21:27:14 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 07 Jun 2023 21:27:14 GMT
RUN docker-php-ext-enable sodium
# Wed, 07 Jun 2023 21:27:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 07 Jun 2023 21:27:14 GMT
WORKDIR /var/www/html
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 07 Jun 2023 21:27:14 GMT
STOPSIGNAL SIGQUIT
# Wed, 07 Jun 2023 21:27:14 GMT
EXPOSE 9000
# Wed, 07 Jun 2023 21:27:14 GMT
CMD ["php-fpm"]
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 07 Jun 2023 21:27:14 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 07 Jun 2023 21:27:14 GMT
ENV DRUPAL_VERSION=7.98
# Wed, 07 Jun 2023 21:27:14 GMT
ENV DRUPAL_MD5=4139f0feecb44a53645242194809b73a
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:bdb2de7ba06c3a4e10b98f439a8c70afd63eee492c2ddc32342331a8e9ef4ff7`  
		Last Modified: Mon, 07 Aug 2023 19:40:08 GMT  
		Size: 2.7 MB (2708023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4873b5500beef0fb0e64486d59afee5c2bb6e5da82b13b0a1c144d2a5723df05`  
		Last Modified: Sat, 21 Oct 2023 05:53:41 GMT  
		Size: 3.1 MB (3136773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca0ef7ff9b3c37b3fd8c65b09b8bbb64bef4e2ab1ddcec7dd3b678ba720ec85`  
		Last Modified: Sat, 21 Oct 2023 05:53:40 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9c8e2ca46cffeed2a842efc18d46bcdad73931b21fcfac02f97f1574411c80`  
		Last Modified: Sat, 21 Oct 2023 05:53:40 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9c741ab944482a846bf596509d75cdacecfbe3f5359890a0c3cf42a87c5b44`  
		Last Modified: Sat, 21 Oct 2023 05:56:37 GMT  
		Size: 10.8 MB (10841088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4c7e9f6c0522373aee45625b9ca9c0857fbfb66d1648d09e9474e352d2ad70`  
		Last Modified: Sat, 21 Oct 2023 05:56:36 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb88782cbb198406f27d9e95dd529882d96961d2f34de05c75bda0b77b0c83db`  
		Last Modified: Sat, 21 Oct 2023 05:57:01 GMT  
		Size: 11.6 MB (11572892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9d2d364fcb5cbb2bde8f2e7ce7a2359206a946f48e148d538a1c1b1c165bb9`  
		Last Modified: Sat, 21 Oct 2023 05:56:59 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996ddf1a56fd5cd3028776ccc1721f753f13dd18584ba89a63a15dfaf3eae0a6`  
		Last Modified: Sat, 21 Oct 2023 05:56:59 GMT  
		Size: 18.7 KB (18683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066c5c2fd57710911258b1eb1f298d23f9d8ac47e72ae6977411f876ac8e0645`  
		Last Modified: Sat, 21 Oct 2023 05:56:59 GMT  
		Size: 8.7 KB (8712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb777de20a38a2f8ffcf0ca80b8210b16b101c69fb478fa7721ead296fd463c3`  
		Last Modified: Wed, 08 Nov 2023 22:03:38 GMT  
		Size: 2.0 MB (1959252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1690f80377823f91acb9a2422f387fc91aba6838caf827f4de5da1258a13db`  
		Last Modified: Wed, 08 Nov 2023 22:03:37 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799e8df72831702fa9242d8119fe4c8646ea1bbb79f1d27a2254a04c7b53cbbe`  
		Last Modified: Wed, 08 Nov 2023 22:10:03 GMT  
		Size: 3.4 MB (3410304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-fpm-alpine3.16` - unknown; unknown

```console
$ docker pull drupal@sha256:fc1d5793a9bf4cf94874c86eee9a9315347c8b269451a29cfcb27ba688d98e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.5 KB (249509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf03b13a406f8686dc968777cbca27ff4779be946992c0d8c8f06f9482b8bdf`

```dockerfile
```

-	Layers:
	-	`sha256:99d36357174603dad0aaa677e50b00d8ac579277f32463333c859bea17473c6c`  
		Last Modified: Wed, 08 Nov 2023 22:10:02 GMT  
		Size: 227.5 KB (227511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2864031cb13ebf3ee725d2c43e8f379e0364e5907c45e5e7a461b2bd0ebe0545`  
		Last Modified: Wed, 08 Nov 2023 22:10:02 GMT  
		Size: 22.0 KB (21998 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-fpm-alpine3.16` - linux; 386

```console
$ docker pull drupal@sha256:12de4226c30f06f378c420dd96d44ef1d7d5e06dc672143e82ff3f8dafcb01f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 MB (35234376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2e55c384ba221ce12ceb26389f8cc88a6bf9f24d77ed55c057a2e4f8cc1bbc`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 07 Jun 2023 21:27:14 GMT
ADD file:c06b4f6991638e506d4d0a4d70c4a78ba30b971767802af4c6b837cdf59d4303 in / 
# Wed, 07 Jun 2023 21:27:14 GMT
CMD ["/bin/sh"]
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 07 Jun 2023 21:27:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 07 Jun 2023 21:27:14 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4 39B641343D8C104B2B146DC3F9C39DC0B9698544
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_VERSION=8.0.30
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.30.tar.xz.asc
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_SHA256=216ab305737a5d392107112d618a755dc5df42058226f1670e9db90e77d777d9
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 07 Jun 2023 21:27:14 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 07 Jun 2023 21:27:14 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 07 Jun 2023 21:27:14 GMT
RUN docker-php-ext-enable sodium
# Wed, 07 Jun 2023 21:27:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 07 Jun 2023 21:27:14 GMT
WORKDIR /var/www/html
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 07 Jun 2023 21:27:14 GMT
STOPSIGNAL SIGQUIT
# Wed, 07 Jun 2023 21:27:14 GMT
EXPOSE 9000
# Wed, 07 Jun 2023 21:27:14 GMT
CMD ["php-fpm"]
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 07 Jun 2023 21:27:14 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 07 Jun 2023 21:27:14 GMT
ENV DRUPAL_VERSION=7.98
# Wed, 07 Jun 2023 21:27:14 GMT
ENV DRUPAL_MD5=4139f0feecb44a53645242194809b73a
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:be0d19c155de823c6b37eaaba7cdec9085e8f1e39b1dd5982a19acb6c8c97cc5`  
		Last Modified: Mon, 07 Aug 2023 19:39:20 GMT  
		Size: 2.8 MB (2810553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab60b11be44ded17255e2b07ef14ff94ca90db0922b4cf1120f63ec19b8a30d7`  
		Last Modified: Sat, 21 Oct 2023 06:42:41 GMT  
		Size: 3.4 MB (3367272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da81c63ee89e22e3f0c57c983ad3cb901858da3f4a7983b84f1ba81b25e63ee`  
		Last Modified: Sat, 21 Oct 2023 06:42:41 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb04f05bfbc194b18efada0fbbd784b8a8219f28d5978f3c9b9a8a7e40a797b`  
		Last Modified: Sat, 21 Oct 2023 06:42:41 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e50ac4051e406f09a0d2428270ed3f033f8f77b26a64d0ac4bc680aca60ac1`  
		Last Modified: Sat, 21 Oct 2023 06:46:13 GMT  
		Size: 10.8 MB (10841080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8af7715789fd69e523c31eb9ec99bf716b26e80f58212d02553977fecba98fc`  
		Last Modified: Sat, 21 Oct 2023 06:46:11 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b20c50a8a0cbe56d40ecf715424bbc74131b226854b1f2ff6d7adaf4ad2a67`  
		Last Modified: Sat, 21 Oct 2023 06:46:40 GMT  
		Size: 12.4 MB (12358006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efbb1b0aab39e7c1abb283fb6854f440e2c28c2db5044ddc74bb4aea07ef547`  
		Last Modified: Sat, 21 Oct 2023 06:46:37 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68cc590ac141aea433c32a42f4429a15c306eb5d270c8f1063717cd1b4ccd5f4`  
		Last Modified: Sat, 21 Oct 2023 06:46:37 GMT  
		Size: 18.7 KB (18676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb83a26c0e1bab3a091b32e56ae0331cda15ceae218e5901af6eb6f1ce423c3`  
		Last Modified: Sat, 21 Oct 2023 06:46:37 GMT  
		Size: 8.7 KB (8713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a459e9847972d84e08afe2b4c32071361128614f57b76f0a57f2b796ad33ad`  
		Last Modified: Wed, 08 Nov 2023 20:28:29 GMT  
		Size: 2.4 MB (2415004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7434bde0b6fcf783953797cbec33d304e330fdb1a27270d8089cb91d2816cd0`  
		Last Modified: Wed, 08 Nov 2023 20:28:29 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da69344712212a0e2511c916f0b6c3f3522fdd0056de6f18453214fb252fadf`  
		Last Modified: Wed, 08 Nov 2023 20:28:30 GMT  
		Size: 3.4 MB (3410280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-fpm-alpine3.16` - unknown; unknown

```console
$ docker pull drupal@sha256:e3648435830612131c983d3df86d4b55af31858f8e2e891effdab406f3bdc495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 KB (23365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af1b777b317af21c62cdf794714f541ce33372ce67cc1e94508019f40adfeb2`

```dockerfile
```

-	Layers:
	-	`sha256:d4650e3a4daf9ef6e6c6b5cc5f804ccb52c18d786c21daa12a117cc7571c3334`  
		Last Modified: Wed, 08 Nov 2023 20:28:28 GMT  
		Size: 23.4 KB (23365 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-fpm-alpine3.16` - linux; ppc64le

```console
$ docker pull drupal@sha256:ee3aeaebd0a533f7df48b5b4f449a035df308818431836b45f855cb0bc9a7e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (34991382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3e971469f4e26b1ed379f4167829946b1383a492cf845e3b1499066133a2b8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 07 Jun 2023 21:27:14 GMT
ADD file:b30c2945bf4c873440b2e390c7120f16abe08ec41b10c2fb248b9b1a7ad223fa in / 
# Wed, 07 Jun 2023 21:27:14 GMT
CMD ["/bin/sh"]
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 07 Jun 2023 21:27:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 07 Jun 2023 21:27:14 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4 39B641343D8C104B2B146DC3F9C39DC0B9698544
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_VERSION=8.0.30
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.30.tar.xz.asc
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_SHA256=216ab305737a5d392107112d618a755dc5df42058226f1670e9db90e77d777d9
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 07 Jun 2023 21:27:14 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 07 Jun 2023 21:27:14 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 07 Jun 2023 21:27:14 GMT
RUN docker-php-ext-enable sodium
# Wed, 07 Jun 2023 21:27:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 07 Jun 2023 21:27:14 GMT
WORKDIR /var/www/html
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 07 Jun 2023 21:27:14 GMT
STOPSIGNAL SIGQUIT
# Wed, 07 Jun 2023 21:27:14 GMT
EXPOSE 9000
# Wed, 07 Jun 2023 21:27:14 GMT
CMD ["php-fpm"]
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 07 Jun 2023 21:27:14 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 07 Jun 2023 21:27:14 GMT
ENV DRUPAL_VERSION=7.98
# Wed, 07 Jun 2023 21:27:14 GMT
ENV DRUPAL_MD5=4139f0feecb44a53645242194809b73a
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:cc1a557f8d111cc8c11359cd168abb441e150c9dc42a046349c5e51132461a47`  
		Last Modified: Mon, 07 Aug 2023 20:17:53 GMT  
		Size: 2.8 MB (2802326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0baf0740d041310f7cb40d5143135ea5f860dc8c15e2e54f1c71d5002f37176`  
		Last Modified: Sat, 21 Oct 2023 03:23:40 GMT  
		Size: 3.2 MB (3244695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1400ad3cd269e6cfd9f1b03b8650fefd415381694befd997045387ffbf1def`  
		Last Modified: Sat, 21 Oct 2023 03:23:38 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81f69a4dd23f1097cc16facc955e21a5e3fce1ef53842932cbd24946a67a96a`  
		Last Modified: Sat, 21 Oct 2023 03:23:39 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6128876b7818010cc7901f06f1987993018c099466a108fc021080b7191a7660`  
		Last Modified: Sat, 21 Oct 2023 03:27:03 GMT  
		Size: 10.8 MB (10841087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39dd6a9717c23fb901cd6a2861c4b33e448a9673fc3407f20789c4ff61e96d9`  
		Last Modified: Sat, 21 Oct 2023 03:27:02 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7371fc9ed83f484bf736bb79d0aa2a8f0e68dea8bb2ba5882afbd89d459360`  
		Last Modified: Sat, 21 Oct 2023 03:27:31 GMT  
		Size: 12.5 MB (12541256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de073fca06aa328e9b3049c87e1b5c4b1e9b6be342b092aa941b29bb5847adf6`  
		Last Modified: Sat, 21 Oct 2023 03:27:29 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094e57b83b33adedd53085aacc9c391289288d1d6990fb18ea63acffb2e71903`  
		Last Modified: Sat, 21 Oct 2023 03:27:29 GMT  
		Size: 18.7 KB (18676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d617d93757c4b018792c4ff302fc4d8333a1908eb4208f24e6a01933b89e3441`  
		Last Modified: Sat, 21 Oct 2023 03:27:29 GMT  
		Size: 8.7 KB (8716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b453210f0d5cff6c49d214135e7c3d40ec4e8dc7e1a4e3064bdb105694bfc833`  
		Last Modified: Wed, 08 Nov 2023 21:39:15 GMT  
		Size: 2.1 MB (2119536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff8e63991457f14881fa1939edd349ff0a49194307feb1d8fbaa4c694bd51d6`  
		Last Modified: Wed, 08 Nov 2023 21:39:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93af864e9d7974ef56b3b738a6696de297eba9c9fc28c48eccf94431453c54c7`  
		Last Modified: Wed, 08 Nov 2023 21:47:44 GMT  
		Size: 3.4 MB (3410300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-fpm-alpine3.16` - unknown; unknown

```console
$ docker pull drupal@sha256:850fa8b962dd9c6a48e0e1f8f6656f5fb838738c1f1b7d29c25b457e5db7b755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.9 KB (247928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79be87119f0c84c2caa8519e9f1d38112f2cd525e025edf6eb6827ed20ab0805`

```dockerfile
```

-	Layers:
	-	`sha256:666f6905d7e28f078e36e17b19146c4b4414d2d444605f64b44424f2c3b0c189`  
		Last Modified: Wed, 08 Nov 2023 21:47:43 GMT  
		Size: 225.9 KB (225898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:740866e824e2dab1cbdb284fca55c0b577972702d5186c572360f51e07616c26`  
		Last Modified: Wed, 08 Nov 2023 21:47:43 GMT  
		Size: 22.0 KB (22030 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-fpm-alpine3.16` - linux; s390x

```console
$ docker pull drupal@sha256:e33307498dd7f0797b7bbd45ea6271bb73a8970d27105c87e4a57ecc93b77d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33261362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be197ad7e5fccb0bbc6db7c78bfb1a330b7dfd662b54f0ee73acdab0400616af`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 07 Jun 2023 21:27:14 GMT
ADD file:39bfe995aa06bc953f4887751caefaa4576f3dfe63f0020b8989bb8b0a09c28f in / 
# Wed, 07 Jun 2023 21:27:14 GMT
CMD ["/bin/sh"]
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 07 Jun 2023 21:27:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 07 Jun 2023 21:27:14 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4 39B641343D8C104B2B146DC3F9C39DC0B9698544
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_VERSION=8.0.30
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.30.tar.xz.asc
# Wed, 07 Jun 2023 21:27:14 GMT
ENV PHP_SHA256=216ab305737a5d392107112d618a755dc5df42058226f1670e9db90e77d777d9
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 07 Jun 2023 21:27:14 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 07 Jun 2023 21:27:14 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 07 Jun 2023 21:27:14 GMT
RUN docker-php-ext-enable sodium
# Wed, 07 Jun 2023 21:27:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 07 Jun 2023 21:27:14 GMT
WORKDIR /var/www/html
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 07 Jun 2023 21:27:14 GMT
STOPSIGNAL SIGQUIT
# Wed, 07 Jun 2023 21:27:14 GMT
EXPOSE 9000
# Wed, 07 Jun 2023 21:27:14 GMT
CMD ["php-fpm"]
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 07 Jun 2023 21:27:14 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 07 Jun 2023 21:27:14 GMT
ENV DRUPAL_VERSION=7.98
# Wed, 07 Jun 2023 21:27:14 GMT
ENV DRUPAL_MD5=4139f0feecb44a53645242194809b73a
# Wed, 07 Jun 2023 21:27:14 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:e5761c1ed80af1ea48f655cdeb0fa9a89fe7d3903985d9ea08286e940a4f30dd`  
		Last Modified: Mon, 07 Aug 2023 19:42:55 GMT  
		Size: 2.6 MB (2591728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20443426c997e5dea66d1e33aa87278b02e934864058a1b568c26bea668ad008`  
		Last Modified: Sat, 21 Oct 2023 03:29:05 GMT  
		Size: 3.1 MB (3060579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593e46b058b7120521ccd39e9b6d8ddbbac17027f0e3b870ec17ae753459b9e9`  
		Last Modified: Sat, 21 Oct 2023 03:29:04 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d56adeebd730ddc00953f6f63aa9f3f1ef994e154c6c0705895ba7c3d68a915`  
		Last Modified: Sat, 21 Oct 2023 03:29:04 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0b02cbd9b91434bed05178be64d3c45f6916e353d6d072bcdeadf336761a36`  
		Last Modified: Sat, 21 Oct 2023 03:31:41 GMT  
		Size: 10.8 MB (10841103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e284fa08f39fa898fbc7d4aa7df250220098c2cc0fe412875398a3a6703c11f`  
		Last Modified: Sat, 21 Oct 2023 03:31:40 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc8a9e79e378645e2f58a5fc99193d2e7a17d2b97bf5dd81d2e1e593147be18`  
		Last Modified: Sat, 21 Oct 2023 03:31:59 GMT  
		Size: 11.3 MB (11336305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715a4bcfb468f19e0745e02ed159cdea00c7f0228f439f32194179300f3a069f`  
		Last Modified: Sat, 21 Oct 2023 03:31:57 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582f3fe36fa4e0f665df9f4916185215f9f4f27794052549181719000d9bcb61`  
		Last Modified: Sat, 21 Oct 2023 03:31:57 GMT  
		Size: 18.7 KB (18692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4946396af9bb4ec13b4b0056f394e74d038666315c23104c766d50e04ac9bc`  
		Last Modified: Sat, 21 Oct 2023 03:31:57 GMT  
		Size: 8.7 KB (8716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9569a456eb704bfd9adbab565f0d01f2ee31bc07a53ece943adc1ff53a5480`  
		Last Modified: Wed, 08 Nov 2023 21:12:04 GMT  
		Size: 2.0 MB (1989131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48edbebd7205d359813f328bf8f4ee4977b877384c2b24ec1c4bae4f6199da67`  
		Last Modified: Wed, 08 Nov 2023 21:12:04 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d6513a2ffb309bb01dd6a147cb4e97ab23f19ac3e1f2e618c3c2071e681cd7`  
		Last Modified: Wed, 08 Nov 2023 21:28:02 GMT  
		Size: 3.4 MB (3410317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-fpm-alpine3.16` - unknown; unknown

```console
$ docker pull drupal@sha256:4e92ee26e86e7b2e684865c3446ccf9777e675e607a760e369a64a53b92d7ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.9 KB (247851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceec11281320bcfc13b4ba448aff6d757b304ee6b45debfcb37a9b14eb32a8e7`

```dockerfile
```

-	Layers:
	-	`sha256:84b40341cf82d12ef1d991aeb65cccc198dc7277d05e660a83315f0ce64a0037`  
		Last Modified: Wed, 08 Nov 2023 21:28:02 GMT  
		Size: 225.9 KB (225864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e0aafb4c8c481dde4768c4db9586775c38edf4fc6fe4914ed5a4dfa0b680f74`  
		Last Modified: Wed, 08 Nov 2023 21:28:02 GMT  
		Size: 22.0 KB (21987 bytes)  
		MIME: application/vnd.in-toto+json
