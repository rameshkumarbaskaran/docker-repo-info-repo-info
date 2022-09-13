## `php:apache-buster`

```console
$ docker pull php@sha256:12d8e9d743666b85e23eb71159e68ae01ab924bef9a253100eb458741e5655dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `php:apache-buster` - linux; amd64

```console
$ docker pull php@sha256:95317ddc94409ebd2c5f20b118f85133e138c33fcef4058ba5f43e51c7248c46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.6 MB (145632157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0f9816466c798f297011a05f8601586049e1cbcc22967d777bfc8b52eb4eed`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:48 GMT
ADD file:782d864aa72c2d5fb599311ebae56db4067d2e91ff532c1aaf1a291c3dbce5bb in / 
# Tue, 13 Sep 2022 00:56:49 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 09:58:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Sep 2022 09:58:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Sep 2022 09:58:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 09:58:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Sep 2022 09:58:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 13 Sep 2022 10:02:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 13 Sep 2022 10:02:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 13 Sep 2022 10:02:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 13 Sep 2022 10:02:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 13 Sep 2022 10:02:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 13 Sep 2022 10:02:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Sep 2022 10:02:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Sep 2022 10:02:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Sep 2022 10:28:51 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 13 Sep 2022 10:28:52 GMT
ENV PHP_VERSION=8.1.10
# Tue, 13 Sep 2022 10:28:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.10.tar.xz.asc
# Tue, 13 Sep 2022 10:28:52 GMT
ENV PHP_SHA256=90e7120c77ee83630e6ac928d23bc6396603d62d83a3cf5df8a450d2e3070162
# Tue, 13 Sep 2022 10:29:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 13 Sep 2022 10:29:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 13 Sep 2022 10:32:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 13 Sep 2022 10:32:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 13 Sep 2022 10:32:03 GMT
RUN docker-php-ext-enable sodium
# Tue, 13 Sep 2022 10:32:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Sep 2022 10:32:04 GMT
STOPSIGNAL SIGWINCH
# Tue, 13 Sep 2022 10:32:04 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 13 Sep 2022 10:32:04 GMT
WORKDIR /var/www/html
# Tue, 13 Sep 2022 10:32:04 GMT
EXPOSE 80
# Tue, 13 Sep 2022 10:32:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4b7b4a8876e2f677668e51b8473f97a237d3d4df201b9df4031bcaa8068370b1`  
		Last Modified: Tue, 13 Sep 2022 01:01:16 GMT  
		Size: 27.1 MB (27130552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7926108d61967de3c3b394f117df9a36ef11dcc7cc15729265869f6e5318a82e`  
		Last Modified: Tue, 13 Sep 2022 11:30:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a32af496e5b7b67ea2e864ade872ec4811aa871eb14dd3dd8e1cdfb3acc5427`  
		Last Modified: Tue, 13 Sep 2022 11:30:20 GMT  
		Size: 76.7 MB (76685702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48af7de5a6952f43c58d2fb6f3a24ee447392b1bf3d720a9ec69b690c7717ae7`  
		Last Modified: Tue, 13 Sep 2022 11:30:08 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa4808661da9ef3a05ed6368fbf9d8dd15cba9c3a812d28b227f66b14de5684`  
		Last Modified: Tue, 13 Sep 2022 11:30:41 GMT  
		Size: 18.7 MB (18682052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd0cd632b13a6c1270788d4626fe9eae2b513f2ea1be092d8f5b05ab55124561`  
		Last Modified: Tue, 13 Sep 2022 11:30:38 GMT  
		Size: 485.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2248ede2395b89c0e8f3585bf3297c39ff9df8f1e3729213bd33fcb61b9d68df`  
		Last Modified: Tue, 13 Sep 2022 11:30:38 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a896a79b2f7071fefd74d8f43d0a2adda8beda9950839ba917ef614ff9cdeb28`  
		Last Modified: Tue, 13 Sep 2022 11:35:54 GMT  
		Size: 12.1 MB (12074449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4240468f8f3c2f2fe5577f9ef502c7cbbc5b3e7fa37ec278594c892a735c8ab7`  
		Last Modified: Tue, 13 Sep 2022 11:35:51 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3937f4a1e18842d293992c5fcb4ba34d07c84b9c29af3f0694c997f573187b69`  
		Last Modified: Tue, 13 Sep 2022 11:35:53 GMT  
		Size: 11.1 MB (11053818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8c76aa969dc990c6807c37c463b46f364b5b3202c7daa9b786a10a5bf35584`  
		Last Modified: Tue, 13 Sep 2022 11:35:51 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acee180c2725faf40061b50886703d1fc255bd7bd066da37f57a726856087b0a`  
		Last Modified: Tue, 13 Sep 2022 11:35:51 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30614793ae26660d821608fbec648c5a55dfbdedd2009b76be26bec701b3a907`  
		Last Modified: Tue, 13 Sep 2022 11:35:51 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:apache-buster` - linux; arm variant v7

```console
$ docker pull php@sha256:de38386307d634cf7237b8e102f12373e0a64e016999f67ead109a2a51885bb2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121701927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4c270bf2720cb0d9de0f8babc3f7c906220a9a092a8e2f972e9de8e4fc7d3f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 Aug 2022 01:43:37 GMT
ADD file:8d67c07b9926dee5d0124e48bd4b5039e6a84fdfe07a9e1077392f0e5772aa52 in / 
# Tue, 23 Aug 2022 01:43:37 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:31:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 Aug 2022 02:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 Aug 2022 02:31:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:31:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 Aug 2022 02:31:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 23 Aug 2022 02:39:57 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 23 Aug 2022 02:39:57 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 23 Aug 2022 02:40:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 23 Aug 2022 02:40:07 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 23 Aug 2022 02:40:08 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 23 Aug 2022 02:40:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Aug 2022 02:40:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Aug 2022 02:40:08 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 Aug 2022 03:46:45 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 02 Sep 2022 01:48:18 GMT
ENV PHP_VERSION=8.1.10
# Fri, 02 Sep 2022 01:48:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.10.tar.xz.asc
# Fri, 02 Sep 2022 01:48:19 GMT
ENV PHP_SHA256=90e7120c77ee83630e6ac928d23bc6396603d62d83a3cf5df8a450d2e3070162
# Fri, 02 Sep 2022 01:48:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 02 Sep 2022 01:48:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 02 Sep 2022 02:00:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 02 Sep 2022 02:00:53 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 02 Sep 2022 02:00:54 GMT
RUN docker-php-ext-enable sodium
# Fri, 02 Sep 2022 02:00:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 02 Sep 2022 02:00:54 GMT
STOPSIGNAL SIGWINCH
# Fri, 02 Sep 2022 02:00:54 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 02 Sep 2022 02:00:55 GMT
WORKDIR /var/www/html
# Fri, 02 Sep 2022 02:00:55 GMT
EXPOSE 80
# Fri, 02 Sep 2022 02:00:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:838efeda083c4fc3f1262c9c56947c82c6fdb90b64993afdb1375ce01ce1724b`  
		Last Modified: Tue, 23 Aug 2022 01:51:00 GMT  
		Size: 22.7 MB (22746698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe4753428f89a5320662dacc8d10205e22afeea15ffc2e7fab74bc08e09d2f6`  
		Last Modified: Tue, 23 Aug 2022 08:43:22 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e2fe2eb11c0a68ddfc755d2e827770c1c2e6c5bc34ab4b5561c873ea6f5a33`  
		Last Modified: Tue, 23 Aug 2022 08:43:40 GMT  
		Size: 59.5 MB (59539162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98cd239e9ce6cedffe94233fa238a0294d5809db09ce46824f557c32615ebea3`  
		Last Modified: Tue, 23 Aug 2022 08:43:22 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fc1f2ec7b24e8b6d3982c1d9f0e450f345c16c1d67aace932ffdc0778c78b1`  
		Last Modified: Tue, 23 Aug 2022 08:44:07 GMT  
		Size: 17.5 MB (17479484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1cba638cc5b255aa1fef65868a9bf9fd7eee13a8875f69280442333be37d34`  
		Last Modified: Tue, 23 Aug 2022 08:44:02 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf890e5511f88a70dd71e2c42569761f68dbc05607b7e57ae5e23ed59661061`  
		Last Modified: Tue, 23 Aug 2022 08:44:02 GMT  
		Size: 514.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7494a6086c701531622c2a31311e7fa6b2fcd9706033a74feec79d68b58339d`  
		Last Modified: Fri, 02 Sep 2022 05:28:11 GMT  
		Size: 12.1 MB (12072298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6ee0987484a5539fc34e6eb606b70f4af6e77d18f033f9ca6ca1623fd26d80`  
		Last Modified: Fri, 02 Sep 2022 05:28:08 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd7e13fdc12eba7665d61cc196fbd4d0812bb8afa2b7d0517506982d078000b`  
		Last Modified: Fri, 02 Sep 2022 05:28:10 GMT  
		Size: 9.9 MB (9858700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45b824132b2fa20f03946d41fd176986b8f6fc641a6c219cdc11bb96d53c314`  
		Last Modified: Fri, 02 Sep 2022 05:28:08 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b0f97022345029338ba5562e2edb065e056d763c1a5f71fbf519023a4c4e46`  
		Last Modified: Fri, 02 Sep 2022 05:28:08 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078059344154ba3f0b5af7970364661a7809330e480a88c0e524f2f4631c8399`  
		Last Modified: Fri, 02 Sep 2022 05:28:08 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:apache-buster` - linux; arm64 variant v8

```console
$ docker pull php@sha256:d9f1e00272d5d6509e5edf8fda536bf677ef49aca55093220767a4a3f0d83e95
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137634136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4196188bd80e9bea9bd0becaa81e74347d499ddd0b7f90f7d80a352a62ca2f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 13 Sep 2022 02:11:20 GMT
ADD file:18fa3591fcbf0c3e065dbe581a069fc2af6fab9e4446047348404881af960725 in / 
# Tue, 13 Sep 2022 02:11:21 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 10:10:32 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Sep 2022 10:10:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Sep 2022 10:10:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 10:10:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Sep 2022 10:10:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 13 Sep 2022 10:15:01 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 13 Sep 2022 10:15:02 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 13 Sep 2022 10:15:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 13 Sep 2022 10:15:12 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 13 Sep 2022 10:15:12 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 13 Sep 2022 10:15:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Sep 2022 10:15:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Sep 2022 10:15:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Sep 2022 10:48:48 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 13 Sep 2022 10:48:48 GMT
ENV PHP_VERSION=8.1.10
# Tue, 13 Sep 2022 10:48:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.10.tar.xz.asc
# Tue, 13 Sep 2022 10:48:50 GMT
ENV PHP_SHA256=90e7120c77ee83630e6ac928d23bc6396603d62d83a3cf5df8a450d2e3070162
# Tue, 13 Sep 2022 10:49:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 13 Sep 2022 10:49:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 13 Sep 2022 10:52:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 13 Sep 2022 10:52:51 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 13 Sep 2022 10:52:52 GMT
RUN docker-php-ext-enable sodium
# Tue, 13 Sep 2022 10:52:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Sep 2022 10:52:53 GMT
STOPSIGNAL SIGWINCH
# Tue, 13 Sep 2022 10:52:55 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 13 Sep 2022 10:52:55 GMT
WORKDIR /var/www/html
# Tue, 13 Sep 2022 10:52:56 GMT
EXPOSE 80
# Tue, 13 Sep 2022 10:52:57 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4c3f5cce277263c7aeaf67f83255af76927e03363e775f39d7587bc5036fcf1e`  
		Last Modified: Tue, 13 Sep 2022 02:17:10 GMT  
		Size: 25.9 MB (25904152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a3e3f16c7b72516786d9ed34f6c54c6b959187b9ad062218b339676e27eb24`  
		Last Modified: Tue, 13 Sep 2022 11:55:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab9674f41c9cd28c7fb81387cc2902f2c66d7b8c53485ca6bfc9a2e3fab4418`  
		Last Modified: Tue, 13 Sep 2022 11:55:44 GMT  
		Size: 70.4 MB (70364019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c94d46110aa3fd62e36f82b04849cf45178905cef6a3cc34ea68e0e9ef855e`  
		Last Modified: Tue, 13 Sep 2022 11:55:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808573a81f76cc159a4927975fed0e681af22ced32c8cbd28848af4414ffe62e`  
		Last Modified: Tue, 13 Sep 2022 11:56:06 GMT  
		Size: 18.4 MB (18368186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69493ef922cdfc7ac8b0cff39401def607a88737166358d61d700a1e85b0e435`  
		Last Modified: Tue, 13 Sep 2022 11:56:04 GMT  
		Size: 434.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1802b5449d51aef9ebdb8da2e061588df1dca6a20006f01902213b5d748f38be`  
		Last Modified: Tue, 13 Sep 2022 11:56:04 GMT  
		Size: 487.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f9eddf2c45cac25df96618639dd798c69bcc69341773affbf2c7d64f678191`  
		Last Modified: Tue, 13 Sep 2022 12:00:34 GMT  
		Size: 11.9 MB (11860556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b183d8c9ea7ecc0dc3bee1ae41c522736237e2507790ff2ba1e1773b0633105`  
		Last Modified: Tue, 13 Sep 2022 12:00:31 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141161efb7d3d94994f00af8c16d1498a5a795b9de6268ed46a29053222450f0`  
		Last Modified: Tue, 13 Sep 2022 12:00:33 GMT  
		Size: 11.1 MB (11131757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b5162060a2078800db354a299ff48d14a882932f05a06bc8b2874102a9a71f`  
		Last Modified: Tue, 13 Sep 2022 12:00:31 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e1ba3edc6466b9bac4e88f3252bca203104067b26377e93ae7c6f024a08dd79`  
		Last Modified: Tue, 13 Sep 2022 12:00:31 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66a69df81eba9a79dffa2ece9803efa9d1048d822362753b459dff3aa61459f`  
		Last Modified: Tue, 13 Sep 2022 12:00:31 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:apache-buster` - linux; 386

```console
$ docker pull php@sha256:41d721d724d0ccdc4665a13ec18c6316026ff33713f49a6541e839d03fd05bc4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151066850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e4f7a1de9804fbdc6716858a11cd045d8e76857ef6caabfe651af9fbf0defa`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 13 Sep 2022 01:40:12 GMT
ADD file:da95249e10828562612e8b0a3595f3cbf6a5cb5dbfb47302a4d42a4a8c5025b1 in / 
# Tue, 13 Sep 2022 01:40:12 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 10:14:19 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Sep 2022 10:14:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Sep 2022 10:14:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 10:14:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Sep 2022 10:14:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 13 Sep 2022 10:18:01 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 13 Sep 2022 10:18:02 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 13 Sep 2022 10:18:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 13 Sep 2022 10:18:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 13 Sep 2022 10:18:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 13 Sep 2022 10:18:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Sep 2022 10:18:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Sep 2022 10:18:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Sep 2022 10:44:00 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 13 Sep 2022 10:44:01 GMT
ENV PHP_VERSION=8.1.10
# Tue, 13 Sep 2022 10:44:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.10.tar.xz.asc
# Tue, 13 Sep 2022 10:44:03 GMT
ENV PHP_SHA256=90e7120c77ee83630e6ac928d23bc6396603d62d83a3cf5df8a450d2e3070162
# Tue, 13 Sep 2022 10:44:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 13 Sep 2022 10:44:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 13 Sep 2022 10:46:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 13 Sep 2022 10:46:56 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 13 Sep 2022 10:46:56 GMT
RUN docker-php-ext-enable sodium
# Tue, 13 Sep 2022 10:46:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Sep 2022 10:46:58 GMT
STOPSIGNAL SIGWINCH
# Tue, 13 Sep 2022 10:47:00 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 13 Sep 2022 10:47:00 GMT
WORKDIR /var/www/html
# Tue, 13 Sep 2022 10:47:01 GMT
EXPOSE 80
# Tue, 13 Sep 2022 10:47:02 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:7db2238a0cb6ea85529a33cb395b0243796e76066f31656ba5e08232e2fb0308`  
		Last Modified: Tue, 13 Sep 2022 01:46:12 GMT  
		Size: 27.8 MB (27790952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89aa28f3b0cfc2b18632396c601e31c972521c3da150645c671785f61027c7f2`  
		Last Modified: Tue, 13 Sep 2022 11:48:33 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d6f572e9de6ce72a82e19c1a0a5ec37f5aa186aa9e1ace1ce64ceed8c6b6fc`  
		Last Modified: Tue, 13 Sep 2022 11:48:45 GMT  
		Size: 81.2 MB (81230662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33bca40673ce7d27021c9aa671b93b6d9165d7dc62d3c4f9f63eecf80df74695`  
		Last Modified: Tue, 13 Sep 2022 11:48:33 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1df97c12904348db450e01663d53bee03a96fed1d08a514c7008e053b14b5e`  
		Last Modified: Tue, 13 Sep 2022 11:49:09 GMT  
		Size: 18.9 MB (18900768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2804ef62b885608153750d7cb3a3ddb7f05b056ae73e52e7c0c7f9b2274130cc`  
		Last Modified: Tue, 13 Sep 2022 11:49:06 GMT  
		Size: 433.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa0e3978e8efaf69853f8df2738f28657ff7f332a25744be535735dfd7fe270`  
		Last Modified: Tue, 13 Sep 2022 11:49:06 GMT  
		Size: 486.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b8da410606e967f3c9259305d0611e037bbc16b2d357f9d6bd0d8b19a6d9b9`  
		Last Modified: Tue, 13 Sep 2022 11:53:42 GMT  
		Size: 11.9 MB (11861150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2e12fa4e3dcc33cf8363e10a7d6e3ece6cd53a9a0f8b63a67d7b903cce6145`  
		Last Modified: Tue, 13 Sep 2022 11:53:39 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e452f949d73872e971a9b5fafad7f9e767e3675058b915c171d71eed0a96dc`  
		Last Modified: Tue, 13 Sep 2022 11:53:41 GMT  
		Size: 11.3 MB (11277867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958ec4b13a2f10232adf8cde5f769ec2850545625d887c73fe3c36fb7fc5b265`  
		Last Modified: Tue, 13 Sep 2022 11:53:39 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdba7367353205b8d4a77ccb6cb85fc5fe27ab1e710667684f726ca0829c8d6`  
		Last Modified: Tue, 13 Sep 2022 11:53:39 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8071a749298057221bdff733b2680c6c83338263fe20aba2f510eab65614b1f9`  
		Last Modified: Tue, 13 Sep 2022 11:53:39 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
