## `joomla:php8.0`

```console
$ docker pull joomla@sha256:057b0c92bd7958fe3c0d4a3459758801b56dae7e1964076cff2c0e43b541e8cd
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

### `joomla:php8.0` - linux; amd64

```console
$ docker pull joomla@sha256:4b5b480ebddc3f9018aecaead5b5e6f508f4634d855056fb3e6c8cd62f8f9182
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 MB (192578640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:122df816694dff95b50fc59ec7e5a36b57e093604dde39e4c1adba17e84d9247`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:21 GMT
ADD file:19d7ba0fceddd7fc78b5fb96cf8110e5d10e0e5d2554030dfe640d161379cb79 in / 
# Fri, 03 Sep 2021 01:21:21 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 15:54:04 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 03 Sep 2021 15:54:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 03 Sep 2021 15:54:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 15:54:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 03 Sep 2021 15:54:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 03 Sep 2021 16:00:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 03 Sep 2021 16:00:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 03 Sep 2021 16:00:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 03 Sep 2021 16:00:26 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 03 Sep 2021 16:00:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 03 Sep 2021 16:00:27 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 03 Sep 2021 16:00:28 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 03 Sep 2021 16:00:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 03 Sep 2021 16:00:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 03 Sep 2021 16:00:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 03 Sep 2021 16:52:27 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 03 Sep 2021 16:52:28 GMT
ENV PHP_VERSION=8.0.10
# Fri, 03 Sep 2021 16:52:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.10.tar.xz.asc
# Fri, 03 Sep 2021 16:52:29 GMT
ENV PHP_SHA256=66dc4d1bc86d9c1bc255b51b79d337ed1a7a035cf71230daabbf9a4ca35795eb
# Fri, 03 Sep 2021 16:52:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 03 Sep 2021 16:52:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 03 Sep 2021 16:58:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 03 Sep 2021 16:58:48 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Fri, 03 Sep 2021 16:58:49 GMT
RUN docker-php-ext-enable sodium
# Fri, 03 Sep 2021 16:58:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 03 Sep 2021 16:58:50 GMT
STOPSIGNAL SIGWINCH
# Fri, 03 Sep 2021 16:58:50 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 03 Sep 2021 16:58:50 GMT
WORKDIR /var/www/html
# Fri, 03 Sep 2021 16:58:50 GMT
EXPOSE 80
# Fri, 03 Sep 2021 16:58:51 GMT
CMD ["apache2-foreground"]
# Tue, 07 Sep 2021 21:33:28 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 07 Sep 2021 21:33:29 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 07 Sep 2021 21:33:29 GMT
RUN a2enmod rewrite
# Tue, 07 Sep 2021 21:34:50 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libjpeg-dev 		libldap2-dev 		libmcrypt-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-jpeg; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		gmp 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.20; 	pecl install memcached-3.1.5; 	pecl install redis-5.3.4; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Sep 2021 21:34:51 GMT
VOLUME [/var/www/html]
# Wed, 15 Sep 2021 00:26:57 GMT
ENV JOOMLA_VERSION=4.0.3
# Wed, 15 Sep 2021 00:26:57 GMT
ENV JOOMLA_SHA512=9c09a621586fdcc30351a915f283581c92080c210294cacc50e0e390d991f32bee9d61dfc7b0af33c81118e46d775152159c0e27dbf73f5531512328d716901f
# Wed, 15 Sep 2021 00:27:03 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Wed, 15 Sep 2021 00:27:03 GMT
COPY file:f6b7a1c96cc89593a2b9ce4c68af350ae02f2e0c654cd5e842ff6c03641d470e in /entrypoint.sh 
# Wed, 15 Sep 2021 00:27:04 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Wed, 15 Sep 2021 00:27:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Sep 2021 00:27:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f8416d8bac72cefc0ce17bd2dc0c03aa43e123d309db92ee23be9382192cf2ed`  
		Last Modified: Fri, 03 Sep 2021 01:27:25 GMT  
		Size: 31.4 MB (31368702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2259392b425a174e24087b88998f9435dfee626ec8f78b8cc5cca621f7e5308b`  
		Last Modified: Fri, 03 Sep 2021 19:20:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb39fc3daf578abbdb986559d371815b4d0d565a6f27382537ba9efcfb96273`  
		Last Modified: Fri, 03 Sep 2021 19:20:48 GMT  
		Size: 91.6 MB (91605346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c501de24ca4a4f13ad18f4da04cabd46e327c4e2be77f23c696e71efff86d2d`  
		Last Modified: Fri, 03 Sep 2021 19:20:31 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf5f97ffc5cb3ceebcff33df6c7fca3dca7b3e90445ac9bbea422555a31631e`  
		Last Modified: Fri, 03 Sep 2021 19:21:21 GMT  
		Size: 19.2 MB (19222964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a408db913f463316172a6e72cc5579ce530563b6ad140b9650903187b819075c`  
		Last Modified: Fri, 03 Sep 2021 19:21:18 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43600da0ccdc01c77536c4607b851f4b2a372a1108fc422a33e0a0f42d91b1af`  
		Last Modified: Fri, 03 Sep 2021 19:21:17 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd879a50cd745c1f642afc8b6ae5830ecb4a869fdd6301431930e23ff271dfe`  
		Last Modified: Fri, 03 Sep 2021 19:25:00 GMT  
		Size: 11.0 MB (11044056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ef22c774e247efd372805f4191f7e39fe8d3791cc274139bbc9e23944b8591`  
		Last Modified: Fri, 03 Sep 2021 19:24:56 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44cab4e2f895b5b2ccbe78977a4fb07eae107ab7f344e292ed445c625158c77c`  
		Last Modified: Fri, 03 Sep 2021 19:25:00 GMT  
		Size: 15.0 MB (15037479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23fce1b9949db087dd44672a7509db45aee49a6646d2c7dffd428713e2e55f76`  
		Last Modified: Fri, 03 Sep 2021 19:24:56 GMT  
		Size: 2.3 KB (2272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279446384096d2bbd748d55262d69e98516922066abf436c89e928139f95659a`  
		Last Modified: Fri, 03 Sep 2021 19:24:56 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1daf7ecac3785c3e285008c43d4d91f5fe2f33e539e8e05c3b56cf64dcd9b36`  
		Last Modified: Fri, 03 Sep 2021 19:24:56 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b0c021ccb25ec382606b9c052b1ce13abb36006a355a837acf105ab2ea3b29`  
		Last Modified: Tue, 07 Sep 2021 21:46:39 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37648710865eee74685464d91e778a1ee4eac35d0fc9e4aac0e2e2a1e50c4b06`  
		Last Modified: Tue, 07 Sep 2021 21:46:40 GMT  
		Size: 3.0 MB (2968023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdfd9127893606b513ada0e47f753a7f324fa2fc345ad5b250e94e72a1b1d9db`  
		Last Modified: Wed, 15 Sep 2021 00:30:40 GMT  
		Size: 21.3 MB (21324575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d880bd4b221feac02609ad7ccfdd447e7ca4f5302e3489b820c656c53e7314a4`  
		Last Modified: Wed, 15 Sep 2021 00:30:36 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d9dbe3bc5288210c8847dd6728d684fd145b3383361083a5ea33ffccd581e2`  
		Last Modified: Wed, 15 Sep 2021 00:30:37 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php8.0` - linux; arm variant v5

```console
$ docker pull joomla@sha256:dc6ab81a703a6afffad78eb4e850b392998c1d9266f7fe4f90400300668dfc22
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.0 MB (170046520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f92cb35e5d48bd2016ba19d8630ba6eba1ee2f0b41afc9b77e191826517a4e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 03 Sep 2021 00:50:28 GMT
ADD file:3370827f2aa0dc43cfc2dcb693f82d3f450a70850de7e2514117e366f660d302 in / 
# Fri, 03 Sep 2021 00:50:29 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 04:11:10 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 03 Sep 2021 04:11:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 03 Sep 2021 04:11:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 04:12:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 03 Sep 2021 04:12:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 03 Sep 2021 04:17:50 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 03 Sep 2021 04:17:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 03 Sep 2021 04:18:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 03 Sep 2021 04:18:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 03 Sep 2021 04:18:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 03 Sep 2021 04:18:18 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 03 Sep 2021 04:18:19 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 03 Sep 2021 04:18:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 03 Sep 2021 04:18:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 03 Sep 2021 04:18:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 03 Sep 2021 05:07:57 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 03 Sep 2021 05:07:58 GMT
ENV PHP_VERSION=8.0.10
# Fri, 03 Sep 2021 05:07:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.10.tar.xz.asc
# Fri, 03 Sep 2021 05:07:59 GMT
ENV PHP_SHA256=66dc4d1bc86d9c1bc255b51b79d337ed1a7a035cf71230daabbf9a4ca35795eb
# Fri, 03 Sep 2021 05:08:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 03 Sep 2021 05:08:30 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 03 Sep 2021 05:13:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 03 Sep 2021 05:13:34 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Fri, 03 Sep 2021 05:13:35 GMT
RUN docker-php-ext-enable sodium
# Fri, 03 Sep 2021 05:13:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 03 Sep 2021 05:13:36 GMT
STOPSIGNAL SIGWINCH
# Fri, 03 Sep 2021 05:13:37 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 03 Sep 2021 05:13:37 GMT
WORKDIR /var/www/html
# Fri, 03 Sep 2021 05:13:38 GMT
EXPOSE 80
# Fri, 03 Sep 2021 05:13:38 GMT
CMD ["apache2-foreground"]
# Tue, 07 Sep 2021 21:04:00 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 07 Sep 2021 21:04:01 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 07 Sep 2021 21:04:02 GMT
RUN a2enmod rewrite
# Tue, 07 Sep 2021 21:08:22 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libjpeg-dev 		libldap2-dev 		libmcrypt-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-jpeg; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		gmp 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.20; 	pecl install memcached-3.1.5; 	pecl install redis-5.3.4; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Sep 2021 21:08:23 GMT
VOLUME [/var/www/html]
# Tue, 14 Sep 2021 23:49:59 GMT
ENV JOOMLA_VERSION=4.0.3
# Tue, 14 Sep 2021 23:49:59 GMT
ENV JOOMLA_SHA512=9c09a621586fdcc30351a915f283581c92080c210294cacc50e0e390d991f32bee9d61dfc7b0af33c81118e46d775152159c0e27dbf73f5531512328d716901f
# Tue, 14 Sep 2021 23:50:16 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Tue, 14 Sep 2021 23:50:18 GMT
COPY file:f6b7a1c96cc89593a2b9ce4c68af350ae02f2e0c654cd5e842ff6c03641d470e in /entrypoint.sh 
# Tue, 14 Sep 2021 23:50:18 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Tue, 14 Sep 2021 23:50:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Sep 2021 23:50:19 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f97b1d091d60e08b0ff779d3cf24a016e55312c03d0930408ff1e1f18d486139`  
		Last Modified: Fri, 03 Sep 2021 01:05:38 GMT  
		Size: 28.9 MB (28910713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0855b53c06c71ed242ae550f9010975ff3a38ad640fee0958ecc52b5e78302`  
		Last Modified: Fri, 03 Sep 2021 07:29:14 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168c68f9a53c8d179eb9ffe2d4edbb5fc9e2ed1d245215de94cc8b8aee9300d2`  
		Last Modified: Fri, 03 Sep 2021 07:30:05 GMT  
		Size: 73.7 MB (73670746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b119b13b86ab970aa45086e554b440387a7d6dc528d851152486fbc195e2eb25`  
		Last Modified: Fri, 03 Sep 2021 07:29:13 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ed8348f43f49c9514db26b31788e64cb18bebf9b70067f5149f5300ef06f9c`  
		Last Modified: Fri, 03 Sep 2021 07:30:56 GMT  
		Size: 18.5 MB (18523102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcae2769949296af28a0e737a9037d14654ac586ae12c1d99924adb81aed9e0e`  
		Last Modified: Fri, 03 Sep 2021 07:30:45 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a6c6c2d47dc36de52018fe7d338df2ba9bc9f1b5014362dbc67a8a0b66e22f`  
		Last Modified: Fri, 03 Sep 2021 07:30:45 GMT  
		Size: 517.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84719f736ab8dad9f824c6a8c7d8ebf0b0aa5a6bc3a7b13dadb37bcbc148daf`  
		Last Modified: Fri, 03 Sep 2021 07:36:43 GMT  
		Size: 11.0 MB (11042686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc870bbd45a0380cd1aead0f9d2efd901bcae950bfc9380a9b8e2e1deccf5084`  
		Last Modified: Fri, 03 Sep 2021 07:36:37 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e217a9153287a2a5007a2bcaf1096c0e068ad4157ea3e51f151aa312b34b31b6`  
		Last Modified: Fri, 03 Sep 2021 07:36:48 GMT  
		Size: 13.8 MB (13779767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a2afd19692d6734ab4f431867d954b3f409d4bd86094a63baf4bb5027b250e`  
		Last Modified: Fri, 03 Sep 2021 07:36:38 GMT  
		Size: 2.3 KB (2275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e538aab9e304571105d2edf6a9f1ea33fc1464f8d7feb16bbdef363313759d`  
		Last Modified: Fri, 03 Sep 2021 07:36:37 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42bebc8ea9d918e824fb0bfea735468f9522d8755593e08997064eeeefb1fa77`  
		Last Modified: Fri, 03 Sep 2021 07:36:37 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b7c7baac8e756f0cae1603ec7919ccb15d1fe9fa2a396b557bef6d8e6a4f4d`  
		Last Modified: Tue, 07 Sep 2021 21:29:56 GMT  
		Size: 314.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d12ac01f3468dec04ea1d60894fa2e901b4fb560ecc178f0c95beefef06b1f`  
		Last Modified: Tue, 07 Sep 2021 21:29:58 GMT  
		Size: 2.8 MB (2787598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48213dce21121c783daea261af42482c55ae4886190f0b07a80c96623b29b41`  
		Last Modified: Tue, 14 Sep 2021 23:58:23 GMT  
		Size: 21.3 MB (21324391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf58fd4d698692bd71d94c0690a66a3ba41ba4788e92e3ab4f1b55caac00243`  
		Last Modified: Tue, 14 Sep 2021 23:58:05 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ced7532c55cd03d12d971027c4a483564f76f9216ce6b88299c5a193016ee2`  
		Last Modified: Tue, 14 Sep 2021 23:58:05 GMT  
		Size: 613.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php8.0` - linux; arm variant v7

```console
$ docker pull joomla@sha256:e95bd278360f8a9dfb9d61dccacb22a582369b1bf37debd7aabda6a3b2bc3af5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.0 MB (162013360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ea29d864fe484da57a11bf03ef23ab15e2b3f54c9f68a1cfdae7dcb69bf1d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 03 Sep 2021 00:59:39 GMT
ADD file:94917ec8eb06f96483e43104557dd98e5160895900a9d49318eecbb3d5689d41 in / 
# Fri, 03 Sep 2021 00:59:39 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 13:19:09 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 03 Sep 2021 13:19:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 03 Sep 2021 13:19:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 13:19:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 03 Sep 2021 13:19:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 03 Sep 2021 13:25:14 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 03 Sep 2021 13:25:14 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 03 Sep 2021 13:25:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 03 Sep 2021 13:25:37 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 03 Sep 2021 13:25:39 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 03 Sep 2021 13:25:40 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 03 Sep 2021 13:25:40 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 03 Sep 2021 13:25:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 03 Sep 2021 13:25:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 03 Sep 2021 13:25:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 03 Sep 2021 14:09:50 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 03 Sep 2021 14:09:51 GMT
ENV PHP_VERSION=8.0.10
# Fri, 03 Sep 2021 14:09:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.10.tar.xz.asc
# Fri, 03 Sep 2021 14:09:52 GMT
ENV PHP_SHA256=66dc4d1bc86d9c1bc255b51b79d337ed1a7a035cf71230daabbf9a4ca35795eb
# Fri, 03 Sep 2021 14:10:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 03 Sep 2021 14:10:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 03 Sep 2021 14:14:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 03 Sep 2021 14:14:43 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Fri, 03 Sep 2021 14:14:45 GMT
RUN docker-php-ext-enable sodium
# Fri, 03 Sep 2021 14:14:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 03 Sep 2021 14:14:46 GMT
STOPSIGNAL SIGWINCH
# Fri, 03 Sep 2021 14:14:46 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 03 Sep 2021 14:14:47 GMT
WORKDIR /var/www/html
# Fri, 03 Sep 2021 14:14:47 GMT
EXPOSE 80
# Fri, 03 Sep 2021 14:14:48 GMT
CMD ["apache2-foreground"]
# Tue, 07 Sep 2021 21:29:33 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 07 Sep 2021 21:29:34 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 07 Sep 2021 21:29:35 GMT
RUN a2enmod rewrite
# Tue, 07 Sep 2021 21:33:48 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libjpeg-dev 		libldap2-dev 		libmcrypt-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-jpeg; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		gmp 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.20; 	pecl install memcached-3.1.5; 	pecl install redis-5.3.4; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Sep 2021 21:33:49 GMT
VOLUME [/var/www/html]
# Wed, 15 Sep 2021 00:34:16 GMT
ENV JOOMLA_VERSION=4.0.3
# Wed, 15 Sep 2021 00:34:16 GMT
ENV JOOMLA_SHA512=9c09a621586fdcc30351a915f283581c92080c210294cacc50e0e390d991f32bee9d61dfc7b0af33c81118e46d775152159c0e27dbf73f5531512328d716901f
# Wed, 15 Sep 2021 00:34:33 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Wed, 15 Sep 2021 00:34:35 GMT
COPY file:f6b7a1c96cc89593a2b9ce4c68af350ae02f2e0c654cd5e842ff6c03641d470e in /entrypoint.sh 
# Wed, 15 Sep 2021 00:34:35 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Wed, 15 Sep 2021 00:34:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Sep 2021 00:34:36 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:9bd46ffb253d51a8cc84bf034d289b4ca60344ca4446bf38633639b54c7c7ab9`  
		Last Modified: Fri, 03 Sep 2021 01:14:54 GMT  
		Size: 26.6 MB (26571627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98086d1d5d8748a43bc89bf79908db4dcd59985bc8a6ffbd735a3086b0458ce0`  
		Last Modified: Fri, 03 Sep 2021 16:29:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c9e09fff15b471e68b56ece698c546ca2645e0751d7dc552ccdb8c59bd2a82`  
		Last Modified: Fri, 03 Sep 2021 16:30:29 GMT  
		Size: 69.3 MB (69315381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750c1d85f381bb097a930260277acf05927eddcc909604fb67cb27a06bb0a230`  
		Last Modified: Fri, 03 Sep 2021 16:29:46 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7adaef0b8aed940e6d5f02bc1775889c49f91b9323b6b22098afbff5e8d96c10`  
		Last Modified: Fri, 03 Sep 2021 16:31:19 GMT  
		Size: 18.0 MB (17974847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be28e83c0418bb9271dff8e582820d38182412bf4ecf0df02adb90552c724708`  
		Last Modified: Fri, 03 Sep 2021 16:31:10 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd6fa1d3b53e58c32ffaebc3746115bbed0c1af5d218f1afcc41ab018a8ad3c`  
		Last Modified: Fri, 03 Sep 2021 16:31:10 GMT  
		Size: 518.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3e217f6750d2fd2d7da013ece896e87bbf49a4ff3500b28155f79ef8391905`  
		Last Modified: Fri, 03 Sep 2021 16:37:23 GMT  
		Size: 11.0 MB (11042633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3065229553e4ab41b9d2a54f428bfeb4eaf5ad9ca0e7c77a1af402dbdebaf47`  
		Last Modified: Fri, 03 Sep 2021 16:37:17 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9881bb8de01826841871a5bfa76cb9b6f0000d340ca2e4ccc89fb08099bc35e`  
		Last Modified: Fri, 03 Sep 2021 16:37:27 GMT  
		Size: 13.1 MB (13088530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7024eaaaf3fdbecfb1fd7342bba1a4f03739f7f4436b0f39223fbcdb3da6f4`  
		Last Modified: Fri, 03 Sep 2021 16:37:18 GMT  
		Size: 2.3 KB (2272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4353a4a365b799b30ca76b0ed15a69af67c87a2e7b3a35ed058c690b569b6b`  
		Last Modified: Fri, 03 Sep 2021 16:37:17 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaccae5bc9cc1fefa7af23bc40200fbe1eaf6411fd63819b5c44bb34d66e0675`  
		Last Modified: Fri, 03 Sep 2021 16:37:18 GMT  
		Size: 891.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb105dbde44730f6343126ab1dffd6c009d3faca3135680ebdd1c5fcde98431`  
		Last Modified: Tue, 07 Sep 2021 22:07:03 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192736961d7a0e3fea86fbbb7f11d77e007c0a9d9f174bbdebce575999c02cd0`  
		Last Modified: Tue, 07 Sep 2021 22:07:04 GMT  
		Size: 2.7 MB (2688304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d33dbbe4aec58637700d13968ab78afe72d0713d3e7560b963e2762d0ed4141`  
		Last Modified: Wed, 15 Sep 2021 00:45:52 GMT  
		Size: 21.3 MB (21324523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5a83355c8806a02fa6595ba2fd9d3dc83860c6bb52060fe4e2378dc39921ea`  
		Last Modified: Wed, 15 Sep 2021 00:45:33 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085aeecd181296106b0686519346c89f25e20010d59eab3bf8a0a91aa3ec551c`  
		Last Modified: Wed, 15 Sep 2021 00:45:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php8.0` - linux; arm64 variant v8

```console
$ docker pull joomla@sha256:ad350bac39619cede045926369504a7f4667e3286177abfa45260bf852da1342
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.8 MB (185779416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb25da063ed18f5d83460ee78e97c40d7b6f2734f1f63e3b040ab21f29580d44`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 03 Sep 2021 00:40:33 GMT
ADD file:9600a4686ae105acffa54787a7c81f5252e90023cbcfbe37519150b954110c5c in / 
# Fri, 03 Sep 2021 00:40:34 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:06:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 03 Sep 2021 08:06:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 03 Sep 2021 08:06:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 08:06:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 03 Sep 2021 08:06:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 03 Sep 2021 08:12:06 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 03 Sep 2021 08:12:07 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 03 Sep 2021 08:12:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 03 Sep 2021 08:12:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 03 Sep 2021 08:12:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 03 Sep 2021 08:12:16 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 03 Sep 2021 08:12:16 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 03 Sep 2021 08:12:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 03 Sep 2021 08:12:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 03 Sep 2021 08:12:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 03 Sep 2021 08:55:15 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 03 Sep 2021 08:55:15 GMT
ENV PHP_VERSION=8.0.10
# Fri, 03 Sep 2021 08:55:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.10.tar.xz.asc
# Fri, 03 Sep 2021 08:55:15 GMT
ENV PHP_SHA256=66dc4d1bc86d9c1bc255b51b79d337ed1a7a035cf71230daabbf9a4ca35795eb
# Fri, 03 Sep 2021 08:55:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 03 Sep 2021 08:55:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 03 Sep 2021 08:58:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 03 Sep 2021 08:58:48 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Fri, 03 Sep 2021 08:58:49 GMT
RUN docker-php-ext-enable sodium
# Fri, 03 Sep 2021 08:58:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 03 Sep 2021 08:58:49 GMT
STOPSIGNAL SIGWINCH
# Fri, 03 Sep 2021 08:58:50 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 03 Sep 2021 08:58:50 GMT
WORKDIR /var/www/html
# Fri, 03 Sep 2021 08:58:50 GMT
EXPOSE 80
# Fri, 03 Sep 2021 08:58:50 GMT
CMD ["apache2-foreground"]
# Tue, 07 Sep 2021 20:59:26 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 07 Sep 2021 20:59:26 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 07 Sep 2021 20:59:27 GMT
RUN a2enmod rewrite
# Tue, 07 Sep 2021 21:00:52 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libjpeg-dev 		libldap2-dev 		libmcrypt-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-jpeg; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		gmp 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.20; 	pecl install memcached-3.1.5; 	pecl install redis-5.3.4; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Sep 2021 21:00:52 GMT
VOLUME [/var/www/html]
# Tue, 14 Sep 2021 23:57:17 GMT
ENV JOOMLA_VERSION=4.0.3
# Tue, 14 Sep 2021 23:57:18 GMT
ENV JOOMLA_SHA512=9c09a621586fdcc30351a915f283581c92080c210294cacc50e0e390d991f32bee9d61dfc7b0af33c81118e46d775152159c0e27dbf73f5531512328d716901f
# Tue, 14 Sep 2021 23:57:23 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Tue, 14 Sep 2021 23:57:23 GMT
COPY file:f6b7a1c96cc89593a2b9ce4c68af350ae02f2e0c654cd5e842ff6c03641d470e in /entrypoint.sh 
# Tue, 14 Sep 2021 23:57:24 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Tue, 14 Sep 2021 23:57:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Sep 2021 23:57:24 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:1901ca797b5ea06f6a4facc81ad772177fdd833ed4329dc86ef126078633b949`  
		Last Modified: Fri, 03 Sep 2021 00:48:51 GMT  
		Size: 30.1 MB (30055483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e208c3dde644081fc0bf55738a8e668b9c3e2d1f0d6a1cd896fccff72d053a88`  
		Last Modified: Fri, 03 Sep 2021 10:26:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d35ae33d3a3b866de3d3541f9659050060c0e732b29aa00734d40eea2f99bcb`  
		Last Modified: Fri, 03 Sep 2021 10:26:37 GMT  
		Size: 86.9 MB (86920765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656c97547b711b8b733612392f1852b0f8c11acbe09c621a40323801c516d7de`  
		Last Modified: Fri, 03 Sep 2021 10:26:22 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6029d21bab5922f62067d1795788a411a3cb926d90fd882d843dd47c768a431`  
		Last Modified: Fri, 03 Sep 2021 10:27:17 GMT  
		Size: 19.1 MB (19140014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45afe23d9dfbfcbaedbe4794ca5892969bf2f428468f8df1e2440652e35c18c3`  
		Last Modified: Fri, 03 Sep 2021 10:27:13 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819f2bfcedb940f158fe822c423ce9e056e064a51d5aa0afa5b141ad7bf69262`  
		Last Modified: Fri, 03 Sep 2021 10:27:13 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa15754929c1b7753c40ff0f2b46473799b30a002ba6ebe50d7973f153902b8`  
		Last Modified: Fri, 03 Sep 2021 10:31:10 GMT  
		Size: 11.0 MB (11043324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df77cda553ce0a2b2380aa18106591d1f78c0c95132c5daaeeeacc74769093e`  
		Last Modified: Fri, 03 Sep 2021 10:31:06 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcdf57cb33efdadc2cbda812d2d668dc917c0a5828a7e97115d63de741e419db`  
		Last Modified: Fri, 03 Sep 2021 10:31:09 GMT  
		Size: 14.4 MB (14367844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb11198328db0a14be0fd1578209c1393bf5932c3bf6b6fe45a04d765fa81c7`  
		Last Modified: Fri, 03 Sep 2021 10:31:07 GMT  
		Size: 2.3 KB (2274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7b90ac4f2a2f7216a7dc14dffc260f0a36d4eeb32e2a8dcac859c82cff8b07`  
		Last Modified: Fri, 03 Sep 2021 10:31:07 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87b6624da7e6adbed9c1f24c6104398bc2fc3052bb67cbe68da627bac146a71`  
		Last Modified: Fri, 03 Sep 2021 10:31:06 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed8f482dc27c0a94230c34a0c63729752c0bfedc654c503842c6043f1050747`  
		Last Modified: Tue, 07 Sep 2021 21:14:47 GMT  
		Size: 314.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1ddae6d33d622b2af9ee34dfbb433574e9422af784c58268e93d6ac73bc4cb`  
		Last Modified: Tue, 07 Sep 2021 21:14:48 GMT  
		Size: 2.9 MB (2919845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdc87c7f2087677aca6d6949e35bcecd237bffd51153689b1243b37b169baca`  
		Last Modified: Wed, 15 Sep 2021 00:02:47 GMT  
		Size: 21.3 MB (21324635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1183597b3b85bd850b350ea782a46631945e737108d64eda1814808feb951fbc`  
		Last Modified: Wed, 15 Sep 2021 00:02:43 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdcbc5a629ff10dd57b64fa07b880c2ea79f35580d442c275e9de44211286260`  
		Last Modified: Wed, 15 Sep 2021 00:02:43 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php8.0` - linux; 386

```console
$ docker pull joomla@sha256:ebdc9e79f583f82efeb5eef4c69d3434de7c41f741fdb74175d1d64f55319e7b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195558754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9912df677740718815b371f723f4a1ee75827a7e738a7264147b9604caa4e96d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 03 Sep 2021 00:39:52 GMT
ADD file:dcef0e50863a79295fdbbdad2086d337d6935a220550cb8adaedd7929bd7de63 in / 
# Fri, 03 Sep 2021 00:39:52 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 06:57:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 03 Sep 2021 06:57:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 03 Sep 2021 06:57:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 06:57:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 03 Sep 2021 06:57:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 03 Sep 2021 07:04:29 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 03 Sep 2021 07:04:29 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 03 Sep 2021 07:04:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 03 Sep 2021 07:04:41 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 03 Sep 2021 07:04:42 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 03 Sep 2021 07:04:42 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 03 Sep 2021 07:04:43 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 03 Sep 2021 07:04:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 03 Sep 2021 07:04:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 03 Sep 2021 07:04:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 03 Sep 2021 07:57:33 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 03 Sep 2021 07:57:33 GMT
ENV PHP_VERSION=8.0.10
# Fri, 03 Sep 2021 07:57:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.10.tar.xz.asc
# Fri, 03 Sep 2021 07:57:33 GMT
ENV PHP_SHA256=66dc4d1bc86d9c1bc255b51b79d337ed1a7a035cf71230daabbf9a4ca35795eb
# Fri, 03 Sep 2021 07:57:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 03 Sep 2021 07:57:47 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 03 Sep 2021 08:03:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 03 Sep 2021 08:03:29 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Fri, 03 Sep 2021 08:03:30 GMT
RUN docker-php-ext-enable sodium
# Fri, 03 Sep 2021 08:03:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 03 Sep 2021 08:03:30 GMT
STOPSIGNAL SIGWINCH
# Fri, 03 Sep 2021 08:03:30 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 03 Sep 2021 08:03:31 GMT
WORKDIR /var/www/html
# Fri, 03 Sep 2021 08:03:31 GMT
EXPOSE 80
# Fri, 03 Sep 2021 08:03:31 GMT
CMD ["apache2-foreground"]
# Tue, 07 Sep 2021 20:48:52 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 07 Sep 2021 20:48:52 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 07 Sep 2021 20:48:53 GMT
RUN a2enmod rewrite
# Tue, 07 Sep 2021 20:50:19 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libjpeg-dev 		libldap2-dev 		libmcrypt-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-jpeg; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		gmp 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.20; 	pecl install memcached-3.1.5; 	pecl install redis-5.3.4; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Sep 2021 20:50:19 GMT
VOLUME [/var/www/html]
# Tue, 14 Sep 2021 23:45:07 GMT
ENV JOOMLA_VERSION=4.0.3
# Tue, 14 Sep 2021 23:45:07 GMT
ENV JOOMLA_SHA512=9c09a621586fdcc30351a915f283581c92080c210294cacc50e0e390d991f32bee9d61dfc7b0af33c81118e46d775152159c0e27dbf73f5531512328d716901f
# Tue, 14 Sep 2021 23:45:14 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Tue, 14 Sep 2021 23:45:15 GMT
COPY file:f6b7a1c96cc89593a2b9ce4c68af350ae02f2e0c654cd5e842ff6c03641d470e in /entrypoint.sh 
# Tue, 14 Sep 2021 23:45:15 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Tue, 14 Sep 2021 23:45:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Sep 2021 23:45:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e16e03ac165c3106d1f4265c32840999585f4c4f0e56bd13286caeef08c5be9a`  
		Last Modified: Fri, 03 Sep 2021 00:48:04 GMT  
		Size: 32.4 MB (32379875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c426639a80dc4c00780cd81e4cc98fd456fdb77860d03ff18f1e99c367a69788`  
		Last Modified: Fri, 03 Sep 2021 10:41:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25d32a328bbb755d97d4b4fe8ba233c8473d3ab1f708851cf3ac63fccad0302b`  
		Last Modified: Fri, 03 Sep 2021 10:41:49 GMT  
		Size: 92.7 MB (92712721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309cb1c222cc4d605994e6e6f8fda2d134bd40a4c8fccc34b889580c9eeeda26`  
		Last Modified: Fri, 03 Sep 2021 10:41:11 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3c9fbfaedd1a7c53c7bde25caba25e245c396a8c567995ea9d2f45adb3de4e`  
		Last Modified: Fri, 03 Sep 2021 10:42:39 GMT  
		Size: 19.7 MB (19691516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736ced88c0dcecfc31ee32161f51c262524f52fef812be0d351515c4fbcc3722`  
		Last Modified: Fri, 03 Sep 2021 10:42:30 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82d85bae9fd096361da9d3da23541f8f09740810177a8d3a9a7f874866fc3f4`  
		Last Modified: Fri, 03 Sep 2021 10:42:30 GMT  
		Size: 514.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f962437a2a45d3d10aa59a10d3d43c32857546666cbf0f53b0fc6a28f17a85b2`  
		Last Modified: Fri, 03 Sep 2021 10:48:01 GMT  
		Size: 11.0 MB (11043410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98365ef7ebacfc62ca4dd839ed7ea03d5a48aa14b3ef961fb764d87cd4434c60`  
		Last Modified: Fri, 03 Sep 2021 10:47:57 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d78388fb35cf15fa27acb7b4fa228a9212790c42f00cc4fe3087945c8a855bc`  
		Last Modified: Fri, 03 Sep 2021 10:48:02 GMT  
		Size: 15.4 MB (15416667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e3b33e25fa6eb8e3a579982b6151905612ed70c768006b75f7f0e4af611241`  
		Last Modified: Fri, 03 Sep 2021 10:47:57 GMT  
		Size: 2.3 KB (2275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f2d5b2e94b87c9135a9428bcb44c71f8b494cbe5c6f78405af868d53e653ec`  
		Last Modified: Fri, 03 Sep 2021 10:47:57 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd85b4ddcf7fca4063dddd4a6738d9b00f5d8d6f1eea5eb7e5f142eba442de9b`  
		Last Modified: Fri, 03 Sep 2021 10:47:57 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5df1ecd8e6388af6630c61d040a7adce329ee0c1550df9f5d9accf7c82553c`  
		Last Modified: Tue, 07 Sep 2021 21:03:40 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:467b876846b9accebb8cde03f1892f0da856a4d9db01a8f6992ab7571c4b3e55`  
		Last Modified: Tue, 07 Sep 2021 21:03:41 GMT  
		Size: 3.0 MB (2982485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d51a4d043e16d542a675e18e41a3952ab943ffe886898e75765290f9c40c5ca`  
		Last Modified: Tue, 14 Sep 2021 23:53:10 GMT  
		Size: 21.3 MB (21324569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad1429b382598cf558734d4b23c5d0180130bb2ec64dcbef5a3a7dc7080fd5c`  
		Last Modified: Tue, 14 Sep 2021 23:53:05 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eebe71ccf25bb9ee6283127a27615a806b60171c6552301c92a5ad55e11186a0`  
		Last Modified: Tue, 14 Sep 2021 23:53:05 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php8.0` - linux; mips64le

```console
$ docker pull joomla@sha256:dc859c05b4e939439089753a661f57e27dfcab9b526eb1623fd5eceb13654c6c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.0 MB (169950484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b78f372b6c00862e2a03b4a95a8741203178cbf23da1cc297fb31d56ac0f8b08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 03 Sep 2021 01:10:01 GMT
ADD file:e842559443fb9351f1a9ac9ce03dfe0b069d8b9c3409f8d9b21abcbdc2a437c5 in / 
# Fri, 03 Sep 2021 01:10:02 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 03:39:32 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 03 Sep 2021 03:39:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 03 Sep 2021 03:40:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 03:40:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 03 Sep 2021 03:40:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 03 Sep 2021 03:53:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 03 Sep 2021 03:53:32 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 03 Sep 2021 03:53:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 03 Sep 2021 03:54:00 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 03 Sep 2021 03:54:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 03 Sep 2021 03:54:03 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 03 Sep 2021 03:54:03 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 03 Sep 2021 03:54:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 03 Sep 2021 03:54:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 03 Sep 2021 03:54:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 03 Sep 2021 05:41:50 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 03 Sep 2021 05:41:51 GMT
ENV PHP_VERSION=8.0.10
# Fri, 03 Sep 2021 05:41:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.10.tar.xz.asc
# Fri, 03 Sep 2021 05:41:51 GMT
ENV PHP_SHA256=66dc4d1bc86d9c1bc255b51b79d337ed1a7a035cf71230daabbf9a4ca35795eb
# Fri, 03 Sep 2021 05:42:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 03 Sep 2021 05:42:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 03 Sep 2021 05:54:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 03 Sep 2021 05:54:36 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Fri, 03 Sep 2021 05:54:38 GMT
RUN docker-php-ext-enable sodium
# Fri, 03 Sep 2021 05:54:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 03 Sep 2021 05:54:39 GMT
STOPSIGNAL SIGWINCH
# Fri, 03 Sep 2021 05:54:39 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 03 Sep 2021 05:54:40 GMT
WORKDIR /var/www/html
# Fri, 03 Sep 2021 05:54:40 GMT
EXPOSE 80
# Fri, 03 Sep 2021 05:54:40 GMT
CMD ["apache2-foreground"]
# Tue, 07 Sep 2021 21:18:25 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 07 Sep 2021 21:18:26 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 07 Sep 2021 21:18:28 GMT
RUN a2enmod rewrite
# Tue, 07 Sep 2021 21:23:13 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libjpeg-dev 		libldap2-dev 		libmcrypt-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-jpeg; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		gmp 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.20; 	pecl install memcached-3.1.5; 	pecl install redis-5.3.4; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Sep 2021 21:23:13 GMT
VOLUME [/var/www/html]
# Wed, 15 Sep 2021 00:13:42 GMT
ENV JOOMLA_VERSION=4.0.3
# Wed, 15 Sep 2021 00:13:42 GMT
ENV JOOMLA_SHA512=9c09a621586fdcc30351a915f283581c92080c210294cacc50e0e390d991f32bee9d61dfc7b0af33c81118e46d775152159c0e27dbf73f5531512328d716901f
# Wed, 15 Sep 2021 00:14:03 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Wed, 15 Sep 2021 00:14:04 GMT
COPY file:f6b7a1c96cc89593a2b9ce4c68af350ae02f2e0c654cd5e842ff6c03641d470e in /entrypoint.sh 
# Wed, 15 Sep 2021 00:14:05 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Wed, 15 Sep 2021 00:14:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Sep 2021 00:14:05 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2320664dc3760d5d905a15eef2bf52da0cbab097fb4fc626c1f96722a2e2188c`  
		Last Modified: Fri, 03 Sep 2021 01:18:25 GMT  
		Size: 29.6 MB (29627416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dddeccc4720571d71483acc1182db8d8d63700ae941f845925a5b89fd4c8d0c1`  
		Last Modified: Fri, 03 Sep 2021 10:15:51 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de30247ef2b7e693655ed84e97a561f010f2592c6d840d45b089364cdc378018`  
		Last Modified: Fri, 03 Sep 2021 10:16:49 GMT  
		Size: 72.0 MB (72015443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c033f72181f7975d86559a816eb9cc3b8c318726580c6f4e44bdefce9908fe2c`  
		Last Modified: Fri, 03 Sep 2021 10:15:51 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fc21b8be2bf343cf28c6b39fbcea896dd86356e4a0bcb3f7e9d32d537bfac3`  
		Last Modified: Fri, 03 Sep 2021 10:18:25 GMT  
		Size: 19.1 MB (19128878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45aa794ced987a13961e7ce0618a1d241c4dc8f8ca673675fd123265f4c1de9`  
		Last Modified: Fri, 03 Sep 2021 10:18:01 GMT  
		Size: 434.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b095b243e27ec8c11edac04a53c8c4866997e1d4093d2caff14e41ec041486c8`  
		Last Modified: Fri, 03 Sep 2021 10:18:01 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2ca6c85c4ad605f3e97036089e096d006ebbd8b5b2d4a90a7b589448c08ea0`  
		Last Modified: Fri, 03 Sep 2021 10:24:26 GMT  
		Size: 11.0 MB (11041897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5962138ded9edb39577fbe5d9342ce09edf82d2ccffe8482c546ae063c6c0e20`  
		Last Modified: Fri, 03 Sep 2021 10:24:21 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ba9b4bf603d82fd6ae5846d2b556941ccfda1dbe7c6856b8831c6c1be5873c`  
		Last Modified: Fri, 03 Sep 2021 10:24:34 GMT  
		Size: 13.9 MB (13904228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae399c079550eb69a319a70cb897ca050c5ec780dbd1a0c15e489a98889bb394`  
		Last Modified: Fri, 03 Sep 2021 10:24:21 GMT  
		Size: 2.3 KB (2276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29042c9432e9a7ced0398edaf50b953586837fea91b02dc04633910655b38b1`  
		Last Modified: Fri, 03 Sep 2021 10:24:21 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e3761d384c50f7bb26ed15a08c7b8d73fca6995dec06c0fae5838cb13becb7`  
		Last Modified: Fri, 03 Sep 2021 10:24:22 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0c554958a8ffabf434c0ffaf5f3805491d0473ce712d68d9e05868f017f8e5`  
		Last Modified: Tue, 07 Sep 2021 21:42:25 GMT  
		Size: 313.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b229d97cec3dd5ab326965929b52041857b7a220c5a6043cae8facba9affaab`  
		Last Modified: Tue, 07 Sep 2021 21:42:28 GMT  
		Size: 2.9 MB (2900398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e9f6776a6ede97e81edd9a9d9468e420e8a9a61f226ac320b92ae11643f9a2`  
		Last Modified: Wed, 15 Sep 2021 00:18:11 GMT  
		Size: 21.3 MB (21324818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c0c1766791f92aa7d85e43a09b5e3615f65f4aec8ff69d1c7756760033f8273`  
		Last Modified: Wed, 15 Sep 2021 00:17:54 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed16fc7f1b6c0c31dce95d0ecbd03d05eb8b8f21fd4ba5daf1ce27ecf2df8b6`  
		Last Modified: Wed, 15 Sep 2021 00:17:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php8.0` - linux; ppc64le

```console
$ docker pull joomla@sha256:b75012f495392424c351831bde29724cc88f650d56b5c33cd457cd21f31d1b77
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193570644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2b831cc996f452adc57f8658947cabfebe2d8e6b7f542b384308c83a7f1862`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 03 Sep 2021 01:23:11 GMT
ADD file:71b4f3130e43c12907b826b33d9869308eec40607243a12d904fe47311431db9 in / 
# Fri, 03 Sep 2021 01:23:21 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 11:39:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 03 Sep 2021 11:39:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 03 Sep 2021 11:41:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 11:41:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 03 Sep 2021 11:41:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 03 Sep 2021 11:48:52 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 03 Sep 2021 11:48:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 03 Sep 2021 11:50:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 03 Sep 2021 11:50:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 03 Sep 2021 11:50:45 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 03 Sep 2021 11:50:47 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 03 Sep 2021 11:50:49 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 03 Sep 2021 11:50:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 03 Sep 2021 11:50:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 03 Sep 2021 11:51:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 03 Sep 2021 13:02:32 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 03 Sep 2021 13:02:37 GMT
ENV PHP_VERSION=8.0.10
# Fri, 03 Sep 2021 13:02:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.10.tar.xz.asc
# Fri, 03 Sep 2021 13:02:45 GMT
ENV PHP_SHA256=66dc4d1bc86d9c1bc255b51b79d337ed1a7a035cf71230daabbf9a4ca35795eb
# Fri, 03 Sep 2021 13:03:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 03 Sep 2021 13:03:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 03 Sep 2021 13:09:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 03 Sep 2021 13:09:59 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Fri, 03 Sep 2021 13:10:08 GMT
RUN docker-php-ext-enable sodium
# Fri, 03 Sep 2021 13:10:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 03 Sep 2021 13:10:12 GMT
STOPSIGNAL SIGWINCH
# Fri, 03 Sep 2021 13:10:14 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 03 Sep 2021 13:10:19 GMT
WORKDIR /var/www/html
# Fri, 03 Sep 2021 13:10:21 GMT
EXPOSE 80
# Fri, 03 Sep 2021 13:10:24 GMT
CMD ["apache2-foreground"]
# Tue, 07 Sep 2021 21:48:23 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 07 Sep 2021 21:48:26 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 07 Sep 2021 21:48:31 GMT
RUN a2enmod rewrite
# Tue, 07 Sep 2021 21:51:37 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libjpeg-dev 		libldap2-dev 		libmcrypt-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-jpeg; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		gmp 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.20; 	pecl install memcached-3.1.5; 	pecl install redis-5.3.4; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Sep 2021 21:51:42 GMT
VOLUME [/var/www/html]
# Wed, 15 Sep 2021 00:55:01 GMT
ENV JOOMLA_VERSION=4.0.3
# Wed, 15 Sep 2021 00:55:07 GMT
ENV JOOMLA_SHA512=9c09a621586fdcc30351a915f283581c92080c210294cacc50e0e390d991f32bee9d61dfc7b0af33c81118e46d775152159c0e27dbf73f5531512328d716901f
# Wed, 15 Sep 2021 00:55:31 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Wed, 15 Sep 2021 00:55:37 GMT
COPY file:f6b7a1c96cc89593a2b9ce4c68af350ae02f2e0c654cd5e842ff6c03641d470e in /entrypoint.sh 
# Wed, 15 Sep 2021 00:55:38 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Wed, 15 Sep 2021 00:55:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Sep 2021 00:55:46 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:be889fbf38c25cf263aa8d8c960d58470da7f841ab3f4949b8a1ac5c4514956c`  
		Last Modified: Fri, 03 Sep 2021 01:36:58 GMT  
		Size: 35.3 MB (35272405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9a3a7bdcc5e09f63ea4a3f403c5fb0ff46b25c93859d06be80f380cc83f690`  
		Last Modified: Fri, 03 Sep 2021 16:22:29 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f7118b88826130f05a6867f42c170ffda007d7dbd24545309b1d22a2452632`  
		Last Modified: Fri, 03 Sep 2021 16:24:04 GMT  
		Size: 86.6 MB (86624386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2e3e6d795b768e15a082582e865400aed1c0ba996a28958ef763ef6cda0b48`  
		Last Modified: Fri, 03 Sep 2021 16:22:28 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:701c58090211df6b0082d5e7e34fae73eb5f7bfea764546e2613de10272bbea1`  
		Last Modified: Fri, 03 Sep 2021 16:24:58 GMT  
		Size: 20.4 MB (20434425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b0d870f802094ece7b498296f6a897fbd7a362c0fb37bc4271e593e09265f6`  
		Last Modified: Fri, 03 Sep 2021 16:24:42 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3424b9768c349a096fdd808ea455b7aee6575558e5083932694ec06fd820f99c`  
		Last Modified: Fri, 03 Sep 2021 16:24:41 GMT  
		Size: 521.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30166637acf5728f6183af16791b1701c3aa3a237f931fcb2c33be3120f28e33`  
		Last Modified: Fri, 03 Sep 2021 16:31:33 GMT  
		Size: 11.0 MB (11044529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86bc20b38468d5495c1962974a02c9c3ce48d69d18cf0b3da5949d9d66cc1ef3`  
		Last Modified: Fri, 03 Sep 2021 16:31:28 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1031dd63cd1d4510ecf31a832e041fb6e05306a0fa952bf6cc0a0cf4d2cf2683`  
		Last Modified: Fri, 03 Sep 2021 16:31:48 GMT  
		Size: 15.7 MB (15694718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a996abc146dc4eeed482342b8ad5445a66d9033b262ad89305ee664bb66f000b`  
		Last Modified: Fri, 03 Sep 2021 16:31:29 GMT  
		Size: 2.3 KB (2274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95746b630ea0f0a5c5547c6c1f47b079d731d8574faba430f7f4036588871f4`  
		Last Modified: Fri, 03 Sep 2021 16:31:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bc798da9072b2202783e0574debb8b86e2dbc2014ed971ce0ab9d4241a9322`  
		Last Modified: Fri, 03 Sep 2021 16:31:28 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0c892356b4784a2687cef21238cb2dd75958e1b58559773e7efd2a6265cb84`  
		Last Modified: Tue, 07 Sep 2021 22:22:26 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc98517c89ae04639bc99cdd42828514e93ebb18e24178106bdf89ce394cbef5`  
		Last Modified: Tue, 07 Sep 2021 22:22:27 GMT  
		Size: 3.2 MB (3168181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5175c96c388f316ae82b4014266419a5f19a17ff8f9d8dbf1c9795c8b6cdb8`  
		Last Modified: Wed, 15 Sep 2021 01:09:34 GMT  
		Size: 21.3 MB (21324477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9734b108a2a594e59ced6e2e1775288d8418fba824d1aa75493252097120205a`  
		Last Modified: Wed, 15 Sep 2021 01:09:30 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d780227d5f1374ad766d5dc52adf46e4e0b2efa8b360e3c6c43f390eef993138`  
		Last Modified: Wed, 15 Sep 2021 01:09:30 GMT  
		Size: 613.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php8.0` - linux; s390x

```console
$ docker pull joomla@sha256:0ea8b33907baaaaa7c551e0ec623661c5bce58ad76c9db9710ae8963b08bc645
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169490901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbe705a834483b13030862303b4146d52f18ce8862ded2aeede50b2be4cf3827`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 03 Sep 2021 00:43:48 GMT
ADD file:9e72d98b2c920e433c6b776ed8eaf6a90cbf367d0ee37a8461d191499be72d39 in / 
# Fri, 03 Sep 2021 00:43:52 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:48:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 03 Sep 2021 08:48:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 03 Sep 2021 08:49:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 08:49:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 03 Sep 2021 08:49:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 03 Sep 2021 08:56:49 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 03 Sep 2021 08:56:50 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 03 Sep 2021 08:57:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 03 Sep 2021 08:57:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 03 Sep 2021 08:57:19 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 03 Sep 2021 08:57:19 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 03 Sep 2021 08:57:20 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 03 Sep 2021 08:57:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 03 Sep 2021 08:57:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 03 Sep 2021 08:57:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 03 Sep 2021 09:52:15 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 03 Sep 2021 09:52:15 GMT
ENV PHP_VERSION=8.0.10
# Fri, 03 Sep 2021 09:52:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.10.tar.xz.asc
# Fri, 03 Sep 2021 09:52:16 GMT
ENV PHP_SHA256=66dc4d1bc86d9c1bc255b51b79d337ed1a7a035cf71230daabbf9a4ca35795eb
# Fri, 03 Sep 2021 09:52:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 03 Sep 2021 09:52:39 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 03 Sep 2021 09:59:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 03 Sep 2021 09:59:14 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Fri, 03 Sep 2021 09:59:15 GMT
RUN docker-php-ext-enable sodium
# Fri, 03 Sep 2021 09:59:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 03 Sep 2021 09:59:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 03 Sep 2021 09:59:17 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 03 Sep 2021 09:59:17 GMT
WORKDIR /var/www/html
# Fri, 03 Sep 2021 09:59:18 GMT
EXPOSE 80
# Fri, 03 Sep 2021 09:59:19 GMT
CMD ["apache2-foreground"]
# Tue, 07 Sep 2021 21:00:32 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 07 Sep 2021 21:00:33 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 07 Sep 2021 21:00:34 GMT
RUN a2enmod rewrite
# Tue, 07 Sep 2021 21:02:53 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libjpeg-dev 		libldap2-dev 		libmcrypt-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-jpeg; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		gmp 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.20; 	pecl install memcached-3.1.5; 	pecl install redis-5.3.4; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Sep 2021 21:02:54 GMT
VOLUME [/var/www/html]
# Tue, 14 Sep 2021 23:50:35 GMT
ENV JOOMLA_VERSION=4.0.3
# Tue, 14 Sep 2021 23:50:35 GMT
ENV JOOMLA_SHA512=9c09a621586fdcc30351a915f283581c92080c210294cacc50e0e390d991f32bee9d61dfc7b0af33c81118e46d775152159c0e27dbf73f5531512328d716901f
# Tue, 14 Sep 2021 23:50:41 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Tue, 14 Sep 2021 23:50:42 GMT
COPY file:f6b7a1c96cc89593a2b9ce4c68af350ae02f2e0c654cd5e842ff6c03641d470e in /entrypoint.sh 
# Tue, 14 Sep 2021 23:50:43 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Tue, 14 Sep 2021 23:50:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Sep 2021 23:50:43 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:33fe066e16e87fca4bcb280b7ec53d44c561299928e592068e985314cf93215b`  
		Last Modified: Fri, 03 Sep 2021 00:52:58 GMT  
		Size: 29.7 MB (29650625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21b1207f1fa6570c494278708a52572e3410b6d2caf07d5244ed0ad1f512fb2`  
		Last Modified: Fri, 03 Sep 2021 12:42:23 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef466ee241a5736fb11f7726cedd6a92f4e9f15aef11e248f0439bda0788d1a2`  
		Last Modified: Fri, 03 Sep 2021 12:42:34 GMT  
		Size: 71.6 MB (71623349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d36fd8ed70be33246601a1fcda01906ff1efb2a19145f86f9c04af5627c831`  
		Last Modified: Fri, 03 Sep 2021 12:42:22 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cad3a25346451506f9ade60d22975759e2bc7d58da3eae35a12887e06ce2f0`  
		Last Modified: Fri, 03 Sep 2021 12:43:04 GMT  
		Size: 19.0 MB (19026546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707de03a4ae6e3095f0333b0322ebe2eab87d14b42f17c64f1b44a99aed9fa60`  
		Last Modified: Fri, 03 Sep 2021 12:43:01 GMT  
		Size: 482.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7359018f2f26d60edb4812839bfafde0d251db93c6916aa730cb5be3c7da85`  
		Last Modified: Fri, 03 Sep 2021 12:43:01 GMT  
		Size: 516.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c495d98ad1bf96ee0676b7e3f67d8723876229fb9a052ba761e76f1709818595`  
		Last Modified: Fri, 03 Sep 2021 12:46:24 GMT  
		Size: 11.0 MB (11043176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9deadf2fda7805be8824e0fdc47e868226ddeaae9d3ba97cb0142589f821102e`  
		Last Modified: Fri, 03 Sep 2021 12:46:22 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9af073428d54ae626aeb974ffd151b19f489da86e741c627418e05b828e0b09`  
		Last Modified: Fri, 03 Sep 2021 12:46:24 GMT  
		Size: 13.9 MB (13892481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbb412a76a7e1eaf934655465802fba68c222fac494710b5ba1ea42e134d430`  
		Last Modified: Fri, 03 Sep 2021 12:46:22 GMT  
		Size: 2.3 KB (2275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6156f3a5bc8eb266be5b2bfe5e14483a2bcb5ee24c51590be2ccc50ca2e35364`  
		Last Modified: Fri, 03 Sep 2021 12:46:22 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cede703c0e8be522cff4bb329b2539ad1ca5a960bc1dc8b77a7b9c875a505d66`  
		Last Modified: Fri, 03 Sep 2021 12:46:22 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0df9debfd13d70266ff36eb381cde64ba2d7c15a887d272d40519d488a4c9fb`  
		Last Modified: Tue, 07 Sep 2021 21:21:43 GMT  
		Size: 318.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911101dcc9925b5910c8bd25d7278d7cf009c6a2c32c13ea9747112f898d5748`  
		Last Modified: Tue, 07 Sep 2021 21:21:44 GMT  
		Size: 2.9 MB (2922745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d01b7906c7c916ad00a630b7a2b3a7df63b3b86460976ac4b12e599d837b677a`  
		Last Modified: Tue, 14 Sep 2021 23:55:34 GMT  
		Size: 21.3 MB (21324455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8181fc8b3e54928a42c3051764845fd073ef99f723b4bf736bd51a48678f7acf`  
		Last Modified: Tue, 14 Sep 2021 23:55:32 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff27f030856af74988f2671b4274a647205032feba5ca3a2ccd33e2b25cfcb4`  
		Last Modified: Tue, 14 Sep 2021 23:55:31 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
