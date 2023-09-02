## `phpmyadmin:fpm`

```console
$ docker pull phpmyadmin@sha256:619f5c653b8383e403a6c83c93c6a17bb4921d3b9fb664d8af7ce108d795222e
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

### `phpmyadmin:fpm` - linux; amd64

```console
$ docker pull phpmyadmin@sha256:9503a098039d2e71c5153bac6f20d4b2c047e60992ac141173d5c567f1ef0b4e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.8 MB (189817002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b4f631a2406a32d26f94db1c2905f5fdc276d391a804deac9132606926719e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 16 Aug 2023 00:59:46 GMT
ADD file:997f5a9b32407d96efac41a1cfafb318f77de077c8b5cd7065b6ec9796b4bf5e in / 
# Wed, 16 Aug 2023 00:59:47 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 02:12:09 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 16 Aug 2023 02:12:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 16 Aug 2023 02:12:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 02:12:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 16 Aug 2023 02:12:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 16 Aug 2023 02:12:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Aug 2023 02:12:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Aug 2023 02:12:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 16 Aug 2023 02:41:04 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 02 Sep 2023 06:35:31 GMT
ENV PHP_VERSION=8.2.10
# Sat, 02 Sep 2023 06:35:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.10.tar.xz.asc
# Sat, 02 Sep 2023 06:35:31 GMT
ENV PHP_SHA256=561dc4acd5386e47f25be76f2c8df6ae854756469159248313bcf276e282fbb3
# Sat, 02 Sep 2023 06:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 02 Sep 2023 06:35:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 02 Sep 2023 06:46:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 02 Sep 2023 06:46:43 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 02 Sep 2023 06:46:44 GMT
RUN docker-php-ext-enable sodium
# Sat, 02 Sep 2023 06:46:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 02 Sep 2023 06:46:44 GMT
WORKDIR /var/www/html
# Sat, 02 Sep 2023 06:46:44 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 02 Sep 2023 06:46:44 GMT
STOPSIGNAL SIGQUIT
# Sat, 02 Sep 2023 06:46:44 GMT
EXPOSE 9000
# Sat, 02 Sep 2023 06:46:44 GMT
CMD ["php-fpm"]
# Sat, 02 Sep 2023 10:37:32 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libbz2-dev         libfreetype6-dev         libjpeg-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     extdir="$(php -r 'echo ini_get("extension_dir");')";     ldd "$extdir"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     ldd "$extdir"/*.so | grep -qzv "=> not found" || (echo "Sanity check failed: missing libraries:"; ldd "$extdir"/*.so | grep " => not found"; exit 1);     ldd "$extdir"/*.so | grep -q "libzip.so.* => .*/libzip.so.*" || (echo "Sanity check failed: libzip.so is not referenced"; ldd "$extdir"/*.so; exit 1);     err="$(php --version 3>&1 1>&2 2>&3)";     [ -z "$err" ] || (echo "Sanity check failed: php returned errors; $err"; exit 1;);
# Sat, 02 Sep 2023 10:37:32 GMT
ENV MAX_EXECUTION_TIME=600
# Sat, 02 Sep 2023 10:37:32 GMT
ENV MEMORY_LIMIT=512M
# Sat, 02 Sep 2023 10:37:32 GMT
ENV UPLOAD_LIMIT=2048K
# Sat, 02 Sep 2023 10:37:32 GMT
ENV TZ=UTC
# Sat, 02 Sep 2023 10:37:32 GMT
ENV SESSION_SAVE_PATH=/sessions
# Sat, 02 Sep 2023 10:37:33 GMT
RUN set -ex;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini
# Sat, 02 Sep 2023 10:37:33 GMT
ENV VERSION=5.2.1
# Sat, 02 Sep 2023 10:37:33 GMT
ENV SHA256=373f9599dfbd96d6fe75316d5dad189e68c305f297edf42377db9dd6b41b2557
# Sat, 02 Sep 2023 10:37:33 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.1/phpMyAdmin-5.2.1-all-languages.tar.xz
# Sat, 02 Sep 2023 10:37:33 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.1 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Sat, 02 Sep 2023 10:37:44 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         gnupg         dirmngr     ;     mkdir $SESSION_SAVE_PATH;     chmod 1777 $SESSION_SAVE_PATH;     chown www-data:www-data $SESSION_SAVE_PATH;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     chown www-data:www-data /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 10:37:44 GMT
COPY file:f697d9b67ffcb023f485f153138036d27b209f81ffe35ce3b93a825c617138cd in /etc/phpmyadmin/config.inc.php 
# Sat, 02 Sep 2023 10:37:44 GMT
COPY file:d8c9f50886f5865fe589f64cb31544582913bb98f2cfa51a8828d71871363ce9 in /docker-entrypoint.sh 
# Sat, 02 Sep 2023 10:37:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 02 Sep 2023 10:37:44 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:52d2b7f179e32b4cbd579ee3c4958027988f9a8274850ab0c7c24661e3adaac5`  
		Last Modified: Wed, 16 Aug 2023 01:04:30 GMT  
		Size: 29.1 MB (29124563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635676b59bff48bb8bf1480dd07a2ec477ac43d5d8f589b04a4b49600280dbf0`  
		Last Modified: Wed, 16 Aug 2023 04:30:36 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08dbc2d7054ba7a357e67b9a5bbeb76074fa786bbeb65777f71fbbc4106e616d`  
		Last Modified: Wed, 16 Aug 2023 04:30:51 GMT  
		Size: 104.3 MB (104340610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8748b1b28b494d0c88f7ff96b5b0e31ae6f2db72cafa2a6f4e6f50f9359c2c26`  
		Last Modified: Wed, 16 Aug 2023 04:30:36 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cccfd282f9b3b171618286c3a0df70baae4787b972bcf4d202f7bae035638e8f`  
		Last Modified: Sat, 02 Sep 2023 08:35:00 GMT  
		Size: 12.4 MB (12354634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b6f2bb26004a477bd8728dbd6b281dd28fd001d0f87e64ce7ec81bcf14582d`  
		Last Modified: Sat, 02 Sep 2023 08:34:59 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2fc59ad47bc49f429f9e1b76a7b70d0ed89e78bcc0e32b7111af789281e61d`  
		Last Modified: Sat, 02 Sep 2023 08:36:10 GMT  
		Size: 27.8 MB (27793186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf13dac9526759df137a36cd01fd924919485135661c73419a362757fd331cdc`  
		Last Modified: Sat, 02 Sep 2023 08:36:06 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e89b7036b992924d12cf334061a96df757da1b88098e75738c938853d9c6153`  
		Last Modified: Sat, 02 Sep 2023 08:36:06 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9add0967676b70701b3b17ba3de8b5c51c582d636e6f19ebb0c35b966f936db8`  
		Last Modified: Sat, 02 Sep 2023 08:36:06 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005c8478dea8d9dabd0e97c9b12922e823bf2bec01cfc38c3f78899d8d81a11c`  
		Last Modified: Sat, 02 Sep 2023 10:39:42 GMT  
		Size: 3.2 MB (3184123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14da55a0551c726e89ab1cb5732820242068f427736095171b7329da0679785a`  
		Last Modified: Sat, 02 Sep 2023 10:39:42 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd17ea0e1c53dd6a3a86c218692e22a2297d42f378990eff35346e5af86d9488`  
		Last Modified: Sat, 02 Sep 2023 10:39:44 GMT  
		Size: 13.0 MB (13004037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f8945e71c3c8ab90474856b8519fc654f487b6e33c5e4aaf2265030a7bd02e`  
		Last Modified: Sat, 02 Sep 2023 10:39:42 GMT  
		Size: 1.6 KB (1614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acbaf985924e79289856c1d342f487b49de9ad098b89c84a85200ce0abab7042`  
		Last Modified: Sat, 02 Sep 2023 10:39:42 GMT  
		Size: 782.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `phpmyadmin:fpm` - linux; arm variant v5

```console
$ docker pull phpmyadmin@sha256:3fed8ef4a0203ed809036c565b3ff06e766e6b8e5aaa6b88856f77eed967dbbc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163273422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284e876d36c10b34c37301b4601451ac414d83e15518503d5e5423e06e32fd5b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 15 Aug 2023 23:48:32 GMT
ADD file:661e14e9730f2608fba590f84fbb357838a3068db018f1e0569c79035783c86d in / 
# Tue, 15 Aug 2023 23:48:33 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 05:27:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 16 Aug 2023 05:27:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 16 Aug 2023 05:27:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 05:27:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 16 Aug 2023 05:27:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 16 Aug 2023 05:27:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Aug 2023 05:27:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Aug 2023 05:27:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 16 Aug 2023 05:50:21 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 02 Sep 2023 02:49:54 GMT
ENV PHP_VERSION=8.2.10
# Sat, 02 Sep 2023 02:49:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.10.tar.xz.asc
# Sat, 02 Sep 2023 02:49:55 GMT
ENV PHP_SHA256=561dc4acd5386e47f25be76f2c8df6ae854756469159248313bcf276e282fbb3
# Sat, 02 Sep 2023 02:50:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 02 Sep 2023 02:50:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 02 Sep 2023 03:04:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 02 Sep 2023 03:04:41 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 02 Sep 2023 03:04:42 GMT
RUN docker-php-ext-enable sodium
# Sat, 02 Sep 2023 03:04:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 02 Sep 2023 03:04:42 GMT
WORKDIR /var/www/html
# Sat, 02 Sep 2023 03:04:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 02 Sep 2023 03:04:43 GMT
STOPSIGNAL SIGQUIT
# Sat, 02 Sep 2023 03:04:43 GMT
EXPOSE 9000
# Sat, 02 Sep 2023 03:04:43 GMT
CMD ["php-fpm"]
# Sat, 02 Sep 2023 05:58:41 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libbz2-dev         libfreetype6-dev         libjpeg-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     extdir="$(php -r 'echo ini_get("extension_dir");')";     ldd "$extdir"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     ldd "$extdir"/*.so | grep -qzv "=> not found" || (echo "Sanity check failed: missing libraries:"; ldd "$extdir"/*.so | grep " => not found"; exit 1);     ldd "$extdir"/*.so | grep -q "libzip.so.* => .*/libzip.so.*" || (echo "Sanity check failed: libzip.so is not referenced"; ldd "$extdir"/*.so; exit 1);     err="$(php --version 3>&1 1>&2 2>&3)";     [ -z "$err" ] || (echo "Sanity check failed: php returned errors; $err"; exit 1;);
# Sat, 02 Sep 2023 05:58:42 GMT
ENV MAX_EXECUTION_TIME=600
# Sat, 02 Sep 2023 05:58:42 GMT
ENV MEMORY_LIMIT=512M
# Sat, 02 Sep 2023 05:58:42 GMT
ENV UPLOAD_LIMIT=2048K
# Sat, 02 Sep 2023 05:58:42 GMT
ENV TZ=UTC
# Sat, 02 Sep 2023 05:58:42 GMT
ENV SESSION_SAVE_PATH=/sessions
# Sat, 02 Sep 2023 05:58:42 GMT
RUN set -ex;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini
# Sat, 02 Sep 2023 05:58:43 GMT
ENV VERSION=5.2.1
# Sat, 02 Sep 2023 05:58:43 GMT
ENV SHA256=373f9599dfbd96d6fe75316d5dad189e68c305f297edf42377db9dd6b41b2557
# Sat, 02 Sep 2023 05:58:43 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.1/phpMyAdmin-5.2.1-all-languages.tar.xz
# Sat, 02 Sep 2023 05:58:43 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.1 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Sat, 02 Sep 2023 05:58:58 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         gnupg         dirmngr     ;     mkdir $SESSION_SAVE_PATH;     chmod 1777 $SESSION_SAVE_PATH;     chown www-data:www-data $SESSION_SAVE_PATH;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     chown www-data:www-data /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 05:58:58 GMT
COPY file:f697d9b67ffcb023f485f153138036d27b209f81ffe35ce3b93a825c617138cd in /etc/phpmyadmin/config.inc.php 
# Sat, 02 Sep 2023 05:58:58 GMT
COPY file:d8c9f50886f5865fe589f64cb31544582913bb98f2cfa51a8828d71871363ce9 in /docker-entrypoint.sh 
# Sat, 02 Sep 2023 05:58:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 02 Sep 2023 05:58:58 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:46d4cdda07fa660f92a3251737b0b22ad71ebafb783af374930d636935a2d8eb`  
		Last Modified: Tue, 15 Aug 2023 23:51:34 GMT  
		Size: 27.0 MB (26983543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8889e6e8f72bab0c23f476e5a62ce6013d6ac07d266d1ddbf6e526dc901ff35`  
		Last Modified: Wed, 16 Aug 2023 07:20:10 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b0d3f2f7bdddaf01b13e6c2abb7032ba6553bc28113022f2dacf06fc6fb32a`  
		Last Modified: Wed, 16 Aug 2023 07:20:27 GMT  
		Size: 82.0 MB (82026853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b12aa4778eae7d15f7aa828db4d967dd9e67946171ccdd523b398747e076b08`  
		Last Modified: Wed, 16 Aug 2023 07:20:10 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bd62184609d896d5f63e42f057768f454815f7cd475611304309fbcde0aff3`  
		Last Modified: Sat, 02 Sep 2023 04:02:26 GMT  
		Size: 12.4 MB (12352874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9350ebe5ae43ec3d588539de91aae83f10eb889b9308f800bf6ae38634c62e91`  
		Last Modified: Sat, 02 Sep 2023 04:02:26 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5783ebad3d636296b8927ebdb77871dff7ba269a3f58f1d19e8a26d82e347a75`  
		Last Modified: Sat, 02 Sep 2023 04:03:42 GMT  
		Size: 26.3 MB (26292015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a019193d9ac53966eb6c2b38ed654b124f6db6ef690d9d945be7aebbcbc8d0ef`  
		Last Modified: Sat, 02 Sep 2023 04:03:36 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d471ac6835560ce42ea61f47f4ea5f852b4aa8e2f0594f3326148f303b3013b`  
		Last Modified: Sat, 02 Sep 2023 04:03:36 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e27e9518691cd5be2bc17682a7fc54857d958986b27dda32c6920141856dd73`  
		Last Modified: Sat, 02 Sep 2023 04:03:36 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983660ab90f314e92d0491ddf9b9404e1eded06d06b5e0631e026245949305e9`  
		Last Modified: Sat, 02 Sep 2023 05:59:36 GMT  
		Size: 2.6 MB (2598110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5350d3a2ade307165e7b171b215b168930bd01f6133c07985be1018c6ec215`  
		Last Modified: Sat, 02 Sep 2023 05:59:35 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695c9b53d648f1b2a3cc8c4e1a8043b10f8dfa720e556a228da8003b502bdcd2`  
		Last Modified: Sat, 02 Sep 2023 05:59:38 GMT  
		Size: 13.0 MB (13004175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04f0f6d9a40815a08c41c83df4f51f075c85bb4aa336c2973adba0ff084a624`  
		Last Modified: Sat, 02 Sep 2023 05:59:35 GMT  
		Size: 1.6 KB (1615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ae0ac392792697fc72a3953bc81a3e7faae5aead93f465b5430dd569a83e65`  
		Last Modified: Sat, 02 Sep 2023 05:59:35 GMT  
		Size: 783.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `phpmyadmin:fpm` - linux; arm variant v7

```console
$ docker pull phpmyadmin@sha256:051e2caa23f4f7cd57d8d4c476b046930863f8fbc4c49e367057a8b29602361b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154234774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f50384e0681c9a48987c7f09831480177a7883898b781656e81fadbf6bd1dfea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 16 Aug 2023 00:17:12 GMT
ADD file:45cc27bd11f601d2fef5d7494a1a6253287e6d22e108e39c0884761c7533cd9c in / 
# Wed, 16 Aug 2023 00:17:12 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:09:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 16 Aug 2023 01:09:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 16 Aug 2023 01:09:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 01:09:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 16 Aug 2023 01:09:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 16 Aug 2023 01:09:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Aug 2023 01:09:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Aug 2023 01:09:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 16 Aug 2023 01:34:00 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 02 Sep 2023 02:44:31 GMT
ENV PHP_VERSION=8.2.10
# Sat, 02 Sep 2023 02:44:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.10.tar.xz.asc
# Sat, 02 Sep 2023 02:44:32 GMT
ENV PHP_SHA256=561dc4acd5386e47f25be76f2c8df6ae854756469159248313bcf276e282fbb3
# Sat, 02 Sep 2023 02:44:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 02 Sep 2023 02:44:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 02 Sep 2023 02:58:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 02 Sep 2023 02:58:50 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 02 Sep 2023 02:58:51 GMT
RUN docker-php-ext-enable sodium
# Sat, 02 Sep 2023 02:58:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 02 Sep 2023 02:58:51 GMT
WORKDIR /var/www/html
# Sat, 02 Sep 2023 02:58:52 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 02 Sep 2023 02:58:52 GMT
STOPSIGNAL SIGQUIT
# Sat, 02 Sep 2023 02:58:53 GMT
EXPOSE 9000
# Sat, 02 Sep 2023 02:58:53 GMT
CMD ["php-fpm"]
# Sat, 02 Sep 2023 07:49:32 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libbz2-dev         libfreetype6-dev         libjpeg-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     extdir="$(php -r 'echo ini_get("extension_dir");')";     ldd "$extdir"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     ldd "$extdir"/*.so | grep -qzv "=> not found" || (echo "Sanity check failed: missing libraries:"; ldd "$extdir"/*.so | grep " => not found"; exit 1);     ldd "$extdir"/*.so | grep -q "libzip.so.* => .*/libzip.so.*" || (echo "Sanity check failed: libzip.so is not referenced"; ldd "$extdir"/*.so; exit 1);     err="$(php --version 3>&1 1>&2 2>&3)";     [ -z "$err" ] || (echo "Sanity check failed: php returned errors; $err"; exit 1;);
# Sat, 02 Sep 2023 07:49:32 GMT
ENV MAX_EXECUTION_TIME=600
# Sat, 02 Sep 2023 07:49:32 GMT
ENV MEMORY_LIMIT=512M
# Sat, 02 Sep 2023 07:49:32 GMT
ENV UPLOAD_LIMIT=2048K
# Sat, 02 Sep 2023 07:49:32 GMT
ENV TZ=UTC
# Sat, 02 Sep 2023 07:49:32 GMT
ENV SESSION_SAVE_PATH=/sessions
# Sat, 02 Sep 2023 07:49:33 GMT
RUN set -ex;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini
# Sat, 02 Sep 2023 07:49:33 GMT
ENV VERSION=5.2.1
# Sat, 02 Sep 2023 07:49:33 GMT
ENV SHA256=373f9599dfbd96d6fe75316d5dad189e68c305f297edf42377db9dd6b41b2557
# Sat, 02 Sep 2023 07:49:33 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.1/phpMyAdmin-5.2.1-all-languages.tar.xz
# Sat, 02 Sep 2023 07:49:33 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.1 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Sat, 02 Sep 2023 07:49:45 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         gnupg         dirmngr     ;     mkdir $SESSION_SAVE_PATH;     chmod 1777 $SESSION_SAVE_PATH;     chown www-data:www-data $SESSION_SAVE_PATH;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     chown www-data:www-data /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 07:49:45 GMT
COPY file:f697d9b67ffcb023f485f153138036d27b209f81ffe35ce3b93a825c617138cd in /etc/phpmyadmin/config.inc.php 
# Sat, 02 Sep 2023 07:49:45 GMT
COPY file:d8c9f50886f5865fe589f64cb31544582913bb98f2cfa51a8828d71871363ce9 in /docker-entrypoint.sh 
# Sat, 02 Sep 2023 07:49:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 02 Sep 2023 07:49:45 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a44aa9565b062e4216f7b39ce6c67dcc5376e10f76caec55bd3acd1cc8b76b75`  
		Last Modified: Wed, 16 Aug 2023 00:21:27 GMT  
		Size: 24.8 MB (24805419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08b4dde5a9219b85577e6b27a7ad67564abbd05e87b21ddbba71ef5765ef432`  
		Last Modified: Wed, 16 Aug 2023 03:05:55 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9a339e07912a00b79ade0609518d0b6c9a890ef8ed5b1aaf6f123b28fa2dc`  
		Last Modified: Wed, 16 Aug 2023 03:06:07 GMT  
		Size: 76.2 MB (76217037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7b4363d3fbe8892ffc33a00cc8899d85c243b0f9d757d4824e7725a6d0b1d7`  
		Last Modified: Wed, 16 Aug 2023 03:05:54 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6b9ea9a9103e929aafb0f8b7dd6510bd639f1dc591b85c4a8bad655d3f4bc5`  
		Last Modified: Sat, 02 Sep 2023 04:38:40 GMT  
		Size: 12.4 MB (12352911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e80c8044e8180f4ce9cecbd0f908e2fecf929169a25d47ac2c114794e2d50e`  
		Last Modified: Sat, 02 Sep 2023 04:38:39 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d1114fccd2aa62362900c36a851e2c46f3632656197c3873bf48ec846ccfd9`  
		Last Modified: Sat, 02 Sep 2023 04:39:53 GMT  
		Size: 25.4 MB (25400486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b16d71ab54925004181bc03e45acb80506572fc9e1af72526801d68e14e5144`  
		Last Modified: Sat, 02 Sep 2023 04:39:49 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23c685db7081673e03e88568dd7f2a41d3befa8f286c6ba7526d461fa44dfd14`  
		Last Modified: Sat, 02 Sep 2023 04:39:49 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef62c80b297d2555ad1564b78a8372011270187473c8942adc6c9850b38e67a`  
		Last Modified: Sat, 02 Sep 2023 04:39:49 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1860acc90519ea8fb649d9ec9a7705008872a58a64b2a3a59bbfd6437f4fdf5d`  
		Last Modified: Sat, 02 Sep 2023 07:51:14 GMT  
		Size: 2.4 MB (2438834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f6f379d969db8976ad1e8a5bfc11d636720958182187618b017e3c88a93156`  
		Last Modified: Sat, 02 Sep 2023 07:51:13 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803168def0106c5cc8ea21b1e2fea8a74fde9505c1da28b1a364065abc7fd618`  
		Last Modified: Sat, 02 Sep 2023 07:51:17 GMT  
		Size: 13.0 MB (13004231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8b90faecddeb06b084d9a380732b6b885bd89090bf8327904e6d2d273f0fef`  
		Last Modified: Sat, 02 Sep 2023 07:51:14 GMT  
		Size: 1.6 KB (1614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5e33467158b9b92166aa8a49072498d721a1742187daa9584ff046cc3b28d2`  
		Last Modified: Sat, 02 Sep 2023 07:51:13 GMT  
		Size: 782.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `phpmyadmin:fpm` - linux; arm64 variant v8

```console
$ docker pull phpmyadmin@sha256:76c79a84f781d55e9838dae4f889a7cb6dc3565061d37b1ce27820cc0d5ed201
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.8 MB (183834913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceeb9350199f62b502108915a321a9b891455c493458aabc34c049a18d3883cb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:57 GMT
ADD file:bc58956fa3d1aff2efb0264655d039fedfff28dc4ff19a65a235e82754ee1cfa in / 
# Tue, 15 Aug 2023 23:39:57 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 04:21:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 16 Aug 2023 04:21:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 16 Aug 2023 04:22:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 04:22:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 16 Aug 2023 04:22:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 16 Aug 2023 04:22:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Aug 2023 04:22:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Aug 2023 04:22:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 16 Aug 2023 04:49:38 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 02 Sep 2023 05:18:58 GMT
ENV PHP_VERSION=8.2.10
# Sat, 02 Sep 2023 05:18:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.10.tar.xz.asc
# Sat, 02 Sep 2023 05:18:58 GMT
ENV PHP_SHA256=561dc4acd5386e47f25be76f2c8df6ae854756469159248313bcf276e282fbb3
# Sat, 02 Sep 2023 05:19:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 02 Sep 2023 05:19:08 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 02 Sep 2023 05:29:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 02 Sep 2023 05:29:23 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 02 Sep 2023 05:29:23 GMT
RUN docker-php-ext-enable sodium
# Sat, 02 Sep 2023 05:29:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 02 Sep 2023 05:29:23 GMT
WORKDIR /var/www/html
# Sat, 02 Sep 2023 05:29:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 02 Sep 2023 05:29:24 GMT
STOPSIGNAL SIGQUIT
# Sat, 02 Sep 2023 05:29:24 GMT
EXPOSE 9000
# Sat, 02 Sep 2023 05:29:24 GMT
CMD ["php-fpm"]
# Sat, 02 Sep 2023 09:46:42 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libbz2-dev         libfreetype6-dev         libjpeg-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     extdir="$(php -r 'echo ini_get("extension_dir");')";     ldd "$extdir"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     ldd "$extdir"/*.so | grep -qzv "=> not found" || (echo "Sanity check failed: missing libraries:"; ldd "$extdir"/*.so | grep " => not found"; exit 1);     ldd "$extdir"/*.so | grep -q "libzip.so.* => .*/libzip.so.*" || (echo "Sanity check failed: libzip.so is not referenced"; ldd "$extdir"/*.so; exit 1);     err="$(php --version 3>&1 1>&2 2>&3)";     [ -z "$err" ] || (echo "Sanity check failed: php returned errors; $err"; exit 1;);
# Sat, 02 Sep 2023 09:46:42 GMT
ENV MAX_EXECUTION_TIME=600
# Sat, 02 Sep 2023 09:46:42 GMT
ENV MEMORY_LIMIT=512M
# Sat, 02 Sep 2023 09:46:42 GMT
ENV UPLOAD_LIMIT=2048K
# Sat, 02 Sep 2023 09:46:42 GMT
ENV TZ=UTC
# Sat, 02 Sep 2023 09:46:42 GMT
ENV SESSION_SAVE_PATH=/sessions
# Sat, 02 Sep 2023 09:46:43 GMT
RUN set -ex;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini
# Sat, 02 Sep 2023 09:46:43 GMT
ENV VERSION=5.2.1
# Sat, 02 Sep 2023 09:46:43 GMT
ENV SHA256=373f9599dfbd96d6fe75316d5dad189e68c305f297edf42377db9dd6b41b2557
# Sat, 02 Sep 2023 09:46:43 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.1/phpMyAdmin-5.2.1-all-languages.tar.xz
# Sat, 02 Sep 2023 09:46:43 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.1 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Sat, 02 Sep 2023 09:46:52 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         gnupg         dirmngr     ;     mkdir $SESSION_SAVE_PATH;     chmod 1777 $SESSION_SAVE_PATH;     chown www-data:www-data $SESSION_SAVE_PATH;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     chown www-data:www-data /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 09:46:52 GMT
COPY file:f697d9b67ffcb023f485f153138036d27b209f81ffe35ce3b93a825c617138cd in /etc/phpmyadmin/config.inc.php 
# Sat, 02 Sep 2023 09:46:52 GMT
COPY file:d8c9f50886f5865fe589f64cb31544582913bb98f2cfa51a8828d71871363ce9 in /docker-entrypoint.sh 
# Sat, 02 Sep 2023 09:46:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 02 Sep 2023 09:46:53 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4ee097f9a36616fddb52e45aba72142c4bc6f2e594f0a746e406acfde4f02f51`  
		Last Modified: Tue, 15 Aug 2023 23:43:21 GMT  
		Size: 29.2 MB (29157256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cbea39f63906a97f303179be046ab209476a01863e9bdec86af8f323302906`  
		Last Modified: Wed, 16 Aug 2023 06:26:06 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e255c1ce22a7316f5c3b6a28b2b1eafc749afbe18efadf8f72a871a2136b5a6f`  
		Last Modified: Wed, 16 Aug 2023 06:26:16 GMT  
		Size: 98.1 MB (98111384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd06eedb7624b234e9cc7f3e03a7b1878d16c13b439a1bf49317c8a4771fa18e`  
		Last Modified: Wed, 16 Aug 2023 06:26:06 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8575105243dd82ca52359a912633d7d2373517d2ab0c699f179887702231bae4`  
		Last Modified: Sat, 02 Sep 2023 07:13:04 GMT  
		Size: 12.4 MB (12354457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc37097238b963a13d2fbdcb266255469ecc27485e456aa3947c7b4904b0de3`  
		Last Modified: Sat, 02 Sep 2023 07:12:59 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db486b1efd2e8c9fa5933d536a0fddfe52dab524c582d1ab0035579a2118fe2`  
		Last Modified: Sat, 02 Sep 2023 07:14:09 GMT  
		Size: 27.8 MB (27757795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a773e4b92be855036e7c83e835dd2e242726fd406cee9d8d9f369810d0ab2914`  
		Last Modified: Sat, 02 Sep 2023 07:14:06 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946ef57bdcbc49305937cad73633a66ce5bad9b1a6fe7170612a546ab9d8382d`  
		Last Modified: Sat, 02 Sep 2023 07:14:06 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63a2b717fd62fc2b670c507babf50897b17b979e74b77178c4e7bbbb54fa02a`  
		Last Modified: Sat, 02 Sep 2023 07:14:06 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5dcb3dae041383beb6ab594219241970daf719aff5ac41918bf6b6a976cc23`  
		Last Modified: Sat, 02 Sep 2023 09:49:21 GMT  
		Size: 3.4 MB (3434152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde0642bee447d27b2060861ccdff4fa892cd246e52bf0608f2810ee784ec4df`  
		Last Modified: Sat, 02 Sep 2023 09:49:20 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a25d58bb7dc195e173f43066d30950434069bf106ecbe8249ac066ec6603a3b`  
		Last Modified: Sat, 02 Sep 2023 09:49:22 GMT  
		Size: 13.0 MB (13004012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c3ab29d29015b1d7e60a3901cf94333413856e15d628464ef6fd5d51ad58dba`  
		Last Modified: Sat, 02 Sep 2023 09:49:20 GMT  
		Size: 1.6 KB (1615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa1b5dd3034acb2c4b585272e2d3ed8bb89f538090dff8f836ff3f45cee5ab4`  
		Last Modified: Sat, 02 Sep 2023 09:49:20 GMT  
		Size: 782.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `phpmyadmin:fpm` - linux; 386

```console
$ docker pull phpmyadmin@sha256:5e592ee714a3a2d1fe27cbb25345e3a0e97798dff01ef462b4acd866cca03cc5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.6 MB (188612225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2167d5b901911041eae9792ffe5e2d55a5dd50d615547f93a53b99cac18833b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:01 GMT
ADD file:ffdb2f26091492ac2e82793b461bb70da9ce1d68d219ec0db182b4510e82586b in / 
# Tue, 15 Aug 2023 23:39:01 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:44:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 16 Aug 2023 03:44:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 16 Aug 2023 03:44:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:44:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 16 Aug 2023 03:44:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 16 Aug 2023 03:44:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Aug 2023 03:44:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Aug 2023 03:44:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 16 Aug 2023 04:32:17 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 02 Sep 2023 03:27:37 GMT
ENV PHP_VERSION=8.2.10
# Sat, 02 Sep 2023 03:27:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.10.tar.xz.asc
# Sat, 02 Sep 2023 03:27:37 GMT
ENV PHP_SHA256=561dc4acd5386e47f25be76f2c8df6ae854756469159248313bcf276e282fbb3
# Sat, 02 Sep 2023 03:27:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 02 Sep 2023 03:27:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 02 Sep 2023 03:48:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 02 Sep 2023 03:48:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 02 Sep 2023 03:48:18 GMT
RUN docker-php-ext-enable sodium
# Sat, 02 Sep 2023 03:48:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 02 Sep 2023 03:48:18 GMT
WORKDIR /var/www/html
# Sat, 02 Sep 2023 03:48:19 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 02 Sep 2023 03:48:19 GMT
STOPSIGNAL SIGQUIT
# Sat, 02 Sep 2023 03:48:19 GMT
EXPOSE 9000
# Sat, 02 Sep 2023 03:48:19 GMT
CMD ["php-fpm"]
# Sat, 02 Sep 2023 10:00:37 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libbz2-dev         libfreetype6-dev         libjpeg-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     extdir="$(php -r 'echo ini_get("extension_dir");')";     ldd "$extdir"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     ldd "$extdir"/*.so | grep -qzv "=> not found" || (echo "Sanity check failed: missing libraries:"; ldd "$extdir"/*.so | grep " => not found"; exit 1);     ldd "$extdir"/*.so | grep -q "libzip.so.* => .*/libzip.so.*" || (echo "Sanity check failed: libzip.so is not referenced"; ldd "$extdir"/*.so; exit 1);     err="$(php --version 3>&1 1>&2 2>&3)";     [ -z "$err" ] || (echo "Sanity check failed: php returned errors; $err"; exit 1;);
# Sat, 02 Sep 2023 10:00:37 GMT
ENV MAX_EXECUTION_TIME=600
# Sat, 02 Sep 2023 10:00:37 GMT
ENV MEMORY_LIMIT=512M
# Sat, 02 Sep 2023 10:00:38 GMT
ENV UPLOAD_LIMIT=2048K
# Sat, 02 Sep 2023 10:00:38 GMT
ENV TZ=UTC
# Sat, 02 Sep 2023 10:00:38 GMT
ENV SESSION_SAVE_PATH=/sessions
# Sat, 02 Sep 2023 10:00:38 GMT
RUN set -ex;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini
# Sat, 02 Sep 2023 10:00:38 GMT
ENV VERSION=5.2.1
# Sat, 02 Sep 2023 10:00:39 GMT
ENV SHA256=373f9599dfbd96d6fe75316d5dad189e68c305f297edf42377db9dd6b41b2557
# Sat, 02 Sep 2023 10:00:39 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.1/phpMyAdmin-5.2.1-all-languages.tar.xz
# Sat, 02 Sep 2023 10:00:39 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.1 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Sat, 02 Sep 2023 10:00:53 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         gnupg         dirmngr     ;     mkdir $SESSION_SAVE_PATH;     chmod 1777 $SESSION_SAVE_PATH;     chown www-data:www-data $SESSION_SAVE_PATH;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     chown www-data:www-data /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 10:00:54 GMT
COPY file:f697d9b67ffcb023f485f153138036d27b209f81ffe35ce3b93a825c617138cd in /etc/phpmyadmin/config.inc.php 
# Sat, 02 Sep 2023 10:00:54 GMT
COPY file:d8c9f50886f5865fe589f64cb31544582913bb98f2cfa51a8828d71871363ce9 in /docker-entrypoint.sh 
# Sat, 02 Sep 2023 10:00:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 02 Sep 2023 10:00:54 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a12cc43de7614ac71c57865601eb4cedd27ce910b66c5091e07781b8547d5b0b`  
		Last Modified: Tue, 15 Aug 2023 23:43:26 GMT  
		Size: 30.1 MB (30141823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb61ec40f5db69c213102749fea3915c3ce93b2064e3bf6a045e986dfe20a7bc`  
		Last Modified: Wed, 16 Aug 2023 07:31:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d167e851ee2ef31308f9f4ecfc454e5bea793866222cc2afc69c7b0bf37809c`  
		Last Modified: Wed, 16 Aug 2023 07:32:03 GMT  
		Size: 101.5 MB (101506138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e90fee09e6b0af369884a2562788ef1f96299e6e1325a3e892f38b5590f398`  
		Last Modified: Wed, 16 Aug 2023 07:31:39 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:355eb07320612cc643ae3f1a0afeeb4822e821ca31c0e99bee85fc172808d44e`  
		Last Modified: Sat, 02 Sep 2023 07:00:35 GMT  
		Size: 12.4 MB (12353891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43f850f2834112335b624c5eedda7ed02691167fae58b72c318853aeac93a75`  
		Last Modified: Sat, 02 Sep 2023 07:00:34 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb819e9e561a1c51a1fb66fae69505a0adbf85512df0651a31c564369ffded46`  
		Last Modified: Sat, 02 Sep 2023 07:01:56 GMT  
		Size: 28.3 MB (28323141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860d66cefe99bf22dc1be903ed383f8515458078906e05ba2b1c3072c8f91dff`  
		Last Modified: Sat, 02 Sep 2023 07:01:50 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a200a61a29016fcf97774dccd2f60c281169cb4903887d3f4a22f644e1fc3bf`  
		Last Modified: Sat, 02 Sep 2023 07:01:50 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3822edde06773f63c1e438bc8f1336881577fa8ec86ee7eae8713f0023abeb80`  
		Last Modified: Sat, 02 Sep 2023 07:01:50 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef220216f22a3164e0541c58802289987247838b0de771b481d60342f6a45452`  
		Last Modified: Sat, 02 Sep 2023 10:03:30 GMT  
		Size: 3.3 MB (3267487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8db5ef95fd1d5d4315cde00465755c7051241141e9224bf47d0eda98e5dc80`  
		Last Modified: Sat, 02 Sep 2023 10:03:28 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3cad35476485691a77b78b4c526a02f6f823a008bc67415ad36d01f6a817f8b`  
		Last Modified: Sat, 02 Sep 2023 10:03:33 GMT  
		Size: 13.0 MB (13003896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72050fcf682675691f40b1ca80140907a07ef8bc7d5097216f9c9ad7bfec2cb`  
		Last Modified: Sat, 02 Sep 2023 10:03:28 GMT  
		Size: 1.6 KB (1613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4251888ffb2eef54292dfd94fca0cacc73ddf60ad4544e728eafab1cd9b8f10d`  
		Last Modified: Sat, 02 Sep 2023 10:03:28 GMT  
		Size: 782.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `phpmyadmin:fpm` - linux; mips64le

```console
$ docker pull phpmyadmin@sha256:fd9c05b79fd1fe7e15282cf1b8edd1cfc79185357f14b60d8cab8472fcf2a849
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.9 MB (163944431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f465d5a2cc49c026e23151878cb03514014a37120954490ea965b58f9a7d4c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 16 Aug 2023 00:08:43 GMT
ADD file:6122efd66f4e010b48e48eeb243d900439ef783f5a10df76043546a288d35d38 in / 
# Wed, 16 Aug 2023 00:08:47 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 00:47:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 16 Aug 2023 00:47:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 16 Aug 2023 00:49:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 00:49:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 16 Aug 2023 00:49:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 16 Aug 2023 00:49:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Aug 2023 00:49:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Aug 2023 00:49:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 16 Aug 2023 02:58:21 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 18 Aug 2023 01:55:46 GMT
ENV PHP_VERSION=8.2.9
# Fri, 18 Aug 2023 01:55:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.9.tar.xz.asc
# Fri, 18 Aug 2023 01:55:53 GMT
ENV PHP_SHA256=1e6cb77f997613864ab3127fbfc6a8c7fdaa89a95e8ed6167617b913b4de4765
# Fri, 18 Aug 2023 01:56:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 18 Aug 2023 01:56:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 18 Aug 2023 02:43:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 18 Aug 2023 02:43:47 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 18 Aug 2023 02:43:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 18 Aug 2023 02:43:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 18 Aug 2023 02:44:01 GMT
WORKDIR /var/www/html
# Fri, 18 Aug 2023 02:44:07 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 18 Aug 2023 02:44:11 GMT
STOPSIGNAL SIGQUIT
# Fri, 18 Aug 2023 02:44:15 GMT
EXPOSE 9000
# Fri, 18 Aug 2023 02:44:19 GMT
CMD ["php-fpm"]
# Fri, 18 Aug 2023 05:09:42 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libbz2-dev         libfreetype6-dev         libjpeg-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     extdir="$(php -r 'echo ini_get("extension_dir");')";     ldd "$extdir"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     ldd "$extdir"/*.so | grep -qzv "=> not found" || (echo "Sanity check failed: missing libraries:"; ldd "$extdir"/*.so | grep " => not found"; exit 1);     ldd "$extdir"/*.so | grep -q "libzip.so.* => .*/libzip.so.*" || (echo "Sanity check failed: libzip.so is not referenced"; ldd "$extdir"/*.so; exit 1);     err="$(php --version 3>&1 1>&2 2>&3)";     [ -z "$err" ] || (echo "Sanity check failed: php returned errors; $err"; exit 1;);
# Fri, 18 Aug 2023 05:09:46 GMT
ENV MAX_EXECUTION_TIME=600
# Fri, 18 Aug 2023 05:09:49 GMT
ENV MEMORY_LIMIT=512M
# Fri, 18 Aug 2023 05:09:53 GMT
ENV UPLOAD_LIMIT=2048K
# Fri, 18 Aug 2023 05:09:56 GMT
ENV TZ=UTC
# Fri, 18 Aug 2023 05:09:59 GMT
ENV SESSION_SAVE_PATH=/sessions
# Fri, 18 Aug 2023 05:10:05 GMT
RUN set -ex;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini
# Fri, 18 Aug 2023 05:10:09 GMT
ENV VERSION=5.2.1
# Fri, 18 Aug 2023 05:10:12 GMT
ENV SHA256=373f9599dfbd96d6fe75316d5dad189e68c305f297edf42377db9dd6b41b2557
# Fri, 18 Aug 2023 05:10:16 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.1/phpMyAdmin-5.2.1-all-languages.tar.xz
# Fri, 18 Aug 2023 05:10:19 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.1 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Fri, 18 Aug 2023 05:11:22 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         gnupg         dirmngr     ;     mkdir $SESSION_SAVE_PATH;     chmod 1777 $SESSION_SAVE_PATH;     chown www-data:www-data $SESSION_SAVE_PATH;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     chown www-data:www-data /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 18 Aug 2023 05:11:26 GMT
COPY file:f697d9b67ffcb023f485f153138036d27b209f81ffe35ce3b93a825c617138cd in /etc/phpmyadmin/config.inc.php 
# Fri, 18 Aug 2023 05:11:30 GMT
COPY file:d8c9f50886f5865fe589f64cb31544582913bb98f2cfa51a8828d71871363ce9 in /docker-entrypoint.sh 
# Fri, 18 Aug 2023 05:11:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 18 Aug 2023 05:11:39 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:52390931db742e6fb36945aff79b92fea76dcfe0964f8a5cf7e5b5faaa40b80f`  
		Last Modified: Wed, 16 Aug 2023 00:19:34 GMT  
		Size: 29.1 MB (29121481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3862b29f341bbf3da16b944e02f2d0961e69940ccb034fb905880cf79c6a11`  
		Last Modified: Wed, 16 Aug 2023 10:01:54 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a7f5b8a93b3d93f636840f197a35dfeac134e5a661b80cd59b7221b3212371`  
		Last Modified: Wed, 16 Aug 2023 10:02:49 GMT  
		Size: 80.7 MB (80670713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8baacd58ebb9b6781c5a69d6fde75aa2193e3ffe207f9e0f9ded1d5f75cfdb9`  
		Last Modified: Wed, 16 Aug 2023 10:01:54 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd8b2bf849878f0d51d94a247a0ca40f3d12fb7e5031df0919c77cce7669e56`  
		Last Modified: Fri, 18 Aug 2023 04:00:17 GMT  
		Size: 12.1 MB (12142408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f31901a4282b1d4d15060777584295b5befa857b9763babbc56603bd8ca7e9`  
		Last Modified: Fri, 18 Aug 2023 04:00:14 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a9047387794dd3d20a8d3788c72cfc5a600cb86a22e982a5dca53a8a0b3c4`  
		Last Modified: Fri, 18 Aug 2023 04:02:43 GMT  
		Size: 26.7 MB (26691691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfbee4d355f53684096d43b40b269de2c9726c386e2e9ca394ecfb17bab30f3`  
		Last Modified: Fri, 18 Aug 2023 04:02:27 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4179830a9a977b1b7f0419ce62fc757517fc425d84dbedc437c419203b4349c`  
		Last Modified: Fri, 18 Aug 2023 04:02:27 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74766ea91ff0ff1ae06afc876df06d127216a453592ec7858dcf9a7c8b4e4590`  
		Last Modified: Fri, 18 Aug 2023 04:02:27 GMT  
		Size: 9.2 KB (9188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432e5b1b007d1b65d12ee5aecac74b69ef74136d0054f0ccad42910bab9d6c42`  
		Last Modified: Fri, 18 Aug 2023 05:12:48 GMT  
		Size: 2.5 MB (2511332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a5059ed63f5326fb5ea7d0b015211a6d8081e3d7d78ef6782dc15bc0817cc2`  
		Last Modified: Fri, 18 Aug 2023 05:12:46 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29afbd13d3d466efc44a97d0660e7a7e4ce9749d9bdb206136fcdff5ecdef659`  
		Last Modified: Fri, 18 Aug 2023 05:12:57 GMT  
		Size: 12.8 MB (12791025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288876b888c7845bad981e4953d967c7874a0bb5e74190309e7bf266e6219e6a`  
		Last Modified: Fri, 18 Aug 2023 05:12:46 GMT  
		Size: 1.6 KB (1587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1dec8e235fadb4c80b40559d2a7474ad1b822e5b35f6a340bf2fa3e5b80af4a`  
		Last Modified: Fri, 18 Aug 2023 05:12:47 GMT  
		Size: 783.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `phpmyadmin:fpm` - linux; ppc64le

```console
$ docker pull phpmyadmin@sha256:9fb1b6cb5338e2af0df7d981b3b0db8dc86330055aecffdb259c01ee38dd9c42
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193786743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df48c5d7b741d0880f0c7ea51549471309d982557a13afa19955259e9f7edda3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 16 Aug 2023 01:09:33 GMT
ADD file:9578bf6d6b33f2ba960ab9309642d1c9dcc131d7b9e6f818b8cc4b843fe3aec8 in / 
# Wed, 16 Aug 2023 01:09:35 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 05:28:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 16 Aug 2023 05:28:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 16 Aug 2023 05:29:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 05:29:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 16 Aug 2023 05:29:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 16 Aug 2023 05:29:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Aug 2023 05:29:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Aug 2023 05:29:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 16 Aug 2023 06:12:01 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 17 Aug 2023 22:19:05 GMT
ENV PHP_VERSION=8.2.9
# Thu, 17 Aug 2023 22:19:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.9.tar.xz.asc
# Thu, 17 Aug 2023 22:19:06 GMT
ENV PHP_SHA256=1e6cb77f997613864ab3127fbfc6a8c7fdaa89a95e8ed6167617b913b4de4765
# Thu, 17 Aug 2023 22:19:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 17 Aug 2023 22:19:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 17 Aug 2023 22:34:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 17 Aug 2023 22:34:24 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 17 Aug 2023 22:34:25 GMT
RUN docker-php-ext-enable sodium
# Thu, 17 Aug 2023 22:34:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Aug 2023 22:34:26 GMT
WORKDIR /var/www/html
# Thu, 17 Aug 2023 22:34:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 17 Aug 2023 22:34:28 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Aug 2023 22:34:28 GMT
EXPOSE 9000
# Thu, 17 Aug 2023 22:34:28 GMT
CMD ["php-fpm"]
# Fri, 18 Aug 2023 02:22:06 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libbz2-dev         libfreetype6-dev         libjpeg-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     extdir="$(php -r 'echo ini_get("extension_dir");')";     ldd "$extdir"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     ldd "$extdir"/*.so | grep -qzv "=> not found" || (echo "Sanity check failed: missing libraries:"; ldd "$extdir"/*.so | grep " => not found"; exit 1);     ldd "$extdir"/*.so | grep -q "libzip.so.* => .*/libzip.so.*" || (echo "Sanity check failed: libzip.so is not referenced"; ldd "$extdir"/*.so; exit 1);     err="$(php --version 3>&1 1>&2 2>&3)";     [ -z "$err" ] || (echo "Sanity check failed: php returned errors; $err"; exit 1;);
# Fri, 18 Aug 2023 02:22:07 GMT
ENV MAX_EXECUTION_TIME=600
# Fri, 18 Aug 2023 02:22:07 GMT
ENV MEMORY_LIMIT=512M
# Fri, 18 Aug 2023 02:22:07 GMT
ENV UPLOAD_LIMIT=2048K
# Fri, 18 Aug 2023 02:22:08 GMT
ENV TZ=UTC
# Fri, 18 Aug 2023 02:22:08 GMT
ENV SESSION_SAVE_PATH=/sessions
# Fri, 18 Aug 2023 02:22:09 GMT
RUN set -ex;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini
# Fri, 18 Aug 2023 02:22:09 GMT
ENV VERSION=5.2.1
# Fri, 18 Aug 2023 02:22:09 GMT
ENV SHA256=373f9599dfbd96d6fe75316d5dad189e68c305f297edf42377db9dd6b41b2557
# Fri, 18 Aug 2023 02:22:10 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.1/phpMyAdmin-5.2.1-all-languages.tar.xz
# Fri, 18 Aug 2023 02:22:10 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.1 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Fri, 18 Aug 2023 02:22:35 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         gnupg         dirmngr     ;     mkdir $SESSION_SAVE_PATH;     chmod 1777 $SESSION_SAVE_PATH;     chown www-data:www-data $SESSION_SAVE_PATH;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     chown www-data:www-data /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 18 Aug 2023 02:22:36 GMT
COPY file:f697d9b67ffcb023f485f153138036d27b209f81ffe35ce3b93a825c617138cd in /etc/phpmyadmin/config.inc.php 
# Fri, 18 Aug 2023 02:22:36 GMT
COPY file:d8c9f50886f5865fe589f64cb31544582913bb98f2cfa51a8828d71871363ce9 in /docker-entrypoint.sh 
# Fri, 18 Aug 2023 02:22:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 18 Aug 2023 02:22:37 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:0500920b409f06d69819525676ebf090702285435050f7b1f973c8c7b034ea7c`  
		Last Modified: Wed, 16 Aug 2023 01:15:59 GMT  
		Size: 33.1 MB (33119300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2e6e5406b2dccdbf8965fa25b50cc70411a95216b41467e2ede0212a0e7f08`  
		Last Modified: Wed, 16 Aug 2023 08:58:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80755cdde4fd6e8e28d68655d3521ec5e67290dfee7272cd3acd0dcc17b068de`  
		Last Modified: Wed, 16 Aug 2023 08:58:43 GMT  
		Size: 103.3 MB (103305694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0254a184608d86c91650e63d986034b42c934a37347cb3805b628077221bd4d`  
		Last Modified: Wed, 16 Aug 2023 08:58:14 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb77ba85cb7de5cc5aa9e293b9d85eb62915229f27d729a7da8c1cc42ff05fab`  
		Last Modified: Thu, 17 Aug 2023 23:27:12 GMT  
		Size: 12.3 MB (12348691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b51a527afa91b46b3785e0b4bdc7a6e138d6507302035bbca9ae24772266dc4`  
		Last Modified: Thu, 17 Aug 2023 23:27:11 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e854b6b20d7285dbeca019020472dc4a90af03bbea78d330435481ed9f04c61`  
		Last Modified: Thu, 17 Aug 2023 23:29:13 GMT  
		Size: 28.9 MB (28861659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a597ef06423ec08f3794865f8857d2b49213498b969fedbfbb7c9f800d29bd`  
		Last Modified: Thu, 17 Aug 2023 23:29:05 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2efd533d7587330e3beb9946573dfb4428c9ad2d9f40ce355c4d9da56affb3d`  
		Last Modified: Thu, 17 Aug 2023 23:29:06 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5d030a72302eae199d4ccfcf244b89bb3fd22a026375e583369e961dfb8fc4`  
		Last Modified: Thu, 17 Aug 2023 23:29:06 GMT  
		Size: 9.2 KB (9186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a888fc0e43f170b931f4ec6f7b299c17cbc9127d6e18fc54ad9e885570c3092`  
		Last Modified: Fri, 18 Aug 2023 02:25:14 GMT  
		Size: 3.1 MB (3131448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19fd88607927ff99bc8acf003186d5c510ac72f9f765b26817bed413a975044`  
		Last Modified: Fri, 18 Aug 2023 02:25:13 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4979f146e4dc221b762fc1ce867a1132af749dbbc3127e32c5e756e808886c51`  
		Last Modified: Fri, 18 Aug 2023 02:25:18 GMT  
		Size: 13.0 MB (13004094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04429a2615c7edfd675084551df9884d681f48cded996996d66f103b1d05ae95`  
		Last Modified: Fri, 18 Aug 2023 02:25:13 GMT  
		Size: 1.6 KB (1616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f77e01e8b54bb84925547f506210e32525460528a7bff3cf687a355c06b3ab52`  
		Last Modified: Fri, 18 Aug 2023 02:25:13 GMT  
		Size: 782.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `phpmyadmin:fpm` - linux; s390x

```console
$ docker pull phpmyadmin@sha256:5e00092255efda7f070b67f59ef6de0406cc59e79ee533ef8a144c39cc6e4ad7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163119794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa2284a672633608d5f7cc8ba53e4dc376fa6a5b93a14f108d993e3c27a9bf17`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 15 Aug 2023 23:42:31 GMT
ADD file:53543c10022986b61ebedef43821a8984443468fb85c225a6fa19c8d6c76f642 in / 
# Tue, 15 Aug 2023 23:42:34 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 07:30:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 16 Aug 2023 07:30:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 16 Aug 2023 07:30:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 07:30:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 16 Aug 2023 07:30:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 16 Aug 2023 07:30:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Aug 2023 07:30:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Aug 2023 07:30:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 16 Aug 2023 07:52:51 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 02 Sep 2023 02:56:12 GMT
ENV PHP_VERSION=8.2.10
# Sat, 02 Sep 2023 02:56:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.10.tar.xz.asc
# Sat, 02 Sep 2023 02:56:13 GMT
ENV PHP_SHA256=561dc4acd5386e47f25be76f2c8df6ae854756469159248313bcf276e282fbb3
# Sat, 02 Sep 2023 02:56:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 02 Sep 2023 02:56:21 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 02 Sep 2023 03:04:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 02 Sep 2023 03:04:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 02 Sep 2023 03:04:18 GMT
RUN docker-php-ext-enable sodium
# Sat, 02 Sep 2023 03:04:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 02 Sep 2023 03:04:18 GMT
WORKDIR /var/www/html
# Sat, 02 Sep 2023 03:04:19 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 02 Sep 2023 03:04:19 GMT
STOPSIGNAL SIGQUIT
# Sat, 02 Sep 2023 03:04:19 GMT
EXPOSE 9000
# Sat, 02 Sep 2023 03:04:19 GMT
CMD ["php-fpm"]
# Sat, 02 Sep 2023 06:22:06 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libbz2-dev         libfreetype6-dev         libjpeg-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     extdir="$(php -r 'echo ini_get("extension_dir");')";     ldd "$extdir"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     ldd "$extdir"/*.so | grep -qzv "=> not found" || (echo "Sanity check failed: missing libraries:"; ldd "$extdir"/*.so | grep " => not found"; exit 1);     ldd "$extdir"/*.so | grep -q "libzip.so.* => .*/libzip.so.*" || (echo "Sanity check failed: libzip.so is not referenced"; ldd "$extdir"/*.so; exit 1);     err="$(php --version 3>&1 1>&2 2>&3)";     [ -z "$err" ] || (echo "Sanity check failed: php returned errors; $err"; exit 1;);
# Sat, 02 Sep 2023 06:22:06 GMT
ENV MAX_EXECUTION_TIME=600
# Sat, 02 Sep 2023 06:22:06 GMT
ENV MEMORY_LIMIT=512M
# Sat, 02 Sep 2023 06:22:06 GMT
ENV UPLOAD_LIMIT=2048K
# Sat, 02 Sep 2023 06:22:07 GMT
ENV TZ=UTC
# Sat, 02 Sep 2023 06:22:07 GMT
ENV SESSION_SAVE_PATH=/sessions
# Sat, 02 Sep 2023 06:22:07 GMT
RUN set -ex;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini
# Sat, 02 Sep 2023 06:22:07 GMT
ENV VERSION=5.2.1
# Sat, 02 Sep 2023 06:22:07 GMT
ENV SHA256=373f9599dfbd96d6fe75316d5dad189e68c305f297edf42377db9dd6b41b2557
# Sat, 02 Sep 2023 06:22:08 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.1/phpMyAdmin-5.2.1-all-languages.tar.xz
# Sat, 02 Sep 2023 06:22:08 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.1 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Sat, 02 Sep 2023 06:22:18 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         gnupg         dirmngr     ;     mkdir $SESSION_SAVE_PATH;     chmod 1777 $SESSION_SAVE_PATH;     chown www-data:www-data $SESSION_SAVE_PATH;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     chown www-data:www-data /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 06:22:19 GMT
COPY file:f697d9b67ffcb023f485f153138036d27b209f81ffe35ce3b93a825c617138cd in /etc/phpmyadmin/config.inc.php 
# Sat, 02 Sep 2023 06:22:20 GMT
COPY file:d8c9f50886f5865fe589f64cb31544582913bb98f2cfa51a8828d71871363ce9 in /docker-entrypoint.sh 
# Sat, 02 Sep 2023 06:22:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 02 Sep 2023 06:22:20 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:e165c0f9e8f698888061cd00c559fc4e4751505fa2e647bfbf5b2ff0dadafbd2`  
		Last Modified: Tue, 15 Aug 2023 23:47:53 GMT  
		Size: 27.5 MB (27489761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e30d834caf2222467a93c5d22e9493c707e2425a7435eeb8657e1709895060`  
		Last Modified: Wed, 16 Aug 2023 09:10:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ad83262d187e94f990c751c94c41771b823f0fb0b3e991f229d2514ddab5a4`  
		Last Modified: Wed, 16 Aug 2023 09:10:55 GMT  
		Size: 80.8 MB (80803885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cc457ca056620bcf6317223056b768b7c0137e6603db8b0341ae10f2bba5fe`  
		Last Modified: Wed, 16 Aug 2023 09:10:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b891bbfea8ff90ab36bd6db3f3c6c8d0f4d8a89515274b7f7a8fc94c08baebbe`  
		Last Modified: Sat, 02 Sep 2023 04:28:26 GMT  
		Size: 12.4 MB (12353314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58bbcd13f0c38b363deba5cbae9eaf71987a0200781595fd796186c4d9b924e`  
		Last Modified: Sat, 02 Sep 2023 04:28:25 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c27256b76b60d88f76bd8fd497f972bda99d6e6a4f945ab83fb01fd760c8a4`  
		Last Modified: Sat, 02 Sep 2023 04:29:07 GMT  
		Size: 26.7 MB (26731213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa36b80dad95c1c771e190b83c5c26b10e1909eb8395c8745fabaf7c2c22cb92`  
		Last Modified: Sat, 02 Sep 2023 04:29:03 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f11b566d3b61f964b0055ed3acb7d7ac826fd9b544e3822c6cebd9adc609ba7`  
		Last Modified: Sat, 02 Sep 2023 04:29:03 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d818f183dc677ccbe9873e4d8a76e86588cf1f6c29c26600b54a4391a7d2106`  
		Last Modified: Sat, 02 Sep 2023 04:29:03 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd9798be4e8a99f36f7463723a21d2fa8ab70bfe2ef0ba6ae550fc521e2f2a6`  
		Last Modified: Sat, 02 Sep 2023 06:23:37 GMT  
		Size: 2.7 MB (2721465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4191ef8d1dacdc1e4474df5d770caf1e048a5a18ea7e216b629074e7ebd1c3fa`  
		Last Modified: Sat, 02 Sep 2023 06:23:37 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6637032c755552a93648e13ff1975ebb5cdfb96dbd91b48dad0d6180ddeb43c5`  
		Last Modified: Sat, 02 Sep 2023 06:23:39 GMT  
		Size: 13.0 MB (13004297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:069a9d4d4572367f10dc7f4b273ff5ad143bb53e549ea9031a21aaf075ada94c`  
		Last Modified: Sat, 02 Sep 2023 06:23:37 GMT  
		Size: 1.6 KB (1615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554be5c99c736b8ff45c6b76b879780a3c0c2a4e7bbaafeb31d73dc370c67ba6`  
		Last Modified: Sat, 02 Sep 2023 06:23:37 GMT  
		Size: 783.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
