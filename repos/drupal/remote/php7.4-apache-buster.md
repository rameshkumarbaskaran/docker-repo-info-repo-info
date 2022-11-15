## `drupal:php7.4-apache-buster`

```console
$ docker pull drupal@sha256:d78193c8573ff791a6db4bb93f7a319f59271fc89eb5cd765f93beb1365c60f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `drupal:php7.4-apache-buster` - linux; amd64

```console
$ docker pull drupal@sha256:8d984bf40c417f2597101a46a79c8bbc2ac9828d295e053461f33d34ca58bf7a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.9 MB (167928358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39177555bc2bf4543a26e3a0870b7f49d2a3170aa4822f0bf7c5b8f28c5be07d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 15 Nov 2022 04:05:14 GMT
ADD file:9461639b945ced6fb6164491a7e0131261a1b7d69264cce516e75c71e4df22d2 in / 
# Tue, 15 Nov 2022 04:05:14 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 04:26:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 15 Nov 2022 04:26:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 15 Nov 2022 04:27:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 04:27:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 15 Nov 2022 04:27:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 15 Nov 2022 04:30:41 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 15 Nov 2022 04:30:41 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 15 Nov 2022 04:30:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 15 Nov 2022 04:30:51 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 15 Nov 2022 04:30:51 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 15 Nov 2022 04:30:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 15 Nov 2022 04:30:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 15 Nov 2022 04:30:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 15 Nov 2022 06:11:04 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 15 Nov 2022 06:11:04 GMT
ENV PHP_VERSION=7.4.33
# Tue, 15 Nov 2022 06:11:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.33.tar.xz.asc
# Tue, 15 Nov 2022 06:11:04 GMT
ENV PHP_SHA256=924846abf93bc613815c55dd3f5809377813ac62a9ec4eb3778675b82a27b927
# Tue, 15 Nov 2022 06:11:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 15 Nov 2022 06:11:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 15 Nov 2022 06:13:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 15 Nov 2022 06:13:11 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 15 Nov 2022 06:13:12 GMT
RUN docker-php-ext-enable sodium
# Tue, 15 Nov 2022 06:13:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 15 Nov 2022 06:13:12 GMT
STOPSIGNAL SIGWINCH
# Tue, 15 Nov 2022 06:13:12 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 15 Nov 2022 06:13:12 GMT
WORKDIR /var/www/html
# Tue, 15 Nov 2022 06:13:12 GMT
EXPOSE 80
# Tue, 15 Nov 2022 06:13:12 GMT
CMD ["apache2-foreground"]
# Tue, 15 Nov 2022 08:25:14 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 08:25:15 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 15 Nov 2022 08:25:15 GMT
COPY file:e2da1c2113094da76d330eef39e0e1916af11394dff778e02af557c116266d7c in /usr/local/bin/ 
# Tue, 15 Nov 2022 08:25:15 GMT
ENV DRUPAL_VERSION=9.4.8
# Tue, 15 Nov 2022 08:25:15 GMT
WORKDIR /opt/drupal
# Tue, 15 Nov 2022 08:25:26 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Tue, 15 Nov 2022 08:25:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:32820e52a00eb22dc76d70d992be7082cd24b636cfb597ff3951d29a821b46b9`  
		Last Modified: Tue, 15 Nov 2022 04:09:26 GMT  
		Size: 27.1 MB (27140332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a022f9f4db63bdf619d892ab06b0861dc6b1b17b3a137c35093f0937aa7e57`  
		Last Modified: Tue, 15 Nov 2022 06:24:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff96ba8ea962f6736c4fa62505f2aa4b5405f5388b5424727cd3af64cb7cf44`  
		Last Modified: Tue, 15 Nov 2022 06:25:00 GMT  
		Size: 76.7 MB (76687327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b28c78a7e238dc26ddcd2d9ea3c2512abab7fb02db8f343763046433d33bc9c`  
		Last Modified: Tue, 15 Nov 2022 06:24:48 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c6c4ace6279a87de82880fb1e218025922a28cf5d96174cdaaf60662395f839`  
		Last Modified: Tue, 15 Nov 2022 06:25:21 GMT  
		Size: 18.7 MB (18684868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c02c5e391e989a090f207fa47f38b8c603b1cc5711e47164ec7dc65df096d1e`  
		Last Modified: Tue, 15 Nov 2022 06:25:16 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3334e90311c0d3629f199c090647e052dbe1f1da4633eaaa985a43027da56582`  
		Last Modified: Tue, 15 Nov 2022 06:25:16 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc1233d55eb702f6e3ae5d80d4dac0be3b80196d095fd6e6bdbf7538f24e717`  
		Last Modified: Tue, 15 Nov 2022 06:36:57 GMT  
		Size: 10.8 MB (10758595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346ff24d3a614a8eb6c6032ec6d23c0397392aa07d2ddbbc5b8955522392589d`  
		Last Modified: Tue, 15 Nov 2022 06:36:54 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2739aec943e733d8ef08ddec34b382684c1b525368c750386282b876ad4f989e`  
		Last Modified: Tue, 15 Nov 2022 06:36:56 GMT  
		Size: 10.2 MB (10157059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3671c31988c18653265775bd4605d2d96a31c7e4062ffc1d12b13150ae6c8a1`  
		Last Modified: Tue, 15 Nov 2022 06:36:54 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a677e48605f004a64c60c5778b4e4cbc6f9ac0a82f279b5bf60215144d89fd1`  
		Last Modified: Tue, 15 Nov 2022 06:36:54 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f32c69ecfbf74f3cbb52f6e7baf33035731059a754eb8e09b5ab150f16b189e`  
		Last Modified: Tue, 15 Nov 2022 06:36:54 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8e0cb3b2604fef27eb89a856f675966335fe2b12901a143e5661f6a40726c0`  
		Last Modified: Tue, 15 Nov 2022 08:45:07 GMT  
		Size: 1.9 MB (1901093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d868fecdcb810a209feed4b37325a8c0117d0d41e956004eb6ce9f8ffc8f45`  
		Last Modified: Tue, 15 Nov 2022 08:45:06 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ee98e9aeba34d5807a0940a27c6d652f79d80296456467441c9e9804fb5991`  
		Last Modified: Tue, 15 Nov 2022 08:45:06 GMT  
		Size: 695.2 KB (695191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565146fdfd83a81e12f025e070631243bb82c53d95c674d740f8bee663496a4f`  
		Last Modified: Tue, 15 Nov 2022 08:45:06 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d468f794d7e2b00d52955b8d4a5c1f3704536c0cdd2d691bb6dee9fa90b96ef`  
		Last Modified: Tue, 15 Nov 2022 08:45:11 GMT  
		Size: 21.9 MB (21897848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:php7.4-apache-buster` - linux; arm variant v7

```console
$ docker pull drupal@sha256:d912a8ab3369bb6f47a06a6fa9ee37ceaf901533bc09434868d4867897dd7692
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143783567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0d98e3508235cc6014cc6b4d6a9b0e75f0f9c0d84c5893ce6d13fb29d10fde`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 15 Nov 2022 03:43:57 GMT
ADD file:02e51e32df426f4ee14093de5240d396191761b03f60af08b7e920c86c3df725 in / 
# Tue, 15 Nov 2022 03:43:57 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 04:07:37 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 15 Nov 2022 04:07:37 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 15 Nov 2022 04:07:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 04:07:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 15 Nov 2022 04:07:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 15 Nov 2022 04:10:50 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 15 Nov 2022 04:10:50 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 15 Nov 2022 04:11:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 15 Nov 2022 04:11:01 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 15 Nov 2022 04:11:02 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 15 Nov 2022 04:11:02 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 15 Nov 2022 04:11:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 15 Nov 2022 04:11:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 15 Nov 2022 05:42:47 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 15 Nov 2022 05:42:48 GMT
ENV PHP_VERSION=7.4.33
# Tue, 15 Nov 2022 05:42:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.33.tar.xz.asc
# Tue, 15 Nov 2022 05:42:48 GMT
ENV PHP_SHA256=924846abf93bc613815c55dd3f5809377813ac62a9ec4eb3778675b82a27b927
# Tue, 15 Nov 2022 05:43:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 15 Nov 2022 05:43:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 15 Nov 2022 05:44:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 15 Nov 2022 05:44:56 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 15 Nov 2022 05:44:57 GMT
RUN docker-php-ext-enable sodium
# Tue, 15 Nov 2022 05:44:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 15 Nov 2022 05:44:57 GMT
STOPSIGNAL SIGWINCH
# Tue, 15 Nov 2022 05:44:57 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 15 Nov 2022 05:44:57 GMT
WORKDIR /var/www/html
# Tue, 15 Nov 2022 05:44:57 GMT
EXPOSE 80
# Tue, 15 Nov 2022 05:44:57 GMT
CMD ["apache2-foreground"]
# Tue, 15 Nov 2022 07:58:45 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 07:58:46 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 15 Nov 2022 07:58:46 GMT
COPY file:e2da1c2113094da76d330eef39e0e1916af11394dff778e02af557c116266d7c in /usr/local/bin/ 
# Tue, 15 Nov 2022 07:58:46 GMT
ENV DRUPAL_VERSION=9.4.8
# Tue, 15 Nov 2022 07:58:46 GMT
WORKDIR /opt/drupal
# Tue, 15 Nov 2022 07:59:14 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Tue, 15 Nov 2022 07:59:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:e14edb06ef42285b9a4c82509f85d76caeb037799d6631d8d272f86af363a045`  
		Last Modified: Tue, 15 Nov 2022 03:51:01 GMT  
		Size: 22.7 MB (22748928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a744950c0c95ea35eac5bd289ec7493aa3d866cb171b0b7b2617100323dafddd`  
		Last Modified: Tue, 15 Nov 2022 06:06:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a0c468d8145d2641efffc44b06bbdbbcb730f11fcc94864e28dcc5ab9d69f2`  
		Last Modified: Tue, 15 Nov 2022 06:06:56 GMT  
		Size: 59.5 MB (59542292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cf3287317716a59fab00c89f0f363fdfab61ba1aa6ec645c3ec4b50c904401`  
		Last Modified: Tue, 15 Nov 2022 06:06:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910ed8a0f9ab85aa53bb3a463ce1595df97aa1dfaf69371336fce0f357a95fad`  
		Last Modified: Tue, 15 Nov 2022 06:07:29 GMT  
		Size: 17.5 MB (17481439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fae8520fc548030078cec2ed4915cdae2f8854221f28824a820d5269ed90a7e`  
		Last Modified: Tue, 15 Nov 2022 06:07:26 GMT  
		Size: 433.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525fdb1b4933aad49c00994faa7e2e7b9b0ed5be662da530c97c843dccf65160`  
		Last Modified: Tue, 15 Nov 2022 06:07:26 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eff50c1354a3e4a4aa57ca66fdd0c7ecdd935c3c854c75c9a1045d45b83d8d2`  
		Last Modified: Tue, 15 Nov 2022 06:22:53 GMT  
		Size: 10.8 MB (10756780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0330292c251ad43c3dfe1874e3bde8af230c3128bd9e1522dd342eafd4ee470a`  
		Last Modified: Tue, 15 Nov 2022 06:22:50 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f55691c15f41256ff8528fb35a3a855d642ac3135e07a6c1f6455005f4a277`  
		Last Modified: Tue, 15 Nov 2022 06:22:52 GMT  
		Size: 9.0 MB (9038636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4392f9e67f2380f2b65671b9d54035401780e683990312a89d67ff94f5e756e7`  
		Last Modified: Tue, 15 Nov 2022 06:22:50 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c556306874320e319a79f784e320d194eb74b5105afe4e12a0576be2105bdb49`  
		Last Modified: Tue, 15 Nov 2022 06:22:50 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55808613cd6781101bde59198bb4fbf52f622873fb3bb8f8a89034c264ce7485`  
		Last Modified: Tue, 15 Nov 2022 06:22:50 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8021291107bf880ce61581d7740eec0335e784dfbdb509579bf97dc0f21aa8d`  
		Last Modified: Tue, 15 Nov 2022 08:36:56 GMT  
		Size: 1.6 MB (1616651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8aa2968aca959ff7dafcc2f5b0ec6d8f6e0792b257675f60a96b2cda1319a8`  
		Last Modified: Tue, 15 Nov 2022 08:36:56 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a23170c5a312f45eb58dbfab1b485734826d9eed3991bd0e6b27694f5cd9806`  
		Last Modified: Tue, 15 Nov 2022 08:36:56 GMT  
		Size: 695.2 KB (695198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4077af694dc5f7de886b81a3ec3a2bcad6a6b82737da71af69b2ef0c77e68699`  
		Last Modified: Tue, 15 Nov 2022 08:36:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4c2ed6b981f143b5f2787a24be2138f926bf67a2121bbef3aa5f77b1c72ae6`  
		Last Modified: Tue, 15 Nov 2022 08:37:04 GMT  
		Size: 21.9 MB (21897739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:php7.4-apache-buster` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:62300e7556d225a35df646d522ddf89cc855d721aa0cee30f834c98def92b01a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.4 MB (161387827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73e9783506829de332b968c2413d3c1a1cf702526891aa7c69ae469e18c601f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:13 GMT
ADD file:342233874a06722375663380e7e3a04502a995dfbbc425cd1913f10e96a50dcb in / 
# Tue, 25 Oct 2022 05:46:14 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 16:12:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 25 Oct 2022 16:12:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 25 Oct 2022 16:12:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 16:12:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 25 Oct 2022 16:12:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 25 Oct 2022 16:16:00 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 25 Oct 2022 16:16:01 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 25 Oct 2022 16:16:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 25 Oct 2022 16:16:11 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 25 Oct 2022 16:16:11 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 25 Oct 2022 16:16:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Oct 2022 16:16:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Oct 2022 16:16:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 25 Oct 2022 19:11:17 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 03 Nov 2022 16:51:12 GMT
ENV PHP_VERSION=7.4.33
# Thu, 03 Nov 2022 16:51:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.33.tar.xz.asc
# Thu, 03 Nov 2022 16:51:13 GMT
ENV PHP_SHA256=924846abf93bc613815c55dd3f5809377813ac62a9ec4eb3778675b82a27b927
# Thu, 03 Nov 2022 16:51:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 03 Nov 2022 16:51:23 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 03 Nov 2022 16:52:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 03 Nov 2022 16:52:50 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 03 Nov 2022 16:52:50 GMT
RUN docker-php-ext-enable sodium
# Thu, 03 Nov 2022 16:52:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Nov 2022 16:52:51 GMT
STOPSIGNAL SIGWINCH
# Thu, 03 Nov 2022 16:52:51 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 03 Nov 2022 16:52:51 GMT
WORKDIR /var/www/html
# Thu, 03 Nov 2022 16:52:51 GMT
EXPOSE 80
# Thu, 03 Nov 2022 16:52:51 GMT
CMD ["apache2-foreground"]
# Thu, 03 Nov 2022 18:41:53 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Nov 2022 18:41:53 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 03 Nov 2022 18:41:53 GMT
COPY file:e2da1c2113094da76d330eef39e0e1916af11394dff778e02af557c116266d7c in /usr/local/bin/ 
# Thu, 03 Nov 2022 18:41:53 GMT
ENV DRUPAL_VERSION=9.4.8
# Thu, 03 Nov 2022 18:41:53 GMT
WORKDIR /opt/drupal
# Thu, 03 Nov 2022 18:42:23 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Thu, 03 Nov 2022 18:42:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:5f30c56efde95016859c51bdc10e665dd57dc3c8d22e7abbf384ae9722dfa19e`  
		Last Modified: Tue, 25 Oct 2022 05:49:47 GMT  
		Size: 25.9 MB (25914885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db72537674c01746e8cfe0de3e33e690ea7b2ae6fa309c2ffa58dee432a2bceb`  
		Last Modified: Tue, 25 Oct 2022 19:40:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7b984e345891e702f79e87a64afcb69f5638c39f8c4b4ab7a47ef6b684ade7`  
		Last Modified: Tue, 25 Oct 2022 19:40:27 GMT  
		Size: 70.4 MB (70363634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69589caadcdad7bc8722fad7dc9dc935cc8c3ef7d482ca924922ee280d6fb06d`  
		Last Modified: Tue, 25 Oct 2022 19:40:19 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f30c34bb868e79def32132e1af63dcc95297810349e2fb2ecc147924089501c`  
		Last Modified: Tue, 25 Oct 2022 19:40:48 GMT  
		Size: 18.6 MB (18583655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0bd3642839a18503f373dfa482936f015eb7467f1199aca6a1631d7d37116c`  
		Last Modified: Tue, 25 Oct 2022 19:40:45 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4213b9b6d7a9cc8a47a69b38cd848e9f5c84becd2e2d88c400a5ce708932c8`  
		Last Modified: Tue, 25 Oct 2022 19:40:45 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c95dd449de04044611616dd05b0ad538879f93bd8befb3e750d683ff3eba450`  
		Last Modified: Thu, 03 Nov 2022 17:21:31 GMT  
		Size: 10.8 MB (10757488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08cbe687584b1ab5756f81dc1f333edd47acc044a2c68c899c90a41659c5153e`  
		Last Modified: Thu, 03 Nov 2022 17:21:28 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510862346151bf215401c127c616007ad8803271d318ddb07e8d62a6b2db2e70`  
		Last Modified: Thu, 03 Nov 2022 17:21:29 GMT  
		Size: 11.3 MB (11287119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb10cd12fb83fac1bf85ee6f93ac3394dbaf8513fb2e656bc20e681ad2f83373`  
		Last Modified: Thu, 03 Nov 2022 17:21:28 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6d28b1ab3133ede319b24e1a7531240b8adddfae5c9ddc42c2781bdb31d238`  
		Last Modified: Thu, 03 Nov 2022 17:21:28 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c842c82776af2e23f1a4b2374a2743dc67426b5592b06bcc9faa8880ba8e7c3a`  
		Last Modified: Thu, 03 Nov 2022 17:21:28 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8995dff2f46bc91104b223dbc6aa7c0ee981d78b3a2a235ef3b7f68af25f8659`  
		Last Modified: Thu, 03 Nov 2022 18:56:11 GMT  
		Size: 1.9 MB (1882162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1dc27bcd905fd26a9d7de5a15a9188f9c742259217f900b0970e296dbaf82d6`  
		Last Modified: Thu, 03 Nov 2022 18:56:11 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6822dccd9a9aa5f40734663cf2568288da2bb0723d1d7acc4617814b857660bc`  
		Last Modified: Thu, 03 Nov 2022 18:56:11 GMT  
		Size: 695.2 KB (695190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54c608c972ab1e502988c25005c511772c0d97ff1f235feb172bebddfd65c53`  
		Last Modified: Thu, 03 Nov 2022 18:56:10 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3193299b97f7400a6086b16f18f6dbc44afbb05372aed62a9972efbbeb6b59`  
		Last Modified: Thu, 03 Nov 2022 18:56:14 GMT  
		Size: 21.9 MB (21897654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:php7.4-apache-buster` - linux; 386

```console
$ docker pull drupal@sha256:ca58eafdfde107df0c4f7e5334f239894ea923ac4cd6ba0457f59f4d98b5b8a3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174680044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e07322d480cc4af761a38d3d0360f655fba8d34f6668e23d281eaf32708a36`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 25 Oct 2022 02:23:02 GMT
ADD file:49981fa4bc36bce6e4fdd74b2c4429cc4faef5498c3d8fb20fb98b426bbf8c4d in / 
# Tue, 25 Oct 2022 02:23:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:56:19 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 25 Oct 2022 07:56:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 25 Oct 2022 07:56:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:56:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 25 Oct 2022 07:56:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 25 Oct 2022 08:00:01 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 25 Oct 2022 08:00:02 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 25 Oct 2022 08:00:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 25 Oct 2022 08:00:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 25 Oct 2022 08:00:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 25 Oct 2022 08:00:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Oct 2022 08:00:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Oct 2022 08:00:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 25 Oct 2022 09:37:08 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 03 Nov 2022 16:54:32 GMT
ENV PHP_VERSION=7.4.33
# Thu, 03 Nov 2022 16:54:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.33.tar.xz.asc
# Thu, 03 Nov 2022 16:54:34 GMT
ENV PHP_SHA256=924846abf93bc613815c55dd3f5809377813ac62a9ec4eb3778675b82a27b927
# Thu, 03 Nov 2022 16:54:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 03 Nov 2022 16:54:47 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 03 Nov 2022 16:56:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 03 Nov 2022 16:56:31 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 03 Nov 2022 16:56:31 GMT
RUN docker-php-ext-enable sodium
# Thu, 03 Nov 2022 16:56:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Nov 2022 16:56:33 GMT
STOPSIGNAL SIGWINCH
# Thu, 03 Nov 2022 16:56:35 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 03 Nov 2022 16:56:35 GMT
WORKDIR /var/www/html
# Thu, 03 Nov 2022 16:56:36 GMT
EXPOSE 80
# Thu, 03 Nov 2022 16:56:37 GMT
CMD ["apache2-foreground"]
# Thu, 03 Nov 2022 18:03:58 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Nov 2022 18:03:59 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 03 Nov 2022 18:04:01 GMT
COPY file:e2da1c2113094da76d330eef39e0e1916af11394dff778e02af557c116266d7c in /usr/local/bin/ 
# Thu, 03 Nov 2022 18:04:01 GMT
ENV DRUPAL_VERSION=9.4.8
# Thu, 03 Nov 2022 18:04:02 GMT
WORKDIR /opt/drupal
# Thu, 03 Nov 2022 18:04:15 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Thu, 03 Nov 2022 18:04:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:32caca2e9abac2a8ffc2b083d202d57e1970d8adc212be17451a992441fad01b`  
		Last Modified: Tue, 25 Oct 2022 02:29:19 GMT  
		Size: 27.8 MB (27799224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140e6bcf950ee2d755ce50e370b6647bc357dcbd24dd0ece7e8d7b388f84d94d`  
		Last Modified: Tue, 25 Oct 2022 09:56:51 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d087454ecae3a96210f9074f3beccfe18b333cf212f9946b1aa8a54c4d0c064c`  
		Last Modified: Tue, 25 Oct 2022 09:57:02 GMT  
		Size: 81.2 MB (81234271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2520a6c0f52f7418abcd797a402d8844158c345af1bc2f6a196ef56b0d9b85d6`  
		Last Modified: Tue, 25 Oct 2022 09:56:50 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c10767ffcd61bf365893f41478142575a626be4309a58d0ff91365a013c2976b`  
		Last Modified: Tue, 25 Oct 2022 09:57:26 GMT  
		Size: 18.9 MB (18900801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e017d214c18776904c54b35b1b5803ba97d3dd0cd9ac7ebf134e7beb0235aa`  
		Last Modified: Tue, 25 Oct 2022 09:57:23 GMT  
		Size: 431.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353ace81a532edeb6342ba0eeb71d4a12b5f458af2c0f8af8a56d0bd2e80c050`  
		Last Modified: Tue, 25 Oct 2022 09:57:23 GMT  
		Size: 487.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e26bec27c4b59672aabab9ca855398e2bfd80e4c2ba74e461c6284e1f3afd2`  
		Last Modified: Thu, 03 Nov 2022 17:37:52 GMT  
		Size: 10.5 MB (10545249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c032b85541f555c674d31a45ae42e3fbcf8265d0c3c6aedd71f773232fcf23`  
		Last Modified: Thu, 03 Nov 2022 17:37:48 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718ada16f63ae836ce863de8ee68c05b214f7d6494029682e88e71b860fdfb61`  
		Last Modified: Thu, 03 Nov 2022 17:37:50 GMT  
		Size: 11.8 MB (11820343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19676fe09484b56d58bf1fd7ef48a7aec9df6a1b482751b7a27e04c91f6f0c6e`  
		Last Modified: Thu, 03 Nov 2022 17:37:48 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:714055c92860b8d6db523ecc04cf1c5a28d861f29e175a22afe2d75d6bbb9a5a`  
		Last Modified: Thu, 03 Nov 2022 17:37:48 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a14fd07d286f556cac8a3cf7c95f44235c3c747a572005abaf4a2b03c42a5ce`  
		Last Modified: Thu, 03 Nov 2022 17:37:48 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd68eb56c852bb4910cc518cab6c041120b83e6fdaed584d1aa49b58a3f434a9`  
		Last Modified: Thu, 03 Nov 2022 18:27:19 GMT  
		Size: 1.8 MB (1780148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5973ceba8034068417ac982a05acfe04b0a4d8cc9359a8d5926b4e6ccfacc5a3`  
		Last Modified: Thu, 03 Nov 2022 18:27:18 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab17d3070595809381db2b85b92b1aefacd3ad0da5a5db2fb097b634be8302f`  
		Last Modified: Thu, 03 Nov 2022 18:27:18 GMT  
		Size: 695.2 KB (695199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73663043a5458489423094e5cca0138af775325c94005149a25f1975f699e00`  
		Last Modified: Thu, 03 Nov 2022 18:27:18 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca86fdb34ef6348b65c39061d8c880e8bfbbaf3ff341d6a53059e73cb18ff0`  
		Last Modified: Thu, 03 Nov 2022 18:27:24 GMT  
		Size: 21.9 MB (21898908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
