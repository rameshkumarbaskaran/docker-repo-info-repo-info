## `drupal:7-apache`

```console
$ docker pull drupal@sha256:20b1cb54eacdd3888cff6906276c157d1bb3431c63c727b879c686d1fa80f9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `drupal:7-apache` - linux; amd64

```console
$ docker pull drupal@sha256:18efab6d464fd91bf59053c63f3dac9ec81e1f46b1576f32612ae71b41eca278
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.9 MB (169909517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa487de42f28b170f8b1dd53ecb8c36819e7116c1cad1c0bd549a4fb7013449e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 04:37:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 May 2023 04:37:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 May 2023 04:37:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 04:37:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 May 2023 04:37:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 May 2023 04:41:02 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 03 May 2023 04:41:02 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 03 May 2023 04:41:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 03 May 2023 04:41:12 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 03 May 2023 04:41:12 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 03 May 2023 04:41:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 04:41:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 04:41:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 May 2023 06:27:02 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Wed, 03 May 2023 06:27:02 GMT
ENV PHP_VERSION=8.0.28
# Wed, 03 May 2023 06:27:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.28.tar.xz.asc
# Wed, 03 May 2023 06:27:02 GMT
ENV PHP_SHA256=5e07278a1f315a67d36a676c01343ca2d4da5ec5bdb15d018e4248b3012bc0cd
# Wed, 03 May 2023 06:27:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 May 2023 06:27:14 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 May 2023 06:30:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 May 2023 06:30:08 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 03 May 2023 06:30:09 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 May 2023 06:30:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 May 2023 06:30:09 GMT
STOPSIGNAL SIGWINCH
# Wed, 03 May 2023 06:30:09 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 03 May 2023 06:30:09 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 06:30:09 GMT
EXPOSE 80
# Wed, 03 May 2023 06:30:09 GMT
CMD ["apache2-foreground"]
# Thu, 04 May 2023 05:01:45 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 05:01:46 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 04 May 2023 05:08:58 GMT
ENV DRUPAL_VERSION=7.97
# Thu, 04 May 2023 05:08:58 GMT
ENV DRUPAL_MD5=37b63299e115a9e8863f564780a026e9
# Thu, 04 May 2023 05:08:59 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07353b772b5e325bf0abf03512cfaebe590a14a0858cf0ec2740b5ab055a31a7`  
		Last Modified: Wed, 03 May 2023 06:50:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5908153120ba6d8988feadd5f6a8c68a281970ad001ac3be0f5bc9dc030b5c4d`  
		Last Modified: Wed, 03 May 2023 06:51:01 GMT  
		Size: 91.6 MB (91635527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8681ad2eeea6fa7d3aed97bcd471bddff6b4932f405ecb84452c3d2522390e2a`  
		Last Modified: Wed, 03 May 2023 06:50:49 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92711ce78973323920b717b53e3a3e197c7b958c6e1a1be2a69b72718519c96a`  
		Last Modified: Wed, 03 May 2023 06:51:31 GMT  
		Size: 19.2 MB (19248134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1c5be6427ed0108e9859238ab41d37f43b792c65758e165f1cb957e7c4ab45`  
		Last Modified: Wed, 03 May 2023 06:51:28 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d02a81768ed9803772d4654c2b55b24c54d1200a872fccc3b689b8dd84cebd9`  
		Last Modified: Wed, 03 May 2023 06:51:28 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d674a0135f85fa25714f9d22cc061f1e3743cd2274d0446b1943113027bb67a5`  
		Last Modified: Wed, 03 May 2023 07:01:33 GMT  
		Size: 11.1 MB (11142906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d87d03598175bfd15a7f8d90700ae62943df3c9be72b1434b7df1506e42bd32`  
		Last Modified: Wed, 03 May 2023 07:01:30 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8c2df9b69e488567399d647cb6e6cb0fe697131f891fb5210a5a9c91e24910`  
		Last Modified: Wed, 03 May 2023 07:01:32 GMT  
		Size: 10.8 MB (10775910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aacfb138e3c154e9bd1ba67b86c7eebf6ab10d180f6e8ede5073b9e3c608c6e3`  
		Last Modified: Wed, 03 May 2023 07:01:31 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db2528ade336d6a364955db7f8f00b611f66e103ccebbc0ff8ce392861dbae7`  
		Last Modified: Wed, 03 May 2023 07:01:30 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beeef66f0c04e387386a2642675efa5b32bf6a5d69e9abe09896e07828508758`  
		Last Modified: Wed, 03 May 2023 07:01:30 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac3c4efeb1180441da05384c731f8263e2500711199b53115a0be8a11547d73`  
		Last Modified: Thu, 04 May 2023 05:21:05 GMT  
		Size: 2.3 MB (2294096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092461e9b9864f8d0347d4b9c58f27073f272572437d96b4effd1a10c6205489`  
		Last Modified: Thu, 04 May 2023 05:21:05 GMT  
		Size: 313.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7a9bca10f7cd7a90797f46b78cabc1a604ff75b48c54fdd1a5b2925ea63eb2`  
		Last Modified: Thu, 04 May 2023 05:26:46 GMT  
		Size: 3.4 MB (3403544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:7-apache` - linux; arm variant v5

```console
$ docker pull drupal@sha256:26e34f43035ea13a9eef0cd644b5d11167350c2c811df79f627f700049839f93
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.3 MB (147276378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d1c361369f8d6688991b9051a6532ac271a2585c819ef74dada94672e772c66`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 02 May 2023 22:48:53 GMT
ADD file:ca82c0d9094c1022a00b5f2157a02e1a9032aafc357a41c76c6b60bd74d25395 in / 
# Tue, 02 May 2023 22:48:53 GMT
CMD ["bash"]
# Wed, 03 May 2023 04:52:59 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 May 2023 04:52:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 May 2023 04:53:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 04:53:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 May 2023 04:53:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 May 2023 04:57:06 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 03 May 2023 04:57:06 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 03 May 2023 04:57:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 03 May 2023 04:57:18 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 03 May 2023 04:57:19 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 03 May 2023 04:57:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 04:57:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 04:57:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 May 2023 05:50:22 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Wed, 03 May 2023 05:50:22 GMT
ENV PHP_VERSION=8.0.28
# Wed, 03 May 2023 05:50:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.28.tar.xz.asc
# Wed, 03 May 2023 05:50:23 GMT
ENV PHP_SHA256=5e07278a1f315a67d36a676c01343ca2d4da5ec5bdb15d018e4248b3012bc0cd
# Wed, 03 May 2023 05:50:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 May 2023 05:50:36 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 May 2023 05:52:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 May 2023 05:52:53 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 03 May 2023 05:52:53 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 May 2023 05:52:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 May 2023 05:52:54 GMT
STOPSIGNAL SIGWINCH
# Wed, 03 May 2023 05:52:54 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 03 May 2023 05:52:54 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 05:52:54 GMT
EXPOSE 80
# Wed, 03 May 2023 05:52:54 GMT
CMD ["apache2-foreground"]
# Wed, 03 May 2023 12:15:19 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 12:15:20 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 03 May 2023 12:15:20 GMT
ENV DRUPAL_VERSION=7.97
# Wed, 03 May 2023 12:15:20 GMT
ENV DRUPAL_MD5=37b63299e115a9e8863f564780a026e9
# Wed, 03 May 2023 12:15:22 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:eb6ee5d3f82142e70aca665cea92048b1a46ff1aa5c5be47a04c27a471470c07`  
		Last Modified: Tue, 02 May 2023 22:51:25 GMT  
		Size: 28.9 MB (28903418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85385d8a3476710ef72295538768f9c56689b7564ab9659e81ba54b2c44cd6ac`  
		Last Modified: Wed, 03 May 2023 05:58:33 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1055ef3089b9a2f598b1acf9be9ce3f9c8ca52737a33b747346c1d95163280eb`  
		Last Modified: Wed, 03 May 2023 05:58:46 GMT  
		Size: 73.7 MB (73687109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bce127d0f710a63a0c4f56d4db41b96c20ef29e12706dd814ad1791a03d4e78`  
		Last Modified: Wed, 03 May 2023 05:58:33 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5128568fc52dd737c8c7c6e4619d2d953f7823880670051fb58a3cd97f4f142f`  
		Last Modified: Wed, 03 May 2023 05:59:16 GMT  
		Size: 18.5 MB (18548530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3ea7ea903f65a529fc14b10916ebd2596aeab47d1938317742b4cd4879d69b`  
		Last Modified: Wed, 03 May 2023 05:59:12 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8260da688e16d2b01fda95e7d18674e0b415261617c9ab6ec78996b1015add03`  
		Last Modified: Wed, 03 May 2023 05:59:12 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e76a169e6ba8a3e3fa7f4510c18d739df1adf4d3de5b44ce809c14a02c698cc`  
		Last Modified: Wed, 03 May 2023 06:05:05 GMT  
		Size: 11.1 MB (11141296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5ed44202b7b045f43835747f11b56474ccd9c1e83ebaa98741ed10d200a399`  
		Last Modified: Wed, 03 May 2023 06:05:02 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89de207f7d4ba17c653c634e4645598d0f0bac9abf00dc4db20c2e39e62b238`  
		Last Modified: Wed, 03 May 2023 06:05:04 GMT  
		Size: 9.8 MB (9789589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df160b9595aa81059b8be0fe49ef1bd2cb78353b666323f3d66c9a3a9a7a91c9`  
		Last Modified: Wed, 03 May 2023 06:05:02 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2fefb5eb7f12946eb453da70ce480698e71416940a3633834a62df88031739e`  
		Last Modified: Wed, 03 May 2023 06:05:02 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f3d926634d167a3b8af714426dae5fa317bee0feadb23e96d0b8f9d0cd67b1`  
		Last Modified: Wed, 03 May 2023 06:05:02 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:549ff4664295014e321bf691225050db4ee95147a3e8c47010d3964c1ca915a4`  
		Last Modified: Wed, 03 May 2023 12:16:31 GMT  
		Size: 1.8 MB (1797007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f089e0831aa78497092040108e0734425ca7650f9314b6d62521971f92f8ea`  
		Last Modified: Wed, 03 May 2023 12:16:30 GMT  
		Size: 314.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8f4ebdc773f980dc51e20ad6b478812042d48f22dda5e0d3b9707919c3a4a9`  
		Last Modified: Wed, 03 May 2023 12:16:32 GMT  
		Size: 3.4 MB (3403543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:7-apache` - linux; arm variant v7

```console
$ docker pull drupal@sha256:692edf22de9ba722cc72d7833c9eaf8dd3a778ecb948daf947edfe4989f4428f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139415960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0943cf53c6ac4eceb07503bcce4b434571ddccaf05436edfc5b49f268d2100f8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 02 May 2023 23:47:57 GMT
ADD file:69d82e947b50a0f0ec610822ffe7c23ec1f6eb41bc17068502380f827cbcce40 in / 
# Tue, 02 May 2023 23:47:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 06:02:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 May 2023 06:02:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 May 2023 06:02:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 06:02:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 May 2023 06:02:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 May 2023 06:05:32 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 03 May 2023 06:05:32 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 03 May 2023 06:05:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 03 May 2023 06:05:44 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 03 May 2023 06:05:44 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 03 May 2023 06:05:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 06:05:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 06:05:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 May 2023 07:27:11 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Wed, 03 May 2023 07:27:12 GMT
ENV PHP_VERSION=8.0.28
# Wed, 03 May 2023 07:27:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.28.tar.xz.asc
# Wed, 03 May 2023 07:27:12 GMT
ENV PHP_SHA256=5e07278a1f315a67d36a676c01343ca2d4da5ec5bdb15d018e4248b3012bc0cd
# Wed, 03 May 2023 07:27:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 May 2023 07:27:23 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 May 2023 07:29:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 May 2023 07:29:29 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 03 May 2023 07:29:30 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 May 2023 07:29:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 May 2023 07:29:30 GMT
STOPSIGNAL SIGWINCH
# Wed, 03 May 2023 07:29:30 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 03 May 2023 07:29:30 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 07:29:30 GMT
EXPOSE 80
# Wed, 03 May 2023 07:29:30 GMT
CMD ["apache2-foreground"]
# Thu, 04 May 2023 02:51:19 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 02:51:20 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 04 May 2023 02:59:35 GMT
ENV DRUPAL_VERSION=7.97
# Thu, 04 May 2023 02:59:35 GMT
ENV DRUPAL_MD5=37b63299e115a9e8863f564780a026e9
# Thu, 04 May 2023 02:59:36 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:9c7c4e67baad3ce38491ce8c1ffaa9ca9ce37409270ce53ab3472054f35d097e`  
		Last Modified: Tue, 02 May 2023 23:51:30 GMT  
		Size: 26.6 MB (26564648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4223092dddf6040b9cb3d66826248ca3c50557af6320203e8a40b6e549bb0f2c`  
		Last Modified: Wed, 03 May 2023 07:46:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922e3f7fe606e6c4954d1d9e944c9f9e610ff10a76127e6d51a955e8cc42772b`  
		Last Modified: Wed, 03 May 2023 07:46:36 GMT  
		Size: 69.3 MB (69320181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3bf68a94eff4021eeb6ae2522f556ef8567c37e2fb6f1155469a278208edf3`  
		Last Modified: Wed, 03 May 2023 07:46:25 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70939fb624f471cb7fcaaa48c91697a6b8745045cfa06a955b53b7517a5f26c3`  
		Last Modified: Wed, 03 May 2023 07:47:00 GMT  
		Size: 18.0 MB (18007946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2479125a48d14056528c5be7d389f2fb2b0977398a03fc50730f41f2944a26`  
		Last Modified: Wed, 03 May 2023 07:46:57 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c698e83c34140865f214984aca5d4ab163aa1df710e78e5df4fb286f2043e9e`  
		Last Modified: Wed, 03 May 2023 07:46:57 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec47d452f87cbba6f5ae35c1fd030c19586505f76e8fcf458454aeba80ee7f78`  
		Last Modified: Wed, 03 May 2023 07:56:55 GMT  
		Size: 11.1 MB (11141282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6495a9c7d22df04ddff3164fc71c9fbdb6595ebc60f3d6116c81c8f7d587c8f`  
		Last Modified: Wed, 03 May 2023 07:56:52 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2dd95f296a4dc85bb83446f32f041abad42bb387a84ee0d507b46b8bcd343a`  
		Last Modified: Wed, 03 May 2023 07:56:55 GMT  
		Size: 9.3 MB (9306020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc8940b12102a6d233e3524fcb02ba54a16281339ed467b935de9b4b6e5b648`  
		Last Modified: Wed, 03 May 2023 07:56:53 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567f7483c19ceab3fe882715c6b265b824ce685bc99b6e4e8608d758ca24d0f6`  
		Last Modified: Wed, 03 May 2023 07:56:52 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad0ffb8c0cbe0fb433b890d6297282ef5e7cc7d962e91c60065e77c7a401a92`  
		Last Modified: Wed, 03 May 2023 07:56:53 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffcd2bc22a4e97180d21809dae1d4c79b64e8694d12392e37b0550c001399b95`  
		Last Modified: Thu, 04 May 2023 03:12:17 GMT  
		Size: 1.7 MB (1666455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d7d49178da529c83891163c8ec5883f697146899479e2c427b6a0af691c91f`  
		Last Modified: Thu, 04 May 2023 03:12:18 GMT  
		Size: 313.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a26216d8fc1a75a63883f200045bab1f24d5cc162b420daa4e3fc49d55b2d7`  
		Last Modified: Thu, 04 May 2023 03:18:21 GMT  
		Size: 3.4 MB (3403544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:7-apache` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:7c1893e71186dbca790fed6436205f1cfed1d731f537869785607fe844334baa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162873530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856cb2462341266176c863013e000fe3182eb342072fba5e226d1639b35b66ea`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 03:52:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 May 2023 03:52:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 May 2023 03:52:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 03:52:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 May 2023 03:52:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 May 2023 03:56:04 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 03 May 2023 03:56:04 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 03 May 2023 03:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 03 May 2023 03:56:14 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 03 May 2023 03:56:14 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 03 May 2023 03:56:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 03:56:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 03:56:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 May 2023 05:33:29 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Wed, 03 May 2023 05:33:29 GMT
ENV PHP_VERSION=8.0.28
# Wed, 03 May 2023 05:33:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.28.tar.xz.asc
# Wed, 03 May 2023 05:33:29 GMT
ENV PHP_SHA256=5e07278a1f315a67d36a676c01343ca2d4da5ec5bdb15d018e4248b3012bc0cd
# Wed, 03 May 2023 05:33:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 May 2023 05:33:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 May 2023 05:35:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 May 2023 05:35:36 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 03 May 2023 05:35:37 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 May 2023 05:35:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 May 2023 05:35:37 GMT
STOPSIGNAL SIGWINCH
# Wed, 03 May 2023 05:35:37 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 03 May 2023 05:35:37 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 05:35:37 GMT
EXPOSE 80
# Wed, 03 May 2023 05:35:37 GMT
CMD ["apache2-foreground"]
# Wed, 03 May 2023 23:16:00 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 23:16:00 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 03 May 2023 23:23:06 GMT
ENV DRUPAL_VERSION=7.97
# Wed, 03 May 2023 23:23:07 GMT
ENV DRUPAL_MD5=37b63299e115a9e8863f564780a026e9
# Wed, 03 May 2023 23:23:07 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3582e155c24272674265389c3b317b84bec7ca237a6761ee690aed30a1c5ec9`  
		Last Modified: Wed, 03 May 2023 05:50:53 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:313de6edf03aac188b999f642b424cdc014f9f45e218d5ad620a727ef81fa7e1`  
		Last Modified: Wed, 03 May 2023 05:51:02 GMT  
		Size: 86.9 MB (86928311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a576c500430404ceffd53e7ce6f2898b260e011e85c77bdabd75342c1a6a54`  
		Last Modified: Wed, 03 May 2023 05:50:53 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249c4246fc75d4a1eefb130895fc367d8150e7076da4e329f94094a45c81cf4e`  
		Last Modified: Wed, 03 May 2023 05:51:26 GMT  
		Size: 19.2 MB (19170211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbc677cfb25a8634144c25b4c4f43c1173f08ca1eb16b4f3ae53aa11bc62040`  
		Last Modified: Wed, 03 May 2023 05:51:24 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca53ccc29d8c43aeff9c96a48096d009ccf0ee902bf0b5076defe39003f2a0e`  
		Last Modified: Wed, 03 May 2023 05:51:24 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81fde7a89e62b6048c9cb62c2ffe6af63c3083044645e382ea6a6ad99c1cac5`  
		Last Modified: Wed, 03 May 2023 06:01:01 GMT  
		Size: 11.1 MB (11142070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65465ad9ad827553311e6e589e563ab48e70b441b6a369b15163ab326c3a62b3`  
		Last Modified: Wed, 03 May 2023 06:00:59 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7f5fcc23917c72adb8430fc98e44fa15e6f0487bc44078a92955a1bb6adfa8`  
		Last Modified: Wed, 03 May 2023 06:01:00 GMT  
		Size: 10.2 MB (10233356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2e89a0acdeb3cb212a47433f7ccdaf15b941e51127926df285895723e903b4`  
		Last Modified: Wed, 03 May 2023 06:00:59 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56acc6a80c81b29997974b32b1455395b67a8602e8f6e2a28932dfb7ab58eea2`  
		Last Modified: Wed, 03 May 2023 06:00:59 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03cfc6f00bd090afde0726e6b7a4fe9caaca71065629f4ef636659f988f96052`  
		Last Modified: Wed, 03 May 2023 06:00:59 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de46447455d249671742e8fda287064c0a2bce527fa83f97492519f1cccde7d8`  
		Last Modified: Wed, 03 May 2023 23:34:50 GMT  
		Size: 1.9 MB (1937454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6921edabaabebe1918e7187a080e1522719dd17625ef45751f047d7a920eaa`  
		Last Modified: Wed, 03 May 2023 23:34:50 GMT  
		Size: 313.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34836bd1cf3f595c60ff42a6615b048033efcdb1982f0d2c06f8bc1254e91062`  
		Last Modified: Wed, 03 May 2023 23:40:11 GMT  
		Size: 3.4 MB (3403525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:7-apache` - linux; 386

```console
$ docker pull drupal@sha256:ad9e527a43ceba4ae0e6590efc502030a4deb1502fe27961c7acd68072958ce6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172737744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65bc0111870ed2e9d063843b7b98895f6e0fe8fcc46e79e4e44a2f73ed8ba146`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 03 May 2023 00:00:58 GMT
ADD file:caea439e2dbe0148904e3b9a0c5a843d2d0b7c196725d2b41790594e64dcdce8 in / 
# Wed, 03 May 2023 00:00:58 GMT
CMD ["bash"]
# Wed, 03 May 2023 08:55:46 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 May 2023 08:55:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 May 2023 08:56:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 08:56:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 May 2023 08:56:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 May 2023 09:01:39 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 03 May 2023 09:01:39 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 03 May 2023 09:01:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 03 May 2023 09:01:51 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 03 May 2023 09:01:52 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 03 May 2023 09:01:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 09:01:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 09:01:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 May 2023 11:50:10 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Wed, 03 May 2023 11:50:10 GMT
ENV PHP_VERSION=8.0.28
# Wed, 03 May 2023 11:50:10 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.28.tar.xz.asc
# Wed, 03 May 2023 11:50:10 GMT
ENV PHP_SHA256=5e07278a1f315a67d36a676c01343ca2d4da5ec5bdb15d018e4248b3012bc0cd
# Wed, 03 May 2023 11:50:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 May 2023 11:50:23 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 May 2023 11:55:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 May 2023 11:55:17 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 03 May 2023 11:55:17 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 May 2023 11:55:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 May 2023 11:55:17 GMT
STOPSIGNAL SIGWINCH
# Wed, 03 May 2023 11:55:18 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 03 May 2023 11:55:18 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 11:55:18 GMT
EXPOSE 80
# Wed, 03 May 2023 11:55:18 GMT
CMD ["apache2-foreground"]
# Thu, 04 May 2023 04:44:02 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 04:44:03 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 04 May 2023 04:52:31 GMT
ENV DRUPAL_VERSION=7.97
# Thu, 04 May 2023 04:52:31 GMT
ENV DRUPAL_MD5=37b63299e115a9e8863f564780a026e9
# Thu, 04 May 2023 04:52:32 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:10b34014bd1c165cc57a10e7492f17dce658513b7329319fe6c193c85bf752db`  
		Last Modified: Wed, 03 May 2023 00:05:12 GMT  
		Size: 32.4 MB (32388208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e767304c8a25a06c5180cd0487b1d298c8eb93b9276d7f8a33605daeec5deed`  
		Last Modified: Wed, 03 May 2023 12:27:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8469e5ef909b43afbcce2cb261155375a3b3f423dadb11383bf91b8d037358f`  
		Last Modified: Wed, 03 May 2023 12:28:07 GMT  
		Size: 92.7 MB (92719962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d946dbb11b755f5978864d6cb1f395dc513c314f5d182df53bd573895bbeb7a5`  
		Last Modified: Wed, 03 May 2023 12:27:47 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:924158f9311822c03627e43631de70ccf581b97a0430f7b72985bb4724547e87`  
		Last Modified: Wed, 03 May 2023 12:28:33 GMT  
		Size: 19.7 MB (19737280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace747d85a92d8e6182f02d61b25843d51b0e593121c7df2951fb700f4a49e55`  
		Last Modified: Wed, 03 May 2023 12:28:29 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cb964761efe81d0142e55a3784ad2802e32884c20d5859d2443482372701fa`  
		Last Modified: Wed, 03 May 2023 12:28:29 GMT  
		Size: 515.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec181025602d9b5319276036182dbc708b01d9aded2dd675b4aa55cde30c47e1`  
		Last Modified: Wed, 03 May 2023 12:39:45 GMT  
		Size: 11.1 MB (11142130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a49f575098ae44e020f1a87fb77d00c18a184bb0e3f84b24b039fb7d77dd9c4`  
		Last Modified: Wed, 03 May 2023 12:39:42 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039fde4b9a9f6169c1fc4921bde107d911adcada5692a370757606639ba3aa61`  
		Last Modified: Wed, 03 May 2023 12:39:45 GMT  
		Size: 11.0 MB (10981835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c632c1ff89860bcb0f45db1a4f4c20d69335bbc952f5f0846d8fe973c3e7e59e`  
		Last Modified: Wed, 03 May 2023 12:39:42 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b9f84b019d6bb5293bd7f47e4b19403d92268537a602bd895016170654cfbc`  
		Last Modified: Wed, 03 May 2023 12:39:42 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceebd725582d8d670a68d1a4f739676d4ea5bc3dc5e808783581d802c69621c7`  
		Last Modified: Wed, 03 May 2023 12:39:42 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849a1862c179e97cce90765a3cb4722a23812d60e19e1662c9df829e50b6c1ae`  
		Last Modified: Thu, 04 May 2023 05:05:57 GMT  
		Size: 2.4 MB (2358902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf96812cabe961cd31608b76ec9774098aa524d3aaf3ad9776e037d4691f04a9`  
		Last Modified: Thu, 04 May 2023 05:05:56 GMT  
		Size: 313.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52c62b785d74123584f50b623dc89e855ccaa456f08575e6dd38f7f71830c07`  
		Last Modified: Thu, 04 May 2023 05:12:31 GMT  
		Size: 3.4 MB (3403544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:7-apache` - linux; mips64le

```console
$ docker pull drupal@sha256:fc4963a28bc56323a4d8233bd87fa47cb31187daa6d47f33be9e8ee1a6946cd1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146549457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a57186a289000221724436bc5f5010b64adcc7ed518b19267bdbf5da92de04`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 12 Apr 2023 00:09:59 GMT
ADD file:2f558bb3cf4bc685f98fcdb12200961e3059267213f0caf7686523305967a663 in / 
# Wed, 12 Apr 2023 00:10:03 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 17:40:09 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 12 Apr 2023 17:40:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 12 Apr 2023 17:41:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 17:41:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 12 Apr 2023 17:41:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 12 Apr 2023 17:56:43 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 12 Apr 2023 17:56:47 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 12 Apr 2023 17:57:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 12 Apr 2023 17:57:52 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 12 Apr 2023 17:57:58 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 12 Apr 2023 17:58:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 12 Apr 2023 17:58:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 12 Apr 2023 17:58:08 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 12 Apr 2023 21:47:56 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Wed, 12 Apr 2023 21:48:00 GMT
ENV PHP_VERSION=8.0.28
# Wed, 12 Apr 2023 21:48:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.28.tar.xz.asc
# Wed, 12 Apr 2023 21:48:07 GMT
ENV PHP_SHA256=5e07278a1f315a67d36a676c01343ca2d4da5ec5bdb15d018e4248b3012bc0cd
# Wed, 12 Apr 2023 21:48:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 12 Apr 2023 21:49:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 12 Apr 2023 22:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 12 Apr 2023 22:02:26 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 12 Apr 2023 22:02:32 GMT
RUN docker-php-ext-enable sodium
# Wed, 12 Apr 2023 22:02:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 12 Apr 2023 22:02:40 GMT
STOPSIGNAL SIGWINCH
# Wed, 12 Apr 2023 22:02:43 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 12 Apr 2023 22:02:47 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 22:02:51 GMT
EXPOSE 80
# Wed, 12 Apr 2023 22:02:54 GMT
CMD ["apache2-foreground"]
# Thu, 13 Apr 2023 07:41:03 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Apr 2023 07:41:09 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 21 Apr 2023 21:00:46 GMT
ENV DRUPAL_VERSION=7.97
# Fri, 21 Apr 2023 21:00:50 GMT
ENV DRUPAL_MD5=37b63299e115a9e8863f564780a026e9
# Fri, 21 Apr 2023 21:01:00 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:8b0f62b0d33641c5348fd31abfd06463bdc4213a072d71479a0765756673777b`  
		Last Modified: Wed, 12 Apr 2023 00:17:28 GMT  
		Size: 29.6 MB (29639206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a69bb16c3f89448ac4380e4a6c9d78eeddcaa3c300324594dd6e2e4cf02617`  
		Last Modified: Wed, 12 Apr 2023 22:31:17 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92516d65e1f532cbcef2ec02722c2d8bfbe523ae63a6e14f136fad8253bf69e`  
		Last Modified: Wed, 12 Apr 2023 22:32:08 GMT  
		Size: 72.0 MB (72018898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c16f0df3f45b7f1adec8d38deb8031c5e01c12d046bf66f6d1b198ad3718dd5f`  
		Last Modified: Wed, 12 Apr 2023 22:31:17 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594e6b065bcbdea60291978c977209f7ed682e2c3d4c796dbf6e9ae2fb95518b`  
		Last Modified: Wed, 12 Apr 2023 22:32:48 GMT  
		Size: 18.9 MB (18946910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672065c916307da45f7abfbe36d6b608219f84fbbabb42b46a524986bda9a772`  
		Last Modified: Wed, 12 Apr 2023 22:32:36 GMT  
		Size: 438.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb687000899ee36170e2630950ff55713686987cdc618d935e1ca22fe2611a9`  
		Last Modified: Wed, 12 Apr 2023 22:32:35 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f0633b809e504e517e279ccd8b129cf322b033aefac585b2700707553a73f2`  
		Last Modified: Wed, 12 Apr 2023 22:42:09 GMT  
		Size: 10.9 MB (10924977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c51748b3474429257cd56f7ef11765a797033ca34c02a7fb1598202c561d82`  
		Last Modified: Wed, 12 Apr 2023 22:42:04 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c1affb4e4af37670a001a06a6e4b472746ebc4516251239e6a32adcfa610e57`  
		Last Modified: Wed, 12 Apr 2023 22:42:12 GMT  
		Size: 9.9 MB (9918235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0d36b11ca89dbaff67f1350a7dc2c909abaad686535be7253a779d668045c2`  
		Last Modified: Wed, 12 Apr 2023 22:42:04 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3968331e746bf3efde188be8202900c608f9080e2694fb2d5c2afc854b394373`  
		Last Modified: Wed, 12 Apr 2023 22:42:04 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfcac924a54e78b2b833deebeb6a3235fe274cf3ede0c3ed81ad1a6330efc0f2`  
		Last Modified: Wed, 12 Apr 2023 22:42:04 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f40db3d10dbf4f15ded5dd70feae821cef92cf2b07e505d515e8063a735eec6`  
		Last Modified: Thu, 13 Apr 2023 07:45:17 GMT  
		Size: 1.7 MB (1692206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95c66d28264ccf4b31fde99651d0aca318a1d8446db580ae6ea661ea96ea5d8`  
		Last Modified: Thu, 13 Apr 2023 07:45:16 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2dfbfd2572b09ffba549596af5db43ad4908fbf3a309af065bbe1d3046b4fe4`  
		Last Modified: Fri, 21 Apr 2023 21:01:51 GMT  
		Size: 3.4 MB (3403241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:7-apache` - linux; ppc64le

```console
$ docker pull drupal@sha256:28c7c651b87894137a40fc4ac8bf0d363bf1c4dc4b46e81b30a6cd201bb80851
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170282537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e87d6706c760716aa059662971fd389c121f0ba0d0feee78d0c672ae7d74860`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 12 Apr 2023 00:08:20 GMT
ADD file:63eb52aaff02c15bceabb87a78eb1b36389066ff4774cf8a754160ca7d509816 in / 
# Wed, 12 Apr 2023 00:08:23 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 02:53:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 12 Apr 2023 02:53:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 12 Apr 2023 02:54:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 02:55:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 12 Apr 2023 02:55:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 12 Apr 2023 03:00:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 12 Apr 2023 03:00:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 12 Apr 2023 03:00:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 12 Apr 2023 03:00:30 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 12 Apr 2023 03:00:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 12 Apr 2023 03:00:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 12 Apr 2023 03:00:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 12 Apr 2023 03:00:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 12 Apr 2023 04:31:09 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Wed, 12 Apr 2023 04:31:09 GMT
ENV PHP_VERSION=8.0.28
# Wed, 12 Apr 2023 04:31:10 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.28.tar.xz.asc
# Wed, 12 Apr 2023 04:31:11 GMT
ENV PHP_SHA256=5e07278a1f315a67d36a676c01343ca2d4da5ec5bdb15d018e4248b3012bc0cd
# Wed, 12 Apr 2023 04:32:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 12 Apr 2023 04:32:44 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 12 Apr 2023 04:38:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 12 Apr 2023 04:38:34 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 12 Apr 2023 04:38:39 GMT
RUN docker-php-ext-enable sodium
# Wed, 12 Apr 2023 04:38:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 12 Apr 2023 04:38:41 GMT
STOPSIGNAL SIGWINCH
# Wed, 12 Apr 2023 04:38:43 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 12 Apr 2023 04:38:44 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 04:38:46 GMT
EXPOSE 80
# Wed, 12 Apr 2023 04:38:46 GMT
CMD ["apache2-foreground"]
# Wed, 12 Apr 2023 12:07:40 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 12:07:41 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 21 Apr 2023 19:53:48 GMT
ENV DRUPAL_VERSION=7.97
# Fri, 21 Apr 2023 19:53:49 GMT
ENV DRUPAL_MD5=37b63299e115a9e8863f564780a026e9
# Fri, 21 Apr 2023 19:53:51 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:5b41d5ec640939cf684959234ad3b80909268a32bfd520a31c6720a91521c2fa`  
		Last Modified: Wed, 12 Apr 2023 00:13:13 GMT  
		Size: 35.3 MB (35291995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4881dab4e16a2b31707f063b4a6d06a7622c29a571e9941b45d4f1dbab9fa535`  
		Last Modified: Wed, 12 Apr 2023 04:52:52 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7112207942602cdd0c4444cb2cf85085ac4ac494a4140f7ad0d4b40bc5d9af2`  
		Last Modified: Wed, 12 Apr 2023 04:53:17 GMT  
		Size: 86.6 MB (86633054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc8a1d48af817593b6b8be59cd4822dcbbf90138a02afc42d1c359a66cef044`  
		Last Modified: Wed, 12 Apr 2023 04:52:52 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eebee4fe70939a7f850866922cd16aca329703d3398407739e4b38a6f027d89`  
		Last Modified: Wed, 12 Apr 2023 04:53:47 GMT  
		Size: 20.5 MB (20464162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbb6aa8a531755afded14a8c4ba085e312d53bcaf78332aeafd1dd4d3d8dbc0`  
		Last Modified: Wed, 12 Apr 2023 04:53:42 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef12174c7227dbbeb6d056ac319756c11bf63363c72a33b9ab7899b9dfc7f097`  
		Last Modified: Wed, 12 Apr 2023 04:53:42 GMT  
		Size: 514.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b352a09c77b083930793aa5c916e4c368eb2824b20ea20ff93af2421ef3f94`  
		Last Modified: Wed, 12 Apr 2023 05:01:21 GMT  
		Size: 11.1 MB (11142949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038e09744792299a6d85de69f02bea62e10ed9792a773af5b30fc0082f2fae44`  
		Last Modified: Wed, 12 Apr 2023 05:01:17 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b61986f00a0803adb5a7fe07c7716f019da2c97c381b983b95414ccc7d536c`  
		Last Modified: Wed, 12 Apr 2023 05:01:21 GMT  
		Size: 11.1 MB (11140292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf14fb455b1c2633429b80d26dfe8f189d9eacdb4ff23aa8417c9444e660f90`  
		Last Modified: Wed, 12 Apr 2023 05:01:17 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53621022b295fa0c7dfc4ef55592018e784c0d077c1f2247e6833d7c85dacadf`  
		Last Modified: Wed, 12 Apr 2023 05:01:17 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7119f73e1679a3ccf6604d2271d6bb56ab6be0a25f1aea828530b937b79d503`  
		Last Modified: Wed, 12 Apr 2023 05:01:17 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6185d1db295e126d608d1fdccdc4657c87b08b4aed567736a02615319433f66`  
		Last Modified: Wed, 12 Apr 2023 12:21:35 GMT  
		Size: 2.2 MB (2200664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c4084ef4c915c8e66307720a1e02b177565b354485ec940c1598a30d3d46a6`  
		Last Modified: Wed, 12 Apr 2023 12:21:35 GMT  
		Size: 312.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e5e61e8c765ff54765206056ad4ec4bd4f2dfeb927303bae051a28bf252a0d`  
		Last Modified: Fri, 21 Apr 2023 19:56:13 GMT  
		Size: 3.4 MB (3403536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:7-apache` - linux; s390x

```console
$ docker pull drupal@sha256:3ae957caf55a6d79a68fd3a8c12f4f2ce36ce7200476d6fade1b6525a5b9914b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.7 MB (146742607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f29a10109b774cd1348e30f3ed54015cae16efa4d487f894c540f83af5a40321`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 12 Apr 2023 00:01:00 GMT
ADD file:b6463dba97ba9c0a29bacfafc4d67bc603ab57e80b75e23cd42d7ef4b0f8e6ae in / 
# Wed, 12 Apr 2023 00:01:04 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 03:36:39 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 12 Apr 2023 03:36:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 12 Apr 2023 03:37:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 03:37:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 12 Apr 2023 03:37:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 12 Apr 2023 03:41:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 12 Apr 2023 03:41:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 12 Apr 2023 03:41:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 12 Apr 2023 03:41:37 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 12 Apr 2023 03:41:38 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 12 Apr 2023 03:41:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 12 Apr 2023 03:41:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 12 Apr 2023 03:41:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 12 Apr 2023 04:30:22 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Wed, 12 Apr 2023 04:30:22 GMT
ENV PHP_VERSION=8.0.28
# Wed, 12 Apr 2023 04:30:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.28.tar.xz.asc
# Wed, 12 Apr 2023 04:30:23 GMT
ENV PHP_SHA256=5e07278a1f315a67d36a676c01343ca2d4da5ec5bdb15d018e4248b3012bc0cd
# Wed, 12 Apr 2023 04:30:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 12 Apr 2023 04:30:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 12 Apr 2023 04:32:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 12 Apr 2023 04:32:40 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 12 Apr 2023 04:32:41 GMT
RUN docker-php-ext-enable sodium
# Wed, 12 Apr 2023 04:32:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 12 Apr 2023 04:32:41 GMT
STOPSIGNAL SIGWINCH
# Wed, 12 Apr 2023 04:32:41 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 12 Apr 2023 04:32:41 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 04:32:41 GMT
EXPOSE 80
# Wed, 12 Apr 2023 04:32:42 GMT
CMD ["apache2-foreground"]
# Wed, 12 Apr 2023 11:58:45 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 11:58:45 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 21 Apr 2023 20:16:11 GMT
ENV DRUPAL_VERSION=7.97
# Fri, 21 Apr 2023 20:16:12 GMT
ENV DRUPAL_MD5=37b63299e115a9e8863f564780a026e9
# Fri, 21 Apr 2023 20:16:17 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:97fe10bc7def58e7938e97e41eec4788ec7a45b6ef2cb1770cec02fa831fd19d`  
		Last Modified: Wed, 12 Apr 2023 00:05:18 GMT  
		Size: 29.7 MB (29653156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943e763db148606393f8c21697bc30f68ac8de11269141ae6e0d5e8483fe3e26`  
		Last Modified: Wed, 12 Apr 2023 04:40:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f8d95603c0d1c5673103183c025b2e49c72c82f4e8b4b3a86201eb804e7ffa`  
		Last Modified: Wed, 12 Apr 2023 04:40:55 GMT  
		Size: 71.6 MB (71629155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e864c428fd73e9e002327cf91695b364814ad36e7552a314e87ab897ca522f`  
		Last Modified: Wed, 12 Apr 2023 04:40:46 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4dc168720ddd2f3887093d1b990253b126ba4d7c7b85c8cdcaaa56cde796d25`  
		Last Modified: Wed, 12 Apr 2023 04:41:11 GMT  
		Size: 19.1 MB (19077445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994e736e66f1a50d03c9d0c3f816ba709888f0c93602761fdd8ce401cf3393d1`  
		Last Modified: Wed, 12 Apr 2023 04:41:09 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b0a054484820a2aa7ec78a477993298451eb46eb32bedad190e57fb199bee4`  
		Last Modified: Wed, 12 Apr 2023 04:41:09 GMT  
		Size: 515.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8683faa7c44d55e03f816e1db890fc7fd890c8b7b445744a3ac05c16f82ec4`  
		Last Modified: Wed, 12 Apr 2023 04:45:24 GMT  
		Size: 11.1 MB (11141781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d627bb0f0ada7387930f6852880d2f60ab065a450ddce0d0663e9b1b892e5a59`  
		Last Modified: Wed, 12 Apr 2023 04:45:22 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55dcfdab8ffb707b6125a24526687a30cb7fc22933689d654d3fd04083cac822`  
		Last Modified: Wed, 12 Apr 2023 04:45:24 GMT  
		Size: 9.9 MB (9923774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5cb76f81643def1d749f1ab1f70d7bac31a659659a41c0948fea63fce7d6c76`  
		Last Modified: Wed, 12 Apr 2023 04:45:22 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeda22061b9718cde4b9126baff4ffb5c3d8bfc84cce7df153a838929fbe5355`  
		Last Modified: Wed, 12 Apr 2023 04:45:22 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7018291d6100048d689d5dbbc8c9576509f3a6ac4702220d0622a193a84e45c9`  
		Last Modified: Wed, 12 Apr 2023 04:45:22 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4fe0a21a555576601e1d3ed994d0a3c6895665cb5c8ced21eee74fb15b991af`  
		Last Modified: Wed, 12 Apr 2023 12:07:16 GMT  
		Size: 1.9 MB (1907875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa04125de1324853eba122cc3aea6111e248400ee8f39ef4fe33c0d95639e54d`  
		Last Modified: Wed, 12 Apr 2023 12:07:16 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed41243400501ade288640a3f692c3e23aa3b7cd71f2b1c7fd6806a220373bf`  
		Last Modified: Fri, 21 Apr 2023 20:20:02 GMT  
		Size: 3.4 MB (3403526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
