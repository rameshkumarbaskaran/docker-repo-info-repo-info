## `yourls:apache`

```console
$ docker pull yourls@sha256:3e3fe88f1de38a8a160e3b5e1d17838fbb1ccf36f919c2af00e2077a3648c601
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

### `yourls:apache` - linux; amd64

```console
$ docker pull yourls@sha256:83ebbbb6d8f69fb40dd90945c95c341a7e180a82473cbbb6696fe7ffa71c372e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.9 MB (169851634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5525b2c1bde7aa74adace6d08dd5864e8e775283039bb8e63f92e6282498e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 04:12:59 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 15 Nov 2022 04:12:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 15 Nov 2022 04:13:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 04:13:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 15 Nov 2022 04:13:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 15 Nov 2022 04:16:52 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 15 Nov 2022 04:16:52 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 15 Nov 2022 04:17:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 15 Nov 2022 04:17:02 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 15 Nov 2022 04:17:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 15 Nov 2022 04:17:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 15 Nov 2022 04:17:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 15 Nov 2022 04:17:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 15 Nov 2022 04:44:12 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 15 Nov 2022 04:44:12 GMT
ENV PHP_VERSION=8.1.12
# Tue, 15 Nov 2022 04:44:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.12.tar.xz.asc
# Tue, 15 Nov 2022 04:44:13 GMT
ENV PHP_SHA256=08243359e2204d842082269eedc15f08d2eca726d0e65b93fb11f4bfc51bbbab
# Tue, 15 Nov 2022 04:44:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 15 Nov 2022 04:44:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 15 Nov 2022 04:47:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 15 Nov 2022 04:47:26 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 15 Nov 2022 04:47:27 GMT
RUN docker-php-ext-enable sodium
# Tue, 15 Nov 2022 04:47:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 15 Nov 2022 04:47:27 GMT
STOPSIGNAL SIGWINCH
# Tue, 15 Nov 2022 04:47:27 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 15 Nov 2022 04:47:27 GMT
WORKDIR /var/www/html
# Tue, 15 Nov 2022 04:47:27 GMT
EXPOSE 80
# Tue, 15 Nov 2022 04:47:27 GMT
CMD ["apache2-foreground"]
# Tue, 15 Nov 2022 08:03:23 GMT
LABEL org.opencontainers.image.title=YOURLS
# Tue, 15 Nov 2022 08:03:23 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Tue, 15 Nov 2022 08:03:23 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Tue, 15 Nov 2022 08:03:23 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Tue, 15 Nov 2022 08:03:23 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Tue, 15 Nov 2022 08:03:23 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Tue, 15 Nov 2022 08:03:23 GMT
LABEL org.opencontainers.image.licenses=MIT
# Tue, 15 Nov 2022 08:03:23 GMT
LABEL io.artifacthub.package.readme-url=https://raw.githubusercontent.com/YOURLS/YOURLS/master/README.md
# Tue, 15 Nov 2022 08:04:04 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Tue, 15 Nov 2022 08:04:05 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 15 Nov 2022 08:04:05 GMT
RUN a2enmod rewrite expires
# Tue, 15 Nov 2022 08:04:06 GMT
ARG YOURLS_VERSION=1.9.1
# Tue, 15 Nov 2022 08:04:06 GMT
ARG YOURLS_SHA256=0bf53290e8f86ea2e0121aac70f7c64d70d3dfb54823acb9dcc343dd7c5f455a
# Tue, 15 Nov 2022 08:04:06 GMT
LABEL org.opencontainers.image.version=1.9.1
# Tue, 15 Nov 2022 08:04:06 GMT
ENV YOURLS_VERSION=1.9.1
# Tue, 15 Nov 2022 08:04:06 GMT
ENV YOURLS_SHA256=0bf53290e8f86ea2e0121aac70f7c64d70d3dfb54823acb9dcc343dd7c5f455a
# Tue, 15 Nov 2022 08:04:08 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Tue, 15 Nov 2022 08:04:08 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Tue, 15 Nov 2022 08:04:08 GMT
COPY file:975ababf859e7cabd8184ab0b2b317a5d8d3ccb6f4922be7f2a5d28c20d075a2 in /usr/local/bin/ 
# Tue, 15 Nov 2022 08:04:08 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Tue, 15 Nov 2022 08:04:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 08:04:09 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c428f1a494230852524a2a5957cc5199c36c8b403305e0e877d580bd0ec9e763`  
		Last Modified: Tue, 15 Nov 2022 06:23:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:156740b07ef8a632f9f7bea4e57e4ee5541ade376adf9169351a1265382e39de`  
		Last Modified: Tue, 15 Nov 2022 06:23:30 GMT  
		Size: 91.6 MB (91634870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5a4c8af82f00730b7427e47bda7f76cea2e2b9aea421750bc9025aface98d8`  
		Last Modified: Tue, 15 Nov 2022 06:23:16 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f85b498fd5bfc6cce951513219fe480850daba71e6e997741e984d18483971`  
		Last Modified: Tue, 15 Nov 2022 06:23:58 GMT  
		Size: 19.2 MB (19245291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b233e420ac7bbca645bb82c213029762acf1742400c076360dc303213c309d5`  
		Last Modified: Tue, 15 Nov 2022 06:23:55 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe42347c4ecfc90333acd9cad13912387eea39d13827a25cfa78727fa5d200e9`  
		Last Modified: Tue, 15 Nov 2022 06:23:56 GMT  
		Size: 514.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6d1815e1923f68b568648087cebf98f3d504a88e4ef98502db7612d2b82b02`  
		Last Modified: Tue, 15 Nov 2022 06:27:01 GMT  
		Size: 12.1 MB (12088098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75b3fa4d0aa553e437549394a9b5e6d2ea9ab2db400a43e5086a279ce05d82d`  
		Last Modified: Tue, 15 Nov 2022 06:26:58 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7dfcc62e5349d3c3fc3ab7a525f8a8986ad5cf2b81d81169b1313b6746719b9`  
		Last Modified: Tue, 15 Nov 2022 06:27:00 GMT  
		Size: 11.0 MB (11042674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c066aae5daa531f64c2736abf59b5d627e0a7a04e34b8c9dd4b55fe2a01741`  
		Last Modified: Tue, 15 Nov 2022 06:26:58 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e78f1cb630fcc58d66cc3b21046a7409cb6361dd698b5a66fed5d7cb9c5ba47`  
		Last Modified: Tue, 15 Nov 2022 06:26:58 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ca68bf26ea241b62c309b7a8840ea6102cf8636ecf10ebb5b03aa07c998ff8`  
		Last Modified: Tue, 15 Nov 2022 06:26:58 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca694daf8138b68dbc40ca5c6ecff605936fcf78d9016d1a338993a74095867`  
		Last Modified: Tue, 15 Nov 2022 08:05:21 GMT  
		Size: 514.4 KB (514371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b749422a64557334df73e1c0dc88b8bdeb9e70b377145654245cc739d35be33c`  
		Last Modified: Tue, 15 Nov 2022 08:05:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0cad90db526851c91d71a586f8211bd1173405412ae6d647eb4c65e189f309`  
		Last Modified: Tue, 15 Nov 2022 08:05:19 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae093ea115d38b3e3fb0d2d924f0358475aa669c35fb01e4cb09c538608b7bb`  
		Last Modified: Tue, 15 Nov 2022 08:05:20 GMT  
		Size: 3.9 MB (3903528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cac76614764cd792915f69f80bacbbe5811bcb11ca43fc9ffbd1dc23aff43e2`  
		Last Modified: Tue, 15 Nov 2022 08:05:19 GMT  
		Size: 2.0 KB (2050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d50299e3a3ceb2e732b0fe6363ebb24ae02edf6495ed8a36602e102a290b946`  
		Last Modified: Tue, 15 Nov 2022 08:05:19 GMT  
		Size: 1.6 KB (1554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e0b6afbf9b4719712060269ab1938180c1e8d8b54ba541543326e447cacc5d`  
		Last Modified: Tue, 15 Nov 2022 08:05:19 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:apache` - linux; arm variant v5

```console
$ docker pull yourls@sha256:e239b342793c9ecb44be51fb1a49f8ed9acdb298e18851aac08be067e1f9a3ae
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147372762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f111aab1e48e5dee1e434b02baf6e3eb697aac90cafc1412fb85b0a95dcdf73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 15 Nov 2022 01:49:18 GMT
ADD file:1949af7e583a1b54055a421129c32315fc101e53e2cda05da3171ed461bde0a6 in / 
# Tue, 15 Nov 2022 01:49:19 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:57:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 15 Nov 2022 01:57:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 15 Nov 2022 01:58:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 01:58:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 15 Nov 2022 01:58:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 15 Nov 2022 02:01:52 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 15 Nov 2022 02:01:52 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 15 Nov 2022 02:02:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 15 Nov 2022 02:02:06 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 15 Nov 2022 02:02:07 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 15 Nov 2022 02:02:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 15 Nov 2022 02:02:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 15 Nov 2022 02:02:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 15 Nov 2022 02:17:59 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 15 Nov 2022 02:17:59 GMT
ENV PHP_VERSION=8.1.12
# Tue, 15 Nov 2022 02:17:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.12.tar.xz.asc
# Tue, 15 Nov 2022 02:17:59 GMT
ENV PHP_SHA256=08243359e2204d842082269eedc15f08d2eca726d0e65b93fb11f4bfc51bbbab
# Tue, 15 Nov 2022 02:18:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 15 Nov 2022 02:18:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 15 Nov 2022 02:23:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 15 Nov 2022 02:23:11 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 15 Nov 2022 02:23:12 GMT
RUN docker-php-ext-enable sodium
# Tue, 15 Nov 2022 02:23:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 15 Nov 2022 02:23:13 GMT
STOPSIGNAL SIGWINCH
# Tue, 15 Nov 2022 02:23:13 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 15 Nov 2022 02:23:13 GMT
WORKDIR /var/www/html
# Tue, 15 Nov 2022 02:23:13 GMT
EXPOSE 80
# Tue, 15 Nov 2022 02:23:13 GMT
CMD ["apache2-foreground"]
# Tue, 15 Nov 2022 13:01:31 GMT
LABEL org.opencontainers.image.title=YOURLS
# Tue, 15 Nov 2022 13:01:31 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Tue, 15 Nov 2022 13:01:31 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Tue, 15 Nov 2022 13:01:32 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Tue, 15 Nov 2022 13:01:32 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Tue, 15 Nov 2022 13:01:32 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Tue, 15 Nov 2022 13:01:32 GMT
LABEL org.opencontainers.image.licenses=MIT
# Tue, 15 Nov 2022 13:01:32 GMT
LABEL io.artifacthub.package.readme-url=https://raw.githubusercontent.com/YOURLS/YOURLS/master/README.md
# Tue, 15 Nov 2022 13:01:56 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Tue, 15 Nov 2022 13:01:57 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 15 Nov 2022 13:01:58 GMT
RUN a2enmod rewrite expires
# Tue, 15 Nov 2022 13:01:58 GMT
ARG YOURLS_VERSION=1.9.1
# Tue, 15 Nov 2022 13:01:58 GMT
ARG YOURLS_SHA256=0bf53290e8f86ea2e0121aac70f7c64d70d3dfb54823acb9dcc343dd7c5f455a
# Tue, 15 Nov 2022 13:01:58 GMT
LABEL org.opencontainers.image.version=1.9.1
# Tue, 15 Nov 2022 13:01:58 GMT
ENV YOURLS_VERSION=1.9.1
# Tue, 15 Nov 2022 13:01:58 GMT
ENV YOURLS_SHA256=0bf53290e8f86ea2e0121aac70f7c64d70d3dfb54823acb9dcc343dd7c5f455a
# Tue, 15 Nov 2022 13:02:01 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Tue, 15 Nov 2022 13:02:01 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Tue, 15 Nov 2022 13:02:01 GMT
COPY file:975ababf859e7cabd8184ab0b2b317a5d8d3ccb6f4922be7f2a5d28c20d075a2 in /usr/local/bin/ 
# Tue, 15 Nov 2022 13:02:01 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Tue, 15 Nov 2022 13:02:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 13:02:01 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b56836d864a6d857be3d12242b65962f2a2cf0d77c48cfb85bbbdf9d56a7e93d`  
		Last Modified: Tue, 15 Nov 2022 01:54:26 GMT  
		Size: 28.9 MB (28914126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf8f13a67ff628e982fa37f19e46a30b6c95f885b9caf0fe288d9e44fc0fe23`  
		Last Modified: Tue, 15 Nov 2022 03:18:33 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0b67f60155678149aec805bafe02c6067447f321279766240c3ae4d1bf9745`  
		Last Modified: Tue, 15 Nov 2022 03:18:47 GMT  
		Size: 73.7 MB (73687967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee4232fc94727d61967ec10566bb2eb1be8604bec5ccee5d4cbf30b97fac1a7`  
		Last Modified: Tue, 15 Nov 2022 03:18:33 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34b8b60e851c4b269f4b5712234fdb5bf26b82175012efee89f2a93b46332cc`  
		Last Modified: Tue, 15 Nov 2022 03:19:23 GMT  
		Size: 18.6 MB (18554768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6920c0af9b512e8602f43052e8093089a43c2340e4061dacfa39bcd3b17efce4`  
		Last Modified: Tue, 15 Nov 2022 03:19:20 GMT  
		Size: 433.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0590765527cfdc9d56faac74f8393f036bf4d551848b5657bcdd822c34fd4be`  
		Last Modified: Tue, 15 Nov 2022 03:19:20 GMT  
		Size: 486.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08420d31b1086298c4d44cf37912c065402dd9a6e96a3d74d4a87c8e2410939c`  
		Last Modified: Tue, 15 Nov 2022 03:21:29 GMT  
		Size: 12.1 MB (12086567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f2c73a7cdcb7ae183751ecca31ef5b262503aecffcfd3c34e73ebe075f07e5`  
		Last Modified: Tue, 15 Nov 2022 03:21:26 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b857d19106fd05c2a95c605510f8ee57800681850d22743fba6e429e9088be0a`  
		Last Modified: Tue, 15 Nov 2022 03:21:29 GMT  
		Size: 10.1 MB (10064988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85aeffc318b04361d7f0ba6aca158f480baccb4a7da0a6890634a1f9b99e6784`  
		Last Modified: Tue, 15 Nov 2022 03:21:26 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a58ccaef78b35c844d215ab15edf5b536f868bfe4e676f1e0df0c46af76407f`  
		Last Modified: Tue, 15 Nov 2022 03:21:26 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb23fa0a773a95be940a3313772c723c194d36726390c48ce03eab67fcaac04`  
		Last Modified: Tue, 15 Nov 2022 03:21:26 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220dbf2204022f283613e42b14804cc62b80a4568e73465a07459663b6301c73`  
		Last Modified: Tue, 15 Nov 2022 13:03:25 GMT  
		Size: 150.7 KB (150742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39c676589213c20892ff26314badd0466fd63b17f82a2b1defd98348b2ef305`  
		Last Modified: Tue, 15 Nov 2022 13:03:24 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1480a13cc889c46e1a3bd6b934d98a527dd9d8f7b317e9702394574671137a`  
		Last Modified: Tue, 15 Nov 2022 13:03:23 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e1aa4cfaa849a0c490b819e662f8077271b6e90fe2135da6225cbf7cb9647a`  
		Last Modified: Tue, 15 Nov 2022 13:03:24 GMT  
		Size: 3.9 MB (3903535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5001a6b6227a7d6996986396af638163b176a819b90dc21e63b2172ca7d75182`  
		Last Modified: Tue, 15 Nov 2022 13:03:22 GMT  
		Size: 2.1 KB (2051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c8393d4f5f1387b340ef2be84aa2b937d952c481b449a8189b143f3a10bac74`  
		Last Modified: Tue, 15 Nov 2022 13:03:23 GMT  
		Size: 1.6 KB (1556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447eae83060d1a433cd9bb4ed9e1c526dbfa2352f3e1b2822f754cabf3b17fb5`  
		Last Modified: Tue, 15 Nov 2022 13:03:23 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:apache` - linux; arm variant v7

```console
$ docker pull yourls@sha256:143fb752ea54354e595933af1419e7f5f804b7fd73c16908ff0662738a021a1c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139568873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc576023a551b6c69e2098aa1553a7cc25f033248baf12a15e95da77c11be321`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 15 Nov 2022 03:43:25 GMT
ADD file:1b5c939bd2a35667d7fc44c3009a56ed92a932f512a73df1617dec6ccbd6e6b1 in / 
# Tue, 15 Nov 2022 03:43:26 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 03:55:46 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 15 Nov 2022 03:55:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 15 Nov 2022 03:56:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 03:56:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 15 Nov 2022 03:56:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 15 Nov 2022 03:58:58 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 15 Nov 2022 03:58:58 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 15 Nov 2022 03:59:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 15 Nov 2022 03:59:10 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 15 Nov 2022 03:59:10 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 15 Nov 2022 03:59:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 15 Nov 2022 03:59:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 15 Nov 2022 03:59:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 15 Nov 2022 04:23:37 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 15 Nov 2022 04:23:37 GMT
ENV PHP_VERSION=8.1.12
# Tue, 15 Nov 2022 04:23:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.12.tar.xz.asc
# Tue, 15 Nov 2022 04:23:37 GMT
ENV PHP_SHA256=08243359e2204d842082269eedc15f08d2eca726d0e65b93fb11f4bfc51bbbab
# Tue, 15 Nov 2022 04:23:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 15 Nov 2022 04:23:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 15 Nov 2022 04:26:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 15 Nov 2022 04:26:19 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 15 Nov 2022 04:26:19 GMT
RUN docker-php-ext-enable sodium
# Tue, 15 Nov 2022 04:26:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 15 Nov 2022 04:26:20 GMT
STOPSIGNAL SIGWINCH
# Tue, 15 Nov 2022 04:26:20 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 15 Nov 2022 04:26:20 GMT
WORKDIR /var/www/html
# Tue, 15 Nov 2022 04:26:20 GMT
EXPOSE 80
# Tue, 15 Nov 2022 04:26:20 GMT
CMD ["apache2-foreground"]
# Tue, 15 Nov 2022 10:25:31 GMT
LABEL org.opencontainers.image.title=YOURLS
# Tue, 15 Nov 2022 10:25:31 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Tue, 15 Nov 2022 10:25:31 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Tue, 15 Nov 2022 10:25:31 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Tue, 15 Nov 2022 10:25:31 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Tue, 15 Nov 2022 10:25:31 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Tue, 15 Nov 2022 10:25:32 GMT
LABEL org.opencontainers.image.licenses=MIT
# Tue, 15 Nov 2022 10:25:32 GMT
LABEL io.artifacthub.package.readme-url=https://raw.githubusercontent.com/YOURLS/YOURLS/master/README.md
# Tue, 15 Nov 2022 10:25:57 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Tue, 15 Nov 2022 10:25:57 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 15 Nov 2022 10:25:58 GMT
RUN a2enmod rewrite expires
# Tue, 15 Nov 2022 10:25:58 GMT
ARG YOURLS_VERSION=1.9.1
# Tue, 15 Nov 2022 10:25:58 GMT
ARG YOURLS_SHA256=0bf53290e8f86ea2e0121aac70f7c64d70d3dfb54823acb9dcc343dd7c5f455a
# Tue, 15 Nov 2022 10:25:58 GMT
LABEL org.opencontainers.image.version=1.9.1
# Tue, 15 Nov 2022 10:25:58 GMT
ENV YOURLS_VERSION=1.9.1
# Tue, 15 Nov 2022 10:25:58 GMT
ENV YOURLS_SHA256=0bf53290e8f86ea2e0121aac70f7c64d70d3dfb54823acb9dcc343dd7c5f455a
# Tue, 15 Nov 2022 10:26:01 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Tue, 15 Nov 2022 10:26:01 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Tue, 15 Nov 2022 10:26:01 GMT
COPY file:975ababf859e7cabd8184ab0b2b317a5d8d3ccb6f4922be7f2a5d28c20d075a2 in /usr/local/bin/ 
# Tue, 15 Nov 2022 10:26:01 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Tue, 15 Nov 2022 10:26:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 10:26:01 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:fd18d0201d0ce0c5e103902d894f5d601fc5dde76688aa7dae786840141d23e4`  
		Last Modified: Tue, 15 Nov 2022 03:50:11 GMT  
		Size: 26.6 MB (26576195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9882e3666a8ea23dcd83cf24efee4c2bc629f92dcf64bbfb5c9323497a250bd`  
		Last Modified: Tue, 15 Nov 2022 06:04:52 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc118326146d74f82c6277eb8df1029bf3b7f96486d7830fea19631b696893be`  
		Last Modified: Tue, 15 Nov 2022 06:05:05 GMT  
		Size: 69.3 MB (69320668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823b0bab372d5757e3e8f322d5ca5aefbd8984c35bed9771179b5de70ac8aad0`  
		Last Modified: Tue, 15 Nov 2022 06:04:52 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:821aad38acd8081587ed34af24add9d0aa67c574e056373044edf7b1429ad4d2`  
		Last Modified: Tue, 15 Nov 2022 06:05:41 GMT  
		Size: 18.0 MB (17998468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6391212ad86f9de174ba9712196fdf9d7387c2673b491a78fb937af64feadc`  
		Last Modified: Tue, 15 Nov 2022 06:05:38 GMT  
		Size: 434.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b1d20f19b4c6453c4bc0e3ba102bb3a3daa81fa53828e516ce1838fae1d4e9`  
		Last Modified: Tue, 15 Nov 2022 06:05:38 GMT  
		Size: 487.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627003b163d98ef02cce4cf2e67df3ccce3f731dca02007044ba6656fca476f3`  
		Last Modified: Tue, 15 Nov 2022 06:09:35 GMT  
		Size: 12.1 MB (12086534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf3dfbf36f467a435b2c984349e974cfa38c8327b24b8e445299c442a392402`  
		Last Modified: Tue, 15 Nov 2022 06:09:32 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1de9e7441fc4e3054169143b811afc362e1a24181d00b1d2ecd4e1687f64b9f`  
		Last Modified: Tue, 15 Nov 2022 06:09:34 GMT  
		Size: 9.5 MB (9534985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a44930aa1e2efad752c181d0071abb7c5cf6f0c0f5832b924db145cfc73c729`  
		Last Modified: Tue, 15 Nov 2022 06:09:32 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64aed35b976366053147c57987b6a3cbf58a28f3235bc6fa4682801344a899fa`  
		Last Modified: Tue, 15 Nov 2022 06:09:32 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734d9c7aaab2ec1258d809ca4df60e978055413263d8fde5a78739b4e9f9bf65`  
		Last Modified: Tue, 15 Nov 2022 06:09:32 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168b08bf02fabeb41c00d4a6075337c98eefea04cf797bb61cd47d60e5f56281`  
		Last Modified: Tue, 15 Nov 2022 10:27:34 GMT  
		Size: 138.4 KB (138430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f0fd4248f0dece3f7776ddfac2210942b99418d3dd4b0c86303244e99b81209`  
		Last Modified: Tue, 15 Nov 2022 10:27:33 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8194d588929f8110f19cd059a4bb303d26489604b9cabcb3945225d2f4ab4977`  
		Last Modified: Tue, 15 Nov 2022 10:27:31 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5c8bf95a17002dc1ace2cf32e051b5a00aa277a2a58f239ea8c863a30bc596`  
		Last Modified: Tue, 15 Nov 2022 10:27:32 GMT  
		Size: 3.9 MB (3903534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab09e2e2c91cbedcac5f4257602d13f662dcce9094b9b55b9cdd3fa00f0c9d9`  
		Last Modified: Tue, 15 Nov 2022 10:27:31 GMT  
		Size: 2.0 KB (2048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d6b4129d6f7bfed4b5eb92e3d5b369779c91ca8230886732c1a15c05a70beb`  
		Last Modified: Tue, 15 Nov 2022 10:27:31 GMT  
		Size: 1.6 KB (1551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b385e705f539e67c594d4ce14fadab5a367757271410ba37b8536882148b45e`  
		Last Modified: Tue, 15 Nov 2022 10:27:31 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:apache` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:89d7178a2eb1b4ca902a06272b912d861c81f770746f1d72fd372bd2fe1c445e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.1 MB (164066604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:115340ea35b5b95431b5c39e81c481bcd2241332a28aa1f52850c493d4da91c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 16:00:07 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 25 Oct 2022 16:00:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 25 Oct 2022 16:00:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 16:00:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 25 Oct 2022 16:00:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 25 Oct 2022 16:03:30 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 25 Oct 2022 16:03:30 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 25 Oct 2022 16:03:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 25 Oct 2022 16:03:38 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 25 Oct 2022 16:03:38 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 25 Oct 2022 16:03:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Oct 2022 16:03:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Oct 2022 16:03:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 25 Oct 2022 16:52:19 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 28 Oct 2022 18:44:01 GMT
ENV PHP_VERSION=8.1.12
# Fri, 28 Oct 2022 18:44:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.12.tar.xz.asc
# Fri, 28 Oct 2022 18:44:01 GMT
ENV PHP_SHA256=08243359e2204d842082269eedc15f08d2eca726d0e65b93fb11f4bfc51bbbab
# Fri, 28 Oct 2022 18:44:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 28 Oct 2022 18:44:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 28 Oct 2022 18:47:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 28 Oct 2022 18:47:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 28 Oct 2022 18:47:03 GMT
RUN docker-php-ext-enable sodium
# Fri, 28 Oct 2022 18:47:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 28 Oct 2022 18:47:04 GMT
STOPSIGNAL SIGWINCH
# Fri, 28 Oct 2022 18:47:04 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 28 Oct 2022 18:47:04 GMT
WORKDIR /var/www/html
# Fri, 28 Oct 2022 18:47:04 GMT
EXPOSE 80
# Fri, 28 Oct 2022 18:47:04 GMT
CMD ["apache2-foreground"]
# Sat, 29 Oct 2022 14:25:49 GMT
LABEL org.opencontainers.image.title=YOURLS
# Sat, 29 Oct 2022 14:25:49 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Sat, 29 Oct 2022 14:25:49 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Sat, 29 Oct 2022 14:25:49 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Sat, 29 Oct 2022 14:25:49 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Sat, 29 Oct 2022 14:25:49 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Sat, 29 Oct 2022 14:25:49 GMT
LABEL org.opencontainers.image.licenses=MIT
# Sat, 29 Oct 2022 14:25:49 GMT
LABEL io.artifacthub.package.readme-url=https://raw.githubusercontent.com/YOURLS/YOURLS/master/README.md
# Sat, 29 Oct 2022 14:26:46 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Sat, 29 Oct 2022 14:26:46 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 29 Oct 2022 14:26:47 GMT
RUN a2enmod rewrite expires
# Sat, 29 Oct 2022 14:26:47 GMT
ARG YOURLS_VERSION=1.9.1
# Sat, 29 Oct 2022 14:26:47 GMT
ARG YOURLS_SHA256=0bf53290e8f86ea2e0121aac70f7c64d70d3dfb54823acb9dcc343dd7c5f455a
# Sat, 29 Oct 2022 14:26:47 GMT
LABEL org.opencontainers.image.version=1.9.1
# Sat, 29 Oct 2022 14:26:47 GMT
ENV YOURLS_VERSION=1.9.1
# Sat, 29 Oct 2022 14:26:47 GMT
ENV YOURLS_SHA256=0bf53290e8f86ea2e0121aac70f7c64d70d3dfb54823acb9dcc343dd7c5f455a
# Sat, 29 Oct 2022 14:26:49 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Sat, 29 Oct 2022 14:26:49 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Sat, 29 Oct 2022 14:26:49 GMT
COPY file:975ababf859e7cabd8184ab0b2b317a5d8d3ccb6f4922be7f2a5d28c20d075a2 in /usr/local/bin/ 
# Sat, 29 Oct 2022 14:26:49 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Sat, 29 Oct 2022 14:26:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Oct 2022 14:26:49 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0561680dabe2de60226eae9b638b31d60cc7380348ed91f16fb2323135a44ab4`  
		Last Modified: Tue, 25 Oct 2022 19:38:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351526f9a72c42ff7e19d5c66c23824d15a33b23d4f0614a04aaa485df9e2131`  
		Last Modified: Tue, 25 Oct 2022 19:38:52 GMT  
		Size: 86.9 MB (86928284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b21a5da3a7b221650e7528802ac2b8cdb5c28537f5bd131de3a6dc02694405`  
		Last Modified: Tue, 25 Oct 2022 19:38:41 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87711ceb3120efe71b86a11c3dbb1f0d3747cad16ed2534ba0f86ce8d6e953ed`  
		Last Modified: Tue, 25 Oct 2022 19:39:23 GMT  
		Size: 19.2 MB (19167499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21369f734b3ab2b4443bd50603048938ed939e1a8c8ffc8c66a62d7492c7396a`  
		Last Modified: Tue, 25 Oct 2022 19:39:20 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a313d43eb653350da1f8410ebdc3e4d093091f93a81b84e071962f34c513b8a`  
		Last Modified: Tue, 25 Oct 2022 19:39:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c49ebc4923bdce5a56e36e3386ab299f21cc1b874e3cb54f8a09e08df2ccc1`  
		Last Modified: Fri, 28 Oct 2022 20:07:46 GMT  
		Size: 12.1 MB (12087367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638e36e31a8a22b345b2a8c19031bb48327b72bbe3609866d7d54714496d62fe`  
		Last Modified: Fri, 28 Oct 2022 20:07:44 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b81be9c8df179a9320dfc2ab3165417cf93fae1ae6e560e94705c9045699484`  
		Last Modified: Fri, 28 Oct 2022 20:07:46 GMT  
		Size: 11.1 MB (11112286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9b4256df936bda8f33b6e2f5909b03baee3bdeaaf1adf4741d0347e7c014ec`  
		Last Modified: Fri, 28 Oct 2022 20:07:44 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953edeb63067bafdee3aac49e20a66f88a836f50b16ad611cdc58e02106d64d7`  
		Last Modified: Fri, 28 Oct 2022 20:07:44 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc940785c3690de26ce04dfc497dbf3ec409745aad5ec122dbc05dd9c99ee5b4`  
		Last Modified: Fri, 28 Oct 2022 20:07:44 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeda33f11e6e75f10e0e20eced1106fad9b7820ae6f2ca6a5257b250cd58938c`  
		Last Modified: Sat, 29 Oct 2022 14:30:05 GMT  
		Size: 793.6 KB (793556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea68238a8a76a2c0df03270637c26db668b686455e4e0a3c02170550066b5312`  
		Last Modified: Sat, 29 Oct 2022 14:30:05 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16287095e3ff7badd7debf9abe39741a00f207c58dec44da60cea716d39323f2`  
		Last Modified: Sat, 29 Oct 2022 14:30:02 GMT  
		Size: 346.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d02c095f732fa1695144d9a503d85b68ad60d23b37b6add486229bfd87789a70`  
		Last Modified: Sat, 29 Oct 2022 14:30:03 GMT  
		Size: 3.9 MB (3903529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5fe77111098e642fcf960c42b31a992ccd46b6371741fb6298777b418709943`  
		Last Modified: Sat, 29 Oct 2022 14:30:02 GMT  
		Size: 2.1 KB (2051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470bf555829f27d5fb826352f605251dd8e1a79260c9a05c7eac74a50ded96ca`  
		Last Modified: Sat, 29 Oct 2022 14:30:02 GMT  
		Size: 1.6 KB (1555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02ad73eccd726dbf94bb642628308eb0842178d2ba90f7fb8b01cb619ba9b16`  
		Last Modified: Sat, 29 Oct 2022 14:30:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:apache` - linux; 386

```console
$ docker pull yourls@sha256:59a6230817271bd5b71490a8c4d64c39710be6bdce7462af767aa18b03a4a882
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.0 MB (171972617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e2c449187762ad4e5b216270ee3b6fe57e4c7365765899697d94bcb4c5eb7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 25 Oct 2022 02:22:34 GMT
ADD file:14adaece72e410cf04ac21a101e5b530aab1d5e5a189a2be72d195ec0ac5e6d4 in / 
# Tue, 25 Oct 2022 02:22:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:43:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 25 Oct 2022 07:43:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 25 Oct 2022 07:43:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:43:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 25 Oct 2022 07:43:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 25 Oct 2022 07:46:56 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 25 Oct 2022 07:46:56 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 25 Oct 2022 07:47:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 25 Oct 2022 07:47:06 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 25 Oct 2022 07:47:07 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 25 Oct 2022 07:47:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Oct 2022 07:47:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Oct 2022 07:47:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 25 Oct 2022 08:13:21 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 28 Oct 2022 18:58:02 GMT
ENV PHP_VERSION=8.1.12
# Fri, 28 Oct 2022 18:58:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.12.tar.xz.asc
# Fri, 28 Oct 2022 18:58:04 GMT
ENV PHP_SHA256=08243359e2204d842082269eedc15f08d2eca726d0e65b93fb11f4bfc51bbbab
# Fri, 28 Oct 2022 18:58:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 28 Oct 2022 18:58:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 28 Oct 2022 19:01:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 28 Oct 2022 19:01:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 28 Oct 2022 19:01:03 GMT
RUN docker-php-ext-enable sodium
# Fri, 28 Oct 2022 19:01:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 28 Oct 2022 19:01:05 GMT
STOPSIGNAL SIGWINCH
# Fri, 28 Oct 2022 19:01:07 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 28 Oct 2022 19:01:07 GMT
WORKDIR /var/www/html
# Fri, 28 Oct 2022 19:01:08 GMT
EXPOSE 80
# Fri, 28 Oct 2022 19:01:09 GMT
CMD ["apache2-foreground"]
# Fri, 28 Oct 2022 23:55:53 GMT
LABEL org.opencontainers.image.title=YOURLS
# Fri, 28 Oct 2022 23:55:54 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Fri, 28 Oct 2022 23:55:55 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Fri, 28 Oct 2022 23:55:56 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Fri, 28 Oct 2022 23:55:57 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Fri, 28 Oct 2022 23:55:58 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Fri, 28 Oct 2022 23:55:59 GMT
LABEL org.opencontainers.image.licenses=MIT
# Fri, 28 Oct 2022 23:56:00 GMT
LABEL io.artifacthub.package.readme-url=https://raw.githubusercontent.com/YOURLS/YOURLS/master/README.md
# Fri, 28 Oct 2022 23:56:36 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Fri, 28 Oct 2022 23:56:37 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 28 Oct 2022 23:56:38 GMT
RUN a2enmod rewrite expires
# Fri, 28 Oct 2022 23:56:39 GMT
ARG YOURLS_VERSION=1.9.1
# Fri, 28 Oct 2022 23:56:40 GMT
ARG YOURLS_SHA256=0bf53290e8f86ea2e0121aac70f7c64d70d3dfb54823acb9dcc343dd7c5f455a
# Fri, 28 Oct 2022 23:56:41 GMT
LABEL org.opencontainers.image.version=1.9.1
# Fri, 28 Oct 2022 23:56:42 GMT
ENV YOURLS_VERSION=1.9.1
# Fri, 28 Oct 2022 23:56:43 GMT
ENV YOURLS_SHA256=0bf53290e8f86ea2e0121aac70f7c64d70d3dfb54823acb9dcc343dd7c5f455a
# Fri, 28 Oct 2022 23:56:46 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 28 Oct 2022 23:56:47 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Fri, 28 Oct 2022 23:56:48 GMT
COPY file:975ababf859e7cabd8184ab0b2b317a5d8d3ccb6f4922be7f2a5d28c20d075a2 in /usr/local/bin/ 
# Fri, 28 Oct 2022 23:56:49 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Fri, 28 Oct 2022 23:56:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 23:56:50 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3c83067056c0f1bc4e162249831ac686f3a9a9c64c5366b903581580de8fcac2`  
		Last Modified: Tue, 25 Oct 2022 02:28:26 GMT  
		Size: 32.4 MB (32396384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0948a6cb6a1d2f6c786b617951b1ab3ec89dd42c99ab607b1177341d0240a14`  
		Last Modified: Tue, 25 Oct 2022 09:54:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f955a2c6bc1276cc28b9f9fc151b352557d065804eff5792b1a09bf369b3c7`  
		Last Modified: Tue, 25 Oct 2022 09:55:09 GMT  
		Size: 92.5 MB (92512305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a438033acf7f8657b99ad5fd36439e01c536f52e25597c2500f250496ce6dba`  
		Last Modified: Tue, 25 Oct 2022 09:54:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56625f8160a2ba4c165333c50d823de6db1db0e9380dc5a5f9ba84ea23ad7b5f`  
		Last Modified: Tue, 25 Oct 2022 09:55:45 GMT  
		Size: 19.5 MB (19515785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1df45ea2be624f5d8fad984cb35d281ffb45b4e165d17bccede80e1c66ec03`  
		Last Modified: Tue, 25 Oct 2022 09:55:43 GMT  
		Size: 430.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7626ffb48900bf481e2b39482a8d476beff0d161a701f494c6855b1863c1482`  
		Last Modified: Tue, 25 Oct 2022 09:55:43 GMT  
		Size: 485.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea79bf1dc05d6d079144d1b5d62810726f29d81e463c99b898aa9aa4c23b6f3`  
		Last Modified: Fri, 28 Oct 2022 20:43:21 GMT  
		Size: 11.9 MB (11871883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4b9673012c6d296c8b48d21cfefa1b239bf72c9504ebc31d87ced83f65d635`  
		Last Modified: Fri, 28 Oct 2022 20:43:17 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698be58ae3b367d7e4f3b8871a0cbb4eca5272076270e9af7c3b016de9061a7d`  
		Last Modified: Fri, 28 Oct 2022 20:43:19 GMT  
		Size: 11.3 MB (11267882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ebca1fb9fb524f1c85191df1afaa8fb90805fe6d26e26a8248338a8ccfb874`  
		Last Modified: Fri, 28 Oct 2022 20:43:17 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e5a0d106977f6e9dad04c7ee95b7cbd9d74bd9a5e4e3f4df347bfee10dd5d1`  
		Last Modified: Fri, 28 Oct 2022 20:43:17 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c823f33d19cefe0535f941c1953377c1e57f19428625e77d48f21b6f53689df8`  
		Last Modified: Fri, 28 Oct 2022 20:43:17 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1acbf21efe5af4ce9344bc225eb3db1ef31a064e223ece3ab0cc4f671cb62dbb`  
		Last Modified: Sat, 29 Oct 2022 00:00:05 GMT  
		Size: 494.9 KB (494895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fdb1b0a05e6059e38923ad6fcbb357873ec4de7a2b74b5ec8cf8f8be12f5ee8`  
		Last Modified: Sat, 29 Oct 2022 00:00:02 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7157c13c4da712812f7c4b32c7ba7c8f62cd30286fbf4e3f62e1647d9fca46`  
		Last Modified: Sat, 29 Oct 2022 00:00:00 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a4ae31992a14a6dbf54c207dad00d27cdffa8d7f22886e8a480a3c39aba4340`  
		Last Modified: Sat, 29 Oct 2022 00:00:00 GMT  
		Size: 3.9 MB (3903424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75d3e10b55a29309a5faa098def3d7c15efa473f52b9324edca5af98550bdea`  
		Last Modified: Fri, 28 Oct 2022 23:59:59 GMT  
		Size: 2.0 KB (2050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed3b991073f4373cb388a86548c4d224d83767be55e2d54cd3e4ab3db1e9d22a`  
		Last Modified: Sat, 29 Oct 2022 00:00:00 GMT  
		Size: 1.6 KB (1552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078423ce332108d5c540c6f98c5e542d5bcef0f0dcb8491d0fb0d67f2aa23e27`  
		Last Modified: Sat, 29 Oct 2022 00:00:00 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:apache` - linux; mips64le

```console
$ docker pull yourls@sha256:09a86291f39b05ed66abdd20daa59651a524fa941685f6d93dece8a468c50b83
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146520695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47229c316dd7ff32d052d895dec6f0164e76679878edf2f5fa3809ba16b9d786`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 25 Oct 2022 04:39:25 GMT
ADD file:222c5611b805658925ba615b0e69d40aa3dfa37223bc06f150909f7e944e426b in / 
# Tue, 25 Oct 2022 04:39:29 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 18:56:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 25 Oct 2022 18:56:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 25 Oct 2022 18:58:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 18:58:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 25 Oct 2022 18:58:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 25 Oct 2022 19:17:50 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 25 Oct 2022 19:17:54 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 25 Oct 2022 19:18:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 25 Oct 2022 19:18:59 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 25 Oct 2022 19:19:05 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 25 Oct 2022 19:19:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Oct 2022 19:19:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Oct 2022 19:19:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 25 Oct 2022 20:20:59 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 28 Oct 2022 19:41:03 GMT
ENV PHP_VERSION=8.1.12
# Fri, 28 Oct 2022 19:41:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.12.tar.xz.asc
# Fri, 28 Oct 2022 19:41:09 GMT
ENV PHP_SHA256=08243359e2204d842082269eedc15f08d2eca726d0e65b93fb11f4bfc51bbbab
# Fri, 28 Oct 2022 19:41:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 28 Oct 2022 19:42:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 28 Oct 2022 19:55:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 28 Oct 2022 19:55:30 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 28 Oct 2022 19:55:36 GMT
RUN docker-php-ext-enable sodium
# Fri, 28 Oct 2022 19:55:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 28 Oct 2022 19:55:43 GMT
STOPSIGNAL SIGWINCH
# Fri, 28 Oct 2022 19:55:46 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 28 Oct 2022 19:55:49 GMT
WORKDIR /var/www/html
# Fri, 28 Oct 2022 19:55:52 GMT
EXPOSE 80
# Fri, 28 Oct 2022 19:55:56 GMT
CMD ["apache2-foreground"]
# Sat, 29 Oct 2022 03:19:17 GMT
LABEL org.opencontainers.image.title=YOURLS
# Sat, 29 Oct 2022 03:19:21 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Sat, 29 Oct 2022 03:19:24 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Sat, 29 Oct 2022 03:19:28 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Sat, 29 Oct 2022 03:19:31 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Sat, 29 Oct 2022 03:19:35 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Sat, 29 Oct 2022 03:19:38 GMT
LABEL org.opencontainers.image.licenses=MIT
# Sat, 29 Oct 2022 03:19:42 GMT
LABEL io.artifacthub.package.readme-url=https://raw.githubusercontent.com/YOURLS/YOURLS/master/README.md
# Sat, 29 Oct 2022 03:20:47 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Sat, 29 Oct 2022 03:20:53 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 29 Oct 2022 03:20:59 GMT
RUN a2enmod rewrite expires
# Sat, 29 Oct 2022 03:21:02 GMT
ARG YOURLS_VERSION=1.9.1
# Sat, 29 Oct 2022 03:21:06 GMT
ARG YOURLS_SHA256=0bf53290e8f86ea2e0121aac70f7c64d70d3dfb54823acb9dcc343dd7c5f455a
# Sat, 29 Oct 2022 03:21:09 GMT
LABEL org.opencontainers.image.version=1.9.1
# Sat, 29 Oct 2022 03:21:13 GMT
ENV YOURLS_VERSION=1.9.1
# Sat, 29 Oct 2022 03:21:17 GMT
ENV YOURLS_SHA256=0bf53290e8f86ea2e0121aac70f7c64d70d3dfb54823acb9dcc343dd7c5f455a
# Sat, 29 Oct 2022 03:21:26 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Sat, 29 Oct 2022 03:21:29 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Sat, 29 Oct 2022 03:21:32 GMT
COPY file:975ababf859e7cabd8184ab0b2b317a5d8d3ccb6f4922be7f2a5d28c20d075a2 in /usr/local/bin/ 
# Sat, 29 Oct 2022 03:21:35 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Sat, 29 Oct 2022 03:21:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Oct 2022 03:21:42 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:85f344f7fa0587aa4dbdc8d09d838d444853a1789047586a0927fa09fa89bb8f`  
		Last Modified: Tue, 25 Oct 2022 04:47:25 GMT  
		Size: 29.6 MB (29640590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1753d3f2251836c7265e2d11e160979e9d4c04bb3e7706e4d203a69fd459cb1e`  
		Last Modified: Tue, 25 Oct 2022 23:39:58 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eab562ae938cccba58076572171eae0954f14d6835e383fd194f67606c69bac`  
		Last Modified: Tue, 25 Oct 2022 23:40:51 GMT  
		Size: 71.8 MB (71813985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d1abf6854edcb865c86fcfc17a0c116eb58a079f8603b5dcae5002ad0de8926`  
		Last Modified: Tue, 25 Oct 2022 23:39:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d574602fb5f55baaf8825beb92924214b7751ebfe9cfc8fa9ae47ec4d8dd54f`  
		Last Modified: Tue, 25 Oct 2022 23:41:34 GMT  
		Size: 18.9 MB (18940139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110aa31b0b1515f8087ae7c02237ca54a556ff5983ee846509835dbbfe5ffba9`  
		Last Modified: Tue, 25 Oct 2022 23:41:22 GMT  
		Size: 437.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da809472b424c3484a545d67ac4da7cbd0468147097306db188aeb74a220855`  
		Last Modified: Tue, 25 Oct 2022 23:41:22 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa02eaf3c79ba1f5ab3edea39b6f1285488e6d40e1558b96c51270f6873ea91`  
		Last Modified: Fri, 28 Oct 2022 21:20:59 GMT  
		Size: 11.9 MB (11870697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c0d0b11ccbc5c0ca295c7187af929eb88c0e9821509e4dcdae01fc4c69d2bf`  
		Last Modified: Fri, 28 Oct 2022 21:20:54 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9887691021a9b5b0b8c064803e456c33828d9223b51b0cfd55927f788cf36627`  
		Last Modified: Fri, 28 Oct 2022 21:21:02 GMT  
		Size: 10.2 MB (10192823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033103d6f55b8eecd4e9de06bdc5c21cac7e6b833bf40dce45b3db524888667b`  
		Last Modified: Fri, 28 Oct 2022 21:20:54 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede4f6d1f1129703048e884cd8d16323280671fe06c0e26bcf040b90b42a528e`  
		Last Modified: Fri, 28 Oct 2022 21:20:54 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f935dbb4200103c2a5035cf239e503834a1cacb3366dc0b6a9422f5232a2a9e`  
		Last Modified: Fri, 28 Oct 2022 21:20:54 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e161fbcd4a098ebc5da194662fc3360f4c950e6042588dc2340f89c55ed5ff8`  
		Last Modified: Sat, 29 Oct 2022 03:24:40 GMT  
		Size: 148.9 KB (148939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d2cfa5e89c3fad3de51a1f9fa0a7a8007cfb62243cae0c5d08c34e4094b009`  
		Last Modified: Sat, 29 Oct 2022 03:24:40 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b3f2d5432f1785ebfedb378291a5028efddcf6395775e563bbdd50e10b3d1b`  
		Last Modified: Sat, 29 Oct 2022 03:24:37 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe46573e2f1d367e06578e86147e2106304accf5caabf6585ea32d8ac6765d8`  
		Last Modified: Sat, 29 Oct 2022 03:24:40 GMT  
		Size: 3.9 MB (3903424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3815cc1181c92d770161d63e7993ab68ed47b08b2f2828f67a5465dbda124515`  
		Last Modified: Sat, 29 Oct 2022 03:24:37 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6112a46670724848b7e154becacfa0dbfda0a2dd9fa9f73355c4f43cb2287f`  
		Last Modified: Sat, 29 Oct 2022 03:24:37 GMT  
		Size: 1.6 KB (1553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82d840b2c67aab82430cf5462f9dcd1a4c1187490c1288bb05588334e124867`  
		Last Modified: Sat, 29 Oct 2022 03:24:37 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:apache` - linux; ppc64le

```console
$ docker pull yourls@sha256:3b0aaab127664c834c40f057e9d0ff2d95e482aeec0f66058e8ba26eac39a115
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.0 MB (170006257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c24c817197e428fc84906d3fad729eff0257865c0698263998b805ff710e263c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 15 Nov 2022 05:18:45 GMT
ADD file:520926164fdc762143905745329e568c67289232bec450e48645d82a4613dccf in / 
# Tue, 15 Nov 2022 05:18:47 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:28:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 15 Nov 2022 05:28:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 15 Nov 2022 05:29:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 05:29:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 15 Nov 2022 05:29:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 15 Nov 2022 05:33:52 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 15 Nov 2022 05:33:52 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 15 Nov 2022 05:34:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 15 Nov 2022 05:34:14 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 15 Nov 2022 05:34:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 15 Nov 2022 05:34:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 15 Nov 2022 05:34:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 15 Nov 2022 05:34:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 15 Nov 2022 05:51:35 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 15 Nov 2022 05:51:35 GMT
ENV PHP_VERSION=8.1.12
# Tue, 15 Nov 2022 05:51:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.12.tar.xz.asc
# Tue, 15 Nov 2022 05:51:36 GMT
ENV PHP_SHA256=08243359e2204d842082269eedc15f08d2eca726d0e65b93fb11f4bfc51bbbab
# Tue, 15 Nov 2022 05:51:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 15 Nov 2022 05:52:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 15 Nov 2022 05:55:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 15 Nov 2022 05:55:55 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 15 Nov 2022 05:55:56 GMT
RUN docker-php-ext-enable sodium
# Tue, 15 Nov 2022 05:55:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 15 Nov 2022 05:55:57 GMT
STOPSIGNAL SIGWINCH
# Tue, 15 Nov 2022 05:55:58 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 15 Nov 2022 05:55:58 GMT
WORKDIR /var/www/html
# Tue, 15 Nov 2022 05:55:58 GMT
EXPOSE 80
# Tue, 15 Nov 2022 05:55:59 GMT
CMD ["apache2-foreground"]
# Tue, 15 Nov 2022 07:57:02 GMT
LABEL org.opencontainers.image.title=YOURLS
# Tue, 15 Nov 2022 07:57:02 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Tue, 15 Nov 2022 07:57:03 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Tue, 15 Nov 2022 07:57:03 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Tue, 15 Nov 2022 07:57:04 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Tue, 15 Nov 2022 07:57:04 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Tue, 15 Nov 2022 07:57:04 GMT
LABEL org.opencontainers.image.licenses=MIT
# Tue, 15 Nov 2022 07:57:04 GMT
LABEL io.artifacthub.package.readme-url=https://raw.githubusercontent.com/YOURLS/YOURLS/master/README.md
# Tue, 15 Nov 2022 07:57:37 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Tue, 15 Nov 2022 07:57:38 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 15 Nov 2022 07:57:39 GMT
RUN a2enmod rewrite expires
# Tue, 15 Nov 2022 07:57:40 GMT
ARG YOURLS_VERSION=1.9.1
# Tue, 15 Nov 2022 07:57:40 GMT
ARG YOURLS_SHA256=0bf53290e8f86ea2e0121aac70f7c64d70d3dfb54823acb9dcc343dd7c5f455a
# Tue, 15 Nov 2022 07:57:40 GMT
LABEL org.opencontainers.image.version=1.9.1
# Tue, 15 Nov 2022 07:57:41 GMT
ENV YOURLS_VERSION=1.9.1
# Tue, 15 Nov 2022 07:57:41 GMT
ENV YOURLS_SHA256=0bf53290e8f86ea2e0121aac70f7c64d70d3dfb54823acb9dcc343dd7c5f455a
# Tue, 15 Nov 2022 07:57:44 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Tue, 15 Nov 2022 07:57:44 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Tue, 15 Nov 2022 07:57:45 GMT
COPY file:975ababf859e7cabd8184ab0b2b317a5d8d3ccb6f4922be7f2a5d28c20d075a2 in /usr/local/bin/ 
# Tue, 15 Nov 2022 07:57:45 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Tue, 15 Nov 2022 07:57:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 07:57:46 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c57913b7d0318ef1a47f0348ce54d9865316776aa1ffb2c7871b1473b3d29407`  
		Last Modified: Tue, 15 Nov 2022 05:24:22 GMT  
		Size: 35.3 MB (35285140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f0beaf56e20c42dc99adac83339859a68fe21121e2a97694ccf17bb3d80a1f`  
		Last Modified: Tue, 15 Nov 2022 07:02:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb01e5ff921e5a6fdfd50966abf1a71511e1fc3d7c5b93c0f0d23c4b01bde8ad`  
		Last Modified: Tue, 15 Nov 2022 07:03:05 GMT  
		Size: 86.6 MB (86632107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b444ab201aca26c541ce9ce4732f100ccd2fd815497509f4281f39038ecdb838`  
		Last Modified: Tue, 15 Nov 2022 07:02:41 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fca4b0f24135682d7d43d92cc3e475e3a1f7d0b0685dac72569e8aeb202701`  
		Last Modified: Tue, 15 Nov 2022 07:03:44 GMT  
		Size: 20.5 MB (20465178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f0a8d837f689661b3916dc15531fa63568b8f8dd569bcdf1419e76c70fe957`  
		Last Modified: Tue, 15 Nov 2022 07:03:39 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7270d82c3d39663e1b3ad3a50a772b6757d614fec5eb597256a1c63eb532cc15`  
		Last Modified: Tue, 15 Nov 2022 07:03:39 GMT  
		Size: 514.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1868fd131248f8b46b4697272e5f994b2342afb86032b19160bfc225ee0844`  
		Last Modified: Tue, 15 Nov 2022 07:06:19 GMT  
		Size: 12.1 MB (12088033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a74e531ea1424c6fd8838fb09ee1efb32a9c16f4568e6fbf5473fd846419c8`  
		Last Modified: Tue, 15 Nov 2022 07:06:16 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9c86f1ee1eba0f0b04f71f08662b6fe84e84dca068977c39ab3ff2b6459f3b`  
		Last Modified: Tue, 15 Nov 2022 07:06:17 GMT  
		Size: 11.4 MB (11438349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f93ec1658455d4e9ba9830c040b50bfd232cd6ba0a278a19d8247d45c419ad`  
		Last Modified: Tue, 15 Nov 2022 07:06:14 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0a391f38fac0984781fed01a0bdee4ebbfb62959bb17d5b1c046fedae00456`  
		Last Modified: Tue, 15 Nov 2022 07:06:14 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7330ae538872a67b7e9a053e9e2d3e39e2d7e49b02363d9d9fadf509e097b4`  
		Last Modified: Tue, 15 Nov 2022 07:06:16 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac92ba4934f9cd519067bb4c71d6cae55e4c44009b0258ce09b93910432e125`  
		Last Modified: Tue, 15 Nov 2022 07:59:27 GMT  
		Size: 183.7 KB (183741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59bc9722d11ad152bce1661bc888f87826cc0ffe8558ae02e3024e04cb0a98ba`  
		Last Modified: Tue, 15 Nov 2022 07:59:27 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8508831a52b5a6bfe2fa31090580cbd2cfcda7a2edba123066959d22d30078`  
		Last Modified: Tue, 15 Nov 2022 07:59:25 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68d404b8ea150e71e36bb0d32fa45b8a29e4d6e41569e75b8ca362b2e01ca2f`  
		Last Modified: Tue, 15 Nov 2022 07:59:26 GMT  
		Size: 3.9 MB (3903529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291acb1bd8f4d126c6e1742cc63e16fb17a522fc6bc1545cbe326871f7f190e7`  
		Last Modified: Tue, 15 Nov 2022 07:59:25 GMT  
		Size: 2.1 KB (2051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5a3429e8ddaeeabc21c79cdf19da440d35576cc2fb519820483d80c1cdc836`  
		Last Modified: Tue, 15 Nov 2022 07:59:25 GMT  
		Size: 1.6 KB (1551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902c5922a0e32c3fea89b75629ae9850407d712cd66d0e33f1d0f58e4c11a320`  
		Last Modified: Tue, 15 Nov 2022 07:59:25 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:apache` - linux; s390x

```console
$ docker pull yourls@sha256:624e81e372ac938682593194c2d0409914dcd06791343cdfc33472fc9b6d00d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.7 MB (146687628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1578805b9e90a6dd11530d221b10bab0e0178c3479ba10547dad7127a35fc825`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 25 Oct 2022 01:14:42 GMT
ADD file:1bb8efa7f80e494b9d2831490a7e74810350c1f9ee2d100596d2e1cb4c62f529 in / 
# Tue, 25 Oct 2022 01:14:44 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:44:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 25 Oct 2022 04:44:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 25 Oct 2022 04:44:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:44:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 25 Oct 2022 04:44:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 25 Oct 2022 04:47:09 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 25 Oct 2022 04:47:10 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 25 Oct 2022 04:47:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 25 Oct 2022 04:47:20 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 25 Oct 2022 04:47:20 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 25 Oct 2022 04:47:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Oct 2022 04:47:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Oct 2022 04:47:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 25 Oct 2022 04:57:21 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 28 Oct 2022 18:45:28 GMT
ENV PHP_VERSION=8.1.12
# Fri, 28 Oct 2022 18:45:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.12.tar.xz.asc
# Fri, 28 Oct 2022 18:45:29 GMT
ENV PHP_SHA256=08243359e2204d842082269eedc15f08d2eca726d0e65b93fb11f4bfc51bbbab
# Fri, 28 Oct 2022 18:45:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 28 Oct 2022 18:45:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 28 Oct 2022 18:47:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 28 Oct 2022 18:47:37 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 28 Oct 2022 18:47:38 GMT
RUN docker-php-ext-enable sodium
# Fri, 28 Oct 2022 18:47:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 28 Oct 2022 18:47:38 GMT
STOPSIGNAL SIGWINCH
# Fri, 28 Oct 2022 18:47:38 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 28 Oct 2022 18:47:38 GMT
WORKDIR /var/www/html
# Fri, 28 Oct 2022 18:47:39 GMT
EXPOSE 80
# Fri, 28 Oct 2022 18:47:39 GMT
CMD ["apache2-foreground"]
# Fri, 28 Oct 2022 21:54:01 GMT
LABEL org.opencontainers.image.title=YOURLS
# Fri, 28 Oct 2022 21:54:01 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Fri, 28 Oct 2022 21:54:01 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Fri, 28 Oct 2022 21:54:02 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Fri, 28 Oct 2022 21:54:02 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Fri, 28 Oct 2022 21:54:02 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Fri, 28 Oct 2022 21:54:02 GMT
LABEL org.opencontainers.image.licenses=MIT
# Fri, 28 Oct 2022 21:54:02 GMT
LABEL io.artifacthub.package.readme-url=https://raw.githubusercontent.com/YOURLS/YOURLS/master/README.md
# Fri, 28 Oct 2022 21:54:16 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Fri, 28 Oct 2022 21:54:17 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 28 Oct 2022 21:54:17 GMT
RUN a2enmod rewrite expires
# Fri, 28 Oct 2022 21:54:17 GMT
ARG YOURLS_VERSION=1.9.1
# Fri, 28 Oct 2022 21:54:17 GMT
ARG YOURLS_SHA256=0bf53290e8f86ea2e0121aac70f7c64d70d3dfb54823acb9dcc343dd7c5f455a
# Fri, 28 Oct 2022 21:54:18 GMT
LABEL org.opencontainers.image.version=1.9.1
# Fri, 28 Oct 2022 21:54:18 GMT
ENV YOURLS_VERSION=1.9.1
# Fri, 28 Oct 2022 21:54:18 GMT
ENV YOURLS_SHA256=0bf53290e8f86ea2e0121aac70f7c64d70d3dfb54823acb9dcc343dd7c5f455a
# Fri, 28 Oct 2022 21:54:20 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 28 Oct 2022 21:54:20 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Fri, 28 Oct 2022 21:54:20 GMT
COPY file:975ababf859e7cabd8184ab0b2b317a5d8d3ccb6f4922be7f2a5d28c20d075a2 in /usr/local/bin/ 
# Fri, 28 Oct 2022 21:54:20 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Fri, 28 Oct 2022 21:54:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 21:54:20 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:abc14eb2518761d53b91fc564a31b657914f96b531f99a74ac8268f0717b007e`  
		Last Modified: Tue, 25 Oct 2022 01:19:01 GMT  
		Size: 29.7 MB (29650722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d036b7cffe54cd9d789fe0faa587ecaf8b153f4d347002ed7998536a576ae062`  
		Last Modified: Tue, 25 Oct 2022 05:42:14 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070976ca7bd4e77169299c5a0ea0650757087daf6336a25abb7081a0fa21d54b`  
		Last Modified: Tue, 25 Oct 2022 05:42:24 GMT  
		Size: 71.6 MB (71627350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29da416964c90c6db6eda606ac4b2abecd381679522e3ab489e10647a073d4b`  
		Last Modified: Tue, 25 Oct 2022 05:42:14 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa39ea5aaa0ffd5cecec38111af54dc638f8bc44aebc4e171b8ab9d4c472185b`  
		Last Modified: Tue, 25 Oct 2022 05:42:48 GMT  
		Size: 19.1 MB (19072156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80401cf2ff359a61b436397dc7d370995f9f8a74d13f718342fe4269672a4016`  
		Last Modified: Tue, 25 Oct 2022 05:42:45 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7653ac31134af41584a523d68f26d723c79148816378a6d90a5fe287b75df997`  
		Last Modified: Tue, 25 Oct 2022 05:42:45 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa04b4a3e5d712e1d91fda7d727f1fd9e612da2df3c90806a1a4f013720b7dee`  
		Last Modified: Fri, 28 Oct 2022 19:49:58 GMT  
		Size: 12.1 MB (12087130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea18c7307b148be56d40e5894e74502ff2e25809a7d5b3ff1230bddf02ef50b`  
		Last Modified: Fri, 28 Oct 2022 19:49:57 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f1367e7aae88eda780c06751d73b36f383947e328a79822c45992d8dacf38b`  
		Last Modified: Fri, 28 Oct 2022 19:49:59 GMT  
		Size: 10.2 MB (10178353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f750adc3fe79441dae37842cf6a945fe122fa83d3810ac54569c1e38fbf97548`  
		Last Modified: Fri, 28 Oct 2022 19:49:57 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea02ea68c5525f3755d84d7e50daca1c350ff32a276e57387f5e94874166ab7e`  
		Last Modified: Fri, 28 Oct 2022 19:49:57 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3e277344758c8e817a74146bc13eff7475f92b75171541b24e7e4ddc907417`  
		Last Modified: Fri, 28 Oct 2022 19:49:57 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2194641d9acb549f913431c12eed54497a58a591231bf54dd97a6ec19df4e2f9`  
		Last Modified: Fri, 28 Oct 2022 21:56:06 GMT  
		Size: 158.2 KB (158206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20858f700bfe677cf3395b6d92b0948fa46c6bd6f1001bd54ae21c4ec1791b9d`  
		Last Modified: Fri, 28 Oct 2022 21:56:06 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2425b43e179657d56d53e618482b0e7eeaf503c12599381d7f13f9a91c16cd3`  
		Last Modified: Fri, 28 Oct 2022 21:56:05 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b97c2dd75eb4e8b56f7e9aad6ece9f397a118a4616d3308074332ca99a0ed9`  
		Last Modified: Fri, 28 Oct 2022 21:56:06 GMT  
		Size: 3.9 MB (3903531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e644aa768beeb17ccab9ee9abc00ce747cd234c60ea25877278240da412dae2d`  
		Last Modified: Fri, 28 Oct 2022 21:56:05 GMT  
		Size: 2.0 KB (2050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c189056fd7938e8e22c49e06bbc64a4208a3bf8df107a4cbe7b03b61286051`  
		Last Modified: Fri, 28 Oct 2022 21:56:05 GMT  
		Size: 1.6 KB (1554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3586cb5f76eb98d44a62c2fb37b13e346156c53d6ca137f943d262d6269179`  
		Last Modified: Fri, 28 Oct 2022 21:56:05 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
