## `drupal:rc-php8.3`

```console
$ docker pull drupal@sha256:ae229f7b72f7bf09d483249fbeeb7cc8051d1296adf1a73d0c9e45573e0cf281
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
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

### `drupal:rc-php8.3` - linux; amd64

```console
$ docker pull drupal@sha256:318ce8cf8cf9967c4601af8df73aa6b701afcd640dbd06a21d2eee689b29ae4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.1 MB (200145688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080eb3ed397139b969d8e13d83d28f443fd1692ea1e09903aae4ff238017ee90`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:37 GMT
ADD file:d261a6f6921593f1e0b3f472ab1b1822e2c6deb0b369200f0b3370556bfad017 in / 
# Tue, 21 Nov 2023 05:21:37 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 13:45:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 21 Nov 2023 13:45:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 21 Nov 2023 13:46:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 13:46:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Nov 2023 13:46:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 21 Nov 2023 13:50:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 21 Nov 2023 13:50:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 21 Nov 2023 13:50:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 21 Nov 2023 13:50:12 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 21 Nov 2023 13:50:12 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 21 Nov 2023 13:50:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Nov 2023 13:50:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Nov 2023 13:50:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Nov 2023 13:50:13 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 27 Nov 2023 21:25:47 GMT
ENV PHP_VERSION=8.3.0
# Mon, 27 Nov 2023 21:25:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Mon, 27 Nov 2023 21:25:47 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Mon, 27 Nov 2023 21:25:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 27 Nov 2023 21:25:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 27 Nov 2023 21:29:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 27 Nov 2023 21:29:33 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Mon, 27 Nov 2023 21:29:33 GMT
RUN docker-php-ext-enable sodium
# Mon, 27 Nov 2023 21:29:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 27 Nov 2023 21:29:34 GMT
STOPSIGNAL SIGWINCH
# Mon, 27 Nov 2023 21:29:34 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Mon, 27 Nov 2023 21:29:34 GMT
WORKDIR /var/www/html
# Mon, 27 Nov 2023 21:29:34 GMT
EXPOSE 80
# Mon, 27 Nov 2023 21:29:34 GMT
CMD ["apache2-foreground"]
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:1f7ce2fa46ab3942feabee654933948821303a5a821789dddab2d8c3df59e227`  
		Last Modified: Tue, 21 Nov 2023 05:25:58 GMT  
		Size: 29.1 MB (29149908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48824c101c6a9acdf3c9bf530c0f96b2fef6937560eaf6bb7d3811a02f69f894`  
		Last Modified: Tue, 21 Nov 2023 16:36:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249ff3a7bbe60797aad2ea6e666e3d5739b4d18915e5d91297875d883eb15cff`  
		Last Modified: Tue, 21 Nov 2023 16:36:18 GMT  
		Size: 104.4 MB (104353566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5d47f22b646304165bc2653d8436809c1202159ab1f8ca2003f54bbb900ec8`  
		Last Modified: Tue, 21 Nov 2023 16:36:03 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83ad87cf6a67083d44e82ef8e129e444eb1ae9cdebe0d1b49ef61c131ba92e8`  
		Last Modified: Tue, 21 Nov 2023 16:36:52 GMT  
		Size: 20.3 MB (20305146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92eeb6cb00683a848dba2b1a3195ae17ebbc18c8eb66ef67d25a1b464af8cc68`  
		Last Modified: Tue, 21 Nov 2023 16:36:50 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a08d032c4e601048a8ee006e33ee1c25a134d82f2aef48b06d89d1426d014f`  
		Last Modified: Tue, 21 Nov 2023 16:36:49 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4917eca7a83fe07bc82f776c28acd2def6f809f5e60b7255d52e9bc96dea4f`  
		Last Modified: Tue, 28 Nov 2023 00:10:05 GMT  
		Size: 12.8 MB (12766128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f34393d3a2a89458727effcd4f0ec8b148e9b214dae6150386b5910a1494ff0`  
		Last Modified: Tue, 28 Nov 2023 00:10:02 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec40d4381201e05d247ae6fa5d79bec7a76cb76650120eb2a8bee53125b53579`  
		Last Modified: Tue, 28 Nov 2023 00:10:04 GMT  
		Size: 11.7 MB (11667319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51f7f116b075066c28541c47b8bbc6f7718e215b429c43994ebaccdd7d99c3c`  
		Last Modified: Tue, 28 Nov 2023 00:10:02 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24aa8368a24e399624faccfd19de4bd4fd8b68db66c246a6da27359486639df8`  
		Last Modified: Tue, 28 Nov 2023 00:10:02 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38972f936082d81ca91b740066b56a321d3443a1ec9570b1baf78fb41c719638`  
		Last Modified: Tue, 28 Nov 2023 00:10:02 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8142528f1847c61621406df0a89e5bcb25c1d290ba14632c165fd493bd396ad6`  
		Last Modified: Tue, 05 Dec 2023 02:11:55 GMT  
		Size: 2.0 MB (1999061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c58dd053776553a8fd93586cf019302e1bf1318abc525bc9863ae7a8212ba3b`  
		Last Modified: Tue, 05 Dec 2023 02:11:55 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7636b9315faccbb21c7222a7042fe7b53c7c602394d592f2391e95a95419315a`  
		Last Modified: Tue, 05 Dec 2023 02:11:56 GMT  
		Size: 705.0 KB (705010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31cb55115d1e450a138835a8e7ce777cefb897d836249950559f220d45619b9`  
		Last Modified: Tue, 05 Dec 2023 02:11:55 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5155630b4d432b4c10faccf08a4443ffaffe378324969379443f4ed8e374d74`  
		Last Modified: Tue, 05 Dec 2023 02:11:58 GMT  
		Size: 19.2 MB (19193547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3` - unknown; unknown

```console
$ docker pull drupal@sha256:c4e254b2d2f82c6268f15e7bce5aa9557c47e7627ade37fff651ec5c659b7ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5954704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b917fc8dea2caee5acd22be289bb1dde634dbfe0c0892753f4b247cbf2ba011`

```dockerfile
```

-	Layers:
	-	`sha256:5e659b16b2f4726b6d61c46b40069eea548e811a6c775071780d54ff7a423c88`  
		Last Modified: Tue, 05 Dec 2023 02:11:54 GMT  
		Size: 5.9 MB (5913712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8114ab565ac7b41a2be5788706686091ab2da3966b2af4560a8164036eaafb1a`  
		Last Modified: Tue, 05 Dec 2023 02:11:53 GMT  
		Size: 41.0 KB (40992 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3` - linux; arm variant v7

```console
$ docker pull drupal@sha256:b00344d9dc3c0e6c17bd531ec0f3ddace0ca5c597e88a8d518ad91bc58dc9fea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.1 MB (164112079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7542e8f1695795393f383315b791f7b61f9e76ae7054e9e4e00a9a255c0f06e6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Nov 2023 03:57:43 GMT
ADD file:b693944382a95fa47622fde77eb98f0cdeafa40261e7334bd355e00f650b6632 in / 
# Tue, 21 Nov 2023 03:57:43 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:24:09 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 21 Nov 2023 08:24:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 21 Nov 2023 08:24:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:24:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Nov 2023 08:24:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 21 Nov 2023 08:27:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 21 Nov 2023 08:27:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 21 Nov 2023 08:27:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 21 Nov 2023 08:27:26 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 21 Nov 2023 08:27:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 21 Nov 2023 08:27:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Nov 2023 08:27:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Nov 2023 08:27:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Nov 2023 08:27:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 27 Nov 2023 21:03:19 GMT
ENV PHP_VERSION=8.3.0
# Mon, 27 Nov 2023 21:03:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Mon, 27 Nov 2023 21:03:19 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Mon, 27 Nov 2023 21:03:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 27 Nov 2023 21:03:35 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 27 Nov 2023 21:08:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 27 Nov 2023 21:08:37 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Mon, 27 Nov 2023 21:08:38 GMT
RUN docker-php-ext-enable sodium
# Mon, 27 Nov 2023 21:08:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 27 Nov 2023 21:08:39 GMT
STOPSIGNAL SIGWINCH
# Mon, 27 Nov 2023 21:08:39 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Mon, 27 Nov 2023 21:08:39 GMT
WORKDIR /var/www/html
# Mon, 27 Nov 2023 21:08:39 GMT
EXPOSE 80
# Mon, 27 Nov 2023 21:08:40 GMT
CMD ["apache2-foreground"]
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:b4ce590529bbcf84326048a22fce76fcfcb5c60af5519debd7935a74c1e9126e`  
		Last Modified: Tue, 21 Nov 2023 04:01:50 GMT  
		Size: 24.7 MB (24748925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c1c4147c53597e5b07cc3da6a4f2bc1153b627dbf415b2b595b2b6433ace84`  
		Last Modified: Tue, 21 Nov 2023 10:50:48 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccd91a599fb4e546a1b11496c7cde449b0a62782471ca6b57c7ccd447c465ff`  
		Last Modified: Tue, 21 Nov 2023 10:51:04 GMT  
		Size: 76.2 MB (76225648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28aecabad1653a96793880791ff49eaacb2fcb0b9498620f8bc5a9f4e2d4c67`  
		Last Modified: Tue, 21 Nov 2023 10:50:48 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd22fd75afd798303c122a7847b5a3dd3d553fc6308430df3331c76f5c27884`  
		Last Modified: Tue, 21 Nov 2023 10:51:32 GMT  
		Size: 19.0 MB (19046541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b37c46693beec8e40b5ca3291b55d05bf05c91bfa505abf03f1ae41aa7312d`  
		Last Modified: Tue, 21 Nov 2023 10:51:29 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a8e1883ef04ccbbb0af337e641a9d7fc88368c310238fa8d58e40e58166091`  
		Last Modified: Tue, 21 Nov 2023 10:51:29 GMT  
		Size: 514.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a31493d9655dd0c02fd16d47b86297d9d76b40ddfad870180eb6572a4626b99`  
		Last Modified: Mon, 27 Nov 2023 23:47:39 GMT  
		Size: 12.8 MB (12764183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674e44b51a2b750e243923d4d1d2894017680675bc24571907f236fecba53633`  
		Last Modified: Mon, 27 Nov 2023 23:47:36 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb14160d9030549096f59dbba457fa6e3f1e72e06231697af61bfe1863aa8d13`  
		Last Modified: Mon, 27 Nov 2023 23:47:38 GMT  
		Size: 10.1 MB (10066888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f7f86f02a4665bdfae6d8e31577dbe3eb65e259078020f5dd509e140df134e`  
		Last Modified: Mon, 27 Nov 2023 23:47:36 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce7d1a05b71f4ebbafa8c48ba77ab16d78f860302fc733110df1af1e995ca20`  
		Last Modified: Mon, 27 Nov 2023 23:47:36 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e6afd025459a28526f24b7f9cea547978616b41c1a4ec974065baa1c222c4e`  
		Last Modified: Mon, 27 Nov 2023 23:47:36 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4910b26c5e437ed7aba20fbda69624e7f6335296de4a014e92d488fed665dc21`  
		Last Modified: Tue, 05 Dec 2023 02:12:03 GMT  
		Size: 1.4 MB (1355358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3386cbb7404b436abff7976714ff8a01432c1273c0b37548937c11f4fd2527`  
		Last Modified: Tue, 05 Dec 2023 02:12:03 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e7059ad4ac2a863733d7afabf8c723cf5aa028b5163cd199757d5c18fc22bd`  
		Last Modified: Tue, 05 Dec 2023 02:12:04 GMT  
		Size: 705.0 KB (705008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31cb55115d1e450a138835a8e7ce777cefb897d836249950559f220d45619b9`  
		Last Modified: Tue, 05 Dec 2023 02:11:55 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab47618af62520c03e699d0ca48da1d4ac75e225a6f01fcae6849699b50c92fe`  
		Last Modified: Tue, 05 Dec 2023 02:12:05 GMT  
		Size: 19.2 MB (19193507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3` - unknown; unknown

```console
$ docker pull drupal@sha256:331bf66c1c8bcf112cc121dcb2b77981b54b80be9d4f616019ba084d7d42eacd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5794492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3fc2b2ee3e8d4cd661cf092a72edf0a5bfa48d2c0faf3d0a6be1f89c03a998`

```dockerfile
```

-	Layers:
	-	`sha256:8bf983d124b2f65c6918a10fd3b73274fadd012995aa321feee997e9ab6ec359`  
		Last Modified: Tue, 05 Dec 2023 02:12:02 GMT  
		Size: 5.8 MB (5753355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28a296eb42a5f89d1f7bcf3ed3702f17cdd075c1c4391e51284cda54bd23a3a0`  
		Last Modified: Tue, 05 Dec 2023 02:12:01 GMT  
		Size: 41.1 KB (41137 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:8987b6fe4fb010172ba52749d479299fd1df922ce44d3af232ea41f6b2363284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.2 MB (194208425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3948cf060945ef80c966aa7da0308883bf0ad08a369a02cc89dd77aa5bb9fbb7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:06 GMT
ADD file:869c7d0747a17c53715581a2e862992eb8516c7f45f167821dfa80966a4870d1 in / 
# Tue, 21 Nov 2023 06:27:06 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:00:07 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 21 Nov 2023 14:00:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 21 Nov 2023 14:00:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:00:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Nov 2023 14:00:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 21 Nov 2023 14:04:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 21 Nov 2023 14:04:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 21 Nov 2023 14:04:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 21 Nov 2023 14:04:24 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 21 Nov 2023 14:04:24 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 21 Nov 2023 14:04:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Nov 2023 14:04:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Nov 2023 14:04:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Nov 2023 14:04:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 27 Nov 2023 20:54:46 GMT
ENV PHP_VERSION=8.3.0
# Mon, 27 Nov 2023 20:54:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Mon, 27 Nov 2023 20:54:46 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Mon, 27 Nov 2023 20:54:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 27 Nov 2023 20:54:57 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 27 Nov 2023 20:58:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 27 Nov 2023 20:58:34 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Mon, 27 Nov 2023 20:58:34 GMT
RUN docker-php-ext-enable sodium
# Mon, 27 Nov 2023 20:58:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 27 Nov 2023 20:58:35 GMT
STOPSIGNAL SIGWINCH
# Mon, 27 Nov 2023 20:58:35 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Mon, 27 Nov 2023 20:58:35 GMT
WORKDIR /var/www/html
# Mon, 27 Nov 2023 20:58:35 GMT
EXPOSE 80
# Mon, 27 Nov 2023 20:58:35 GMT
CMD ["apache2-foreground"]
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:2c6d21737d8318aa15c4cc838475029a5efc36c0429e3d8da80d97d0b96d9aaf`  
		Last Modified: Tue, 21 Nov 2023 06:30:30 GMT  
		Size: 29.2 MB (29179277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f459fbdcda04d1eefe3ddbdd0fced7d3e294226fdd1f422f0605cbdc13cede`  
		Last Modified: Tue, 21 Nov 2023 16:35:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47c20ea5e2ac0c311dad37ac3196272e470d76b89225c64210f1e8e0cffd87f`  
		Last Modified: Tue, 21 Nov 2023 16:35:23 GMT  
		Size: 98.1 MB (98131989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc98159c6c08d2ac4a93193df61324117e3d5aeae8bce8f7d8cb3a4569616b3`  
		Last Modified: Tue, 21 Nov 2023 16:35:12 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8038060ce77aaf1e958eee1f19e255a10b8ca735de0c270bdbe64aa0a883ffb2`  
		Last Modified: Tue, 21 Nov 2023 16:35:51 GMT  
		Size: 20.3 MB (20306779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd40f4e2e435fe2408096e0827b91d164f4d2267ae305243616522b2d187ed1`  
		Last Modified: Tue, 21 Nov 2023 16:35:48 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88e99c1804cf3780d07fadaece2e4e50cd72a6c96198f1ec51a67aa52de1b6e`  
		Last Modified: Tue, 21 Nov 2023 16:35:48 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c78fde5defc7cad5217f45bf5aecbae2e319a99463a0712ec268a4101a37ae`  
		Last Modified: Mon, 27 Nov 2023 23:35:55 GMT  
		Size: 12.8 MB (12765760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c98789940c96dec173cc6f3cd4b57ec4c2bee86e42843dab339de55fe8f959`  
		Last Modified: Mon, 27 Nov 2023 23:35:52 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8a366abed5806d7e089218d7b045ad9b0c1ee1aa12da2b1a58824bbc462b57`  
		Last Modified: Mon, 27 Nov 2023 23:35:54 GMT  
		Size: 11.7 MB (11661386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ff9aea4808cec7d394bfef5ddb97aa6d9f416af64a21c0d109d50cc0b0c943`  
		Last Modified: Mon, 27 Nov 2023 23:35:52 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1bbb249e445d6d25b9517d0174a8a53750283a795efa11b16e49f79ba53a7d2`  
		Last Modified: Mon, 27 Nov 2023 23:35:52 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3593c151fbe5c8bf07fce976ea20ee01b46e48db3e0262489d70b1032e3e5bd9`  
		Last Modified: Mon, 27 Nov 2023 23:35:52 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b78049e86103851ceb8f3717cedd4e052ca1c9d860771c2b19d28c4aa9225b`  
		Last Modified: Tue, 05 Dec 2023 02:15:42 GMT  
		Size: 2.3 MB (2258445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece4a63850b306562fc036bc3110b1e15e856e90891f45ca923e12e6c976376e`  
		Last Modified: Tue, 05 Dec 2023 02:15:42 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9bad98452a7eea98fc90d8a3df8b601053b75573a57d85901e27ddaa5a9213`  
		Last Modified: Tue, 05 Dec 2023 02:15:42 GMT  
		Size: 705.0 KB (705006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a021ed2eac0a7eb3631411764e054fc27b56617d2a0755125b2af94878dd3e6e`  
		Last Modified: Tue, 05 Dec 2023 02:15:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddf8006bb61502a9a441b6fae389965bef675dd3e998dcef19d3c8db33df22d`  
		Last Modified: Tue, 05 Dec 2023 02:15:43 GMT  
		Size: 19.2 MB (19193769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3` - unknown; unknown

```console
$ docker pull drupal@sha256:01fa0aaacf1f5d4c151ff0c6bb43df30ef131822e96bc125ff13ecb6405b92b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5979734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a785ca04788cde86c3d7eba74e68437cd1b5cb8d439bd9b53faef8fed3474b4`

```dockerfile
```

-	Layers:
	-	`sha256:49cfbb4d169c130ed556c56e15bc7a00dc6de4bc7fbcb843a82f1f701f83e6a8`  
		Last Modified: Tue, 05 Dec 2023 02:15:41 GMT  
		Size: 5.9 MB (5938729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e49593f98aee943fa2f979d402ac0c5fa7d9120b1d9cdcb9aa1800e0a3eff096`  
		Last Modified: Tue, 05 Dec 2023 02:15:40 GMT  
		Size: 41.0 KB (41005 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3` - linux; 386

```console
$ docker pull drupal@sha256:c16e9f1b04067516af58768776824184e7ca4562a3fc2dea1288a4bd16eb6d6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199131479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c1c499a09340fdf645d00f3b43ad65851145309f582dc7a653acd071bea67d4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Nov 2023 04:39:53 GMT
ADD file:930e1b9d85b6927c4d3046f7c75de2f3bfc6ec29100c314d0ab2b780ea30e962 in / 
# Tue, 21 Nov 2023 04:39:53 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:19:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 21 Nov 2023 09:19:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 21 Nov 2023 09:20:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:20:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Nov 2023 09:20:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 21 Nov 2023 09:27:19 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 21 Nov 2023 09:27:19 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 21 Nov 2023 09:27:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 21 Nov 2023 09:27:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 21 Nov 2023 09:27:34 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 21 Nov 2023 09:27:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Nov 2023 09:27:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Nov 2023 09:27:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Nov 2023 09:27:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 27 Nov 2023 20:45:27 GMT
ENV PHP_VERSION=8.3.0
# Mon, 27 Nov 2023 20:45:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Mon, 27 Nov 2023 20:45:27 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Mon, 27 Nov 2023 20:45:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 27 Nov 2023 20:45:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 27 Nov 2023 20:52:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 27 Nov 2023 20:52:14 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Mon, 27 Nov 2023 20:52:15 GMT
RUN docker-php-ext-enable sodium
# Mon, 27 Nov 2023 20:52:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 27 Nov 2023 20:52:15 GMT
STOPSIGNAL SIGWINCH
# Mon, 27 Nov 2023 20:52:15 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Mon, 27 Nov 2023 20:52:15 GMT
WORKDIR /var/www/html
# Mon, 27 Nov 2023 20:52:15 GMT
EXPOSE 80
# Mon, 27 Nov 2023 20:52:15 GMT
CMD ["apache2-foreground"]
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:c0734eabce8885d8904dbd11b77aa97c2d2b04bc8e2af9e89d47c4bda590dd8e`  
		Last Modified: Tue, 21 Nov 2023 04:44:34 GMT  
		Size: 30.2 MB (30164109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89090867ba89e0914603f0aaa2982d94d141eefc215d406364d3347331a329e`  
		Last Modified: Tue, 21 Nov 2023 14:11:55 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef61714f071aa04227b826da64a97bb2a4b31b44dfac6bf42e6f5cde2f75b196`  
		Last Modified: Tue, 21 Nov 2023 14:12:19 GMT  
		Size: 101.5 MB (101532658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0f5dd0a218260c92c9896edbbf6aa33e888ee38871d1cc023fa1ff75ba32d5`  
		Last Modified: Tue, 21 Nov 2023 14:11:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e5f5952e6b664a76523d4b17e66236eea681362ec18717f95d41b420858056`  
		Last Modified: Tue, 21 Nov 2023 14:12:48 GMT  
		Size: 20.8 MB (20826790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f30f614ac19ae735734c0b1774377e18e36c8677093210616a2227fc388c83b`  
		Last Modified: Tue, 21 Nov 2023 14:12:43 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e744e7aec12e0fcb8f62be92f065cab544fab292b20911946fcd9031b575095f`  
		Last Modified: Tue, 21 Nov 2023 14:12:43 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff93be0eefe991053fec488738d7ad24a7b1777a9884913603373b11765d99e8`  
		Last Modified: Tue, 28 Nov 2023 01:32:03 GMT  
		Size: 12.8 MB (12765234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b980f934769bd096351a585dd6f4bbc594b49029fb2e35d3447c99be618f68`  
		Last Modified: Tue, 28 Nov 2023 01:32:00 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64f98ad806a6b78f322b12a3445f41907538461d8a94cc42b05f1c0b95563ee`  
		Last Modified: Tue, 28 Nov 2023 01:32:04 GMT  
		Size: 11.9 MB (11885215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20c99d566fc1a319fac6643d3d01eaa2a77d35df0dd20a25529b67e6afa4aa0`  
		Last Modified: Tue, 28 Nov 2023 01:32:00 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51aadf85e7ac01a623edec2c572fe7bbfcce666a8e1bdf8e774ed51927fc4b2`  
		Last Modified: Tue, 28 Nov 2023 01:32:00 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ce41d6345260a4e4e5fa0d8298b2d609a08a034229cead8ff0c9b90255e31c`  
		Last Modified: Tue, 28 Nov 2023 01:32:00 GMT  
		Size: 897.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17abd9e217ba6dffe01b9863e6be53105cc2fbaa51d547d86e8ade19f858b8f2`  
		Last Modified: Tue, 05 Dec 2023 02:11:51 GMT  
		Size: 2.1 MB (2052873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab5fac0a25674afeb8947e26bf3bd3558e67af8a19287207a3b5db04b1bc219`  
		Last Modified: Tue, 05 Dec 2023 02:11:50 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc2cfdb657e211ebdff59f5803f55aeee8059cb0ef11a402e3d82946d0fb1e1`  
		Last Modified: Tue, 05 Dec 2023 02:11:50 GMT  
		Size: 705.0 KB (705010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274bed7014ab374b5c4c1f049ad07eaedea045e2ca9ab743894cdd12ce18caa2`  
		Last Modified: Tue, 05 Dec 2023 02:11:49 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d95914198ce703b92cf99d2b763b98507702ddf5838977df48f5d42e6d0f08a`  
		Last Modified: Tue, 05 Dec 2023 02:11:52 GMT  
		Size: 19.2 MB (19193576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3` - unknown; unknown

```console
$ docker pull drupal@sha256:0f5a4e3df150a0dfe3f96e92d5040ff33d3266f5c5b81b9317ac3997990fb0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 KB (40715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:570c45c31cdf849ed7e8312171dfddb453c2417c36dd997300101af4d76972e4`

```dockerfile
```

-	Layers:
	-	`sha256:779cffeaa03b8d9d959412b9cb4c3ca7ec4cc12066ca1060b70584d73cd29ace`  
		Last Modified: Tue, 05 Dec 2023 02:11:48 GMT  
		Size: 40.7 KB (40715 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3` - linux; ppc64le

```console
$ docker pull drupal@sha256:e97b0362fcfe6d937bfe1a7a8bc5ef17c74418de11d16b867825eaf3f7969052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.6 MB (204569527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4c01212c7c29cb4797be4bcb3f5b15075220ee0c13498928172eeeddd21e5e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Nov 2023 04:24:14 GMT
ADD file:8b22a531b6611a1e63dfc20e4e2931592e2d821bd4b64c4b2810bb9a36640c02 in / 
# Tue, 21 Nov 2023 04:24:16 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 13:03:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 21 Nov 2023 13:03:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 21 Nov 2023 13:03:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 13:03:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Nov 2023 13:03:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 21 Nov 2023 13:07:13 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 21 Nov 2023 13:07:13 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 21 Nov 2023 13:07:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 21 Nov 2023 13:07:29 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 21 Nov 2023 13:07:30 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 21 Nov 2023 13:07:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Nov 2023 13:07:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Nov 2023 13:07:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Nov 2023 13:07:31 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 27 Nov 2023 21:26:56 GMT
ENV PHP_VERSION=8.3.0
# Mon, 27 Nov 2023 21:26:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Mon, 27 Nov 2023 21:26:57 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Mon, 27 Nov 2023 21:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 27 Nov 2023 21:27:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 27 Nov 2023 21:30:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 27 Nov 2023 21:30:32 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Mon, 27 Nov 2023 21:30:33 GMT
RUN docker-php-ext-enable sodium
# Mon, 27 Nov 2023 21:30:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 27 Nov 2023 21:30:34 GMT
STOPSIGNAL SIGWINCH
# Mon, 27 Nov 2023 21:30:34 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Mon, 27 Nov 2023 21:30:34 GMT
WORKDIR /var/www/html
# Mon, 27 Nov 2023 21:30:35 GMT
EXPOSE 80
# Mon, 27 Nov 2023 21:30:35 GMT
CMD ["apache2-foreground"]
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:c570d04e61d8e35a3c8f12179d048d701451f97f9cf2099ea3e3738512dbf062`  
		Last Modified: Tue, 21 Nov 2023 04:28:58 GMT  
		Size: 33.1 MB (33141607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82a664b07ee97a51b3cda0d3c288ec64eb5e92be846f5cff8a7015b7e67d418`  
		Last Modified: Tue, 21 Nov 2023 15:17:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ee042a03e72d648db3e608b3e68c6776cd32dabe79f650b4666305f6820ea0`  
		Last Modified: Tue, 21 Nov 2023 15:17:59 GMT  
		Size: 103.3 MB (103321918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d869be71ab64ef6b34e324746d041204b8262173bd6e64c32f0cc0b6f081576c`  
		Last Modified: Tue, 21 Nov 2023 15:17:42 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a84070310a80e6e1d601e77d02287d05158e8dc837d53c55d5029555207f4fa`  
		Last Modified: Tue, 21 Nov 2023 15:18:30 GMT  
		Size: 21.5 MB (21490294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fda3039825248ac15db201f1eac41f62065888a5efbf2fb317c7c9fceac313`  
		Last Modified: Tue, 21 Nov 2023 15:18:26 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab7bddb2a35d16d0c9b4aa82769f4121b3684f949ef72d7aa45301d45d8b0be`  
		Last Modified: Tue, 21 Nov 2023 15:18:26 GMT  
		Size: 514.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed018c5a169ed3d732cd98e5b03117ffd58f19ad3d20ec5ca6b1e5912850759`  
		Last Modified: Mon, 27 Nov 2023 23:47:14 GMT  
		Size: 12.8 MB (12765458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e528512d1d6c608a0ce486a7928663d8481881f8409e45916a4322b19068fd04`  
		Last Modified: Mon, 27 Nov 2023 23:47:10 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbec9bb6559a059ee3430fb3ae2ad3b65c73b4c1fbe76e59753a20bf8df72fe`  
		Last Modified: Mon, 27 Nov 2023 23:47:14 GMT  
		Size: 12.1 MB (12089132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a543b2c6a5a89c0ff98bd7d2b2b08f9b5b11b540c9394cc3cd5115f193ee92`  
		Last Modified: Mon, 27 Nov 2023 23:47:10 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e235ba97f1271e8e8fec7008a6449bdceb2a470bfc39e8ec9b59a64868e2bbe`  
		Last Modified: Mon, 27 Nov 2023 23:47:10 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9027f557201fc8f14eb0e5735e5512423bec4b33c0f5d8c4bc00812f372031a`  
		Last Modified: Mon, 27 Nov 2023 23:47:10 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7aad3370aea778c32282283149e3061c8944049bf9b8d3e42a42ccc18f82c8`  
		Last Modified: Tue, 05 Dec 2023 02:13:09 GMT  
		Size: 1.9 MB (1856079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d35cc32d262e822d26a599ada97ef0ab47c4ac9a05dbfcfbffbae0bb5e54c1`  
		Last Modified: Tue, 05 Dec 2023 02:13:09 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bbb96efd9b4610f700943d285decb601a16a072cc856b817e35517bb4d4d52`  
		Last Modified: Tue, 05 Dec 2023 02:13:09 GMT  
		Size: 705.0 KB (705009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ed8fddb9323992ea97bda04c166bcb4af44ced160dff335966106c0606bbb1`  
		Last Modified: Tue, 05 Dec 2023 02:13:09 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b92ca50a78d24a2289aad101b577693bef99dcef44689bf268bbffecddb822a`  
		Last Modified: Tue, 05 Dec 2023 02:13:10 GMT  
		Size: 19.2 MB (19194019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3` - unknown; unknown

```console
$ docker pull drupal@sha256:0613fdb5b3e14cf91a3283c58ade136d618bb094650c577bb2b33869d4ae610c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5936137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:707a1f030e61437cc9b07cd36b6a0f4c810a36a103d3bbb5c0c9e8d6bc21c377`

```dockerfile
```

-	Layers:
	-	`sha256:ce1ee4b3e7d7c5bda79918b1071a38c8b71427ef0d4d72015d08d659015c1115`  
		Last Modified: Tue, 05 Dec 2023 02:13:07 GMT  
		Size: 5.9 MB (5895069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5e7d0559ca4f45c1091d7092085f1502b8474e1ac4482730ea8d4c206c56325`  
		Last Modified: Tue, 05 Dec 2023 02:13:06 GMT  
		Size: 41.1 KB (41068 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3` - linux; s390x

```console
$ docker pull drupal@sha256:78de673abdce4eafdda4747c6f6369d5c3be1eff7c745e9f30d67afbaaf4c235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173342039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:976f26d11fcf19ae3a43a22d64a6f35dc04979d8222044b6eb920dc99eb12a3b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Nov 2023 05:04:35 GMT
ADD file:c33fa9fdde73983850798b6eb1cd062e0398109d1d773e6a937fead7475c8efc in / 
# Tue, 21 Nov 2023 05:04:41 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:20:30 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 21 Nov 2023 10:20:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 21 Nov 2023 10:20:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 10:20:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Nov 2023 10:20:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 21 Nov 2023 10:23:54 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 21 Nov 2023 10:23:54 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 21 Nov 2023 10:24:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 21 Nov 2023 10:24:04 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 21 Nov 2023 10:24:04 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 21 Nov 2023 10:24:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Nov 2023 10:24:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Nov 2023 10:24:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Nov 2023 10:24:05 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 27 Nov 2023 20:46:09 GMT
ENV PHP_VERSION=8.3.0
# Mon, 27 Nov 2023 20:46:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Mon, 27 Nov 2023 20:46:10 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Mon, 27 Nov 2023 20:46:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 27 Nov 2023 20:46:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 27 Nov 2023 20:48:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 27 Nov 2023 20:48:54 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Mon, 27 Nov 2023 20:48:54 GMT
RUN docker-php-ext-enable sodium
# Mon, 27 Nov 2023 20:48:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 27 Nov 2023 20:48:55 GMT
STOPSIGNAL SIGWINCH
# Mon, 27 Nov 2023 20:48:55 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Mon, 27 Nov 2023 20:48:55 GMT
WORKDIR /var/www/html
# Mon, 27 Nov 2023 20:48:55 GMT
EXPOSE 80
# Mon, 27 Nov 2023 20:48:55 GMT
CMD ["apache2-foreground"]
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:6daa625e5a040476e253e7acd0befa74254a4865ec836d6334a544d82a21d4be`  
		Last Modified: Tue, 21 Nov 2023 05:10:21 GMT  
		Size: 27.5 MB (27512885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b073bc5f3b6460a2e86e6384462103c710b42906361c6fbf338c39d9c58ceb`  
		Last Modified: Tue, 21 Nov 2023 12:25:59 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca956902ffd9934a4d2fb043c2f4c6e1fb6f0642f0568699e799c560c20ea15`  
		Last Modified: Tue, 21 Nov 2023 12:26:10 GMT  
		Size: 80.8 MB (80819423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b8dfba35b49398dd688150d0c85decd88885387485c3525ac75e093b667ed3`  
		Last Modified: Tue, 21 Nov 2023 12:25:59 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd69aaa769727a63be006dd6fa255115d2086b2833811e887149e906a3bd92aa`  
		Last Modified: Tue, 21 Nov 2023 12:26:30 GMT  
		Size: 20.1 MB (20084572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b0f2410c9e7b7bdff692338f17dc61648dd4c4d36f9bcb4acffe5800ea041e`  
		Last Modified: Tue, 21 Nov 2023 12:26:28 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac15cf9228cfb1e9d2f6feb3fcdffb4de33873052e9f846e1ec24778ad1c9b4`  
		Last Modified: Tue, 21 Nov 2023 12:26:28 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1eb38d81fe897e9354fe5f0014d972d9006a50da4aaba5ad67fc56fdf841d58`  
		Last Modified: Mon, 27 Nov 2023 23:26:01 GMT  
		Size: 12.8 MB (12764545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f51ac73c124c7f6f623d56bb475c8e60a547667832918a7dd3bd2786fd34be1`  
		Last Modified: Mon, 27 Nov 2023 23:25:59 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13f5391ca52b34cf44e1b18bed81452976f466d559887b7da4643a17afc49bf`  
		Last Modified: Mon, 27 Nov 2023 23:26:01 GMT  
		Size: 10.7 MB (10700785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7a9d99f7ebd09666fa346af779ba4e792fd984f768f2936fe4e33593baf1c9`  
		Last Modified: Mon, 27 Nov 2023 23:26:00 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247039aa7dde3943cb2032e4b133556720ea4d1faef58250bc102dfe2cf0a25e`  
		Last Modified: Mon, 27 Nov 2023 23:26:00 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2ebf229f4ab4ec38151951e533683dc247abd772144396d257866016a88581`  
		Last Modified: Mon, 27 Nov 2023 23:26:00 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb06c395c028411ee25692cc3da53f7293932f89610be1ca4aa77913fd46d56`  
		Last Modified: Tue, 05 Dec 2023 02:14:13 GMT  
		Size: 1.6 MB (1555250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29bd1a177aaa3744468a0735892ce843e6eb4a3533f2fdd8718d966acdeae0b`  
		Last Modified: Tue, 05 Dec 2023 02:14:13 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93e53b045b32e380957b1bd46b89b043cbedf070975dbb58732e6d6116bf582`  
		Last Modified: Tue, 05 Dec 2023 02:14:13 GMT  
		Size: 705.0 KB (705010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:504f625cf9f12d1d50ebe5bcc8883038c12e7ec1c18dee76eb2e31831c75949f`  
		Last Modified: Tue, 05 Dec 2023 02:14:13 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453a7fb8743bebbe6c13d24b7ee4c85864ca1c5272fbdd509048e6c515697d5c`  
		Last Modified: Tue, 05 Dec 2023 02:14:14 GMT  
		Size: 19.2 MB (19193571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3` - unknown; unknown

```console
$ docker pull drupal@sha256:b03cd17952b8320f2943ccbc0662970ebec0a7cfa6fa4da83a8e84d42cf65e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5816199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0aeaf2a64dd755b0148e3c08400ef02d752d82a5330cb2ac2a1e2ed13be61b`

```dockerfile
```

-	Layers:
	-	`sha256:7a16433cc95a2684e6be889367df26c9bb8a4e55b9ccfe58404cd3b8174cdc6c`  
		Last Modified: Tue, 05 Dec 2023 02:14:11 GMT  
		Size: 5.8 MB (5775214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9687c186d9a15c6c7594e4f110471847ad4b844ce4bb38c0db7661fb441b92d4`  
		Last Modified: Tue, 05 Dec 2023 02:14:11 GMT  
		Size: 41.0 KB (40985 bytes)  
		MIME: application/vnd.in-toto+json
