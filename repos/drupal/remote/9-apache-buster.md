## `drupal:9-apache-buster`

```console
$ docker pull drupal@sha256:bd66a652a9a018b85019a05a48e678f3ab674ab5d57bd694ac5f44038bed37e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `drupal:9-apache-buster` - linux; amd64

```console
$ docker pull drupal@sha256:69cf168725aec2280cb72c73f9dcb706bf7e3be7852781a7ee9062701f9dee74
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.3 MB (169309209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff2f828cbe07990223486051dbccdb7d83b610e9f93883d75858dd8863fbb5c0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 04 Oct 2022 23:27:01 GMT
ADD file:706105a4a2ea63ba10911afb5998d321ff745f9bcedd2e2e8efcf33f5dad584b in / 
# Tue, 04 Oct 2022 23:27:01 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 07:22:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 05 Oct 2022 07:22:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 05 Oct 2022 07:23:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 07:23:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Oct 2022 07:23:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 05 Oct 2022 07:26:20 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 05 Oct 2022 07:26:20 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 05 Oct 2022 07:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 05 Oct 2022 07:26:31 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 05 Oct 2022 07:26:32 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 05 Oct 2022 07:26:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Oct 2022 07:26:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Oct 2022 07:26:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Oct 2022 08:19:03 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Wed, 05 Oct 2022 08:19:03 GMT
ENV PHP_VERSION=8.0.24
# Wed, 05 Oct 2022 08:19:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.24.tar.xz.asc
# Wed, 05 Oct 2022 08:19:03 GMT
ENV PHP_SHA256=8e6a63ac9cdabe4c345b32a54b18f348d9e50a1decda217faf2d61278d22f08b
# Wed, 05 Oct 2022 08:19:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 05 Oct 2022 08:19:15 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 05 Oct 2022 08:22:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 05 Oct 2022 08:22:10 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 05 Oct 2022 08:22:10 GMT
RUN docker-php-ext-enable sodium
# Wed, 05 Oct 2022 08:22:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Oct 2022 08:22:10 GMT
STOPSIGNAL SIGWINCH
# Wed, 05 Oct 2022 08:22:11 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 05 Oct 2022 08:22:11 GMT
WORKDIR /var/www/html
# Wed, 05 Oct 2022 08:22:11 GMT
EXPOSE 80
# Wed, 05 Oct 2022 08:22:11 GMT
CMD ["apache2-foreground"]
# Thu, 06 Oct 2022 00:11:39 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 00:11:39 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 06 Oct 2022 00:11:40 GMT
COPY file:31957edf88ab81c875036fac642510adba17e7f664ade12ad4cc270b8b01a7d0 in /usr/local/bin/ 
# Thu, 06 Oct 2022 00:11:40 GMT
ENV DRUPAL_VERSION=9.4.7
# Thu, 06 Oct 2022 00:11:40 GMT
WORKDIR /opt/drupal
# Thu, 06 Oct 2022 00:11:52 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Thu, 06 Oct 2022 00:11:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:f6e04ba6531065d60cd73d6509ec153307f5cc6f95e72ca47745d37aef6380a7`  
		Last Modified: Tue, 04 Oct 2022 23:31:38 GMT  
		Size: 27.1 MB (27138043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caafd74e30285bd82a1099001fdf19d68f60215ba05e12c11340639dc0a73f93`  
		Last Modified: Wed, 05 Oct 2022 08:53:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45715cafb97372e282f0648031a4262cd5bc34a8ce99a69c52a7ecbd1b8c126`  
		Last Modified: Wed, 05 Oct 2022 08:53:41 GMT  
		Size: 76.7 MB (76685017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5328863c71ccdb1520344da48f46073fd3675534ca660a0886215a3108b9477`  
		Last Modified: Wed, 05 Oct 2022 08:53:30 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d484c2d69b14085576b62d019b18a555de540b9c9d04b7834a15d504a61903d9`  
		Last Modified: Wed, 05 Oct 2022 08:54:01 GMT  
		Size: 18.7 MB (18682095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf8ffbd2f0e980468903416d66292244a20e06b9ca9d9320ee2ef9ac0fc6fdb`  
		Last Modified: Wed, 05 Oct 2022 08:53:59 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d8654c6608de8e61da9589091c125f2ec04e1b10d268904eaa118db8bfbf7e`  
		Last Modified: Wed, 05 Oct 2022 08:53:59 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8925728d1275cf89dff93a157f759c5f29ac86f1a430ea30b7b5016c96eab1a`  
		Last Modified: Wed, 05 Oct 2022 09:00:33 GMT  
		Size: 11.2 MB (11233041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:673b2c72c7a37b7db350f25270d2bf36b57ea274b5aabe89a137b7485c47c191`  
		Last Modified: Wed, 05 Oct 2022 09:00:30 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b389fccf99971ca852be887b9024e7399cd9887e53a610647a0995f7030e19c3`  
		Last Modified: Wed, 05 Oct 2022 09:00:33 GMT  
		Size: 10.7 MB (10733003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af3cb320e2bedaabee5f8083d1221dbb9e62dbd43a9fa49a10005c3223f69c7`  
		Last Modified: Wed, 05 Oct 2022 09:00:30 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2749a246c3127d64ff0f10e86e10663ae5f3420eedb1906b0f6a999ab362005`  
		Last Modified: Wed, 05 Oct 2022 09:00:30 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3d23eea9093637a787b36d855b37735a070675e6e257db4db7656295f656ac`  
		Last Modified: Wed, 05 Oct 2022 09:00:30 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e8cfa9288dd799ab692dcdb2bc84fb292b022adbc1056c24186a1ec0296434`  
		Last Modified: Thu, 06 Oct 2022 00:33:52 GMT  
		Size: 2.2 MB (2245820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db7a6529f7144e052687448f5ef48ce9925d278bf02bf2d0d4f704d4efd70a2`  
		Last Modified: Thu, 06 Oct 2022 00:33:52 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a617e15b934efecc3ed6cecea7a337db006b92d73ae6990b6190b883be3e5f`  
		Last Modified: Thu, 06 Oct 2022 00:33:52 GMT  
		Size: 692.6 KB (692594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1d3047e6f4d35abf056b11162c10306b49d24778454677409c47b75b251462`  
		Last Modified: Thu, 06 Oct 2022 00:33:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66bdd5cb20591a4d3fc1c2351c5ce63e75982c6ef3c1db34029ab881129e113`  
		Last Modified: Thu, 06 Oct 2022 00:33:57 GMT  
		Size: 21.9 MB (21893548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:9-apache-buster` - linux; arm variant v7

```console
$ docker pull drupal@sha256:474a608b6233bb81db6cb072439df996f66b979683fd0cba158eada0b10a4094
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145179494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97ed13c88df48b3a2e5a056614fae8c0f5056d236ab46da041978a542eb1cb3`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 13 Sep 2022 03:43:14 GMT
ADD file:0a80cba5196c5f463d85aeb456ee0f5778155ac5b1d3ce93a2023f1141aac44a in / 
# Tue, 13 Sep 2022 03:43:14 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 19:45:30 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Sep 2022 19:45:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Sep 2022 19:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 19:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Sep 2022 19:46:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 13 Sep 2022 19:53:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 13 Sep 2022 19:53:25 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 13 Sep 2022 19:53:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 13 Sep 2022 19:53:39 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 13 Sep 2022 19:53:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 13 Sep 2022 19:53:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Sep 2022 19:53:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Sep 2022 19:53:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Sep 2022 22:27:19 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Sat, 01 Oct 2022 00:43:25 GMT
ENV PHP_VERSION=8.0.24
# Sat, 01 Oct 2022 00:43:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.24.tar.xz.asc
# Sat, 01 Oct 2022 00:43:25 GMT
ENV PHP_SHA256=8e6a63ac9cdabe4c345b32a54b18f348d9e50a1decda217faf2d61278d22f08b
# Sat, 01 Oct 2022 00:43:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 01 Oct 2022 00:43:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 01 Oct 2022 00:54:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 01 Oct 2022 00:54:56 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 01 Oct 2022 00:54:57 GMT
RUN docker-php-ext-enable sodium
# Sat, 01 Oct 2022 00:54:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 01 Oct 2022 00:54:57 GMT
STOPSIGNAL SIGWINCH
# Sat, 01 Oct 2022 00:54:58 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 01 Oct 2022 00:54:58 GMT
WORKDIR /var/www/html
# Sat, 01 Oct 2022 00:54:58 GMT
EXPOSE 80
# Sat, 01 Oct 2022 00:54:58 GMT
CMD ["apache2-foreground"]
# Sat, 01 Oct 2022 04:31:02 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Sat, 01 Oct 2022 04:31:03 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 01 Oct 2022 04:31:03 GMT
COPY file:31957edf88ab81c875036fac642510adba17e7f664ade12ad4cc270b8b01a7d0 in /usr/local/bin/ 
# Sat, 01 Oct 2022 04:31:03 GMT
ENV DRUPAL_VERSION=9.4.7
# Sat, 01 Oct 2022 04:31:03 GMT
WORKDIR /opt/drupal
# Sat, 01 Oct 2022 04:31:36 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Sat, 01 Oct 2022 04:31:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:04df89f99dde583959eeb3f2964381f6e5a3199fa335ea1b9862aab596638515`  
		Last Modified: Tue, 13 Sep 2022 03:50:50 GMT  
		Size: 22.7 MB (22740495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c0e8bbe2c6e458b7783701258d3eae9edde02832a121b7f447c3d3783e1047`  
		Last Modified: Wed, 14 Sep 2022 00:06:57 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7d9007b99f7194046023d68fc9fd86ca8a98585cece2f4e55c1c5df6ee045b`  
		Last Modified: Wed, 14 Sep 2022 00:07:16 GMT  
		Size: 59.5 MB (59539491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104f39f65cce60b96bbdccc1c0d54e5b0acbdc48b47602ae70f2b0ba7bdd04d5`  
		Last Modified: Wed, 14 Sep 2022 00:06:57 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aeb9839442dcdc4588e996e77db1b251098b61c700793a1bf3fa7fbc0e1ca28`  
		Last Modified: Wed, 14 Sep 2022 00:07:45 GMT  
		Size: 17.5 MB (17480824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97959223410099ea3108cde3c6c828c8471a79f233b50247dda00efeeafd6fe4`  
		Last Modified: Wed, 14 Sep 2022 00:07:40 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f54a809c6ac9ee541387127cb7994be3bce6b7cd55a71589db81353d88eee66`  
		Last Modified: Wed, 14 Sep 2022 00:07:40 GMT  
		Size: 517.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0274d408417887f8df2032517bcd97cadea6154a27746030f60418596e52522`  
		Last Modified: Sat, 01 Oct 2022 02:58:36 GMT  
		Size: 11.2 MB (11231293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca925a3a2e520a5dae3e57b367e443b540a220fbbf9ef9e7c8d282251d4654e`  
		Last Modified: Sat, 01 Oct 2022 02:58:32 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146d387cf47477ac189540036fa6a34a845916b72d6bf8e86e43f88c793aa4d1`  
		Last Modified: Sat, 01 Oct 2022 02:58:36 GMT  
		Size: 10.0 MB (9962568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64364b0883b79d94cfe52b4770bcd16da43e26f7b813b5a0fa3cffb9daa35982`  
		Last Modified: Sat, 01 Oct 2022 02:58:32 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962e24f4a6f6ff43dae97ca02a1d971d9ca815861491e3ee77b454a7918da7af`  
		Last Modified: Sat, 01 Oct 2022 02:58:33 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc13f97f6bad77ed84a314fd3a6cd59a53695339107159226c06b7a603118d67`  
		Last Modified: Sat, 01 Oct 2022 02:58:32 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486d619e9b13dc85ecffb221b66144ed25855a41af3d4a31faf2d59620a963f2`  
		Last Modified: Sat, 01 Oct 2022 04:59:07 GMT  
		Size: 1.6 MB (1632355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e313e36a92467bf7e95b2e78ab3270ccfc178eb5797177e7483d2645bbc1a64`  
		Last Modified: Sat, 01 Oct 2022 04:59:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b457f455d203d4d2d77d94dc9a5caf2609f6009789322bf2afbaced076db8733`  
		Last Modified: Sat, 01 Oct 2022 04:59:07 GMT  
		Size: 692.6 KB (692586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c350cc679a47b92230f1f4c574eee4890172a45eaaab117cc5465303b76f6b`  
		Last Modified: Sat, 01 Oct 2022 04:59:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0ba311015e131634e51bd1f07675b178a0eea6516c19a286ffc805423b191e`  
		Last Modified: Sat, 01 Oct 2022 04:59:19 GMT  
		Size: 21.9 MB (21893817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:9-apache-buster` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:ee66104efafd0090ea131e7468b6a20025c320c6a0c346cea31d37b3da30df77
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.1 MB (160145122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d2861cd3516f7a8313d4bf9836c1ede4f72cd8af12555df7d90587872d38f4c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 04 Oct 2022 23:45:10 GMT
ADD file:5395cc8536f80a7cce6fbae552f35b892b152e1db2fce6274fc514d8fc77d7c9 in / 
# Tue, 04 Oct 2022 23:45:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 07:21:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 05 Oct 2022 07:21:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 05 Oct 2022 07:21:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 07:21:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Oct 2022 07:21:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 05 Oct 2022 07:25:57 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 05 Oct 2022 07:25:58 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 05 Oct 2022 07:26:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 05 Oct 2022 07:26:08 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 05 Oct 2022 07:26:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 05 Oct 2022 07:26:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Oct 2022 07:26:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Oct 2022 07:26:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Oct 2022 08:26:58 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Wed, 05 Oct 2022 08:26:58 GMT
ENV PHP_VERSION=8.0.24
# Wed, 05 Oct 2022 08:26:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.24.tar.xz.asc
# Wed, 05 Oct 2022 08:27:00 GMT
ENV PHP_SHA256=8e6a63ac9cdabe4c345b32a54b18f348d9e50a1decda217faf2d61278d22f08b
# Wed, 05 Oct 2022 08:27:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 05 Oct 2022 08:27:21 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 05 Oct 2022 08:29:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 05 Oct 2022 08:29:55 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 05 Oct 2022 08:29:55 GMT
RUN docker-php-ext-enable sodium
# Wed, 05 Oct 2022 08:29:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Oct 2022 08:29:57 GMT
STOPSIGNAL SIGWINCH
# Wed, 05 Oct 2022 08:29:59 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 05 Oct 2022 08:29:59 GMT
WORKDIR /var/www/html
# Wed, 05 Oct 2022 08:30:00 GMT
EXPOSE 80
# Wed, 05 Oct 2022 08:30:01 GMT
CMD ["apache2-foreground"]
# Wed, 05 Oct 2022 22:55:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 22:55:19 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 05 Oct 2022 22:55:21 GMT
COPY file:31957edf88ab81c875036fac642510adba17e7f664ade12ad4cc270b8b01a7d0 in /usr/local/bin/ 
# Wed, 05 Oct 2022 22:55:21 GMT
ENV DRUPAL_VERSION=9.4.7
# Wed, 05 Oct 2022 22:55:22 GMT
WORKDIR /opt/drupal
# Wed, 05 Oct 2022 22:55:52 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Wed, 05 Oct 2022 22:55:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:2c1ba50780a9bc2b2a8f3d639ceca4285c97f51fd1c51c783fe34e150ff35e60`  
		Last Modified: Tue, 04 Oct 2022 23:51:14 GMT  
		Size: 25.9 MB (25911903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f294832078061b7415f272ec2761b7719b3e5280f601911d1a0a846bed1c697`  
		Last Modified: Wed, 05 Oct 2022 09:06:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb1423a6acc78299080d62705715735db968d712c0911f2a538c7bb78846c0c`  
		Last Modified: Wed, 05 Oct 2022 09:06:38 GMT  
		Size: 70.4 MB (70364283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881544aca2f719ccea538ad8809af4daf3fe9e67150d222ea07989311fe44c39`  
		Last Modified: Wed, 05 Oct 2022 09:06:28 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae13209809b5abef3c1b647925326afb012b6511c81cffb8c712758f3caa187e`  
		Last Modified: Wed, 05 Oct 2022 09:07:01 GMT  
		Size: 18.4 MB (18368122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f01584fbc5074a7a7d1e26d03de2482b150008be4f61939960aa3f146e10b46`  
		Last Modified: Wed, 05 Oct 2022 09:06:58 GMT  
		Size: 430.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5248523969968f0f8f49ada0b881a295b69fe3ad0d0e8ae40a533be4975808`  
		Last Modified: Wed, 05 Oct 2022 09:06:58 GMT  
		Size: 487.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a06a4588b764b9fd58fcd273825ded2f6482cba95574a00f7eaa4f87b8cd58`  
		Last Modified: Wed, 05 Oct 2022 09:14:51 GMT  
		Size: 11.0 MB (11019849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d00b8fd17584dc2a2dc321520a08913443f502416401e70611c2a89a3849c02`  
		Last Modified: Wed, 05 Oct 2022 09:14:47 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac6780e2e78d589efcec49ebda5feb477f728015de6d741b24efca9c94f7a47`  
		Last Modified: Wed, 05 Oct 2022 09:14:49 GMT  
		Size: 10.2 MB (10205023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766df25f68bd82dda6f546dfcaf075962c5414a594110465307b4dc020eafc66`  
		Last Modified: Wed, 05 Oct 2022 09:14:47 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe913ab08a18134fc0e9e17e4592ed533503a7213ca00b6710f1b68161e1656`  
		Last Modified: Wed, 05 Oct 2022 09:14:48 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6794d6119e0ccd394604bba6e76fd7fd5280ae733aa6b338593edb7b0300f8a7`  
		Last Modified: Wed, 05 Oct 2022 09:14:48 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d39b02948024a488ae2921eb4c2bc121149ea12aead236c8cad74c04007fed8`  
		Last Modified: Wed, 05 Oct 2022 23:31:06 GMT  
		Size: 1.7 MB (1686346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb79fc6ab0594b6eb3d7882ca2a3a397b58b4ac5dc64805cae16b6a5392fe2a`  
		Last Modified: Wed, 05 Oct 2022 23:31:05 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:831dcfc6e2624dd54d1cfbcd6f80ae29f3f42db15a9c217a2ad4b3042a4c0ce2`  
		Last Modified: Wed, 05 Oct 2022 23:31:06 GMT  
		Size: 692.6 KB (692585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41898a1d981252665b3aa5b79a04524126ebe1008ea771748a9450a379d82a32`  
		Last Modified: Wed, 05 Oct 2022 23:31:05 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08dbc1a066e116f448eee0b35cc2f9559eaf2321fd7b20d30027bc85efdcbf12`  
		Last Modified: Wed, 05 Oct 2022 23:31:11 GMT  
		Size: 21.9 MB (21891109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:9-apache-buster` - linux; 386

```console
$ docker pull drupal@sha256:52f0c8b252eda3e34e9fc9e9520db8e8dcd1207df245b5eb305ee958a2f007b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174580061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c26d32ffe65a41a28f9132f2ffd4536d89e4be61399858e759620ab7646f069`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 04 Oct 2022 23:40:08 GMT
ADD file:b1ef7e7f4c48770bde0d19751bb1624a887b657a5a5ab5d453fd5365b3448618 in / 
# Tue, 04 Oct 2022 23:40:09 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 05:32:19 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 05 Oct 2022 05:32:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 05 Oct 2022 05:32:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 05:32:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Oct 2022 05:32:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 05 Oct 2022 05:36:01 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 05 Oct 2022 05:36:02 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 05 Oct 2022 05:36:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 05 Oct 2022 05:36:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 05 Oct 2022 05:36:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 05 Oct 2022 05:36:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Oct 2022 05:36:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Oct 2022 05:36:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Oct 2022 06:27:16 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Wed, 05 Oct 2022 06:27:17 GMT
ENV PHP_VERSION=8.0.24
# Wed, 05 Oct 2022 06:27:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.24.tar.xz.asc
# Wed, 05 Oct 2022 06:27:19 GMT
ENV PHP_SHA256=8e6a63ac9cdabe4c345b32a54b18f348d9e50a1decda217faf2d61278d22f08b
# Wed, 05 Oct 2022 06:27:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 05 Oct 2022 06:27:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 05 Oct 2022 06:30:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 05 Oct 2022 06:30:07 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 05 Oct 2022 06:30:08 GMT
RUN docker-php-ext-enable sodium
# Wed, 05 Oct 2022 06:30:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Oct 2022 06:30:09 GMT
STOPSIGNAL SIGWINCH
# Wed, 05 Oct 2022 06:30:11 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 05 Oct 2022 06:30:11 GMT
WORKDIR /var/www/html
# Wed, 05 Oct 2022 06:30:12 GMT
EXPOSE 80
# Wed, 05 Oct 2022 06:30:13 GMT
CMD ["apache2-foreground"]
# Wed, 05 Oct 2022 15:23:27 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 15:23:28 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 05 Oct 2022 15:23:30 GMT
COPY file:31957edf88ab81c875036fac642510adba17e7f664ade12ad4cc270b8b01a7d0 in /usr/local/bin/ 
# Wed, 05 Oct 2022 15:23:30 GMT
ENV DRUPAL_VERSION=9.4.7
# Wed, 05 Oct 2022 15:23:31 GMT
WORKDIR /opt/drupal
# Wed, 05 Oct 2022 15:23:44 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Wed, 05 Oct 2022 15:23:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d1d1dd08a5009b10b72285f23ffd4c1978d3445cc3855d22f4112018b15a9420`  
		Last Modified: Tue, 04 Oct 2022 23:46:26 GMT  
		Size: 27.8 MB (27797501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ef26ef223ed430be44b1235ee1081af95576204d4884d89a6e84dac64e910f`  
		Last Modified: Wed, 05 Oct 2022 07:06:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94647b3f1d6fd0bcf270dc4840a5ae6379b62e6d764b8b8d2937a0ab3a59b1c7`  
		Last Modified: Wed, 05 Oct 2022 07:06:31 GMT  
		Size: 81.2 MB (81230534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91945b578017157defacefb4c3d8bd957711756468948721f363702724ba8a60`  
		Last Modified: Wed, 05 Oct 2022 07:06:20 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290adc7cc28a1d3d90e930ddae2334588586c9eb0c7a221199a12806510639ed`  
		Last Modified: Wed, 05 Oct 2022 07:06:56 GMT  
		Size: 18.9 MB (18900656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80107ede7cd4b39b296becad1595f86914f27fd5895208ae467bde3525861dad`  
		Last Modified: Wed, 05 Oct 2022 07:06:53 GMT  
		Size: 433.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3aeb6a27065fdaee49f3b16b90097b252c18b0b9b61c8fd9255fb58b293763`  
		Last Modified: Wed, 05 Oct 2022 07:06:52 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bcd3d63a7bb2275e6e903965994389952d5e66f0689f42d86933474ebf0966b`  
		Last Modified: Wed, 05 Oct 2022 07:15:22 GMT  
		Size: 11.0 MB (11020351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f705e4447480f64997f40b5e0771a1f5ac824b2a154b1dd4992fe4f984501c56`  
		Last Modified: Wed, 05 Oct 2022 07:15:19 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127870ccd550513f3da0a16f9c8a29cdf852fdb7e3ca3f0f9d017ab4bfcb81bc`  
		Last Modified: Wed, 05 Oct 2022 07:15:21 GMT  
		Size: 10.9 MB (10939787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba1be5dbb48c31be81bd0da49942dc11a7d2d0a89b31ba954881a304b408918`  
		Last Modified: Wed, 05 Oct 2022 07:15:19 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305b31d99d8e4dfef1ac42aa9d0ad8df167ea0e5927c5c443cfada2538830673`  
		Last Modified: Wed, 05 Oct 2022 07:15:19 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d845ded6b51e222607c12e2c71e17e7714599ea2b2b277b9bf5628b819424bec`  
		Last Modified: Wed, 05 Oct 2022 07:15:19 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332c96c0358f55ecc270a3e31079592df004e587cc4d9612bebbfdb48161a22a`  
		Last Modified: Wed, 05 Oct 2022 15:56:37 GMT  
		Size: 2.1 MB (2102162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65cc0df95e50bf22763f1dfc97591e12ea320d440172f1d8ee01eba5d9c508c4`  
		Last Modified: Wed, 05 Oct 2022 15:56:37 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d834a78bba8b9d3d2492bf09715074bbdc57376efbb7f2d602ebb84ad54d69`  
		Last Modified: Wed, 05 Oct 2022 15:56:37 GMT  
		Size: 692.6 KB (692585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7161834ecb607543815bbd59c3b7220c54941aefe20592bb8dc0b6d50e52c100`  
		Last Modified: Wed, 05 Oct 2022 15:56:37 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8404c50a0a39f3aaf8a3b628c5be2fb56427d2f1887d82db7fa0abb42846d606`  
		Last Modified: Wed, 05 Oct 2022 15:56:42 GMT  
		Size: 21.9 MB (21890582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
