## `mediawiki:legacylts`

```console
$ docker pull mediawiki@sha256:c526d3e09724b877b6e180e08c7e80b05e5ee16355b1ca134314f77015b55d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mediawiki:legacylts` - linux; amd64

```console
$ docker pull mediawiki@sha256:9ad776b5f13b143546ce5742955f8637cf3e3abfc127d180380b466b63eb9c4d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.5 MB (252477983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b7c17ab006228c08f1759974507a1f18803fb50e9ab056abc326d37b07e3073`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 11:48:30 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 23 Jun 2021 11:48:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 23 Jun 2021 11:48:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 11:48:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 23 Jun 2021 11:48:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 23 Jun 2021 11:55:42 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 23 Jun 2021 11:55:42 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 23 Jun 2021 11:55:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 23 Jun 2021 11:55:53 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 23 Jun 2021 11:55:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 23 Jun 2021 11:55:55 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Wed, 23 Jun 2021 11:55:55 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Wed, 23 Jun 2021 11:55:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Jun 2021 11:55:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Jun 2021 11:55:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 23 Jun 2021 13:07:30 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Wed, 23 Jun 2021 13:07:30 GMT
ENV PHP_VERSION=7.3.28
# Wed, 23 Jun 2021 13:07:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.28.tar.xz.asc
# Wed, 23 Jun 2021 13:07:30 GMT
ENV PHP_SHA256=a2a84dbec8c1eee3f46c5f249eaaa2ecb3f9e7a6f5d0604d2df44ff8d4904dbe
# Mon, 28 Jun 2021 22:55:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 28 Jun 2021 22:55:35 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 28 Jun 2021 23:00:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 28 Jun 2021 23:00:14 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Mon, 28 Jun 2021 23:00:15 GMT
RUN docker-php-ext-enable sodium
# Mon, 28 Jun 2021 23:00:16 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Mon, 28 Jun 2021 23:00:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 28 Jun 2021 23:00:17 GMT
STOPSIGNAL SIGWINCH
# Mon, 28 Jun 2021 23:00:17 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Mon, 28 Jun 2021 23:00:17 GMT
WORKDIR /var/www/html
# Mon, 28 Jun 2021 23:00:18 GMT
EXPOSE 80
# Mon, 28 Jun 2021 23:00:18 GMT
CMD ["apache2-foreground"]
# Tue, 29 Jun 2021 04:15:27 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Jun 2021 04:16:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 	; 		docker-php-ext-install -j "$(nproc)" 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.20; 	docker-php-ext-enable 		apcu 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Jun 2021 04:16:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 29 Jun 2021 04:16:44 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data
# Tue, 29 Jun 2021 04:16:44 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.31
# Tue, 29 Jun 2021 04:16:44 GMT
ENV MEDIAWIKI_VERSION=1.31.15
# Tue, 29 Jun 2021 04:17:00 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Jun 2021 04:17:01 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b85dd8f01492a64ab518247894d5b93db91b5ef9c770b601b37f612278b602`  
		Last Modified: Wed, 23 Jun 2021 13:53:31 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8589b26a90be6577309788924232d8900e0e44f0a7fb4ca01c32c6467578a27d`  
		Last Modified: Wed, 23 Jun 2021 13:53:50 GMT  
		Size: 76.7 MB (76680976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5af5d6419462987bdb2cd60de0729dcf0c35933ca87692f2eb9ca1ae292a642`  
		Last Modified: Wed, 23 Jun 2021 13:53:31 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614ec6f0b8d6a562071e6a2584ca97b4237364aa3b78b00aa6c601a00c80d019`  
		Last Modified: Wed, 23 Jun 2021 13:54:26 GMT  
		Size: 18.7 MB (18679261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b28f3797fbefaacc6339a39139cd689c6038bdbe1ee96bd947d58397be3538`  
		Last Modified: Wed, 23 Jun 2021 13:54:22 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96bcb7d2e6b049343069918b727a239aa0ae67500a2f20744af37dd6c89d90d9`  
		Last Modified: Wed, 23 Jun 2021 13:54:22 GMT  
		Size: 515.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e3b41f326dce12b8f49edd37cfbad64890cb4d9b4d3e98bed809d1e0586410`  
		Last Modified: Tue, 29 Jun 2021 00:51:20 GMT  
		Size: 12.5 MB (12477517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0fd0eca074e2cd94d2bb2ccf51ad5101fcffef9c961a52cbc8faacd13be377`  
		Last Modified: Tue, 29 Jun 2021 00:51:18 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfad420f634b68946cfae9cde54236c1049343e937b4ae21bd4940775219fbe1`  
		Last Modified: Tue, 29 Jun 2021 00:51:20 GMT  
		Size: 14.1 MB (14061180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4bd4cce9e4b62b54d7fbc8eeb485d08cb5ca0538e875a6e3775e0e6b54b96c2`  
		Last Modified: Tue, 29 Jun 2021 00:51:16 GMT  
		Size: 2.3 KB (2278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dc712e236b9723290bcc2f83a30c2703c507f5c9e6cc53a484bc9257082d4d`  
		Last Modified: Tue, 29 Jun 2021 00:51:16 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b25019c1023b3cb46372b881449e9f03bc515a32066f743e05a05f978c001d7`  
		Last Modified: Tue, 29 Jun 2021 00:51:16 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba8d6a6e59ff4fca53b6eacf6043c9dd75345d87f5a54880f0f6eccc8159c91`  
		Last Modified: Tue, 29 Jun 2021 00:51:16 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9114e6940e1158e2fe5eeee64e0b8e4794cf76c93960dca6c59efe565fd50b5`  
		Last Modified: Tue, 29 Jun 2021 04:24:48 GMT  
		Size: 64.4 MB (64446628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0688f15977a4085353b4c5f88e29255dee7df2bb9192d01b28f5976853738e3f`  
		Last Modified: Tue, 29 Jun 2021 04:24:37 GMT  
		Size: 2.8 MB (2771426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55ea685c1f05b135861a825f79c39b65c87ff6bdaf553a8cae0f447f2b04179`  
		Last Modified: Tue, 29 Jun 2021 04:24:36 GMT  
		Size: 314.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b0be526282cc7073cb72de6357e5770fe8a01221dcc7ead1bfc22588095394`  
		Last Modified: Tue, 29 Jun 2021 04:24:37 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944fb875c05650166b1dd55462b3a9d101ebfea9aad4a8586b9aeee38820268e`  
		Last Modified: Tue, 29 Jun 2021 04:24:46 GMT  
		Size: 36.2 MB (36209047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mediawiki:legacylts` - linux; arm variant v5

```console
$ docker pull mediawiki@sha256:fa6e48d25c6a799cece5329136c561b0bb767f7ce6c03757a4bc3425334e8b02
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.9 MB (226949479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3597fe2d4a65a271f32d1d480023d9fe880257d9b46e2f264abb2ec793af65f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 22 Jun 2021 23:50:09 GMT
ADD file:78d4ced31112d85490c684f350aceeebfc72a804262c7ad3e033257e3894f5c4 in / 
# Tue, 22 Jun 2021 23:50:11 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 06:34:32 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 23 Jun 2021 06:34:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 23 Jun 2021 06:35:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 06:35:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 23 Jun 2021 06:35:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 23 Jun 2021 06:41:07 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 23 Jun 2021 06:41:08 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 23 Jun 2021 06:41:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 23 Jun 2021 06:41:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 23 Jun 2021 06:41:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 23 Jun 2021 06:41:35 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Wed, 23 Jun 2021 06:41:35 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Wed, 23 Jun 2021 06:41:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Jun 2021 06:41:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Jun 2021 06:41:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 23 Jun 2021 07:47:33 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Wed, 23 Jun 2021 07:47:33 GMT
ENV PHP_VERSION=7.3.28
# Wed, 23 Jun 2021 07:47:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.28.tar.xz.asc
# Wed, 23 Jun 2021 07:47:34 GMT
ENV PHP_SHA256=a2a84dbec8c1eee3f46c5f249eaaa2ecb3f9e7a6f5d0604d2df44ff8d4904dbe
# Mon, 28 Jun 2021 20:05:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 28 Jun 2021 20:05:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 28 Jun 2021 20:10:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 28 Jun 2021 20:10:11 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Mon, 28 Jun 2021 20:10:13 GMT
RUN docker-php-ext-enable sodium
# Mon, 28 Jun 2021 20:10:14 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Mon, 28 Jun 2021 20:10:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 28 Jun 2021 20:10:15 GMT
STOPSIGNAL SIGWINCH
# Mon, 28 Jun 2021 20:10:16 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Mon, 28 Jun 2021 20:10:16 GMT
WORKDIR /var/www/html
# Mon, 28 Jun 2021 20:10:17 GMT
EXPOSE 80
# Mon, 28 Jun 2021 20:10:17 GMT
CMD ["apache2-foreground"]
# Mon, 28 Jun 2021 23:38:12 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 28 Jun 2021 23:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 	; 		docker-php-ext-install -j "$(nproc)" 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.20; 	docker-php-ext-enable 		apcu 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Mon, 28 Jun 2021 23:40:45 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Mon, 28 Jun 2021 23:40:47 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data
# Mon, 28 Jun 2021 23:40:47 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.31
# Mon, 28 Jun 2021 23:40:47 GMT
ENV MEDIAWIKI_VERSION=1.31.15
# Mon, 28 Jun 2021 23:41:25 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Mon, 28 Jun 2021 23:41:27 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:532d6df30af5174ac6e1b379c32b8f464d44651ac060376a560c4a76a87704a7`  
		Last Modified: Wed, 23 Jun 2021 00:01:46 GMT  
		Size: 24.9 MB (24878945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4201a900b66f4e05c8ee53ef7ecdffa56d4cfc141826c4899ba2c7ea1565c3`  
		Last Modified: Wed, 23 Jun 2021 08:37:06 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8759f5b6f404f221d7035198880caf6e5b60d43c01daf59b9c7ff32e8ba5038f`  
		Last Modified: Wed, 23 Jun 2021 08:37:51 GMT  
		Size: 58.8 MB (58820428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bee84cde96b6e1abd89640d87273fd846cad74593b3ec8bdd0167bb76f06398`  
		Last Modified: Wed, 23 Jun 2021 08:37:06 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d04a75937c26e6facc2a34e28c4f30008fb2c8c38d4a6109ab3bd73a1a4d516`  
		Last Modified: Wed, 23 Jun 2021 08:38:40 GMT  
		Size: 18.0 MB (18026172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ecd491048519ab1e7d82a3cf53d86795ba9b3b230f90332de7efe0d76f16cd`  
		Last Modified: Wed, 23 Jun 2021 08:38:29 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b63bc3f991d218876d985827b11cbce08ca267e836215529cbbfbd0a0abf7b`  
		Last Modified: Wed, 23 Jun 2021 08:38:29 GMT  
		Size: 517.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29bd5f96faa63b2a2fc210d747b6d94ff0be480eb56d30cfef0f3864a57f972a`  
		Last Modified: Mon, 28 Jun 2021 21:07:46 GMT  
		Size: 12.5 MB (12475714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5062f8e74a696beb6eee02bdb3ac7ca3b39a93eb10c27896a6c6f2ceb0f926b1`  
		Last Modified: Mon, 28 Jun 2021 21:07:42 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2996f510817471d07fef5df9c3bb79b042f3fe4d5a99413c62a01f97c2ff7059`  
		Last Modified: Mon, 28 Jun 2021 21:07:51 GMT  
		Size: 13.1 MB (13072674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b79a7bb5a216fbb8cd61824589f5d73b80f74929591f0681d57d8b4973d8959`  
		Last Modified: Mon, 28 Jun 2021 21:07:40 GMT  
		Size: 2.3 KB (2277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60572da7a9de4d65048b90c959c67fde7a157ddf5a444cf5cf729a9cedc531b8`  
		Last Modified: Mon, 28 Jun 2021 21:07:40 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2606f0c7ad54a18dc6d554bf7eab8a58b3777aa79dc8f9d9a31f5a1891353a4`  
		Last Modified: Mon, 28 Jun 2021 21:07:41 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e816dd48d3bf0fd4a22fa0d1b7326da32ae896f0a6a521693bed9ab2170758`  
		Last Modified: Mon, 28 Jun 2021 21:07:41 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ee331b7bc032d8de7567cfa24d5819b16e8baf7cd004ac1de223804fc234ac8`  
		Last Modified: Mon, 28 Jun 2021 23:53:39 GMT  
		Size: 60.8 MB (60775067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150149f17c1e382e761fac9e2ee19f7bebde8b648cbf09d3aa33384ccc4bcd9c`  
		Last Modified: Mon, 28 Jun 2021 23:53:01 GMT  
		Size: 2.7 MB (2691413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6a3ad1f4b2049f91e915e22ba9b979294654fb5f9d19d32e648a1e4971a1e8`  
		Last Modified: Mon, 28 Jun 2021 23:53:00 GMT  
		Size: 314.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1431b5ccbb065cbc4901f3cf47bad7e741576c9c9b77fb4077c0e87ecf06c46b`  
		Last Modified: Mon, 28 Jun 2021 23:53:00 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440ccb82d6dab5bfb634290b998acdf6c6c97cbcb37b61d772e068d00f34aefd`  
		Last Modified: Mon, 28 Jun 2021 23:53:39 GMT  
		Size: 36.2 MB (36202969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mediawiki:legacylts` - linux; arm variant v7

```console
$ docker pull mediawiki@sha256:dfafe74cf0bdc6e50e47037c7e2163409f1aa5b7219cc50a16e277259b62b1f9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 MB (220495173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ef51f3017e5fc33316994f9cd8be303dc386156ecbbde91da8de0be261e074`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:31 GMT
ADD file:8d200a3bbe985ff355343675c5555852f27550a9e367969df6bc98034efb8fd4 in / 
# Wed, 23 Jun 2021 00:20:31 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 08:21:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 23 Jun 2021 08:21:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 23 Jun 2021 08:22:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 08:22:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 23 Jun 2021 08:22:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 23 Jun 2021 08:27:04 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 23 Jun 2021 08:27:04 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 23 Jun 2021 08:27:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 23 Jun 2021 08:27:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 23 Jun 2021 08:27:28 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 23 Jun 2021 08:27:29 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Wed, 23 Jun 2021 08:27:29 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Wed, 23 Jun 2021 08:27:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Jun 2021 08:27:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Jun 2021 08:27:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 23 Jun 2021 10:32:05 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Wed, 23 Jun 2021 10:32:06 GMT
ENV PHP_VERSION=7.3.28
# Wed, 23 Jun 2021 10:32:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.28.tar.xz.asc
# Wed, 23 Jun 2021 10:32:07 GMT
ENV PHP_SHA256=a2a84dbec8c1eee3f46c5f249eaaa2ecb3f9e7a6f5d0604d2df44ff8d4904dbe
# Mon, 28 Jun 2021 22:05:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 28 Jun 2021 22:05:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 28 Jun 2021 22:09:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 28 Jun 2021 22:09:22 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Mon, 28 Jun 2021 22:09:24 GMT
RUN docker-php-ext-enable sodium
# Mon, 28 Jun 2021 22:09:25 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Mon, 28 Jun 2021 22:09:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 28 Jun 2021 22:09:26 GMT
STOPSIGNAL SIGWINCH
# Mon, 28 Jun 2021 22:09:27 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Mon, 28 Jun 2021 22:09:27 GMT
WORKDIR /var/www/html
# Mon, 28 Jun 2021 22:09:27 GMT
EXPOSE 80
# Mon, 28 Jun 2021 22:09:28 GMT
CMD ["apache2-foreground"]
# Tue, 29 Jun 2021 06:46:37 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Jun 2021 06:49:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 	; 		docker-php-ext-install -j "$(nproc)" 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.20; 	docker-php-ext-enable 		apcu 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Jun 2021 06:49:05 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 29 Jun 2021 06:49:07 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data
# Tue, 29 Jun 2021 06:49:07 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.31
# Tue, 29 Jun 2021 06:49:08 GMT
ENV MEDIAWIKI_VERSION=1.31.15
# Tue, 29 Jun 2021 06:49:44 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Jun 2021 06:49:46 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8452be1adf00f91570fe21a8e61aaf4c12e014daf67d7de65d984f4e8ecca2f1`  
		Last Modified: Wed, 23 Jun 2021 00:31:49 GMT  
		Size: 22.7 MB (22746055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9600bb4c83e3ef3465228eed7d6e9dfed7dc9078d2ab47f0bbdc8ccd6cb2b4`  
		Last Modified: Wed, 23 Jun 2021 11:51:40 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4b7395146be79190767115c26cc6b70ac8d5af36c4a7acf9de1f34d06b41d7`  
		Last Modified: Wed, 23 Jun 2021 11:52:18 GMT  
		Size: 59.5 MB (59514051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3641f6e3173b95d08e8b4ec00f48cb7e09d9813f88a086a422173594dfc93ddd`  
		Last Modified: Wed, 23 Jun 2021 11:51:40 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7d1aa9268ffe2596e041fe0130bbdc37fb7e587a9b8d7c5346360e2f27b41d`  
		Last Modified: Wed, 23 Jun 2021 11:53:09 GMT  
		Size: 17.5 MB (17481801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d56adf5c38075c402f8bf5f30dee3d2dd1d1f5c327b12641f29af33f5ba950a`  
		Last Modified: Wed, 23 Jun 2021 11:52:58 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17bf5eeb5d260e70dda8e6cf6bf12b837eca9e5650117ad4e659861a5ecc31f5`  
		Last Modified: Wed, 23 Jun 2021 11:52:58 GMT  
		Size: 518.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5132162a6fbe4bbd065574517d0c172ccefe7ec80b311d2e8ef43e176e3829`  
		Last Modified: Mon, 28 Jun 2021 23:47:44 GMT  
		Size: 12.5 MB (12475824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67ebbb5ecb0ac2015d09362485802a3e24e6c1e9709c0c8d6c688dbcfae0615`  
		Last Modified: Mon, 28 Jun 2021 23:47:41 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15072f3b205bed8a9843458cb709712b5801421995af9dfaa96f8f0dfc71d7e9`  
		Last Modified: Mon, 28 Jun 2021 23:47:48 GMT  
		Size: 12.4 MB (12372616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180b06e79f83f8e659df37c1b4efc98c90e67e7bf89940257a919304527bb89f`  
		Last Modified: Mon, 28 Jun 2021 23:47:39 GMT  
		Size: 2.3 KB (2278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4efd3a8bfe523fe88c2ea15411c75aef6300edb89680fee20d64ebdc4e5c3761`  
		Last Modified: Mon, 28 Jun 2021 23:47:39 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2838d7c9c746badeb44117baf4d6acc5d4c2f22bc962c7dc87a9060d5677544`  
		Last Modified: Mon, 28 Jun 2021 23:47:39 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23c7b29bfc87a94f1a3209bbb4adad494d8486d0405aa5e3689d463d0026963f`  
		Last Modified: Mon, 28 Jun 2021 23:47:39 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870bb95115d71348624c1bf4cf95d9066f5d3fdc3aad12a446fe137b405c3ab8`  
		Last Modified: Tue, 29 Jun 2021 07:07:41 GMT  
		Size: 57.1 MB (57070132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6bb476188bb295ba4d1e162327612d29d5eaf2146582f946468501979f3f844`  
		Last Modified: Tue, 29 Jun 2021 07:07:19 GMT  
		Size: 2.6 MB (2625360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495da3a50bbd40b25efcf6d7e013ecf2ae61b80a760a666e578205d12612ec9d`  
		Last Modified: Tue, 29 Jun 2021 07:07:18 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767e4fd68d2878a408ba06e0b9f1b89ed3771cef0f22e2324e2a9c22ea99fc4f`  
		Last Modified: Tue, 29 Jun 2021 07:07:18 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9e4171edc195eec6ee5c0b09907a724478bcbad1b902526d3c090193e2a8eb`  
		Last Modified: Tue, 29 Jun 2021 07:07:48 GMT  
		Size: 36.2 MB (36203231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mediawiki:legacylts` - linux; arm64 variant v8

```console
$ docker pull mediawiki@sha256:2db9434d895958f98204c168a560d09a61416ccc8c2b2b03e4ec253b6e7485a3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242296424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e8e273bab1ca562faa5fea5b6eeede3f1c17a43394a3ca4c925c27e9baf521e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 22 Jun 2021 23:49:40 GMT
ADD file:beee00b59da720f68e12e2ba2a8134207c80c777ddb4ceb03c71e3e4c3f51c93 in / 
# Tue, 22 Jun 2021 23:49:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 08:48:19 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 23 Jun 2021 08:48:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 23 Jun 2021 08:48:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 08:48:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 23 Jun 2021 08:48:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 23 Jun 2021 08:53:46 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 23 Jun 2021 08:53:47 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 23 Jun 2021 08:53:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 23 Jun 2021 08:53:56 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 23 Jun 2021 08:53:57 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 23 Jun 2021 08:53:57 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Wed, 23 Jun 2021 08:53:57 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Wed, 23 Jun 2021 08:53:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Jun 2021 08:53:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Jun 2021 08:53:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 23 Jun 2021 09:50:35 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Wed, 23 Jun 2021 09:50:35 GMT
ENV PHP_VERSION=7.3.28
# Wed, 23 Jun 2021 09:50:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.28.tar.xz.asc
# Wed, 23 Jun 2021 09:50:36 GMT
ENV PHP_SHA256=a2a84dbec8c1eee3f46c5f249eaaa2ecb3f9e7a6f5d0604d2df44ff8d4904dbe
# Mon, 28 Jun 2021 21:52:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 28 Jun 2021 21:52:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 28 Jun 2021 21:55:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 28 Jun 2021 21:55:05 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Mon, 28 Jun 2021 21:55:06 GMT
RUN docker-php-ext-enable sodium
# Mon, 28 Jun 2021 21:55:06 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Mon, 28 Jun 2021 21:55:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 28 Jun 2021 21:55:07 GMT
STOPSIGNAL SIGWINCH
# Mon, 28 Jun 2021 21:55:07 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Mon, 28 Jun 2021 21:55:07 GMT
WORKDIR /var/www/html
# Mon, 28 Jun 2021 21:55:07 GMT
EXPOSE 80
# Mon, 28 Jun 2021 21:55:08 GMT
CMD ["apache2-foreground"]
# Tue, 29 Jun 2021 01:52:28 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Jun 2021 01:53:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 	; 		docker-php-ext-install -j "$(nproc)" 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.20; 	docker-php-ext-enable 		apcu 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Jun 2021 01:53:32 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 29 Jun 2021 01:53:33 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data
# Tue, 29 Jun 2021 01:53:33 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.31
# Tue, 29 Jun 2021 01:53:34 GMT
ENV MEDIAWIKI_VERSION=1.31.15
# Tue, 29 Jun 2021 01:53:48 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Jun 2021 01:53:49 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:448f6bf000e31217a7c202c659b03b7f8ac8d3ae6b03ef7a2f8339be2f00ff4a`  
		Last Modified: Tue, 22 Jun 2021 23:55:25 GMT  
		Size: 25.9 MB (25914993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce6585fd70baac65871dafb05b7f408940165f163c30d7e0f9ec3518709e908`  
		Last Modified: Wed, 23 Jun 2021 10:25:12 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab6c01ccebb7fc71b44dfe6966672e34b47ea5e22d53a11e4481e76243cd44b`  
		Last Modified: Wed, 23 Jun 2021 10:25:24 GMT  
		Size: 70.4 MB (70356352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ed9f96098643713fabf62c17f792254db16c6623e3cec0b4a4ea602af2e742`  
		Last Modified: Wed, 23 Jun 2021 10:25:12 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6852e08c882a542c19980b469e16cebe09c20c56cb6a883fe46d7fa71c77a5bf`  
		Last Modified: Wed, 23 Jun 2021 10:26:10 GMT  
		Size: 18.6 MB (18579813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650d5012e5fa16b3bcc69043ccc3b45a8e75bd3651354579204af7abe7ae4eae`  
		Last Modified: Wed, 23 Jun 2021 10:26:01 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390447f485b4746ca973bb40b4a5ef8edc132fc2fd3b4c1e3681b22c5fa1ca47`  
		Last Modified: Wed, 23 Jun 2021 10:26:01 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0de77a2d45abd9759c2214d135511d922e74c684546d9c3f80b20d6625611d`  
		Last Modified: Mon, 28 Jun 2021 23:07:17 GMT  
		Size: 12.5 MB (12476346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ee70d280d223753c155196f8d9230d979accc1fefea6d8dfdbf5c60f39d038`  
		Last Modified: Mon, 28 Jun 2021 23:07:15 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8e54c128f3d44aff53f2548b2075ea803d3a009a36decd4ff307d4e0ae82aa`  
		Last Modified: Mon, 28 Jun 2021 23:07:16 GMT  
		Size: 13.8 MB (13752445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e1196d2e71da4277e2c0b08778bb9589392abfe22b09885a0ef98d38f915be`  
		Last Modified: Mon, 28 Jun 2021 23:07:13 GMT  
		Size: 2.3 KB (2276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2554af6ba1f35cc5528f1475dcff17f0abcbe2f708fcc8b7a53bca55a3a9e635`  
		Last Modified: Mon, 28 Jun 2021 23:07:13 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455f833d45e30000a88b814ec6fb412c064b48932cc7135af51788fdaa0d4802`  
		Last Modified: Mon, 28 Jun 2021 23:07:13 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8368f224737c59a99a51976c981b655c3c6e79f72d2635e7ccd6f6e441bdb010`  
		Last Modified: Mon, 28 Jun 2021 23:07:13 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343d099a36c562cc57434196fe8eb1cffd12bdd66bd8a54ffb54fc9f215839ad`  
		Last Modified: Tue, 29 Jun 2021 02:02:13 GMT  
		Size: 62.3 MB (62262434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a12fca55623b195bfd3cbc7875e9fb5ff8d8c3f9db7d76afe1fd54aeb62c6a72`  
		Last Modified: Tue, 29 Jun 2021 02:02:04 GMT  
		Size: 2.7 MB (2743177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57314a6e9e475a9b412743a457d5ae6196761c317ea2c8067684c224880d2c29`  
		Last Modified: Tue, 29 Jun 2021 02:02:03 GMT  
		Size: 313.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cf2d016029255f7277643f5164f75ecea6b95de84ba199348481c8c859b0ca`  
		Last Modified: Tue, 29 Jun 2021 02:02:03 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722d22ce2e8f35432471ba96ef10401667508d9d58c467791cb5d9a63aab73f5`  
		Last Modified: Tue, 29 Jun 2021 02:02:12 GMT  
		Size: 36.2 MB (36204781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mediawiki:legacylts` - linux; 386

```console
$ docker pull mediawiki@sha256:065c3f69d565e6ce09737f919b6f27aaa1cc9bb6af77f5f12876bf3015f3a8a9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.4 MB (260362986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f89c6ba87dbc9681c91c61abe4ef27de71340a30fb9f4a96ea52ac195a9bea4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 22 Jun 2021 23:39:35 GMT
ADD file:48f656ac6733911048b3de850490438d0233b3badc11861fca62062d4edfaf40 in / 
# Tue, 22 Jun 2021 23:39:35 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 09:40:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 23 Jun 2021 09:40:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 23 Jun 2021 09:40:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 09:40:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 23 Jun 2021 09:40:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 23 Jun 2021 09:49:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 23 Jun 2021 09:49:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 23 Jun 2021 09:49:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 23 Jun 2021 09:49:44 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 23 Jun 2021 09:49:46 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 23 Jun 2021 09:49:46 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Wed, 23 Jun 2021 09:49:47 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Wed, 23 Jun 2021 09:49:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Jun 2021 09:49:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Jun 2021 09:49:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 23 Jun 2021 11:32:22 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Wed, 23 Jun 2021 11:32:22 GMT
ENV PHP_VERSION=7.3.28
# Wed, 23 Jun 2021 11:32:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.28.tar.xz.asc
# Wed, 23 Jun 2021 11:32:22 GMT
ENV PHP_SHA256=a2a84dbec8c1eee3f46c5f249eaaa2ecb3f9e7a6f5d0604d2df44ff8d4904dbe
# Mon, 28 Jun 2021 23:32:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 28 Jun 2021 23:32:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 28 Jun 2021 23:36:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 28 Jun 2021 23:36:21 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Mon, 28 Jun 2021 23:36:22 GMT
RUN docker-php-ext-enable sodium
# Mon, 28 Jun 2021 23:36:23 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Mon, 28 Jun 2021 23:36:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 28 Jun 2021 23:36:24 GMT
STOPSIGNAL SIGWINCH
# Mon, 28 Jun 2021 23:36:24 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Mon, 28 Jun 2021 23:36:25 GMT
WORKDIR /var/www/html
# Mon, 28 Jun 2021 23:36:25 GMT
EXPOSE 80
# Mon, 28 Jun 2021 23:36:25 GMT
CMD ["apache2-foreground"]
# Tue, 29 Jun 2021 05:15:59 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Jun 2021 05:17:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 	; 		docker-php-ext-install -j "$(nproc)" 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.20; 	docker-php-ext-enable 		apcu 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Jun 2021 05:17:28 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 29 Jun 2021 05:17:29 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data
# Tue, 29 Jun 2021 05:17:29 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.31
# Tue, 29 Jun 2021 05:17:29 GMT
ENV MEDIAWIKI_VERSION=1.31.15
# Tue, 29 Jun 2021 05:17:48 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Jun 2021 05:17:48 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:33af2dcb865e65d53cdeb843b67a0ef62151fa32df292293e7c6b0eb728ac5ac`  
		Last Modified: Tue, 22 Jun 2021 23:46:23 GMT  
		Size: 27.8 MB (27797411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:851ded1e6779ac12f2623fa13c3d156987e0e3748e10171438e042c4a18cada8`  
		Last Modified: Wed, 23 Jun 2021 12:27:42 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9108f1298d19c1c39f13396485b32141017e3d97dcc7093d43854940c92b6c`  
		Last Modified: Wed, 23 Jun 2021 12:28:14 GMT  
		Size: 81.2 MB (81230041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a8cc691843125fa492ce4109092746e47e36d222eceef5b59dd10271176374`  
		Last Modified: Wed, 23 Jun 2021 12:27:42 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ce571916f9fd350c507c0b0f4ba7db9c473cb95da721dfeab5acd167c05197`  
		Last Modified: Wed, 23 Jun 2021 12:29:05 GMT  
		Size: 19.1 MB (19115037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7abad9c9b3f342c41ff79e0b1832309d795f17e4aaafd51a979891c9c747684c`  
		Last Modified: Wed, 23 Jun 2021 12:28:58 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ecb5db768b6cdd9c3b371c253bc49fc82700b113499943217799b6cf74aab9`  
		Last Modified: Wed, 23 Jun 2021 12:28:58 GMT  
		Size: 516.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4d62125c4092fd1f65b85eb0225935afcddd2326bc45cef99fe303c2867cbb`  
		Last Modified: Tue, 29 Jun 2021 01:34:37 GMT  
		Size: 12.5 MB (12476922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70fcef0bbdac3118f1d82c323dfe7892f282e96891600b973f6ac2d0f6657482`  
		Last Modified: Tue, 29 Jun 2021 01:34:35 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb2af70ee017de058b3c68ff3264c207a165f28d88ede5084c2e87de27d4170`  
		Last Modified: Tue, 29 Jun 2021 01:34:37 GMT  
		Size: 14.4 MB (14363234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d243ac8d40ccac0048faff0f394670c829fbf9222952a3ab8b9f309e999e49`  
		Last Modified: Tue, 29 Jun 2021 01:34:33 GMT  
		Size: 2.3 KB (2276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f041db4759255d1a36b553611d061506fe50ae334ba918ad7c78ebc79535208a`  
		Last Modified: Tue, 29 Jun 2021 01:34:33 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e7b446e0a968a82412d9c055bdee47123d8ec6bb075d8b5161fe91fc0ba7373`  
		Last Modified: Tue, 29 Jun 2021 01:34:33 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d8ca4f4f3c1bffab68383152169b1bacc01dd6f94f74330916cddbf70321f5`  
		Last Modified: Tue, 29 Jun 2021 01:34:32 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3aae7082247054a616a03a01c4ecdd41ba57f6b01bf7498596b131b0ba3b09`  
		Last Modified: Tue, 29 Jun 2021 05:27:34 GMT  
		Size: 66.4 MB (66394684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de6e5efee31e81ee1017c70ef62c8bb81cd246ff85fda79faaf90b1d227e62f`  
		Last Modified: Tue, 29 Jun 2021 05:27:18 GMT  
		Size: 2.8 MB (2772846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344cc66e7ebb8dde3f4e3a944258b96f1ded29982afe6605368335a40d420f34`  
		Last Modified: Tue, 29 Jun 2021 05:27:17 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db9aaf16ed224ad5421a1c9c1bf1d83108536431393c5514b23d7040b910d725`  
		Last Modified: Tue, 29 Jun 2021 05:27:17 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce03881701675573a1780383a475d0b84a7728240343388476bd8966b06998d`  
		Last Modified: Tue, 29 Jun 2021 05:27:31 GMT  
		Size: 36.2 MB (36206712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mediawiki:legacylts` - linux; ppc64le

```console
$ docker pull mediawiki@sha256:af2ef7ad6c2740e7294757a49e814475a05a0d29c0e8218fe0298824847857e4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270614054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f50947a16daac05e8f757b0a879a7e560b7b9b12f96fccb809c3ddee037e48`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 23 Jun 2021 00:30:38 GMT
ADD file:e599654230c9fe95fe2c591dbe60e8a0a886cd053b6117230fbae47561145731 in / 
# Wed, 23 Jun 2021 00:30:46 GMT
CMD ["bash"]
# Sat, 26 Jun 2021 04:04:21 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 26 Jun 2021 04:04:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 26 Jun 2021 04:09:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 26 Jun 2021 04:09:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 26 Jun 2021 04:09:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 26 Jun 2021 04:24:20 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 26 Jun 2021 04:24:28 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 26 Jun 2021 04:26:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 26 Jun 2021 04:26:31 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 26 Jun 2021 04:26:44 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 26 Jun 2021 04:26:47 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 26 Jun 2021 04:26:53 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 26 Jun 2021 04:26:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 26 Jun 2021 04:27:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 26 Jun 2021 04:27:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 26 Jun 2021 07:55:11 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Sat, 26 Jun 2021 07:55:17 GMT
ENV PHP_VERSION=7.3.28
# Sat, 26 Jun 2021 07:55:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.28.tar.xz.asc
# Sat, 26 Jun 2021 07:55:32 GMT
ENV PHP_SHA256=a2a84dbec8c1eee3f46c5f249eaaa2ecb3f9e7a6f5d0604d2df44ff8d4904dbe
# Sat, 26 Jun 2021 07:57:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 26 Jun 2021 07:57:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 26 Jun 2021 08:04:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 26 Jun 2021 08:04:46 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Sat, 26 Jun 2021 08:05:03 GMT
RUN docker-php-ext-enable sodium
# Sat, 26 Jun 2021 08:05:18 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Sat, 26 Jun 2021 08:05:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 26 Jun 2021 08:05:30 GMT
STOPSIGNAL SIGWINCH
# Sat, 26 Jun 2021 08:05:33 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 26 Jun 2021 08:05:38 GMT
WORKDIR /var/www/html
# Sat, 26 Jun 2021 08:05:42 GMT
EXPOSE 80
# Sat, 26 Jun 2021 08:05:46 GMT
CMD ["apache2-foreground"]
# Sun, 27 Jun 2021 13:10:06 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 27 Jun 2021 13:12:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 	; 		docker-php-ext-install -j "$(nproc)" 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.20; 	docker-php-ext-enable 		apcu 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Sun, 27 Jun 2021 13:12:41 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sun, 27 Jun 2021 13:13:18 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data
# Sun, 27 Jun 2021 13:13:27 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.31
# Mon, 28 Jun 2021 17:40:49 GMT
ENV MEDIAWIKI_VERSION=1.31.15
# Mon, 28 Jun 2021 17:42:23 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Mon, 28 Jun 2021 17:42:37 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f9cb1946299ce1824ee44809cd0c8b419528fee2f0f89e86400787a14b666f59`  
		Last Modified: Wed, 23 Jun 2021 00:37:07 GMT  
		Size: 30.6 MB (30553627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bede12a66c305ed12d280c6b7a6022061a73d9568433f643b06ec9893f790c0`  
		Last Modified: Sat, 26 Jun 2021 09:01:49 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b569ead47e80d494e6f64ea9e5b97bcc6a4d42355effc0aedead32f63c7ba733`  
		Last Modified: Sat, 26 Jun 2021 09:03:27 GMT  
		Size: 82.3 MB (82291015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b0e4b30eb84311f540a9331dfc8db99c35e188d1fc36e8862ed80fd320c431`  
		Last Modified: Sat, 26 Jun 2021 09:01:48 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0be226e932ae202655cabfbdf039de068fd0668bc10270960d28e04010caf9d`  
		Last Modified: Sat, 26 Jun 2021 09:04:48 GMT  
		Size: 19.8 MB (19818544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a6a8c2dc286478f193e642b39db64063501e03463223f793d17bf4b4d548a4`  
		Last Modified: Sat, 26 Jun 2021 09:04:35 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d8e7e98a0047f2938ddec0785e0b8a93b3b086bfd03f29c6d1a903ec5bfd69`  
		Last Modified: Sat, 26 Jun 2021 09:04:35 GMT  
		Size: 517.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cae82816334191ffa0d305fa891d046c6a3d99bfef43fcc7a452887cb355df`  
		Last Modified: Sat, 26 Jun 2021 09:14:56 GMT  
		Size: 12.5 MB (12477663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c978da0ab05a47dd5319dd2a0eab7b34796e6ae3371dd76aaca963ab2fa781`  
		Last Modified: Sat, 26 Jun 2021 09:14:54 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a3fbb448097d7ed5f3716795916f28984d03f74715be07f339fc2b3ce88f27`  
		Last Modified: Sat, 26 Jun 2021 09:14:56 GMT  
		Size: 15.1 MB (15100639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95f607e772b8ee087139614c120a018a19840d64b5bd9b9f6c064f9030c6f69`  
		Last Modified: Sat, 26 Jun 2021 09:14:51 GMT  
		Size: 2.3 KB (2278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc41b7e378268c3f30451fb1dc1388d61423d74111c9c04df5599423c8f5993`  
		Last Modified: Sat, 26 Jun 2021 09:14:51 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ff35b7f7658d4dc75495df66154050bde8190bfa1e7f5bb3d020e6ef32485e`  
		Last Modified: Sat, 26 Jun 2021 09:14:51 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b02473ac89d969690176dfbdd44feb3d2dab92916151ea0054c085df9717e0`  
		Last Modified: Sat, 26 Jun 2021 09:14:51 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c96cce52186cc8134b0a9305ee7346f09c3bc18855bad44ec5470aa090adea5`  
		Last Modified: Sun, 27 Jun 2021 13:54:01 GMT  
		Size: 71.3 MB (71300450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a19015328c0193a6b2ae19a2690530fe5e665e02f17835d825475335d315e2`  
		Last Modified: Sun, 27 Jun 2021 13:52:04 GMT  
		Size: 2.9 MB (2854264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f329dc9ba4d7fd946c6911220155809682ecc6e20ad12dcb9302d57a989a7b`  
		Last Modified: Sun, 27 Jun 2021 13:51:59 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e126c8403008a8cfc8a899cdfb227bcba76e0c6a3542e1baa6ceee754676326`  
		Last Modified: Sun, 27 Jun 2021 13:51:58 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507c4ef5cc67195b5cd69b451007d2526c9f849ee01b988126d9474d9a1813c9`  
		Last Modified: Mon, 28 Jun 2021 17:56:48 GMT  
		Size: 36.2 MB (36211755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
