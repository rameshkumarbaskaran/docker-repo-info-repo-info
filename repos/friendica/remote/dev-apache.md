## `friendica:dev-apache`

```console
$ docker pull friendica@sha256:89119c1879ec3535f2c9e31f78ce5b99f46ed1cbee944b39d180ebcbbacea93d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `friendica:dev-apache` - linux; amd64

```console
$ docker pull friendica@sha256:18e352b99ef89056f5783402d849bbfa22b3dd7ec28b81b3208d8c51ae5507b8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.1 MB (160131656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81442c7898a95e92620e5996ca79c08c6f417ef8528d2b8c65f43a1d5bdc0ac`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 14:34:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 09 Jun 2020 14:34:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Jun 2020 14:34:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 14:34:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Jun 2020 14:34:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 09 Jun 2020 14:42:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 09 Jun 2020 14:42:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 09 Jun 2020 14:42:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 09 Jun 2020 14:42:38 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 09 Jun 2020 14:42:39 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 09 Jun 2020 14:42:39 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 09 Jun 2020 14:42:40 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 09 Jun 2020 14:42:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 14:42:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 14:42:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Jun 2020 14:42:41 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 11 Jun 2020 20:26:42 GMT
ENV PHP_VERSION=7.3.19
# Thu, 11 Jun 2020 20:26:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.19.tar.xz.asc
# Thu, 11 Jun 2020 20:26:43 GMT
ENV PHP_SHA256=6402faa19b1a8c4317c7612632bce985684a5bbae0980a5779a4019439882422 PHP_MD5=
# Thu, 11 Jun 2020 20:26:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 11 Jun 2020 20:26:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 Jun 2020 20:32:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	sed -e 's/stretch/buster/g' /etc/apt/sources.list > /etc/apt/sources.list.d/buster.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: -10'; 		echo; 		echo 'Package: libargon2*'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: 990'; 	} > /etc/apt/preferences.d/argon2-buster; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 11 Jun 2020 20:32:30 GMT
COPY multi:af24b1d34daac0a277386947399eceaaf20d3065d4be5db00b1d6466cf006c49 in /usr/local/bin/ 
# Thu, 11 Jun 2020 20:32:32 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 Jun 2020 20:32:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2020 20:32:32 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Jun 2020 20:32:33 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 11 Jun 2020 20:32:33 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2020 20:32:34 GMT
EXPOSE 80
# Thu, 11 Jun 2020 20:32:34 GMT
CMD ["apache2-foreground"]
# Fri, 12 Jun 2020 01:27:46 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         ssmtp         gnupg dirmngr     ;     rm -rf /var/lib/apt/lists/*;
# Fri, 12 Jun 2020 01:27:47 GMT
ENV TINI_VERSION=v0.18.0
# Fri, 12 Jun 2020 01:27:51 GMT
RUN export BUILD_ARCH=$(dpkg-architecture --query DEB_BUILD_ARCH)  && curl -L -o /sbin/tini https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}  && curl -L -o /tini.asc https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}.asc  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7  && gpg --batch --verify /tini.asc /sbin/tini  && chmod +x /sbin/tini
# Fri, 12 Jun 2020 01:31:19 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mysql-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         	--with-libdir=lib/$debMultiarch/ 	;     docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.2.1;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so       | awk '/=>/ { print $3 }'       | sort -u       | xargs -r dpkg-query -S       | cut -d: -f1       | sort -u       | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 01:31:20 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 12 Jun 2020 01:31:20 GMT
VOLUME [/var/www/html]
# Fri, 12 Jun 2020 01:31:21 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Fri, 12 Jun 2020 01:38:58 GMT
ENV FRIENDICA_VERSION=2020.06-dev
# Fri, 12 Jun 2020 01:38:58 GMT
ENV FRIENDICA_ADDONS=2020.06-dev
# Fri, 12 Jun 2020 01:38:59 GMT
COPY multi:79c18253e95b11e5d803cb19685ac5cb4fcedfeda73215d7e2e3f89d93570667 in / 
# Fri, 12 Jun 2020 01:39:00 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Fri, 12 Jun 2020 01:39:00 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Fri, 12 Jun 2020 01:39:01 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91190bcc56254a5cdaafb416a5a4e01543442c451af753d0442804c924a08fb`  
		Last Modified: Tue, 09 Jun 2020 16:00:37 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980980888a3d5f680fbad3f6701844789e5a6f0284ac94fff081a5e38cab09d6`  
		Last Modified: Tue, 09 Jun 2020 16:00:55 GMT  
		Size: 67.4 MB (67412170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd615770b9224dcf72a5f3ef5fe7fb60ea0af4fbcd8808a899d4ab140dc8e14`  
		Last Modified: Tue, 09 Jun 2020 16:00:36 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd0bce484b914222f405074a7a741b56f3764c9be971deb42239f693646c5be`  
		Last Modified: Tue, 09 Jun 2020 16:01:09 GMT  
		Size: 17.1 MB (17125226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013fe8ffd3398fc563f105ccc43de5097cfcbfc9b9edc69dac31efcd16c4bdd0`  
		Last Modified: Tue, 09 Jun 2020 16:01:04 GMT  
		Size: 430.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9fcda9985125a1c797ebce95b5fb482911891a7b39647890080af67ec2237e0`  
		Last Modified: Tue, 09 Jun 2020 16:01:04 GMT  
		Size: 487.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ebc0469bf9ea913c4ab618f45c5040c898dc13e2a5e16118b83a09593cde566`  
		Last Modified: Thu, 11 Jun 2020 22:18:15 GMT  
		Size: 12.5 MB (12466094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b547a21e1932e3c1efb17ef28e52ff6ae57b13f3c665effc2ddb337132abebd7`  
		Last Modified: Thu, 11 Jun 2020 22:18:13 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f5b0a8d45e12ce491c888b36593bd7cbe1d8b452ada1785dd17fe02f7135a7`  
		Last Modified: Thu, 11 Jun 2020 22:18:20 GMT  
		Size: 13.8 MB (13798817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152371cb2a14024dcf6b1a8046839a4fc8e6f35febf4064f71f09c28d4912378`  
		Last Modified: Thu, 11 Jun 2020 22:18:13 GMT  
		Size: 2.3 KB (2296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cc1f0867a795e708f70bede38bc7b7c0c65b88bbbd73b92b8ccdd0c10871e9`  
		Last Modified: Thu, 11 Jun 2020 22:18:13 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66397b3d97278028c24ef4a348f67f776127acc9bfa0408ec2ebe1baade12570`  
		Last Modified: Thu, 11 Jun 2020 22:18:13 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c6f3d376b83df2755a667636712cfa1cd3545be4fdacc41168647c2ac6e3ae`  
		Last Modified: Fri, 12 Jun 2020 01:39:35 GMT  
		Size: 15.1 MB (15078244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b07c49b921f2b1cfb8d087d7a69e26a1696b62bfc95aedc658fcc7df6093ae`  
		Last Modified: Fri, 12 Jun 2020 01:39:33 GMT  
		Size: 16.3 KB (16290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674e192b2be24ea849f6b3f4cdbcea72708645d4b051f0ac4cb882d42bdfcd8b`  
		Last Modified: Fri, 12 Jun 2020 01:39:34 GMT  
		Size: 11.7 MB (11704847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f233abad4830fe2de736968e3456da167c2131ef2e3e54ca068e126cdf7e51`  
		Last Modified: Fri, 12 Jun 2020 01:39:31 GMT  
		Size: 566.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f49f51bc4ccc21db140cf60ff966be9845b60e1f625682de972127c0b0e25b7`  
		Last Modified: Fri, 12 Jun 2020 01:39:31 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d399f1a40996b0de391db75006d1624c86cc84700c1fb2c4167108bf0912cb`  
		Last Modified: Fri, 12 Jun 2020 01:39:32 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1368c428c0407d95660518053adae69075b2d1e0d1919e13b6e7480f3527836f`  
		Last Modified: Fri, 12 Jun 2020 01:39:31 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-apache` - linux; arm variant v5

```console
$ docker pull friendica@sha256:24ff4c4acd5338f5aa98eac11e10564c05808eead87e08cbbd7d639dd36d840a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.3 MB (146312502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a124a9976197cd67ecd77b26b6cd2eb845e0622a51cc45975e8e8317383e3965`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 09 Jun 2020 00:55:49 GMT
ADD file:af949d376cc9a2ac87d0052d22fe17be59dfe65905f0645d1a903b359208d26d in / 
# Tue, 09 Jun 2020 00:55:51 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:47:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 09 Jun 2020 03:47:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Jun 2020 03:48:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:48:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Jun 2020 03:48:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 09 Jun 2020 03:52:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 09 Jun 2020 03:52:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 09 Jun 2020 03:53:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 09 Jun 2020 03:53:05 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 09 Jun 2020 03:53:07 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 09 Jun 2020 03:53:08 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 09 Jun 2020 03:53:08 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 09 Jun 2020 03:53:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 03:53:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 03:53:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Jun 2020 03:53:11 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 11 Jun 2020 19:02:23 GMT
ENV PHP_VERSION=7.3.19
# Thu, 11 Jun 2020 19:02:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.19.tar.xz.asc
# Thu, 11 Jun 2020 19:02:25 GMT
ENV PHP_SHA256=6402faa19b1a8c4317c7612632bce985684a5bbae0980a5779a4019439882422 PHP_MD5=
# Thu, 11 Jun 2020 19:02:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 11 Jun 2020 19:02:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 Jun 2020 19:07:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	sed -e 's/stretch/buster/g' /etc/apt/sources.list > /etc/apt/sources.list.d/buster.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: -10'; 		echo; 		echo 'Package: libargon2*'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: 990'; 	} > /etc/apt/preferences.d/argon2-buster; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 11 Jun 2020 19:07:13 GMT
COPY multi:af24b1d34daac0a277386947399eceaaf20d3065d4be5db00b1d6466cf006c49 in /usr/local/bin/ 
# Thu, 11 Jun 2020 19:07:16 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 Jun 2020 19:07:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2020 19:07:17 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Jun 2020 19:07:18 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 11 Jun 2020 19:07:19 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2020 19:07:19 GMT
EXPOSE 80
# Thu, 11 Jun 2020 19:07:20 GMT
CMD ["apache2-foreground"]
# Thu, 11 Jun 2020 20:06:29 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         ssmtp         gnupg dirmngr     ;     rm -rf /var/lib/apt/lists/*;
# Thu, 11 Jun 2020 20:06:30 GMT
ENV TINI_VERSION=v0.18.0
# Thu, 11 Jun 2020 20:06:37 GMT
RUN export BUILD_ARCH=$(dpkg-architecture --query DEB_BUILD_ARCH)  && curl -L -o /sbin/tini https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}  && curl -L -o /tini.asc https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}.asc  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7  && gpg --batch --verify /tini.asc /sbin/tini  && chmod +x /sbin/tini
# Thu, 11 Jun 2020 20:13:07 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mysql-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         	--with-libdir=lib/$debMultiarch/ 	;     docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.2.1;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so       | awk '/=>/ { print $3 }'       | sort -u       | xargs -r dpkg-query -S       | cut -d: -f1       | sort -u       | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jun 2020 20:13:10 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Thu, 11 Jun 2020 20:13:10 GMT
VOLUME [/var/www/html]
# Thu, 11 Jun 2020 20:13:13 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Thu, 11 Jun 2020 20:21:42 GMT
ENV FRIENDICA_VERSION=2020.06-dev
# Thu, 11 Jun 2020 20:21:43 GMT
ENV FRIENDICA_ADDONS=2020.06-dev
# Thu, 11 Jun 2020 20:21:45 GMT
COPY multi:79c18253e95b11e5d803cb19685ac5cb4fcedfeda73215d7e2e3f89d93570667 in / 
# Thu, 11 Jun 2020 20:21:48 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Thu, 11 Jun 2020 20:21:50 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 11 Jun 2020 20:21:53 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c9b35828d9245f0a85299b96b2d9b0d70390689cf7df0fe7ef29ca6028c0ab56`  
		Last Modified: Tue, 09 Jun 2020 01:03:09 GMT  
		Size: 21.2 MB (21197337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54880485c9e08abdbce3b0f76c307a0b9f7aa394b2ce9bac77918ff8a8e31dee`  
		Last Modified: Tue, 09 Jun 2020 04:46:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f743b703af8a45a29170c64a7bc2ac5c574f5f1b7f2b048aff482141d9e1a88`  
		Last Modified: Tue, 09 Jun 2020 04:46:51 GMT  
		Size: 57.4 MB (57430558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc54e06c6d384a48529a64b0b997115c84fb8158108be2409619e46d249e5427`  
		Last Modified: Tue, 09 Jun 2020 04:46:30 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a131ad31f965fcf10f5e6480abbff66bd851d40dc38f8ee1c33e46e4273d83`  
		Last Modified: Tue, 09 Jun 2020 04:47:10 GMT  
		Size: 16.6 MB (16643927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1336bb4bbf07a2c5e817a06d08c35627e120c4249a0b72da3f8d71161931fc`  
		Last Modified: Tue, 09 Jun 2020 04:47:05 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8b372ad30148c4c47000aef600b46aabe5ba94f16068430ff0eb26a59444d5`  
		Last Modified: Tue, 09 Jun 2020 04:47:04 GMT  
		Size: 519.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90633b7e795d166d41617b8f900155c2cc1040bd25ec6307102c96495b42af3`  
		Last Modified: Thu, 11 Jun 2020 19:24:05 GMT  
		Size: 12.5 MB (12464143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f355b45b81607aa7d141ccd72ad99b60d1ffdfaa2074539512dd6093ca13bedf`  
		Last Modified: Thu, 11 Jun 2020 19:24:01 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e5c8fa00217d2c8cd7b6fec2acd7ab244e4a8338f04ae52158a2cb8b17b897`  
		Last Modified: Thu, 11 Jun 2020 19:24:07 GMT  
		Size: 13.1 MB (13071563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7f9273012f03636dfdac772471e3b751a99796acdcbae1ff6925cc360f1224`  
		Last Modified: Thu, 11 Jun 2020 19:24:00 GMT  
		Size: 2.3 KB (2297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccab51c6a0ccb86513545a2de08de64ea7bb7edea042a8646550a7b217bdf8cc`  
		Last Modified: Thu, 11 Jun 2020 19:24:00 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7471c594f0de5af497d0e209257baa69576b7e139b5714739c6c267405ea594b`  
		Last Modified: Thu, 11 Jun 2020 19:24:00 GMT  
		Size: 905.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ea6b21c634799c25309a80b69970de3e42fb8aadc9d3b3500b75489468af10`  
		Last Modified: Thu, 11 Jun 2020 20:22:30 GMT  
		Size: 14.0 MB (14013297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:115715aa678a6fb4081b48b0a59870c48279fecd2169719a6c6168c4852e83cd`  
		Last Modified: Thu, 11 Jun 2020 20:22:26 GMT  
		Size: 15.7 KB (15712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d3c5063597206e74ed97c3a6f54197f4b08407a91344157d7dcb9d40103333`  
		Last Modified: Thu, 11 Jun 2020 20:22:28 GMT  
		Size: 11.5 MB (11465416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a284a3607ef429a360e9cd3ec9cac40a26836f35b7e883b55baa3f6387671d`  
		Last Modified: Thu, 11 Jun 2020 20:22:24 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1381c207fcaad869090505ca98624126106f96a8f4a50fa126887cf1d07438ac`  
		Last Modified: Thu, 11 Jun 2020 20:22:24 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d570ed9c0b8106a850e0832d6dfd120558d7b4b4b03539a25a45ed2c6800f0ce`  
		Last Modified: Thu, 11 Jun 2020 20:22:25 GMT  
		Size: 2.9 KB (2851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef237862be34f290e526a9416f1be7ef7db1624aca7166ce75b9b05a3c729b0`  
		Last Modified: Thu, 11 Jun 2020 20:22:25 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-apache` - linux; arm variant v7

```console
$ docker pull friendica@sha256:4a673dc378d64a929a9c7121ae22674d3fb1673799995ba60396b64bc6a38545
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137293738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18321c3be45b497792d01534dadba36922162c5456abda09b7953a9462ffb6e2`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 09 Jun 2020 01:06:35 GMT
ADD file:4a0a863669948b35130fcf8cdb52999c49f7b3ee0620a1eef5f1a2e850a42f05 in / 
# Tue, 09 Jun 2020 01:06:37 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 10:12:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 09 Jun 2020 10:12:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Jun 2020 10:13:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 10:13:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Jun 2020 10:13:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 09 Jun 2020 10:17:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 09 Jun 2020 10:17:52 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 09 Jun 2020 10:18:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 09 Jun 2020 10:18:20 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 09 Jun 2020 10:18:25 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 09 Jun 2020 10:18:26 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 09 Jun 2020 10:18:27 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 09 Jun 2020 10:18:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 10:18:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 10:18:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Jun 2020 10:18:30 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 11 Jun 2020 19:21:14 GMT
ENV PHP_VERSION=7.3.19
# Thu, 11 Jun 2020 19:21:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.19.tar.xz.asc
# Thu, 11 Jun 2020 19:21:17 GMT
ENV PHP_SHA256=6402faa19b1a8c4317c7612632bce985684a5bbae0980a5779a4019439882422 PHP_MD5=
# Thu, 11 Jun 2020 19:21:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 11 Jun 2020 19:21:45 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 Jun 2020 19:25:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	sed -e 's/stretch/buster/g' /etc/apt/sources.list > /etc/apt/sources.list.d/buster.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: -10'; 		echo; 		echo 'Package: libargon2*'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: 990'; 	} > /etc/apt/preferences.d/argon2-buster; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 11 Jun 2020 19:25:45 GMT
COPY multi:af24b1d34daac0a277386947399eceaaf20d3065d4be5db00b1d6466cf006c49 in /usr/local/bin/ 
# Thu, 11 Jun 2020 19:25:48 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 Jun 2020 19:25:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2020 19:25:50 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Jun 2020 19:25:50 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 11 Jun 2020 19:25:52 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2020 19:25:53 GMT
EXPOSE 80
# Thu, 11 Jun 2020 19:25:55 GMT
CMD ["apache2-foreground"]
# Fri, 12 Jun 2020 00:51:24 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         ssmtp         gnupg dirmngr     ;     rm -rf /var/lib/apt/lists/*;
# Fri, 12 Jun 2020 00:51:26 GMT
ENV TINI_VERSION=v0.18.0
# Fri, 12 Jun 2020 00:51:33 GMT
RUN export BUILD_ARCH=$(dpkg-architecture --query DEB_BUILD_ARCH)  && curl -L -o /sbin/tini https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}  && curl -L -o /tini.asc https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}.asc  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7  && gpg --batch --verify /tini.asc /sbin/tini  && chmod +x /sbin/tini
# Fri, 12 Jun 2020 00:59:25 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mysql-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         	--with-libdir=lib/$debMultiarch/ 	;     docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.2.1;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so       | awk '/=>/ { print $3 }'       | sort -u       | xargs -r dpkg-query -S       | cut -d: -f1       | sort -u       | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 00:59:28 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 12 Jun 2020 00:59:30 GMT
VOLUME [/var/www/html]
# Fri, 12 Jun 2020 00:59:36 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Fri, 12 Jun 2020 01:12:47 GMT
ENV FRIENDICA_VERSION=2020.06-dev
# Fri, 12 Jun 2020 01:12:49 GMT
ENV FRIENDICA_ADDONS=2020.06-dev
# Fri, 12 Jun 2020 01:12:50 GMT
COPY multi:79c18253e95b11e5d803cb19685ac5cb4fcedfeda73215d7e2e3f89d93570667 in / 
# Fri, 12 Jun 2020 01:12:52 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Fri, 12 Jun 2020 01:12:53 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Fri, 12 Jun 2020 01:12:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c439312a9c212b64af3c38cb326bb5fbe14bcf4a622115d59d44985e949bee82`  
		Last Modified: Tue, 09 Jun 2020 01:13:51 GMT  
		Size: 19.3 MB (19304370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73725dbb9cd7f8c9d89450287e1a202e01555c3ab64c6985a953ea2aee9cc82`  
		Last Modified: Tue, 09 Jun 2020 11:14:30 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e57eaf0280ce9f5a65c9374b4cfa0c3d2569e0f32eb4f16c516cec9dbb152f6`  
		Last Modified: Tue, 09 Jun 2020 11:14:47 GMT  
		Size: 53.5 MB (53543440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd383ea222181c9908027fecd2fdaa413c796228ebf9d9e49a6109c023fd448`  
		Last Modified: Tue, 09 Jun 2020 11:14:30 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460de74305a98744e1cc0bde989ada7fc9cc6e34920af0a20322ef1edca8e68d`  
		Last Modified: Tue, 09 Jun 2020 11:15:01 GMT  
		Size: 16.2 MB (16159381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e457a50fafa8e307da55c6c498562339728bd72080bd90926fce15e396ece22e`  
		Last Modified: Tue, 09 Jun 2020 11:14:56 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d42e663ca807a85f0eba07caa76ca78dad1fb3c62bb311399de8de1217bffd16`  
		Last Modified: Tue, 09 Jun 2020 11:14:56 GMT  
		Size: 516.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09035258c649fb5c87756e11c8c3d61ab333d513fbe86186ff0f147bc34de07`  
		Last Modified: Thu, 11 Jun 2020 20:16:17 GMT  
		Size: 12.5 MB (12464126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41d0341af51c9a25d0c2598c7127d87c4ae1ec38355419a0afa87dbbf1000db`  
		Last Modified: Thu, 11 Jun 2020 20:16:14 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b052b21a9523d3718a33bc5f95b016025d17c0050902bb78ce13864abc2ba5a7`  
		Last Modified: Thu, 11 Jun 2020 20:16:18 GMT  
		Size: 12.4 MB (12390890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fcc4924ea99a14f55647586bb75b9a9d5597bac2b2f77d88dc5de8f838cbf20`  
		Last Modified: Thu, 11 Jun 2020 20:16:14 GMT  
		Size: 2.3 KB (2296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cbe461747fb7f3564b93cc583e73f16824aff0855f77125315c9e3ef37b2b0`  
		Last Modified: Thu, 11 Jun 2020 20:16:14 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9aeaf5c4de02cfabcc627c0fd283b724b1116cbc610e26a5cfe0174d25af85d`  
		Last Modified: Thu, 11 Jun 2020 20:16:14 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a04040ac7e58fa0a9c91dfc9de35b1117d62c54efd6962242f36af0809addb7`  
		Last Modified: Fri, 12 Jun 2020 01:13:51 GMT  
		Size: 12.7 MB (12735629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80dfe428c6027038c0054c6ee3649b108f8fbc30cbb521f8dea0e37d1e69ee66`  
		Last Modified: Fri, 12 Jun 2020 01:13:46 GMT  
		Size: 14.9 KB (14948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b930eee89d6aa3a3fcdfad459ca5b76838e6a39f14c31487473f12805dffbc27`  
		Last Modified: Fri, 12 Jun 2020 01:13:47 GMT  
		Size: 10.7 MB (10670406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7444e2adfb675f52cbf5445bb13ccf44258a177f78e5e44063f9b109076e2f61`  
		Last Modified: Fri, 12 Jun 2020 01:13:44 GMT  
		Size: 596.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53970e93336be2fab3d5022509a86a31f973b6e10383d1383fed487041b51e51`  
		Last Modified: Fri, 12 Jun 2020 01:13:44 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ab1f06b474b7c8a15ece7f12138d897a9a2e6d02c070821871e89282cd083e`  
		Last Modified: Fri, 12 Jun 2020 01:13:44 GMT  
		Size: 2.9 KB (2851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83bab08259ea37962d8b88c2f7070c3d1c1d0bf8343c2025498343e53e17b19c`  
		Last Modified: Fri, 12 Jun 2020 01:13:45 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-apache` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:8ad94d9f54a478fee90891525df7e80463cc37a67d9d54ade19ee6b1a40e38f9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144318159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764cce56219fb887c896cb571b785ca9dca4ae2c8cdcfbb160141b680dfaae3f`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:49 GMT
ADD file:c85d28567b6123deb660b71c8b60d92378b5ba15ba5dcf495d9388817dc3aa44 in / 
# Tue, 09 Jun 2020 01:54:52 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 11:01:51 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 09 Jun 2020 11:01:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Jun 2020 11:02:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 11:02:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Jun 2020 11:02:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 09 Jun 2020 11:07:26 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 09 Jun 2020 11:07:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 09 Jun 2020 11:07:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 09 Jun 2020 11:07:47 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 09 Jun 2020 11:07:49 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 09 Jun 2020 11:07:50 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 09 Jun 2020 11:07:51 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 09 Jun 2020 11:07:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 11:07:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 11:07:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Jun 2020 11:07:54 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 11 Jun 2020 19:35:15 GMT
ENV PHP_VERSION=7.3.19
# Thu, 11 Jun 2020 19:35:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.19.tar.xz.asc
# Thu, 11 Jun 2020 19:35:17 GMT
ENV PHP_SHA256=6402faa19b1a8c4317c7612632bce985684a5bbae0980a5779a4019439882422 PHP_MD5=
# Thu, 11 Jun 2020 19:35:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 11 Jun 2020 19:35:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 Jun 2020 19:39:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	sed -e 's/stretch/buster/g' /etc/apt/sources.list > /etc/apt/sources.list.d/buster.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: -10'; 		echo; 		echo 'Package: libargon2*'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: 990'; 	} > /etc/apt/preferences.d/argon2-buster; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 11 Jun 2020 19:39:14 GMT
COPY multi:af24b1d34daac0a277386947399eceaaf20d3065d4be5db00b1d6466cf006c49 in /usr/local/bin/ 
# Thu, 11 Jun 2020 19:39:20 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 Jun 2020 19:39:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2020 19:39:23 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Jun 2020 19:39:24 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 11 Jun 2020 19:39:26 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2020 19:39:26 GMT
EXPOSE 80
# Thu, 11 Jun 2020 19:39:27 GMT
CMD ["apache2-foreground"]
# Thu, 11 Jun 2020 23:04:09 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         ssmtp         gnupg dirmngr     ;     rm -rf /var/lib/apt/lists/*;
# Thu, 11 Jun 2020 23:04:16 GMT
ENV TINI_VERSION=v0.18.0
# Thu, 11 Jun 2020 23:04:49 GMT
RUN export BUILD_ARCH=$(dpkg-architecture --query DEB_BUILD_ARCH)  && curl -L -o /sbin/tini https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}  && curl -L -o /tini.asc https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}.asc  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7  && gpg --batch --verify /tini.asc /sbin/tini  && chmod +x /sbin/tini
# Thu, 11 Jun 2020 23:11:48 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mysql-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         	--with-libdir=lib/$debMultiarch/ 	;     docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.2.1;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so       | awk '/=>/ { print $3 }'       | sort -u       | xargs -r dpkg-query -S       | cut -d: -f1       | sort -u       | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jun 2020 23:12:30 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Thu, 11 Jun 2020 23:12:36 GMT
VOLUME [/var/www/html]
# Thu, 11 Jun 2020 23:12:54 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Thu, 11 Jun 2020 23:35:25 GMT
ENV FRIENDICA_VERSION=2020.06-dev
# Thu, 11 Jun 2020 23:35:30 GMT
ENV FRIENDICA_ADDONS=2020.06-dev
# Thu, 11 Jun 2020 23:35:46 GMT
COPY multi:79c18253e95b11e5d803cb19685ac5cb4fcedfeda73215d7e2e3f89d93570667 in / 
# Thu, 11 Jun 2020 23:36:00 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Thu, 11 Jun 2020 23:36:11 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 11 Jun 2020 23:36:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:622dc742b82743ebf5607b215a65869096390ee41b0a61b5532f859fb94590b1`  
		Last Modified: Tue, 09 Jun 2020 02:00:28 GMT  
		Size: 20.4 MB (20375150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f1ac10028b11eda5306594db4aed4c31d711170b1f963ecb9144c4559c5a7c`  
		Last Modified: Tue, 09 Jun 2020 12:00:22 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c83c05c7e4d0233a5344499641630bb718814b9821d28b8b714691b4e66b01`  
		Last Modified: Tue, 09 Jun 2020 12:00:39 GMT  
		Size: 57.6 MB (57578779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d95aec92ba4e1aff170dd91600f93bdc9c0713772a061f12c01254f6ef0aaa`  
		Last Modified: Tue, 09 Jun 2020 12:00:21 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e8dd9acb3f16735b5404c60c0b5a8674fbcd399802159fb3dd481242d98747`  
		Last Modified: Tue, 09 Jun 2020 12:00:54 GMT  
		Size: 16.7 MB (16708196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d173215d0c062e558062daad5eb1d80635a3fd057dce4050b132179f632cde29`  
		Last Modified: Tue, 09 Jun 2020 12:00:49 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244e606ea11ac743f9e9eaa3bf9cfb08663f3c922f8bedafa8abf294782e3956`  
		Last Modified: Tue, 09 Jun 2020 12:00:48 GMT  
		Size: 519.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17868af8de4f4fe027606ccd917f6661a5b42dc2c7c8c89c06f41f5c170dffc7`  
		Last Modified: Thu, 11 Jun 2020 20:33:26 GMT  
		Size: 12.5 MB (12464031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d50af188bde6f4adc586dda94f14e90840d52f37efff9dbd5d990e9a084b81`  
		Last Modified: Thu, 11 Jun 2020 20:33:23 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93563c1076336d8060d88a84d8dcf4768002550ea21482e2a08c5c77c2c340df`  
		Last Modified: Thu, 11 Jun 2020 20:33:27 GMT  
		Size: 12.9 MB (12864200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d117dd73d18b20ff56b70970c68e660782716faee9ba0533a6487075c2f6c950`  
		Last Modified: Thu, 11 Jun 2020 20:33:22 GMT  
		Size: 2.3 KB (2296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32583556b2257d88f9790e72b0644ffbfbe70974ce62afa3b0f2562a8a2430b1`  
		Last Modified: Thu, 11 Jun 2020 20:33:22 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a55fcd7451ea486b920a6d67b4f791a1b91e33fb94e9e4b2845f9a1fe630ea`  
		Last Modified: Thu, 11 Jun 2020 20:33:22 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e2371a353987964dcad452f09d8227b81c70a2336057f77292c63dbba08570`  
		Last Modified: Thu, 11 Jun 2020 23:40:45 GMT  
		Size: 13.6 MB (13617542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fdead1c23f9403033c873e67812b9fcdb81a12664e2fe9f2affc48dc11ea50f`  
		Last Modified: Thu, 11 Jun 2020 23:40:41 GMT  
		Size: 15.9 KB (15906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0a5d093c0061c49e7849109dc85a80390feec3fd5cff7c52fdbcd286e38b48`  
		Last Modified: Thu, 11 Jun 2020 23:40:37 GMT  
		Size: 10.7 MB (10683807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aaea1fe2b386f49bf95ed8e0f34b0f525b672491fdce1e3f05230fec8234aa0`  
		Last Modified: Thu, 11 Jun 2020 23:40:37 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b913041eec5f62ec5eea20dff6704b98a2f7ba0b46d00474460b8089b795af`  
		Last Modified: Thu, 11 Jun 2020 23:40:37 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba6682ba9f796c005f62a2a48d350d8d97283b5b73eee5f04f4286c75f8cd20`  
		Last Modified: Thu, 11 Jun 2020 23:40:38 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce44500914f431d60d7eb5f6905da28a187ddd8964acf31d6174cfa6dac269df`  
		Last Modified: Thu, 11 Jun 2020 23:40:38 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-apache` - linux; 386

```console
$ docker pull friendica@sha256:033a824e28dee20112016b790b75449fdbb1b07400b25375b5c506141df039c4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167377437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffd8142c20a16bf596f9d2d450ae1f181a56b3bae79e154ba645037a8da0df3`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:33 GMT
ADD file:8ef252685ffefc58654053bf145c830928a2cf423a6c757180649df772f1523d in / 
# Tue, 09 Jun 2020 01:42:34 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 08:20:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 09 Jun 2020 08:20:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Jun 2020 08:21:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 08:21:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Jun 2020 08:21:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 09 Jun 2020 08:28:01 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 09 Jun 2020 08:28:01 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 09 Jun 2020 08:28:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 09 Jun 2020 08:28:13 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 09 Jun 2020 08:28:14 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 09 Jun 2020 08:28:14 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 09 Jun 2020 08:28:14 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 09 Jun 2020 08:28:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 08:28:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 08:28:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Jun 2020 08:28:15 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 11 Jun 2020 20:34:52 GMT
ENV PHP_VERSION=7.3.19
# Thu, 11 Jun 2020 20:34:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.19.tar.xz.asc
# Thu, 11 Jun 2020 20:34:53 GMT
ENV PHP_SHA256=6402faa19b1a8c4317c7612632bce985684a5bbae0980a5779a4019439882422 PHP_MD5=
# Thu, 11 Jun 2020 20:35:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 11 Jun 2020 20:35:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 Jun 2020 20:40:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	sed -e 's/stretch/buster/g' /etc/apt/sources.list > /etc/apt/sources.list.d/buster.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: -10'; 		echo; 		echo 'Package: libargon2*'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: 990'; 	} > /etc/apt/preferences.d/argon2-buster; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 11 Jun 2020 20:40:55 GMT
COPY multi:af24b1d34daac0a277386947399eceaaf20d3065d4be5db00b1d6466cf006c49 in /usr/local/bin/ 
# Thu, 11 Jun 2020 20:40:56 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 Jun 2020 20:40:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2020 20:40:57 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Jun 2020 20:40:57 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 11 Jun 2020 20:40:57 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2020 20:40:57 GMT
EXPOSE 80
# Thu, 11 Jun 2020 20:40:58 GMT
CMD ["apache2-foreground"]
# Fri, 12 Jun 2020 02:13:25 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         ssmtp         gnupg dirmngr     ;     rm -rf /var/lib/apt/lists/*;
# Fri, 12 Jun 2020 02:13:25 GMT
ENV TINI_VERSION=v0.18.0
# Fri, 12 Jun 2020 02:13:29 GMT
RUN export BUILD_ARCH=$(dpkg-architecture --query DEB_BUILD_ARCH)  && curl -L -o /sbin/tini https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}  && curl -L -o /tini.asc https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}.asc  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7  && gpg --batch --verify /tini.asc /sbin/tini  && chmod +x /sbin/tini
# Fri, 12 Jun 2020 02:16:10 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mysql-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         	--with-libdir=lib/$debMultiarch/ 	;     docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.2.1;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so       | awk '/=>/ { print $3 }'       | sort -u       | xargs -r dpkg-query -S       | cut -d: -f1       | sort -u       | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 02:16:11 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 12 Jun 2020 02:16:11 GMT
VOLUME [/var/www/html]
# Fri, 12 Jun 2020 02:16:12 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Fri, 12 Jun 2020 02:23:10 GMT
ENV FRIENDICA_VERSION=2020.06-dev
# Fri, 12 Jun 2020 02:23:10 GMT
ENV FRIENDICA_ADDONS=2020.06-dev
# Fri, 12 Jun 2020 02:23:10 GMT
COPY multi:79c18253e95b11e5d803cb19685ac5cb4fcedfeda73215d7e2e3f89d93570667 in / 
# Fri, 12 Jun 2020 02:23:11 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Fri, 12 Jun 2020 02:23:11 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Fri, 12 Jun 2020 02:23:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4ffbd6ec7974e514763a8d7d9fcf5e86e9440e2280e6e9561ea373b4bc50588e`  
		Last Modified: Tue, 09 Jun 2020 01:48:28 GMT  
		Size: 23.1 MB (23147892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463dfa508128348413fa1ffb6a611c6d99d79aa410e1df71c7f07df0cd5ad021`  
		Last Modified: Tue, 09 Jun 2020 10:02:57 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3599720fc3acd49e3af1c3be76cafd42195e9e8d8b0a8c27324e140c42d10fd`  
		Last Modified: Tue, 09 Jun 2020 10:03:20 GMT  
		Size: 71.5 MB (71490438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc50bf54aec4e5f21d1d4addb5a094817d5091a9af01d8818be1d07d9779d9a`  
		Last Modified: Tue, 09 Jun 2020 10:02:56 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3022ce4bbdbb1413d990f1eefa3c63417a1a2a0f5db8ec27b8677482155b876`  
		Last Modified: Tue, 09 Jun 2020 10:03:34 GMT  
		Size: 17.6 MB (17559296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fd0d61fc767f0b7d46451db341a918bf0829bc5c70cdfc4a782d69acf61d58`  
		Last Modified: Tue, 09 Jun 2020 10:03:28 GMT  
		Size: 435.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9744944fb0453b2086b24253a11b19fdb73b7bdb3989ffd8f393f12b474df78`  
		Last Modified: Tue, 09 Jun 2020 10:03:28 GMT  
		Size: 486.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b33355e2384cabbe48b3f95e0e1e89ee8a1ebbb03883996ce67c93be1db985`  
		Last Modified: Thu, 11 Jun 2020 22:31:45 GMT  
		Size: 12.5 MB (12465542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af98b9e86356cf3fd982ca875e1b5fd7a85d43bf92dbc163275fb14d8b206902`  
		Last Modified: Thu, 11 Jun 2020 22:31:43 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd51341ddb5b61173188634ad8665260c6488354f425806b79192c57248b4cd`  
		Last Modified: Thu, 11 Jun 2020 22:31:48 GMT  
		Size: 14.1 MB (14122943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7bb241cc2548ccc3c882e61d7648c7e08679ee5f819ce9877b68268bb0c9b0`  
		Last Modified: Thu, 11 Jun 2020 22:31:43 GMT  
		Size: 2.3 KB (2296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8909de86ec8595828ed2adb55c9890468c62001ca5d98c58473b1adcb1f2379f`  
		Last Modified: Thu, 11 Jun 2020 22:31:43 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d422c8053f375ccc1be31985c27d63ca209afc3b8bfaf4f8e499047b544aaa6`  
		Last Modified: Thu, 11 Jun 2020 22:31:43 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc40148e61849b73980d90672c7ef332ee7991cba8ed4f50883c9f923ed1392`  
		Last Modified: Fri, 12 Jun 2020 02:23:39 GMT  
		Size: 16.8 MB (16799265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289889bfb285f181c82fe8728cc3ee65434967c6e2e5213a155f71e6940c3b74`  
		Last Modified: Fri, 12 Jun 2020 02:23:35 GMT  
		Size: 16.3 KB (16316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ca3b592d160f6065c8bd9273d5c3d9e53ff3977922abfd6db62b24e58093b5`  
		Last Modified: Fri, 12 Jun 2020 02:23:36 GMT  
		Size: 11.8 MB (11765374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae9340c27cb39950837f7bf3058b2dbe9bfca756b8c45347e75d008f0e1c2f4`  
		Last Modified: Fri, 12 Jun 2020 02:23:33 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c87463c39bddad3a13a8bc2125666b1030c781ad73c71713c94d90d30c148e`  
		Last Modified: Fri, 12 Jun 2020 02:23:34 GMT  
		Size: 550.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb7ccdb55263a127cebc0320406bc85d07578b6ccc5365532cdcf5212d598d4`  
		Last Modified: Fri, 12 Jun 2020 02:23:33 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d2d03f682b228d1dbcad0532d6f79f8d652b0d03b6a3a18ce189795640a196`  
		Last Modified: Fri, 12 Jun 2020 02:23:33 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-apache` - linux; ppc64le

```console
$ docker pull friendica@sha256:276888c213cb3cd58e407a306468ab2c5d1d6839c432d66fcd0ac19a5bdedb6b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154400805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:070cf1747d3712081a0e095e4d2e15e7241ed4e4bb81e154267a0969edb39fd2`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:38 GMT
ADD file:41ec53d65aa183c2835f73989c9e4922f818e59774811eaa6e7395e5a36d5eab in / 
# Tue, 09 Jun 2020 01:25:42 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 06:19:34 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 09 Jun 2020 06:19:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Jun 2020 06:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 06:27:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Jun 2020 06:28:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 09 Jun 2020 06:40:14 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 09 Jun 2020 06:40:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 09 Jun 2020 06:42:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 09 Jun 2020 06:42:54 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 09 Jun 2020 06:43:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 09 Jun 2020 06:43:14 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 09 Jun 2020 06:43:18 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 09 Jun 2020 06:43:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 06:43:37 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 06:43:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Jun 2020 06:44:02 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 11 Jun 2020 19:46:42 GMT
ENV PHP_VERSION=7.3.19
# Thu, 11 Jun 2020 19:46:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.19.tar.xz.asc
# Thu, 11 Jun 2020 19:46:46 GMT
ENV PHP_SHA256=6402faa19b1a8c4317c7612632bce985684a5bbae0980a5779a4019439882422 PHP_MD5=
# Thu, 11 Jun 2020 19:48:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 11 Jun 2020 19:48:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 Jun 2020 19:52:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	sed -e 's/stretch/buster/g' /etc/apt/sources.list > /etc/apt/sources.list.d/buster.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: -10'; 		echo; 		echo 'Package: libargon2*'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: 990'; 	} > /etc/apt/preferences.d/argon2-buster; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 11 Jun 2020 19:52:34 GMT
COPY multi:af24b1d34daac0a277386947399eceaaf20d3065d4be5db00b1d6466cf006c49 in /usr/local/bin/ 
# Thu, 11 Jun 2020 19:52:41 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 Jun 2020 19:52:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2020 19:52:50 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Jun 2020 19:52:51 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 11 Jun 2020 19:52:59 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2020 19:53:05 GMT
EXPOSE 80
# Thu, 11 Jun 2020 19:53:08 GMT
CMD ["apache2-foreground"]
# Fri, 12 Jun 2020 01:14:00 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         ssmtp         gnupg dirmngr     ;     rm -rf /var/lib/apt/lists/*;
# Fri, 12 Jun 2020 01:14:07 GMT
ENV TINI_VERSION=v0.18.0
# Fri, 12 Jun 2020 01:14:22 GMT
RUN export BUILD_ARCH=$(dpkg-architecture --query DEB_BUILD_ARCH)  && curl -L -o /sbin/tini https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}  && curl -L -o /tini.asc https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}.asc  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7  && gpg --batch --verify /tini.asc /sbin/tini  && chmod +x /sbin/tini
# Fri, 12 Jun 2020 01:27:43 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mysql-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         	--with-libdir=lib/$debMultiarch/ 	;     docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.2.1;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so       | awk '/=>/ { print $3 }'       | sort -u       | xargs -r dpkg-query -S       | cut -d: -f1       | sort -u       | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 01:27:57 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 12 Jun 2020 01:28:01 GMT
VOLUME [/var/www/html]
# Fri, 12 Jun 2020 01:28:14 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Fri, 12 Jun 2020 01:49:47 GMT
ENV FRIENDICA_VERSION=2020.06-dev
# Fri, 12 Jun 2020 01:49:50 GMT
ENV FRIENDICA_ADDONS=2020.06-dev
# Fri, 12 Jun 2020 01:49:52 GMT
COPY multi:79c18253e95b11e5d803cb19685ac5cb4fcedfeda73215d7e2e3f89d93570667 in / 
# Fri, 12 Jun 2020 01:49:53 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Fri, 12 Jun 2020 01:49:54 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Fri, 12 Jun 2020 01:49:56 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a29e28607c9b96acae7ff89e56214e4339a87c59e40a6f030fa4cbcaab753f2c`  
		Last Modified: Tue, 09 Jun 2020 01:37:25 GMT  
		Size: 22.8 MB (22791269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f186626aaa4cd5bb161ad9d2ff0fbb907fa467c920f97408dad6a526dce5edf`  
		Last Modified: Tue, 09 Jun 2020 09:00:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bf7962f6d57c985a8a94c5a53357dd6e5456f90a666b55ba2a97b90851508d`  
		Last Modified: Tue, 09 Jun 2020 09:01:09 GMT  
		Size: 61.8 MB (61815598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9016218bc1cd4fdb9871844e822b1fdee1a70c384fa0c13782343b352e4de01`  
		Last Modified: Tue, 09 Jun 2020 09:00:52 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c0cc1d048f1730de55cdb124d6912938b0ee1e67403eea6928f5c97eefbae87`  
		Last Modified: Tue, 09 Jun 2020 09:01:35 GMT  
		Size: 17.3 MB (17341240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92efeee42782700ce3be500ad1ae9d9a0e793f572db8ada342967dc98b7a1d74`  
		Last Modified: Tue, 09 Jun 2020 09:01:31 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996ac857e1d9a97ed3b61513dd6a79a56057ae2585ee5eaf64db319332f2c31d`  
		Last Modified: Tue, 09 Jun 2020 09:01:29 GMT  
		Size: 518.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45daf51f43b4c4d3f9298e3fd761d8d50399a132562a9e882ebf8470ecd5ba16`  
		Last Modified: Thu, 11 Jun 2020 21:02:05 GMT  
		Size: 12.5 MB (12465018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbec56176482f1b4f39ebedfb43f5d03610c34aa85b16ea1339d7c73082198a7`  
		Last Modified: Thu, 11 Jun 2020 21:02:00 GMT  
		Size: 502.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe3fe0f93286f2e284c15dcde0dde11c6b0626918737a2a5769d7c99a2e7551`  
		Last Modified: Thu, 11 Jun 2020 21:02:03 GMT  
		Size: 13.6 MB (13585778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc75cdd7adf5c21163ec57255b6c852ae3626a3c8fb8e06fa3558e3feb1defe8`  
		Last Modified: Thu, 11 Jun 2020 21:02:00 GMT  
		Size: 2.3 KB (2293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db9814382cb3ad322d6377881ee4defa7250109934308a47afbd9f4a3ee1d1ca`  
		Last Modified: Thu, 11 Jun 2020 21:02:00 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129d2b00cc0e9013338bdc1a1a3669d4eeb82e60e17bcdb6cde80479b2e90f4e`  
		Last Modified: Thu, 11 Jun 2020 21:02:00 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83db65e3f8cd8210ab79b3fc29e36e6db3dcd014e78ec1be757e2b1da15188ae`  
		Last Modified: Fri, 12 Jun 2020 01:51:10 GMT  
		Size: 14.9 MB (14944689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c020e46103c7cbabfde2c81d7d38f1d6746ddb4bdc85561f5600ba6775ca33a3`  
		Last Modified: Fri, 12 Jun 2020 01:51:05 GMT  
		Size: 16.5 KB (16515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fdd34b398f2308ac30cf1f85b05bb6e395facd2a0c864b2cef990adfce44b4b`  
		Last Modified: Fri, 12 Jun 2020 01:51:04 GMT  
		Size: 11.4 MB (11430152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98306a000a338cc009114be30b7611bb82459958248f30db8259f1480839523f`  
		Last Modified: Fri, 12 Jun 2020 01:51:01 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54df804849c5f0929cda947063be9481a03ed2fcaf472b2a6fd17e9d5d9f3b72`  
		Last Modified: Fri, 12 Jun 2020 01:51:01 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49b150a0fb0dd04dfe107b3bf7c7de9634507a01fc77cd168b0dcf4c40ce240`  
		Last Modified: Fri, 12 Jun 2020 01:51:01 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccef47705596a601f8474b983b273e42e8205a7ec2f212a78df03a2f9d5ade43`  
		Last Modified: Fri, 12 Jun 2020 01:51:01 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
