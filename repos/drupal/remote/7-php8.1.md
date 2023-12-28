## `drupal:7-php8.1`

```console
$ docker pull drupal@sha256:456fa560998cf352cec84249786318115dc66532a66a6b00f05a6c83d7bea224
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `drupal:7-php8.1` - linux; amd64

```console
$ docker pull drupal@sha256:d9df9ce83f53cb40df4195be145dd3db3bcce95144bb8808801be8eb0a1b0fa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.1 MB (183114468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e55b012712fe12c4706812ffadecd427dcc68f5ffb4ebc0bf68fd75bb733388`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Dec 2023 16:27:27 GMT
ADD file:ac3cd70031d35e46d86b876934946ffc8756de4de065fbc926dce642dac07ff3 in / 
# Wed, 06 Dec 2023 16:27:27 GMT
CMD ["bash"]
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Dec 2023 16:27:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 06 Dec 2023 16:27:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 06 Dec 2023 16:27:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 06 Dec 2023 16:27:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Dec 2023 16:27:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_VERSION=8.1.27
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 06 Dec 2023 16:27:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Dec 2023 16:27:27 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 06 Dec 2023 16:27:27 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Dec 2023 16:27:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Dec 2023 16:27:27 GMT
STOPSIGNAL SIGWINCH
# Wed, 06 Dec 2023 16:27:27 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 06 Dec 2023 16:27:27 GMT
WORKDIR /var/www/html
# Wed, 06 Dec 2023 16:27:27 GMT
EXPOSE 80
# Wed, 06 Dec 2023 16:27:27 GMT
CMD ["apache2-foreground"]
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Dec 2023 16:27:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Dec 2023 16:27:27 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 06 Dec 2023 16:27:27 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:af107e978371b6cd6339127a05502c5eacd1e6b0e9eb7b2f4aa7b6fc87e2dd81`  
		Last Modified: Tue, 19 Dec 2023 01:24:59 GMT  
		Size: 29.1 MB (29125963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6480d4ad61d22c10d4a7237828e51d8a2ca3b5d60fcdf3d9800350353b5ac3fa`  
		Last Modified: Tue, 19 Dec 2023 15:37:58 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f5176ece8bbdb815830df5e9eab427554c171d3b1459ced51bd7f991b2d9c5`  
		Last Modified: Tue, 19 Dec 2023 15:38:13 GMT  
		Size: 104.4 MB (104353017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebe7ec824ca8231eb30bfc1bc1416a2e73ecc77cefb226cba43ab8c84676045`  
		Last Modified: Tue, 19 Dec 2023 15:37:58 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673e01769ec9ab92c5580bf1b3de45ce83ad6fb946a2a1c53bf6f546d61ab109`  
		Last Modified: Tue, 19 Dec 2023 15:38:40 GMT  
		Size: 20.3 MB (20303667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f0c50b3097295649c2ae489f3540f903bff7f8d18a53e291445c931f6cc7a0`  
		Last Modified: Tue, 19 Dec 2023 15:38:36 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a19a72eb529a45c1f923059e6e81d8d3fef65976b2272628309d6b46464f661`  
		Last Modified: Tue, 19 Dec 2023 15:38:36 GMT  
		Size: 512.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0cd18e26046f651008c1ad2d54f2ac671b62aed31e3a24149f78e67418df8f`  
		Last Modified: Thu, 28 Dec 2023 01:23:41 GMT  
		Size: 12.2 MB (12247865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51ef88f85cfc79981d41f34d76c9e4144835f7c73ecbbaa903e2f4f48855bb5`  
		Last Modified: Thu, 28 Dec 2023 01:23:39 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b92334d134c68f1a7d38b12c82e3532991269ae044ee8539381d7a4a3abe2f`  
		Last Modified: Thu, 28 Dec 2023 01:23:41 GMT  
		Size: 11.7 MB (11663105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb99e086d955b16bfc644959fb0fab20e51a6c723b74bbadde5f38a2ea46e31c`  
		Last Modified: Thu, 28 Dec 2023 01:23:39 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b348e609e61b76f4b296665495448725be757967665590287241d656cd6826d7`  
		Last Modified: Thu, 28 Dec 2023 01:23:39 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c8a004defd34ba7a18d811304b0f081e40e5d32e6e9b2601047d1e1f67fd17`  
		Last Modified: Thu, 28 Dec 2023 01:23:39 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ec7a52a337b59c83ddd0846ccad19af9223a99b35f3d8bf21e345871b0a3ab`  
		Last Modified: Thu, 28 Dec 2023 02:48:55 GMT  
		Size: 2.0 MB (1996069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9149b1362f5def03394b8400b19c65f614d9137bc6454e67fe11bf50af988d4a`  
		Last Modified: Thu, 28 Dec 2023 02:48:55 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e574b29444890dad8c54cf2715bb1541b31facbf0042fd921361c941768fb7`  
		Last Modified: Thu, 28 Dec 2023 02:48:56 GMT  
		Size: 3.4 MB (3418878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1` - unknown; unknown

```console
$ docker pull drupal@sha256:e929b646b8076e9c0159313cb5198434140823bd268ae9d55d2a0d0d2a866b08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5895967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54187452b8a0607bb552b274eb37405965230d4b44237ad584964becf5146a67`

```dockerfile
```

-	Layers:
	-	`sha256:c5ca7a8f2c7c79f7da25060b06e4698e5c0b1a1fe75f520d94b52408a678b43a`  
		Last Modified: Thu, 28 Dec 2023 02:48:54 GMT  
		Size: 5.9 MB (5866132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b183e879ac1a3079230bda6d134dcd9b3c03343722d4d9db4bb7520c6523aac5`  
		Last Modified: Thu, 28 Dec 2023 02:48:54 GMT  
		Size: 29.8 KB (29835 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1` - linux; arm variant v5

```console
$ docker pull drupal@sha256:b9b951069c46e5906ddf431c62da92aeac3e73c6f2af63f045ac8fc69cffec92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156220347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47dc33b19250d75b10219cf9cd000a0b5eac32c0761e1043507948127659204`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Dec 2023 16:27:27 GMT
ADD file:9503ab966c9dd707eeccc7c2f633bccc94c199f8714ec4ff2c8b54dde3dbabf9 in / 
# Wed, 06 Dec 2023 16:27:27 GMT
CMD ["bash"]
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Dec 2023 16:27:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 06 Dec 2023 16:27:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 06 Dec 2023 16:27:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 06 Dec 2023 16:27:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Dec 2023 16:27:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_VERSION=8.1.27
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 06 Dec 2023 16:27:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Dec 2023 16:27:27 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 06 Dec 2023 16:27:27 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Dec 2023 16:27:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Dec 2023 16:27:27 GMT
STOPSIGNAL SIGWINCH
# Wed, 06 Dec 2023 16:27:27 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 06 Dec 2023 16:27:27 GMT
WORKDIR /var/www/html
# Wed, 06 Dec 2023 16:27:27 GMT
EXPOSE 80
# Wed, 06 Dec 2023 16:27:27 GMT
CMD ["apache2-foreground"]
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Dec 2023 16:27:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Dec 2023 16:27:27 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 06 Dec 2023 16:27:27 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:1ae9a2844c8c70942d2220553689b62e841cc706d77284fbfedbd770080fd699`  
		Last Modified: Tue, 19 Dec 2023 01:58:33 GMT  
		Size: 26.9 MB (26885440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f34b73d2d8e6b1b2c10c6eb4b942988f6ab53d0815dcfbc221d087c716a8b22`  
		Last Modified: Tue, 19 Dec 2023 04:47:53 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c7dffc50fc2b8f2714576406c9c543112a528c0e55e72bb5dcd48e02d697ba`  
		Last Modified: Tue, 19 Dec 2023 04:48:08 GMT  
		Size: 82.0 MB (81999515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0cdf3a474021cac2a6c3b988a5a48cf4a73327b3205a3ba51d644f6035b4456`  
		Last Modified: Tue, 19 Dec 2023 04:47:53 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ddaddfc8f048c69c45769fae6c7545f575b88ca39d32f7e745157aacfaefe3`  
		Last Modified: Tue, 19 Dec 2023 04:48:35 GMT  
		Size: 19.6 MB (19608241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97e438b6275096e6d3a330b3d49be2ece9486d7bb206bea33328ce2364eaa6f`  
		Last Modified: Tue, 19 Dec 2023 04:48:32 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298b2a8ea271468b38aed2074dec7c9ef02c04bf65e903e14b264641f3ca2ff5`  
		Last Modified: Tue, 19 Dec 2023 04:48:32 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14001dc8ec2814eba15e233ef5739a2ce1ef36a70d40cf6d5409eb0bd9f31c55`  
		Last Modified: Thu, 28 Dec 2023 00:38:14 GMT  
		Size: 12.2 MB (12245914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abad5007734cd58b0c66e24f7bf61adff179744c659c7b3c36d1e37563cf89d3`  
		Last Modified: Thu, 28 Dec 2023 00:38:11 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4a4eb4f1d09dbc769d915a6d01a0ef4b91ed7eb8a17faafa2437b04169b544`  
		Last Modified: Thu, 28 Dec 2023 00:38:14 GMT  
		Size: 10.6 MB (10593991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbd06163cd5e58e925dc7844872e89138ce83e1fb4369f0729116a642eafee3`  
		Last Modified: Thu, 28 Dec 2023 00:38:11 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9caee4d7320dddda3e8c9d7d7d9e788edc5b9fbd2e7167e65a66c82f0bfe758c`  
		Last Modified: Thu, 28 Dec 2023 00:38:11 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf6ff1c00544cd117c02c17fdd17a438ad777f9aa67e2eb5e84473684efacfa`  
		Last Modified: Thu, 28 Dec 2023 00:38:11 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7d9b6fe932347d958ddf888fb1463d97177fa007f385f5c1efc404486ace22`  
		Last Modified: Thu, 28 Dec 2023 04:09:07 GMT  
		Size: 1.5 MB (1462468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2e90812fff864c17040521dc5523e308080d34c27f7fd0300975b24c9707c9`  
		Last Modified: Thu, 28 Dec 2023 04:09:07 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabe64cd98905720daa13d46b715ab728ba15a4309130d0e95f0374fab93c7cb`  
		Last Modified: Thu, 28 Dec 2023 04:09:08 GMT  
		Size: 3.4 MB (3418877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1` - unknown; unknown

```console
$ docker pull drupal@sha256:81778a89dace2a5e2be563c7524677ee1f7261e9f6216d85fab0f5d0c72394bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5731804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8620145d829ab95ae8a2835d6314aff656fff1eacb58fd10fc828ba9b7407486`

```dockerfile
```

-	Layers:
	-	`sha256:f2eb5d0077546b1bde20bb849b4609f9dd806f2aaae44ad1d1481134ff283563`  
		Last Modified: Thu, 28 Dec 2023 04:09:06 GMT  
		Size: 5.7 MB (5701813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13931fb6ebf6957b7337eb1d98f1ad039db9aa914242490243a251b6ea4e5c08`  
		Last Modified: Thu, 28 Dec 2023 04:09:05 GMT  
		Size: 30.0 KB (29991 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1` - linux; arm variant v7

```console
$ docker pull drupal@sha256:a8e7690d00b611b9d8d5fb7ea659f59858150d01e0fb566761a6996b35bc753d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.0 MB (146971254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8f5126ba895db14e9224373ba0f2cb5146e1c8703bf68f7468dc97a44b772a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Dec 2023 16:27:27 GMT
ADD file:aef112919e7924ad6da32181b1df5099cd692680c104118da3a24cd4dfe55a1d in / 
# Wed, 06 Dec 2023 16:27:27 GMT
CMD ["bash"]
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Dec 2023 16:27:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 06 Dec 2023 16:27:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 06 Dec 2023 16:27:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 06 Dec 2023 16:27:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Dec 2023 16:27:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_VERSION=8.1.27
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 06 Dec 2023 16:27:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Dec 2023 16:27:27 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 06 Dec 2023 16:27:27 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Dec 2023 16:27:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Dec 2023 16:27:27 GMT
STOPSIGNAL SIGWINCH
# Wed, 06 Dec 2023 16:27:27 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 06 Dec 2023 16:27:27 GMT
WORKDIR /var/www/html
# Wed, 06 Dec 2023 16:27:27 GMT
EXPOSE 80
# Wed, 06 Dec 2023 16:27:27 GMT
CMD ["apache2-foreground"]
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Dec 2023 16:27:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Dec 2023 16:27:27 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 06 Dec 2023 16:27:27 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:65ab19615c01a3b542f77fadb3bd27872b6a20cba3e9269fb951de36d8fa6805`  
		Last Modified: Tue, 19 Dec 2023 02:11:52 GMT  
		Size: 24.7 MB (24718157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65740699e811c46b300dc1c124377acd0b62ad6293d766b800ff0b0b1b15ee4`  
		Last Modified: Tue, 19 Dec 2023 07:35:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec00c82ca03d32d2179c766fbeb2791d1a6a7104cd30a45449f41afb3f0330b`  
		Last Modified: Tue, 19 Dec 2023 07:35:33 GMT  
		Size: 76.2 MB (76167957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0665bd380315b2d7d72a79a178c0632e460bcca310ce7a4d22f72d74308b66`  
		Last Modified: Tue, 19 Dec 2023 07:35:21 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87e8e176db52cf02bbac190df26c2b5b2d182d6fc422d729b45cbbd4dc7d955`  
		Last Modified: Tue, 19 Dec 2023 07:36:03 GMT  
		Size: 19.0 MB (19045352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e9c21e2f8d836c54fb9350565c794082c47ae434dd3144be72fc15ac3a9279`  
		Last Modified: Tue, 19 Dec 2023 07:35:59 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1927f0f803b500e6a170c314fa969007b5682fd1ffd745f1de74bee82a931f0`  
		Last Modified: Tue, 19 Dec 2023 07:35:59 GMT  
		Size: 512.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ed6cac110eaa072c8e54e24f2f72e71067c3ff3d9b3b491e328cf0ff91012e`  
		Last Modified: Thu, 28 Dec 2023 02:56:04 GMT  
		Size: 12.2 MB (12245895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02f2521d0131b12aee553634bc0a77264e8efbb7b3149fca19706f98c143482`  
		Last Modified: Thu, 28 Dec 2023 02:56:01 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d56039f6425053b12d7803ddd97b1fada42f38d231f8b8103bfa536ed22a63`  
		Last Modified: Thu, 28 Dec 2023 02:56:04 GMT  
		Size: 10.0 MB (10024261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2fd9439b47c9f4ac2e616965544c53e73452f74aa3970316b30d9a7beeabe3d`  
		Last Modified: Thu, 28 Dec 2023 02:56:01 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8cb315c8b7dd28eb7710cf655501a11877dce475a404e9e113b90326529182`  
		Last Modified: Thu, 28 Dec 2023 02:56:01 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f23331ad58108ec19356a3e7682be534465c5764fe439d39cb7c782523db06`  
		Last Modified: Thu, 28 Dec 2023 02:56:01 GMT  
		Size: 897.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e946312da6c557bbde1f87e5681dcda9f33c3395ae6aea12f961f692b00417`  
		Last Modified: Thu, 28 Dec 2023 08:51:09 GMT  
		Size: 1.3 MB (1344852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be10f0607b62c43db6d33b2173489ce4f9254f35b8df318bf064621338691502`  
		Last Modified: Thu, 28 Dec 2023 08:51:09 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d137378864c655bb38218821f9fab0029d8fe5a5c0b00d2c7ffc59a589276a`  
		Last Modified: Thu, 28 Dec 2023 09:29:59 GMT  
		Size: 3.4 MB (3418879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1` - unknown; unknown

```console
$ docker pull drupal@sha256:fa8d659a0d1ebf39a6de333641b34d51eee49e6f82f158d5732faabe1b3690ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5733681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083bab0a63550047c4a0b0623bfc3dcdfc8b3ea20ae0aead58c20f04e966b140`

```dockerfile
```

-	Layers:
	-	`sha256:65418bff0bcdee75210fda3142a2b862d014fd3fc9e2990695fdd55e5a3608ee`  
		Last Modified: Thu, 28 Dec 2023 09:29:58 GMT  
		Size: 5.7 MB (5705799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:436c90d20dae618752d04745b8e246751b83acdde51a664e7fef9ae31c8ce7a8`  
		Last Modified: Thu, 28 Dec 2023 09:29:57 GMT  
		Size: 27.9 KB (27882 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:791012d28a822d227af577e16a90eb789c68ce2e0fe8f2e981674a2bb9b8482d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.2 MB (177168628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b51d372473a8ff316a2398e355f4634b0e2163fe58df3164e568dd629138a8ae`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Dec 2023 16:27:27 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Wed, 06 Dec 2023 16:27:27 GMT
CMD ["bash"]
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Dec 2023 16:27:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 06 Dec 2023 16:27:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 06 Dec 2023 16:27:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 06 Dec 2023 16:27:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Dec 2023 16:27:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_VERSION=8.1.27
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 06 Dec 2023 16:27:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Dec 2023 16:27:27 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 06 Dec 2023 16:27:27 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Dec 2023 16:27:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Dec 2023 16:27:27 GMT
STOPSIGNAL SIGWINCH
# Wed, 06 Dec 2023 16:27:27 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 06 Dec 2023 16:27:27 GMT
WORKDIR /var/www/html
# Wed, 06 Dec 2023 16:27:27 GMT
EXPOSE 80
# Wed, 06 Dec 2023 16:27:27 GMT
CMD ["apache2-foreground"]
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Dec 2023 16:27:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Dec 2023 16:27:27 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 06 Dec 2023 16:27:27 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e96785d20e673831d412d2f9b010766cf6cc304754506c9f319a0c310648a0`  
		Last Modified: Tue, 19 Dec 2023 06:09:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938e1c871e0583217541b555fdb548e900c71ae825a7b19ce7a08b9263ad1e06`  
		Last Modified: Tue, 19 Dec 2023 06:09:26 GMT  
		Size: 98.1 MB (98126940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c628ed3e4c42b1a141608f9c9e2b48f01921e2ad6dc5ae8821b194a014a954c6`  
		Last Modified: Tue, 19 Dec 2023 06:09:15 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ba4aaa606d2789d4d1e1ea8b1e3f2941844d13760133bd44eeb1b74d49578f`  
		Last Modified: Tue, 19 Dec 2023 06:09:55 GMT  
		Size: 20.3 MB (20305017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aac66f1c9c7993085a363e1621997697944a88c2c12e1d308c13f30477a7072`  
		Last Modified: Tue, 19 Dec 2023 06:09:51 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8425f87af575dd0a67b357b654b7e598884925e2e771055d7806bdc98ca125`  
		Last Modified: Tue, 19 Dec 2023 06:09:51 GMT  
		Size: 514.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57268dd07433db6b42a2e8d755c048cdf2260656bc225879704fd2fe6a3de1c3`  
		Last Modified: Thu, 28 Dec 2023 00:39:32 GMT  
		Size: 12.2 MB (12247514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac09d2edb2e7db42a44944e892e8a89e7f400b4a7f17cfdc4ae490a782dced7`  
		Last Modified: Thu, 28 Dec 2023 00:39:29 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07559cf411acc4ff99914fea6ac1ab8503b8f44e8bbdcf244af928d9bbe6caba`  
		Last Modified: Thu, 28 Dec 2023 00:39:31 GMT  
		Size: 11.7 MB (11652831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac916f2a0323e85f0839f02950316541bb3503b05422afc86f162d33198550ff`  
		Last Modified: Thu, 28 Dec 2023 00:39:29 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f12e96a4387cd46194b875d94a735b4c4fecd545764ebd3378cb1266b1b33b7`  
		Last Modified: Thu, 28 Dec 2023 00:39:29 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7de4d59077d1ee358000304e94f398766ebcf3757a13ff0be1de5f2b3f90a37`  
		Last Modified: Thu, 28 Dec 2023 00:39:29 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3189ba380dbae7b4765e460de34186b380c5a1a79564744b98801ec1358b3e33`  
		Last Modified: Thu, 28 Dec 2023 05:57:10 GMT  
		Size: 2.3 MB (2254277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d9e9c00f76665e2cbc0f173953398d9ff6f30569e5654bc3ff461b0dadfdaa`  
		Last Modified: Thu, 28 Dec 2023 05:57:10 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e35e049f4a4349199458870ff931a81ddfe2590b8ce339e0e1d84d047b13dcf`  
		Last Modified: Thu, 28 Dec 2023 06:14:55 GMT  
		Size: 3.4 MB (3418879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1` - unknown; unknown

```console
$ docker pull drupal@sha256:99f856763e5bea64483c7ce37929ae57992f45153b1c0c3bc6357cdb5bcaaefb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5918904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0860d64eb6bb64903a7625b29aa1b12312f373de1acafd21449bb3058754fb9`

```dockerfile
```

-	Layers:
	-	`sha256:380adce1d5feacfef7f49eea8ea8a8b9f61a4bb1a2de305e03e5da74ac109971`  
		Last Modified: Thu, 28 Dec 2023 06:14:54 GMT  
		Size: 5.9 MB (5891155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9307408c84c02565830ac6de4ebc8dfe5a5583d713ee2a24d0e32b48616708b0`  
		Last Modified: Thu, 28 Dec 2023 06:14:54 GMT  
		Size: 27.7 KB (27749 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1` - linux; 386

```console
$ docker pull drupal@sha256:b06c47f2e6962fefce5a000e5757be3d3bece902988e6a5463f5ddec47ff61bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.2 MB (182153586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745d563647f0f6dbd154b84f1f8cf96ec3e3cb0b8121b7e10347a784efb44b7f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Dec 2023 16:27:27 GMT
ADD file:6f4083d57ea9644b5a827e67b0725087a15aa428272ec223ab968bf8b4623e42 in / 
# Wed, 06 Dec 2023 16:27:27 GMT
CMD ["bash"]
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Dec 2023 16:27:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 06 Dec 2023 16:27:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 06 Dec 2023 16:27:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 06 Dec 2023 16:27:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Dec 2023 16:27:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_VERSION=8.1.27
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 06 Dec 2023 16:27:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Dec 2023 16:27:27 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 06 Dec 2023 16:27:27 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Dec 2023 16:27:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Dec 2023 16:27:27 GMT
STOPSIGNAL SIGWINCH
# Wed, 06 Dec 2023 16:27:27 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 06 Dec 2023 16:27:27 GMT
WORKDIR /var/www/html
# Wed, 06 Dec 2023 16:27:27 GMT
EXPOSE 80
# Wed, 06 Dec 2023 16:27:27 GMT
CMD ["apache2-foreground"]
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Dec 2023 16:27:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Dec 2023 16:27:27 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 06 Dec 2023 16:27:27 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:8d4aad22fb6a12b8cc7a78d338dfb9bc2bd6d621517b374e446f2915833ea883`  
		Last Modified: Tue, 19 Dec 2023 01:43:45 GMT  
		Size: 30.1 MB (30143863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a67261edd7b9e6693f4cb4099c5f0cac3b8242bb32462503c7b4601fb022c0f`  
		Last Modified: Tue, 19 Dec 2023 21:54:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34da8f089333e690321a44246a643bc3740e16fa4b064ad14edebdc446947cf`  
		Last Modified: Tue, 19 Dec 2023 21:54:37 GMT  
		Size: 101.5 MB (101534007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f20232fd1a6a3744f261b8cd8703645db2b73ba9c6f9f8767ed58c0035369b9`  
		Last Modified: Tue, 19 Dec 2023 21:54:13 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583c28de16ed8105fb75c436c9824fa03b132682c59c628af399c890092f4686`  
		Last Modified: Tue, 19 Dec 2023 21:55:07 GMT  
		Size: 20.8 MB (20825931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06b93afaa9d72db57b4db14cfe41e83f4b76c91b3bfc984b97039b917be5b46`  
		Last Modified: Tue, 19 Dec 2023 21:55:02 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ae963a8ff2191c2e247d38578ad8643b11cc4903c0dac19a5a41f6b3ef2daf`  
		Last Modified: Tue, 19 Dec 2023 21:55:02 GMT  
		Size: 515.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7e91010d4db11ab5c2370b97ce1e328b46255fa90c0155871d5f13cf3b6ca6`  
		Last Modified: Thu, 28 Dec 2023 02:24:15 GMT  
		Size: 12.2 MB (12246916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7626bf4fd162423cb72350b1627fe343017449b2d52c7bfe4f6e52ff9929a973`  
		Last Modified: Thu, 28 Dec 2023 02:24:11 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b7a9a7dbaae5d64ad8581574e7e04e2b8107d5f1b3703957bb924791ff2e7d`  
		Last Modified: Thu, 28 Dec 2023 02:24:16 GMT  
		Size: 11.9 MB (11930067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541509d027a4b41d779b3d225e6032800bdc351fa3be6b83f5cc7910e5839c13`  
		Last Modified: Thu, 28 Dec 2023 02:24:11 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b94ac801558778f527c9fd8e90546db224b012de837cc65b41f4a41f0f8a7d`  
		Last Modified: Thu, 28 Dec 2023 02:24:11 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f348589cf477a96e216bdd57b54b3f40824457907ed2f62197c9a094e112251a`  
		Last Modified: Thu, 28 Dec 2023 02:24:11 GMT  
		Size: 897.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb4fd3fbc9aff4933469015e0f85c739ef9423aefe369911a564582ae85d1fb`  
		Last Modified: Thu, 28 Dec 2023 06:50:41 GMT  
		Size: 2.0 MB (2048024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872b6b82c2e72ebf533c892dfd64f9d694056f2874eb54bb0b7c85d0c2425635`  
		Last Modified: Thu, 28 Dec 2023 06:50:41 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32eb9dfd754ad363d2aecdb96fd7ea5059b8759c7997b92b19177d9bd32afe70`  
		Last Modified: Thu, 28 Dec 2023 06:50:41 GMT  
		Size: 3.4 MB (3418876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1` - unknown; unknown

```console
$ docker pull drupal@sha256:02e7825a46b232f2288894f2e3e7317a8366d7a19277e88deb9835221794c26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5877991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f703feedb56195d013fddfc9a53a287c492544e8c251dbd4cbfa56247aa28d5`

```dockerfile
```

-	Layers:
	-	`sha256:fd20bef8991cdc21e531268a87456b24f0a7ac48cfa6f26b69b8b8755f9a6f89`  
		Last Modified: Thu, 28 Dec 2023 06:50:41 GMT  
		Size: 5.8 MB (5848228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb911f24c4cf37f0482b512b6350315c7d94ccda619fda974c4136e4522c434c`  
		Last Modified: Thu, 28 Dec 2023 06:50:41 GMT  
		Size: 29.8 KB (29763 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1` - linux; mips64le

```console
$ docker pull drupal@sha256:9e68d1da4bd51899aae0fd1b9c9a4a44573d89269da467c98322333993775ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157592278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ac8233a850024c866d8d7d58eb85dea8d94d211e2c8c0c9266d4c25f433163`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Dec 2023 16:27:27 GMT
ADD file:dcd5696ac281b24df52a518e2402c7f7a4caedfcba0d82e195b7c06cd3a38fdd in / 
# Wed, 06 Dec 2023 16:27:27 GMT
CMD ["bash"]
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Dec 2023 16:27:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 06 Dec 2023 16:27:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 06 Dec 2023 16:27:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 06 Dec 2023 16:27:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Dec 2023 16:27:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_VERSION=8.1.27
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 06 Dec 2023 16:27:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Dec 2023 16:27:27 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 06 Dec 2023 16:27:27 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Dec 2023 16:27:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Dec 2023 16:27:27 GMT
STOPSIGNAL SIGWINCH
# Wed, 06 Dec 2023 16:27:27 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 06 Dec 2023 16:27:27 GMT
WORKDIR /var/www/html
# Wed, 06 Dec 2023 16:27:27 GMT
EXPOSE 80
# Wed, 06 Dec 2023 16:27:27 GMT
CMD ["apache2-foreground"]
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Dec 2023 16:27:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Dec 2023 16:27:27 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 06 Dec 2023 16:27:27 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:12b1322ffb17b8e81ca1c6d9d7118e2fcee0b9d971aa3c90601e6345804a60d1`  
		Last Modified: Tue, 19 Dec 2023 02:24:36 GMT  
		Size: 29.1 MB (29121427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff381284c38c37d044a037404bee595ddb632e19af4a73c9058bea92695edbb`  
		Last Modified: Wed, 20 Dec 2023 07:56:19 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edab9ad60196317b7f02dfcef36f9ad767f6874b4de61ca1f73fab286d082fb3`  
		Last Modified: Wed, 20 Dec 2023 07:57:17 GMT  
		Size: 80.7 MB (80667789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3523b846b656b447f978cf98633f848ecc8faf559395c2a42429df15228ef3f`  
		Last Modified: Wed, 20 Dec 2023 07:56:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bd9b49ee2f2c9ffd8c228cc5e88d4b269d7580e1466a8e569d92f72f259a9e`  
		Last Modified: Wed, 20 Dec 2023 07:57:58 GMT  
		Size: 20.1 MB (20053889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b188605258ed68260d81033659d0de0109c45d7a018eb667017a329ec48ebc8`  
		Last Modified: Wed, 20 Dec 2023 07:57:44 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d86fcf97450d81fdfeb49958420896ee40c5d50d6dc6ab326588a3b7ec4f125`  
		Last Modified: Wed, 20 Dec 2023 07:57:43 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea1bdf930db5ef10c30e36c0175eb078d63cd1e5fff1bfd282725d4348807d1`  
		Last Modified: Thu, 28 Dec 2023 04:29:30 GMT  
		Size: 12.0 MB (12041223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf1aa0789fb562c778c0b78811622c5fa4f80039cb17ac2639767c38d464bc9`  
		Last Modified: Thu, 28 Dec 2023 04:29:25 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce1d25faa45e95f013fba3d4a0d6ef89949c99a0314cf2daf5d9609bf318f4e`  
		Last Modified: Thu, 28 Dec 2023 04:29:33 GMT  
		Size: 10.7 MB (10718553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89211ee7aa0ff3c668842e92dffb9e3cd0d8629b05d327d2584cf1933d493945`  
		Last Modified: Thu, 28 Dec 2023 04:29:25 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251c00248b2289745f68e003d4a47aad4f2b12fa987eafad5f14e5dd4164e8d2`  
		Last Modified: Thu, 28 Dec 2023 04:29:25 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743b008ecf8d08ed839b0a3c1ad39aeb51578450a2802559b204187dcbedd778`  
		Last Modified: Thu, 28 Dec 2023 04:29:25 GMT  
		Size: 897.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2537bafb34b9b873801be5667b914fe2be43941bdaaf47ccb8cb4f035e37668a`  
		Last Modified: Thu, 28 Dec 2023 10:16:13 GMT  
		Size: 1.6 MB (1564714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2468052b27d6b087429c9c2c553d456460d63ad101e86271696124c4ac894f87`  
		Last Modified: Thu, 28 Dec 2023 10:16:13 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4721e823b05640cdb5c8fbe4feb821ba2db05f017cdb8f0aab9b42579ecf3029`  
		Last Modified: Thu, 28 Dec 2023 10:16:14 GMT  
		Size: 3.4 MB (3418879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1` - unknown; unknown

```console
$ docker pull drupal@sha256:12499819d59da20203baec736f7765c0307e9aa7690d0da1d05c1b76ba5529dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 KB (29750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2e6323c166cbc5f182142217c305578e9ad438d621d029ae86f57173d7dd75`

```dockerfile
```

-	Layers:
	-	`sha256:83ca6a0a65946ec8a8c499299232c45aa08ecfaace4c41735a131aca26ff905f`  
		Last Modified: Thu, 28 Dec 2023 10:16:10 GMT  
		Size: 29.8 KB (29750 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1` - linux; ppc64le

```console
$ docker pull drupal@sha256:4f91cdce39a111183466ce21adec162deadb432705a5e1c941c84a597b2991e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187553718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62efbb5d13cb5a92a4376d366b5cac43eaa80900435765f87f67c18d9c4dbafd`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Dec 2023 16:27:27 GMT
ADD file:ca1db68689e0b0388337ba450ad2c8e79c159c6b78f5aa6d3ff2b89b8d7edc93 in / 
# Wed, 06 Dec 2023 16:27:27 GMT
CMD ["bash"]
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Dec 2023 16:27:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 06 Dec 2023 16:27:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 06 Dec 2023 16:27:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 06 Dec 2023 16:27:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Dec 2023 16:27:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_VERSION=8.1.27
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 06 Dec 2023 16:27:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Dec 2023 16:27:27 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 06 Dec 2023 16:27:27 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Dec 2023 16:27:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Dec 2023 16:27:27 GMT
STOPSIGNAL SIGWINCH
# Wed, 06 Dec 2023 16:27:27 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 06 Dec 2023 16:27:27 GMT
WORKDIR /var/www/html
# Wed, 06 Dec 2023 16:27:27 GMT
EXPOSE 80
# Wed, 06 Dec 2023 16:27:27 GMT
CMD ["apache2-foreground"]
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Dec 2023 16:27:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Dec 2023 16:27:27 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 06 Dec 2023 16:27:27 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:fc9b8f5eec3aa37ab3aace05165427479352f290d53904cea87dca6349633a09`  
		Last Modified: Tue, 19 Dec 2023 01:26:19 GMT  
		Size: 33.1 MB (33120558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2c39e6db4944508d5e3e708b7b22cdaf778ff9c9719d85d9c759ac4dd574cb`  
		Last Modified: Tue, 19 Dec 2023 10:12:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59183cd2ba3932a3cf6fbac25c2794bfc4ffc7cd8880225207922103ae571620`  
		Last Modified: Tue, 19 Dec 2023 10:12:51 GMT  
		Size: 103.3 MB (103320425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aaf39f49d7e2ae60934f00b5f11cb1f82ba015bf7fde4197881f9a9ca07b75`  
		Last Modified: Tue, 19 Dec 2023 10:12:33 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6239371a8cd761a8e82c2ba70c38ba8bbb48f64800c357ca5dce40bb464f8d`  
		Last Modified: Tue, 19 Dec 2023 10:13:23 GMT  
		Size: 21.5 MB (21489279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ab0c5806bcf9602169aed031ded72c52757eb2c61d6d1e98406e6c011fe84b`  
		Last Modified: Tue, 19 Dec 2023 10:13:20 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2153bb81aa045f8d4106985a468d5c289e2031704b25f0e16b91ca519835f8a`  
		Last Modified: Tue, 19 Dec 2023 10:13:19 GMT  
		Size: 514.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b5672627c5bb9a102adfa4cd0997bf468873e068e7a2ed8920d4d6e9672085`  
		Last Modified: Thu, 28 Dec 2023 01:07:58 GMT  
		Size: 12.2 MB (12247207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e564ac5b8b3ad8fa8ed2e049c9e7236b197dd861feec966ccf4aef4bccbc1c`  
		Last Modified: Thu, 28 Dec 2023 01:07:56 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88cca4ca243f5dc527040f8cecd26142a6722707e257a0bac255d1e6f333844`  
		Last Modified: Thu, 28 Dec 2023 01:07:58 GMT  
		Size: 12.1 MB (12102490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291a78f0ec2a8eeb85c8d8001f815edf2967c2a0ffee22aa68255f2fd41e4d43`  
		Last Modified: Thu, 28 Dec 2023 01:07:56 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9608fa9c7d2365685c72187e30b0f04371baf471fe12dc11c3f0054884eacf`  
		Last Modified: Thu, 28 Dec 2023 01:07:55 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489470ae4a97b367dc5a3e34248d8a4cc21afe870d7da3042d5dd92820c826e4`  
		Last Modified: Thu, 28 Dec 2023 01:07:55 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38cfceb73055223bb82c0189192213920554c2632c6a7b52d4f88edf33f3e56`  
		Last Modified: Thu, 28 Dec 2023 05:48:37 GMT  
		Size: 1.8 MB (1848994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51adf45e3d5c3ef18132b7ee33fd8240986e9fd6156f0ef50bd7f8d8b7ee661b`  
		Last Modified: Thu, 28 Dec 2023 05:48:37 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ade006d2a1440159ed64dde500b0baba15c4b00bb182bd3c60f8693111dc449`  
		Last Modified: Thu, 28 Dec 2023 06:11:58 GMT  
		Size: 3.4 MB (3418875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1` - unknown; unknown

```console
$ docker pull drupal@sha256:7705f01f21a6beb30e6fede6bc8dbb4854b5dfd8ade0b489248c64258fef4a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5875324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec8a7828843606fad3fa18afdb13abb3acbc3e111eddc43a6fec44c2d20e0d6`

```dockerfile
```

-	Layers:
	-	`sha256:0ec0f23a7f3d7dd5fc6076e34f636b3674a7cf15ec65387b6f0ca9a0dbc182fb`  
		Last Modified: Thu, 28 Dec 2023 06:11:58 GMT  
		Size: 5.8 MB (5847507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbaf041b2f2318ec67b75bf07f371c1a5bd58fdc9a6f57198cb8929d1759c8f2`  
		Last Modified: Thu, 28 Dec 2023 06:11:57 GMT  
		Size: 27.8 KB (27817 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1` - linux; s390x

```console
$ docker pull drupal@sha256:d15231d611a6b2e5d789c75570267818900a9197ab69577a3405107d8036f588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156316260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef81e953b13c2ce05a074aca50c5e382ef339129a7ec053e7162efb6bad971c4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Dec 2023 16:27:27 GMT
ADD file:f06f12fa5a93afc3a79ac4371d24b0a471a5a1818cf34c1d90004c8f410914b9 in / 
# Wed, 06 Dec 2023 16:27:27 GMT
CMD ["bash"]
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Dec 2023 16:27:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 06 Dec 2023 16:27:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 06 Dec 2023 16:27:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 06 Dec 2023 16:27:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Dec 2023 16:27:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_VERSION=8.1.27
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 06 Dec 2023 16:27:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Dec 2023 16:27:27 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 06 Dec 2023 16:27:27 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Dec 2023 16:27:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Dec 2023 16:27:27 GMT
STOPSIGNAL SIGWINCH
# Wed, 06 Dec 2023 16:27:27 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 06 Dec 2023 16:27:27 GMT
WORKDIR /var/www/html
# Wed, 06 Dec 2023 16:27:27 GMT
EXPOSE 80
# Wed, 06 Dec 2023 16:27:27 GMT
CMD ["apache2-foreground"]
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Dec 2023 16:27:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Dec 2023 16:27:27 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 06 Dec 2023 16:27:27 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 06 Dec 2023 16:27:27 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:bc6b1888979d3ceb063da848b2034e980e2c2613642159c1e856550b79aa620c`  
		Last Modified: Tue, 19 Dec 2023 01:47:38 GMT  
		Size: 27.5 MB (27491874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9993e12ceea1ed9ab1957e772571c1402e00c56af6350d38cb28b84fab395fe5`  
		Last Modified: Tue, 19 Dec 2023 06:07:47 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdbaa3864255466905f8344dd4efe349cde8c5ca9073a12ae0fbf9825d3204b1`  
		Last Modified: Tue, 19 Dec 2023 06:07:59 GMT  
		Size: 80.8 MB (80814232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f2d7b23522c637c77fedeb3e91c28de912e575dcb61875b074a831136c9a99`  
		Last Modified: Tue, 19 Dec 2023 06:07:47 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67e70d27d6b690ba47e87f1f888675d50761326913207a9e15144bf0b6a8cbf`  
		Last Modified: Tue, 19 Dec 2023 06:08:15 GMT  
		Size: 20.1 MB (20082981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da85699a84ac1f4cce8508e1beb3b2dbc234025fcbafc77062a76426fdfc708e`  
		Last Modified: Tue, 19 Dec 2023 06:08:13 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2663f96dd77fe8464a27af74b2ebaf28c557c094cb1fbdb2770ff36c4d8d0c`  
		Last Modified: Tue, 19 Dec 2023 06:08:13 GMT  
		Size: 517.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566753614f26c0c563bd61c13b1f11fc483c3707e2be0195bc676ae73fd77c66`  
		Last Modified: Wed, 27 Dec 2023 23:46:01 GMT  
		Size: 12.2 MB (12246275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6086e307f856bcd944b382468bc1b6e42bdbcac68abb14d9480efaf187e555`  
		Last Modified: Wed, 27 Dec 2023 23:45:59 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a82dc8ea27ce39bb735144135ea1ff593692302cb9ce4b3352a8714a7c4d8de`  
		Last Modified: Wed, 27 Dec 2023 23:46:01 GMT  
		Size: 10.7 MB (10709555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c74e2562172e73e87d09a12086b011de18043b57d65a3e1bb5e2b4970e3bc64`  
		Last Modified: Wed, 27 Dec 2023 23:45:59 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce960df2e6910bf06108774d9674780418ea380e8b40772b26ea6c83f0c9a8f`  
		Last Modified: Wed, 27 Dec 2023 23:45:59 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5734b48e99ec94946ddd9d927015802bee2071169fc045faa3ab852271309722`  
		Last Modified: Wed, 27 Dec 2023 23:45:59 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d84bd99c2d6fef826ededdb87663902a67e82013b82f38a55ee91884f3974e`  
		Last Modified: Thu, 28 Dec 2023 03:15:20 GMT  
		Size: 1.5 MB (1546579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4860263d11a1df5720a99dbd208467e5e7d8d96616a6102787164fb5cf5a99`  
		Last Modified: Thu, 28 Dec 2023 03:15:20 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10b4a0c83720d746d63665fdeaac52a0fa0414a7fc0c1198b6e9b33d8f79d40`  
		Last Modified: Thu, 28 Dec 2023 03:36:07 GMT  
		Size: 3.4 MB (3418875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1` - unknown; unknown

```console
$ docker pull drupal@sha256:769604d8295dc22d6c41b5b350cc927b2b95609fb13c622a7cc12c63e2af8d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5755357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f2ff0bc596bcf8c051ca0108da879081987fc10721b56fcd4ed50f83e49597`

```dockerfile
```

-	Layers:
	-	`sha256:b2cff1382927909d47839675bb81c0242bcefaeb9b4c6e5711519daeca8613e1`  
		Last Modified: Thu, 28 Dec 2023 03:36:07 GMT  
		Size: 5.7 MB (5727634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:339c29aede7a08d34373df9600ab8714bb61b17041849955b42a87d6b61545e1`  
		Last Modified: Thu, 28 Dec 2023 03:36:07 GMT  
		Size: 27.7 KB (27723 bytes)  
		MIME: application/vnd.in-toto+json
