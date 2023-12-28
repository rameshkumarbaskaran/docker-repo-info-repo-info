## `drupal:apache-bullseye`

```console
$ docker pull drupal@sha256:25f9822b5f66c8cafb5012d7762b8f13c014591dff20f1ea5dae30802324de87
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

### `drupal:apache-bullseye` - linux; amd64

```console
$ docker pull drupal@sha256:3b4d54e8f7828bb614870fddc819afb29c4ea91cbc73e787195b42e008630c1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187747723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4adc2d179149395b0c305acc71a8a74baba4e10d959be1215f682aed9c298fa0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Dec 2023 10:27:26 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Wed, 06 Dec 2023 10:27:26 GMT
CMD ["bash"]
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Dec 2023 10:27:26 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 06 Dec 2023 10:27:26 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 06 Dec 2023 10:27:26 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 06 Dec 2023 10:27:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Dec 2023 10:27:26 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_VERSION=8.2.14
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.14.tar.xz.asc
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_SHA256=763ecd39fcf51c3815af6ef6e43fa9aa0d0bd8e5a615009e5f4780c92705f583
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 06 Dec 2023 10:27:26 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Dec 2023 10:27:26 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 06 Dec 2023 10:27:26 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Dec 2023 10:27:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Dec 2023 10:27:26 GMT
STOPSIGNAL SIGWINCH
# Wed, 06 Dec 2023 10:27:26 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 06 Dec 2023 10:27:26 GMT
WORKDIR /var/www/html
# Wed, 06 Dec 2023 10:27:26 GMT
EXPOSE 80
# Wed, 06 Dec 2023 10:27:26 GMT
CMD ["apache2-foreground"]
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Dec 2023 10:27:26 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Dec 2023 10:27:26 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 06 Dec 2023 10:27:26 GMT
ENV DRUPAL_VERSION=10.1.7
# Wed, 06 Dec 2023 10:27:26 GMT
WORKDIR /opt/drupal
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
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
	-	`sha256:1dd00a6221fd445c43abc93137728c9ff85c85c97d40011e05bfbad0b5380506`  
		Last Modified: Thu, 28 Dec 2023 01:20:53 GMT  
		Size: 12.4 MB (12423141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937e99ae69966f3f887cfafae48f48e722b93d39a6f4893d54bc996a23258dcf`  
		Last Modified: Thu, 28 Dec 2023 01:20:50 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91f768b096f5926471f1089c78493b29445dbe502debdbdd3021675d7923073`  
		Last Modified: Thu, 28 Dec 2023 01:20:52 GMT  
		Size: 11.8 MB (11816671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b445f4e53850a2128eb6ccccd492be46571e00df95233740f44b60b1af73b542`  
		Last Modified: Thu, 28 Dec 2023 01:20:50 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9755abc57f5a99d5cf39b016e7f9689867a8e30bf8026e91037ed33d23d05c31`  
		Last Modified: Thu, 28 Dec 2023 01:20:50 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fded1b38dd56ab2b2055d55beaa1ba268dbece475fd397172db3414f27013378`  
		Last Modified: Thu, 28 Dec 2023 01:20:50 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef96e3a3091a07298140108da4a4e28190e0d778a94cc1efd8e5cf408af4968`  
		Last Modified: Thu, 28 Dec 2023 06:49:11 GMT  
		Size: 1.9 MB (1928163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59046334752e4d7429a9e5f0d5ee480debd4bbbcd8e6f896a1689ce83bf5e6b7`  
		Last Modified: Thu, 28 Dec 2023 06:49:11 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ace081b55d66d3fd9a238dd3552f8ca4bc5f9402d33b2eb036bc734054234f`  
		Last Modified: Thu, 28 Dec 2023 06:49:11 GMT  
		Size: 705.2 KB (705211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8832200a8672c19dfb8c9cd04f6d7f4a20f7980318b6a4d979e9a58b9b9121`  
		Last Modified: Thu, 28 Dec 2023 06:49:11 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6904234c019fce6ae9cffde33d9edb737d2208edadc3cf1b90ff76923c155e`  
		Last Modified: Thu, 28 Dec 2023 06:49:13 GMT  
		Size: 18.6 MB (18556354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:a8df4ecbc0f00c795214909351ad114d69591a11bdcaa0a6291cbf94f8f71539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6007421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55934a510ce706c8f5993c8591a0a201544e78b330c757c6ff1773123f16de41`

```dockerfile
```

-	Layers:
	-	`sha256:98e10f30edec71088ab2b2f5380ecb053a7f8704add7fdfd6cbf21369954314e`  
		Last Modified: Thu, 28 Dec 2023 06:49:11 GMT  
		Size: 6.0 MB (5966748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a124646f16d0ec86eddbe05c2244f2cfaa8b1f1ba900ca234de7cbf73d995a9`  
		Last Modified: Thu, 28 Dec 2023 06:49:11 GMT  
		Size: 40.7 KB (40673 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache-bullseye` - linux; arm variant v7

```console
$ docker pull drupal@sha256:9393758bfe5e5ba85cb5b872b5a00c7cca54386f9b160ffc4aeeb97491a5e7a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157139654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe31e3dc5e79c4ef10086145ebdca692396b17479c4307aa8fa9472f70d4d80`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Dec 2023 10:27:26 GMT
ADD file:496e70a34ff4dabb4eefdf40e4e2f0563bea0c120bb43206f8f52ab5a887b637 in / 
# Wed, 06 Dec 2023 10:27:26 GMT
CMD ["bash"]
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Dec 2023 10:27:26 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 06 Dec 2023 10:27:26 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 06 Dec 2023 10:27:26 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 06 Dec 2023 10:27:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Dec 2023 10:27:26 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_VERSION=8.2.14
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.14.tar.xz.asc
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_SHA256=763ecd39fcf51c3815af6ef6e43fa9aa0d0bd8e5a615009e5f4780c92705f583
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 06 Dec 2023 10:27:26 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Dec 2023 10:27:26 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 06 Dec 2023 10:27:26 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Dec 2023 10:27:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Dec 2023 10:27:26 GMT
STOPSIGNAL SIGWINCH
# Wed, 06 Dec 2023 10:27:26 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 06 Dec 2023 10:27:26 GMT
WORKDIR /var/www/html
# Wed, 06 Dec 2023 10:27:26 GMT
EXPOSE 80
# Wed, 06 Dec 2023 10:27:26 GMT
CMD ["apache2-foreground"]
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Dec 2023 10:27:26 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Dec 2023 10:27:26 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 06 Dec 2023 10:27:26 GMT
ENV DRUPAL_VERSION=10.1.7
# Wed, 06 Dec 2023 10:27:26 GMT
WORKDIR /opt/drupal
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
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
	-	`sha256:365b20de24de945a768f9bdf8da51f3b13f6e64577147bf8fa5bec4d4034c5ff`  
		Last Modified: Thu, 28 Dec 2023 02:53:13 GMT  
		Size: 12.4 MB (12421589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4ac820f29daed4505abd97e03f45bb6cb5a7b3acb81da5a602869879333c90`  
		Last Modified: Thu, 28 Dec 2023 02:53:10 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6644845b17bead54a0f228d686fbe441e864de68cd9015f7a315d10f6956f890`  
		Last Modified: Thu, 28 Dec 2023 02:53:13 GMT  
		Size: 10.2 MB (10221252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab484290c5d1326096e4e63ed2d90c55fe33c067c62c7c2ba87ea94bdf4742c`  
		Last Modified: Thu, 28 Dec 2023 02:53:10 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950c7f29adf82798da94e2d80dcaa345ae4fb0555ac4c32b44de25a06294fcbe`  
		Last Modified: Thu, 28 Dec 2023 02:53:10 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fe812a8604090cd0285467d35d931ddae14a1bcd56d34127f0b9758edf61f8`  
		Last Modified: Thu, 28 Dec 2023 02:53:10 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cde5d491aae5be2149f64b57bf571cfcf53e7a028bea164eac02cf5bac7bcea`  
		Last Modified: Thu, 28 Dec 2023 08:35:16 GMT  
		Size: 1.3 MB (1309467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7523268d7a36ebdd9c3e904be999ff4db7651cecb38595fa1f743da53210ad25`  
		Last Modified: Thu, 28 Dec 2023 08:35:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2149d39a2660d02c025b4a8999d07a289bfc1bb26def2935f58be37ecbbcae`  
		Last Modified: Thu, 28 Dec 2023 08:35:17 GMT  
		Size: 705.2 KB (705211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40720c5930a428e72508537940be8c4b84ebd65f81a43d02741ca3619a91802`  
		Last Modified: Thu, 28 Dec 2023 08:35:16 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc3b21d41c4782cae023ffb60bdabac3c72025629b1a24e5e7e1f5599558c2d`  
		Last Modified: Thu, 28 Dec 2023 08:45:53 GMT  
		Size: 18.6 MB (18556507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:e950867197ab3d3d10fe2aa73266114119b6668fe427e37a205dee8a9e3ce474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5837684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae88a2da76bc2f1bdf43cd335b38f735143ef4fc679a44f80f5063dc0244c92`

```dockerfile
```

-	Layers:
	-	`sha256:7b3b6a9b40e94fb282206db7a0f55e7d82bdd3dd0446ea218750fdabba7b4345`  
		Last Modified: Thu, 28 Dec 2023 08:45:52 GMT  
		Size: 5.8 MB (5801248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17954f405e3a14c49ac203a0f91b624d8505855683992559720fe4f89fde15a1`  
		Last Modified: Thu, 28 Dec 2023 08:45:51 GMT  
		Size: 36.4 KB (36436 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache-bullseye` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:bd6d633fa1ea123ed9c02f38ad13ffa6229e4acf0c5066665d30cb91fd9af410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (181960076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590ac1e424ec6beaf6045c1d8360b6609e4987e98d59cabb3953679ebdd4c20e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Dec 2023 10:27:26 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Wed, 06 Dec 2023 10:27:26 GMT
CMD ["bash"]
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Dec 2023 10:27:26 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 06 Dec 2023 10:27:26 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 06 Dec 2023 10:27:26 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 06 Dec 2023 10:27:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Dec 2023 10:27:26 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_VERSION=8.2.14
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.14.tar.xz.asc
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_SHA256=763ecd39fcf51c3815af6ef6e43fa9aa0d0bd8e5a615009e5f4780c92705f583
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 06 Dec 2023 10:27:26 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Dec 2023 10:27:26 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 06 Dec 2023 10:27:26 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Dec 2023 10:27:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Dec 2023 10:27:26 GMT
STOPSIGNAL SIGWINCH
# Wed, 06 Dec 2023 10:27:26 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 06 Dec 2023 10:27:26 GMT
WORKDIR /var/www/html
# Wed, 06 Dec 2023 10:27:26 GMT
EXPOSE 80
# Wed, 06 Dec 2023 10:27:26 GMT
CMD ["apache2-foreground"]
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Dec 2023 10:27:26 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Dec 2023 10:27:26 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 06 Dec 2023 10:27:26 GMT
ENV DRUPAL_VERSION=10.1.7
# Wed, 06 Dec 2023 10:27:26 GMT
WORKDIR /opt/drupal
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
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
	-	`sha256:6072994e6724058fda7e00728f371f5ad669f287f751dbdfc768440a931ba5c8`  
		Last Modified: Thu, 28 Dec 2023 00:36:59 GMT  
		Size: 12.4 MB (12422392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9c91ed38d280a35db5b77e6709ff6998eb32d859cdb1941625fa113d22bd84`  
		Last Modified: Thu, 28 Dec 2023 00:36:56 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115faf5dfc6f63bd1afb311f7967454771efd21761bd7db5494feebf5cdfac1b`  
		Last Modified: Thu, 28 Dec 2023 00:36:58 GMT  
		Size: 11.9 MB (11899873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9553513b49fc9f15ad6ec4a0964f41b825050e943047c724f8223b042dabdbe2`  
		Last Modified: Thu, 28 Dec 2023 00:36:56 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c065dc0b64679669b63f9c1d01aab9e10d1a8ab09dd1256c376f613b82f35e`  
		Last Modified: Thu, 28 Dec 2023 00:36:56 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db0ea7333421586ffea2a1ef6c7e51f500fb6a122c16fdde82cd6a8174a577b`  
		Last Modified: Thu, 28 Dec 2023 00:36:56 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd789b386bd9baf1df696e9806943c9fb67961e57cd327ab9cdc69b2d166ce3`  
		Last Modified: Thu, 28 Dec 2023 05:35:42 GMT  
		Size: 2.2 MB (2193824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd97e0047f517f3af4c404bfc18b35b9ea8e983b6fc496f1ab8314459257dde`  
		Last Modified: Thu, 28 Dec 2023 05:35:42 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1df6e3ae74f898ba1af390ae8e767911f51551e4494c7230ce4f9bc6d047bd`  
		Last Modified: Thu, 28 Dec 2023 05:35:42 GMT  
		Size: 705.2 KB (705213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7581e44d84c862a1a7a9160e823d6d012d3f93c13e5d04ce2b07882b475e312c`  
		Last Modified: Thu, 28 Dec 2023 05:35:43 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76c6b85e14fb89e416c286b5b1b82af447434a9ec413c8739ec810acabfd803`  
		Last Modified: Thu, 28 Dec 2023 05:53:46 GMT  
		Size: 18.6 MB (18556387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:8e47ef20cc6d1993f4f066daf89fdf2d85c58d8ce22c1945d1db59dc14e3d601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6005755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7274f5e50beca43fd4ea6e87e6a12f59169f7e01dfd11a97f0b80d27d8c0c28`

```dockerfile
```

-	Layers:
	-	`sha256:8c5543487fcea03977b75e9f365cb26657e964b27002450a206ad8cc56b07745`  
		Last Modified: Thu, 28 Dec 2023 07:23:22 GMT  
		Size: 6.0 MB (5969444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48e0c668c40e4b09d4045567e5ffd2d21accca9790fb17edad95db6de58b7f15`  
		Last Modified: Thu, 28 Dec 2023 07:23:22 GMT  
		Size: 36.3 KB (36311 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache-bullseye` - linux; 386

```console
$ docker pull drupal@sha256:e003c6678292a562751e6a83833187ae99e85c9253d45c305ebfa5347ffa70b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.7 MB (190666903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e50a1f4f3994f9e305ae0880644364fd75df8e8883fad911e5a4f63e94ae88`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Dec 2023 10:27:26 GMT
ADD file:e9c344f1bffba57e46b30e3c70e4247dcf2e9d3e0484b2768f83ffd789bf3686 in / 
# Wed, 06 Dec 2023 10:27:26 GMT
CMD ["bash"]
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Dec 2023 10:27:26 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 06 Dec 2023 10:27:26 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 06 Dec 2023 10:27:26 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 06 Dec 2023 10:27:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Dec 2023 10:27:26 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_VERSION=8.2.14
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.14.tar.xz.asc
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_SHA256=763ecd39fcf51c3815af6ef6e43fa9aa0d0bd8e5a615009e5f4780c92705f583
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 06 Dec 2023 10:27:26 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Dec 2023 10:27:26 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 06 Dec 2023 10:27:26 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Dec 2023 10:27:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Dec 2023 10:27:26 GMT
STOPSIGNAL SIGWINCH
# Wed, 06 Dec 2023 10:27:26 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 06 Dec 2023 10:27:26 GMT
WORKDIR /var/www/html
# Wed, 06 Dec 2023 10:27:26 GMT
EXPOSE 80
# Wed, 06 Dec 2023 10:27:26 GMT
CMD ["apache2-foreground"]
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Dec 2023 10:27:26 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Dec 2023 10:27:26 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 06 Dec 2023 10:27:26 GMT
ENV DRUPAL_VERSION=10.1.7
# Wed, 06 Dec 2023 10:27:26 GMT
WORKDIR /opt/drupal
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
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
	-	`sha256:a22ef8de7cf08a07e31f10639ee3af58e2c43f229e792dc8a0562f25f8725991`  
		Last Modified: Thu, 28 Dec 2023 02:21:07 GMT  
		Size: 12.4 MB (12422432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce1f41386ae4bb4d81cf9aae2b051ef4b0e278ab75f036a22e2cd88724bcadd`  
		Last Modified: Thu, 28 Dec 2023 02:21:03 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af25b1df0b48cf49d2394333d8b9a5fb6129342a89e605736013b4658d5ff3fa`  
		Last Modified: Thu, 28 Dec 2023 02:21:07 GMT  
		Size: 12.1 MB (12107051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff95d8ada831f1ee189a45445b827973d120d3321e982cc4d6799decd41890e`  
		Last Modified: Thu, 28 Dec 2023 02:21:04 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77168e9254a6ec522fb6b4a1a05f81bdcfc997fdd2e52a4be82f745ad08a047`  
		Last Modified: Thu, 28 Dec 2023 02:21:03 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb6075db1521678dfaafbe596f87c4ace87a7d61e83c67139e4ca7c088b1f5b`  
		Last Modified: Thu, 28 Dec 2023 02:21:03 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d04f15cf26eb0ab3b624e4a734bc625dd4e296c80d5f55926d40f3c330daec2`  
		Last Modified: Thu, 28 Dec 2023 06:49:21 GMT  
		Size: 2.0 MB (1996041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75fd84c15bac5cbdacd7034bbbcffbadcc07e77018570ec9e0afd151f8c5277`  
		Last Modified: Thu, 28 Dec 2023 06:49:21 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f3ba35463a9576999d0d162d858bace53dce2f0ebb4e88ba8e9c93d10e78e8`  
		Last Modified: Thu, 28 Dec 2023 06:49:21 GMT  
		Size: 705.2 KB (705212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60410f39e17c90464322e83d89df418998255e9ef2d2baacbcd87e859d10e7a`  
		Last Modified: Thu, 28 Dec 2023 06:49:17 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1517c923a0fdd46080c62d6cf0e51898910e0bf243a9ac81050b1b450d633b12`  
		Last Modified: Thu, 28 Dec 2023 06:49:22 GMT  
		Size: 18.6 MB (18556310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:f55046af09cce19352e69af36cd427fc35cafb8eef733324a8a9f42e9a5ad92b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5998449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7206b7695eea2739b812af2aa282beaa3f79d87b2fa4d550e381efca2e83764`

```dockerfile
```

-	Layers:
	-	`sha256:22e87d6b0e04a586e7aa6c78eb14b9a91c6cdf758d05689d6e5ad1fdb28500f9`  
		Last Modified: Thu, 28 Dec 2023 06:49:20 GMT  
		Size: 6.0 MB (5957832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2f685d460c8e1580d27e783afaeaa00a4649d6712d9e49b36f34e713c7a2386`  
		Last Modified: Thu, 28 Dec 2023 06:49:20 GMT  
		Size: 40.6 KB (40617 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache-bullseye` - linux; ppc64le

```console
$ docker pull drupal@sha256:0d97f6a2b67953c2d0f075c6dac3620777cc3322e059f187295c0c6e1b2ea77a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 MB (188235304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b76704ff8c67d980dcf199c5b4b4c59c077d716ed0fecd957798bff390a8fb`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Dec 2023 10:27:26 GMT
ADD file:1cb772a6ad8ca6301624db3141029490564de7673bc0f2d4bedb5a1578ea85bd in / 
# Wed, 06 Dec 2023 10:27:26 GMT
CMD ["bash"]
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Dec 2023 10:27:26 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 06 Dec 2023 10:27:26 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 06 Dec 2023 10:27:26 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 06 Dec 2023 10:27:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Dec 2023 10:27:26 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_VERSION=8.2.14
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.14.tar.xz.asc
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_SHA256=763ecd39fcf51c3815af6ef6e43fa9aa0d0bd8e5a615009e5f4780c92705f583
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 06 Dec 2023 10:27:26 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Dec 2023 10:27:26 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 06 Dec 2023 10:27:26 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Dec 2023 10:27:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Dec 2023 10:27:26 GMT
STOPSIGNAL SIGWINCH
# Wed, 06 Dec 2023 10:27:26 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 06 Dec 2023 10:27:26 GMT
WORKDIR /var/www/html
# Wed, 06 Dec 2023 10:27:26 GMT
EXPOSE 80
# Wed, 06 Dec 2023 10:27:26 GMT
CMD ["apache2-foreground"]
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Dec 2023 10:27:26 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Dec 2023 10:27:26 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 06 Dec 2023 10:27:26 GMT
ENV DRUPAL_VERSION=10.1.7
# Wed, 06 Dec 2023 10:27:26 GMT
WORKDIR /opt/drupal
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
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
	-	`sha256:3e2ffd98af05b14c2996fe3114f52c11cc3cdbcf60e51f10b7c9d586827ce848`  
		Last Modified: Thu, 28 Dec 2023 01:04:46 GMT  
		Size: 12.4 MB (12423078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08d57252a2a8fde560d940ec3faa0b20ba61eb198a8d90d7b4f6aee3a6ec1ae`  
		Last Modified: Thu, 28 Dec 2023 01:04:43 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433684682d63052ab67a46cdadc5d94c18b31c5cb87207ec492d0f0b1bb05547`  
		Last Modified: Thu, 28 Dec 2023 01:04:46 GMT  
		Size: 12.3 MB (12337509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b871690322a1e53b0a77500c4bbdbc1812ecc763f6e92959b6851f554c56a8b6`  
		Last Modified: Thu, 28 Dec 2023 01:04:43 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de653ad00d26657f2280777817dd889e1a4d613d28a171555d6c057782df8f72`  
		Last Modified: Thu, 28 Dec 2023 01:04:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b4e8a405ec8bc40e859a49f68985a65d351280ea7857cdc8113a6a6711ca49`  
		Last Modified: Thu, 28 Dec 2023 01:04:43 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efa88554625948fb7e6ee2f5b584f807fa0404cba27fb81ae4fb6755daf621a`  
		Last Modified: Thu, 28 Dec 2023 05:36:00 GMT  
		Size: 1.8 MB (1794608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f5ef284bd0dfea55b5f65135e6a77c99d8b476b7fc95c03ba8d857c612c82e`  
		Last Modified: Thu, 28 Dec 2023 05:36:00 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903546607555beeb6a3eb5c4aee160841d0bbb325d12d46a23baa4f29e35b5a7`  
		Last Modified: Thu, 28 Dec 2023 05:36:00 GMT  
		Size: 705.2 KB (705211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7140729493d8db95628f8c4b80e1f4e6a9caa2c2b1badfd44623ac372b9e509`  
		Last Modified: Thu, 28 Dec 2023 05:36:00 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f26d0f7f5d3bbe2373af8febb22456782c1dcddd9d9eeb824c6967a2033ac48`  
		Last Modified: Thu, 28 Dec 2023 05:44:13 GMT  
		Size: 18.6 MB (18556428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:c5b17eac731ff663c3cc3d7d96f50d693fdca3ea7b45d23085c309a528e67198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5975012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60922a997d29c1281887ec156c211fd16e7770e29eafa345ed73c64f8dde3256`

```dockerfile
```

-	Layers:
	-	`sha256:fa20cbe7dc4f9d19e6dfbe0c0a35ad11f579ca4fe4da1fa1926bfddcd52232f4`  
		Last Modified: Thu, 28 Dec 2023 07:15:00 GMT  
		Size: 5.9 MB (5938649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5d251f4ef0748aed5d05797caa60937ae492a0c122485dd10306ea0e0fb09fd`  
		Last Modified: Thu, 28 Dec 2023 07:15:00 GMT  
		Size: 36.4 KB (36363 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache-bullseye` - linux; s390x

```console
$ docker pull drupal@sha256:473caf1097f66fad50c413c8026338e0b36b74c019860c3060bf9050343c22fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.5 MB (164511730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127493e1ec05d6af52f1d1388d5c9eb077ade33fcfe9e04ab3febcddd04aba0a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Dec 2023 10:27:26 GMT
ADD file:36a070457acddafcd6cdda22a3c41efcbd4e2b1694831eb74c8143520ebf1cf2 in / 
# Wed, 06 Dec 2023 10:27:26 GMT
CMD ["bash"]
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Dec 2023 10:27:26 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 06 Dec 2023 10:27:26 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 06 Dec 2023 10:27:26 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 06 Dec 2023 10:27:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Dec 2023 10:27:26 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_VERSION=8.2.14
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.14.tar.xz.asc
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PHP_SHA256=763ecd39fcf51c3815af6ef6e43fa9aa0d0bd8e5a615009e5f4780c92705f583
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 06 Dec 2023 10:27:26 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Dec 2023 10:27:26 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 06 Dec 2023 10:27:26 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Dec 2023 10:27:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Dec 2023 10:27:26 GMT
STOPSIGNAL SIGWINCH
# Wed, 06 Dec 2023 10:27:26 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 06 Dec 2023 10:27:26 GMT
WORKDIR /var/www/html
# Wed, 06 Dec 2023 10:27:26 GMT
EXPOSE 80
# Wed, 06 Dec 2023 10:27:26 GMT
CMD ["apache2-foreground"]
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Dec 2023 10:27:26 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Dec 2023 10:27:26 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 06 Dec 2023 10:27:26 GMT
ENV DRUPAL_VERSION=10.1.7
# Wed, 06 Dec 2023 10:27:26 GMT
WORKDIR /opt/drupal
# Wed, 06 Dec 2023 10:27:26 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 06 Dec 2023 10:27:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
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
	-	`sha256:417872a1ffa0382cb20507e28e2def560fe3034ad5e386680912e932a3869251`  
		Last Modified: Wed, 27 Dec 2023 23:44:06 GMT  
		Size: 12.4 MB (12422064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef95e093c6e07b0811c0003dea78fb3df5acc2114050b5c06b0341bf6165997`  
		Last Modified: Wed, 27 Dec 2023 23:44:05 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43317b2f3fffa46a7c52d640bace7f38cfdeef454e3d671beebaa77a7dcbeac`  
		Last Modified: Wed, 27 Dec 2023 23:44:07 GMT  
		Size: 10.9 MB (10927357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e74e73245ed79efeb0a032b35dc680c08401a32aa74ccf7c699d7dde080dc70`  
		Last Modified: Wed, 27 Dec 2023 23:44:05 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d108d3688ebfe03e9e8be399a9e2d4c48460c86570ef96b7d2ef6f4c27d6e9a`  
		Last Modified: Wed, 27 Dec 2023 23:44:05 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1565cd212e079a08bc5e42ded9018b94a25e4c9e0b8985c865385d118df3c127`  
		Last Modified: Wed, 27 Dec 2023 23:44:05 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a5038ba70ea7fb9252742d2a91255cc24150a1889e2e659f032881d5b3145f`  
		Last Modified: Thu, 28 Dec 2023 03:05:48 GMT  
		Size: 1.5 MB (1522425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891dacc27792399f47f8fb5df6d21e68c4bf03b62f379de0124154fa1a7a6b13`  
		Last Modified: Thu, 28 Dec 2023 03:05:49 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd9d10f25ba5d017a719e7ecd55d22932d1738fbd4476d7ff0baa57d589d81d`  
		Last Modified: Thu, 28 Dec 2023 03:05:49 GMT  
		Size: 705.2 KB (705212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3357650ebf1fda5ec1bf5228d2cf04e142eaa531f7fe81c31625733a966dba0f`  
		Last Modified: Thu, 28 Dec 2023 03:05:49 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26e5e792e60154686004b01774ad4e4a8c99b1b1373df868df97d835ce460a8`  
		Last Modified: Thu, 28 Dec 2023 03:11:54 GMT  
		Size: 18.6 MB (18556305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:fed5a54925a4d76a81fb6e6081b1325142b4f0c039f32bf08a975e0197db5262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5855164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939a507d07390d1351fcacd56ec0d01255e758859466e5a7ffbcdc7e9ea38541`

```dockerfile
```

-	Layers:
	-	`sha256:b115750fbb06d9b291d709986821a3f6138abb42a7437462b5af577ef3616188`  
		Last Modified: Thu, 28 Dec 2023 03:11:54 GMT  
		Size: 5.8 MB (5818871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89c4789ba19a541cf62b7ca1db0980fba6945c4d5a4fa02d33a847548d69ff2e`  
		Last Modified: Thu, 28 Dec 2023 03:11:53 GMT  
		Size: 36.3 KB (36293 bytes)  
		MIME: application/vnd.in-toto+json
