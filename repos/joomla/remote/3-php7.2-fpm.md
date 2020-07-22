## `joomla:3-php7.2-fpm`

```console
$ docker pull joomla@sha256:34e00b3a4c3fac98c0adbf4976bf0b9829bf211bb3f2997b515134689b95be1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `joomla:3-php7.2-fpm` - linux; amd64

```console
$ docker pull joomla@sha256:31b57ae94211dca842cb07eba5db5753b63b2bbeba8659e8311c5d2385e5aa6f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.9 MB (157860323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60c0ea7f6bf88415092c85f5decfdc6edd57e950d4230f8e146789087104faa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 13:35:08 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 09 Jun 2020 13:35:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Jun 2020 13:35:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 13:35:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Jun 2020 13:35:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 09 Jun 2020 13:48:50 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Tue, 09 Jun 2020 13:48:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 13:48:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 13:48:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Jun 2020 15:17:18 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 10 Jul 2020 02:39:48 GMT
ENV PHP_VERSION=7.2.32
# Fri, 10 Jul 2020 02:39:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.32.tar.xz.asc
# Fri, 10 Jul 2020 02:39:48 GMT
ENV PHP_SHA256=050fc16ca56d8d2365d980998220a4eb06439da71dfd38de49b42fea72310ef1 PHP_MD5=
# Fri, 10 Jul 2020 02:39:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 10 Jul 2020 02:39:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 10 Jul 2020 02:47:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 10 Jul 2020 02:47:58 GMT
COPY multi:bd67471e0c4047be362a8a0e199558e6245207a6f70b72fdfe55aa2d2cae15e6 in /usr/local/bin/ 
# Fri, 10 Jul 2020 02:47:59 GMT
RUN docker-php-ext-enable sodium
# Fri, 10 Jul 2020 02:48:01 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 10 Jul 2020 02:48:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Jul 2020 02:48:01 GMT
WORKDIR /var/www/html
# Fri, 10 Jul 2020 02:48:03 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 10 Jul 2020 02:48:03 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Jul 2020 02:48:04 GMT
EXPOSE 9000
# Fri, 10 Jul 2020 02:48:04 GMT
CMD ["php-fpm"]
# Fri, 10 Jul 2020 05:26:34 GMT
LABEL maintainer=Michael Babker <michael.babker@joomla.org> (@mbabker)
# Fri, 10 Jul 2020 05:26:34 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 10 Jul 2020 05:28:07 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jul 2020 05:28:07 GMT
VOLUME [/var/www/html]
# Fri, 10 Jul 2020 05:28:08 GMT
ENV JOOMLA_VERSION=3.9.18
# Fri, 10 Jul 2020 05:28:08 GMT
ENV JOOMLA_SHA512=1bf4590a761cc24f59fc0d5b07ffbb8f9e50073b3536edc261b8785ff168aca2066d133a81c4ac33bcfe7b843559320ef4d1f97c5eb16096ca4b550a18b7f44d
# Fri, 10 Jul 2020 05:28:12 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Fri, 10 Jul 2020 05:28:13 GMT
COPY file:fcc18c5b9c2d514cfb965bab84e10b4f924a39a5f202055df75d7990da099d8f in /entrypoint.sh 
# Fri, 10 Jul 2020 05:28:13 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Fri, 10 Jul 2020 05:28:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Jul 2020 05:28:13 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0276193a084c10343c4ce4b455dfb8ffc8bfdf6812492ee8307475bac574514`  
		Last Modified: Tue, 09 Jun 2020 15:58:02 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2d00c10344025e5f7a6826b8e2600cd2f8b89eae906d651f34dbc931baa44c`  
		Last Modified: Tue, 09 Jun 2020 15:58:26 GMT  
		Size: 76.6 MB (76648863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54006e0dc2977f45274054d49dcbbf6494d375b13337a5724d904107e9c64da`  
		Last Modified: Tue, 09 Jun 2020 15:58:03 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162483b3eca15d47ec43e31aad3e3a4e4e88c68f0408336c405f301a1cdb0731`  
		Last Modified: Fri, 10 Jul 2020 04:31:50 GMT  
		Size: 12.6 MB (12572684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5640b2e2769aa6cf4885cb72914d45ef072fe067cf4ca93d307e8fed2034889d`  
		Last Modified: Fri, 10 Jul 2020 04:31:49 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5481b26c9742da173c4a16ebae323d2ae38fe370d27bc729709e921ce897495`  
		Last Modified: Fri, 10 Jul 2020 04:31:54 GMT  
		Size: 28.5 MB (28529439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095a3758a34d919f9b9987df678c5bba2a169cab849d2461c908556bcb8bfdb7`  
		Last Modified: Fri, 10 Jul 2020 04:31:49 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00637fcc282bfb63c2c3af27335d32a52702818de345e89d08bfd739d3fe038`  
		Last Modified: Fri, 10 Jul 2020 04:31:48 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a092f8ec74930c8009ce3e281c5ae95180979c08f393fb81958a887c3a227ad`  
		Last Modified: Fri, 10 Jul 2020 04:31:48 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b435d9a7467c34b811fbd191db7e5ffab1c6fae390447d9b09a7d3213a204f`  
		Last Modified: Fri, 10 Jul 2020 04:31:48 GMT  
		Size: 7.8 KB (7787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a94b4191d4a4f1a41edc0208b4994cbaed8bc5eab66e977fd10517e6ce88d5e`  
		Last Modified: Fri, 10 Jul 2020 05:42:17 GMT  
		Size: 3.3 MB (3344532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c4a878aa30ec5c5fac7f9db72100a45b6ef24be6a21c45a4bd293667229df1`  
		Last Modified: Fri, 10 Jul 2020 05:42:19 GMT  
		Size: 9.7 MB (9653284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad491185fa355900bbd26a9b92575eca5bdef48da2764c3e76e131a095a6a5e`  
		Last Modified: Fri, 10 Jul 2020 05:42:16 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5774ffdbe4f8abf8fa64d40ab714cb8915f15694bd8ba14b187a1b05c0c5e85`  
		Last Modified: Fri, 10 Jul 2020 05:42:16 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:3-php7.2-fpm` - linux; arm variant v5

```console
$ docker pull joomla@sha256:f572a2b85d0636b74cbef8aaf5b3172e7a15229ea48f51c0bf4136f06216192d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136176027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a57c826f1ff9d8f3619c2f4a8969cd48f0a92a7fa3d9b2eee20914d3262d73d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Jun 2020 00:51:58 GMT
ADD file:7fde417d1c70a9ef2b4e468f6e2ee4cbd3f340fb2d5b67ede087c81520c95f4a in / 
# Tue, 09 Jun 2020 00:51:59 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:10:06 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 09 Jun 2020 03:10:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Jun 2020 03:10:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:10:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Jun 2020 03:10:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 09 Jun 2020 03:19:18 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Tue, 09 Jun 2020 03:19:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 03:19:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 03:19:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Jun 2020 04:15:32 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 09 Jul 2020 23:21:55 GMT
ENV PHP_VERSION=7.2.32
# Thu, 09 Jul 2020 23:21:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.32.tar.xz.asc
# Thu, 09 Jul 2020 23:21:57 GMT
ENV PHP_SHA256=050fc16ca56d8d2365d980998220a4eb06439da71dfd38de49b42fea72310ef1 PHP_MD5=
# Thu, 09 Jul 2020 23:22:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 09 Jul 2020 23:22:39 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 09 Jul 2020 23:26:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 09 Jul 2020 23:27:01 GMT
COPY multi:bd67471e0c4047be362a8a0e199558e6245207a6f70b72fdfe55aa2d2cae15e6 in /usr/local/bin/ 
# Thu, 09 Jul 2020 23:27:04 GMT
RUN docker-php-ext-enable sodium
# Thu, 09 Jul 2020 23:27:06 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 09 Jul 2020 23:27:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Jul 2020 23:27:08 GMT
WORKDIR /var/www/html
# Thu, 09 Jul 2020 23:27:10 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 09 Jul 2020 23:27:10 GMT
STOPSIGNAL SIGQUIT
# Thu, 09 Jul 2020 23:27:11 GMT
EXPOSE 9000
# Thu, 09 Jul 2020 23:27:12 GMT
CMD ["php-fpm"]
# Fri, 10 Jul 2020 00:19:13 GMT
LABEL maintainer=Michael Babker <michael.babker@joomla.org> (@mbabker)
# Fri, 10 Jul 2020 00:19:14 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 10 Jul 2020 00:22:45 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jul 2020 00:22:46 GMT
VOLUME [/var/www/html]
# Fri, 10 Jul 2020 00:22:47 GMT
ENV JOOMLA_VERSION=3.9.18
# Fri, 10 Jul 2020 00:22:48 GMT
ENV JOOMLA_SHA512=1bf4590a761cc24f59fc0d5b07ffbb8f9e50073b3536edc261b8785ff168aca2066d133a81c4ac33bcfe7b843559320ef4d1f97c5eb16096ca4b550a18b7f44d
# Fri, 10 Jul 2020 00:23:00 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Fri, 10 Jul 2020 00:23:01 GMT
COPY file:fcc18c5b9c2d514cfb965bab84e10b4f924a39a5f202055df75d7990da099d8f in /entrypoint.sh 
# Fri, 10 Jul 2020 00:23:02 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Fri, 10 Jul 2020 00:23:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Jul 2020 00:23:04 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5b11fc09c1a26b11a7df7d593adf43baff53c5cdba71cf8a87ae4a6dd17eb52c`  
		Last Modified: Tue, 09 Jun 2020 00:59:24 GMT  
		Size: 24.8 MB (24837249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c59829855f6b9cf9ed11eac29dfab1d2404aaa7f8271e7b8094fe8fa504826`  
		Last Modified: Tue, 09 Jun 2020 04:43:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b5b6ca74676b662141f56903c72f19688a5a4371073acdce1ff972f5d2b6ab`  
		Last Modified: Tue, 09 Jun 2020 04:43:57 GMT  
		Size: 58.8 MB (58800169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2007b021f74b717a083b49fbc784030ebc6afd3f87f38f0b441253aac4a2fd`  
		Last Modified: Tue, 09 Jun 2020 04:43:35 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a809070685c4c2586cc0b2bd9628f28d796626c666364d066ce413b7ab6fb9`  
		Last Modified: Thu, 09 Jul 2020 23:58:01 GMT  
		Size: 12.6 MB (12570694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4ef6ae1efbc5b95e6a67511f9d789cb23c708aa70a992c27ac2ee288df78ec`  
		Last Modified: Thu, 09 Jul 2020 23:57:59 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fcde2fd9125767c0e345fe6add657306ff1d6f493e0d3189a044e75276a8a6b`  
		Last Modified: Thu, 09 Jul 2020 23:58:07 GMT  
		Size: 27.1 MB (27139973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a71c7055e9307545b5672e494de80ea962da98f83a6fd9afaf52eb783c4488a`  
		Last Modified: Thu, 09 Jul 2020 23:57:58 GMT  
		Size: 2.3 KB (2276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2874aed3e7fb6e04ff4e511a4119261490a1f3cec2227eec92ef48776126bc`  
		Last Modified: Thu, 09 Jul 2020 23:57:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8affb3a10c20101cfa89ceffe1e238ee3071eb40143517cc8d2a383327fea1be`  
		Last Modified: Thu, 09 Jul 2020 23:57:57 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d7397ca79c6c58bd442aa89bc698c6d32c27493920d1b10fcc753040213fc3`  
		Last Modified: Thu, 09 Jul 2020 23:57:57 GMT  
		Size: 7.8 KB (7787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db2fc0163d5d01014309b484ccc7513ecc52c7dc5c61833e7d385ccbafc82c3`  
		Last Modified: Fri, 10 Jul 2020 00:40:44 GMT  
		Size: 3.2 MB (3161359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7a00793c247d61c9011b787238efc43a73f0c170ef03dfb3b6afd3843fc3e6`  
		Last Modified: Fri, 10 Jul 2020 00:40:50 GMT  
		Size: 9.7 MB (9653282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a85eb4d4be2f7affd4008f234b58e6a4852d129343e071a00999f1cf791af6`  
		Last Modified: Fri, 10 Jul 2020 00:40:42 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6129d50d3e01af74f352aa363a07a36cfc5b48512a76cec796e0e16a4866f345`  
		Last Modified: Fri, 10 Jul 2020 00:40:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:3-php7.2-fpm` - linux; arm variant v7

```console
$ docker pull joomla@sha256:3c62ca99546d3bddb0afbc297b4a022dbd5cc216a7810581b07e2cebcab5d9a7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133644404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7ef4e4164957889227f05f2ae3dcc032a633798b41074e5f149212f2d98039`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Jun 2020 01:01:24 GMT
ADD file:a35ca31d2a743d6a1738b1652f4f06c789abbca314d120f0e7e748311ac09ed2 in / 
# Tue, 09 Jun 2020 01:01:30 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 09:38:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 09 Jun 2020 09:38:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Jun 2020 09:39:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 09:39:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Jun 2020 09:39:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 09 Jun 2020 09:47:14 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Tue, 09 Jun 2020 09:47:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 09:47:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 09:47:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Jun 2020 10:41:47 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 10 Jul 2020 00:08:05 GMT
ENV PHP_VERSION=7.2.32
# Fri, 10 Jul 2020 00:08:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.32.tar.xz.asc
# Fri, 10 Jul 2020 00:08:07 GMT
ENV PHP_SHA256=050fc16ca56d8d2365d980998220a4eb06439da71dfd38de49b42fea72310ef1 PHP_MD5=
# Fri, 10 Jul 2020 00:08:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 10 Jul 2020 00:08:29 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 10 Jul 2020 00:11:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 10 Jul 2020 00:11:55 GMT
COPY multi:bd67471e0c4047be362a8a0e199558e6245207a6f70b72fdfe55aa2d2cae15e6 in /usr/local/bin/ 
# Fri, 10 Jul 2020 00:11:57 GMT
RUN docker-php-ext-enable sodium
# Fri, 10 Jul 2020 00:11:59 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 10 Jul 2020 00:12:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Jul 2020 00:12:01 GMT
WORKDIR /var/www/html
# Fri, 10 Jul 2020 00:12:04 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 10 Jul 2020 00:12:05 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Jul 2020 00:12:06 GMT
EXPOSE 9000
# Fri, 10 Jul 2020 00:12:08 GMT
CMD ["php-fpm"]
# Fri, 10 Jul 2020 02:11:16 GMT
LABEL maintainer=Michael Babker <michael.babker@joomla.org> (@mbabker)
# Fri, 10 Jul 2020 02:11:17 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 10 Jul 2020 02:13:50 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jul 2020 02:13:52 GMT
VOLUME [/var/www/html]
# Fri, 10 Jul 2020 02:13:52 GMT
ENV JOOMLA_VERSION=3.9.18
# Fri, 10 Jul 2020 02:13:54 GMT
ENV JOOMLA_SHA512=1bf4590a761cc24f59fc0d5b07ffbb8f9e50073b3536edc261b8785ff168aca2066d133a81c4ac33bcfe7b843559320ef4d1f97c5eb16096ca4b550a18b7f44d
# Fri, 10 Jul 2020 02:14:04 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Fri, 10 Jul 2020 02:14:06 GMT
COPY file:fcc18c5b9c2d514cfb965bab84e10b4f924a39a5f202055df75d7990da099d8f in /entrypoint.sh 
# Fri, 10 Jul 2020 02:14:07 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Fri, 10 Jul 2020 02:14:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Jul 2020 02:14:09 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2dd003996c9ab82cac8112be0a4c04068e666e7a5d0cce3c65fb8f064de284e7`  
		Last Modified: Tue, 09 Jun 2020 01:10:25 GMT  
		Size: 22.7 MB (22705913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a06dc047a60bc8c7f6dd7236a59edd0ac74556e9f9a4375cd2d64e1b5ef56dd`  
		Last Modified: Tue, 09 Jun 2020 11:11:27 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8445ea067b9b6c8bbaff4521c1fcd1b8e9cbcf970e9144d4d3d4ec2a419b83ea`  
		Last Modified: Tue, 09 Jun 2020 11:11:45 GMT  
		Size: 59.5 MB (59505705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3427b10e03731502c05abd929b3f5877453d9bd99926d1c7fd6454d036781a0`  
		Last Modified: Tue, 09 Jun 2020 11:11:26 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435672d047a20a2ae7d3037aa33c6875546631e85a3a3af64d93ba1341cda418`  
		Last Modified: Fri, 10 Jul 2020 01:13:07 GMT  
		Size: 12.6 MB (12570629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bd7d173f2b859a97bd41672a47e3e2fc6bbbc0809e36bc898dc86ea20d5ba3`  
		Last Modified: Fri, 10 Jul 2020 01:13:01 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d736e84cd3734f3cb4e5b5bf72329d8e287ba62dd2582a8dea690dcd3186f3d8`  
		Last Modified: Fri, 10 Jul 2020 01:13:03 GMT  
		Size: 26.1 MB (26117250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd0e34b3244f61f4d5ac80e4136418714808897389fadc2989548e840a73e2cd`  
		Last Modified: Fri, 10 Jul 2020 01:12:55 GMT  
		Size: 2.3 KB (2275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14a645532ba065a83d78b06b539acab3c87939b42ac2ebef94f1271e84c74c9`  
		Last Modified: Fri, 10 Jul 2020 01:12:55 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bbd41a33d7e94071716ad73d31ea1524778119607d110821f5ae23b31664518`  
		Last Modified: Fri, 10 Jul 2020 01:12:55 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2cc65b3b67904fc68e5eb7b2d351afff091b3a4fd08b871e9f6c104bad425c7`  
		Last Modified: Fri, 10 Jul 2020 01:12:55 GMT  
		Size: 7.8 KB (7787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c73ace11b8bebb8f36bf6d7d7b81f7ead1df7895be3f05fe37deaef1481bbac4`  
		Last Modified: Fri, 10 Jul 2020 02:41:02 GMT  
		Size: 3.1 MB (3078317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970f26388505bf815250d5c15d35c0ab1abdf04e329be781520bf93ce3a3f6a3`  
		Last Modified: Fri, 10 Jul 2020 02:41:07 GMT  
		Size: 9.7 MB (9653289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df987d852b7db446550f799b47c392d13a9e273e0adc5b70de61530ceca1558`  
		Last Modified: Fri, 10 Jul 2020 02:41:01 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc57a3d05ca154abdac9435e216c139f37c38b40763cba82b91498a58e7944b3`  
		Last Modified: Fri, 10 Jul 2020 02:41:01 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:3-php7.2-fpm` - linux; arm64 variant v8

```console
$ docker pull joomla@sha256:ab5c94cd00a47252d7c4df9b9e140cab54bb36e85da610096db2b78f0503db0f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149929430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce1a2eeb31495734decaab9b4f0d076af5142e163ec87104952117050ffe8f4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 10:22:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 09 Jun 2020 10:22:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Jun 2020 10:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 10:23:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Jun 2020 10:23:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 09 Jun 2020 10:33:01 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Tue, 09 Jun 2020 10:33:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 10:33:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 10:33:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Jun 2020 11:29:41 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 10 Jul 2020 01:09:58 GMT
ENV PHP_VERSION=7.2.32
# Fri, 10 Jul 2020 01:09:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.32.tar.xz.asc
# Fri, 10 Jul 2020 01:10:02 GMT
ENV PHP_SHA256=050fc16ca56d8d2365d980998220a4eb06439da71dfd38de49b42fea72310ef1 PHP_MD5=
# Fri, 10 Jul 2020 01:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 10 Jul 2020 01:10:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 10 Jul 2020 01:14:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 10 Jul 2020 01:14:28 GMT
COPY multi:bd67471e0c4047be362a8a0e199558e6245207a6f70b72fdfe55aa2d2cae15e6 in /usr/local/bin/ 
# Fri, 10 Jul 2020 01:14:30 GMT
RUN docker-php-ext-enable sodium
# Fri, 10 Jul 2020 01:14:32 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 10 Jul 2020 01:14:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Jul 2020 01:14:34 GMT
WORKDIR /var/www/html
# Fri, 10 Jul 2020 01:14:36 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 10 Jul 2020 01:14:38 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Jul 2020 01:14:39 GMT
EXPOSE 9000
# Fri, 10 Jul 2020 01:14:40 GMT
CMD ["php-fpm"]
# Fri, 10 Jul 2020 02:59:46 GMT
LABEL maintainer=Michael Babker <michael.babker@joomla.org> (@mbabker)
# Fri, 10 Jul 2020 02:59:47 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 10 Jul 2020 03:02:34 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jul 2020 03:02:35 GMT
VOLUME [/var/www/html]
# Fri, 10 Jul 2020 03:02:36 GMT
ENV JOOMLA_VERSION=3.9.18
# Fri, 10 Jul 2020 03:02:37 GMT
ENV JOOMLA_SHA512=1bf4590a761cc24f59fc0d5b07ffbb8f9e50073b3536edc261b8785ff168aca2066d133a81c4ac33bcfe7b843559320ef4d1f97c5eb16096ca4b550a18b7f44d
# Fri, 10 Jul 2020 03:02:47 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Fri, 10 Jul 2020 03:02:49 GMT
COPY file:fcc18c5b9c2d514cfb965bab84e10b4f924a39a5f202055df75d7990da099d8f in /entrypoint.sh 
# Fri, 10 Jul 2020 03:02:49 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Fri, 10 Jul 2020 03:02:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Jul 2020 03:02:51 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e42a0c192db5b0cb97d83007911b8069b7120ef4d150564a32e9ec94753ca03`  
		Last Modified: Tue, 09 Jun 2020 11:57:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b23edfc2b677695687c477af83edbcfb24140f7186ed405faef4d5947c0a0c9`  
		Last Modified: Tue, 09 Jun 2020 11:57:42 GMT  
		Size: 70.3 MB (70337397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22952435701f91bcb4b63b22ba1c37c84d3a2c0d2f3c98109e18618040b7bb32`  
		Last Modified: Tue, 09 Jun 2020 11:57:21 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed525e0b90ff62f5a53f098de34c169f0a10d0ac9ce7dd20b3a1506434e3aa8`  
		Last Modified: Fri, 10 Jul 2020 02:12:21 GMT  
		Size: 12.6 MB (12571500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b9fcf53ea2ae40561ab1538fde1b4896534c3103976fe24fe5e38c702e5f8c`  
		Last Modified: Fri, 10 Jul 2020 02:12:19 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435fcdb929076b0dcdf738661b32cfaf976ce96ee6586ef3a8929f444884d6eb`  
		Last Modified: Fri, 10 Jul 2020 02:12:26 GMT  
		Size: 28.2 MB (28205715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fc8e2b440b97840f2f6016ece0ace3f83bb5480d8e6cb0bffd7b6a56f168f43`  
		Last Modified: Fri, 10 Jul 2020 02:12:18 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b22b89bc8c673f7ad3b49d6710d0080d879db1bebd2cd65f04446e7cd00021a`  
		Last Modified: Fri, 10 Jul 2020 02:12:18 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a222ead1237713530d1d75a6e8271d0efcf269fe3e47cfad1b73f6f4cfab9709`  
		Last Modified: Fri, 10 Jul 2020 02:12:18 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:831d88434d04de4d62f4516d37b59520ba448a2b1b62507bb0a34d9259a2a4bd`  
		Last Modified: Fri, 10 Jul 2020 02:12:18 GMT  
		Size: 7.8 KB (7786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70a8229278e376c48f07565250434f49b40ab82a55ea93ad9793d0e7e3844d7`  
		Last Modified: Fri, 10 Jul 2020 03:27:13 GMT  
		Size: 3.3 MB (3290518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:714916d4508865a4c97637691b86b721caacc4062d62bea3af872443f21b3431`  
		Last Modified: Fri, 10 Jul 2020 03:27:16 GMT  
		Size: 9.7 MB (9653291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37baa8f4b6d79b46af9e70fb7c5e80f15ff00fd0337ebd07c05b4ed15d688ee5`  
		Last Modified: Fri, 10 Jul 2020 03:27:12 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc19002d8e45f8615eb7e0534ea7f8866d8d2fbde0f944952aa4ff90596e646`  
		Last Modified: Fri, 10 Jul 2020 03:27:12 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:3-php7.2-fpm` - linux; 386

```console
$ docker pull joomla@sha256:f77a390b49edb6f3a03e7f4af12f2fb36968362623f5a7a5dbb31cbe9f1d5291
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163585202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a0f47fd6ed99750236bc8ca28d0d3b556c40e4ffb3b09843fdf9c2a6d39deb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Jun 2020 01:39:49 GMT
ADD file:9fb8fd8bf970c4134f555964fe485a3baa84f1d4c91c5aa35276c24404de9d5d in / 
# Tue, 09 Jun 2020 01:39:49 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:29:01 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 09 Jun 2020 07:29:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Jun 2020 07:29:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:29:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Jun 2020 07:29:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 09 Jun 2020 07:40:40 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Tue, 09 Jun 2020 07:40:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 07:40:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 07:40:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Jun 2020 09:06:01 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 10 Jul 2020 03:25:54 GMT
ENV PHP_VERSION=7.2.32
# Fri, 10 Jul 2020 03:25:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.32.tar.xz.asc
# Fri, 10 Jul 2020 03:25:54 GMT
ENV PHP_SHA256=050fc16ca56d8d2365d980998220a4eb06439da71dfd38de49b42fea72310ef1 PHP_MD5=
# Fri, 10 Jul 2020 03:26:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 10 Jul 2020 03:26:05 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 10 Jul 2020 03:35:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 10 Jul 2020 03:35:05 GMT
COPY multi:bd67471e0c4047be362a8a0e199558e6245207a6f70b72fdfe55aa2d2cae15e6 in /usr/local/bin/ 
# Fri, 10 Jul 2020 03:35:06 GMT
RUN docker-php-ext-enable sodium
# Fri, 10 Jul 2020 03:35:06 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 10 Jul 2020 03:35:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Jul 2020 03:35:07 GMT
WORKDIR /var/www/html
# Fri, 10 Jul 2020 03:35:08 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 10 Jul 2020 03:35:08 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Jul 2020 03:35:08 GMT
EXPOSE 9000
# Fri, 10 Jul 2020 03:35:08 GMT
CMD ["php-fpm"]
# Fri, 10 Jul 2020 05:45:29 GMT
LABEL maintainer=Michael Babker <michael.babker@joomla.org> (@mbabker)
# Fri, 10 Jul 2020 05:45:29 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 10 Jul 2020 05:47:29 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jul 2020 05:47:30 GMT
VOLUME [/var/www/html]
# Fri, 10 Jul 2020 05:47:30 GMT
ENV JOOMLA_VERSION=3.9.18
# Fri, 10 Jul 2020 05:47:30 GMT
ENV JOOMLA_SHA512=1bf4590a761cc24f59fc0d5b07ffbb8f9e50073b3536edc261b8785ff168aca2066d133a81c4ac33bcfe7b843559320ef4d1f97c5eb16096ca4b550a18b7f44d
# Fri, 10 Jul 2020 05:47:38 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Fri, 10 Jul 2020 05:47:39 GMT
COPY file:fcc18c5b9c2d514cfb965bab84e10b4f924a39a5f202055df75d7990da099d8f in /entrypoint.sh 
# Fri, 10 Jul 2020 05:47:40 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Fri, 10 Jul 2020 05:47:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Jul 2020 05:47:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:860f8957d8be856e2235a28e49fc4dca17254951e0eb67d760769755656f5cad`  
		Last Modified: Tue, 09 Jun 2020 01:45:01 GMT  
		Size: 27.8 MB (27754909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e56aaa35138d917890d6385d97e3551b2c7f733e0ffb4190f8ab0926d45535d`  
		Last Modified: Tue, 09 Jun 2020 09:59:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cde5a58e2a1076acb6f13762ae3b1f732448e2f9fdef2e266ca694f8699139`  
		Last Modified: Tue, 09 Jun 2020 10:00:10 GMT  
		Size: 81.2 MB (81195220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b360659c28c29c8e5663391e3f169aee77802ea8c4fdc2aa8d23201818fcaae`  
		Last Modified: Tue, 09 Jun 2020 09:59:33 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42dd20bab2e9ce885354052804da04c505b11b1b58ffe359bb7a041ba82231a4`  
		Last Modified: Fri, 10 Jul 2020 05:12:00 GMT  
		Size: 12.6 MB (12571926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e983c6421d85008348407df231b129a7f4d8a5618be04d936be68d14125694`  
		Last Modified: Fri, 10 Jul 2020 05:12:00 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63458308c44f13dc8407931826663321e2fff1ae355fe6fcffd3fdb3dde2d9ea`  
		Last Modified: Fri, 10 Jul 2020 05:12:06 GMT  
		Size: 29.1 MB (29082383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdfe6c6b9cff5ca0c4fafe52b2ce1b5d515146f8f0e2b3a4ab4774c0e04e2ef`  
		Last Modified: Fri, 10 Jul 2020 05:11:58 GMT  
		Size: 2.3 KB (2275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4cd27f669db771510d3a8ec3ddb4ada45048952e3199fa55d1892d5c93fdb7f`  
		Last Modified: Fri, 10 Jul 2020 05:11:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db20357ac86e6638e5c95526aa8a979f86a3d6008eff3f7895cd6e2d39ef8e9`  
		Last Modified: Fri, 10 Jul 2020 05:11:58 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92219e1db46bdf17cae981e0a13437f8ee677df9efcb38e656e9955bce657ffd`  
		Last Modified: Fri, 10 Jul 2020 05:11:58 GMT  
		Size: 7.8 KB (7785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14129d0beaa224eb2d9d92ab17372ff5e2f840f0c1ea8347ab3ccd7e44201c4a`  
		Last Modified: Fri, 10 Jul 2020 06:03:38 GMT  
		Size: 3.3 MB (3314234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b996161746ae0bc5b155bbd5f76f3facd8fb12a23a1b1ea6b604e0e02ff72936`  
		Last Modified: Fri, 10 Jul 2020 06:03:42 GMT  
		Size: 9.7 MB (9653286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c0bd8beb8852c132165032b0fd903ec194db3585fa137fe4215eaa63c6890a`  
		Last Modified: Fri, 10 Jul 2020 06:03:37 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1a7227b5b8479dcd4cb5b3b5c873ca1a603d947099894ea02c75f391438a5e`  
		Last Modified: Fri, 10 Jul 2020 06:03:37 GMT  
		Size: 609.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:3-php7.2-fpm` - linux; ppc64le

```console
$ docker pull joomla@sha256:b599f7d7da2de73da0d379bd8a827fdd28026fc5fe570bcd950458d3b3a32e4f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.8 MB (168756094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3da709dfa7399064cb0d1d44dade09a2780550913ce938f2938670e7368d8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Jun 2020 01:22:34 GMT
ADD file:796aad1a35ba276b8cccc19987c152a713db101b2b65e30923db753f5b7f4b0f in / 
# Tue, 09 Jun 2020 01:22:38 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 05:09:08 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 09 Jun 2020 05:09:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Jun 2020 05:11:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 05:11:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Jun 2020 05:11:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 09 Jun 2020 05:26:55 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Tue, 09 Jun 2020 05:27:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 05:27:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 05:27:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Jun 2020 07:38:08 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 10 Jul 2020 02:18:29 GMT
ENV PHP_VERSION=7.2.32
# Fri, 10 Jul 2020 02:18:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.32.tar.xz.asc
# Fri, 10 Jul 2020 02:18:38 GMT
ENV PHP_SHA256=050fc16ca56d8d2365d980998220a4eb06439da71dfd38de49b42fea72310ef1 PHP_MD5=
# Fri, 10 Jul 2020 02:20:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 10 Jul 2020 02:20:05 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 10 Jul 2020 02:26:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 10 Jul 2020 02:26:14 GMT
COPY multi:bd67471e0c4047be362a8a0e199558e6245207a6f70b72fdfe55aa2d2cae15e6 in /usr/local/bin/ 
# Fri, 10 Jul 2020 02:26:23 GMT
RUN docker-php-ext-enable sodium
# Fri, 10 Jul 2020 02:26:30 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 10 Jul 2020 02:26:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Jul 2020 02:26:36 GMT
WORKDIR /var/www/html
# Fri, 10 Jul 2020 02:26:44 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 10 Jul 2020 02:26:47 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Jul 2020 02:26:51 GMT
EXPOSE 9000
# Fri, 10 Jul 2020 02:26:55 GMT
CMD ["php-fpm"]
# Fri, 10 Jul 2020 04:48:15 GMT
LABEL maintainer=Michael Babker <michael.babker@joomla.org> (@mbabker)
# Fri, 10 Jul 2020 04:48:17 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 10 Jul 2020 04:50:49 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jul 2020 04:50:51 GMT
VOLUME [/var/www/html]
# Fri, 10 Jul 2020 04:50:54 GMT
ENV JOOMLA_VERSION=3.9.18
# Fri, 10 Jul 2020 04:50:57 GMT
ENV JOOMLA_SHA512=1bf4590a761cc24f59fc0d5b07ffbb8f9e50073b3536edc261b8785ff168aca2066d133a81c4ac33bcfe7b843559320ef4d1f97c5eb16096ca4b550a18b7f44d
# Fri, 10 Jul 2020 04:51:10 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Fri, 10 Jul 2020 04:51:13 GMT
COPY file:fcc18c5b9c2d514cfb965bab84e10b4f924a39a5f202055df75d7990da099d8f in /entrypoint.sh 
# Fri, 10 Jul 2020 04:51:15 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Fri, 10 Jul 2020 04:51:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Jul 2020 04:51:21 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:63dbb66c5119bb5086d9e6fb6b154211afc20b44ed136ab7df808f6044cfc6f1`  
		Last Modified: Tue, 09 Jun 2020 01:31:04 GMT  
		Size: 30.5 MB (30524405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad44f0796ea364793d3ac145c002c7ed180fe56cd09eed97a971a2e20999794`  
		Last Modified: Tue, 09 Jun 2020 08:55:13 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501de6851c5eeb5b1bd75588fa67abb74d85b869f36d4815f1e4ae4e007fc4f1`  
		Last Modified: Tue, 09 Jun 2020 08:56:28 GMT  
		Size: 82.3 MB (82262725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4824564d8a89ca8405d5fcf32fb84ff63852689cf385a5bcffa8023a86fa4a69`  
		Last Modified: Tue, 09 Jun 2020 08:55:10 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccc2da9523219c3d5e0b05d8060fa546c03a280497f8f5b17efaae9929d70f0`  
		Last Modified: Fri, 10 Jul 2020 03:33:08 GMT  
		Size: 12.6 MB (12572531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7765b06189c08f5b3fc63db57ccd27c8e37709ce2d8762a17c57e4be9d375e7e`  
		Last Modified: Fri, 10 Jul 2020 03:33:04 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7526371a86c419b54f45527618fb8ea4474659ee86d83a0e798848fffe48b1`  
		Last Modified: Fri, 10 Jul 2020 03:33:06 GMT  
		Size: 30.2 MB (30215647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353e15a6986407cf688ab5c86d10610035d70ce115be8771fe4fc852290eb5b2`  
		Last Modified: Fri, 10 Jul 2020 03:33:00 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf891b5d2bb1fcd87cc18e13d9b591eac77b242537755c0d2e16a04bf5aa25f`  
		Last Modified: Fri, 10 Jul 2020 03:33:00 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:361f8b2121bcf49174e7cfc04a0b6f5e2dbb46d2cef118efe705772a4843d891`  
		Last Modified: Fri, 10 Jul 2020 03:33:00 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b4f4847d9fbe187c979fe3ac6bcab4d48bbbec88ce6b9919b8b69a954be085`  
		Last Modified: Fri, 10 Jul 2020 03:33:00 GMT  
		Size: 7.8 KB (7787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f33aab4ee6bb1375261ec7e2c093f9681e2099b8aa5a7bb697c45a579d787fa`  
		Last Modified: Fri, 10 Jul 2020 05:17:10 GMT  
		Size: 3.5 MB (3514185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e732159f2f047886efd85646d9bcab54a947398becf53508e259bba4b0f0616`  
		Last Modified: Fri, 10 Jul 2020 05:17:27 GMT  
		Size: 9.7 MB (9653295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b9068ebf42da17fa15558b32542db5d19c799937d5ba6d6bab4ea3872743c2`  
		Last Modified: Fri, 10 Jul 2020 05:17:03 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28868ba7f708662c722fb9f21b854015ec7a2341104de1d30cc1887e7c69efaa`  
		Last Modified: Fri, 10 Jul 2020 05:17:03 GMT  
		Size: 613.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:3-php7.2-fpm` - linux; s390x

```console
$ docker pull joomla@sha256:5bc2ec6e2e268afe576dfa2e6b06adcba65252635ee93f39c0043b4b98450b18
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143651452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5c99f35b2828374214deb108c40d69efc2cbc2bc1443b6f981024893077838`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 Jul 2020 00:42:41 GMT
ADD file:2864b647009a85c176c3aeb2d75843b9336b02a18412124b8a03710df61dc971 in / 
# Wed, 22 Jul 2020 00:42:43 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:22:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 22 Jul 2020 01:22:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Jul 2020 01:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:22:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Jul 2020 01:22:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 22 Jul 2020 01:26:56 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Wed, 22 Jul 2020 01:26:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Jul 2020 01:26:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Jul 2020 01:26:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Jul 2020 02:05:51 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Wed, 22 Jul 2020 02:05:51 GMT
ENV PHP_VERSION=7.2.32
# Wed, 22 Jul 2020 02:05:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.32.tar.xz.asc
# Wed, 22 Jul 2020 02:05:51 GMT
ENV PHP_SHA256=050fc16ca56d8d2365d980998220a4eb06439da71dfd38de49b42fea72310ef1 PHP_MD5=
# Wed, 22 Jul 2020 02:05:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 22 Jul 2020 02:05:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 Jul 2020 02:08:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Wed, 22 Jul 2020 02:08:07 GMT
COPY multi:bd67471e0c4047be362a8a0e199558e6245207a6f70b72fdfe55aa2d2cae15e6 in /usr/local/bin/ 
# Wed, 22 Jul 2020 02:08:08 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 Jul 2020 02:08:08 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Wed, 22 Jul 2020 02:08:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Jul 2020 02:08:09 GMT
WORKDIR /var/www/html
# Wed, 22 Jul 2020 02:08:09 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Wed, 22 Jul 2020 02:08:10 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Jul 2020 02:08:10 GMT
EXPOSE 9000
# Wed, 22 Jul 2020 02:08:10 GMT
CMD ["php-fpm"]
# Wed, 22 Jul 2020 09:15:55 GMT
LABEL maintainer=Michael Babker <michael.babker@joomla.org> (@mbabker)
# Wed, 22 Jul 2020 09:15:55 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 22 Jul 2020 09:17:10 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 09:17:11 GMT
VOLUME [/var/www/html]
# Wed, 22 Jul 2020 09:17:11 GMT
ENV JOOMLA_VERSION=3.9.18
# Wed, 22 Jul 2020 09:17:11 GMT
ENV JOOMLA_SHA512=1bf4590a761cc24f59fc0d5b07ffbb8f9e50073b3536edc261b8785ff168aca2066d133a81c4ac33bcfe7b843559320ef4d1f97c5eb16096ca4b550a18b7f44d
# Wed, 22 Jul 2020 09:17:21 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Wed, 22 Jul 2020 09:17:22 GMT
COPY file:fcc18c5b9c2d514cfb965bab84e10b4f924a39a5f202055df75d7990da099d8f in /entrypoint.sh 
# Wed, 22 Jul 2020 09:17:23 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Wed, 22 Jul 2020 09:17:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jul 2020 09:17:23 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:71104c8b0e24cdcb6152cf3a5afb2944f578c741e6defa1905768c590598a79a`  
		Last Modified: Wed, 22 Jul 2020 00:45:48 GMT  
		Size: 25.7 MB (25712820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ecc131263818db5f20aed7935f4291b9e58c37ce83bdebcac487792acd41ebd`  
		Last Modified: Wed, 22 Jul 2020 02:21:56 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a521bafb5af984b78fd960dfc41a141df9b4a287161769db0b06918ae7b2bf0c`  
		Last Modified: Wed, 22 Jul 2020 02:22:05 GMT  
		Size: 64.7 MB (64697792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e65d722eeb3c0a8076e675ef7a082b4ce3b64802d43adbfa2957039e02882a`  
		Last Modified: Wed, 22 Jul 2020 02:21:55 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e45ee31ba27d6126824b6073b6a680d6d9e982a521ae8e6e2e253c7e82a6db6`  
		Last Modified: Wed, 22 Jul 2020 02:28:22 GMT  
		Size: 12.6 MB (12570823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dfa3a2f3f34b1157fa4e7e99323ab4051e2f9081003f7878b7b63dc4048d2bb`  
		Last Modified: Wed, 22 Jul 2020 02:28:18 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486c09710a84f1cd07f391b106b087e83044a86692adcebf8580d66074824e3e`  
		Last Modified: Wed, 22 Jul 2020 02:28:22 GMT  
		Size: 27.7 MB (27702097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fdfef32c02a7318edd92844eff411b852a981b827cdf99caf74b1567bc20fcc`  
		Last Modified: Wed, 22 Jul 2020 02:28:22 GMT  
		Size: 2.3 KB (2274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0368cbbc7e3de0b7e0a691aa15a46986a464e1367f2aa9609119fda0e6e1e9`  
		Last Modified: Wed, 22 Jul 2020 02:28:17 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77bad066f69989ebd35c1c3fdac853e95e0e8ba7cd5062e32c33b9821136e919`  
		Last Modified: Wed, 22 Jul 2020 02:28:22 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41aff6bd1735fcb56fd222eecba03e3cd857f0ecf25d595312bf58ed6c614507`  
		Last Modified: Wed, 22 Jul 2020 02:28:22 GMT  
		Size: 7.8 KB (7786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c373c35e87f6a6981800b071313643554f84ee3fda2224fe7e2976b3155885cf`  
		Last Modified: Wed, 22 Jul 2020 09:25:46 GMT  
		Size: 3.3 MB (3301355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1878d873cae0dff65fffbb17221fdbf5776787ac23723a8e155e7a363ad56a8`  
		Last Modified: Wed, 22 Jul 2020 09:25:47 GMT  
		Size: 9.7 MB (9653279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa0878f36ab875ecc857bd31026c9836194fc245d7fff2e8abd7a3345dd8115`  
		Last Modified: Wed, 22 Jul 2020 09:25:51 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af688c3de0ac0e0aab8eef28f955af2e368d8c91bb7530044b913e6d9fcdd0cc`  
		Last Modified: Wed, 22 Jul 2020 09:25:50 GMT  
		Size: 610.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
