## `nextcloud:production-fpm`

```console
$ docker pull nextcloud@sha256:babe93de0237aa162700163fdbd211ef958ef05ebb070f77c25afd1024130266
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

### `nextcloud:production-fpm` - linux; amd64

```console
$ docker pull nextcloud@sha256:8704ed25046c3dcd6fed860a45395e1dd27221b50d82315ae4a15b56e1d5934f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.4 MB (314401365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764d70d3598951d9eaba39dca798bed999c2c0254f1ad6eb6948cfbd9fc5b472`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 12:15:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 17 Aug 2021 12:15:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 17 Aug 2021 12:15:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 12:15:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 17 Aug 2021 12:15:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 17 Aug 2021 12:28:58 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Tue, 17 Aug 2021 12:28:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Aug 2021 12:28:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Aug 2021 12:28:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 17 Aug 2021 13:10:03 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 27 Aug 2021 00:02:57 GMT
ENV PHP_VERSION=7.4.23
# Fri, 27 Aug 2021 00:02:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.23.tar.xz.asc
# Fri, 27 Aug 2021 00:02:58 GMT
ENV PHP_SHA256=cea52313fcffe56343bcd3c66dbb23cd5507dc559cc2e3547cf8f5452e88a05d
# Fri, 27 Aug 2021 00:03:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 27 Aug 2021 00:03:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Aug 2021 00:09:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Aug 2021 00:09:39 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 27 Aug 2021 00:09:40 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Aug 2021 00:09:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Aug 2021 00:09:41 GMT
WORKDIR /var/www/html
# Fri, 27 Aug 2021 00:09:42 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 27 Aug 2021 00:09:42 GMT
STOPSIGNAL SIGQUIT
# Fri, 27 Aug 2021 00:09:42 GMT
EXPOSE 9000
# Fri, 27 Aug 2021 00:09:43 GMT
CMD ["php-fpm"]
# Fri, 27 Aug 2021 06:11:04 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         busybox-static     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 27 Aug 2021 06:11:04 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 27 Aug 2021 06:11:05 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 27 Aug 2021 06:13:56 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libxml2-dev         libmagickwand-dev         libzip-dev         libwebp-dev         libgmp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.20;     pecl install memcached-3.1.5;     pecl install redis-5.3.4;     pecl install imagick-3.5.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Aug 2021 06:13:57 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/nextcloud.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 27 Aug 2021 06:13:57 GMT
VOLUME [/var/www/html]
# Fri, 27 Aug 2021 06:19:49 GMT
ENV NEXTCLOUD_VERSION=21.0.4
# Fri, 27 Aug 2021 06:20:39 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Aug 2021 06:20:40 GMT
COPY multi:5c7d3e21c40c6f3326b9c24bb148355014771883d3bc821f8ada4fed6795cbb4 in / 
# Fri, 27 Aug 2021 06:20:41 GMT
COPY multi:d1870de3d4b4de5680360a8bcad7129a7c7615ba76daad773ab1eee24d4a949f in /usr/src/nextcloud/config/ 
# Fri, 27 Aug 2021 06:20:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 27 Aug 2021 06:20:42 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4909824c2d9e8528562a0eeab6573b4553f598555dd0a29f6f3fb2c28f6e4f2`  
		Last Modified: Tue, 17 Aug 2021 14:14:31 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d250e5f539524d16c1024cbbc0ba50cbde53f2ffce91a99088af37712f9e89`  
		Last Modified: Tue, 17 Aug 2021 14:14:48 GMT  
		Size: 76.7 MB (76680781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8ea4156ce7c000260f63ef26989a499cb20b8aea4f2d8a4cd0da0e79903b07`  
		Last Modified: Tue, 17 Aug 2021 14:14:30 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca750c14f6ab0cd213d4664e7ea86d1b56793be6590d1949b2b6d71d652948d7`  
		Last Modified: Fri, 27 Aug 2021 03:25:38 GMT  
		Size: 10.7 MB (10692373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c09beb5d4ed1ea2d61f59fa73a870981fe635947a53e7f7870ed6d34072abe`  
		Last Modified: Fri, 27 Aug 2021 03:25:35 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3b41a311ec12bf8a4ea012944e6f2fbc1b94d1a84cd2c41d180a723ae3f75f`  
		Last Modified: Fri, 27 Aug 2021 03:25:40 GMT  
		Size: 31.2 MB (31198460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbcef5c36f0b9f549ca46f6626273bffc5d68978699700704916c7fba97e1aa2`  
		Last Modified: Fri, 27 Aug 2021 03:25:35 GMT  
		Size: 2.3 KB (2271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9832f030fd94296c659c851f510d5be0ec3baf969de1b40515db4c8a22acaf2`  
		Last Modified: Fri, 27 Aug 2021 03:25:35 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c2472ce622f9e475842df67e7b87ab8ee507e883f3e3a77d6965f07994f224`  
		Last Modified: Fri, 27 Aug 2021 03:25:35 GMT  
		Size: 8.4 KB (8449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dccb659c49c4cdc94965c4fc785653ea009e532d8b0966efc8c315d608cf17c`  
		Last Modified: Fri, 27 Aug 2021 06:26:29 GMT  
		Size: 1.6 MB (1641006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47c20c0559982446e8dff1ad3018edc13add65fd8418ceed14715c542914a2d`  
		Last Modified: Fri, 27 Aug 2021 06:26:29 GMT  
		Size: 15.9 MB (15892350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002418c3ee3b3fb90f1929480e4b915e2883a03672e93a83a187e2dceae765a9`  
		Last Modified: Fri, 27 Aug 2021 06:26:26 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c3848f4f90a6fbc0d203bc39d656a229aea6affdd1093509d2c408edb7ffd0`  
		Last Modified: Fri, 27 Aug 2021 06:29:02 GMT  
		Size: 151.1 MB (151133176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910108b14f89f9b024ce4a6e44faf53c08cd8b7b8306af8b3bed686f19c99d26`  
		Last Modified: Fri, 27 Aug 2021 06:28:40 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd75c49729ebb748b133e20054c95f178de0fbac50c4eb2f258b639ab832037`  
		Last Modified: Fri, 27 Aug 2021 06:28:40 GMT  
		Size: 2.1 KB (2051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production-fpm` - linux; arm variant v5

```console
$ docker pull nextcloud@sha256:1f0a7cb001f39d3d68829134e74f2a7f92d2239b92a948f0f24ca06e20516381
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.2 MB (291152585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef754349affe9bca3027aaf50977e8f16fc239111c5cf9b15bee20220303a75f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 17 Aug 2021 01:56:50 GMT
ADD file:f29260935f1f8b3eef5eb0d5e49dd4cf5370e8731a3f4006d6023724bce09601 in / 
# Tue, 17 Aug 2021 01:56:51 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:50:04 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 17 Aug 2021 09:50:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 17 Aug 2021 09:50:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:50:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 17 Aug 2021 09:50:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 17 Aug 2021 10:03:15 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Tue, 17 Aug 2021 10:03:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Aug 2021 10:03:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Aug 2021 10:03:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 17 Aug 2021 10:46:58 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Aug 2021 21:37:18 GMT
ENV PHP_VERSION=7.4.23
# Thu, 26 Aug 2021 21:37:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.23.tar.xz.asc
# Thu, 26 Aug 2021 21:37:19 GMT
ENV PHP_SHA256=cea52313fcffe56343bcd3c66dbb23cd5507dc559cc2e3547cf8f5452e88a05d
# Thu, 26 Aug 2021 21:37:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 26 Aug 2021 21:37:48 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Aug 2021 21:43:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 26 Aug 2021 21:43:11 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Thu, 26 Aug 2021 21:43:13 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Aug 2021 21:43:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Aug 2021 21:43:14 GMT
WORKDIR /var/www/html
# Thu, 26 Aug 2021 21:43:16 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 26 Aug 2021 21:43:16 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Aug 2021 21:43:17 GMT
EXPOSE 9000
# Thu, 26 Aug 2021 21:43:17 GMT
CMD ["php-fpm"]
# Fri, 27 Aug 2021 02:25:30 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         busybox-static     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 27 Aug 2021 02:25:31 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 27 Aug 2021 02:25:31 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 27 Aug 2021 02:32:27 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libxml2-dev         libmagickwand-dev         libzip-dev         libwebp-dev         libgmp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.20;     pecl install memcached-3.1.5;     pecl install redis-5.3.4;     pecl install imagick-3.5.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Aug 2021 02:32:29 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/nextcloud.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 27 Aug 2021 02:32:29 GMT
VOLUME [/var/www/html]
# Fri, 27 Aug 2021 02:36:14 GMT
ENV NEXTCLOUD_VERSION=21.0.4
# Fri, 27 Aug 2021 02:37:49 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Aug 2021 02:37:52 GMT
COPY multi:5c7d3e21c40c6f3326b9c24bb148355014771883d3bc821f8ada4fed6795cbb4 in / 
# Fri, 27 Aug 2021 02:37:54 GMT
COPY multi:d1870de3d4b4de5680360a8bcad7129a7c7615ba76daad773ab1eee24d4a949f in /usr/src/nextcloud/config/ 
# Fri, 27 Aug 2021 02:37:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 27 Aug 2021 02:37:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3dfab4a5b2accf2d709d8c7d14a42715948ecf2d6da4943a6e2c0de8ae7536a0`  
		Last Modified: Tue, 17 Aug 2021 02:12:42 GMT  
		Size: 24.9 MB (24879063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d321d8f4d7296db7b3f84788c07d175b2504e3cb238dcf6d902c00d2f767c7d`  
		Last Modified: Tue, 17 Aug 2021 11:53:57 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9034c2264011ba14ef8ccef384c6f6af0f92c68e0c9712c91ed2e172eb0bc1c6`  
		Last Modified: Tue, 17 Aug 2021 11:54:39 GMT  
		Size: 58.8 MB (58820510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c3914b89d903a4a841688fa553ea06173ed81ef703b0421fb8b8c8c37223d0`  
		Last Modified: Tue, 17 Aug 2021 11:53:57 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb022b3829aba4c5ca4e2bf5826c661671e4fa1db196c09729aa10988c88c47f`  
		Last Modified: Thu, 26 Aug 2021 23:03:04 GMT  
		Size: 10.7 MB (10690517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b52fba290b31a61b7a312004fd4b4d00b784568b389db238a7b1811c3b6cd65`  
		Last Modified: Thu, 26 Aug 2021 23:03:00 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36a7a2e91dd1691b2344c5bf3c0087d65b5d1039196ccac2211b4ea540a16a6`  
		Last Modified: Thu, 26 Aug 2021 23:03:13 GMT  
		Size: 29.6 MB (29574402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1d2b69c09ef007798d21905b78390dc3dbea39445638fd450fa1a664b640bb`  
		Last Modified: Thu, 26 Aug 2021 23:03:00 GMT  
		Size: 2.3 KB (2269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49601d9903866d39ed4bbd9735746a52de12057ae3b91c55e27ba47519140302`  
		Last Modified: Thu, 26 Aug 2021 23:03:00 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625d070310c21379592b47c8ed5bef869239fc64b44f05e501f396f05fd50d49`  
		Last Modified: Thu, 26 Aug 2021 23:03:00 GMT  
		Size: 8.4 KB (8447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513ee137aa6f07d5443e86b9f8f9b57c972b2467b08c2216fe693e5baaad0e2d`  
		Last Modified: Fri, 27 Aug 2021 02:46:58 GMT  
		Size: 1.6 MB (1578847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ccfaccd070416e20efe4a42d2ad020d2ecc3cf4a1a0db70c330e3762fba2c4c`  
		Last Modified: Fri, 27 Aug 2021 02:47:09 GMT  
		Size: 14.5 MB (14459965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604a38aeeeac5e444e34a2532050287018cc0f931493ecffebd5f62dcada56a1`  
		Last Modified: Fri, 27 Aug 2021 02:46:56 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf8e80a2e35f0ed0fad6c670b73f554d05b7fff678d1a0667f3d72d15a47d3b`  
		Last Modified: Fri, 27 Aug 2021 02:52:42 GMT  
		Size: 151.1 MB (151132052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e919bdab2fe47652736048ec09c37ff7ec00a5fbd9228589a46241f20e971f4`  
		Last Modified: Fri, 27 Aug 2021 02:51:07 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e9bed350965a5e94dcc1859c61afb563020039daa7eaa42f7709151339ecae`  
		Last Modified: Fri, 27 Aug 2021 02:51:07 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production-fpm` - linux; arm variant v7

```console
$ docker pull nextcloud@sha256:b04c51b5ba8b7030ddf6bf465eb39bd51459f9c85950416c49b23f00bf002ef9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285051506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab9afedc944ffc33318ceeaab60da2afaa61bb2c010df1ab082ceefaed565aa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 17 Aug 2021 02:14:25 GMT
ADD file:ca8cc4b509e305fa07662fbf2234ed78f0056569f6ca047305dc02bcd60f1558 in / 
# Tue, 17 Aug 2021 02:14:26 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 21:42:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 17 Aug 2021 21:42:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 17 Aug 2021 21:42:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 21:42:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 17 Aug 2021 21:42:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 17 Aug 2021 21:58:00 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Tue, 17 Aug 2021 21:58:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Aug 2021 21:58:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Aug 2021 21:58:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 17 Aug 2021 23:26:37 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 17 Aug 2021 23:26:37 GMT
ENV PHP_VERSION=7.4.22
# Tue, 17 Aug 2021 23:26:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.22.tar.xz.asc
# Tue, 17 Aug 2021 23:26:39 GMT
ENV PHP_SHA256=8e078cd7d2f49ac3fcff902490a5bb1addc885e7e3b0d8dd068f42c68297bde8
# Tue, 17 Aug 2021 23:27:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 17 Aug 2021 23:27:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 17 Aug 2021 23:31:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libonig-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 17 Aug 2021 23:31:47 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Tue, 17 Aug 2021 23:31:48 GMT
RUN docker-php-ext-enable sodium
# Tue, 17 Aug 2021 23:31:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 17 Aug 2021 23:31:49 GMT
WORKDIR /var/www/html
# Tue, 17 Aug 2021 23:31:51 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 17 Aug 2021 23:31:52 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Aug 2021 23:31:52 GMT
EXPOSE 9000
# Tue, 17 Aug 2021 23:31:53 GMT
CMD ["php-fpm"]
# Thu, 19 Aug 2021 02:41:07 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         busybox-static     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Thu, 19 Aug 2021 02:41:08 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 19 Aug 2021 02:41:08 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 19 Aug 2021 02:47:48 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libxml2-dev         libmagickwand-dev         libzip-dev         libwebp-dev         libgmp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.20;     pecl install memcached-3.1.5;     pecl install redis-5.3.4;     pecl install imagick-3.5.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 19 Aug 2021 02:47:50 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/nextcloud.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Thu, 19 Aug 2021 02:47:50 GMT
VOLUME [/var/www/html]
# Thu, 19 Aug 2021 02:51:42 GMT
ENV NEXTCLOUD_VERSION=21.0.4
# Thu, 19 Aug 2021 02:53:12 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Thu, 19 Aug 2021 02:53:15 GMT
COPY multi:5c7d3e21c40c6f3326b9c24bb148355014771883d3bc821f8ada4fed6795cbb4 in / 
# Thu, 19 Aug 2021 02:53:17 GMT
COPY multi:d1870de3d4b4de5680360a8bcad7129a7c7615ba76daad773ab1eee24d4a949f in /usr/src/nextcloud/config/ 
# Thu, 19 Aug 2021 02:53:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Aug 2021 02:53:18 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:13e3f03410ff211945a725435c13065288d48a8cb740f0530e7588012c2679a4`  
		Last Modified: Tue, 17 Aug 2021 02:30:58 GMT  
		Size: 22.7 MB (22746254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33c060d8eec1708da27f0a9a76b0a314310580ed93439479c9ae092af343369`  
		Last Modified: Wed, 18 Aug 2021 00:43:22 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a525ebb74853898f10007afc7de780282b21a9ea0a864beded94ab9ad168eac5`  
		Last Modified: Wed, 18 Aug 2021 00:43:56 GMT  
		Size: 59.5 MB (59513282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890c2ff8fc03c934f3f2800273f710d7816ef3874597613e207973b7ef71188a`  
		Last Modified: Wed, 18 Aug 2021 00:43:20 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30711849a8b861c1f9f156805be56ac86b4dc572f33dd2893bd74c76abe2638c`  
		Last Modified: Wed, 18 Aug 2021 00:58:29 GMT  
		Size: 10.7 MB (10667708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380cddd135014b373a5730599320528da0d6ee942331c4e4598fc124ac106876`  
		Last Modified: Wed, 18 Aug 2021 00:58:25 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a425ea01eb3092783cc05e2d44d8649e2f2c45cab6f2c4ac23f5f8d6aea216d`  
		Last Modified: Wed, 18 Aug 2021 00:58:33 GMT  
		Size: 26.2 MB (26204990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c550998d3eee755c75482fe8d4d45a42bc35864f45724cbb6ac72a28556ecd`  
		Last Modified: Wed, 18 Aug 2021 00:58:25 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01c3182d5c9430c13cc57ee2fc2088304d88ede17753890eec78d5993432e45`  
		Last Modified: Wed, 18 Aug 2021 00:58:25 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f64a50cb3cd890ee258248467d325c5258c0c107cf1f6113ce940dae917478`  
		Last Modified: Wed, 18 Aug 2021 00:58:25 GMT  
		Size: 8.4 KB (8447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c09b97e05eda53de9918cf80ee7c829aba75ea48e413536927ee9bdd1fcbf0`  
		Last Modified: Thu, 19 Aug 2021 03:03:05 GMT  
		Size: 1.4 MB (1425745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516100ef537fc61fccc0d7a5f4117bc21e2fad23a06d73c8c27473096a01e1ce`  
		Last Modified: Thu, 19 Aug 2021 03:03:09 GMT  
		Size: 13.3 MB (13344199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66683af006f21c167165f98709cd224b4038f8a81ec3daa714d833bb076f9331`  
		Last Modified: Thu, 19 Aug 2021 03:03:02 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e28d5cfe6d36f535aee02fe90bdd01bbc06b3251c5ee6c948426eae7ac1d344`  
		Last Modified: Thu, 19 Aug 2021 03:08:55 GMT  
		Size: 151.1 MB (151132102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22994509a507cd3f4563dd881ad62b5a61bff13d4561ada389be6e49d01c92ff`  
		Last Modified: Thu, 19 Aug 2021 03:07:19 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835106ffeba3bb49de762cc65c8f01dc442ef02b928e6d69e5e8a51624527c62`  
		Last Modified: Thu, 19 Aug 2021 03:07:19 GMT  
		Size: 2.0 KB (2050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production-fpm` - linux; arm64 variant v8

```console
$ docker pull nextcloud@sha256:eaa89f2660bbc35bc67761439c570b74374e4307282705b5606b20549ec69ff0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.7 MB (304723954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1161d7b8f8b964e58a98d5f8b66a6e12cbba4b08bece97566867914b15d55a2d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:31 GMT
ADD file:a62249c8d6f38120ba61478f35ce3cc947234ac504859ced66532a60de786609 in / 
# Tue, 17 Aug 2021 01:46:31 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:22:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 17 Aug 2021 09:22:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 17 Aug 2021 09:22:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:22:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 17 Aug 2021 09:22:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 17 Aug 2021 09:33:20 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Tue, 17 Aug 2021 09:33:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Aug 2021 09:33:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Aug 2021 09:33:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 17 Aug 2021 10:05:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 27 Aug 2021 00:53:17 GMT
ENV PHP_VERSION=7.4.23
# Fri, 27 Aug 2021 00:53:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.23.tar.xz.asc
# Fri, 27 Aug 2021 00:53:17 GMT
ENV PHP_SHA256=cea52313fcffe56343bcd3c66dbb23cd5507dc559cc2e3547cf8f5452e88a05d
# Fri, 27 Aug 2021 00:53:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 27 Aug 2021 00:53:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Aug 2021 00:56:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Aug 2021 00:56:53 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 27 Aug 2021 00:56:54 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Aug 2021 00:56:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Aug 2021 00:56:55 GMT
WORKDIR /var/www/html
# Fri, 27 Aug 2021 00:56:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 27 Aug 2021 00:56:55 GMT
STOPSIGNAL SIGQUIT
# Fri, 27 Aug 2021 00:56:56 GMT
EXPOSE 9000
# Fri, 27 Aug 2021 00:56:56 GMT
CMD ["php-fpm"]
# Fri, 27 Aug 2021 05:36:43 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         busybox-static     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 27 Aug 2021 05:36:43 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 27 Aug 2021 05:36:43 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 27 Aug 2021 05:39:17 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libxml2-dev         libmagickwand-dev         libzip-dev         libwebp-dev         libgmp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.20;     pecl install memcached-3.1.5;     pecl install redis-5.3.4;     pecl install imagick-3.5.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Aug 2021 05:39:18 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/nextcloud.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 27 Aug 2021 05:39:18 GMT
VOLUME [/var/www/html]
# Fri, 27 Aug 2021 05:44:49 GMT
ENV NEXTCLOUD_VERSION=21.0.4
# Fri, 27 Aug 2021 05:45:34 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Aug 2021 05:45:36 GMT
COPY multi:5c7d3e21c40c6f3326b9c24bb148355014771883d3bc821f8ada4fed6795cbb4 in / 
# Fri, 27 Aug 2021 05:45:37 GMT
COPY multi:d1870de3d4b4de5680360a8bcad7129a7c7615ba76daad773ab1eee24d4a949f in /usr/src/nextcloud/config/ 
# Fri, 27 Aug 2021 05:45:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 27 Aug 2021 05:45:37 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:64ac1a72c06aa20e6c3b2e37ce66ddf902187eb683a427a477895f158a930e31`  
		Last Modified: Tue, 17 Aug 2021 01:54:22 GMT  
		Size: 25.9 MB (25915072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2900799337938aef6f721ade2a9bd22c057d46c83eb42ff623555b6eb4b1e9e9`  
		Last Modified: Tue, 17 Aug 2021 10:48:38 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22e74ac47771369d7c92bd6f47d92fcf96086e1d641c9d87462359bbda7d65e`  
		Last Modified: Tue, 17 Aug 2021 10:48:49 GMT  
		Size: 70.4 MB (70356766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1783e2b14bb08062d9096cd548d94f9327c5ba658efb80d09669f3ff2fc4d5a`  
		Last Modified: Tue, 17 Aug 2021 10:48:38 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab78889fb6c11ef2fd1b20279001520a6c1bc44397017c31583c3c834791df87`  
		Last Modified: Fri, 27 Aug 2021 02:51:18 GMT  
		Size: 10.7 MB (10691212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6359b0fb5efe510b5735558d56d3559d47e96f161082be663a90322e7827281`  
		Last Modified: Fri, 27 Aug 2021 02:51:14 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b11fff2fd93edf192e1b63bbf7100d46a2a3c17a38229380ebc95330db4112`  
		Last Modified: Fri, 27 Aug 2021 02:51:19 GMT  
		Size: 30.8 MB (30757524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d527b0c3a7c661afddbc17958aa39aee9e63aa1ce3621c91fbc63d134a5643cf`  
		Last Modified: Fri, 27 Aug 2021 02:51:14 GMT  
		Size: 2.3 KB (2271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daaef9970db3fed5e1396f7ec46fb0b34853787f3d3ecd93f5118573e56bf802`  
		Last Modified: Fri, 27 Aug 2021 02:51:14 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f6e474e7b164abbf4a54445d8d1a670f9d9496653c08fa33b2b35f54e0edc4`  
		Last Modified: Fri, 27 Aug 2021 02:51:14 GMT  
		Size: 8.4 KB (8443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd36cc6494706fa63c046322c2490faf75539bd5b1eb63a9b4b77a3e3ccbe0d3`  
		Last Modified: Fri, 27 Aug 2021 05:52:01 GMT  
		Size: 1.6 MB (1606451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d273750558ee4953fc695989534f6a4d8ae8a15fd1d408549eaf8dbc303ef9c`  
		Last Modified: Fri, 27 Aug 2021 05:52:00 GMT  
		Size: 14.2 MB (14247466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38009d6add0f7fed91ff0b3dbb583d3e46e49d5a815d02501f8bf1378682c372`  
		Last Modified: Fri, 27 Aug 2021 05:51:57 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f526237251661144ac59a1b9863166d2b28dd3f86c4664ca595645389894d92`  
		Last Modified: Fri, 27 Aug 2021 05:54:39 GMT  
		Size: 151.1 MB (151132237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83eff9d360e717dcafb68e9a55250ba4d2442fa035e608407d7a43e9e0b95466`  
		Last Modified: Fri, 27 Aug 2021 05:54:18 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab169bcbf92365e3cb0f574f4bcf0e45412f05e3070894eeff64c6e631e3b7fb`  
		Last Modified: Fri, 27 Aug 2021 05:54:18 GMT  
		Size: 2.1 KB (2052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production-fpm` - linux; 386

```console
$ docker pull nextcloud@sha256:0f1a1463822e3dd1042c1dacda4dd2b1eb182ef39955c2dacb617adda84aa005
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.7 MB (319671309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494f752951b0855cb647044a79ec6e4820dc0239715ea75fe6fae8d27cd14af4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 17 Aug 2021 01:41:16 GMT
ADD file:0418032b55cd0a6dd515ac277fb9f92354397503cab212d446d3a3d8c647a60f in / 
# Tue, 17 Aug 2021 01:41:17 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 17:50:01 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 17 Aug 2021 17:50:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 17 Aug 2021 17:50:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 17:50:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 17 Aug 2021 17:50:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 17 Aug 2021 18:02:12 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Tue, 17 Aug 2021 18:02:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Aug 2021 18:02:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Aug 2021 18:02:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 17 Aug 2021 18:46:06 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 27 Aug 2021 00:16:59 GMT
ENV PHP_VERSION=7.4.23
# Fri, 27 Aug 2021 00:16:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.23.tar.xz.asc
# Fri, 27 Aug 2021 00:16:59 GMT
ENV PHP_SHA256=cea52313fcffe56343bcd3c66dbb23cd5507dc559cc2e3547cf8f5452e88a05d
# Fri, 27 Aug 2021 00:17:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 27 Aug 2021 00:17:19 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Aug 2021 00:25:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Aug 2021 00:25:41 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 27 Aug 2021 00:25:42 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Aug 2021 00:25:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Aug 2021 00:25:43 GMT
WORKDIR /var/www/html
# Fri, 27 Aug 2021 00:25:44 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 27 Aug 2021 00:25:44 GMT
STOPSIGNAL SIGQUIT
# Fri, 27 Aug 2021 00:25:44 GMT
EXPOSE 9000
# Fri, 27 Aug 2021 00:25:44 GMT
CMD ["php-fpm"]
# Fri, 27 Aug 2021 06:43:21 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         busybox-static     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 27 Aug 2021 06:43:21 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 27 Aug 2021 06:43:21 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 27 Aug 2021 06:46:15 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libxml2-dev         libmagickwand-dev         libzip-dev         libwebp-dev         libgmp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.20;     pecl install memcached-3.1.5;     pecl install redis-5.3.4;     pecl install imagick-3.5.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Aug 2021 06:46:16 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/nextcloud.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 27 Aug 2021 06:46:16 GMT
VOLUME [/var/www/html]
# Fri, 27 Aug 2021 06:52:23 GMT
ENV NEXTCLOUD_VERSION=21.0.4
# Fri, 27 Aug 2021 06:53:18 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Aug 2021 06:53:19 GMT
COPY multi:5c7d3e21c40c6f3326b9c24bb148355014771883d3bc821f8ada4fed6795cbb4 in / 
# Fri, 27 Aug 2021 06:53:20 GMT
COPY multi:d1870de3d4b4de5680360a8bcad7129a7c7615ba76daad773ab1eee24d4a949f in /usr/src/nextcloud/config/ 
# Fri, 27 Aug 2021 06:53:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 27 Aug 2021 06:53:21 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c1c94e1f2523d69effaa463d64fc9962cfc67e2a956f0476c94200e7cf19edf0`  
		Last Modified: Tue, 17 Aug 2021 01:50:57 GMT  
		Size: 27.8 MB (27797627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e9eeed7bb21b82111b77c53bee07740bd5cd6dbfdf8b4f7184f37223efbe3b`  
		Last Modified: Tue, 17 Aug 2021 19:44:06 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e06f2ca62ad9d4559e5f42075c39284a2344543f09b27ba2335228b2d85a187`  
		Last Modified: Tue, 17 Aug 2021 19:44:27 GMT  
		Size: 81.2 MB (81230104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31f4ca0fa0ea804356df67cb3c353fbe8208878ec45ffbb9164eb9aa8bede35`  
		Last Modified: Tue, 17 Aug 2021 19:44:06 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d35f3613fbcd5106e2cb3190a21638bf4f9c016400ed71e2a6cbd28ac28d75`  
		Last Modified: Fri, 27 Aug 2021 03:51:18 GMT  
		Size: 10.7 MB (10691701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa712a5566488e05eaaf2aa9c5e8c040c3e447579abf266e8f804fef70d519f`  
		Last Modified: Fri, 27 Aug 2021 03:51:15 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298099bfd1d726c0656501475ebdd6353ab16df192dbf80edf03de42d65de516`  
		Last Modified: Fri, 27 Aug 2021 03:51:23 GMT  
		Size: 31.9 MB (31905546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff252a5eddf0c093128f9495e33bdd958f04011f9468185bdf5f2c72a9294ddc`  
		Last Modified: Fri, 27 Aug 2021 03:51:15 GMT  
		Size: 2.3 KB (2274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b116f7e0511a1157d602d7569dc42df187c81c864c97896695c8fe4d0e63abef`  
		Last Modified: Fri, 27 Aug 2021 03:51:15 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27014576929e287b42d90d4ec1656f4b20e9a14f39c761ad11a363f90891ac07`  
		Last Modified: Fri, 27 Aug 2021 03:51:15 GMT  
		Size: 8.4 KB (8450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0ec51441b0259b1df95a5979398d9ac4aab3cf37369f370322c4c04bdd0c24`  
		Last Modified: Fri, 27 Aug 2021 07:01:06 GMT  
		Size: 1.7 MB (1664111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d9c817f79c5bb88f54f7f700108b88198dd4fbedbdf270f017e0178b6999de`  
		Last Modified: Fri, 27 Aug 2021 07:01:07 GMT  
		Size: 15.2 MB (15231702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50fe732c6e83147cbb03980f4807a571f9a467338894d915602f16866d4f73f`  
		Last Modified: Fri, 27 Aug 2021 07:01:03 GMT  
		Size: 596.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434f1ca5eee05f1528dffd3b87c8b4c0a10b29160b5a088dc05d93f06319827e`  
		Last Modified: Fri, 27 Aug 2021 07:04:16 GMT  
		Size: 151.1 MB (151133285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731189bee70ca9a2c71da8624b678f6118908b190b73606229cc11c1e5d602f9`  
		Last Modified: Fri, 27 Aug 2021 07:03:50 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d62da82eb568075603279ce0daea3cfeea75401c2b5130fed47c18e395a84f`  
		Last Modified: Fri, 27 Aug 2021 07:03:50 GMT  
		Size: 2.0 KB (2048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production-fpm` - linux; mips64le

```console
$ docker pull nextcloud@sha256:addef5b1b97a358eb70081193710db028b3616a4c6230c9105056422832a023c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295135205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54b614c8a67509cbd1eae9e5fbcc8eaf5ede5031f80af9883cb305a1d56296b4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 17 Aug 2021 01:12:26 GMT
ADD file:8bd279803ead4ddce8db90b65e89c423f84fbf6042bfbeae8c09486b2e884cde in / 
# Tue, 17 Aug 2021 01:12:27 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 21:57:50 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 17 Aug 2021 21:57:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 17 Aug 2021 21:58:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 21:58:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 17 Aug 2021 21:58:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 17 Aug 2021 22:25:04 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Tue, 17 Aug 2021 22:25:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Aug 2021 22:25:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Aug 2021 22:25:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 18 Aug 2021 01:35:26 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Aug 2021 23:40:46 GMT
ENV PHP_VERSION=7.4.23
# Thu, 26 Aug 2021 23:40:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.23.tar.xz.asc
# Thu, 26 Aug 2021 23:40:47 GMT
ENV PHP_SHA256=cea52313fcffe56343bcd3c66dbb23cd5507dc559cc2e3547cf8f5452e88a05d
# Thu, 26 Aug 2021 23:41:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 26 Aug 2021 23:41:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Aug 2021 23:54:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 26 Aug 2021 23:54:02 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Thu, 26 Aug 2021 23:54:04 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Aug 2021 23:54:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Aug 2021 23:54:05 GMT
WORKDIR /var/www/html
# Thu, 26 Aug 2021 23:54:07 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 26 Aug 2021 23:54:07 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Aug 2021 23:54:08 GMT
EXPOSE 9000
# Thu, 26 Aug 2021 23:54:08 GMT
CMD ["php-fpm"]
# Fri, 27 Aug 2021 03:41:53 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         busybox-static     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 27 Aug 2021 03:41:54 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 27 Aug 2021 03:41:54 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 27 Aug 2021 03:49:38 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libxml2-dev         libmagickwand-dev         libzip-dev         libwebp-dev         libgmp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.20;     pecl install memcached-3.1.5;     pecl install redis-5.3.4;     pecl install imagick-3.5.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Aug 2021 03:49:40 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/nextcloud.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 27 Aug 2021 03:49:41 GMT
VOLUME [/var/www/html]
# Fri, 27 Aug 2021 03:53:51 GMT
ENV NEXTCLOUD_VERSION=21.0.4
# Fri, 27 Aug 2021 03:55:52 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Aug 2021 03:55:56 GMT
COPY multi:5c7d3e21c40c6f3326b9c24bb148355014771883d3bc821f8ada4fed6795cbb4 in / 
# Fri, 27 Aug 2021 03:55:57 GMT
COPY multi:d1870de3d4b4de5680360a8bcad7129a7c7615ba76daad773ab1eee24d4a949f in /usr/src/nextcloud/config/ 
# Fri, 27 Aug 2021 03:55:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 27 Aug 2021 03:55:58 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a711e3e37b88ef77496c07ed663bb4270ecba9057eba452a91cc9be0bafb9c32`  
		Last Modified: Tue, 17 Aug 2021 01:21:44 GMT  
		Size: 25.8 MB (25813007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf84c4fd36e09e3b64922af82aaeb18671cd58784fc1244b0b8181fc5a2e2b3`  
		Last Modified: Wed, 18 Aug 2021 03:35:33 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a1a289c2e9231e9dde511bbfd8a54a27c3b3a66d012521f5069200c8167aa3`  
		Last Modified: Wed, 18 Aug 2021 03:36:23 GMT  
		Size: 61.4 MB (61404043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7dff628db72bf68c02df5239dbd86edd54217fbfe9442d22e2090ab3421b60b`  
		Last Modified: Wed, 18 Aug 2021 03:35:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac39194df8231c96a6011ed0f5c8bb889e3c790dbf515303ec00acc854ef3fe`  
		Last Modified: Fri, 27 Aug 2021 01:55:45 GMT  
		Size: 10.7 MB (10689826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16883e3f42261ca47922ed0b6cc44cc1c358f534a8377e8f625dd3c8b18e12c8`  
		Last Modified: Fri, 27 Aug 2021 01:55:39 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a8fa3ad274ca7ef97f798438349ccec704a9e318aeddb9e927e0f753ba88d3`  
		Last Modified: Fri, 27 Aug 2021 01:56:01 GMT  
		Size: 30.0 MB (30040159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0db7d82e05f1cdd7dccab1b4c9e5d80fa3d0fffa5a3352e80969003305e664f`  
		Last Modified: Fri, 27 Aug 2021 01:55:40 GMT  
		Size: 2.3 KB (2272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675eebecf2560b47236030475680433448a4800dced638ce1fd002cec5fa64ce`  
		Last Modified: Fri, 27 Aug 2021 01:55:39 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3940be9776af678c1ee0bed11ef8ccc513219981e72913170d388e43b7d6dd61`  
		Last Modified: Fri, 27 Aug 2021 01:55:39 GMT  
		Size: 8.4 KB (8450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35af744d1f5453d321a17b339b914052685ac54992759f767f43d2ccd39b26ba`  
		Last Modified: Fri, 27 Aug 2021 04:03:18 GMT  
		Size: 1.7 MB (1745571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e01e1f84e6242080cce7e29633f2eefa356c93478ad901d202d2483e7ba6860`  
		Last Modified: Fri, 27 Aug 2021 04:03:25 GMT  
		Size: 14.3 MB (14293560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e92551231bea4a44f7aa1119309c44c4da226f931da14e3c14d79768c9a83d`  
		Last Modified: Fri, 27 Aug 2021 04:03:13 GMT  
		Size: 565.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b4fe7030ce14552491bbd706b5d96619682e13bc99b92aa416f7587ab77d573`  
		Last Modified: Fri, 27 Aug 2021 04:08:41 GMT  
		Size: 151.1 MB (151131877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f304f00b97ed1b29c935d8f1d7b651eb3ccb6c0dc62724943622d9883399d9`  
		Last Modified: Fri, 27 Aug 2021 04:07:08 GMT  
		Size: 2.6 KB (2627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d29d08784a0b98667087bb322d931ccfe469fc93d73a707b84fb276d5d6e6a6`  
		Last Modified: Fri, 27 Aug 2021 04:07:08 GMT  
		Size: 2.1 KB (2055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production-fpm` - linux; ppc64le

```console
$ docker pull nextcloud@sha256:1c12918a0b2ef30ef17947ed21d4b79779903d5c8e8f39ed3cb3b1b20f32e1b6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.8 MB (322847187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ffe1b89cd9db135e576adf07bd4b9b2586d7364c10fea5ed3a96595e75bbf7d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 17 Aug 2021 01:34:13 GMT
ADD file:8b9b12a994a2519f725d1ed1f4ab5a444665262678fd8e6c42cf78f32dacb7fa in / 
# Tue, 17 Aug 2021 01:34:20 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 20:07:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 17 Aug 2021 20:08:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 17 Aug 2021 20:12:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 20:12:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 17 Aug 2021 20:12:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 17 Aug 2021 20:39:42 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Tue, 17 Aug 2021 20:39:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Aug 2021 20:39:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Aug 2021 20:39:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 17 Aug 2021 23:05:34 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 17 Aug 2021 23:05:41 GMT
ENV PHP_VERSION=7.4.22
# Tue, 17 Aug 2021 23:05:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.22.tar.xz.asc
# Tue, 17 Aug 2021 23:05:50 GMT
ENV PHP_SHA256=8e078cd7d2f49ac3fcff902490a5bb1addc885e7e3b0d8dd068f42c68297bde8
# Tue, 17 Aug 2021 23:08:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 17 Aug 2021 23:08:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 17 Aug 2021 23:13:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libonig-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 17 Aug 2021 23:13:51 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Tue, 17 Aug 2021 23:14:04 GMT
RUN docker-php-ext-enable sodium
# Tue, 17 Aug 2021 23:14:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 17 Aug 2021 23:14:18 GMT
WORKDIR /var/www/html
# Tue, 17 Aug 2021 23:14:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 17 Aug 2021 23:14:30 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Aug 2021 23:14:35 GMT
EXPOSE 9000
# Tue, 17 Aug 2021 23:14:39 GMT
CMD ["php-fpm"]
# Wed, 18 Aug 2021 23:11:13 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         busybox-static     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Wed, 18 Aug 2021 23:11:16 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 18 Aug 2021 23:11:18 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 18 Aug 2021 23:23:51 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libxml2-dev         libmagickwand-dev         libzip-dev         libwebp-dev         libgmp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.20;     pecl install memcached-3.1.5;     pecl install redis-5.3.4;     pecl install imagick-3.5.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 23:24:07 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/nextcloud.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Wed, 18 Aug 2021 23:24:12 GMT
VOLUME [/var/www/html]
# Wed, 18 Aug 2021 23:32:43 GMT
ENV NEXTCLOUD_VERSION=21.0.4
# Wed, 18 Aug 2021 23:36:39 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 23:36:48 GMT
COPY multi:5c7d3e21c40c6f3326b9c24bb148355014771883d3bc821f8ada4fed6795cbb4 in / 
# Wed, 18 Aug 2021 23:36:52 GMT
COPY multi:d1870de3d4b4de5680360a8bcad7129a7c7615ba76daad773ab1eee24d4a949f in /usr/src/nextcloud/config/ 
# Wed, 18 Aug 2021 23:36:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Aug 2021 23:37:08 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c3e09f0e3e7f6fcb741a4c9214b63e341e1d9b53d7689a5ad6ff640b61a82541`  
		Last Modified: Tue, 17 Aug 2021 01:48:22 GMT  
		Size: 30.6 MB (30553721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccbb63881ed3aea74b5666bddbed760e2efb176d46887dffeaaad47865b97e86`  
		Last Modified: Wed, 18 Aug 2021 01:00:02 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99be8a44948af202f4c13e5f1ac9bca6d60ee898dd4fb70b92f36cfd380de14a`  
		Last Modified: Wed, 18 Aug 2021 01:01:26 GMT  
		Size: 82.3 MB (82290875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd90ce4a2fb80614fa9611ab92d7169578640316dfda1eabf6a877dcd89f487`  
		Last Modified: Wed, 18 Aug 2021 01:00:00 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa55bef5d1e4bea1966c5ac97c83006e8e2474f706effaa44382c62e5cf8c23`  
		Last Modified: Wed, 18 Aug 2021 01:15:10 GMT  
		Size: 10.7 MB (10669380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9144b3791a3a9e200b4a4113cb525c7e9a24ab15c4e9b0d13bd822bc243ea66`  
		Last Modified: Wed, 18 Aug 2021 01:15:02 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa2613cc3f37404eb929ae1570d57f5786bb084e513527e149d328085be174b`  
		Last Modified: Wed, 18 Aug 2021 01:15:21 GMT  
		Size: 30.3 MB (30262005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d67fe86cb0ee594fd55bcadc641232bd9ebe2a461a406da2048aa9d9e603571`  
		Last Modified: Wed, 18 Aug 2021 01:15:02 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a471fe36200352217c7400e771bc6af29f2693a41e88eee4c8d6ced210f6db`  
		Last Modified: Wed, 18 Aug 2021 01:15:02 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773a600ff59ae44004ea5491344c47bce07a74d5ee5b0b57aadc1d4fbf28104f`  
		Last Modified: Wed, 18 Aug 2021 01:15:03 GMT  
		Size: 8.4 KB (8447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d223bc63e596045b2ec6d4aa4f45dd09df33e72b2c088c10fdf4ae07b2ab6e4`  
		Last Modified: Wed, 18 Aug 2021 23:48:57 GMT  
		Size: 1.8 MB (1803367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9fbec84aee499de0264aeebad23253dc1bf405159148f2fc00cebf284de1e7`  
		Last Modified: Wed, 18 Aug 2021 23:49:23 GMT  
		Size: 16.1 MB (16115016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d539f97ec77ec5864cc8331f601dd4381b90831342e2d3dfbc8c5abb9af151`  
		Last Modified: Wed, 18 Aug 2021 23:48:51 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779f045cc097218f77f594aeed32dd1ef054e674000a3bceee5a710235139e67`  
		Last Modified: Wed, 18 Aug 2021 23:52:11 GMT  
		Size: 151.1 MB (151135596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0adf13ebf043411d295bea0d7ae1d0bf2f3c43e30e489d09b6cf968926e0be80`  
		Last Modified: Wed, 18 Aug 2021 23:51:45 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5d4f164bb3073d9f4bbed4f767ac17b6fe7b511f1e22b793f54894fdee10c7`  
		Last Modified: Wed, 18 Aug 2021 23:51:45 GMT  
		Size: 2.1 KB (2055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production-fpm` - linux; s390x

```console
$ docker pull nextcloud@sha256:4ba5da0e1b60222a0d131b90ffbc9d961b71064dedafc65a1284344d2085827e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298221188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e6fce7b0a054753d2576714a9a494023a7546534d47480ff56713e00a629c75`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 17 Aug 2021 01:49:55 GMT
ADD file:f99acf07eb8c42cc90080a195bbcdb18850a1d7a333b385d5d8ebe31c9e9f783 in / 
# Tue, 17 Aug 2021 01:49:59 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:14:47 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 17 Aug 2021 08:14:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 17 Aug 2021 08:15:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 08:15:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 17 Aug 2021 08:15:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 17 Aug 2021 08:21:45 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Tue, 17 Aug 2021 08:21:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Aug 2021 08:21:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Aug 2021 08:21:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 17 Aug 2021 09:01:41 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Aug 2021 21:45:04 GMT
ENV PHP_VERSION=7.4.23
# Thu, 26 Aug 2021 21:45:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.23.tar.xz.asc
# Thu, 26 Aug 2021 21:45:05 GMT
ENV PHP_SHA256=cea52313fcffe56343bcd3c66dbb23cd5507dc559cc2e3547cf8f5452e88a05d
# Thu, 26 Aug 2021 21:45:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 26 Aug 2021 21:45:31 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Aug 2021 21:49:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 26 Aug 2021 21:49:30 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Thu, 26 Aug 2021 21:49:31 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Aug 2021 21:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Aug 2021 21:49:32 GMT
WORKDIR /var/www/html
# Thu, 26 Aug 2021 21:49:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 26 Aug 2021 21:49:33 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Aug 2021 21:49:34 GMT
EXPOSE 9000
# Thu, 26 Aug 2021 21:49:34 GMT
CMD ["php-fpm"]
# Fri, 27 Aug 2021 06:06:04 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         busybox-static     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 27 Aug 2021 06:06:04 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 27 Aug 2021 06:06:05 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 27 Aug 2021 06:10:07 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libxml2-dev         libmagickwand-dev         libzip-dev         libwebp-dev         libgmp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.20;     pecl install memcached-3.1.5;     pecl install redis-5.3.4;     pecl install imagick-3.5.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Aug 2021 06:10:10 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/nextcloud.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 27 Aug 2021 06:10:11 GMT
VOLUME [/var/www/html]
# Fri, 27 Aug 2021 06:18:19 GMT
ENV NEXTCLOUD_VERSION=21.0.4
# Fri, 27 Aug 2021 06:19:19 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Aug 2021 06:19:37 GMT
COPY multi:5c7d3e21c40c6f3326b9c24bb148355014771883d3bc821f8ada4fed6795cbb4 in / 
# Fri, 27 Aug 2021 06:19:38 GMT
COPY multi:d1870de3d4b4de5680360a8bcad7129a7c7615ba76daad773ab1eee24d4a949f in /usr/src/nextcloud/config/ 
# Fri, 27 Aug 2021 06:19:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 27 Aug 2021 06:19:39 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ed4fb22ab70391b36e4b9f97e34387c33652dc2b91b5f0c7ef4ada070bfd32c3`  
		Last Modified: Tue, 17 Aug 2021 01:58:12 GMT  
		Size: 25.8 MB (25760856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b509377d804e99fd3d8c5eb11fdcb06ac0592b467e1a5d34f296426a6cec6a14`  
		Last Modified: Tue, 17 Aug 2021 09:47:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef8dd0e3b36bc333683aafc6e422e5b3a9294feb703deb0a71a749175c45da6`  
		Last Modified: Tue, 17 Aug 2021 09:47:10 GMT  
		Size: 64.7 MB (64710852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b280bc6a9cfb9647c076d519d4cb4187708961862386bd0840ea7453ef0e7992`  
		Last Modified: Tue, 17 Aug 2021 09:47:00 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c3c1b80b2c964126a11ebf6f96f6bd0118e75ae92a536b14b3f0669c2271fc`  
		Last Modified: Fri, 27 Aug 2021 00:21:35 GMT  
		Size: 10.7 MB (10690805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574647cb9f60effd6f92e7d3f99abe8666004357a16e7dd604c78783d141ed9c`  
		Last Modified: Fri, 27 Aug 2021 00:21:33 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:119f63596707b4074d4c1af322c29747030480c4db6f50739cf12c3983098ffd`  
		Last Modified: Fri, 27 Aug 2021 00:21:37 GMT  
		Size: 29.9 MB (29948054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1abe2a5116ab6b11ad7966bc3c21636955804d4db72cca24dc3327a7aeee79de`  
		Last Modified: Fri, 27 Aug 2021 00:21:33 GMT  
		Size: 2.3 KB (2269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ce4557986c47b07c020f9c862d8978ea85fbd5dbe7d800f61c573b14288e25`  
		Last Modified: Fri, 27 Aug 2021 00:21:33 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7181e1c9639f2e7dae05f379b3d4429d8ba1010fbcb33245072edd16c86f4fa7`  
		Last Modified: Fri, 27 Aug 2021 00:21:33 GMT  
		Size: 8.4 KB (8447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190fc1fbe5d01009a968e17f8747b3ce6eb6e66122191ae1cbc067df621a88a9`  
		Last Modified: Fri, 27 Aug 2021 06:27:48 GMT  
		Size: 1.6 MB (1600539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3d5f79f8973c50584ede8d29e4190e13e128c2472d23dea90e51faa78a831a`  
		Last Modified: Fri, 27 Aug 2021 06:27:48 GMT  
		Size: 14.4 MB (14360382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2977c7a7713b9e7acaa8a8378985c0d322066823a5eff68229275abc3188046`  
		Last Modified: Fri, 27 Aug 2021 06:27:46 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40c11656324925bb69a8e61fa2cf42efb3a3bced44392c50d0a1156fcafa5a5`  
		Last Modified: Fri, 27 Aug 2021 06:29:41 GMT  
		Size: 151.1 MB (151132473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5acee31d536cb93bf3b689137c515c06b77cde964b08e9422da816f7fede483a`  
		Last Modified: Fri, 27 Aug 2021 06:29:24 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f734d071293c1ce475041c3b2bb01444015111e9ac8e2e43ab54cb6bbd72ed2`  
		Last Modified: Fri, 27 Aug 2021 06:29:24 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
