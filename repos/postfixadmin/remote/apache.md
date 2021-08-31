## `postfixadmin:apache`

```console
$ docker pull postfixadmin@sha256:69473273695a6a824b7c27d2e35ffdb1268fef41664e6d3e0891545312a72639
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

### `postfixadmin:apache` - linux; amd64

```console
$ docker pull postfixadmin@sha256:7b9cd6c8f2efd54af05d4958eeb2b64e6d22d861dd128a765166d2a1509cc23e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173346115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef339cad8522529faa14fdb260676e83b6fbc5390861687d050a3d161c1251b3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:40 GMT
ADD file:5e8343ab9a73edc27c2889634896e792ab289b85c206de0fc31183fdc0a32ac7 in / 
# Tue, 17 Aug 2021 01:23:41 GMT
CMD ["bash"]
# Wed, 18 Aug 2021 12:27:35 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 18 Aug 2021 12:27:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 18 Aug 2021 12:27:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 12:27:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 18 Aug 2021 12:27:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 18 Aug 2021 12:33:01 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 18 Aug 2021 12:33:02 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 18 Aug 2021 12:33:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 18 Aug 2021 12:33:11 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 18 Aug 2021 12:33:12 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 18 Aug 2021 12:33:12 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Wed, 18 Aug 2021 12:33:12 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Wed, 18 Aug 2021 12:33:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 18 Aug 2021 12:33:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 18 Aug 2021 12:33:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 18 Aug 2021 13:13:01 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Aug 2021 23:31:41 GMT
ENV PHP_VERSION=7.4.23
# Thu, 26 Aug 2021 23:31:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.23.tar.xz.asc
# Thu, 26 Aug 2021 23:31:42 GMT
ENV PHP_SHA256=cea52313fcffe56343bcd3c66dbb23cd5507dc559cc2e3547cf8f5452e88a05d
# Thu, 26 Aug 2021 23:31:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 26 Aug 2021 23:32:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Aug 2021 23:38:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 26 Aug 2021 23:38:02 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Thu, 26 Aug 2021 23:38:04 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Aug 2021 23:38:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Aug 2021 23:38:04 GMT
STOPSIGNAL SIGWINCH
# Thu, 26 Aug 2021 23:38:05 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 26 Aug 2021 23:38:05 GMT
WORKDIR /var/www/html
# Thu, 26 Aug 2021 23:38:06 GMT
EXPOSE 80
# Thu, 26 Aug 2021 23:38:06 GMT
CMD ["apache2-foreground"]
# Fri, 27 Aug 2021 06:40:40 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 27 Aug 2021 06:40:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Aug 2021 06:41:20 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Aug 2021 06:41:20 GMT
ARG POSTFIXADMIN_VERSION=3.3.10
# Mon, 30 Aug 2021 21:05:33 GMT
ARG POSTFIXADMIN_SHA512=e00fc9ea343a928976d191adfa01020ee0c6ddbe80a39e01ca2ee414a18247958f033970f378fe4a9974636172a5e094e57117ee9ac7b930c592f433097a7aca
# Mon, 30 Aug 2021 21:05:33 GMT
ENV POSTFIXADMIN_VERSION=3.3.10
# Mon, 30 Aug 2021 21:05:34 GMT
ENV POSTFIXADMIN_SHA512=e00fc9ea343a928976d191adfa01020ee0c6ddbe80a39e01ca2ee414a18247958f033970f378fe4a9974636172a5e094e57117ee9ac7b930c592f433097a7aca
# Mon, 30 Aug 2021 21:05:34 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Mon, 30 Aug 2021 21:05:35 GMT
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf
# Mon, 30 Aug 2021 21:05:37 GMT
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin
# Mon, 30 Aug 2021 21:05:38 GMT
COPY file:c9d831137af59b25a21b91306762892f72362178f6096a24bafecc047bbe6d37 in /usr/local/bin/ 
# Mon, 30 Aug 2021 21:05:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Mon, 30 Aug 2021 21:05:39 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:99046ad9247f8a1cbd1048d9099d026191ad9cda63c08aadeb704b7000a51717`  
		Last Modified: Tue, 17 Aug 2021 01:29:35 GMT  
		Size: 31.4 MB (31361314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3875fa64ab1e7ef45b19c31db513b33dd704aead9360fc096cbf4831311233d8`  
		Last Modified: Wed, 18 Aug 2021 13:46:40 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9329a8f553a5ecad9cc8380347dffa88323f980abc0b3698b7ab3ccf1f8c0dc`  
		Last Modified: Wed, 18 Aug 2021 13:46:54 GMT  
		Size: 91.6 MB (91606024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb327f9b0a4fafe951989e97bdefa22796c2829e0f0d668ff0638958d826f47`  
		Last Modified: Wed, 18 Aug 2021 13:46:40 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051b56f0e6a30e70de79489f2598c38b0aec3f1c71b234ea61143f56bd629877`  
		Last Modified: Wed, 18 Aug 2021 13:47:26 GMT  
		Size: 19.2 MB (19222921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da02d3111b48164dfee80bc29ab9b966cef46cc8ac9bf689e69a65445b7fa4a6`  
		Last Modified: Wed, 18 Aug 2021 13:47:23 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ca514d99e4fe525f869a88ca49847800a2aa9828b353aadebda54cf89cc19c`  
		Last Modified: Wed, 18 Aug 2021 13:47:22 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154679899a9908dd3a71fc39a066349e9b9d14c1593a47466ea0be063b3d977b`  
		Last Modified: Fri, 27 Aug 2021 03:23:30 GMT  
		Size: 10.7 MB (10710799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d349b281398af93636e4795b7061943e0b3d80b627ab118613362743c7c6cb6c`  
		Last Modified: Fri, 27 Aug 2021 03:23:26 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb54f7be0e41ad1fc2165c55ca126e44889983d50c5cd01eaad2ab061e1cc481`  
		Last Modified: Fri, 27 Aug 2021 03:23:30 GMT  
		Size: 16.1 MB (16078287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf4a9770fb49ee3ddb9cb6bc214240b4de7396c023f8a65e681ee04795d29db`  
		Last Modified: Fri, 27 Aug 2021 03:23:26 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3fc0948039d6e0cb1a092c7cd11a97875645f96327a4632c33631375cb932c`  
		Last Modified: Fri, 27 Aug 2021 03:23:26 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a301421a94086364628b3d70b3a0a65edd0ed2b4097c443175d4da1097116074`  
		Last Modified: Fri, 27 Aug 2021 03:23:26 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97893ec9a57731582338934626fe82360ba52d290fa4a675a2cc0e63cd834eac`  
		Last Modified: Mon, 30 Aug 2021 21:06:21 GMT  
		Size: 1.3 MB (1284032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4391e9c44216153aa106050347ec5d7a3d061845a60ed8a2c2d5a64356f675c9`  
		Last Modified: Mon, 30 Aug 2021 21:06:21 GMT  
		Size: 1.2 MB (1202708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33c816e72594bd91b87e46a09cbcb2b29b11a01e78388a621e59d0c316b3947`  
		Last Modified: Mon, 30 Aug 2021 21:06:21 GMT  
		Size: 8.2 KB (8223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc4c60fb897a7f429fb2a172a2856d6ad2e298deb1d2821d2187f36ea0ccd29`  
		Last Modified: Mon, 30 Aug 2021 21:06:21 GMT  
		Size: 1.9 MB (1864810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e3ed5afc9ef8c2992b9fd86a77808b281e0fc50ed239cc58bcf357fcc69a64`  
		Last Modified: Mon, 30 Aug 2021 21:06:21 GMT  
		Size: 1.6 KB (1599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postfixadmin:apache` - linux; arm variant v5

```console
$ docker pull postfixadmin@sha256:1a460e41a0b95d53db1afea70e84bc91efb039ae77de633be80b9a1cc638146e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (150955472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b89987b6303880f507a56e1030cf8ad92182efb5426fb597727796fcd7f82205`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 17 Aug 2021 01:55:48 GMT
ADD file:9ab41fbe9b84c147eb71d451b4d31f27a0eb362bb6d14ee3ba6279d67ae25531 in / 
# Tue, 17 Aug 2021 01:55:49 GMT
CMD ["bash"]
# Wed, 18 Aug 2021 08:33:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 18 Aug 2021 08:33:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 18 Aug 2021 08:34:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 08:34:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 18 Aug 2021 08:34:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 18 Aug 2021 08:40:08 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 18 Aug 2021 08:40:09 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 18 Aug 2021 08:40:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 18 Aug 2021 08:40:36 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 18 Aug 2021 08:40:38 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 18 Aug 2021 08:40:38 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Wed, 18 Aug 2021 08:40:39 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Wed, 18 Aug 2021 08:40:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 18 Aug 2021 08:40:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 18 Aug 2021 08:40:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 18 Aug 2021 09:25:44 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Aug 2021 21:10:06 GMT
ENV PHP_VERSION=7.4.23
# Thu, 26 Aug 2021 21:10:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.23.tar.xz.asc
# Thu, 26 Aug 2021 21:10:07 GMT
ENV PHP_SHA256=cea52313fcffe56343bcd3c66dbb23cd5507dc559cc2e3547cf8f5452e88a05d
# Thu, 26 Aug 2021 21:10:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 26 Aug 2021 21:10:31 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Aug 2021 21:14:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 26 Aug 2021 21:14:38 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Thu, 26 Aug 2021 21:14:39 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Aug 2021 21:14:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Aug 2021 21:14:40 GMT
STOPSIGNAL SIGWINCH
# Thu, 26 Aug 2021 21:14:40 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 26 Aug 2021 21:14:41 GMT
WORKDIR /var/www/html
# Thu, 26 Aug 2021 21:14:41 GMT
EXPOSE 80
# Thu, 26 Aug 2021 21:14:42 GMT
CMD ["apache2-foreground"]
# Fri, 27 Aug 2021 02:57:55 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 27 Aug 2021 02:58:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Aug 2021 02:59:59 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Aug 2021 02:59:59 GMT
ARG POSTFIXADMIN_VERSION=3.3.10
# Mon, 30 Aug 2021 22:45:58 GMT
ARG POSTFIXADMIN_SHA512=e00fc9ea343a928976d191adfa01020ee0c6ddbe80a39e01ca2ee414a18247958f033970f378fe4a9974636172a5e094e57117ee9ac7b930c592f433097a7aca
# Mon, 30 Aug 2021 22:45:59 GMT
ENV POSTFIXADMIN_VERSION=3.3.10
# Mon, 30 Aug 2021 22:45:59 GMT
ENV POSTFIXADMIN_SHA512=e00fc9ea343a928976d191adfa01020ee0c6ddbe80a39e01ca2ee414a18247958f033970f378fe4a9974636172a5e094e57117ee9ac7b930c592f433097a7aca
# Mon, 30 Aug 2021 22:46:00 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Mon, 30 Aug 2021 22:46:01 GMT
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf
# Mon, 30 Aug 2021 22:46:05 GMT
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin
# Mon, 30 Aug 2021 22:46:05 GMT
COPY file:c9d831137af59b25a21b91306762892f72362178f6096a24bafecc047bbe6d37 in /usr/local/bin/ 
# Mon, 30 Aug 2021 22:46:06 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Mon, 30 Aug 2021 22:46:06 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:91b48139ec3e0280b0a9be84b502b3d6394149000106be38ac11a1c31b59d956`  
		Last Modified: Tue, 17 Aug 2021 02:11:08 GMT  
		Size: 28.9 MB (28904169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa2796fe1de11330173a65d9c79bd200115ed2bbe4a010226c01033778d8c3f`  
		Last Modified: Wed, 18 Aug 2021 10:15:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb10f22b0293b7ff792f98dc678a22c7b6f3eca97496bef4e50daece21e0ee80`  
		Last Modified: Wed, 18 Aug 2021 10:16:19 GMT  
		Size: 73.7 MB (73670748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ea0ba062254d8e5013c25abe70301cc348d021f0813a2d82181961a2b48c50`  
		Last Modified: Wed, 18 Aug 2021 10:15:31 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5008017b2ff93a998b2ed04b0d3cddabd0df1d59bee90c66e9ed6d6af66859`  
		Last Modified: Wed, 18 Aug 2021 10:17:17 GMT  
		Size: 18.5 MB (18523066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9adc384e97a58bed5588c04e8f1b38dda571fb3abd02f78859396a4f88d84af3`  
		Last Modified: Wed, 18 Aug 2021 10:17:06 GMT  
		Size: 484.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c856b3f94fae66ce8d19e9722a35d944808ee96f5532cfae449a690c448f2317`  
		Last Modified: Wed, 18 Aug 2021 10:17:05 GMT  
		Size: 520.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb916219860d2a4fa1548774d3755d5637766e944d47aea48113bda0eb6f3be`  
		Last Modified: Thu, 26 Aug 2021 22:59:36 GMT  
		Size: 10.7 MB (10709459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d9b5fd3a637bb34bacf63624c55e6a116716d1df74e22595582b4502f76378`  
		Last Modified: Thu, 26 Aug 2021 22:59:32 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78aff5db2afefe5763aa6d07415f4c3a9ba220d8458c50142e2a44af3924476f`  
		Last Modified: Thu, 26 Aug 2021 22:59:39 GMT  
		Size: 14.9 MB (14889600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cbab8b88c7346ede716f21daf75f10640b72c24cec8e00e6fa56573773b4a4`  
		Last Modified: Thu, 26 Aug 2021 22:59:32 GMT  
		Size: 2.3 KB (2275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95dc3ebc2ac831def0cd0187a6c9f8432eed3271784172f3aeb289f2e9a83d0`  
		Last Modified: Thu, 26 Aug 2021 22:59:32 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de3f11519e30503e33cc8393e02c4bce39f9adc9e182b31e70f4a861abab49a`  
		Last Modified: Thu, 26 Aug 2021 22:59:32 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c31279451b4442648b7c563ebf757f87371f472b3b6f779cc174073278de12d`  
		Last Modified: Mon, 30 Aug 2021 22:47:41 GMT  
		Size: 1.2 MB (1229998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe65eefa2ea29b4382ab1d46a0ed1b2e9538f70b755cd269829aff3422cc91e`  
		Last Modified: Mon, 30 Aug 2021 22:47:41 GMT  
		Size: 1.1 MB (1148371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ae9589f65ac9f10b5698732f9893bd7de943275d0cfbbd1b099d997a9c252e`  
		Last Modified: Mon, 30 Aug 2021 22:47:41 GMT  
		Size: 8.2 KB (8225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15102e73e181e2784347259b67a3c0f1d7f54622938ce06d2feaba7d4fb0d32b`  
		Last Modified: Mon, 30 Aug 2021 22:47:42 GMT  
		Size: 1.9 MB (1864834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0d3edffd45bd1cbf847cecca96b987af7d761213fd7dcc35a6e221d6b919e6`  
		Last Modified: Mon, 30 Aug 2021 22:47:41 GMT  
		Size: 1.6 KB (1595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postfixadmin:apache` - linux; arm variant v7

```console
$ docker pull postfixadmin@sha256:bef2acbf8bd7f3b5fecdd00f47b33b21f0a714d9260b047d00f43bff8fb5c7c7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.9 MB (142891875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92c67fafbc1791b1b4e1e00ccd14df4a3214b540a59806c664281e9f7bee8c83`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 17 Aug 2021 02:13:16 GMT
ADD file:56b22dfd365932a88a68ec72e6b9c1af8c5747606e0387a2c189dfb49998d029 in / 
# Tue, 17 Aug 2021 02:13:17 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 21:17:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 17 Aug 2021 21:17:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 17 Aug 2021 21:18:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 21:18:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 17 Aug 2021 21:18:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 17 Aug 2021 21:23:02 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 17 Aug 2021 21:23:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 17 Aug 2021 21:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 17 Aug 2021 21:23:26 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 17 Aug 2021 21:23:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 17 Aug 2021 21:23:29 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 17 Aug 2021 21:23:30 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 17 Aug 2021 21:23:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Aug 2021 21:23:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Aug 2021 21:23:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 17 Aug 2021 23:00:03 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Aug 2021 23:40:14 GMT
ENV PHP_VERSION=7.4.23
# Thu, 26 Aug 2021 23:40:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.23.tar.xz.asc
# Thu, 26 Aug 2021 23:40:15 GMT
ENV PHP_SHA256=cea52313fcffe56343bcd3c66dbb23cd5507dc559cc2e3547cf8f5452e88a05d
# Thu, 26 Aug 2021 23:40:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 26 Aug 2021 23:40:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Aug 2021 23:44:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 26 Aug 2021 23:44:30 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Thu, 26 Aug 2021 23:44:32 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Aug 2021 23:44:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Aug 2021 23:44:33 GMT
STOPSIGNAL SIGWINCH
# Thu, 26 Aug 2021 23:44:33 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 26 Aug 2021 23:44:34 GMT
WORKDIR /var/www/html
# Thu, 26 Aug 2021 23:44:34 GMT
EXPOSE 80
# Thu, 26 Aug 2021 23:44:35 GMT
CMD ["apache2-foreground"]
# Fri, 27 Aug 2021 08:14:04 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 27 Aug 2021 08:14:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Aug 2021 08:15:54 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Aug 2021 08:15:54 GMT
ARG POSTFIXADMIN_VERSION=3.3.10
# Mon, 30 Aug 2021 22:50:21 GMT
ARG POSTFIXADMIN_SHA512=e00fc9ea343a928976d191adfa01020ee0c6ddbe80a39e01ca2ee414a18247958f033970f378fe4a9974636172a5e094e57117ee9ac7b930c592f433097a7aca
# Mon, 30 Aug 2021 22:50:21 GMT
ENV POSTFIXADMIN_VERSION=3.3.10
# Mon, 30 Aug 2021 22:50:22 GMT
ENV POSTFIXADMIN_SHA512=e00fc9ea343a928976d191adfa01020ee0c6ddbe80a39e01ca2ee414a18247958f033970f378fe4a9974636172a5e094e57117ee9ac7b930c592f433097a7aca
# Mon, 30 Aug 2021 22:50:22 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Mon, 30 Aug 2021 22:50:24 GMT
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf
# Mon, 30 Aug 2021 22:50:27 GMT
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin
# Mon, 30 Aug 2021 22:50:28 GMT
COPY file:c9d831137af59b25a21b91306762892f72362178f6096a24bafecc047bbe6d37 in /usr/local/bin/ 
# Mon, 30 Aug 2021 22:50:28 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Mon, 30 Aug 2021 22:50:29 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:118503c5404bba02cc6a70fd0b808c846fefe8a3435d831a37127a6fdc8f96a2`  
		Last Modified: Tue, 17 Aug 2021 02:29:31 GMT  
		Size: 26.6 MB (26565574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d84c83978f44f440f81f956fac272ee98a3cd74166cc89ef7ac7f534d15682`  
		Last Modified: Wed, 18 Aug 2021 00:40:19 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f34933fd332e7bec34679975d5ab1632938c0abd22fbaf48d9a1cb3f3d9827`  
		Last Modified: Wed, 18 Aug 2021 00:40:55 GMT  
		Size: 69.3 MB (69315491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1387c6ef22f878c363686effb2c485e787daafa38553bd5e0cdb240f2bc1c679`  
		Last Modified: Wed, 18 Aug 2021 00:40:16 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3df6620f0dccd8ea3174fc34554c212088a4beeaae99870e8736ec946f59de`  
		Last Modified: Wed, 18 Aug 2021 00:41:45 GMT  
		Size: 18.0 MB (17974877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfce6eae7ad9a1af21d8606beccafad08c9645328b0178837349bb8b676a2ffb`  
		Last Modified: Wed, 18 Aug 2021 00:41:35 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e753dd3f6b4dc1c40759b429fbb57f3ec6789b682f6bccf4e19d98253df6a1c9`  
		Last Modified: Wed, 18 Aug 2021 00:41:35 GMT  
		Size: 516.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d463afbaebc6349441e4e99e4eca27997b5964be0207615d541dfca943621c70`  
		Last Modified: Fri, 27 Aug 2021 02:33:38 GMT  
		Size: 10.7 MB (10709541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5803f43350027931019048b400ed3fa98f227792d86f0b64118cc7d9875f34f5`  
		Last Modified: Fri, 27 Aug 2021 02:33:32 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e181dd9f6c4944302d66f2999562e8febbad4e38e0d1d25a2c34b12b8ab4930a`  
		Last Modified: Fri, 27 Aug 2021 02:33:42 GMT  
		Size: 14.1 MB (14123005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f6744f36d7a729eb844666bbf71213c63ef2ffa384fa7e8636f9b14ecdc8ba`  
		Last Modified: Fri, 27 Aug 2021 02:33:33 GMT  
		Size: 2.3 KB (2278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b58d67fd4eefa0f70622622b6687b63956db86b27fe8d87ec85f506f4c8b2f`  
		Last Modified: Fri, 27 Aug 2021 02:33:32 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1a3149c1937cc00cd43b1fbad2839a58722185a7296f1d5dc45801970bb75f`  
		Last Modified: Fri, 27 Aug 2021 02:33:32 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943044a5c58c309127fe40f4b6662b8fd98d6b5e6328dcb20e257e54cedaf1b2`  
		Last Modified: Mon, 30 Aug 2021 22:52:36 GMT  
		Size: 1.2 MB (1224467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60a2c6fe5d0dfd3fc303eb2079acbb27bad6e70d33396a4466bbf22d2e253ba`  
		Last Modified: Mon, 30 Aug 2021 22:52:36 GMT  
		Size: 1.1 MB (1098861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ecfc180189edf610f864f56fdab04cc7a893105dc55a4716a5c2ffff151379d`  
		Last Modified: Mon, 30 Aug 2021 22:52:35 GMT  
		Size: 8.2 KB (8222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62762f5d8e9e861cf9ba6d3f926e98106ddd62831a22c490cd2ec37126ad0de`  
		Last Modified: Mon, 30 Aug 2021 22:52:37 GMT  
		Size: 1.9 MB (1864835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271942b56a518245e67292d5820f41ec40bb30c24e1017dabf6279528389641c`  
		Last Modified: Mon, 30 Aug 2021 22:52:36 GMT  
		Size: 1.6 KB (1596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postfixadmin:apache` - linux; arm64 variant v8

```console
$ docker pull postfixadmin@sha256:1f6130858ad64def433d5e827d25c9f5673830098bab3a162563b1941e7a3bf1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166732693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d424bae57f6bd060c89259ee63cb2561d81eefcb953b7b00a6d907e580c36b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:04 GMT
ADD file:0a42d4a201f0ac7889187c3212fbdfc2747f31f36e690d59c22eec50fe542614 in / 
# Tue, 17 Aug 2021 01:46:05 GMT
CMD ["bash"]
# Wed, 18 Aug 2021 08:36:51 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 18 Aug 2021 08:36:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 18 Aug 2021 08:37:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 08:37:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 18 Aug 2021 08:37:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 18 Aug 2021 08:44:53 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 18 Aug 2021 08:44:53 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 18 Aug 2021 08:45:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 18 Aug 2021 08:45:01 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 18 Aug 2021 08:45:02 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 18 Aug 2021 08:45:02 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Wed, 18 Aug 2021 08:45:02 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Wed, 18 Aug 2021 08:45:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 18 Aug 2021 08:45:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 18 Aug 2021 08:45:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 18 Aug 2021 09:22:46 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 27 Aug 2021 00:37:43 GMT
ENV PHP_VERSION=7.4.23
# Fri, 27 Aug 2021 00:37:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.23.tar.xz.asc
# Fri, 27 Aug 2021 00:37:43 GMT
ENV PHP_SHA256=cea52313fcffe56343bcd3c66dbb23cd5507dc559cc2e3547cf8f5452e88a05d
# Fri, 27 Aug 2021 00:38:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 27 Aug 2021 00:38:02 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Aug 2021 00:40:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Aug 2021 00:40:09 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Fri, 27 Aug 2021 00:40:10 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Aug 2021 00:40:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Aug 2021 00:40:10 GMT
STOPSIGNAL SIGWINCH
# Fri, 27 Aug 2021 00:40:10 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 27 Aug 2021 00:40:10 GMT
WORKDIR /var/www/html
# Fri, 27 Aug 2021 00:40:11 GMT
EXPOSE 80
# Fri, 27 Aug 2021 00:40:11 GMT
CMD ["apache2-foreground"]
# Fri, 27 Aug 2021 06:30:35 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 27 Aug 2021 06:30:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Aug 2021 06:31:08 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Aug 2021 06:31:09 GMT
ARG POSTFIXADMIN_VERSION=3.3.10
# Mon, 30 Aug 2021 21:29:00 GMT
ARG POSTFIXADMIN_SHA512=e00fc9ea343a928976d191adfa01020ee0c6ddbe80a39e01ca2ee414a18247958f033970f378fe4a9974636172a5e094e57117ee9ac7b930c592f433097a7aca
# Mon, 30 Aug 2021 21:29:00 GMT
ENV POSTFIXADMIN_VERSION=3.3.10
# Mon, 30 Aug 2021 21:29:00 GMT
ENV POSTFIXADMIN_SHA512=e00fc9ea343a928976d191adfa01020ee0c6ddbe80a39e01ca2ee414a18247958f033970f378fe4a9974636172a5e094e57117ee9ac7b930c592f433097a7aca
# Mon, 30 Aug 2021 21:29:01 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Mon, 30 Aug 2021 21:29:01 GMT
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf
# Mon, 30 Aug 2021 21:29:03 GMT
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin
# Mon, 30 Aug 2021 21:29:03 GMT
COPY file:c9d831137af59b25a21b91306762892f72362178f6096a24bafecc047bbe6d37 in /usr/local/bin/ 
# Mon, 30 Aug 2021 21:29:03 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Mon, 30 Aug 2021 21:29:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3716b9f3c2f9e7592f5b47c2e6e13e64132071620c7551e0aa3c5c248e106139`  
		Last Modified: Tue, 17 Aug 2021 01:53:29 GMT  
		Size: 30.0 MB (30048801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d866415d3ee37964a1368090e3c4aa263a48fd0596d75470d756470d733cd00`  
		Last Modified: Wed, 18 Aug 2021 10:00:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb031746844ed5917dd3fa8bcff68ca0473331bbaec575ef0d3dff53734d697`  
		Last Modified: Wed, 18 Aug 2021 10:00:54 GMT  
		Size: 86.9 MB (86921080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea9475b4efc00fba612481a916aadd4bc40f01a083b01782899c9f7715ca7b6`  
		Last Modified: Wed, 18 Aug 2021 10:00:39 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767477a4f5e70bffb50c946aa1fc4197beaa701d16c3fef70875896d90af90ff`  
		Last Modified: Wed, 18 Aug 2021 10:01:35 GMT  
		Size: 19.1 MB (19140098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e70956f9cd7382de463766d83f66dc5e6e508007d5789d102844fd61c7bba2`  
		Last Modified: Wed, 18 Aug 2021 10:01:32 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b033e02310007952146912558e123a95d512137579f209dca9419885b3d9cc31`  
		Last Modified: Wed, 18 Aug 2021 10:01:32 GMT  
		Size: 514.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b575b7c591c41d47f09566f76aebe4ca43d4a86ebe4a455c2c22ac542b435c`  
		Last Modified: Fri, 27 Aug 2021 02:48:51 GMT  
		Size: 10.7 MB (10710114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48717a0d58f87cb7c82f4b7941ab2a34da4c152b146b70f3f3366c02f30b0daa`  
		Last Modified: Fri, 27 Aug 2021 02:48:48 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29a12252a663c238de6392ee3af1088b7f460df0e13b31e70c24254b4bf1a11`  
		Last Modified: Fri, 27 Aug 2021 02:48:51 GMT  
		Size: 15.6 MB (15631653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88968cab51b7fe59cda12bf174a29ba8b8700dcffa5dc8d28c79026925fa7ae0`  
		Last Modified: Fri, 27 Aug 2021 02:48:47 GMT  
		Size: 2.3 KB (2278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c093dd2ec5be69f85bb1695796563713700d185d5662ee4168100f88b381d8`  
		Last Modified: Fri, 27 Aug 2021 02:48:48 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fd34f61462f5def902ffd50476758e2133db8416029a36b434ed827a10ae89`  
		Last Modified: Fri, 27 Aug 2021 02:48:47 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7a91140cb0d5f614af898c75375451f8d9766e82f2d66dc366a7e4cd9e3ad6`  
		Last Modified: Mon, 30 Aug 2021 21:30:06 GMT  
		Size: 1.2 MB (1206008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246f189e1e94627056e7e3bccdf096b00d77a1d1924b1cda5a50608234c085d4`  
		Last Modified: Mon, 30 Aug 2021 21:30:06 GMT  
		Size: 1.2 MB (1194924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f69516151dad58c29840719b9f0a020180b1bf2c47e2fbfca87f6a02331725`  
		Last Modified: Mon, 30 Aug 2021 21:30:05 GMT  
		Size: 8.2 KB (8219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bdb300071456881584c43046e8028028f8c8fa9ddd57e12be571e9cbc791cb`  
		Last Modified: Mon, 30 Aug 2021 21:30:06 GMT  
		Size: 1.9 MB (1864811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9bad6764bc6597bcbaf1599ab66dc1ea042b41b5999387aff111ada64089f68`  
		Last Modified: Mon, 30 Aug 2021 21:30:06 GMT  
		Size: 1.6 KB (1594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postfixadmin:apache` - linux; 386

```console
$ docker pull postfixadmin@sha256:5848baccc1a820724c40bba06cb4c21672c66fe34a43225c1f78e956496b0d5e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176318290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ed19ca8043a732d80fa02bfc118653146d60dceecb0b2230ffb943fdb0598c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 17 Aug 2021 01:40:28 GMT
ADD file:9afc107c0880864c9f16852bb6cc272a068f2c82a2df7c3444bbbc533f377156 in / 
# Tue, 17 Aug 2021 01:40:29 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 21:52:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 17 Aug 2021 21:52:53 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 17 Aug 2021 21:53:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 21:53:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 17 Aug 2021 21:53:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 17 Aug 2021 22:02:38 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 17 Aug 2021 22:02:38 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 17 Aug 2021 22:02:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 17 Aug 2021 22:02:58 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 17 Aug 2021 22:03:00 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 17 Aug 2021 22:03:01 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 17 Aug 2021 22:03:02 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 17 Aug 2021 22:03:02 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Aug 2021 22:03:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Aug 2021 22:03:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 17 Aug 2021 23:17:58 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Aug 2021 23:45:45 GMT
ENV PHP_VERSION=7.4.23
# Thu, 26 Aug 2021 23:45:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.23.tar.xz.asc
# Thu, 26 Aug 2021 23:45:46 GMT
ENV PHP_SHA256=cea52313fcffe56343bcd3c66dbb23cd5507dc559cc2e3547cf8f5452e88a05d
# Thu, 26 Aug 2021 23:46:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 26 Aug 2021 23:46:04 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Aug 2021 23:51:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 26 Aug 2021 23:51:30 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Thu, 26 Aug 2021 23:51:31 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Aug 2021 23:51:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Aug 2021 23:51:31 GMT
STOPSIGNAL SIGWINCH
# Thu, 26 Aug 2021 23:51:32 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 26 Aug 2021 23:51:32 GMT
WORKDIR /var/www/html
# Thu, 26 Aug 2021 23:51:32 GMT
EXPOSE 80
# Thu, 26 Aug 2021 23:51:33 GMT
CMD ["apache2-foreground"]
# Fri, 27 Aug 2021 07:14:51 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 27 Aug 2021 07:14:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Aug 2021 07:15:31 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Aug 2021 07:15:31 GMT
ARG POSTFIXADMIN_VERSION=3.3.10
# Mon, 30 Aug 2021 21:36:26 GMT
ARG POSTFIXADMIN_SHA512=e00fc9ea343a928976d191adfa01020ee0c6ddbe80a39e01ca2ee414a18247958f033970f378fe4a9974636172a5e094e57117ee9ac7b930c592f433097a7aca
# Mon, 30 Aug 2021 21:36:26 GMT
ENV POSTFIXADMIN_VERSION=3.3.10
# Mon, 30 Aug 2021 21:36:26 GMT
ENV POSTFIXADMIN_SHA512=e00fc9ea343a928976d191adfa01020ee0c6ddbe80a39e01ca2ee414a18247958f033970f378fe4a9974636172a5e094e57117ee9ac7b930c592f433097a7aca
# Mon, 30 Aug 2021 21:36:26 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Mon, 30 Aug 2021 21:36:27 GMT
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf
# Mon, 30 Aug 2021 21:36:29 GMT
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin
# Mon, 30 Aug 2021 21:36:29 GMT
COPY file:c9d831137af59b25a21b91306762892f72362178f6096a24bafecc047bbe6d37 in /usr/local/bin/ 
# Mon, 30 Aug 2021 21:36:30 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Mon, 30 Aug 2021 21:36:30 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6edd81381c438b83d2749dc056d46cd53320e27fb010b3e931ca1f0a752ddc07`  
		Last Modified: Tue, 17 Aug 2021 01:49:56 GMT  
		Size: 32.4 MB (32375657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde02ea43ea712182954343ee01b737ca6911ebdd1527d70da58d27b7a783340`  
		Last Modified: Wed, 18 Aug 2021 00:29:23 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75e82c83c65eda18ff4d7179d4b89c554a2792d4c36b04e03c2b9ede6515962`  
		Last Modified: Wed, 18 Aug 2021 00:29:45 GMT  
		Size: 92.7 MB (92712724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de8bb8fa63c86a9b01ad32ac4d7d10c7c3908efd8781160574009a46d9ec957`  
		Last Modified: Wed, 18 Aug 2021 00:29:23 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5020b8eb36c1dc1fdc847b0f9e27801ed927145025fa69137fd038e46f734cb`  
		Last Modified: Wed, 18 Aug 2021 00:30:31 GMT  
		Size: 19.7 MB (19691617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75db0c00c48f5a0fb6ca36f599e66882fbf1cb0a0ebccdfeb6c8df7d16448874`  
		Last Modified: Wed, 18 Aug 2021 00:30:24 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a535ab9a73ebe90cfb772df39ddb9b18ce3f36465cdc40ad268b1aebe247ff78`  
		Last Modified: Wed, 18 Aug 2021 00:30:24 GMT  
		Size: 517.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648e15607c23d8c24383819f2f310fff25d854ac5f3f4ac6fdfd95d917a74ba3`  
		Last Modified: Fri, 27 Aug 2021 03:48:38 GMT  
		Size: 10.7 MB (10710165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceef0bc3e0d4d42620f7a436a0d46dfabdf19bba22ab45dbbf0c2ee443bef837`  
		Last Modified: Fri, 27 Aug 2021 03:48:34 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14970a71841864bc12cbe3aea089e065cc06cca69fc147245dbd1b14ae54191e`  
		Last Modified: Fri, 27 Aug 2021 03:48:40 GMT  
		Size: 16.5 MB (16482112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6a8500881b9a3f56475f31128d54eebd035506e1b367e3b283d045332ec78c`  
		Last Modified: Fri, 27 Aug 2021 03:48:34 GMT  
		Size: 2.3 KB (2276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2206a61b81c0ecb794127e4d054bfcea84c25d617063e783b9e7d595a208a114`  
		Last Modified: Fri, 27 Aug 2021 03:48:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89bf5ad1967f191beb64851c90cfb6470a132ff9824893d4ed899de92da3570`  
		Last Modified: Fri, 27 Aug 2021 03:48:35 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188e18416b7393e192aa61969ee3966056084d0dc8f9b0798dce4f499cb0b3c3`  
		Last Modified: Mon, 30 Aug 2021 21:37:34 GMT  
		Size: 1.2 MB (1243304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f5547f3fbd3d09227e66ae2f618b34a72f53a45ce36a2f8d42baa2a7da308d`  
		Last Modified: Mon, 30 Aug 2021 21:37:34 GMT  
		Size: 1.2 MB (1222677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa85bde21e031059b2cfa7a420715391d54d8c4fd88e6c759415cdc41e6ef66`  
		Last Modified: Mon, 30 Aug 2021 21:37:34 GMT  
		Size: 8.2 KB (8225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7bc9a7469560067626dd42a824b9ada41926de967250fa5eba4428a70c70fe`  
		Last Modified: Mon, 30 Aug 2021 21:37:34 GMT  
		Size: 1.9 MB (1864815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154ddaf070515bc3fc55c1e4d9e1e79237796017f3bdebff5f939f54c4df7105`  
		Last Modified: Mon, 30 Aug 2021 21:37:34 GMT  
		Size: 1.6 KB (1595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postfixadmin:apache` - linux; mips64le

```console
$ docker pull postfixadmin@sha256:5ccb874cbfd67d24ae735adb99d36a27b30f0170d57cf421499e8605c7d363f5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150563917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f643087a637a2903db83516d950ca24a8de8daec55d173571e0a16909fd0f8fe`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 17 Aug 2021 01:11:35 GMT
ADD file:4dff23dfe5a1c3cf77be5121c29de84ee66c4d10c85faa65f6122da1bfa13500 in / 
# Tue, 17 Aug 2021 01:11:36 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 21:04:04 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 17 Aug 2021 21:04:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 17 Aug 2021 21:04:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 21:04:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 17 Aug 2021 21:04:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 17 Aug 2021 21:17:48 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 17 Aug 2021 21:17:48 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 17 Aug 2021 21:18:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 17 Aug 2021 21:18:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 17 Aug 2021 21:18:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 17 Aug 2021 21:18:18 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 17 Aug 2021 21:18:18 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 17 Aug 2021 21:18:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Aug 2021 21:18:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Aug 2021 21:18:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 18 Aug 2021 00:43:47 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Aug 2021 22:48:03 GMT
ENV PHP_VERSION=7.4.23
# Thu, 26 Aug 2021 22:48:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.23.tar.xz.asc
# Thu, 26 Aug 2021 22:48:04 GMT
ENV PHP_SHA256=cea52313fcffe56343bcd3c66dbb23cd5507dc559cc2e3547cf8f5452e88a05d
# Thu, 26 Aug 2021 22:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 26 Aug 2021 22:48:29 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Aug 2021 22:56:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 26 Aug 2021 22:56:16 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Thu, 26 Aug 2021 22:56:18 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Aug 2021 22:56:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Aug 2021 22:56:18 GMT
STOPSIGNAL SIGWINCH
# Thu, 26 Aug 2021 22:56:19 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 26 Aug 2021 22:56:19 GMT
WORKDIR /var/www/html
# Thu, 26 Aug 2021 22:56:19 GMT
EXPOSE 80
# Thu, 26 Aug 2021 22:56:20 GMT
CMD ["apache2-foreground"]
# Fri, 27 Aug 2021 02:01:48 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 27 Aug 2021 02:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Aug 2021 02:03:50 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Aug 2021 02:03:50 GMT
ARG POSTFIXADMIN_VERSION=3.3.10
# Mon, 30 Aug 2021 20:07:30 GMT
ARG POSTFIXADMIN_SHA512=e00fc9ea343a928976d191adfa01020ee0c6ddbe80a39e01ca2ee414a18247958f033970f378fe4a9974636172a5e094e57117ee9ac7b930c592f433097a7aca
# Mon, 30 Aug 2021 20:07:31 GMT
ENV POSTFIXADMIN_VERSION=3.3.10
# Mon, 30 Aug 2021 20:07:31 GMT
ENV POSTFIXADMIN_SHA512=e00fc9ea343a928976d191adfa01020ee0c6ddbe80a39e01ca2ee414a18247958f033970f378fe4a9974636172a5e094e57117ee9ac7b930c592f433097a7aca
# Mon, 30 Aug 2021 20:07:31 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Mon, 30 Aug 2021 20:07:33 GMT
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf
# Mon, 30 Aug 2021 20:07:37 GMT
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin
# Mon, 30 Aug 2021 20:07:37 GMT
COPY file:c9d831137af59b25a21b91306762892f72362178f6096a24bafecc047bbe6d37 in /usr/local/bin/ 
# Mon, 30 Aug 2021 20:07:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Mon, 30 Aug 2021 20:07:38 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8375ff99ce3f614d73dc69b03575c7ebf072f4e05da52b0319fc3782d5ebb578`  
		Last Modified: Tue, 17 Aug 2021 01:20:19 GMT  
		Size: 29.6 MB (29619986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8262a73716bc8c43dd96ed353eaa7d6653e1b74527cc476cf5442c2234413f5`  
		Last Modified: Wed, 18 Aug 2021 03:32:21 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683e3b4bd71697f7de190513122c240bd01c1b5c1921be7eb1310c572bf9d081`  
		Last Modified: Wed, 18 Aug 2021 03:33:17 GMT  
		Size: 72.0 MB (72015372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f4cccd84833c8e05c27dff4f468d5dd0c173b6093c29ab18d1e86c443b2ca5`  
		Last Modified: Wed, 18 Aug 2021 03:32:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913f73a12d4e36317bd267870efdbfe1a0af8d0d712bee5247e233dcebfc3c20`  
		Last Modified: Wed, 18 Aug 2021 03:34:01 GMT  
		Size: 19.1 MB (19128742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb8ad622e9f1390c316e66b9bf2e50662245faaf32243bf1948c02180b062b6`  
		Last Modified: Wed, 18 Aug 2021 03:33:47 GMT  
		Size: 435.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e452452e959c3f5daf43604986cec8626399137f5fdb0fe338a8c2aa3d0478e`  
		Last Modified: Wed, 18 Aug 2021 03:33:47 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7fa223617b33bcc7d0ee470d61f747fde0759669556d51bdfa837947bcb240`  
		Last Modified: Fri, 27 Aug 2021 01:52:32 GMT  
		Size: 10.7 MB (10708790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0e8ee26e968f9045088b38a35f982156b8887c0b4bdb1a66013bc3d2df2f59`  
		Last Modified: Fri, 27 Aug 2021 01:52:26 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1523c1cb3bf303248e2080d404a6f68a8ef039a26635fd29c1ef56a6854f38d8`  
		Last Modified: Fri, 27 Aug 2021 01:52:39 GMT  
		Size: 14.9 MB (14880478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1d8bd3b9f90889a08df9306bd09cdace8474350dd291a7706e9c68b56dfa14`  
		Last Modified: Fri, 27 Aug 2021 01:52:26 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d55c0e94a9adb64697bda00eeeec678d585acc07e549c1c5d8d8107fee298bf`  
		Last Modified: Fri, 27 Aug 2021 01:52:26 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6718e7b21ad1e6c92daf38dad347bfbbce3eb4cfcdf080e142ef43d9b73949c`  
		Last Modified: Fri, 27 Aug 2021 01:52:26 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e656c4e3003f651e7356a5ac82cec028f413daaf27163dede79cf57b22e5a4`  
		Last Modified: Mon, 30 Aug 2021 20:08:03 GMT  
		Size: 1.2 MB (1160304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cb41c6570f860d6d1a1506bbddd4ee3ab248cae3fc33ce5f630f668d744850`  
		Last Modified: Mon, 30 Aug 2021 20:08:03 GMT  
		Size: 1.2 MB (1170337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f3c6964d37b99cfe6088263463c509b65411b725d90d4e8457e65932383847`  
		Last Modified: Mon, 30 Aug 2021 20:08:02 GMT  
		Size: 8.2 KB (8221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da8f5bd5dae806e3f5cb3d808409f5b155d59e0dba7e59136209a2ccb627756`  
		Last Modified: Mon, 30 Aug 2021 20:08:03 GMT  
		Size: 1.9 MB (1864795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c339907d3555d4fff6bb19aa931f9ba31db3bdb00f8de4e7df039778768ff2`  
		Last Modified: Mon, 30 Aug 2021 20:08:01 GMT  
		Size: 1.6 KB (1596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postfixadmin:apache` - linux; ppc64le

```console
$ docker pull postfixadmin@sha256:41bdc07b010d29db16111c1ef3cdedb8326a33c949f646bd46af29669acb081b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174595695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a840e08a734c3a3f56da4fde995e11b57816095b42a95b1ac9605738acade8ca`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 17 Aug 2021 01:33:09 GMT
ADD file:b7348f0e1a41ce54354496488a0ee8bb949743444973dc6ab51ea80926f596f2 in / 
# Tue, 17 Aug 2021 01:33:15 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 19:08:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 17 Aug 2021 19:08:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 17 Aug 2021 19:15:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 19:15:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 17 Aug 2021 19:15:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 17 Aug 2021 19:25:49 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 17 Aug 2021 19:25:53 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 17 Aug 2021 19:30:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 17 Aug 2021 19:30:42 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 17 Aug 2021 19:31:06 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 17 Aug 2021 19:31:13 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 17 Aug 2021 19:31:18 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 17 Aug 2021 19:31:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Aug 2021 19:31:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Aug 2021 19:31:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 17 Aug 2021 22:23:57 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 27 Aug 2021 03:38:57 GMT
ENV PHP_VERSION=7.4.23
# Fri, 27 Aug 2021 03:39:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.23.tar.xz.asc
# Fri, 27 Aug 2021 03:39:06 GMT
ENV PHP_SHA256=cea52313fcffe56343bcd3c66dbb23cd5507dc559cc2e3547cf8f5452e88a05d
# Fri, 27 Aug 2021 03:40:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 27 Aug 2021 03:40:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Aug 2021 03:48:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Aug 2021 03:48:49 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Fri, 27 Aug 2021 03:48:56 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Aug 2021 03:49:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Aug 2021 03:49:04 GMT
STOPSIGNAL SIGWINCH
# Fri, 27 Aug 2021 03:49:06 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 27 Aug 2021 03:49:08 GMT
WORKDIR /var/www/html
# Fri, 27 Aug 2021 03:49:11 GMT
EXPOSE 80
# Fri, 27 Aug 2021 03:49:15 GMT
CMD ["apache2-foreground"]
# Fri, 27 Aug 2021 17:04:22 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 27 Aug 2021 17:04:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Aug 2021 17:06:09 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Aug 2021 17:06:13 GMT
ARG POSTFIXADMIN_VERSION=3.3.10
# Mon, 30 Aug 2021 23:54:00 GMT
ARG POSTFIXADMIN_SHA512=e00fc9ea343a928976d191adfa01020ee0c6ddbe80a39e01ca2ee414a18247958f033970f378fe4a9974636172a5e094e57117ee9ac7b930c592f433097a7aca
# Mon, 30 Aug 2021 23:54:02 GMT
ENV POSTFIXADMIN_VERSION=3.3.10
# Mon, 30 Aug 2021 23:54:11 GMT
ENV POSTFIXADMIN_SHA512=e00fc9ea343a928976d191adfa01020ee0c6ddbe80a39e01ca2ee414a18247958f033970f378fe4a9974636172a5e094e57117ee9ac7b930c592f433097a7aca
# Mon, 30 Aug 2021 23:54:17 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Mon, 30 Aug 2021 23:54:39 GMT
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf
# Mon, 30 Aug 2021 23:54:58 GMT
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin
# Mon, 30 Aug 2021 23:55:00 GMT
COPY file:c9d831137af59b25a21b91306762892f72362178f6096a24bafecc047bbe6d37 in /usr/local/bin/ 
# Mon, 30 Aug 2021 23:55:05 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Mon, 30 Aug 2021 23:55:07 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:80e30391b3a42f13bd8cb2b497506fa7a23b074d43f7446d94b06514e408020b`  
		Last Modified: Tue, 17 Aug 2021 01:46:01 GMT  
		Size: 35.3 MB (35264011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8646c6e015f224d6ec83a5a7b9c9d550d3cb41ba828e4a65f5043bdd59cb0478`  
		Last Modified: Wed, 18 Aug 2021 00:55:53 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff665f5767591e9baf3b1773a22867f5b386462082c68cc2702f23e6fc4dc77`  
		Last Modified: Wed, 18 Aug 2021 00:57:22 GMT  
		Size: 86.6 MB (86625207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d962b7814a648284b3391df0d223d98e1e57ce4793774bb7d99830378d00f74c`  
		Last Modified: Wed, 18 Aug 2021 00:55:50 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10233d509a2704a93d6d5d050d26a28662643532326cc414328db466d90c9ca6`  
		Last Modified: Wed, 18 Aug 2021 00:58:17 GMT  
		Size: 20.4 MB (20434613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c44e38c08499ae2a1a7a514cf432cb7b06b3498713e541086c897b54b9b799f`  
		Last Modified: Wed, 18 Aug 2021 00:58:03 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a92c4288cf8b5752018f4442a0115a625113df88901778e639fbf0256a2154e`  
		Last Modified: Wed, 18 Aug 2021 00:58:01 GMT  
		Size: 520.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56e863dd740c853fcb241c5bc41cf5bd9616c6ea5c9c75261a89e43aa6d8055`  
		Last Modified: Fri, 27 Aug 2021 07:58:18 GMT  
		Size: 10.7 MB (10711537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47751cff431c1f816dfa4dff8f4b2b6792af3a542523a34848d7b15bc02251e3`  
		Last Modified: Fri, 27 Aug 2021 07:58:10 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacfdef1bcb3de53b5101020d81cf83035c968f24c5337857a089d6996503723`  
		Last Modified: Fri, 27 Aug 2021 07:58:25 GMT  
		Size: 17.2 MB (17151333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b2cc16e4ed90f94c70de4b4d664a59450eb870faa6d33edfc442c26dc87436`  
		Last Modified: Fri, 27 Aug 2021 07:58:09 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e4f7b9a60319f51f55efb02001004708f35877838825f4f422b03c78fb54d8`  
		Last Modified: Fri, 27 Aug 2021 07:58:09 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d305a6b0a2eb7db090db13645b6c134db1bc9e0cbf46d8c2f44e296d25e0df4`  
		Last Modified: Fri, 27 Aug 2021 07:58:10 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af1887c433f0868f964f2276b6e91136ff2af8a0bf4269e0ac825db29f1a59d`  
		Last Modified: Mon, 30 Aug 2021 23:58:11 GMT  
		Size: 1.2 MB (1187067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6901a33557903954856195a75e224baf319332401d01303af4c028ccd7cd9156`  
		Last Modified: Mon, 30 Aug 2021 23:58:12 GMT  
		Size: 1.3 MB (1341853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af0623a6e345f3c23a8402fae460514059a6acd187ec9cfb51bbc232eee8cb3`  
		Last Modified: Mon, 30 Aug 2021 23:58:10 GMT  
		Size: 8.2 KB (8226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd09bd43bb459ff50003de09633fe44a9d8a20052935c42c841bce2dad3ca64`  
		Last Modified: Mon, 30 Aug 2021 23:58:10 GMT  
		Size: 1.9 MB (1864836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34990c6eaa114971747102792181e82958c598b18469353f5c47bf3e5e70a300`  
		Last Modified: Mon, 30 Aug 2021 23:58:10 GMT  
		Size: 1.6 KB (1597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postfixadmin:apache` - linux; s390x

```console
$ docker pull postfixadmin@sha256:68c51fa60f7537a629bc3a8bf139923048e7854242cad18bd422e8daa5c9461b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.3 MB (150298563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf524317024c58e6e715330cf1100a6cc11a514e8b83a22bad11e79ef9fc74c2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 17 Aug 2021 01:49:02 GMT
ADD file:9a849f976712983c3bf95c9d110ab1c38643273c19644a436242e8b8bd5eb225 in / 
# Tue, 17 Aug 2021 01:49:07 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 23:52:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 17 Aug 2021 23:52:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 17 Aug 2021 23:52:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 23:52:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 17 Aug 2021 23:52:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 17 Aug 2021 23:56:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 17 Aug 2021 23:56:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 17 Aug 2021 23:56:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 17 Aug 2021 23:56:29 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 17 Aug 2021 23:56:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 17 Aug 2021 23:56:30 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 17 Aug 2021 23:56:30 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 17 Aug 2021 23:56:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Aug 2021 23:56:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Aug 2021 23:56:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 18 Aug 2021 00:31:15 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Aug 2021 21:16:41 GMT
ENV PHP_VERSION=7.4.23
# Thu, 26 Aug 2021 21:16:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.23.tar.xz.asc
# Thu, 26 Aug 2021 21:16:43 GMT
ENV PHP_SHA256=cea52313fcffe56343bcd3c66dbb23cd5507dc559cc2e3547cf8f5452e88a05d
# Thu, 26 Aug 2021 21:17:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 26 Aug 2021 21:17:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Aug 2021 21:22:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 26 Aug 2021 21:22:03 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Thu, 26 Aug 2021 21:22:05 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Aug 2021 21:22:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Aug 2021 21:22:06 GMT
STOPSIGNAL SIGWINCH
# Thu, 26 Aug 2021 21:22:06 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 26 Aug 2021 21:22:07 GMT
WORKDIR /var/www/html
# Thu, 26 Aug 2021 21:22:07 GMT
EXPOSE 80
# Thu, 26 Aug 2021 21:22:08 GMT
CMD ["apache2-foreground"]
# Fri, 27 Aug 2021 07:15:45 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 27 Aug 2021 07:15:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Aug 2021 07:16:39 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Aug 2021 07:16:39 GMT
ARG POSTFIXADMIN_VERSION=3.3.10
# Mon, 30 Aug 2021 21:32:23 GMT
ARG POSTFIXADMIN_SHA512=e00fc9ea343a928976d191adfa01020ee0c6ddbe80a39e01ca2ee414a18247958f033970f378fe4a9974636172a5e094e57117ee9ac7b930c592f433097a7aca
# Mon, 30 Aug 2021 21:32:24 GMT
ENV POSTFIXADMIN_VERSION=3.3.10
# Mon, 30 Aug 2021 21:32:24 GMT
ENV POSTFIXADMIN_SHA512=e00fc9ea343a928976d191adfa01020ee0c6ddbe80a39e01ca2ee414a18247958f033970f378fe4a9974636172a5e094e57117ee9ac7b930c592f433097a7aca
# Mon, 30 Aug 2021 21:32:25 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Mon, 30 Aug 2021 21:32:26 GMT
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf
# Mon, 30 Aug 2021 21:32:28 GMT
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin
# Mon, 30 Aug 2021 21:32:28 GMT
COPY file:c9d831137af59b25a21b91306762892f72362178f6096a24bafecc047bbe6d37 in /usr/local/bin/ 
# Mon, 30 Aug 2021 21:32:28 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Mon, 30 Aug 2021 21:32:29 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:16c136b299a1426955abff4eb0ed556e3c2e8e67509fba84e416f1d5cc77189a`  
		Last Modified: Tue, 17 Aug 2021 01:57:33 GMT  
		Size: 29.6 MB (29647028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95186f11f9aca8af9be912823712ea541f8e6e600b179d3616d3be6b93736e00`  
		Last Modified: Wed, 18 Aug 2021 01:12:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a7d93dc02b570d50d80a1aa8b5124a704cb208cb9699b826113438de812870`  
		Last Modified: Wed, 18 Aug 2021 01:12:10 GMT  
		Size: 71.6 MB (71622148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ff946dfc28cc308722046900124caf233323b72bd2783f5b71846a58df3086`  
		Last Modified: Wed, 18 Aug 2021 01:12:01 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf34bdb15c8951c94f3f8be0067bcaed627581e63859f048a815d7579862fe7`  
		Last Modified: Wed, 18 Aug 2021 01:12:35 GMT  
		Size: 19.0 MB (19026307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f21256bcd2a7aa22771523fa8564c09ddcc2e7af08a2cce08745b5ced7860c9`  
		Last Modified: Wed, 18 Aug 2021 01:12:32 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c56103e88f74dc68c3230aa6e167b39fe42d1cdbdedb212633bfe002c6df42`  
		Last Modified: Wed, 18 Aug 2021 01:12:32 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd01ef0a01e3166352b37437ed6a47c478bd2098ee24a8fca857ae412c4849a`  
		Last Modified: Fri, 27 Aug 2021 00:19:52 GMT  
		Size: 10.7 MB (10709890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c445a41b48e7c253a5e8c6ad0d6728133b22210350ea022e9fbdc201c75883`  
		Last Modified: Fri, 27 Aug 2021 00:19:50 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1041b9591c1ac1b48e132217d5bc6bb575a1a99337501665bb525910f65c22b`  
		Last Modified: Fri, 27 Aug 2021 00:19:52 GMT  
		Size: 15.0 MB (14970411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5191a35aaf157144560f1e773a1c7356a14f9167d7e8657dff0553d6a30ebd44`  
		Last Modified: Fri, 27 Aug 2021 00:19:50 GMT  
		Size: 2.3 KB (2277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9acc3992b261d20d1bdee9cf0448eda3e74b241584164af6e282882659025982`  
		Last Modified: Fri, 27 Aug 2021 00:19:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a5b5084076a5b18a6973975cfc403cc740ce5c30a96edd27fdc5212f8c6eb7`  
		Last Modified: Fri, 27 Aug 2021 00:19:50 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75f64fdf5e5b4437a373f5a07b944c048195013a80472fae083ef4a171c065b`  
		Last Modified: Mon, 30 Aug 2021 21:33:41 GMT  
		Size: 1.2 MB (1245655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793605939b2a84191a8fbe0c897f0c5b46a80a46684e6c5a54bd517b3db73136`  
		Last Modified: Mon, 30 Aug 2021 21:33:41 GMT  
		Size: 1.2 MB (1197091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0514f42b130f6e2c3f70b1a0df26a5d19d67d43c74090deb0af4bc7b5f0736`  
		Last Modified: Mon, 30 Aug 2021 21:33:41 GMT  
		Size: 8.2 KB (8222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79baf7a77f7ecec899e5a77e01fded6d190a935c6ec6ef40bcbaea5969d5ffab`  
		Last Modified: Mon, 30 Aug 2021 21:33:41 GMT  
		Size: 1.9 MB (1864818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa584cfcf61d64f03242dddb674b46dcdfcd302597c8df8512ba03e4406d449`  
		Last Modified: Mon, 30 Aug 2021 21:33:40 GMT  
		Size: 1.6 KB (1595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
