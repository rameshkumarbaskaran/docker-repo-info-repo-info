## `php:apache-buster`

```console
$ docker pull php@sha256:81cd8b2cec83d54b79a108e84f78782e19c55634d881a94684c761bad4c15087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `php:apache-buster` - linux; amd64

```console
$ docker pull php@sha256:b71f8e54e65eb981f0b4bf99bf883be9a2765393fb3b0d40fbea0e0fc4ec26bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146178176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d3fb8d7ee58f6dc37140bcf624c2da715e191bfe7273b40b4954283b2fea28`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 May 2023 01:20:37 GMT
ADD file:2058e04b33179527a56999678c1c62dfcf76944675afcd77b5163141fb025f8c in / 
# Tue, 23 May 2023 01:20:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 09:49:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 May 2023 09:49:53 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 May 2023 09:50:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 09:50:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 May 2023 09:50:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 May 2023 09:53:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 23 May 2023 09:53:31 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 23 May 2023 09:53:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 23 May 2023 09:53:41 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 23 May 2023 09:53:42 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 23 May 2023 09:53:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 09:53:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 09:53:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 May 2023 09:53:42 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 23 May 2023 09:53:42 GMT
ENV PHP_VERSION=8.2.6
# Tue, 23 May 2023 09:53:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.6.tar.xz.asc
# Tue, 23 May 2023 09:53:42 GMT
ENV PHP_SHA256=10b796f0ed45574229851212b30a596a76e70ae365322bcaaaf9c00fa7d58cca
# Tue, 23 May 2023 09:53:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 23 May 2023 09:53:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 23 May 2023 09:56:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 23 May 2023 09:56:53 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 23 May 2023 09:56:54 GMT
RUN docker-php-ext-enable sodium
# Tue, 23 May 2023 09:56:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 23 May 2023 09:56:54 GMT
STOPSIGNAL SIGWINCH
# Tue, 23 May 2023 09:56:54 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 23 May 2023 09:56:54 GMT
WORKDIR /var/www/html
# Tue, 23 May 2023 09:56:54 GMT
EXPOSE 80
# Tue, 23 May 2023 09:56:54 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:99bf4787315b60d97d860ac6d006b7835b2241a601e93c2da4af6ca554be8704`  
		Last Modified: Tue, 23 May 2023 01:24:47 GMT  
		Size: 27.1 MB (27138577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55ada1538ae196b25fb974bc489a28592c4e563e5a4a142019da8a502fe84de`  
		Last Modified: Tue, 23 May 2023 10:58:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1deafc62e11b7180330eb4bad22f026f77a0b73e54fcbc51c3d33a91a58ac6`  
		Last Modified: Tue, 23 May 2023 10:58:11 GMT  
		Size: 76.7 MB (76694428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a88ed5b391830f741f158fcfe5f6fc1fd3c12fd510b68e05634de91e8402ec0`  
		Last Modified: Tue, 23 May 2023 10:58:00 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58fe0b2f048be60c1a67a3feb39f923f9d70bd2bd02dfec5345d10d83bef83e6`  
		Last Modified: Tue, 23 May 2023 10:58:39 GMT  
		Size: 18.7 MB (18689849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74f624d861f17bfe8452a39aaa6b604f3ec32548175086320beabbc28e1304e`  
		Last Modified: Tue, 23 May 2023 10:58:36 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a2658f0454892c01b65e280148f40371cfe61e873bd89c6b4d7be81d1ee27b`  
		Last Modified: Tue, 23 May 2023 10:58:36 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c209201ce682fb7538f6365f85769fb80f81aae60d268ed957695b1c6dc509de`  
		Last Modified: Tue, 23 May 2023 10:58:37 GMT  
		Size: 12.4 MB (12355148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14a6f09e1bd2d2ff0746bb2e1b441286737b03c4941fab0516f067e7d9ba19c`  
		Last Modified: Tue, 23 May 2023 10:58:34 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20915f785f58b7f07fe88213fc32f51864a4c23be1b8f5588ce6cda97ea7219e`  
		Last Modified: Tue, 23 May 2023 10:58:36 GMT  
		Size: 11.3 MB (11294599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e099a7c60850a8c1a0658d706c3cd3c7414350a0d583af83f9a5f8b2ef3a083`  
		Last Modified: Tue, 23 May 2023 10:58:34 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2a47dbbb0deb87faecd183678df1f10eaf84200dc42ff2ab5717cb04ccb6c2`  
		Last Modified: Tue, 23 May 2023 10:58:34 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cee52681db83c3dc335ae3e308490ac185715a6d106776d531f34dbd5df068`  
		Last Modified: Tue, 23 May 2023 10:58:35 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:apache-buster` - linux; arm variant v7

```console
$ docker pull php@sha256:f782c6470040e1020c7552bd1c1a2b6493b94931de7d96c8a59cf6cc6312ec9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121903915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08adf9af05fd1af322181dc2a8fd0ab90503bcb0b7aaf5b793b8539921fe191a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 May 2023 00:58:17 GMT
ADD file:fc75413703cf08c1fc3b981ebbde07494b7ad8176aadd5f3a8fb891f0c48e7b9 in / 
# Tue, 23 May 2023 00:58:17 GMT
CMD ["bash"]
# Tue, 23 May 2023 07:08:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 May 2023 07:08:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 May 2023 07:08:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:08:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 May 2023 07:08:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 May 2023 07:11:32 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 23 May 2023 07:11:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 23 May 2023 07:11:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 23 May 2023 07:11:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 23 May 2023 07:11:46 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 23 May 2023 07:11:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 07:11:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 07:11:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 May 2023 07:11:46 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 23 May 2023 07:11:46 GMT
ENV PHP_VERSION=8.2.6
# Tue, 23 May 2023 07:11:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.6.tar.xz.asc
# Tue, 23 May 2023 07:11:46 GMT
ENV PHP_SHA256=10b796f0ed45574229851212b30a596a76e70ae365322bcaaaf9c00fa7d58cca
# Tue, 23 May 2023 07:11:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 23 May 2023 07:11:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 23 May 2023 07:14:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 23 May 2023 07:14:23 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 23 May 2023 07:14:24 GMT
RUN docker-php-ext-enable sodium
# Tue, 23 May 2023 07:14:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 23 May 2023 07:14:24 GMT
STOPSIGNAL SIGWINCH
# Tue, 23 May 2023 07:14:24 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 23 May 2023 07:14:24 GMT
WORKDIR /var/www/html
# Tue, 23 May 2023 07:14:24 GMT
EXPOSE 80
# Tue, 23 May 2023 07:14:25 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:0265ca860f8350954d0667b45b48728e992970f63232c58e18fac59852acd8f2`  
		Last Modified: Tue, 23 May 2023 01:02:24 GMT  
		Size: 22.7 MB (22747412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f10be44c42d6f52275fb4bd6b7b823e71b5d1b0be9ea2185ea7bc5fc43d2e7`  
		Last Modified: Tue, 23 May 2023 08:05:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5517eac767ab2d3e917293eebc32246985d11c0669208b3eb6f20b6e8762c734`  
		Last Modified: Tue, 23 May 2023 08:05:20 GMT  
		Size: 59.5 MB (59544070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4d3e7966887bf66ea9d17b8172aa32c6ce946bef167eba1bd57fb8a2f3093b`  
		Last Modified: Tue, 23 May 2023 08:05:10 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7215c0a9558dac978bceff627fa05026968e09a011b4b1d8c04f5468fdab476`  
		Last Modified: Tue, 23 May 2023 08:05:48 GMT  
		Size: 17.5 MB (17481878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33491e52156a26faba0e26ac3cdd10f2769f1fc8b75d8f81690d15c947e1bc49`  
		Last Modified: Tue, 23 May 2023 08:05:45 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6934476b06beca7ea9b9b23a6f10911ebaafbf25050c6592ebc54916ba1c5b`  
		Last Modified: Tue, 23 May 2023 08:05:45 GMT  
		Size: 516.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0048d99e7a1904e0cac594fc996d934a2ffba16a91f40248fe33b6b2e6a73e3`  
		Last Modified: Tue, 23 May 2023 08:05:46 GMT  
		Size: 12.4 MB (12353083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72640157c8ef448d00fd55a81f17e35a157dff91c66b989fb8dc232b6ea09e9`  
		Last Modified: Tue, 23 May 2023 08:05:43 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929233e31521f61b138a49d6a8f41e52680eec818fb2bbda60fa559c63aca1c1`  
		Last Modified: Tue, 23 May 2023 08:05:46 GMT  
		Size: 9.8 MB (9771887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30702e5e8d1309b2b25bf90f96affaec04e180504784585b03b35e13b47c0ce5`  
		Last Modified: Tue, 23 May 2023 08:05:43 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ee21d22a9ea3efb653a50b8769115aa4fb6ee54e1e1b174995714a32a06a42`  
		Last Modified: Tue, 23 May 2023 08:05:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11dad80b16ed37f4184d94b14595b6075a1e83f59b5a4fed459febfcbe278b55`  
		Last Modified: Tue, 23 May 2023 08:05:43 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:apache-buster` - linux; arm64 variant v8

```console
$ docker pull php@sha256:3e2a3b59a5aa29dd677e4ad7063d8d485016c6db0f2960b6a6c1831d41afa15b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138609155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd77574ef52d57747360a034c8940aac37ca36e172a6954f012ec3d1a99faa3e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 May 2023 00:43:28 GMT
ADD file:55a469039df0bf0e94ef7cd2d6fd355ad0c69e0e23e7921194445dd1fe281e3b in / 
# Tue, 23 May 2023 00:43:28 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:23:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 May 2023 04:23:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 May 2023 04:23:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 04:23:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 May 2023 04:23:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 May 2023 04:27:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 23 May 2023 04:27:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 23 May 2023 04:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 23 May 2023 04:27:36 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 23 May 2023 04:27:36 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 23 May 2023 04:27:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 04:27:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 04:27:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 May 2023 04:27:36 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 23 May 2023 04:27:37 GMT
ENV PHP_VERSION=8.2.6
# Tue, 23 May 2023 04:27:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.6.tar.xz.asc
# Tue, 23 May 2023 04:27:37 GMT
ENV PHP_SHA256=10b796f0ed45574229851212b30a596a76e70ae365322bcaaaf9c00fa7d58cca
# Tue, 23 May 2023 04:27:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 23 May 2023 04:27:47 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 23 May 2023 04:30:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 23 May 2023 04:30:54 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 23 May 2023 04:30:55 GMT
RUN docker-php-ext-enable sodium
# Tue, 23 May 2023 04:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 23 May 2023 04:30:55 GMT
STOPSIGNAL SIGWINCH
# Tue, 23 May 2023 04:30:55 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 23 May 2023 04:30:55 GMT
WORKDIR /var/www/html
# Tue, 23 May 2023 04:30:55 GMT
EXPOSE 80
# Tue, 23 May 2023 04:30:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3ca7b6c7180eac66b9c4301084a16319f41eb7f7365bdf91bcc272bd24cb4149`  
		Last Modified: Tue, 23 May 2023 00:46:44 GMT  
		Size: 25.9 MB (25921744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9b52276f9677dd50f8ec4feda3892eb7c995d3979af3d26a6b4c7a17c43f7e`  
		Last Modified: Tue, 23 May 2023 05:23:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18db47d2f311cb982b22e58c7c13d6a0951f563df1e87747319389823ee445c8`  
		Last Modified: Tue, 23 May 2023 05:23:50 GMT  
		Size: 70.4 MB (70366540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ff8177973c852a42f375db0f3bd2ab12cb0e13c0653f83691745524cb09cc6`  
		Last Modified: Tue, 23 May 2023 05:23:42 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0895005af0e1c480f636e2e952f4e5d50503e5a78edae0327d95fe2fbcc7866e`  
		Last Modified: Tue, 23 May 2023 05:24:14 GMT  
		Size: 18.6 MB (18587106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a918da20b0fb64042d86f1885f1240c0e489532c40b303fffe818b407e092f6`  
		Last Modified: Tue, 23 May 2023 05:24:12 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3cb02374b91e069a07701f09049791d56f83ce345a0e351bcec67ccb5308e60`  
		Last Modified: Tue, 23 May 2023 05:24:12 GMT  
		Size: 514.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343b14f1f6cee750f17cab717bae804eac0bc7279cd36481c80b4c2f237247f3`  
		Last Modified: Tue, 23 May 2023 05:24:13 GMT  
		Size: 12.4 MB (12353935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2b95b35d2540cb2e4d8f892692162125e2260da54914e3a84a4cc69fae7498`  
		Last Modified: Tue, 23 May 2023 05:24:10 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e6abba8ce1324afdc403ff74b969ff8916626ed79dc4d7383c33c7094db710`  
		Last Modified: Tue, 23 May 2023 05:24:12 GMT  
		Size: 11.4 MB (11374254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc03827dd0344a8f7da465e1ecd678625e9a92346a33c3d711268a71a189e58`  
		Last Modified: Tue, 23 May 2023 05:24:10 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c41bd0ff991f8c120e9d1ff28fe9aec77e4456600b94af2963ad79b8b53017`  
		Last Modified: Tue, 23 May 2023 05:24:10 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c59cd52124976feacf995cc4c7de3ab2a916d6a79739b6f32cdb1fc2e8611c5`  
		Last Modified: Tue, 23 May 2023 05:24:10 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:apache-buster` - linux; 386

```console
$ docker pull php@sha256:865ef17e90f8249b0085d4eb500cdc42f9f3b54c1d60c219e95db21196d3783e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (152045817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64163a50fc2cdef560fa89f9208aa8a23147ae5205c821ea34c1c90a88e4f43a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 May 2023 00:40:01 GMT
ADD file:96715cff0e3569a2a1d7e203f0797ed4880da7714d455e25f032c67bff27221f in / 
# Tue, 23 May 2023 00:40:01 GMT
CMD ["bash"]
# Tue, 23 May 2023 12:59:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 May 2023 12:59:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 May 2023 13:00:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 13:00:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 May 2023 13:00:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 May 2023 13:05:49 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 23 May 2023 13:05:49 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 23 May 2023 13:06:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 23 May 2023 13:06:04 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 23 May 2023 13:06:05 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 23 May 2023 13:06:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 13:06:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 13:06:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 May 2023 13:06:05 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 23 May 2023 13:06:06 GMT
ENV PHP_VERSION=8.2.6
# Tue, 23 May 2023 13:06:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.6.tar.xz.asc
# Tue, 23 May 2023 13:06:06 GMT
ENV PHP_SHA256=10b796f0ed45574229851212b30a596a76e70ae365322bcaaaf9c00fa7d58cca
# Tue, 23 May 2023 13:06:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 23 May 2023 13:06:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 23 May 2023 13:11:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 23 May 2023 13:11:17 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 23 May 2023 13:11:18 GMT
RUN docker-php-ext-enable sodium
# Tue, 23 May 2023 13:11:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 23 May 2023 13:11:18 GMT
STOPSIGNAL SIGWINCH
# Tue, 23 May 2023 13:11:18 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 23 May 2023 13:11:18 GMT
WORKDIR /var/www/html
# Tue, 23 May 2023 13:11:18 GMT
EXPOSE 80
# Tue, 23 May 2023 13:11:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3c2058520f8e2dee0c8d97a0e68335849888066e5d0d1b82b6ef302541b5c874`  
		Last Modified: Tue, 23 May 2023 00:45:13 GMT  
		Size: 27.8 MB (27797210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1266a4baadae5ef59725941c991dc5adfa2ed13e7cf3fdd85cc6f709265af87`  
		Last Modified: Tue, 23 May 2023 14:48:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e7447771f969594fe1e4ee64c72e57aa11c42c64255e08710ee80d2b15547d8`  
		Last Modified: Tue, 23 May 2023 14:48:21 GMT  
		Size: 81.2 MB (81239303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c108971a278f401b281b6f0afe922e69a4d522140c9166362e30c6967a76bde6`  
		Last Modified: Tue, 23 May 2023 14:48:03 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46984934df11afc596d6bf8ab7a85398be55d56e014aaa633db188e2f7a6603`  
		Last Modified: Tue, 23 May 2023 14:48:51 GMT  
		Size: 19.1 MB (19117697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1040aba079dfe102c3287d7c3e0dc8670058256d41885c5f9840a474e9aa754`  
		Last Modified: Tue, 23 May 2023 14:48:47 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5cc15d0327b6b0bd19cb07e50d8a9581949b526b796aae521f0cebcc129d75`  
		Last Modified: Tue, 23 May 2023 14:48:47 GMT  
		Size: 517.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e080991e588bf8e0b4b34174cb441fa75215b833aa20addbab4cd14b01eb73`  
		Last Modified: Tue, 23 May 2023 14:48:49 GMT  
		Size: 12.4 MB (12354448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ed0995495ed108d5eea7ba35ee0e88631389df9629106796c6c36f4d61398b`  
		Last Modified: Tue, 23 May 2023 14:48:45 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5309ed7ad5cbd21db413d4e23d7537d2c86d94563a61f8f504516edecbe863e8`  
		Last Modified: Tue, 23 May 2023 14:48:49 GMT  
		Size: 11.5 MB (11531582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adfb2b90e2d6b026c388a10db3cf8d0c38a01f070b76aa003ba91251687c7721`  
		Last Modified: Tue, 23 May 2023 14:48:45 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec3c8bbb69db1b4fa27ea94f1e877d116660c8d331eaed8cd38016d911028e3`  
		Last Modified: Tue, 23 May 2023 14:48:45 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f000325791f444ccc451ec7b79063eb53dba343efa93463f8e54690f9004389`  
		Last Modified: Tue, 23 May 2023 14:48:45 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
