## `joomla:4-php8.0-fpm-alpine`

```console
$ docker pull joomla@sha256:7b17199e0adf91ec27151d013ccc7b9beec7325fb9aa7da9991bd8b29c80a89a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `joomla:4-php8.0-fpm-alpine` - linux; amd64

```console
$ docker pull joomla@sha256:a4537951dc62ae67de3fe421b6a12b0e95783143dfd1bf84d13ce54472ac0630
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58477906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c30299ea09cd72878e52701eac34ada59e827e3f8684bb8cc366a6e8e3529b57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 21:00:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 21:00:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 21:00:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 21:00:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 21:00:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 21:12:06 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 27 Aug 2021 21:12:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 21:12:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 21:12:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 21:33:53 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 27 Aug 2021 21:33:53 GMT
ENV PHP_VERSION=8.0.10
# Fri, 27 Aug 2021 21:33:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.10.tar.xz.asc
# Fri, 27 Aug 2021 21:33:53 GMT
ENV PHP_SHA256=66dc4d1bc86d9c1bc255b51b79d337ed1a7a035cf71230daabbf9a4ca35795eb
# Fri, 27 Aug 2021 21:34:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 27 Aug 2021 21:34:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Aug 2021 21:41:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Aug 2021 21:41:16 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 27 Aug 2021 21:41:18 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Aug 2021 21:41:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Aug 2021 21:41:18 GMT
WORKDIR /var/www/html
# Fri, 27 Aug 2021 21:41:19 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 27 Aug 2021 21:41:19 GMT
STOPSIGNAL SIGQUIT
# Fri, 27 Aug 2021 21:41:19 GMT
EXPOSE 9000
# Fri, 27 Aug 2021 21:41:20 GMT
CMD ["php-fpm"]
# Tue, 07 Sep 2021 21:35:09 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 07 Sep 2021 21:35:09 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 07 Sep 2021 21:35:10 GMT
RUN apk add --no-cache 	bash
# Tue, 07 Sep 2021 21:36:45 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		libjpeg-turbo-dev 		libmcrypt-dev 		libmemcached-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		gmp 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.20; 	pecl install mcrypt-1.0.4; 	pecl install memcached-3.1.5; 	pecl install redis-5.3.4; 		docker-php-ext-enable 		apcu 		mcrypt 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		)"; 	apk add --virtual .joomla-phpext-rundeps $runDeps; 	apk del .build-deps
# Tue, 07 Sep 2021 21:36:45 GMT
VOLUME [/var/www/html]
# Wed, 15 Sep 2021 00:27:10 GMT
ENV JOOMLA_VERSION=4.0.3
# Wed, 15 Sep 2021 00:27:11 GMT
ENV JOOMLA_SHA512=9c09a621586fdcc30351a915f283581c92080c210294cacc50e0e390d991f32bee9d61dfc7b0af33c81118e46d775152159c0e27dbf73f5531512328d716901f
# Wed, 15 Sep 2021 00:27:17 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Wed, 15 Sep 2021 00:27:18 GMT
COPY file:f6b7a1c96cc89593a2b9ce4c68af350ae02f2e0c654cd5e842ff6c03641d470e in /entrypoint.sh 
# Wed, 15 Sep 2021 00:27:18 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Wed, 15 Sep 2021 00:27:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Sep 2021 00:27:18 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153eea49496a46a69cf5f48803e9014824a6be1d3e04f9ee47cd3f395aba6d76`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 1.7 MB (1707843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11efd0df1fcb3f56e825ef3449f199b261f44e0130a10cb77fcf78339cb88173`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f3214c344df86e90fe2ae24d643d9dbc5dcfd6f229f4ee58f7c60c6f0cc895`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca3b156c422290e21480aba21414cdd28483d5dad9427df72d911dc79d0f99a`  
		Last Modified: Fri, 27 Aug 2021 22:43:29 GMT  
		Size: 10.7 MB (10722808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a82b29ca7841e4f869ad49ed2830595c69e5424d419fc603676d2f8eac2bc0`  
		Last Modified: Fri, 27 Aug 2021 22:43:26 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2009e000d9090805fd5d7046f821bc7a4dabbef12bf8468bc2ced38bbc6360`  
		Last Modified: Fri, 27 Aug 2021 22:43:29 GMT  
		Size: 15.1 MB (15082473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b96d2564500849cefb0d6f052fada5294521f8f1f7131587bfbebf4b705ed07`  
		Last Modified: Fri, 27 Aug 2021 22:43:26 GMT  
		Size: 2.3 KB (2263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f280c14bdb5b6903fa52cf29a5ff7fcccdb43d16c856e2128be4b4d703d74ad`  
		Last Modified: Fri, 27 Aug 2021 22:43:26 GMT  
		Size: 17.8 KB (17792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91356e6001923ea92c8eac82094f3dff308d05b81363fb945d1c00f200f68b3c`  
		Last Modified: Fri, 27 Aug 2021 22:43:26 GMT  
		Size: 8.6 KB (8570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e52e9220c6fe9008e78898bffb07145ebd27c6e5f79bf2caf1e23d45b9e1d4f`  
		Last Modified: Tue, 07 Sep 2021 21:47:43 GMT  
		Size: 465.6 KB (465569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885eafc9fbf02688037ea219456bad735930b3ae71b002f9e149dc7ca60ceebe`  
		Last Modified: Tue, 07 Sep 2021 21:47:44 GMT  
		Size: 6.3 MB (6328538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c5321918b3a13bd6e5667431617499235a2f2cf9dc716a9b02bc8e79b02c48`  
		Last Modified: Wed, 15 Sep 2021 00:31:44 GMT  
		Size: 21.3 MB (21323769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b88c5dcad98a9cecb37eae14665b160e9cd0774dcc7ed4212df4d2365b1020d`  
		Last Modified: Wed, 15 Sep 2021 00:31:40 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed2f70c1722568a3b2fe3084ed9c6fe57cf909b524570b82abd7957581be7cd`  
		Last Modified: Wed, 15 Sep 2021 00:31:40 GMT  
		Size: 613.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:4-php8.0-fpm-alpine` - linux; arm variant v6

```console
$ docker pull joomla@sha256:0fd1f4cd309d6647995dd36c78e08de1683c02e5bc93ad6412b69962f095e7e5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56315489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df32af1ae8198412008d94d3183fec68964fef7d21f0e465986061692e75215`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 20:48:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 20:48:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 20:48:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 20:48:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 20:48:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 20:53:20 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 27 Aug 2021 20:53:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 20:53:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 20:53:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 21:03:54 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 27 Aug 2021 21:03:55 GMT
ENV PHP_VERSION=8.0.10
# Fri, 27 Aug 2021 21:03:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.10.tar.xz.asc
# Fri, 27 Aug 2021 21:03:55 GMT
ENV PHP_SHA256=66dc4d1bc86d9c1bc255b51b79d337ed1a7a035cf71230daabbf9a4ca35795eb
# Fri, 27 Aug 2021 21:04:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 27 Aug 2021 21:04:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Aug 2021 21:08:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Aug 2021 21:08:39 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 27 Aug 2021 21:08:41 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Aug 2021 21:08:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Aug 2021 21:08:42 GMT
WORKDIR /var/www/html
# Fri, 27 Aug 2021 21:08:44 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 27 Aug 2021 21:08:44 GMT
STOPSIGNAL SIGQUIT
# Fri, 27 Aug 2021 21:08:45 GMT
EXPOSE 9000
# Fri, 27 Aug 2021 21:08:45 GMT
CMD ["php-fpm"]
# Tue, 07 Sep 2021 20:58:02 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 07 Sep 2021 20:58:02 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 07 Sep 2021 20:58:05 GMT
RUN apk add --no-cache 	bash
# Tue, 07 Sep 2021 21:02:18 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		libjpeg-turbo-dev 		libmcrypt-dev 		libmemcached-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		gmp 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.20; 	pecl install mcrypt-1.0.4; 	pecl install memcached-3.1.5; 	pecl install redis-5.3.4; 		docker-php-ext-enable 		apcu 		mcrypt 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		)"; 	apk add --virtual .joomla-phpext-rundeps $runDeps; 	apk del .build-deps
# Tue, 07 Sep 2021 21:02:19 GMT
VOLUME [/var/www/html]
# Wed, 15 Sep 2021 00:18:35 GMT
ENV JOOMLA_VERSION=4.0.3
# Wed, 15 Sep 2021 00:18:35 GMT
ENV JOOMLA_SHA512=9c09a621586fdcc30351a915f283581c92080c210294cacc50e0e390d991f32bee9d61dfc7b0af33c81118e46d775152159c0e27dbf73f5531512328d716901f
# Wed, 15 Sep 2021 00:18:53 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Wed, 15 Sep 2021 00:18:54 GMT
COPY file:f6b7a1c96cc89593a2b9ce4c68af350ae02f2e0c654cd5e842ff6c03641d470e in /entrypoint.sh 
# Wed, 15 Sep 2021 00:18:55 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Wed, 15 Sep 2021 00:18:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Sep 2021 00:18:56 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05720bf4927bb754d842782fff2d045d42b804759e30b8312cbf75272e200af`  
		Last Modified: Fri, 27 Aug 2021 21:55:19 GMT  
		Size: 1.7 MB (1696736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9951b98a5bb83a868efe164832e7d1a35e9a078a82219f95634454a864a332`  
		Last Modified: Fri, 27 Aug 2021 21:55:18 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6baa29c72aee654b7205fcfbde95333a6e9a5dfadc1a99d94e64c957f543ac`  
		Last Modified: Fri, 27 Aug 2021 21:55:18 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7782128efb22de8c009fb611ff2a882e179d7c920e400bb46eedee9b376177af`  
		Last Modified: Fri, 27 Aug 2021 21:58:13 GMT  
		Size: 10.7 MB (10722822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f768871d9f3b7a2e4dd4f5f40c76804c9d60be941d3528e7f301794911e817ed`  
		Last Modified: Fri, 27 Aug 2021 21:58:09 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78aa3af1d3d2cc2abfb828b05b88257d8c247b1babd2a4d9ca375959d58d8c9b`  
		Last Modified: Fri, 27 Aug 2021 21:58:19 GMT  
		Size: 13.7 MB (13713193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b218ec210bebdfbb6b1df39af6a2f62e301fa23b4eecfb8edff3ab1ceda4f14e`  
		Last Modified: Fri, 27 Aug 2021 21:58:08 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8b5b624f5b2f4d8704a78e97d283d4c24e0709b7b9b55ab3e7272dd520240d`  
		Last Modified: Fri, 27 Aug 2021 21:58:08 GMT  
		Size: 17.8 KB (17812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb01d3044874a53745331feef3483abe6819998c2c8a339093996cda0f4f70a`  
		Last Modified: Fri, 27 Aug 2021 21:58:09 GMT  
		Size: 8.6 KB (8571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ad035b6ff463795b36a31c6365f5942aef4f274f9e3664f140cd663c97fb77`  
		Last Modified: Tue, 07 Sep 2021 21:10:05 GMT  
		Size: 454.3 KB (454259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d672aa0258adf6ded3e17adea07ddfcb8b721de5a610c13a13bde3c03a3b7e5e`  
		Last Modified: Tue, 07 Sep 2021 21:10:08 GMT  
		Size: 5.7 MB (5744856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1cdeaf792179ed6eb83d0b9608bc2ff2e7d64a713644d1fc84dd6f9afec0eca`  
		Last Modified: Wed, 15 Sep 2021 00:22:01 GMT  
		Size: 21.3 MB (21323691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28bf8a41907d7de7f0bd12bfaae83bf829400a6c010dfbbd8d8802306b76bb0`  
		Last Modified: Wed, 15 Sep 2021 00:21:43 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80532da5875ce30af9d11be082dae7f7b29262efbfc7c53e40f98a5fda17767`  
		Last Modified: Wed, 15 Sep 2021 00:21:43 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:4-php8.0-fpm-alpine` - linux; arm variant v7

```console
$ docker pull joomla@sha256:bed3d6cdd8cf4b70fcca65068312724c2dc6863812f1442debb17751824522ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55114597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45be2b29583fadf7100f6278a021e6b88471dfdbc74405f78865f23c75bcdc6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 22:38:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 22:38:57 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 22:38:59 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 22:38:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 22:39:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 22:44:02 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 27 Aug 2021 22:44:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 22:44:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 22:44:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 22:56:22 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 27 Aug 2021 22:56:22 GMT
ENV PHP_VERSION=8.0.10
# Fri, 27 Aug 2021 22:56:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.10.tar.xz.asc
# Fri, 27 Aug 2021 22:56:23 GMT
ENV PHP_SHA256=66dc4d1bc86d9c1bc255b51b79d337ed1a7a035cf71230daabbf9a4ca35795eb
# Fri, 27 Aug 2021 22:56:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 27 Aug 2021 22:56:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Aug 2021 23:01:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Aug 2021 23:01:03 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 27 Aug 2021 23:01:05 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Aug 2021 23:01:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Aug 2021 23:01:06 GMT
WORKDIR /var/www/html
# Fri, 27 Aug 2021 23:01:08 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 27 Aug 2021 23:01:08 GMT
STOPSIGNAL SIGQUIT
# Fri, 27 Aug 2021 23:01:09 GMT
EXPOSE 9000
# Fri, 27 Aug 2021 23:01:09 GMT
CMD ["php-fpm"]
# Tue, 07 Sep 2021 21:34:37 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 07 Sep 2021 21:34:38 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 07 Sep 2021 21:34:40 GMT
RUN apk add --no-cache 	bash
# Tue, 07 Sep 2021 21:38:44 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		libjpeg-turbo-dev 		libmcrypt-dev 		libmemcached-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		gmp 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.20; 	pecl install mcrypt-1.0.4; 	pecl install memcached-3.1.5; 	pecl install redis-5.3.4; 		docker-php-ext-enable 		apcu 		mcrypt 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		)"; 	apk add --virtual .joomla-phpext-rundeps $runDeps; 	apk del .build-deps
# Tue, 07 Sep 2021 21:38:45 GMT
VOLUME [/var/www/html]
# Wed, 15 Sep 2021 00:35:04 GMT
ENV JOOMLA_VERSION=4.0.3
# Wed, 15 Sep 2021 00:35:05 GMT
ENV JOOMLA_SHA512=9c09a621586fdcc30351a915f283581c92080c210294cacc50e0e390d991f32bee9d61dfc7b0af33c81118e46d775152159c0e27dbf73f5531512328d716901f
# Wed, 15 Sep 2021 00:35:22 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Wed, 15 Sep 2021 00:35:24 GMT
COPY file:f6b7a1c96cc89593a2b9ce4c68af350ae02f2e0c654cd5e842ff6c03641d470e in /entrypoint.sh 
# Wed, 15 Sep 2021 00:35:24 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Wed, 15 Sep 2021 00:35:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Sep 2021 00:35:25 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d1ef9481330a95ddf334887e1f8fce317a5ac59b648f285f67a4985d219de7`  
		Last Modified: Fri, 27 Aug 2021 23:55:36 GMT  
		Size: 1.6 MB (1564608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05b9b552be19301d7e17adf942310cefe01c3c4c7bfd107dfa0db3768b973a3`  
		Last Modified: Fri, 27 Aug 2021 23:55:35 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1716cacc7a16c9894f45061a30c476d428c6142feadd35c9c6d4f7f6fd3f510`  
		Last Modified: Fri, 27 Aug 2021 23:55:36 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487f25d187ac01de60b09eaff9672b6dee8e00a0af1c2ddd23d63ef80752580e`  
		Last Modified: Fri, 27 Aug 2021 23:59:52 GMT  
		Size: 10.7 MB (10722806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8fe2d3dd4b7a667be4649d9d8764929856ac5b3f602719916314fa0b74bad21`  
		Last Modified: Fri, 27 Aug 2021 23:59:48 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370e8afe5ac74861a4e39005c5c97416700ae0f896b266d3eca8875fd8bb3a26`  
		Last Modified: Fri, 27 Aug 2021 23:59:57 GMT  
		Size: 12.9 MB (12855470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7926a97ef6fdf54d9aae2e7caadfdcd9e6b92fab634582a75f48abd9f6474eb3`  
		Last Modified: Fri, 27 Aug 2021 23:59:48 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a26196a335ebadc9e24979b7326a8f23d4d7207bc59276a267a052b9b5e3208`  
		Last Modified: Fri, 27 Aug 2021 23:59:48 GMT  
		Size: 17.8 KB (17793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf2bd5437d398d567c555428405a1421c8ca6b4f2c496959d9124c36bf9c642`  
		Last Modified: Fri, 27 Aug 2021 23:59:48 GMT  
		Size: 8.6 KB (8570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c66ab2a5cd72dbac943b7b3cdf5993dc7fefb5bfb749cfdb77bf42c3251a951`  
		Last Modified: Tue, 07 Sep 2021 22:08:40 GMT  
		Size: 414.8 KB (414769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4113d9a63287fd4bd2887278e80b62fe2ab6094f5a9bd54dd0bbb2bbd84e8f83`  
		Last Modified: Tue, 07 Sep 2021 22:08:43 GMT  
		Size: 5.8 MB (5770286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bffc01e357bf80f5bb56eb04c1befb54f195344f53802935064c24b7def2d8b7`  
		Last Modified: Wed, 15 Sep 2021 00:47:34 GMT  
		Size: 21.3 MB (21323774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc49e2a9075c859b81e428b74e3e74ce0caee54e565939b8a22bc9fa5985c5d1`  
		Last Modified: Wed, 15 Sep 2021 00:47:16 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67021a233e58b7d05aee1de151c7eb677f15be5ed9296881dc297cef1de4aeb`  
		Last Modified: Wed, 15 Sep 2021 00:47:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:4-php8.0-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull joomla@sha256:b7f70f7077661b54dec5451588d9415b90bdd26174123bfdfe65d17dec02b2c6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57734783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49686c172d78f4497342be87af15e2389f808614513758c8b594633158f68146`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 22:43:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 22:43:11 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 22:43:11 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 22:43:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 22:43:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 22:50:38 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 27 Aug 2021 22:50:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 22:50:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 22:50:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 23:04:33 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 27 Aug 2021 23:04:33 GMT
ENV PHP_VERSION=8.0.10
# Fri, 27 Aug 2021 23:04:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.10.tar.xz.asc
# Fri, 27 Aug 2021 23:04:34 GMT
ENV PHP_SHA256=66dc4d1bc86d9c1bc255b51b79d337ed1a7a035cf71230daabbf9a4ca35795eb
# Fri, 27 Aug 2021 23:04:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 27 Aug 2021 23:04:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Aug 2021 23:09:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Aug 2021 23:09:36 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 27 Aug 2021 23:09:37 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Aug 2021 23:09:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Aug 2021 23:09:37 GMT
WORKDIR /var/www/html
# Fri, 27 Aug 2021 23:09:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 27 Aug 2021 23:09:38 GMT
STOPSIGNAL SIGQUIT
# Fri, 27 Aug 2021 23:09:38 GMT
EXPOSE 9000
# Fri, 27 Aug 2021 23:09:39 GMT
CMD ["php-fpm"]
# Tue, 07 Sep 2021 21:01:12 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 07 Sep 2021 21:01:12 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 07 Sep 2021 21:01:14 GMT
RUN apk add --no-cache 	bash
# Tue, 07 Sep 2021 21:03:03 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		libjpeg-turbo-dev 		libmcrypt-dev 		libmemcached-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		gmp 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.20; 	pecl install mcrypt-1.0.4; 	pecl install memcached-3.1.5; 	pecl install redis-5.3.4; 		docker-php-ext-enable 		apcu 		mcrypt 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		)"; 	apk add --virtual .joomla-phpext-rundeps $runDeps; 	apk del .build-deps
# Tue, 07 Sep 2021 21:03:03 GMT
VOLUME [/var/www/html]
# Tue, 14 Sep 2021 23:57:37 GMT
ENV JOOMLA_VERSION=4.0.3
# Tue, 14 Sep 2021 23:57:37 GMT
ENV JOOMLA_SHA512=9c09a621586fdcc30351a915f283581c92080c210294cacc50e0e390d991f32bee9d61dfc7b0af33c81118e46d775152159c0e27dbf73f5531512328d716901f
# Tue, 14 Sep 2021 23:57:43 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Tue, 14 Sep 2021 23:57:44 GMT
COPY file:f6b7a1c96cc89593a2b9ce4c68af350ae02f2e0c654cd5e842ff6c03641d470e in /entrypoint.sh 
# Tue, 14 Sep 2021 23:57:44 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Tue, 14 Sep 2021 23:57:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Sep 2021 23:57:45 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410af590d902972d54fd8db93bdaafd236bb6773858e586bf13cbc95e9cd9563`  
		Last Modified: Fri, 27 Aug 2021 23:51:45 GMT  
		Size: 1.7 MB (1710508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c7d56ea46820654b5af561547d3440b151e14cd36fae537c2248e21e53d9ee`  
		Last Modified: Fri, 27 Aug 2021 23:51:45 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6246963785833a508c5863759a793f972f8188ca2704935b327db7bc5a29d831`  
		Last Modified: Fri, 27 Aug 2021 23:51:45 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15065b0296916a4c973d246262d7b891dc5e5e0bf333650e174c647fb2f03310`  
		Last Modified: Fri, 27 Aug 2021 23:54:37 GMT  
		Size: 10.7 MB (10722820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7430ca7d1f730ca38ddc823023c7696abf4a868fc5c925373ef083a3555d9df0`  
		Last Modified: Fri, 27 Aug 2021 23:54:34 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be53fb97d5e4a3f82bc220239d096dbfd067769a229bd4c179ee29a3310c3f3d`  
		Last Modified: Fri, 27 Aug 2021 23:54:37 GMT  
		Size: 14.5 MB (14507356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1464948b766ec2a01e5fd9f6f494ff8e960d77e410327491db1cdfe7be53be6d`  
		Last Modified: Fri, 27 Aug 2021 23:54:34 GMT  
		Size: 2.3 KB (2263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7481da9780e005adf979f249042851115b476e6c402de2d57ff4abfcecf59721`  
		Last Modified: Fri, 27 Aug 2021 23:54:34 GMT  
		Size: 17.8 KB (17808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d106f721c4d2a8b7de8833092018f5356a62a5178d301dff6bba917361eed3d`  
		Last Modified: Fri, 27 Aug 2021 23:54:34 GMT  
		Size: 8.6 KB (8570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04fa718f7e0e6eb8b338d64f106e124374961e9f3691986253ca104b44b1dff`  
		Last Modified: Tue, 07 Sep 2021 21:16:05 GMT  
		Size: 473.9 KB (473923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28e9341343a7098a60e67896f0bdd6ba3b62796965f63ae7ae5f2b40a994fbc`  
		Last Modified: Tue, 07 Sep 2021 21:16:06 GMT  
		Size: 6.3 MB (6252174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0694aca95dcaa45aaf699b188be3e90ec6e85b66feed28b9ffe6e8f880127fe7`  
		Last Modified: Wed, 15 Sep 2021 00:04:09 GMT  
		Size: 21.3 MB (21323701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd9a35f13fddc9396576189c4cebdc72f0e4f280b2fc9f035310ee05bfa508f`  
		Last Modified: Wed, 15 Sep 2021 00:04:06 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994231483512d86e14846f047b3d399b04b3177f91571c7d068abb7beb45e3ee`  
		Last Modified: Wed, 15 Sep 2021 00:04:05 GMT  
		Size: 613.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:4-php8.0-fpm-alpine` - linux; 386

```console
$ docker pull joomla@sha256:17fb76e17c944444d7795b6d3f768307edad0243fd29d40e060db9b2708b82c6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59020576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636e7d155676c02037d65782841ce4271c9ab2fc77b41b102ce4e651bdc6c4f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 27 Aug 2021 17:38:29 GMT
ADD file:42a7bc5a08b546b47049dd0f89ae4e7a8c86342f87000f39ade3ff52916a6c2e in / 
# Fri, 27 Aug 2021 17:38:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 19:59:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 19:59:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 19:59:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 19:59:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 19:59:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 20:10:36 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 27 Aug 2021 20:10:37 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 20:10:37 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 20:10:37 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 20:29:52 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 27 Aug 2021 20:29:52 GMT
ENV PHP_VERSION=8.0.10
# Fri, 27 Aug 2021 20:29:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.10.tar.xz.asc
# Fri, 27 Aug 2021 20:29:52 GMT
ENV PHP_SHA256=66dc4d1bc86d9c1bc255b51b79d337ed1a7a035cf71230daabbf9a4ca35795eb
# Fri, 27 Aug 2021 20:29:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 27 Aug 2021 20:30:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Aug 2021 20:37:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Aug 2021 20:37:19 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 27 Aug 2021 20:37:20 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Aug 2021 20:37:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Aug 2021 20:37:21 GMT
WORKDIR /var/www/html
# Fri, 27 Aug 2021 20:37:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 27 Aug 2021 20:37:22 GMT
STOPSIGNAL SIGQUIT
# Fri, 27 Aug 2021 20:37:22 GMT
EXPOSE 9000
# Fri, 27 Aug 2021 20:37:22 GMT
CMD ["php-fpm"]
# Tue, 07 Sep 2021 20:50:41 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 07 Sep 2021 20:50:41 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 07 Sep 2021 20:50:43 GMT
RUN apk add --no-cache 	bash
# Tue, 07 Sep 2021 20:52:28 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		libjpeg-turbo-dev 		libmcrypt-dev 		libmemcached-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		gmp 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.20; 	pecl install mcrypt-1.0.4; 	pecl install memcached-3.1.5; 	pecl install redis-5.3.4; 		docker-php-ext-enable 		apcu 		mcrypt 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		)"; 	apk add --virtual .joomla-phpext-rundeps $runDeps; 	apk del .build-deps
# Tue, 07 Sep 2021 20:52:28 GMT
VOLUME [/var/www/html]
# Tue, 14 Sep 2021 23:45:28 GMT
ENV JOOMLA_VERSION=4.0.3
# Tue, 14 Sep 2021 23:45:29 GMT
ENV JOOMLA_SHA512=9c09a621586fdcc30351a915f283581c92080c210294cacc50e0e390d991f32bee9d61dfc7b0af33c81118e46d775152159c0e27dbf73f5531512328d716901f
# Tue, 14 Sep 2021 23:45:36 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Tue, 14 Sep 2021 23:45:37 GMT
COPY file:f6b7a1c96cc89593a2b9ce4c68af350ae02f2e0c654cd5e842ff6c03641d470e in /entrypoint.sh 
# Tue, 14 Sep 2021 23:45:37 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Tue, 14 Sep 2021 23:45:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Sep 2021 23:45:38 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b11ae9fc5d8a106cfed3a6f6c75e5b5b5797c566fac4411622b4055df6541286`  
		Last Modified: Fri, 27 Aug 2021 17:39:18 GMT  
		Size: 2.8 MB (2822857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa6b193871895593dd2e9300b768212b024272930161ab8524f40a5735edd63`  
		Last Modified: Fri, 27 Aug 2021 21:44:10 GMT  
		Size: 1.8 MB (1805371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f324621ef2d45fa9d97583b1efc3fb241066b4dbf696e2dd38327a90d1e6813`  
		Last Modified: Fri, 27 Aug 2021 21:44:09 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d22e796392b3e282fea08fa6cb0da352053587b646a938425cb7c4171bf25a2`  
		Last Modified: Fri, 27 Aug 2021 21:44:09 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1f0691b35abc3e1cc0a213f15db883a1934075fe48465c1b96a18f72d39dd7`  
		Last Modified: Fri, 27 Aug 2021 21:48:09 GMT  
		Size: 10.7 MB (10722798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3f90f20de6e799b57fb3490bcee5db23cbf37ce1479f0856171f38597e839c`  
		Last Modified: Fri, 27 Aug 2021 21:48:05 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc166f47eddc24897eae8f431522de273f8bc62f88565ccd6defd1276fc54adb`  
		Last Modified: Fri, 27 Aug 2021 21:48:10 GMT  
		Size: 15.4 MB (15428112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4bfb05604335668ab061d83b90fb7fefbb43a939e2b6e1a1911f57ed336cede`  
		Last Modified: Fri, 27 Aug 2021 21:48:05 GMT  
		Size: 2.3 KB (2269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072c39e7c5738ea8f19930d2c98a7a91c1666468b5be8618e6db3ea5fd7e66aa`  
		Last Modified: Fri, 27 Aug 2021 21:48:05 GMT  
		Size: 17.8 KB (17794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e14b0de3b7bd0bda154b235d679b4ee43957d5971cf4a561e4a3ec52a88eec`  
		Last Modified: Fri, 27 Aug 2021 21:48:05 GMT  
		Size: 8.6 KB (8570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3b32a254666f0e061b97c9591bb2437b4d5325c1e723b046522800561c3193`  
		Last Modified: Tue, 07 Sep 2021 21:04:59 GMT  
		Size: 501.7 KB (501672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6742c4bad347ece7331efc5bb9991de149e6697295f0d95d43ff0553cb0022ad`  
		Last Modified: Tue, 07 Sep 2021 21:04:59 GMT  
		Size: 6.4 MB (6383503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0931432658a4fd2180917a5d61fc463e4ea8f3d861c56dafc9cfaf9db14259e`  
		Last Modified: Tue, 14 Sep 2021 23:54:27 GMT  
		Size: 21.3 MB (21323797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d074d35af07b707881f819c8152f229d45624419b4d09273b72e59899a42c5`  
		Last Modified: Tue, 14 Sep 2021 23:54:22 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8c2ecc813d93f0115f3e12516e5b841e019dfb093ae274513b7c70e3cab69a`  
		Last Modified: Tue, 14 Sep 2021 23:54:22 GMT  
		Size: 613.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:4-php8.0-fpm-alpine` - linux; ppc64le

```console
$ docker pull joomla@sha256:7aa16efaa73f9da656824db422193a7c9559c8ca28ea2e237cbb00b11cead3ba
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59440348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686f867ab01300177e49f6e2b597f0ba2abe50f8a81a1d94fe34ff66c16ac1fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 27 Aug 2021 19:39:54 GMT
ADD file:d213c56ffc24a5051e8060fd0fec1a0520367c10d88ab16321c36336b6c66098 in / 
# Fri, 27 Aug 2021 19:39:59 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 00:22:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 28 Aug 2021 00:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 28 Aug 2021 00:22:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 28 Aug 2021 00:22:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Aug 2021 00:22:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Aug 2021 00:29:16 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 28 Aug 2021 00:29:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Aug 2021 00:29:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Aug 2021 00:29:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 28 Aug 2021 00:43:26 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Sat, 28 Aug 2021 00:43:32 GMT
ENV PHP_VERSION=8.0.10
# Sat, 28 Aug 2021 00:43:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.10.tar.xz.asc
# Sat, 28 Aug 2021 00:43:45 GMT
ENV PHP_SHA256=66dc4d1bc86d9c1bc255b51b79d337ed1a7a035cf71230daabbf9a4ca35795eb
# Sat, 28 Aug 2021 00:44:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 28 Aug 2021 00:44:07 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 28 Aug 2021 00:49:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 28 Aug 2021 00:49:11 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Sat, 28 Aug 2021 00:49:25 GMT
RUN docker-php-ext-enable sodium
# Sat, 28 Aug 2021 00:49:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 28 Aug 2021 00:49:37 GMT
WORKDIR /var/www/html
# Sat, 28 Aug 2021 00:50:00 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Sat, 28 Aug 2021 00:50:03 GMT
STOPSIGNAL SIGQUIT
# Sat, 28 Aug 2021 00:50:05 GMT
EXPOSE 9000
# Sat, 28 Aug 2021 00:50:09 GMT
CMD ["php-fpm"]
# Tue, 07 Sep 2021 21:52:50 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 07 Sep 2021 21:52:52 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 07 Sep 2021 21:53:06 GMT
RUN apk add --no-cache 	bash
# Tue, 07 Sep 2021 21:55:50 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		libjpeg-turbo-dev 		libmcrypt-dev 		libmemcached-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		gmp 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.20; 	pecl install mcrypt-1.0.4; 	pecl install memcached-3.1.5; 	pecl install redis-5.3.4; 		docker-php-ext-enable 		apcu 		mcrypt 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		)"; 	apk add --virtual .joomla-phpext-rundeps $runDeps; 	apk del .build-deps
# Tue, 07 Sep 2021 21:55:58 GMT
VOLUME [/var/www/html]
# Wed, 15 Sep 2021 00:56:12 GMT
ENV JOOMLA_VERSION=4.0.3
# Wed, 15 Sep 2021 00:56:18 GMT
ENV JOOMLA_SHA512=9c09a621586fdcc30351a915f283581c92080c210294cacc50e0e390d991f32bee9d61dfc7b0af33c81118e46d775152159c0e27dbf73f5531512328d716901f
# Wed, 15 Sep 2021 00:56:47 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Wed, 15 Sep 2021 00:56:56 GMT
COPY file:f6b7a1c96cc89593a2b9ce4c68af350ae02f2e0c654cd5e842ff6c03641d470e in /entrypoint.sh 
# Wed, 15 Sep 2021 00:56:58 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Wed, 15 Sep 2021 00:57:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Sep 2021 00:57:07 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:63da8ca98f7b4b94381aed56862a60aecf355d9428b9aeb7c61d5bd017100c18`  
		Last Modified: Fri, 27 Aug 2021 19:41:06 GMT  
		Size: 2.8 MB (2812284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317a4af98e0d6a07fca505c073eaef771202280f717e9eec5693da72e342352b`  
		Last Modified: Sat, 28 Aug 2021 01:41:31 GMT  
		Size: 1.8 MB (1753694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f45086a93088805a1f9f81303c856d62fa5a43ec294f558743c42e803fa376`  
		Last Modified: Sat, 28 Aug 2021 01:41:31 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bbbefa425da2cee0e640dda470f0cb14892652fd6f89c03319eff15fdf1720`  
		Last Modified: Sat, 28 Aug 2021 01:41:31 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de083d77cd88d681040f0da5c1cb14af9c0c04a74452245f63b9fbb92edd2a38`  
		Last Modified: Sat, 28 Aug 2021 01:44:12 GMT  
		Size: 10.7 MB (10722814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9a872bc4ccfa0a73548f6313be2b6650f59fb5ae12fcf516fcfb2502ef4ab2`  
		Last Modified: Sat, 28 Aug 2021 01:44:07 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9829f4fc1affce40f275beef4cf7ec87818b908e64b9af2f7e870a026b5042a`  
		Last Modified: Sat, 28 Aug 2021 01:44:11 GMT  
		Size: 15.8 MB (15818748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b307fdd690faecbd791a1557b87fdd97b65f0fb5b1559c0fec4b44553a4fb233`  
		Last Modified: Sat, 28 Aug 2021 01:44:07 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a06506c576638c1790d94ad8d9187f6aa494c68f3252017b4e48d4063b5497c9`  
		Last Modified: Sat, 28 Aug 2021 01:44:07 GMT  
		Size: 17.8 KB (17809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ea982b4cebb191cc0624d7dce566931e7662ee8a2832c3244965972c22b6cb`  
		Last Modified: Sat, 28 Aug 2021 01:44:07 GMT  
		Size: 8.6 KB (8573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0108ea2d6e541222f7ee8559eff7ffcd429cf70172d1eba1169a9298a707615b`  
		Last Modified: Tue, 07 Sep 2021 22:23:40 GMT  
		Size: 529.7 KB (529675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4923ba9e39a026475d9339ab4c95d1d4c77088c3d04ed8d6e371aded55c928e3`  
		Last Modified: Tue, 07 Sep 2021 22:23:41 GMT  
		Size: 6.4 MB (6446930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4083f21c30ca8258e83a324733cd2a6973cc48b4e0e65a156018e044edeae906`  
		Last Modified: Wed, 15 Sep 2021 01:10:49 GMT  
		Size: 21.3 MB (21323712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e0ce1d5134a9fd235a7cfd0080f984e3affd2e5dfab8b830f4f09d92b25d0a`  
		Last Modified: Wed, 15 Sep 2021 01:10:44 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f77a460cde0d1a41e7573599b630a4a1977adc54ba692ad70fe55ff63ab70421`  
		Last Modified: Wed, 15 Sep 2021 01:10:44 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:4-php8.0-fpm-alpine` - linux; s390x

```console
$ docker pull joomla@sha256:8d9ce328cf9a7b477002e838dc49d005ddaf438ba63f87808999d0fe3d31c56e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (56986038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e035d7ec647820debd1bf816f6088960cea5d7cb2c3eec28caf52f3a760d1e50`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 27 Aug 2021 17:41:29 GMT
ADD file:9b40ee281e8797067fb2ae207c406084cb81593090338a8b7cb09ade52168daa in / 
# Fri, 27 Aug 2021 17:41:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 19:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 19:39:17 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 19:39:19 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 19:39:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 19:39:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 19:45:13 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 27 Aug 2021 19:45:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 19:45:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 19:45:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 19:58:05 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 27 Aug 2021 19:58:05 GMT
ENV PHP_VERSION=8.0.10
# Fri, 27 Aug 2021 19:58:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.10.tar.xz.asc
# Fri, 27 Aug 2021 19:58:06 GMT
ENV PHP_SHA256=66dc4d1bc86d9c1bc255b51b79d337ed1a7a035cf71230daabbf9a4ca35795eb
# Fri, 27 Aug 2021 19:58:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 27 Aug 2021 19:58:19 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Aug 2021 20:03:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Aug 2021 20:03:58 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 27 Aug 2021 20:04:00 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Aug 2021 20:04:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Aug 2021 20:04:01 GMT
WORKDIR /var/www/html
# Fri, 27 Aug 2021 20:04:02 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 27 Aug 2021 20:04:02 GMT
STOPSIGNAL SIGQUIT
# Fri, 27 Aug 2021 20:04:03 GMT
EXPOSE 9000
# Fri, 27 Aug 2021 20:04:03 GMT
CMD ["php-fpm"]
# Tue, 07 Sep 2021 21:03:32 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 07 Sep 2021 21:03:32 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 07 Sep 2021 21:03:34 GMT
RUN apk add --no-cache 	bash
# Tue, 07 Sep 2021 21:06:03 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		libjpeg-turbo-dev 		libmcrypt-dev 		libmemcached-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		gmp 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.20; 	pecl install mcrypt-1.0.4; 	pecl install memcached-3.1.5; 	pecl install redis-5.3.4; 		docker-php-ext-enable 		apcu 		mcrypt 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		)"; 	apk add --virtual .joomla-phpext-rundeps $runDeps; 	apk del .build-deps
# Tue, 07 Sep 2021 21:06:04 GMT
VOLUME [/var/www/html]
# Tue, 14 Sep 2021 23:50:55 GMT
ENV JOOMLA_VERSION=4.0.3
# Tue, 14 Sep 2021 23:50:55 GMT
ENV JOOMLA_SHA512=9c09a621586fdcc30351a915f283581c92080c210294cacc50e0e390d991f32bee9d61dfc7b0af33c81118e46d775152159c0e27dbf73f5531512328d716901f
# Tue, 14 Sep 2021 23:51:01 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Tue, 14 Sep 2021 23:51:03 GMT
COPY file:f6b7a1c96cc89593a2b9ce4c68af350ae02f2e0c654cd5e842ff6c03641d470e in /entrypoint.sh 
# Tue, 14 Sep 2021 23:51:04 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Tue, 14 Sep 2021 23:51:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Sep 2021 23:51:04 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:da14cb6b6dc946dbb2d84386bcaca84e2d46f650767cd11bdb3331ec9d623988`  
		Last Modified: Fri, 27 Aug 2021 17:42:25 GMT  
		Size: 2.6 MB (2603464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ad9a79bad26bb06d3574174d09fe708da08d7c89009c1af214a9c824e97007`  
		Last Modified: Fri, 27 Aug 2021 20:52:39 GMT  
		Size: 1.8 MB (1768214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b673ca8861cb9f3ee8bc162276486c2037e038a90f72a7d1604e8df25f6c10d7`  
		Last Modified: Fri, 27 Aug 2021 20:52:39 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b1a84628a9effaa859862a214dd288520209fad79d46dc04e5559d3853ceea`  
		Last Modified: Fri, 27 Aug 2021 20:52:39 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c17b948cbbc3f223ecf32c5f12bdbf73cd46d987170a61a7367511a8616a91a2`  
		Last Modified: Fri, 27 Aug 2021 20:55:38 GMT  
		Size: 10.7 MB (10722813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f202a8bd124d98ae68ab144d587396d0555ec9f1a3171c6e6461db4f2d9266f9`  
		Last Modified: Fri, 27 Aug 2021 20:55:35 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e065a8551ef98efe77581df70de3e7d2ae4766a4f2e5a6e75b3f7f571d13863d`  
		Last Modified: Fri, 27 Aug 2021 20:55:38 GMT  
		Size: 14.1 MB (14103239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa745c0ac0029250287bfbe8c1a155755df87eca5b54a1d11ec366a675987de`  
		Last Modified: Fri, 27 Aug 2021 20:55:35 GMT  
		Size: 2.3 KB (2265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2275ed4d6bb0530b4cdcdfb17bacef907929f685c181b93191727c6f80dc428`  
		Last Modified: Fri, 27 Aug 2021 20:55:35 GMT  
		Size: 17.8 KB (17820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7682e4814e97645934891865c97817077703bee439797cdae5a7c95b8f7e827`  
		Last Modified: Fri, 27 Aug 2021 20:55:35 GMT  
		Size: 8.6 KB (8571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652c76f9cdfbb1a58eb5d8870ca18a5c51529bc902df3653fd47a5ce05b96f46`  
		Last Modified: Tue, 07 Sep 2021 21:22:33 GMT  
		Size: 482.7 KB (482731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c702d305cd28f609eefff6a42e628c9773d20346aeb460fa8d28502228646b`  
		Last Modified: Tue, 07 Sep 2021 21:22:34 GMT  
		Size: 5.9 MB (5949418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761303c942328ae8e33fe8eae09670d5c8a03cf1a26b20328525898b77d753ef`  
		Last Modified: Tue, 14 Sep 2021 23:56:14 GMT  
		Size: 21.3 MB (21323673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428c675bfc49d7c7093423e703ebf45a7329aa4f0625515594357e2decd89845`  
		Last Modified: Tue, 14 Sep 2021 23:56:11 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f061133fe846d52ecee868b70bec7cb1da23df908d7919079228bb2badd06e1e`  
		Last Modified: Tue, 14 Sep 2021 23:56:11 GMT  
		Size: 613.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
