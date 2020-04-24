## `friendica:latest`

```console
$ docker pull friendica@sha256:b645870d8fe1c80fb422dc13153b54d13433f676e442349c478bdee939c192c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `friendica:latest` - linux; amd64

```console
$ docker pull friendica@sha256:ceb3db92fdbadc7f123438d95efde9bdd8efbcaf59bc5360f873004a5b543117
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.9 MB (217939860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75299c53547095285805d88818148efcc7fd91d6102ceb1909de7512901c83eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 17:26:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Apr 2020 17:26:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Apr 2020 17:27:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 17:27:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Apr 2020 17:27:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 23 Apr 2020 17:34:39 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 23 Apr 2020 17:34:39 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 23 Apr 2020 17:34:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 23 Apr 2020 17:34:49 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 23 Apr 2020 17:34:50 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 23 Apr 2020 17:34:50 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Thu, 23 Apr 2020 17:34:50 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Thu, 23 Apr 2020 17:34:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 17:34:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 17:34:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Apr 2020 17:34:51 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 23 Apr 2020 17:34:51 GMT
ENV PHP_VERSION=7.3.17
# Thu, 23 Apr 2020 17:34:51 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.17.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.17.tar.xz.asc/from/this/mirror
# Thu, 23 Apr 2020 17:34:51 GMT
ENV PHP_SHA256=6a30304c27f7e7a94538f5ffec599f600ee93aedbbecad8aa4f8bec539b10ad8 PHP_MD5=
# Thu, 23 Apr 2020 17:35:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Apr 2020 17:35:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Apr 2020 17:39:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	sed -e 's/stretch/buster/g' /etc/apt/sources.list > /etc/apt/sources.list.d/buster.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: -10'; 		echo; 		echo 'Package: libargon2*'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: 990'; 	} > /etc/apt/preferences.d/argon2-buster; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Apr 2020 17:39:24 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Thu, 23 Apr 2020 17:39:25 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Apr 2020 17:39:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Apr 2020 17:39:25 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Apr 2020 17:39:25 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 23 Apr 2020 17:39:25 GMT
WORKDIR /var/www/html
# Thu, 23 Apr 2020 17:39:26 GMT
EXPOSE 80
# Thu, 23 Apr 2020 17:39:26 GMT
CMD ["apache2-foreground"]
# Fri, 24 Apr 2020 11:24:03 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         ssmtp         gnupg dirmngr     ;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Apr 2020 11:24:04 GMT
ENV TINI_VERSION=v0.18.0
# Fri, 24 Apr 2020 11:24:07 GMT
RUN export BUILD_ARCH=$(dpkg-architecture --query DEB_BUILD_ARCH)  && curl -L -o /sbin/tini https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}  && curl -L -o /tini.asc https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}.asc  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7  && gpg --batch --verify /tini.asc /sbin/tini  && chmod +x /sbin/tini
# Fri, 24 Apr 2020 11:26:23 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mysql-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         	--with-libdir=lib/$debMultiarch/ 	;     docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.2.1;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so       | awk '/=>/ { print $3 }'       | sort -u       | xargs -r dpkg-query -S       | cut -d: -f1       | sort -u       | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:26:24 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 24 Apr 2020 11:26:24 GMT
VOLUME [/var/www/html]
# Fri, 24 Apr 2020 11:26:25 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Fri, 24 Apr 2020 11:26:25 GMT
ENV FRIENDICA_VERSION=2020.03
# Fri, 24 Apr 2020 11:26:26 GMT
ENV FRIENDICA_ADDONS=2020.03
# Fri, 24 Apr 2020 11:26:44 GMT
RUN set -ex;     curl -fsSL -o friendica.tar.gz         "https://github.com/friendica/friendica/archive/${FRIENDICA_VERSION}.tar.gz";     tar -xzf friendica.tar.gz -C /usr/src/;     rm friendica.tar.gz;     mv -f /usr/src/friendica-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;     curl -fsSL -o friendica_addons.tar.gz         "https://github.com/friendica/friendica-addons/archive/${FRIENDICA_ADDONS}.tar.gz";     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica_addons.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica_addons.tar.gz;     /usr/src/friendica/bin/composer.phar install --no-dev -d /usr/src/friendica;
# Fri, 24 Apr 2020 11:26:44 GMT
COPY multi:4ce6218883572e2819aeaf93851e15069cd19fdc80ac04b89a1c335ca7e4d501 in / 
# Fri, 24 Apr 2020 11:26:45 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Fri, 24 Apr 2020 11:26:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Apr 2020 11:26:45 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087a082ea6d9163657392e26b03ba0ee9c934b3577f6da7b5ed154e1507c86f6`  
		Last Modified: Thu, 23 Apr 2020 18:48:51 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fad012f4b99187dc797b4a013e8da79bd442a15ceb8b8fc49d5931bab4967d`  
		Last Modified: Thu, 23 Apr 2020 18:49:08 GMT  
		Size: 67.4 MB (67447140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6174dbcc06b5acdf0e70550d5ff6545376de8c5faa112dfcdb9e10c24c41ea28`  
		Last Modified: Thu, 23 Apr 2020 18:48:50 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e8d7af56940207c863a663a8341dc8bcd340bf7eb2a7244fe4a528078c0c16`  
		Last Modified: Thu, 23 Apr 2020 18:49:19 GMT  
		Size: 17.1 MB (17125390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a107ca22db66820a40800842b8c36edd20985821d020080ecb11f80687d15d18`  
		Last Modified: Thu, 23 Apr 2020 18:49:15 GMT  
		Size: 430.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a40191c5b70fcb0e777e86d9b626a355dc4d05c961ea0d7df682aa92fe8b554`  
		Last Modified: Thu, 23 Apr 2020 18:49:15 GMT  
		Size: 485.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff785eceffe5e4dd3ff353c660affc560f281f48a0070f192cb825b6db992bf1`  
		Last Modified: Thu, 23 Apr 2020 18:49:16 GMT  
		Size: 12.5 MB (12464837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b0390b1a989e0acc56956c43017c42b3b89a1e8163e06530833a596185c030`  
		Last Modified: Thu, 23 Apr 2020 18:49:14 GMT  
		Size: 502.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d1b837d160fb74e060c38b995e98c1686644a27a8070b695f789da2342169f`  
		Last Modified: Thu, 23 Apr 2020 18:49:18 GMT  
		Size: 13.8 MB (13797318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdce6bb2a36af879ee5cfb31adcb68051416f1f12e63ce2ce0652b7b569fa605`  
		Last Modified: Thu, 23 Apr 2020 18:49:14 GMT  
		Size: 2.2 KB (2244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4d473554be52ab435f269ebd694d58f93f36fd919fed70443ac5c77f9154e8`  
		Last Modified: Thu, 23 Apr 2020 18:49:14 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0380cc171781cbfb9c6f426b763ca75643807b8ea7a3b21756af63384c08201`  
		Last Modified: Thu, 23 Apr 2020 18:49:14 GMT  
		Size: 906.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1a20d44943326daed421f64cd274fd9b8788721c59c37497d2c3fc8cbd035c`  
		Last Modified: Fri, 24 Apr 2020 11:30:25 GMT  
		Size: 15.1 MB (15078561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e6d8cf8368edf55d8dfd95e9a4d749dbf8893303e800e3143d8df6f469d82d`  
		Last Modified: Fri, 24 Apr 2020 11:30:22 GMT  
		Size: 16.3 KB (16290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b47b0d4e6ce528e9d6cbdf943fdf79852b5f0cfd258450a05699320fe756dd0`  
		Last Modified: Fri, 24 Apr 2020 11:30:25 GMT  
		Size: 11.7 MB (11704219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409c55c497a583cd3a1f852672eb46ff4fc4d44573b0d7d2bc81bc202d2b32bf`  
		Last Modified: Fri, 24 Apr 2020 11:30:21 GMT  
		Size: 564.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df30bff340c1f2c7ae88597ebe1913c36d1153425beb4fea7b0c419593a426e`  
		Last Modified: Fri, 24 Apr 2020 11:30:21 GMT  
		Size: 539.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0fb18b7eea08cb51e2e3b71285f081215026529da0ff5c72b8917df027757b`  
		Last Modified: Fri, 24 Apr 2020 11:30:29 GMT  
		Size: 57.8 MB (57782963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22cd561d021a1d315b33c21979235cf331cf44a60fedba88944e01cbda814c7`  
		Last Modified: Fri, 24 Apr 2020 11:30:21 GMT  
		Size: 2.2 KB (2192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f82dfb3011b3f86393923eedf60eaa216f7cb45afc480749175f3b4131236c`  
		Last Modified: Fri, 24 Apr 2020 11:30:21 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:latest` - linux; arm variant v5

```console
$ docker pull friendica@sha256:cbacfcbf3f139ad8177eb8e9cced83849f834afc8bac26f28e59561776eebb20
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.1 MB (204141279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5a9e5e840e481ed22d7887c94c3b1dfefe2b65a6c0a003964ca65bcc486ece`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 23 Apr 2020 00:56:04 GMT
ADD file:60586a4bfaca91a5985bf13744e752136a597186e5bd3aa0eddf7bdd600130fe in / 
# Thu, 23 Apr 2020 00:56:06 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 05:39:58 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Apr 2020 05:39:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Apr 2020 05:40:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 05:40:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Apr 2020 05:40:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 23 Apr 2020 05:45:19 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 23 Apr 2020 05:45:20 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 23 Apr 2020 05:45:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 23 Apr 2020 05:45:46 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 23 Apr 2020 05:45:47 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 23 Apr 2020 05:45:48 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Thu, 23 Apr 2020 05:45:49 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Thu, 23 Apr 2020 05:45:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 05:45:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 05:45:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Apr 2020 05:45:51 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 23 Apr 2020 05:45:52 GMT
ENV PHP_VERSION=7.3.17
# Thu, 23 Apr 2020 05:45:53 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.17.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.17.tar.xz.asc/from/this/mirror
# Thu, 23 Apr 2020 05:45:53 GMT
ENV PHP_SHA256=6a30304c27f7e7a94538f5ffec599f600ee93aedbbecad8aa4f8bec539b10ad8 PHP_MD5=
# Thu, 23 Apr 2020 05:46:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Apr 2020 05:46:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Apr 2020 05:49:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	sed -e 's/stretch/buster/g' /etc/apt/sources.list > /etc/apt/sources.list.d/buster.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: -10'; 		echo; 		echo 'Package: libargon2*'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: 990'; 	} > /etc/apt/preferences.d/argon2-buster; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Apr 2020 05:49:21 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Thu, 23 Apr 2020 05:49:24 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Apr 2020 05:49:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Apr 2020 05:49:25 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Apr 2020 05:49:26 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 23 Apr 2020 05:49:28 GMT
WORKDIR /var/www/html
# Thu, 23 Apr 2020 05:49:29 GMT
EXPOSE 80
# Thu, 23 Apr 2020 05:49:29 GMT
CMD ["apache2-foreground"]
# Thu, 23 Apr 2020 10:43:32 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         ssmtp         gnupg dirmngr     ;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Apr 2020 10:43:34 GMT
ENV TINI_VERSION=v0.18.0
# Thu, 23 Apr 2020 10:43:39 GMT
RUN export BUILD_ARCH=$(dpkg-architecture --query DEB_BUILD_ARCH)  && curl -L -o /sbin/tini https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}  && curl -L -o /tini.asc https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}.asc  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7  && gpg --batch --verify /tini.asc /sbin/tini  && chmod +x /sbin/tini
# Thu, 23 Apr 2020 10:49:15 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mysql-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         	--with-libdir=lib/$debMultiarch/ 	;     docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.2.1;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so       | awk '/=>/ { print $3 }'       | sort -u       | xargs -r dpkg-query -S       | cut -d: -f1       | sort -u       | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 10:49:18 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Thu, 23 Apr 2020 10:49:19 GMT
VOLUME [/var/www/html]
# Thu, 23 Apr 2020 10:49:22 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Thu, 23 Apr 2020 10:49:24 GMT
ENV FRIENDICA_VERSION=2020.03
# Thu, 23 Apr 2020 10:49:25 GMT
ENV FRIENDICA_ADDONS=2020.03
# Thu, 23 Apr 2020 10:50:12 GMT
RUN set -ex;     curl -fsSL -o friendica.tar.gz         "https://github.com/friendica/friendica/archive/${FRIENDICA_VERSION}.tar.gz";     tar -xzf friendica.tar.gz -C /usr/src/;     rm friendica.tar.gz;     mv -f /usr/src/friendica-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;     curl -fsSL -o friendica_addons.tar.gz         "https://github.com/friendica/friendica-addons/archive/${FRIENDICA_ADDONS}.tar.gz";     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica_addons.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica_addons.tar.gz;     /usr/src/friendica/bin/composer.phar install --no-dev -d /usr/src/friendica;
# Thu, 23 Apr 2020 10:50:16 GMT
COPY multi:4ce6218883572e2819aeaf93851e15069cd19fdc80ac04b89a1c335ca7e4d501 in / 
# Thu, 23 Apr 2020 10:50:17 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Thu, 23 Apr 2020 10:50:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 10:50:19 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a07595075223d769a641d7054a9dd729aaba7d95a05cf2e83dd10958a78d9e04`  
		Last Modified: Thu, 23 Apr 2020 01:03:53 GMT  
		Size: 21.2 MB (21190846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee3c0e8ff510fe7390f349348d80233a411dbd9d7d62acb4d504db346dea502`  
		Last Modified: Thu, 23 Apr 2020 06:37:28 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854bbb8af73019432d5ceb2dd90b710ea4e88afd0fc67666a8a97d6504dab6af`  
		Last Modified: Thu, 23 Apr 2020 06:37:51 GMT  
		Size: 57.5 MB (57485338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2feb565bb21d645270b67cf8ee21a6117add8e6938367cc3979b8f658b6dba0`  
		Last Modified: Thu, 23 Apr 2020 06:37:28 GMT  
		Size: 289.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f6d9fd8b7bb7f59559c880ae0c97e55af16b8ff75d497679f2f82827d49a26`  
		Last Modified: Thu, 23 Apr 2020 06:38:14 GMT  
		Size: 16.6 MB (16644293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13d8a448cb32e5d36014a076674d43ae4bbd0805e75afa1156b685c32ef1341`  
		Last Modified: Thu, 23 Apr 2020 06:38:08 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5d1460469940e8cf3d7f4481a94df11abed26f00e4f16266ceab24a1c168e8`  
		Last Modified: Thu, 23 Apr 2020 06:38:08 GMT  
		Size: 517.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e0ca919cffeda75002b45758f33d6dfc0e14d4d2af5c268c937c1da1cb5819`  
		Last Modified: Thu, 23 Apr 2020 06:38:10 GMT  
		Size: 12.5 MB (12463139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89bb5cf5d17a145db10c333ba5764318d267897e1099f378919b128019a5625e`  
		Last Modified: Thu, 23 Apr 2020 06:38:06 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff877853c0982c948e7981f2ef6b5798ec95244663d9712765e2fee9fd8cade6`  
		Last Modified: Thu, 23 Apr 2020 06:38:10 GMT  
		Size: 13.1 MB (13069473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb02a75bc74d660a265e25d81962e953a08f7c888e6f9aec2bfa714a86a6a85`  
		Last Modified: Thu, 23 Apr 2020 06:38:05 GMT  
		Size: 2.2 KB (2243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886ec3e80d1c11a9fb08aedef46a90702eec87fa00661600cf32577ada1839b7`  
		Last Modified: Thu, 23 Apr 2020 06:38:05 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deaab7e84b8426848124b9f82b9a8ddafa598d123a91345c250dc667b98ccad8`  
		Last Modified: Thu, 23 Apr 2020 06:38:05 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72d1274ca9d0d07fad6691d783fea3fb4b6ee8731f369b7e16c5ad92d1894a1`  
		Last Modified: Thu, 23 Apr 2020 10:58:19 GMT  
		Size: 14.0 MB (14013476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd207bb055be97f426a7be1065a86ab8b377ca6e5304ef2bdf0017bf0823cd6`  
		Last Modified: Thu, 23 Apr 2020 10:58:14 GMT  
		Size: 15.7 KB (15710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c229c41f6aa454fee48fd6ca88b3205921e3eb5b76ceceeb45a5ac4af349aec3`  
		Last Modified: Thu, 23 Apr 2020 10:58:18 GMT  
		Size: 11.5 MB (11465684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3afb2475acc795c2f04f99ad0b36ce85ff8dd59a0b691ea59fdb776fc04618`  
		Last Modified: Thu, 23 Apr 2020 10:58:11 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b10ee99fcf39e39f039b018a9d40573832421bb86c3ece504f099f449b171e`  
		Last Modified: Thu, 23 Apr 2020 10:58:11 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba9e54231d9352cfa4a705158e275a9c33ba62a1544f589802eaf8d38016d5d`  
		Last Modified: Thu, 23 Apr 2020 10:58:27 GMT  
		Size: 57.8 MB (57783502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f42841658d2887393a4dc8653537a81dd7d5af2e3ffbb797a5fbf4c5c75465bf`  
		Last Modified: Thu, 23 Apr 2020 10:58:11 GMT  
		Size: 2.2 KB (2192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c04e708b13868f5b809cec62d7b7448ceefd76a69f2ba3e31228a8b598fec44`  
		Last Modified: Thu, 23 Apr 2020 10:58:12 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:latest` - linux; arm variant v7

```console
$ docker pull friendica@sha256:b0f700dc7207563c3597f1915cd2c02b82391ce5700f1a0e52145ef7af707dc2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.1 MB (195117445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0e94865137950889d190a4992db2862513544f930648d84ab525f3a0bec8ae5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 23 Apr 2020 01:07:37 GMT
ADD file:d34df50b16579a75bfaa8cce488b954cd5cdc110c3eeda26cfb1d2e285dd53f2 in / 
# Thu, 23 Apr 2020 01:07:39 GMT
CMD ["bash"]
# Fri, 24 Apr 2020 09:45:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 24 Apr 2020 09:45:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 24 Apr 2020 09:46:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 09:46:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 24 Apr 2020 09:46:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 24 Apr 2020 09:50:50 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 24 Apr 2020 09:50:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 24 Apr 2020 09:51:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 24 Apr 2020 09:51:18 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 24 Apr 2020 09:51:21 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 24 Apr 2020 09:51:21 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 24 Apr 2020 09:51:22 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 24 Apr 2020 09:51:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Apr 2020 09:51:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Apr 2020 09:51:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 24 Apr 2020 09:51:24 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 24 Apr 2020 09:51:25 GMT
ENV PHP_VERSION=7.3.17
# Fri, 24 Apr 2020 09:51:26 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.17.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.17.tar.xz.asc/from/this/mirror
# Fri, 24 Apr 2020 09:51:27 GMT
ENV PHP_SHA256=6a30304c27f7e7a94538f5ffec599f600ee93aedbbecad8aa4f8bec539b10ad8 PHP_MD5=
# Fri, 24 Apr 2020 09:51:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Apr 2020 09:51:45 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Apr 2020 09:54:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	sed -e 's/stretch/buster/g' /etc/apt/sources.list > /etc/apt/sources.list.d/buster.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: -10'; 		echo; 		echo 'Package: libargon2*'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: 990'; 	} > /etc/apt/preferences.d/argon2-buster; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Apr 2020 09:54:49 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Fri, 24 Apr 2020 09:54:52 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Apr 2020 09:54:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Apr 2020 09:54:53 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Apr 2020 09:54:54 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 24 Apr 2020 09:54:54 GMT
WORKDIR /var/www/html
# Fri, 24 Apr 2020 09:54:55 GMT
EXPOSE 80
# Fri, 24 Apr 2020 09:54:56 GMT
CMD ["apache2-foreground"]
# Fri, 24 Apr 2020 18:18:20 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         ssmtp         gnupg dirmngr     ;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Apr 2020 18:18:21 GMT
ENV TINI_VERSION=v0.18.0
# Fri, 24 Apr 2020 18:18:26 GMT
RUN export BUILD_ARCH=$(dpkg-architecture --query DEB_BUILD_ARCH)  && curl -L -o /sbin/tini https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}  && curl -L -o /tini.asc https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}.asc  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7  && gpg --batch --verify /tini.asc /sbin/tini  && chmod +x /sbin/tini
# Fri, 24 Apr 2020 18:23:29 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mysql-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         	--with-libdir=lib/$debMultiarch/ 	;     docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.2.1;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so       | awk '/=>/ { print $3 }'       | sort -u       | xargs -r dpkg-query -S       | cut -d: -f1       | sort -u       | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 18:23:32 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 24 Apr 2020 18:23:33 GMT
VOLUME [/var/www/html]
# Fri, 24 Apr 2020 18:23:36 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Fri, 24 Apr 2020 18:23:37 GMT
ENV FRIENDICA_VERSION=2020.03
# Fri, 24 Apr 2020 18:23:37 GMT
ENV FRIENDICA_ADDONS=2020.03
# Fri, 24 Apr 2020 18:24:12 GMT
RUN set -ex;     curl -fsSL -o friendica.tar.gz         "https://github.com/friendica/friendica/archive/${FRIENDICA_VERSION}.tar.gz";     tar -xzf friendica.tar.gz -C /usr/src/;     rm friendica.tar.gz;     mv -f /usr/src/friendica-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;     curl -fsSL -o friendica_addons.tar.gz         "https://github.com/friendica/friendica-addons/archive/${FRIENDICA_ADDONS}.tar.gz";     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica_addons.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica_addons.tar.gz;     /usr/src/friendica/bin/composer.phar install --no-dev -d /usr/src/friendica;
# Fri, 24 Apr 2020 18:24:15 GMT
COPY multi:4ce6218883572e2819aeaf93851e15069cd19fdc80ac04b89a1c335ca7e4d501 in / 
# Fri, 24 Apr 2020 18:24:16 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Fri, 24 Apr 2020 18:24:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Apr 2020 18:24:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:9a298b6c339c562fea435ecbf6369ef71a818d1df1539a329088cdd265ed548f`  
		Last Modified: Thu, 23 Apr 2020 01:14:30 GMT  
		Size: 19.3 MB (19298463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f62408eb4b41f81ce3de58884ba07b2f158540eeb35958297ef5dc13ad5fde5`  
		Last Modified: Fri, 24 Apr 2020 11:21:05 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e583de0e89d8d9b1123df25a12a9f79915dc7627c5a9c8b59f04f597e369b1`  
		Last Modified: Fri, 24 Apr 2020 11:21:21 GMT  
		Size: 53.6 MB (53595038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee4055ba15c5965ecf69fb8f2ac164ade291a7d9f89c3a2bbdda261546e778c`  
		Last Modified: Fri, 24 Apr 2020 11:21:05 GMT  
		Size: 288.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341402225bb0fb0c795356a3eb5aace64156a7d4e423745310709f5236c35e2f`  
		Last Modified: Fri, 24 Apr 2020 11:21:43 GMT  
		Size: 16.2 MB (16159943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ce13f12fbd7a265b9462b0380e2e9138d4057d4d76f7b4f1737f0ae21a3a99`  
		Last Modified: Fri, 24 Apr 2020 11:21:39 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc7eae83feedcee5e8918fc60c07a5eb69703b91ab2b2f1f982430b3e2e2ae3`  
		Last Modified: Fri, 24 Apr 2020 11:21:39 GMT  
		Size: 515.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ca974db4ad02564482d993c4014a81cd9d45c8fccd3f488b7433eff3a1adad`  
		Last Modified: Fri, 24 Apr 2020 11:21:41 GMT  
		Size: 12.5 MB (12463108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52fd3eb375c6567c0eeef00ff31d662935b3caf34f5b883521506e77cad2d69`  
		Last Modified: Fri, 24 Apr 2020 11:21:37 GMT  
		Size: 502.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a9e30f42c841d88024a0eba3978304d11f712c40457b55558a0e03faa97cd41`  
		Last Modified: Fri, 24 Apr 2020 11:21:40 GMT  
		Size: 12.4 MB (12386779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6f4978bdc0a4574f88d413e1d1f0ccf8e1536dd51427261eab3e4b6c742a76`  
		Last Modified: Fri, 24 Apr 2020 11:21:37 GMT  
		Size: 2.2 KB (2239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9653924a7e3af8e34952ac25c6a5c8af466812bf114b1984cd8d2c36d399f5`  
		Last Modified: Fri, 24 Apr 2020 11:21:37 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff99c391eab537c0200d48505da36e648b3c0033955e3663ac0f39bdaf7476a`  
		Last Modified: Fri, 24 Apr 2020 11:21:36 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:294fe173f8fdd345329e327f98bc3aec7b3b3bc4a6315600a6cf2d8b6484c401`  
		Last Modified: Fri, 24 Apr 2020 18:35:05 GMT  
		Size: 12.7 MB (12735778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da91758604f9f35a94bbd6b2307998ae7a6c07cc1b21e07e4aa02e44aaa52693`  
		Last Modified: Fri, 24 Apr 2020 18:35:03 GMT  
		Size: 14.9 KB (14949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ada5f8dcb5c1e184748385320a28e9779a29840c08849ba5df1bbef2b92eb8`  
		Last Modified: Fri, 24 Apr 2020 18:35:05 GMT  
		Size: 10.7 MB (10670176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6241a513646ab5aed863364c4f6ca48e4f26258845d4ad60cf63a0ba616a18c`  
		Last Modified: Fri, 24 Apr 2020 18:35:00 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7b1b5355a96fa7079c7fee8b17c4041b74ba474132442a37038343c4c8d5ec`  
		Last Modified: Fri, 24 Apr 2020 18:35:00 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c1e8f35e6c20988b8896ed9ae1d6cef42494ae106902b11c1f4465d591a450`  
		Last Modified: Fri, 24 Apr 2020 18:35:16 GMT  
		Size: 57.8 MB (57783396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89f14005e8c7337d12cdab192b977a9480e56f74e159e88663fd049e3712e22`  
		Last Modified: Fri, 24 Apr 2020 18:35:00 GMT  
		Size: 2.2 KB (2192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8814a314b4d16344b288f3a891b3fe8fe767465df957e54735df19b1b4fb1ec2`  
		Last Modified: Fri, 24 Apr 2020 18:35:00 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:latest` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:5b129d5640a0c459786f9b876f35041d1bd468f4591c02efb1a74363ec25fd5e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.1 MB (202143914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20aede37c8e051e1cc98c2a0c3d994974e6db419ea9b1d9a46bb5ca0fd0870f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 23 Apr 2020 00:59:03 GMT
ADD file:da103bb73d1c28697756e3558eaa49cc235b07dfea96895f56929eb8fd0fb67c in / 
# Thu, 23 Apr 2020 00:59:05 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 16:57:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Apr 2020 16:57:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Apr 2020 16:58:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 16:58:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Apr 2020 16:58:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 23 Apr 2020 17:02:34 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 23 Apr 2020 17:02:35 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 23 Apr 2020 17:03:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 23 Apr 2020 17:03:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 23 Apr 2020 17:03:05 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 23 Apr 2020 17:03:06 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Thu, 23 Apr 2020 17:03:07 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Thu, 23 Apr 2020 17:03:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 17:03:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 17:03:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Apr 2020 17:03:10 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 23 Apr 2020 17:03:11 GMT
ENV PHP_VERSION=7.3.17
# Thu, 23 Apr 2020 17:03:12 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.17.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.17.tar.xz.asc/from/this/mirror
# Thu, 23 Apr 2020 17:03:13 GMT
ENV PHP_SHA256=6a30304c27f7e7a94538f5ffec599f600ee93aedbbecad8aa4f8bec539b10ad8 PHP_MD5=
# Thu, 23 Apr 2020 17:03:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Apr 2020 17:03:29 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Apr 2020 17:06:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	sed -e 's/stretch/buster/g' /etc/apt/sources.list > /etc/apt/sources.list.d/buster.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: -10'; 		echo; 		echo 'Package: libargon2*'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: 990'; 	} > /etc/apt/preferences.d/argon2-buster; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Apr 2020 17:06:25 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Thu, 23 Apr 2020 17:06:30 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Apr 2020 17:06:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Apr 2020 17:06:32 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Apr 2020 17:06:33 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 23 Apr 2020 17:06:34 GMT
WORKDIR /var/www/html
# Thu, 23 Apr 2020 17:06:35 GMT
EXPOSE 80
# Thu, 23 Apr 2020 17:06:35 GMT
CMD ["apache2-foreground"]
# Fri, 24 Apr 2020 02:07:37 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         ssmtp         gnupg dirmngr     ;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Apr 2020 02:07:40 GMT
ENV TINI_VERSION=v0.18.0
# Fri, 24 Apr 2020 02:07:47 GMT
RUN export BUILD_ARCH=$(dpkg-architecture --query DEB_BUILD_ARCH)  && curl -L -o /sbin/tini https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}  && curl -L -o /tini.asc https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}.asc  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7  && gpg --batch --verify /tini.asc /sbin/tini  && chmod +x /sbin/tini
# Fri, 24 Apr 2020 02:13:19 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mysql-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         	--with-libdir=lib/$debMultiarch/ 	;     docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.2.1;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so       | awk '/=>/ { print $3 }'       | sort -u       | xargs -r dpkg-query -S       | cut -d: -f1       | sort -u       | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 02:13:21 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 24 Apr 2020 02:13:22 GMT
VOLUME [/var/www/html]
# Fri, 24 Apr 2020 02:13:24 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Fri, 24 Apr 2020 02:13:25 GMT
ENV FRIENDICA_VERSION=2020.03
# Fri, 24 Apr 2020 02:13:25 GMT
ENV FRIENDICA_ADDONS=2020.03
# Fri, 24 Apr 2020 02:14:16 GMT
RUN set -ex;     curl -fsSL -o friendica.tar.gz         "https://github.com/friendica/friendica/archive/${FRIENDICA_VERSION}.tar.gz";     tar -xzf friendica.tar.gz -C /usr/src/;     rm friendica.tar.gz;     mv -f /usr/src/friendica-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;     curl -fsSL -o friendica_addons.tar.gz         "https://github.com/friendica/friendica-addons/archive/${FRIENDICA_ADDONS}.tar.gz";     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica_addons.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica_addons.tar.gz;     /usr/src/friendica/bin/composer.phar install --no-dev -d /usr/src/friendica;
# Fri, 24 Apr 2020 02:14:18 GMT
COPY multi:4ce6218883572e2819aeaf93851e15069cd19fdc80ac04b89a1c335ca7e4d501 in / 
# Fri, 24 Apr 2020 02:14:20 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Fri, 24 Apr 2020 02:14:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Apr 2020 02:14:24 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:191ef9a1fd49ca372c51c235b6f6f4579bddb73cfd390f67b4878b465f9bdfd2`  
		Last Modified: Thu, 23 Apr 2020 01:05:53 GMT  
		Size: 20.4 MB (20370093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2249841dff507ba101a4560a90a568aa2170e36d061c1443fd9190b24026cc21`  
		Last Modified: Thu, 23 Apr 2020 17:55:35 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8c2b918818c3fe5c4c97bf9c15daca9386e8df63856fe6ffbb35e62e1d23c5`  
		Last Modified: Thu, 23 Apr 2020 17:55:53 GMT  
		Size: 57.6 MB (57630142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe654e25c4326722f4b39ebc57d5563f728cf8da5662c3279fcfb69e7f60f57`  
		Last Modified: Thu, 23 Apr 2020 17:55:34 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25054e9f5059d1f3e81eab22e45c0243aa76c7dfac71194d593fa4f0728eb4e`  
		Last Modified: Thu, 23 Apr 2020 17:56:13 GMT  
		Size: 16.7 MB (16708470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9b86c9f693a887c8ecf1420042d28615091b8eddf538fbd1e8815d1ba85c0f3`  
		Last Modified: Thu, 23 Apr 2020 17:56:08 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8ca88e3ab17a189d9dafc2084a3475c713c88950b5d40db878437a5b61e2fc`  
		Last Modified: Thu, 23 Apr 2020 17:56:07 GMT  
		Size: 518.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6f26dc71a0fceef4876c9ff22b9800f757e18b4771d1d86c59efc8a78a16dd`  
		Last Modified: Thu, 23 Apr 2020 17:56:10 GMT  
		Size: 12.5 MB (12463014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131b07c63eff4d54655adfccd0e6b73f5eb47910b40acf7ade470735f7541659`  
		Last Modified: Thu, 23 Apr 2020 17:56:06 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172bd7132ab8bc9a8bb6485fe1102be6120be204bdb2495135328d9fbf072ee7`  
		Last Modified: Thu, 23 Apr 2020 17:56:09 GMT  
		Size: 12.9 MB (12861506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37b9bc198fc4fdaf1aed059f232ae0d1a38e471ff7a71662bada7e5f2638c1c`  
		Last Modified: Thu, 23 Apr 2020 17:56:06 GMT  
		Size: 2.2 KB (2240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c7a99a9ea01fdea37454b15471b11d28d3cb242f7e5910d4e3f9fde43f5747`  
		Last Modified: Thu, 23 Apr 2020 17:56:05 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d42880411aed0a8c57c849f8d9c6867ba1ac257fee9578d10bb20faec58498a9`  
		Last Modified: Thu, 23 Apr 2020 17:56:06 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a531aa7f2e0aff17cf79321c222ac833eb2a6944e585be833f013434bd2379`  
		Last Modified: Fri, 24 Apr 2020 02:22:32 GMT  
		Size: 13.6 MB (13617672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cfdbbd02e8686091b1e92203669658cd483fac28f0c3d04018b7c04ccee1b5`  
		Last Modified: Fri, 24 Apr 2020 02:22:28 GMT  
		Size: 15.9 KB (15904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54467d39bf4c8ac64c6df52a4d436539d5499cae9b904e082f60d005d5e26d4b`  
		Last Modified: Fri, 24 Apr 2020 02:22:31 GMT  
		Size: 10.7 MB (10683632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09fad1e5af5a1eb0202ea1d38774e330691402ed9fd595eae2d6f243097ad21b`  
		Last Modified: Fri, 24 Apr 2020 02:22:26 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f96df5da210b4a32e89fed5595c5b55d8f468c503c4a85a0ed9f1f4196c49f`  
		Last Modified: Fri, 24 Apr 2020 02:22:26 GMT  
		Size: 540.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ededd014ce0fada4093f3ab0cb14514a06d0c56e785414aae31850eb5f7365`  
		Last Modified: Fri, 24 Apr 2020 02:22:40 GMT  
		Size: 57.8 MB (57783669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d708ce9c8c4d2289e7e988bc3db8ecd4c1a8b0c26ff64663abe732c9ef5d8269`  
		Last Modified: Fri, 24 Apr 2020 02:22:26 GMT  
		Size: 2.2 KB (2193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1935c615693656841688a15f7bdaf86c33558dd4ce58c7ee2fd9b162255a1a51`  
		Last Modified: Fri, 24 Apr 2020 02:22:26 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:latest` - linux; 386

```console
$ docker pull friendica@sha256:7931f843558b14ba157e2f1e7293f7ba451d1b7a6797473663c1a9872c173fe1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.2 MB (225183784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799d084958edbd8a95b9c84e8f4afd1bc3912c69e06e2b811df3cd7666ba6f01`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 12:58:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Apr 2020 12:58:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Apr 2020 12:59:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 12:59:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Apr 2020 12:59:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 23 Apr 2020 13:05:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 23 Apr 2020 13:05:31 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 23 Apr 2020 13:05:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 23 Apr 2020 13:05:44 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 23 Apr 2020 13:05:45 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 23 Apr 2020 13:05:45 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Thu, 23 Apr 2020 13:05:45 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Thu, 23 Apr 2020 13:05:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 13:05:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 13:05:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Apr 2020 13:05:46 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 23 Apr 2020 13:05:46 GMT
ENV PHP_VERSION=7.3.17
# Thu, 23 Apr 2020 13:05:46 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.17.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.17.tar.xz.asc/from/this/mirror
# Thu, 23 Apr 2020 13:05:46 GMT
ENV PHP_SHA256=6a30304c27f7e7a94538f5ffec599f600ee93aedbbecad8aa4f8bec539b10ad8 PHP_MD5=
# Thu, 23 Apr 2020 13:05:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Apr 2020 13:05:57 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Apr 2020 13:09:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	sed -e 's/stretch/buster/g' /etc/apt/sources.list > /etc/apt/sources.list.d/buster.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: -10'; 		echo; 		echo 'Package: libargon2*'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: 990'; 	} > /etc/apt/preferences.d/argon2-buster; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Apr 2020 13:09:58 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Thu, 23 Apr 2020 13:09:59 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Apr 2020 13:09:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Apr 2020 13:10:00 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Apr 2020 13:10:00 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 23 Apr 2020 13:10:00 GMT
WORKDIR /var/www/html
# Thu, 23 Apr 2020 13:10:00 GMT
EXPOSE 80
# Thu, 23 Apr 2020 13:10:00 GMT
CMD ["apache2-foreground"]
# Thu, 23 Apr 2020 19:33:50 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         ssmtp         gnupg dirmngr     ;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Apr 2020 19:33:51 GMT
ENV TINI_VERSION=v0.18.0
# Thu, 23 Apr 2020 19:33:55 GMT
RUN export BUILD_ARCH=$(dpkg-architecture --query DEB_BUILD_ARCH)  && curl -L -o /sbin/tini https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}  && curl -L -o /tini.asc https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}.asc  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7  && gpg --batch --verify /tini.asc /sbin/tini  && chmod +x /sbin/tini
# Thu, 23 Apr 2020 19:37:22 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mysql-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         	--with-libdir=lib/$debMultiarch/ 	;     docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.2.1;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so       | awk '/=>/ { print $3 }'       | sort -u       | xargs -r dpkg-query -S       | cut -d: -f1       | sort -u       | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 19:37:24 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Thu, 23 Apr 2020 19:37:24 GMT
VOLUME [/var/www/html]
# Thu, 23 Apr 2020 19:37:26 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Thu, 23 Apr 2020 19:37:26 GMT
ENV FRIENDICA_VERSION=2020.03
# Thu, 23 Apr 2020 19:37:27 GMT
ENV FRIENDICA_ADDONS=2020.03
# Thu, 23 Apr 2020 19:37:55 GMT
RUN set -ex;     curl -fsSL -o friendica.tar.gz         "https://github.com/friendica/friendica/archive/${FRIENDICA_VERSION}.tar.gz";     tar -xzf friendica.tar.gz -C /usr/src/;     rm friendica.tar.gz;     mv -f /usr/src/friendica-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;     curl -fsSL -o friendica_addons.tar.gz         "https://github.com/friendica/friendica-addons/archive/${FRIENDICA_ADDONS}.tar.gz";     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica_addons.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica_addons.tar.gz;     /usr/src/friendica/bin/composer.phar install --no-dev -d /usr/src/friendica;
# Thu, 23 Apr 2020 19:37:56 GMT
COPY multi:4ce6218883572e2819aeaf93851e15069cd19fdc80ac04b89a1c335ca7e4d501 in / 
# Thu, 23 Apr 2020 19:37:57 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Thu, 23 Apr 2020 19:37:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 19:37:58 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6226bb743a1d24a228a01371b3e9ffd4282416a12860a77d4c2680bdc680f7d2`  
		Last Modified: Thu, 23 Apr 2020 14:17:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e1a2cabc8872e06e54d0e4fc0dd7ef6072f5da5cb2522ed01403bc8d12e004`  
		Last Modified: Thu, 23 Apr 2020 14:17:35 GMT  
		Size: 71.5 MB (71524397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9071b9da2c56ba51c1efd169a629c952d939d6cd1ba1f8c9867cd393d3d20eb8`  
		Last Modified: Thu, 23 Apr 2020 14:17:12 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305096ebaf827e59f368fb5bd505afe172c31f39e3d531772b487208c7176f59`  
		Last Modified: Thu, 23 Apr 2020 14:17:51 GMT  
		Size: 17.6 MB (17559812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a90d9b85ef26ee109983cc0a291e64f3739c97dc9ac62c818c5df85f88ef52`  
		Last Modified: Thu, 23 Apr 2020 14:17:45 GMT  
		Size: 431.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20675a592a0c7772547533b10d55c6fda96eed0b60afb7df54e917d8965934b5`  
		Last Modified: Thu, 23 Apr 2020 14:17:44 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1d7621c2a6290f302d50f85f5c071240f71266c54c602e9c2ebe626165d9b2`  
		Last Modified: Thu, 23 Apr 2020 14:17:46 GMT  
		Size: 12.5 MB (12464277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c099a189021e487b4faf036c3c5aaf6b3f631490ea427c72a472cc3c64c4b9c`  
		Last Modified: Thu, 23 Apr 2020 14:17:43 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b9f52a8bdf8f27f9bced08ff03d952164ecbc147622428b7242ac988a5b907`  
		Last Modified: Thu, 23 Apr 2020 14:17:49 GMT  
		Size: 14.1 MB (14119934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f50102ae07f1e2385a7f0b20bbbae8a7c55a4da9d1b889bd881b5b665a31ca4`  
		Last Modified: Thu, 23 Apr 2020 14:17:43 GMT  
		Size: 2.2 KB (2240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d73ae4fecbfc4d7fc9a5f1dcac7a8828921640fdeada301410cf7c7f44fb44e`  
		Last Modified: Thu, 23 Apr 2020 14:17:44 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234418ccdedcfea4966c510e064121416d01e187437a8e7fdc12148870651f20`  
		Last Modified: Thu, 23 Apr 2020 14:17:43 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e83000a036a56088edb97f88363b76f999392900b75bf0da7e67dbbbafa1aaa`  
		Last Modified: Thu, 23 Apr 2020 19:43:16 GMT  
		Size: 16.8 MB (16799513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44543f41f4edaa10c945757ede66932b236755db35d47ebcc1d1729f58339fc`  
		Last Modified: Thu, 23 Apr 2020 19:43:10 GMT  
		Size: 16.3 KB (16315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffba43a5e3a7d1fe6c9d8fe0207f3b20303e85fb399d1f876ba603e3dfb8d94c`  
		Last Modified: Thu, 23 Apr 2020 19:43:15 GMT  
		Size: 11.8 MB (11765456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095a6ee05a8c58dba41f878ef207dbcfd13031ea0f28d3f4ef9954012698cacd`  
		Last Modified: Thu, 23 Apr 2020 19:43:09 GMT  
		Size: 564.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2784dbf2f9bd0f31789c01f29a2bd57077e9ea3344134c91544ea6781874a381`  
		Last Modified: Thu, 23 Apr 2020 19:43:09 GMT  
		Size: 540.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1436d35ad6f8c2b9655e291326545cb4f8f52127c545b016d5dc4b3208c7dbe9`  
		Last Modified: Thu, 23 Apr 2020 19:43:26 GMT  
		Size: 57.8 MB (57783002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d063647a06a963d963c1ea5089428b0de3058502a0e30e73078f7a79d55e11`  
		Last Modified: Thu, 23 Apr 2020 19:43:09 GMT  
		Size: 2.2 KB (2193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c95081db5c428958543a61196c2747561cf29ee5b70c630c2c016a7aa03a46c`  
		Last Modified: Thu, 23 Apr 2020 19:43:09 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:latest` - linux; ppc64le

```console
$ docker pull friendica@sha256:748c2bbd14f07ac23f170a3e8ff87507564714f0cebe3029c48f8e65f0d47fef
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212196631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8725c5352da35cc4d07cfacd07b4a51ecc108befa864a254f3783c7bfc32f28f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:37 GMT
ADD file:a18cd8947224196f50b4845289d03b1f4deafb438223194400da0ed4dae92656 in / 
# Thu, 23 Apr 2020 00:42:40 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 15:53:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Apr 2020 15:53:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Apr 2020 15:55:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 15:55:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Apr 2020 15:55:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 23 Apr 2020 16:01:45 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 23 Apr 2020 16:01:49 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 23 Apr 2020 16:02:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 23 Apr 2020 16:03:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 23 Apr 2020 16:03:11 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 23 Apr 2020 16:03:15 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Thu, 23 Apr 2020 16:03:17 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Thu, 23 Apr 2020 16:03:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 16:03:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 16:03:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Apr 2020 16:03:31 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 23 Apr 2020 16:03:32 GMT
ENV PHP_VERSION=7.3.17
# Thu, 23 Apr 2020 16:03:35 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.17.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.17.tar.xz.asc/from/this/mirror
# Thu, 23 Apr 2020 16:03:38 GMT
ENV PHP_SHA256=6a30304c27f7e7a94538f5ffec599f600ee93aedbbecad8aa4f8bec539b10ad8 PHP_MD5=
# Thu, 23 Apr 2020 16:04:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Apr 2020 16:04:39 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Apr 2020 16:09:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	sed -e 's/stretch/buster/g' /etc/apt/sources.list > /etc/apt/sources.list.d/buster.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: -10'; 		echo; 		echo 'Package: libargon2*'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: 990'; 	} > /etc/apt/preferences.d/argon2-buster; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Apr 2020 16:09:51 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Thu, 23 Apr 2020 16:09:56 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Apr 2020 16:10:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Apr 2020 16:10:04 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Apr 2020 16:10:07 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 23 Apr 2020 16:10:13 GMT
WORKDIR /var/www/html
# Thu, 23 Apr 2020 16:10:15 GMT
EXPOSE 80
# Thu, 23 Apr 2020 16:10:17 GMT
CMD ["apache2-foreground"]
# Thu, 23 Apr 2020 23:40:14 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         ssmtp         gnupg dirmngr     ;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Apr 2020 23:40:16 GMT
ENV TINI_VERSION=v0.18.0
# Thu, 23 Apr 2020 23:40:29 GMT
RUN export BUILD_ARCH=$(dpkg-architecture --query DEB_BUILD_ARCH)  && curl -L -o /sbin/tini https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}  && curl -L -o /tini.asc https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}.asc  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7  && gpg --batch --verify /tini.asc /sbin/tini  && chmod +x /sbin/tini
# Thu, 23 Apr 2020 23:51:31 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mysql-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         	--with-libdir=lib/$debMultiarch/ 	;     docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.2.1;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so       | awk '/=>/ { print $3 }'       | sort -u       | xargs -r dpkg-query -S       | cut -d: -f1       | sort -u       | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 23:51:42 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Thu, 23 Apr 2020 23:51:47 GMT
VOLUME [/var/www/html]
# Thu, 23 Apr 2020 23:51:54 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Thu, 23 Apr 2020 23:51:58 GMT
ENV FRIENDICA_VERSION=2020.03
# Thu, 23 Apr 2020 23:52:01 GMT
ENV FRIENDICA_ADDONS=2020.03
# Thu, 23 Apr 2020 23:52:40 GMT
RUN set -ex;     curl -fsSL -o friendica.tar.gz         "https://github.com/friendica/friendica/archive/${FRIENDICA_VERSION}.tar.gz";     tar -xzf friendica.tar.gz -C /usr/src/;     rm friendica.tar.gz;     mv -f /usr/src/friendica-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;     curl -fsSL -o friendica_addons.tar.gz         "https://github.com/friendica/friendica-addons/archive/${FRIENDICA_ADDONS}.tar.gz";     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica_addons.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica_addons.tar.gz;     /usr/src/friendica/bin/composer.phar install --no-dev -d /usr/src/friendica;
# Thu, 23 Apr 2020 23:52:45 GMT
COPY multi:4ce6218883572e2819aeaf93851e15069cd19fdc80ac04b89a1c335ca7e4d501 in / 
# Thu, 23 Apr 2020 23:52:46 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Thu, 23 Apr 2020 23:52:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 23:52:51 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4efde6fe2246d87988ee174dc3ed2e4c3158360e5c80fcb0433bc70a732bd77e`  
		Last Modified: Thu, 23 Apr 2020 00:55:34 GMT  
		Size: 22.8 MB (22785405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf022eef780e41e09d76e40c19f34d9a75157359d20c2cf3d74b48a62c1b6b7c`  
		Last Modified: Thu, 23 Apr 2020 17:22:39 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8569b1b571c58f3fbb618060123b941e122e5b9a0cb0b1f5a9eec79341cb90af`  
		Last Modified: Thu, 23 Apr 2020 17:23:22 GMT  
		Size: 61.8 MB (61836836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453bc9fb1161dec68c598632b4877e4075a30b451efa3de6b52654e22da1d34f`  
		Last Modified: Thu, 23 Apr 2020 17:22:38 GMT  
		Size: 288.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6d6d2633513f3c59d412ebe17f5e27787ffe1fd7c66d33ecd2fcbc252262d0`  
		Last Modified: Thu, 23 Apr 2020 17:23:58 GMT  
		Size: 17.3 MB (17341142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980fd2b668f5a2d9b78bed342f50f8c973609452b4127db70136eaae495d3bfb`  
		Last Modified: Thu, 23 Apr 2020 17:23:42 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2425a7bbde79b291597db64a2ed6a38b1733b2872505b190519efc39794e39c`  
		Last Modified: Thu, 23 Apr 2020 17:23:43 GMT  
		Size: 517.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852ffd0b3d63db584a1a67310513c7a5f6a260f0c1088cd42f367ff8b9e050ba`  
		Last Modified: Thu, 23 Apr 2020 17:23:47 GMT  
		Size: 12.5 MB (12463600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2403a3fe9bd93254610c37f29e422e1b3d738dce186941a228dcdc51114f1c45`  
		Last Modified: Thu, 23 Apr 2020 17:23:39 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01f8ffeb2146489d34237557a556d9a949c8732b0a4d89af87ca64ae29e10cb`  
		Last Modified: Thu, 23 Apr 2020 17:24:02 GMT  
		Size: 13.6 MB (13585094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee76654e3453341d631de3e5cce1f31c7e21354d9a68850f6e14a0882f6fd268`  
		Last Modified: Thu, 23 Apr 2020 17:23:39 GMT  
		Size: 2.2 KB (2242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b832b2350ba3310a1d45b88e9af56faab51b288c93d7b7fee6e932aa1c91dab2`  
		Last Modified: Thu, 23 Apr 2020 17:23:39 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ad4ec39e3fa4233b3d2a5dd99513fe0d75d41b58f4b906c6743dd4c0468f66`  
		Last Modified: Thu, 23 Apr 2020 17:23:39 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a847a35b09186e8c4e9b453307c8cd06635bc7d2488e5433a1269051ade9c957`  
		Last Modified: Fri, 24 Apr 2020 00:04:42 GMT  
		Size: 14.9 MB (14944797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6534c8824291fde3ceb7543b5c6508efe266f22cf72f505c97e83dd478bb5e15`  
		Last Modified: Fri, 24 Apr 2020 00:04:34 GMT  
		Size: 16.5 KB (16520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719e5cab9540e04880d61fd52367905e3d339a5e0539218179b71d4a94579442`  
		Last Modified: Fri, 24 Apr 2020 00:04:43 GMT  
		Size: 11.4 MB (11429854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070dd9d56557ba4aa889f8eed7bd88112505a086401894a12de062024fc9f3ec`  
		Last Modified: Fri, 24 Apr 2020 00:04:31 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad4f74a18f450b6c8ce9618c38daaeabf3a8ff3eb025a84b3150a0cedd82575`  
		Last Modified: Fri, 24 Apr 2020 00:04:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e74fe67f9ad81101d4517914adf132a0d042202b2da9b765e16e69005a60d0c4`  
		Last Modified: Fri, 24 Apr 2020 00:04:46 GMT  
		Size: 57.8 MB (57783559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca1fb8e45edbff29afdea2baff4ab0da3e60e35bf3387ff516ce7baab412fce`  
		Last Modified: Fri, 24 Apr 2020 00:04:31 GMT  
		Size: 2.2 KB (2193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c505818ac01dac24795d0600d08ad477336718641acd8cdb7bdce9e70503412d`  
		Last Modified: Fri, 24 Apr 2020 00:04:31 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
