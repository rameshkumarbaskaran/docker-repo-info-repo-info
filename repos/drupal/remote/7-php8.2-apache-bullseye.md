## `drupal:7-php8.2-apache-bullseye`

```console
$ docker pull drupal@sha256:cc1bc60f5fa4e502b61319eb44efdb8c0e8fe52df5164a4cc48c0d96944b6033
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

### `drupal:7-php8.2-apache-bullseye` - linux; amd64

```console
$ docker pull drupal@sha256:03c8729b12212918c4a2e56657ef24472acb9e04ab20646732946fbd9e64545a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.4 MB (171448674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa429753c008668a504a015c5f9c58505242d0241884cbb11eef92119f8e9fdc`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Dec 2023 16:27:27 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
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
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_VERSION=8.2.13
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.13.tar.xz.asc
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_SHA256=2629bba10117bf78912068a230c68a8fd09b7740267bd8ebd3cfce91515d454b
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
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f2067ef4c9b0c9e0c12ec42bb9725681767c82c63ce30b3d61bdec9dee6734`  
		Last Modified: Tue, 19 Dec 2023 15:39:30 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ba558f2d9945b53d1a0bf19e7bfcfc5df93c00e49e866827238eb35af55634`  
		Last Modified: Tue, 19 Dec 2023 15:39:43 GMT  
		Size: 91.6 MB (91635005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cae92ca9efff667bdfbb8a1c07acb96f3c61dd7206fd8bf6c0c4a4a9a142042`  
		Last Modified: Tue, 19 Dec 2023 15:39:30 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d3fa18b1079e9af1ef4d52703fe69463222016bba36c2863a5a7a219365f56`  
		Last Modified: Tue, 19 Dec 2023 15:40:01 GMT  
		Size: 19.3 MB (19259303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edffd871f270784e52d21898e03189cc4abf2943a2994ebbf651716a02362efe`  
		Last Modified: Tue, 19 Dec 2023 15:39:59 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16be7440aea84e20621bc039eeec3d7ede03c693bf4b018408ae3ac06091dcef`  
		Last Modified: Tue, 19 Dec 2023 15:39:59 GMT  
		Size: 514.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e5f54fea2d5c5e53bc4d1f8ec0ae9e270bcb2e26196f035cf72e5e687e2dda`  
		Last Modified: Tue, 19 Dec 2023 15:48:17 GMT  
		Size: 12.4 MB (12411040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f3fe652ffd5d9c3ff868beea33153ef442a62a051bb44997891a664ce608dd`  
		Last Modified: Tue, 19 Dec 2023 15:48:15 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba724f612c81b50944676e8551af9984798ca14ae04023c947461a71ea5066d`  
		Last Modified: Tue, 19 Dec 2023 15:48:16 GMT  
		Size: 11.4 MB (11372734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9f22ad2b2255c30f8c9df8aeb6c472858124b31ba1e1dcede02e826a999b60`  
		Last Modified: Tue, 19 Dec 2023 15:48:14 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdb6587a5f5e819805cddf73a6c72fad725d3c12173d16babd887dc713aec8d`  
		Last Modified: Tue, 19 Dec 2023 15:48:14 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449b90c243a139624b52e3e587dbb549f5279e519de78f4c06079817fabb3d1a`  
		Last Modified: Tue, 19 Dec 2023 15:48:14 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec9e991d5bc2001f20e92c2f2fe04197906a9e3057aef8ce7637d4179472381`  
		Last Modified: Tue, 19 Dec 2023 17:58:58 GMT  
		Size: 1.9 MB (1927945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad63135715a3adbb7c0d1eb378311f577d4ca3e1e5ba82cc50db75efd8367fa`  
		Last Modified: Tue, 19 Dec 2023 17:58:59 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a4affe7f2caca315739eb10eb217136987cdfc0eadc136838aabd2822437ef`  
		Last Modified: Tue, 19 Dec 2023 17:58:59 GMT  
		Size: 3.4 MB (3418880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:7e3ef04eddbcafc61f8c4cede731635dafa9be61a511ffa6190bf6e4c21e0683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5945282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352e5d86b114d9b5b8bb13b5ef71225f6e95e76832f6b914e96a59b2d7846b28`

```dockerfile
```

-	Layers:
	-	`sha256:0381af24ff5fbdec49de3f394ac49716da681ae445ade7ae472a63b1cc244b17`  
		Last Modified: Tue, 19 Dec 2023 17:58:57 GMT  
		Size: 5.9 MB (5918537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fd323626bae2bcf8fa9d3d38a4a8297071dadedf9798718f6542477d900888c`  
		Last Modified: Tue, 19 Dec 2023 17:58:57 GMT  
		Size: 26.7 KB (26745 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bullseye` - linux; arm variant v5

```console
$ docker pull drupal@sha256:65060be676efd1231453ccb7d98aa05a333df1a97f77d0f78a00c60963f5d10a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148823579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb1b943bb8813fbc262816d4fa20169f2d129ec50f837ab2c4aa1569b8fce70`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Dec 2023 16:27:27 GMT
ADD file:831966ecbc1ad85566dda1f3580cd9306cc099069cd418506e8befd03c296d1c in / 
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
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_VERSION=8.2.13
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.13.tar.xz.asc
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_SHA256=2629bba10117bf78912068a230c68a8fd09b7740267bd8ebd3cfce91515d454b
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
	-	`sha256:fdebea600ba5b47ddd94c41d9d687679a030fdad563a3490945a5433dae01d54`  
		Last Modified: Tue, 19 Dec 2023 01:59:22 GMT  
		Size: 28.9 MB (28921283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd80286abf1a0349dff22a025ce1f8995896cb884c38443684834f7ee53d78a6`  
		Last Modified: Tue, 19 Dec 2023 04:49:27 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4296ee68f6a6d3e5e8b3c49e82b4a6bf047ba2db6746e308f27269d9d012355`  
		Last Modified: Tue, 19 Dec 2023 04:49:41 GMT  
		Size: 73.7 MB (73690328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb68e9d9dc7d1d29014115dacfe87ac57b0e03a99c1d0022ecab600b6b3c0a4`  
		Last Modified: Tue, 19 Dec 2023 04:49:27 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306a0d387905d561734bc6d437f79517197877a460ca909848281e01017ee5de`  
		Last Modified: Tue, 19 Dec 2023 04:50:01 GMT  
		Size: 18.6 MB (18558806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee18df0c891b6f0a9fb57c3e73573cae87b0bef9a1aabadbd5d7b5c717538592`  
		Last Modified: Tue, 19 Dec 2023 04:49:58 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4f88fb381c0c388afeef5382419f930ea5ae20d3f72ed0f5c0c8a7529f2141`  
		Last Modified: Tue, 19 Dec 2023 04:49:57 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284a1370f764f6a5fe99ccd76e25eeda1e59db8f7aafc43f62a1f294f59968ea`  
		Last Modified: Tue, 19 Dec 2023 04:58:10 GMT  
		Size: 12.4 MB (12409443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24bafe6e5bf3e4b727ffee69df589e56f7f50312cb3a91690b25553b535e421`  
		Last Modified: Tue, 19 Dec 2023 04:58:07 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb40db7e7e56d03e7bad88c3cbacccb7b5b6e115790aa541d4d355ee3f7919d`  
		Last Modified: Tue, 19 Dec 2023 04:58:10 GMT  
		Size: 10.4 MB (10399905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b96385679341ceb532c781dc01473cfedc6c5f6a8d5b7697d81cc3eeeaccd8`  
		Last Modified: Tue, 19 Dec 2023 04:58:07 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a352046d44e7d058cc772826fc821d17c0ddbd90353babec927406c7a333e24`  
		Last Modified: Tue, 19 Dec 2023 04:58:07 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3679c857d58d566f3c7aa6f0848abedc39b74c840735c3478e15b689b631d64f`  
		Last Modified: Tue, 19 Dec 2023 04:58:07 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb35984a7811c1f2a5e73c19d44c2a11944094592367dbc3c25fa55a6e299c16`  
		Last Modified: Tue, 19 Dec 2023 19:12:21 GMT  
		Size: 1.4 MB (1419050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5518feeeeff1f82216f910349a7efec0a5e5f884bf903bf45e2277b78065a88d`  
		Last Modified: Tue, 19 Dec 2023 19:12:21 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f59646612b79c5791f6431adede451bd83fabc80d5ba8a690079d27c6c2ef5dd`  
		Last Modified: Tue, 19 Dec 2023 19:12:21 GMT  
		Size: 3.4 MB (3418876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:aba8b1fd5ac1f27e5ade8826ea50a52423a039d957977fde99ab7681e326d1b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7d2fb86ae35ce83f120d169e720b8cc48126ec66057de52346076147571ac1`

```dockerfile
```

-	Layers:
	-	`sha256:f75e4245c9cedc9019f6e5964ad09ffed68db54b2fe2fbcd03af51aa14abc2a0`  
		Last Modified: Tue, 19 Dec 2023 19:12:16 GMT  
		Size: 26.6 KB (26610 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bullseye` - linux; arm variant v7

```console
$ docker pull drupal@sha256:7cb5ba4655db505b4c276c701c7a1b8d110c265b28ed60e2f473e95cadf1a4c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140893076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b34423eef819ed1d70d9055fa437b7d3cb0629e9370836a1d925657bfcf126`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Dec 2023 16:27:27 GMT
ADD file:496e70a34ff4dabb4eefdf40e4e2f0563bea0c120bb43206f8f52ab5a887b637 in / 
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
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_VERSION=8.2.13
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.13.tar.xz.asc
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_SHA256=2629bba10117bf78912068a230c68a8fd09b7740267bd8ebd3cfce91515d454b
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
	-	`sha256:19ccf4d6cc6956e4a5522352be94632923aa376a9939a4f45428a4f304c73bc8`  
		Last Modified: Tue, 19 Dec 2023 02:12:33 GMT  
		Size: 26.6 MB (26578972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57920847d8697c7964a31692261085bf2f2378ae3ecf002e2863475c95222e27`  
		Last Modified: Tue, 19 Dec 2023 07:36:55 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e488984c5928075b5b9dea91064862fa20be8786e9a15c6279b23d7ff93f05`  
		Last Modified: Tue, 19 Dec 2023 07:37:08 GMT  
		Size: 69.3 MB (69322836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e1214fb5d2abafbea1a25bb8db0d422022382b1f6a5ca494d124e9a2a8e596`  
		Last Modified: Tue, 19 Dec 2023 07:36:55 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9432adce1c15ead639c64f24647ce02a16f7228c9dd8f1cd135675d258b28146`  
		Last Modified: Tue, 19 Dec 2023 07:37:26 GMT  
		Size: 18.0 MB (18017808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283f6789f61c24122aea1cbe6e3e1bb61e291d53b89e75d6ba20a18cffc40d4a`  
		Last Modified: Tue, 19 Dec 2023 07:37:22 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d2541e7385efab82a0ed8fe93a53247cf9816b077fa7a116cbc467b8c9985a`  
		Last Modified: Tue, 19 Dec 2023 07:37:22 GMT  
		Size: 512.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24236001587e560166ae3d33201ff4fd2f96aae99019f90bf105bf043a4a8897`  
		Last Modified: Tue, 19 Dec 2023 07:45:53 GMT  
		Size: 12.4 MB (12409371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1dafbbc28e8fbb269ddc4c48ef52c2a4db65d801b961f5f922c0f4b2e7b718`  
		Last Modified: Tue, 19 Dec 2023 07:45:50 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb566ae769820ef5efc1b6c958aeb8265023aad1121a683981b5c9ad19fe0295`  
		Last Modified: Tue, 19 Dec 2023 07:45:52 GMT  
		Size: 9.8 MB (9830047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51c12b6ad14afa3cf07ea405ce7fea649bf59da7fade6c4ff739bd1f3baf2cc`  
		Last Modified: Tue, 19 Dec 2023 07:45:50 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884ba84f0df94c8d2e17c864d9924fc14da9d1d49880fba60c2734fe52f46a10`  
		Last Modified: Tue, 19 Dec 2023 07:45:50 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ac57f92ca49dbec6545e7a1d1855a6395ff0b1541a3b5f20693d3fe88bc680`  
		Last Modified: Tue, 19 Dec 2023 07:45:50 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d627cdd916ae85079120916fffa4f2d6104266aac18952a81c039a7a7c2596b`  
		Last Modified: Wed, 20 Dec 2023 04:05:33 GMT  
		Size: 1.3 MB (1309270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b870b9e05fe7ebd0aeb777bdcd03a385685b583355a46e6a719d32e0fcf3cd`  
		Last Modified: Wed, 20 Dec 2023 04:05:33 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e269b338c983eb87124c7d905726fb024976aaf822675fe3306bff4bc411fbad`  
		Last Modified: Wed, 20 Dec 2023 04:21:58 GMT  
		Size: 3.4 MB (3418876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:bfbeeec93648363b75c47ec0c420d0c57498974e7eb1b4358cff19f3f8a55439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5777702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5ae895e67fc93037ee99794a838cd33e74cc421209b38266f73dee506f7a57`

```dockerfile
```

-	Layers:
	-	`sha256:b5e0d82981a564b38f070b49c1ef1e3bc0cb33aa7f04a31387beb9c9d52ad798`  
		Last Modified: Wed, 20 Dec 2023 04:21:57 GMT  
		Size: 5.8 MB (5752989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc727867e41a3cb0c4eb5cb7d141d4274bd42073dd5f454a04373db3f8e1f540`  
		Last Modified: Wed, 20 Dec 2023 04:21:57 GMT  
		Size: 24.7 KB (24713 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bullseye` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:7362d036cdc0ee62f5de25eee7c37f585e01e3d851a17b397b0ca6ef3e2d4d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165662069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ffb81d0ca696bb6d3f1057f08e436cbc4d0a3e9bfe11962eae3cf6de95fa4cc`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Dec 2023 16:27:27 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
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
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_VERSION=8.2.13
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.13.tar.xz.asc
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_SHA256=2629bba10117bf78912068a230c68a8fd09b7740267bd8ebd3cfce91515d454b
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
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a076a6ccd85e73e29012b8a84aad006e60b307f5df5cca21e9d9bbae5baf5974`  
		Last Modified: Tue, 19 Dec 2023 06:10:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68cc9400cacbe2c77cc31c637154af3be3dcbbf65677d2acd986af40a925f0e`  
		Last Modified: Tue, 19 Dec 2023 06:10:55 GMT  
		Size: 86.9 MB (86934717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279670fefda12a2bab1c29068b63a86160147c69217f64bfe89a84aac931d572`  
		Last Modified: Tue, 19 Dec 2023 06:10:46 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31560e1b11e3f6581d1c50ccded34873858d6efde40c72ca7f2addc31bc1b09c`  
		Last Modified: Tue, 19 Dec 2023 06:11:13 GMT  
		Size: 19.2 MB (19177623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183a34d539323ed02451a3ecc98983f618cfe3a893eccbf995b2da8ee6077e21`  
		Last Modified: Tue, 19 Dec 2023 06:11:10 GMT  
		Size: 470.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744e9735cf6bf3322f39f13f5c14910677042dbd2ef0c8c10fe1f7d14edbe4f7`  
		Last Modified: Tue, 19 Dec 2023 06:11:10 GMT  
		Size: 512.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f7be72ef8213d8e97a9a6cf8d7269767a9a57e4454c9ac814180c9e7edb50f`  
		Last Modified: Tue, 19 Dec 2023 06:19:08 GMT  
		Size: 12.4 MB (12410243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7068bb0f62d2dbf6e6c32505b1c8dcce5a50cf17e3199951b00eb1655ac76635`  
		Last Modified: Tue, 19 Dec 2023 06:19:06 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c27247fa1c1a05f2addf1c242a404b3edabdc26e9ff68f0d3a919c8c6c4628f`  
		Last Modified: Tue, 19 Dec 2023 06:19:07 GMT  
		Size: 11.5 MB (11457826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d579c31f1acf73c2d6ab1e0dc45724b4dc7de1a64c485faa993ec4de3e0c5310`  
		Last Modified: Tue, 19 Dec 2023 06:19:05 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e0ca95bf072a77f4627b76262fbbfbdf7b808dbe4cb5438930b1cb2f258413`  
		Last Modified: Tue, 19 Dec 2023 06:19:05 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e3f6acbaf53ff640e1b7d3f95a29ea554dbb5b33dc7883597a0d5dc242358a`  
		Last Modified: Tue, 19 Dec 2023 06:19:06 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731ee51ef3d25283d0270d30e54f4b0b8f31fccf3872417ed9eb9efe013bbee2`  
		Last Modified: Wed, 20 Dec 2023 04:17:11 GMT  
		Size: 2.2 MB (2192842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053713dd3cf7c78f03c2e062acac1f6b087dbf03aba87ace0fbd32f94a988aa0`  
		Last Modified: Wed, 20 Dec 2023 04:17:11 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f121cd9d3096be96c33c15c21fdc9ab3bc253dfbd603ecba5edfa882201af1`  
		Last Modified: Wed, 20 Dec 2023 04:34:32 GMT  
		Size: 3.4 MB (3418882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:42a9e21f6b8a5f88356989a11609321404e1c969e84ecfcd47a16b22d8fcfdf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5945864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b1cc4022ef23e2a93e50639bfab3752a2838a7b076a3587c30c7163588fa8f`

```dockerfile
```

-	Layers:
	-	`sha256:b8f2d84201c2fae6286a32e23522a4bc7ed007788c60b91db98f3561172f0b63`  
		Last Modified: Wed, 20 Dec 2023 04:34:32 GMT  
		Size: 5.9 MB (5921221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c781f892b633fe596f0e8128b124a4e0bfa87bbc936d60ac4c7a1dff61e526be`  
		Last Modified: Wed, 20 Dec 2023 04:34:31 GMT  
		Size: 24.6 KB (24643 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bullseye` - linux; 386

```console
$ docker pull drupal@sha256:40160d8b6463b4296ed84e5a1542aaa8cc1dcdc4c6425fbbf36e0764fe67f3c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174321043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a10736b605ac856dc49e3d16f8e09c667e9a0b4a5b8e6d923fc8b36ba912fe`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Dec 2023 16:27:27 GMT
ADD file:e9c344f1bffba57e46b30e3c70e4247dcf2e9d3e0484b2768f83ffd789bf3686 in / 
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
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_VERSION=8.2.13
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.13.tar.xz.asc
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_SHA256=2629bba10117bf78912068a230c68a8fd09b7740267bd8ebd3cfce91515d454b
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
	-	`sha256:e5808d881ded1b1deb8675903e6776c5a725d22c8a5c1061a96c74338f07591f`  
		Last Modified: Tue, 19 Dec 2023 01:44:31 GMT  
		Size: 32.4 MB (32402688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39110ba11c8965e66c90db4a166891c890c44c96a8abdf4adc6bc9671fbf63fc`  
		Last Modified: Tue, 19 Dec 2023 21:56:06 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2f8959b86ffec4d26d14f8bcac8c102242de953477eb7372d2ddad03599bb8`  
		Last Modified: Tue, 19 Dec 2023 21:56:27 GMT  
		Size: 92.7 MB (92725759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69416bc6552a7f0a0abdb9113b6b81fa1f0a60b66d43ddfe1af6cf621af62ab4`  
		Last Modified: Tue, 19 Dec 2023 21:56:06 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52439d331c21defc63fce259fa6b3d3c3b41d5bca742ebe90675163c67d0e925`  
		Last Modified: Tue, 19 Dec 2023 21:56:48 GMT  
		Size: 19.7 MB (19745396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fd3944dff0731ac0980ee98a0ade6582011c7ba8dfe9ffe4e3edb8cfd02fff`  
		Last Modified: Tue, 19 Dec 2023 21:56:43 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32172ab49c0481603ea4f62656b951f6a511a4936fd851eadf30f45a6efb497f`  
		Last Modified: Tue, 19 Dec 2023 21:56:43 GMT  
		Size: 513.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824ab8d7423702acf9ef0cd34833ce78ab64292ab5d52a659a8b2441684f31f4`  
		Last Modified: Tue, 19 Dec 2023 22:06:12 GMT  
		Size: 12.4 MB (12410278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e5e8c43fdd70fe48892e23a1a8c6166937f22a2b6fbbcef0f6131c3b43c7e9`  
		Last Modified: Tue, 19 Dec 2023 22:06:08 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26116d34d21ec040079fd62cc110d7bbdd8fca1170b748b46c079f5705ddb00`  
		Last Modified: Tue, 19 Dec 2023 22:06:12 GMT  
		Size: 11.6 MB (11617326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a24f0f42ac385cd31f9b001a7533de15cce4d197e4e061fd602726120243d88`  
		Last Modified: Tue, 19 Dec 2023 22:06:08 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cbf1cdfa3ba472a0fa5e45e0c71ec99cbf8542cfd03caf0798477b55ede009`  
		Last Modified: Tue, 19 Dec 2023 22:06:08 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e54d21fa3465b2b0274dc18219d363169372298da7d315f849497ef9db940b`  
		Last Modified: Tue, 19 Dec 2023 22:06:08 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4990f21f32b7e6ed0f930ccba1d5cb3ae3499663cc18c654a1e679386a7f558`  
		Last Modified: Tue, 19 Dec 2023 22:52:18 GMT  
		Size: 2.0 MB (1994831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef94d028f501231ecd39c66cccea0f8ea5fe70ef2fadaed6b0e8c3da426ef5e9`  
		Last Modified: Tue, 19 Dec 2023 22:52:18 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e615054bcb1a0fb6cd22fffaa47231f7e6a191e759f8005cf0d96db10a89421`  
		Last Modified: Tue, 19 Dec 2023 22:52:18 GMT  
		Size: 3.4 MB (3418876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:8a3351c77ef4c00bb44d62b61b9ee8c19cf10ed7af39cda8a68c36930a7cfd40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4733cdbc3c187c7cfbc012bc481f035fecc682eb737135255a8332144895f6d3`

```dockerfile
```

-	Layers:
	-	`sha256:7c93799f7d360e2faadeb83c144b77ec863d9754c29f4c830afa296635fbf859`  
		Last Modified: Tue, 19 Dec 2023 22:52:17 GMT  
		Size: 26.5 KB (26507 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bullseye` - linux; mips64le

```console
$ docker pull drupal@sha256:1c73f7825f47b906eb25b092f409ef703ec5ab0abae655a55b5261adab1ab2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (148042522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd95ae88f0e103c6b04639f212b5f78c4c9f78ed7887fb30d9941dcd41632ae`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Dec 2023 16:27:27 GMT
ADD file:dcc77071aa6c677714230fd845d154c00ba6ba34a78f8f1073c224e90f17f543 in / 
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
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_VERSION=8.2.13
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.13.tar.xz.asc
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_SHA256=2629bba10117bf78912068a230c68a8fd09b7740267bd8ebd3cfce91515d454b
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
	-	`sha256:f9454980ac665cb2d7641130c738c2054ef7a7516386fc6742b46b5b60dd93ad`  
		Last Modified: Tue, 19 Dec 2023 02:26:03 GMT  
		Size: 29.6 MB (29635982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45840e3413dae74e526f55ddcdf1db42b53ccbb27b4fb21e419a5582ca09dd18`  
		Last Modified: Wed, 20 Dec 2023 07:59:21 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c95c6a802f4dd492ceb4c3eb8e35309d5c95d19cfdb86049d0c9d4882e9b422`  
		Last Modified: Wed, 20 Dec 2023 08:00:12 GMT  
		Size: 71.8 MB (71814805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbc65667ba3423adf4d9419c0ac5e16231796095992eeb158a0bd7eeb0f9100`  
		Last Modified: Wed, 20 Dec 2023 07:59:21 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0988471404e7b79e5ca0dccdbcd416721580ca03a482965ad9f3bc7c6b2f3a11`  
		Last Modified: Wed, 20 Dec 2023 08:00:45 GMT  
		Size: 19.0 MB (18955521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412588df7fc65c5d34a004c66ac9ab05cb03df9c7ef350aaf02bc3e74163414e`  
		Last Modified: Wed, 20 Dec 2023 08:00:32 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b74fc8807170af201647665c2079bb8ca6bb4449a1941cc5838028a2c7e4cd9`  
		Last Modified: Wed, 20 Dec 2023 08:00:32 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9037e8aa485822050f6d52995e4c3cb8e5fffb80ebac58390b53f5696c4bdee9`  
		Last Modified: Wed, 20 Dec 2023 08:14:08 GMT  
		Size: 12.2 MB (12191847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa1c5759070e845cef07958c2b5d909c0f8683e4c779050f3b4ce1c2a9cc2d6`  
		Last Modified: Wed, 20 Dec 2023 08:14:02 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4219ab4e4497239c336d1b8b4dc866b439b2969e447643c1e3c114b7cdd6cdc3`  
		Last Modified: Wed, 20 Dec 2023 08:14:11 GMT  
		Size: 10.5 MB (10501961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff5503663ed6e6559e5a983807c22995f4819c89384cc7abc3407ed9e06f4b8`  
		Last Modified: Wed, 20 Dec 2023 08:14:02 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b9cf1a15309c054eac8a02fecbbcf3d1abf6d5e65fdca3f55d401b47751bbe`  
		Last Modified: Wed, 20 Dec 2023 08:14:03 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94603ee91f57a85de8a55591b035dc0cd6b4b327487937e20af34da027ee5ed`  
		Last Modified: Wed, 20 Dec 2023 08:14:02 GMT  
		Size: 897.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f435ede7d7372cd9025cdff2afa00f4bb13b407f5e49a60dad5e6aaf2ff2dc`  
		Last Modified: Thu, 21 Dec 2023 14:05:51 GMT  
		Size: 1.5 MB (1517729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5afcaae9a8b79bf449e7dd8dc385170b720f3938fdfb4450296c8f3425544da`  
		Last Modified: Thu, 21 Dec 2023 14:05:50 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d827fde029ddc87d40bc1293da1e871e2a5063e6da7105c714cad178d12c247`  
		Last Modified: Thu, 21 Dec 2023 14:05:51 GMT  
		Size: 3.4 MB (3418879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:e16bc1be49e95dfd4854903bab32b104083aba29861885203683eac132541661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76eab8fe19ae695ac865438d20135a2253a96f1608bf006bbe03a09b7ee3e86e`

```dockerfile
```

-	Layers:
	-	`sha256:16430e73f7f7cf1be2ecaf367c3b36422fd4d91cadb9d11f274744aa346c8fa6`  
		Last Modified: Thu, 21 Dec 2023 14:05:45 GMT  
		Size: 26.6 KB (26575 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bullseye` - linux; ppc64le

```console
$ docker pull drupal@sha256:f3a1f228ab30c87d70207f366889ebfdbd34bb9b6d4f72cba7a9a116ff625e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171881060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c479b3797ac29ebd10906fc3350dd008b9a2b20753c8bb11c5a677721202456`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Dec 2023 16:27:27 GMT
ADD file:1cb772a6ad8ca6301624db3141029490564de7673bc0f2d4bedb5a1578ea85bd in / 
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
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_VERSION=8.2.13
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.13.tar.xz.asc
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_SHA256=2629bba10117bf78912068a230c68a8fd09b7740267bd8ebd3cfce91515d454b
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
	-	`sha256:c9f6fac7f65cfc65b7f8de8bc377b135ca95e45a3246cf2bd1bb90922679553e`  
		Last Modified: Tue, 19 Dec 2023 01:27:11 GMT  
		Size: 35.3 MB (35293807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20cf519da704a54ecd293555ffdb5378583eb2868a1e6446dc247a6886dc999`  
		Last Modified: Tue, 19 Dec 2023 10:14:20 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc74cb39269dd60ed201199e7c64cdcbb45ec85b53ac6c23f0e2e855b7ef3f7`  
		Last Modified: Tue, 19 Dec 2023 10:14:34 GMT  
		Size: 86.6 MB (86643602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc627fce51a8d94e83865a3eb6e70a4ce8ac2181ec3fc10971f18a787e5ce54`  
		Last Modified: Tue, 19 Dec 2023 10:14:19 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c42f6a95847156c943dba72d6ebc40b38cd196ed9cf5f98b41bf52926d6c38`  
		Last Modified: Tue, 19 Dec 2023 10:14:54 GMT  
		Size: 20.5 MB (20475053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3da9552fb9610e58d2bf689e0a683d93c7f80ae866f7173bf3cb915fb95501`  
		Last Modified: Tue, 19 Dec 2023 10:14:51 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6cadde5371b7a4a4227c0209d45bf6e9a2996b7324d1606a19fc7a8030ee35c`  
		Last Modified: Tue, 19 Dec 2023 10:14:51 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0076f43fc048b99657dee2633f696adf0ea140542dc3cd58a5f5f1672b5a8bda`  
		Last Modified: Tue, 19 Dec 2023 10:24:05 GMT  
		Size: 12.4 MB (12411071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8f234c16b40f321c84c1498f0056e600435c282ebf256c32a9916e404af2ac`  
		Last Modified: Tue, 19 Dec 2023 10:24:02 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6b5398e621b351fd0aad1dc88eb4880a9d2d136641d559e5ad924a9b1f31d7`  
		Last Modified: Tue, 19 Dec 2023 10:24:04 GMT  
		Size: 11.8 MB (11837980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de77ba8e68f5eb136fc896761264347494bb75e5c7987a1556e1c4ed2eb4e53`  
		Last Modified: Tue, 19 Dec 2023 10:24:02 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbe6612eb7207a723d7bf1d6c424026a0c2260f2b52685d7acec3f9cddf888f`  
		Last Modified: Tue, 19 Dec 2023 10:24:02 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18fbd2dd70c8208e30dba16f69410d3ba7fc68e9fef89145a20a2b5e5618974`  
		Last Modified: Tue, 19 Dec 2023 10:24:02 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea7472e0531ee3a5f347d9eeb261af0c8e9e95f22f709f5478986234f59a4c7`  
		Last Modified: Wed, 20 Dec 2023 02:26:00 GMT  
		Size: 1.8 MB (1794771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417649c6da5d72b6f048a9604b728829bcf3ceeb0f80bb7128650bbe2d0a61d5`  
		Last Modified: Wed, 20 Dec 2023 02:26:00 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ab7e07fe28b36b4c22b2d7f458d0a8ff59b2affe1edb09dd3f2ba538c45a29`  
		Last Modified: Wed, 20 Dec 2023 02:59:32 GMT  
		Size: 3.4 MB (3418879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:9f659c7c6b007ed1441535148cfa13e0875baed3ef69ddfb95f184026ccb80cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5915069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf6103f2b14811b87539fa1e83c070066cf3b59fa4456ea9846435938c05416`

```dockerfile
```

-	Layers:
	-	`sha256:19db759595e2756f89edd4c70187cec66dff527f7fe897dad6d3e6ea709fc0dd`  
		Last Modified: Wed, 20 Dec 2023 02:59:32 GMT  
		Size: 5.9 MB (5890402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:054649bee4a128ff383157412e5fe78d7c23dbcbccba29ff065323357daaa914`  
		Last Modified: Wed, 20 Dec 2023 02:59:31 GMT  
		Size: 24.7 KB (24667 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bullseye` - linux; s390x

```console
$ docker pull drupal@sha256:97e0df7a6830f05810573076a020faaece0b8d2dc8ae18f5f54418f524a69dac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.2 MB (148219744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a9127237059bad73e719bb8f30bd6bcb618ccbb26ceb6228efa47769c553cd`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Dec 2023 16:27:27 GMT
ADD file:36a070457acddafcd6cdda22a3c41efcbd4e2b1694831eb74c8143520ebf1cf2 in / 
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
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_VERSION=8.2.13
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.13.tar.xz.asc
# Wed, 06 Dec 2023 16:27:27 GMT
ENV PHP_SHA256=2629bba10117bf78912068a230c68a8fd09b7740267bd8ebd3cfce91515d454b
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
	-	`sha256:eff2a4367cf88d5103011eba9299da2b4d173b0bde5dc0455020febf72b9b1c4`  
		Last Modified: Tue, 19 Dec 2023 01:48:08 GMT  
		Size: 29.7 MB (29657006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b09eb72e9d386dbf4dcb97b2cd8fb6c959008740372463872bcbb989f9b553`  
		Last Modified: Tue, 19 Dec 2023 06:08:48 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd379a47c6b90f49f4156c7ff2dd2eb18fe68c359cee32fa1f2d5786d853a7e`  
		Last Modified: Tue, 19 Dec 2023 06:08:59 GMT  
		Size: 71.6 MB (71634732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8169479b1d74c4fef21b4c3c845f26c586316508cfb384643eddfd5325797a1`  
		Last Modified: Tue, 19 Dec 2023 06:08:48 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ce7e9939543e6a9f444169e00e0128eef4c91089741b274c4a2b114d8cc176`  
		Last Modified: Tue, 19 Dec 2023 06:09:17 GMT  
		Size: 19.1 MB (19080627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813124d6d9df2062098e9401e27319aaa883fa6976985b1c1c3ab72e9f50e6aa`  
		Last Modified: Tue, 19 Dec 2023 06:09:14 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597ef00b179cc766c8a38ac1743e18947bbd8b665e5121c147c0f344096f444e`  
		Last Modified: Tue, 19 Dec 2023 06:09:13 GMT  
		Size: 514.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92625a21a728b0ab08e83d2f0bb36ae7660f2ec9db44bcaf3595e9fc17ab3e1b`  
		Last Modified: Tue, 19 Dec 2023 06:15:10 GMT  
		Size: 12.4 MB (12409904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5d7207e107c8a31eba7ed428a35ecc308220734d71d96e9b1f8f0e49c4c632`  
		Last Modified: Tue, 19 Dec 2023 06:15:09 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ea4a0f1b9fee39f2bf7fb489c7c0d7a0b6cffc3efbb93bcb6108bfb23adf53`  
		Last Modified: Tue, 19 Dec 2023 06:15:11 GMT  
		Size: 10.5 MB (10490482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ccfc20b354c46643374339375cbe695f0d3185abed0dc494cf04a72eb73d8b`  
		Last Modified: Tue, 19 Dec 2023 06:15:09 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed010de85b181be2be473062f233c31ca68fadc67421797b11da349a8d03527`  
		Last Modified: Tue, 19 Dec 2023 06:15:08 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a995921b0b03045ab5485bbcf51c75b4b61fe42140606b8413077eb4f2320a2`  
		Last Modified: Tue, 19 Dec 2023 06:15:09 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1381e442a602cdbbb0faea48ae9c8b8fe06fb15147dbc14f20ec9388964728c`  
		Last Modified: Tue, 19 Dec 2023 16:07:13 GMT  
		Size: 1.5 MB (1522228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105e809dd969961d94587e5d30a34ce234dc561908148ae28bf165c37f760ea3`  
		Last Modified: Tue, 19 Dec 2023 16:07:13 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca234363abc3c18f513728e6e9be7dcbc2824e05adb4bade44aa947830214341`  
		Last Modified: Tue, 19 Dec 2023 16:24:55 GMT  
		Size: 3.4 MB (3418875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:0f37e5d556991ff273da2c628c67dee4bc505e9d4625e0bf0ae12b7aa67c81a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5795297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7276f620b8cc3bb17de1375154202290f3950211b57ede73c114f507e366ee77`

```dockerfile
```

-	Layers:
	-	`sha256:73c26af4b142864b0b0b9c6e7be110111822c9c9efad1ece5db94da71b900990`  
		Last Modified: Tue, 19 Dec 2023 16:24:54 GMT  
		Size: 5.8 MB (5770660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e871ca8c6e83e7a856054ed9d9b95d334c3f613f8b17708b1df2cd817c06f06`  
		Last Modified: Tue, 19 Dec 2023 16:24:55 GMT  
		Size: 24.6 KB (24637 bytes)  
		MIME: application/vnd.in-toto+json
