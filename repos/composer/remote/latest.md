## `composer:latest`

```console
$ docker pull composer@sha256:3bed9e1168f8689f3454d73b279b52e6de61bec8dc67bf5aebdad7af0aa97f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `composer:latest` - linux; amd64

```console
$ docker pull composer@sha256:cfc2e20a1db2cc3f7b5ad279da5cb1751e2107aad300b7c5103de74f6612d49f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67150386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a4b685d156a93dd11d6cee84a5d2a4db2fddcd58112ca961d73c5449adf0b1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Aug 2021 17:19:45 GMT
ADD file:34eb5c40aa00028921a224d1764ae1b1f3ef710d191e4dfc7df55e0594aa7217 in / 
# Fri, 06 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 22:50:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Aug 2021 22:50:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 06 Aug 2021 22:50:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Aug 2021 22:50:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Aug 2021 22:50:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 06 Aug 2021 22:50:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 22:50:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 22:50:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Aug 2021 23:09:01 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 06 Aug 2021 23:09:01 GMT
ENV PHP_VERSION=8.0.9
# Fri, 06 Aug 2021 23:09:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.9.tar.xz.asc
# Fri, 06 Aug 2021 23:09:02 GMT
ENV PHP_SHA256=71a01b2b56544e20e28696ad5b366e431a0984eaa39aa5e35426a4843e172010
# Fri, 06 Aug 2021 23:09:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 06 Aug 2021 23:09:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Aug 2021 23:17:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Aug 2021 23:17:33 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 06 Aug 2021 23:17:36 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Aug 2021 23:17:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Aug 2021 23:17:36 GMT
CMD ["php" "-a"]
# Tue, 24 Aug 2021 21:19:35 GMT
RUN set -eux;   apk upgrade --no-cache;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Tue, 24 Aug 2021 21:19:36 GMT
RUN set -eux;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://raw.githubusercontent.com/mlocati/docker-php-extension-installer/edf2c4d40de3b86cc1a6e1877eaede05be016389/install-php-extensions;   echo 2c3e48c01d5346be2c6cdd8d6f0a754f107d1119960b3f9d7cad0cae3ac663fb3646eab890310f89aeb3066460fee712034c0f5537608996f9a9f5f413992528 /usr/local/bin/install-php-extensions | sha512sum --strict --check;   chmod +x /usr/local/bin/install-php-extensions
# Tue, 24 Aug 2021 21:20:02 GMT
RUN set -eux;   install-php-extensions     bz2     zip
# Tue, 24 Aug 2021 21:20:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Tue, 24 Aug 2021 21:20:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 24 Aug 2021 21:20:03 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 24 Aug 2021 21:20:03 GMT
ENV COMPOSER_VERSION=2.1.6
# Tue, 24 Aug 2021 21:20:06 GMT
RUN set -eux;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   php -r "     \$signature = '4ac45767e5ec22652f0c1167cbbb8a2b0c708369153e328cad90147dafe50952';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.dev.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, dev public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   php -r "     \$signature = '57815ba27e54dc317ecc7cc5573090d087719ba68f3bb7234e5d42d084a14642';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.tags.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, tags public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   php -r "     \$signature = '756890a4488ce9024fc62c56153228907f1545c228516cbf63f885e036d37e9a59d27d63f46af1d4d07ee0f76181c7d3';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Tue, 24 Aug 2021 21:20:06 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Tue, 24 Aug 2021 21:20:06 GMT
WORKDIR /app
# Tue, 24 Aug 2021 21:20:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Aug 2021 21:20:07 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:29291e31a76a7e560b9b7ad3cada56e8c18d50a96cca8a2573e4f4689d7aca77`  
		Last Modified: Thu, 05 Aug 2021 15:56:25 GMT  
		Size: 2.8 MB (2813006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40df5ce4894c4fe544404fe34e6bb75518b0ae8c6b90819795e09750e8023bc5`  
		Last Modified: Sat, 07 Aug 2021 00:01:43 GMT  
		Size: 1.7 MB (1707767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42904e0b354067c595d0b768fd0ec45eb21ec15058a815b60ade71ee430d732`  
		Last Modified: Sat, 07 Aug 2021 00:01:43 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b0bef73260aa884024d4812378dc7458a626d07690e51be1b680ac2ae2dcb4`  
		Last Modified: Sat, 07 Aug 2021 00:01:43 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67e52d3bd7ecf57d677d30e6b5fd7ed1a8b4aa25807aed469c7c8dcf0ce4b43`  
		Last Modified: Sat, 07 Aug 2021 00:02:49 GMT  
		Size: 10.7 MB (10698204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa625d82d203b81f18bc98df5d3fabdb426efc55b140ab3f87c1a5936d1d865`  
		Last Modified: Sat, 07 Aug 2021 00:02:48 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ae0bbd1d1deeb8a030fdcecf52f4a652ec98374c8adcd47efd171951d56830`  
		Last Modified: Sat, 07 Aug 2021 00:02:51 GMT  
		Size: 15.0 MB (14957954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721381f5e3b5263ccf34fba43994d810511d7473b96d1123b30986778e655959`  
		Last Modified: Sat, 07 Aug 2021 00:02:48 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35fab75c44c21bb83e5f346d58632a857b0bbce597fa6caf0a13032f92df4439`  
		Last Modified: Sat, 07 Aug 2021 00:02:48 GMT  
		Size: 17.8 KB (17787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2068ceff957474cf35f5492b560fa02c133bdf12348f1eabab3d1e9cec2c9e1`  
		Last Modified: Tue, 24 Aug 2021 21:20:39 GMT  
		Size: 36.2 MB (36162563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31503ad8307250ce63a1485df17fcaf9bb19205853ea033535f365b03d9ffeb`  
		Last Modified: Tue, 24 Aug 2021 21:20:33 GMT  
		Size: 19.3 KB (19336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d0ab2698bf55bb9dfa5a482eb089ca25bf6ef2304c70cbe42867b126a483fa`  
		Last Modified: Tue, 24 Aug 2021 21:20:31 GMT  
		Size: 213.0 KB (212958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aada4a18d186c40c5fce5eed378fd23fe91ed784826bfbed8bffaa6111ce801`  
		Last Modified: Tue, 24 Aug 2021 21:20:31 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34b593f73bdc094b29e4300b0ddc9f0423e7f4f4cd78b6702904b825b0d77bf`  
		Last Modified: Tue, 24 Aug 2021 21:20:31 GMT  
		Size: 555.7 KB (555731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67db38d3a7ce498bdddcac7959c52b3fdc0902729c0f6c2dd45bcdb20e873234`  
		Last Modified: Tue, 24 Aug 2021 21:20:31 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cba7e6dcd19c620a1a6d7b8aca992ff4dca4bfcc38ac2aa7459da649340b195`  
		Last Modified: Tue, 24 Aug 2021 21:20:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; arm variant v6

```console
$ docker pull composer@sha256:9024871a5b4d5f6197bc3ca876ec47d722193cdfb7437a3777029e65cb4fe1ef
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62822924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0d60f14d06a7cf85a44c6c8072fa8a39e60b70b570bdfe7ea20b2268eba9978`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Aug 2021 17:49:32 GMT
ADD file:7f2c7deda009eabdcbbdccb11e854043d32c498e64e7e1ca02165d7bb4261d39 in / 
# Fri, 06 Aug 2021 17:49:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 20:25:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Aug 2021 20:25:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 06 Aug 2021 20:25:30 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Aug 2021 20:25:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Aug 2021 20:25:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 06 Aug 2021 20:25:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 20:25:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 20:25:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Aug 2021 20:35:54 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 26 Aug 2021 21:37:36 GMT
ENV PHP_VERSION=8.0.10
# Thu, 26 Aug 2021 21:37:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.10.tar.xz.asc
# Thu, 26 Aug 2021 21:37:37 GMT
ENV PHP_SHA256=66dc4d1bc86d9c1bc255b51b79d337ed1a7a035cf71230daabbf9a4ca35795eb
# Thu, 26 Aug 2021 21:37:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Aug 2021 21:37:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Aug 2021 21:42:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 26 Aug 2021 21:42:27 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 26 Aug 2021 21:42:30 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Aug 2021 21:42:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Aug 2021 21:42:31 GMT
CMD ["php" "-a"]
# Fri, 27 Aug 2021 01:37:29 GMT
RUN set -eux;   apk upgrade --no-cache;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Aug 2021 01:37:31 GMT
RUN set -eux;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://raw.githubusercontent.com/mlocati/docker-php-extension-installer/edf2c4d40de3b86cc1a6e1877eaede05be016389/install-php-extensions;   echo 2c3e48c01d5346be2c6cdd8d6f0a754f107d1119960b3f9d7cad0cae3ac663fb3646eab890310f89aeb3066460fee712034c0f5537608996f9a9f5f413992528 /usr/local/bin/install-php-extensions | sha512sum --strict --check;   chmod +x /usr/local/bin/install-php-extensions
# Fri, 27 Aug 2021 01:38:27 GMT
RUN set -eux;   install-php-extensions     bz2     zip
# Fri, 27 Aug 2021 01:38:29 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Aug 2021 01:38:30 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Aug 2021 01:38:30 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Aug 2021 01:38:31 GMT
ENV COMPOSER_VERSION=2.1.6
# Fri, 27 Aug 2021 01:38:35 GMT
RUN set -eux;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   php -r "     \$signature = '4ac45767e5ec22652f0c1167cbbb8a2b0c708369153e328cad90147dafe50952';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.dev.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, dev public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   php -r "     \$signature = '57815ba27e54dc317ecc7cc5573090d087719ba68f3bb7234e5d42d084a14642';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.tags.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, tags public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   php -r "     \$signature = '756890a4488ce9024fc62c56153228907f1545c228516cbf63f885e036d37e9a59d27d63f46af1d4d07ee0f76181c7d3';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Aug 2021 01:38:36 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 27 Aug 2021 01:38:36 GMT
WORKDIR /app
# Fri, 27 Aug 2021 01:38:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Aug 2021 01:38:37 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:f465bb3e9fcd0c42f936ecc566c6e40353c00f3089b2b2c2ea1663c30f89d3ab`  
		Last Modified: Fri, 06 Aug 2021 17:51:00 GMT  
		Size: 2.6 MB (2626350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c308e0cc29c44fbd995ee591fe7289bde1e488176fb402318132d40caa05c299`  
		Last Modified: Fri, 06 Aug 2021 21:25:23 GMT  
		Size: 1.7 MB (1696670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983c92fbbed0d3241e2a4aa8f6ec320484791f6923f18c795878fea03971b8bd`  
		Last Modified: Fri, 06 Aug 2021 21:25:22 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f89139d48debd7c21fa5272e8bb4a983181e2f8d1f37a9f65ee5c99086cd7c`  
		Last Modified: Fri, 06 Aug 2021 21:25:22 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ec4769f82ce3367d73237dbdf73660e5b378e979d1ad37c5547da846d1249f`  
		Last Modified: Thu, 26 Aug 2021 23:12:55 GMT  
		Size: 10.7 MB (10722828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8d5f7bceeb387f192db3ff0941fee44d2e21fa34cc5b13624a7136839a95b1`  
		Last Modified: Thu, 26 Aug 2021 23:12:52 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b668aac95432f50545c3ef68f159d0aab1d131c1519c9a85ce31dde26bee9fd8`  
		Last Modified: Thu, 26 Aug 2021 23:13:03 GMT  
		Size: 15.0 MB (15017066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354bed15e1d4666170b80cd35659fa482dfd187e8274e8073ec6e2ae9750c171`  
		Last Modified: Thu, 26 Aug 2021 23:12:52 GMT  
		Size: 2.3 KB (2269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7493dd89e93ccd4d8bfcefb097eb43551e469901cd13e27e77dafce9b46b73df`  
		Last Modified: Thu, 26 Aug 2021 23:12:52 GMT  
		Size: 17.9 KB (17859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5f154a95262a8681c11c9ed7140d97a0cdb343dd830cad6961bf4e0a7498bd`  
		Last Modified: Fri, 27 Aug 2021 01:40:02 GMT  
		Size: 32.0 MB (31955913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e255df132cc5e3cb549c7c109467f58ce4686674b236b5b720da602357b07ed`  
		Last Modified: Fri, 27 Aug 2021 01:39:39 GMT  
		Size: 19.3 KB (19333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff571f0990a81ceec47f9765b9cccd67292ecb3ff2d3c114308bb642da946cb`  
		Last Modified: Fri, 27 Aug 2021 01:39:37 GMT  
		Size: 206.1 KB (206101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe5d82b0d18071140dcd74c426bed634193cdb59a81e2c894253b9c9bb340bb`  
		Last Modified: Fri, 27 Aug 2021 01:39:37 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a292ad00c5c194b8661fa41a6b02c71b2ecf6dad68f8b788fbfd247b30d244ad`  
		Last Modified: Fri, 27 Aug 2021 01:39:38 GMT  
		Size: 555.7 KB (555720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2871da3de4a15fcf2350fb1685751b466710e0bfac5c5e24c08a3d620e115f65`  
		Last Modified: Fri, 27 Aug 2021 01:39:37 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c06e89562bb6a1bc0de60e97887f423eb3e60e5b0e49e1eb0946dfce0188c8`  
		Last Modified: Fri, 27 Aug 2021 01:39:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; arm variant v7

```console
$ docker pull composer@sha256:d5d4a910dfb42fbd22567913b1c220b0945378a108b765959a6d62ebe2eae8fd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59859046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d409e348b9f093f170f86ba319d77b339733864f0fae17276c3575e0fb21ba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Aug 2021 17:57:32 GMT
ADD file:3a35ff3ac0d80289d419a4d6d8319610c38e1936d296addafb9aaf506946230f in / 
# Fri, 06 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 20:54:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Aug 2021 20:54:19 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 06 Aug 2021 20:54:20 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Aug 2021 20:54:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Aug 2021 20:54:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 06 Aug 2021 20:54:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 20:54:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 20:54:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Aug 2021 21:05:21 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 06 Aug 2021 21:05:22 GMT
ENV PHP_VERSION=8.0.9
# Fri, 06 Aug 2021 21:05:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.9.tar.xz.asc
# Fri, 06 Aug 2021 21:05:23 GMT
ENV PHP_SHA256=71a01b2b56544e20e28696ad5b366e431a0984eaa39aa5e35426a4843e172010
# Fri, 06 Aug 2021 21:05:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 06 Aug 2021 21:05:31 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Aug 2021 21:09:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Aug 2021 21:09:29 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 06 Aug 2021 21:09:32 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Aug 2021 21:09:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Aug 2021 21:09:33 GMT
CMD ["php" "-a"]
# Tue, 24 Aug 2021 22:24:02 GMT
RUN set -eux;   apk upgrade --no-cache;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Tue, 24 Aug 2021 22:24:04 GMT
RUN set -eux;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://raw.githubusercontent.com/mlocati/docker-php-extension-installer/edf2c4d40de3b86cc1a6e1877eaede05be016389/install-php-extensions;   echo 2c3e48c01d5346be2c6cdd8d6f0a754f107d1119960b3f9d7cad0cae3ac663fb3646eab890310f89aeb3066460fee712034c0f5537608996f9a9f5f413992528 /usr/local/bin/install-php-extensions | sha512sum --strict --check;   chmod +x /usr/local/bin/install-php-extensions
# Tue, 24 Aug 2021 22:24:58 GMT
RUN set -eux;   install-php-extensions     bz2     zip
# Tue, 24 Aug 2021 22:25:00 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Tue, 24 Aug 2021 22:25:00 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 24 Aug 2021 22:25:01 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 24 Aug 2021 22:25:01 GMT
ENV COMPOSER_VERSION=2.1.6
# Tue, 24 Aug 2021 22:25:05 GMT
RUN set -eux;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   php -r "     \$signature = '4ac45767e5ec22652f0c1167cbbb8a2b0c708369153e328cad90147dafe50952';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.dev.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, dev public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   php -r "     \$signature = '57815ba27e54dc317ecc7cc5573090d087719ba68f3bb7234e5d42d084a14642';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.tags.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, tags public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   php -r "     \$signature = '756890a4488ce9024fc62c56153228907f1545c228516cbf63f885e036d37e9a59d27d63f46af1d4d07ee0f76181c7d3';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Tue, 24 Aug 2021 22:25:06 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Tue, 24 Aug 2021 22:25:06 GMT
WORKDIR /app
# Tue, 24 Aug 2021 22:25:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Aug 2021 22:25:07 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:4ee0caa23b369b04827640a4be298bf4ff7bacd030c77e915f5d7fb8f987594a`  
		Last Modified: Fri, 06 Aug 2021 17:58:57 GMT  
		Size: 2.4 MB (2429359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60e2d83b5c992b22cef3665b0ab131088923cffff86634ff4237393a231b13d`  
		Last Modified: Fri, 06 Aug 2021 22:04:23 GMT  
		Size: 1.6 MB (1564630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d851eb12a849920c3886c6a5cc4c6ff6340be6574eae5478f604b4428ab1dc3`  
		Last Modified: Fri, 06 Aug 2021 22:04:22 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7635ae9ae7b01f3f897bee725eb55f2ee4ea71056d85205467700b3d753efc`  
		Last Modified: Fri, 06 Aug 2021 22:04:22 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82da596cafc0fa431be2b06a7d271dc033223a5d45a953d82bd3ea79d6e60983`  
		Last Modified: Fri, 06 Aug 2021 22:06:45 GMT  
		Size: 10.7 MB (10698200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0169c233b02c475a2914d1a8a69c74101c7d0378389f6d371493d64d4b216f81`  
		Last Modified: Fri, 06 Aug 2021 22:06:42 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f815d80da7eb432757f3565b8f68ee5d63817ac0cfae94f9176bcd0374660cce`  
		Last Modified: Fri, 06 Aug 2021 22:06:51 GMT  
		Size: 12.7 MB (12738219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d72d98acb6b8d6521b8769c88846af927351bbce23ac0a4020936081e0e32fc`  
		Last Modified: Fri, 06 Aug 2021 22:06:42 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfec910c009f5f40586bf841e2cf269edba5bc60085761ee4daa8666bc5b7ad1`  
		Last Modified: Fri, 06 Aug 2021 22:06:42 GMT  
		Size: 17.8 KB (17776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d988efe516daf70b509589c3f17f9edce819c2cf9240d4c33789d4fe17ae6186`  
		Last Modified: Tue, 24 Aug 2021 22:26:36 GMT  
		Size: 31.6 MB (31632352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb7b8783e4c8f0966f675d813a16f49b1eba0861bf0b041e6ac9b14342e8c25`  
		Last Modified: Tue, 24 Aug 2021 22:26:15 GMT  
		Size: 19.3 KB (19337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8ad3092cf9ff08075e81940304c5326c556de4be4a9f09d83d11659253bbfb`  
		Last Modified: Tue, 24 Aug 2021 22:26:14 GMT  
		Size: 198.4 KB (198369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c01fc0a2068c76842e0aa03df46f6b726651f3da84015d2868fbd4036368ec0`  
		Last Modified: Tue, 24 Aug 2021 22:26:13 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a4b544b5e91f29eaf9c27d8b673f20035fc5d2f17c7b23e8d09ed84f9b84b7`  
		Last Modified: Tue, 24 Aug 2021 22:26:14 GMT  
		Size: 555.7 KB (555721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916e7706999b22665f5bbd09f9b966053c610238053c3a7185981fb58c366a93`  
		Last Modified: Tue, 24 Aug 2021 22:26:13 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2825fe75c08a1ba837edfbcb3557e1d04c4dc5ce3ac021208e5b36b35743b5`  
		Last Modified: Tue, 24 Aug 2021 22:26:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:c6e30299fc47d66385505e2e60ee216a3f9313d6284ae91ccc288b0982cc30ec
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64674045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f557d6320edf2f326e28c051f945b6f7d3eca33bf791a950f5c51479344ebd8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Aug 2021 17:39:26 GMT
ADD file:1a8fd1066485e1261462e689c1a072f010c1d3be904b73ef2b84128fac652951 in / 
# Fri, 06 Aug 2021 17:39:27 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 22:13:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Aug 2021 22:13:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 06 Aug 2021 22:13:46 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Aug 2021 22:13:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Aug 2021 22:13:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 06 Aug 2021 22:13:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 22:13:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 22:13:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Aug 2021 22:29:25 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 06 Aug 2021 22:29:25 GMT
ENV PHP_VERSION=8.0.9
# Fri, 06 Aug 2021 22:29:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.9.tar.xz.asc
# Fri, 06 Aug 2021 22:29:25 GMT
ENV PHP_SHA256=71a01b2b56544e20e28696ad5b366e431a0984eaa39aa5e35426a4843e172010
# Fri, 06 Aug 2021 22:29:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 06 Aug 2021 22:29:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Aug 2021 22:34:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Aug 2021 22:34:27 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 06 Aug 2021 22:34:29 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Aug 2021 22:34:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Aug 2021 22:34:29 GMT
CMD ["php" "-a"]
# Tue, 24 Aug 2021 21:39:33 GMT
RUN set -eux;   apk upgrade --no-cache;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Tue, 24 Aug 2021 21:39:34 GMT
RUN set -eux;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://raw.githubusercontent.com/mlocati/docker-php-extension-installer/edf2c4d40de3b86cc1a6e1877eaede05be016389/install-php-extensions;   echo 2c3e48c01d5346be2c6cdd8d6f0a754f107d1119960b3f9d7cad0cae3ac663fb3646eab890310f89aeb3066460fee712034c0f5537608996f9a9f5f413992528 /usr/local/bin/install-php-extensions | sha512sum --strict --check;   chmod +x /usr/local/bin/install-php-extensions
# Tue, 24 Aug 2021 21:40:01 GMT
RUN set -eux;   install-php-extensions     bz2     zip
# Tue, 24 Aug 2021 21:40:02 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Tue, 24 Aug 2021 21:40:02 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 24 Aug 2021 21:40:02 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 24 Aug 2021 21:40:03 GMT
ENV COMPOSER_VERSION=2.1.6
# Tue, 24 Aug 2021 21:40:06 GMT
RUN set -eux;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   php -r "     \$signature = '4ac45767e5ec22652f0c1167cbbb8a2b0c708369153e328cad90147dafe50952';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.dev.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, dev public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   php -r "     \$signature = '57815ba27e54dc317ecc7cc5573090d087719ba68f3bb7234e5d42d084a14642';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.tags.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, tags public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   php -r "     \$signature = '756890a4488ce9024fc62c56153228907f1545c228516cbf63f885e036d37e9a59d27d63f46af1d4d07ee0f76181c7d3';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Tue, 24 Aug 2021 21:40:06 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Tue, 24 Aug 2021 21:40:06 GMT
WORKDIR /app
# Tue, 24 Aug 2021 21:40:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Aug 2021 21:40:07 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:fd3acdcea5682abced546ec19fb6ebee725c5184e5d91614c469c0a79e67f2d0`  
		Last Modified: Fri, 06 Aug 2021 17:40:12 GMT  
		Size: 2.7 MB (2710613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e75c04557b83c6887fa33eb52320a5c1afed1d1b8299d3accdf27cea6b5860`  
		Last Modified: Fri, 06 Aug 2021 23:19:35 GMT  
		Size: 1.7 MB (1710420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6439bb8bd6ba02680eef64ad51b996399f05a740cd7ab8e62834b24527f60c`  
		Last Modified: Fri, 06 Aug 2021 23:19:35 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d61d6c7061c67dabfce2227dc9665b59eb7c43fd2f927c11e7c76446b50fed3`  
		Last Modified: Fri, 06 Aug 2021 23:19:35 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c0acbcced8e114e5b3c708dbceeee08fa3a39e95c9b3aa8a62ee63c505a8e8`  
		Last Modified: Fri, 06 Aug 2021 23:21:05 GMT  
		Size: 10.7 MB (10698209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5d6bcb7cfb10d9b61722fadee900785edfb4ccaafc977dfd17aa9b8d8f828f`  
		Last Modified: Fri, 06 Aug 2021 23:21:04 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f05107f18a048512b1e63e652aab792e0a4fb2c18444265dbc06692aa5dedb7`  
		Last Modified: Fri, 06 Aug 2021 23:21:07 GMT  
		Size: 14.4 MB (14395707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c75f30d657ae897d78ec5b5f826700bb068c9cb88983842e2e40aec158c616`  
		Last Modified: Fri, 06 Aug 2021 23:21:04 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553e8a7174bc7aff89aad9b89609d6148499d467e61a5563b76ef5160741a54e`  
		Last Modified: Fri, 06 Aug 2021 23:21:05 GMT  
		Size: 17.8 KB (17788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfe137f03805095df38b9916cc8183391d7f2469c4444ef3e5f9ec17a84b184`  
		Last Modified: Tue, 24 Aug 2021 21:40:47 GMT  
		Size: 34.4 MB (34351091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecc3db5e2709436daf02dffa02faf6c6eeef55f9ded818316d00c0d66c668a2`  
		Last Modified: Tue, 24 Aug 2021 21:40:41 GMT  
		Size: 19.3 KB (19335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d480cefbbbf97740a446e84b52ee877a6c91a489953780eb6cc66b5a7fab5d9`  
		Last Modified: Tue, 24 Aug 2021 21:40:39 GMT  
		Size: 210.1 KB (210070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a947244ac095f01c7b585ccb2b13cf6a7101f8860f38569dd7b436c2d291df2e`  
		Last Modified: Tue, 24 Aug 2021 21:40:38 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a888c9f1212364a12e85724ca98f6e7f4f71169b59ec34df0aa466afd9b20578`  
		Last Modified: Tue, 24 Aug 2021 21:40:39 GMT  
		Size: 555.7 KB (555731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36065af4cd558a19e6a3828f72e3a56ec9a36c1cfbec9af42f7110121cf33eab`  
		Last Modified: Tue, 24 Aug 2021 21:40:38 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e653eef23693bfcb633a4978b82a6671959e6a6506c1f04957f91b58ef0e45`  
		Last Modified: Tue, 24 Aug 2021 21:40:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; 386

```console
$ docker pull composer@sha256:4e02e46ed491da94fe6208449f23bbe2e2c1e2a1b9133b66d659313ac2ec6735
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64112372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b774738d9ed1e3b862eb23e484734c85512fb40e0f82e8b7e8640d514edaca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 03:38:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Apr 2021 03:38:46 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 15 Apr 2021 03:38:47 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 15 Apr 2021 03:38:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Apr 2021 03:38:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 15 Apr 2021 03:38:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Apr 2021 03:38:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Apr 2021 03:38:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Apr 2021 03:38:49 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 04 Jun 2021 19:14:53 GMT
ENV PHP_VERSION=8.0.7
# Fri, 04 Jun 2021 19:14:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.7.tar.xz.asc
# Fri, 04 Jun 2021 19:14:53 GMT
ENV PHP_SHA256=d5fc2e4fc780a32404d88c360e3e0009bc725d936459668e9c2ac992f2d83654
# Fri, 04 Jun 2021 19:15:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Jun 2021 19:15:02 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Jun 2021 19:25:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Jun 2021 19:25:19 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 04 Jun 2021 19:25:21 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Jun 2021 19:25:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Jun 2021 19:25:22 GMT
CMD ["php" "-a"]
# Fri, 04 Jun 2021 20:42:45 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 04 Jun 2021 20:42:56 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 04 Jun 2021 20:42:57 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 04 Jun 2021 20:42:57 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Jun 2021 20:42:57 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 10 Jun 2021 17:38:29 GMT
ENV COMPOSER_VERSION=2.1.3
# Thu, 10 Jun 2021 17:38:32 GMT
RUN set -eux;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   php -r "     \$signature = '4ac45767e5ec22652f0c1167cbbb8a2b0c708369153e328cad90147dafe50952';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.dev.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, dev public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   php -r "     \$signature = '57815ba27e54dc317ecc7cc5573090d087719ba68f3bb7234e5d42d084a14642';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.tags.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, tags public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer   ;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 10 Jun 2021 17:38:32 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 10 Jun 2021 17:38:33 GMT
WORKDIR /app
# Thu, 10 Jun 2021 17:38:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 10 Jun 2021 17:38:33 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3818e7e8eb8d9c0ab0e377e89ed7df3037ec2c0d4c4c89bd3a2abedc459366c`  
		Last Modified: Thu, 15 Apr 2021 05:57:45 GMT  
		Size: 1.8 MB (1799274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274cbc3732aca6ca32c0ba51f7504eb2d19d4fd52d0f89f9ff2597a673484be8`  
		Last Modified: Thu, 15 Apr 2021 05:57:43 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32aa0b7923dc47bd54c1e8cc895686f0638c3a28a9a40f8ed831545df00ce891`  
		Last Modified: Thu, 15 Apr 2021 05:57:46 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c11bf4cbd32494a063621f918fa784556315a314c6d78e5d19dbfc8bd942ab0`  
		Last Modified: Fri, 04 Jun 2021 19:58:41 GMT  
		Size: 10.8 MB (10788550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7825c7bdb9d266701c9228b54056b249ead9c87bb7c598cc697b4e9129cacaae`  
		Last Modified: Fri, 04 Jun 2021 19:58:39 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fc4bd5e9a72405e0b9d3bcdbe0b7262e762c791870713d50bef19042426075`  
		Last Modified: Fri, 04 Jun 2021 19:58:44 GMT  
		Size: 15.6 MB (15569700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909ee12d174e4a1b14451096ba719a4ee697691d0d87bca3bbc007780ac8b9d1`  
		Last Modified: Fri, 04 Jun 2021 19:58:39 GMT  
		Size: 2.3 KB (2264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0db7581e2c6a9e29181306bc72b568bcd37d34d86e82848ab39e9339e1402e8`  
		Last Modified: Fri, 04 Jun 2021 19:58:40 GMT  
		Size: 17.6 KB (17588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a68082e643a7fc161f84cc28dc2bf16a7887e2d4308bd28ecc6fe8b8629886`  
		Last Modified: Fri, 04 Jun 2021 20:43:48 GMT  
		Size: 32.3 MB (32344854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a803220d3be252a04d891ac0da77a9f2ea0f49316dcace07e32952ece50fa6`  
		Last Modified: Fri, 04 Jun 2021 20:43:38 GMT  
		Size: 213.9 KB (213906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03742a6d31e0579e49ad310eef763db9a43325091247f01681d12fb81eccc71`  
		Last Modified: Fri, 04 Jun 2021 20:43:38 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3b7f2db5bc1d340325eeb496287221d43e4ca8251f3bb179744bf7d8cf603a`  
		Last Modified: Thu, 10 Jun 2021 17:39:01 GMT  
		Size: 554.5 KB (554520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63498ecde104628b29fe215bb8920fba90808cbcbe53ae3509376ba3f7319ba3`  
		Last Modified: Thu, 10 Jun 2021 17:39:01 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c476d4a236204c45b6b1aad0808d984df1ec4a7410c75ae462adfc04487296eb`  
		Last Modified: Thu, 10 Jun 2021 17:39:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; ppc64le

```console
$ docker pull composer@sha256:cedae52c08ff3ec536be815a50bc56381a0bb4065e16451b053d231a0c522721
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67064025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc82748227dc1512a115f011f3d2b069a18c3c64faf9ea8839a00ed03af767d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Aug 2021 18:28:28 GMT
ADD file:40f3b617d7ff269d92f0ffcf8aad561b5f2c0626ef519a7f584f1ba0182b3188 in / 
# Fri, 06 Aug 2021 18:28:35 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 23:16:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Aug 2021 23:17:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 06 Aug 2021 23:17:20 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Aug 2021 23:17:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Aug 2021 23:17:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 06 Aug 2021 23:17:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 23:17:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 23:17:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Aug 2021 23:31:24 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 06 Aug 2021 23:31:27 GMT
ENV PHP_VERSION=8.0.9
# Fri, 06 Aug 2021 23:31:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.9.tar.xz.asc
# Fri, 06 Aug 2021 23:31:32 GMT
ENV PHP_SHA256=71a01b2b56544e20e28696ad5b366e431a0984eaa39aa5e35426a4843e172010
# Fri, 06 Aug 2021 23:31:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 06 Aug 2021 23:31:48 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Aug 2021 23:36:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Aug 2021 23:36:39 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 06 Aug 2021 23:36:47 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Aug 2021 23:36:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Aug 2021 23:36:55 GMT
CMD ["php" "-a"]
# Tue, 24 Aug 2021 21:17:03 GMT
RUN set -eux;   apk upgrade --no-cache;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Tue, 24 Aug 2021 21:17:30 GMT
RUN set -eux;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://raw.githubusercontent.com/mlocati/docker-php-extension-installer/edf2c4d40de3b86cc1a6e1877eaede05be016389/install-php-extensions;   echo 2c3e48c01d5346be2c6cdd8d6f0a754f107d1119960b3f9d7cad0cae3ac663fb3646eab890310f89aeb3066460fee712034c0f5537608996f9a9f5f413992528 /usr/local/bin/install-php-extensions | sha512sum --strict --check;   chmod +x /usr/local/bin/install-php-extensions
# Tue, 24 Aug 2021 21:18:35 GMT
RUN set -eux;   install-php-extensions     bz2     zip
# Tue, 24 Aug 2021 21:18:44 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Tue, 24 Aug 2021 21:18:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 24 Aug 2021 21:18:53 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 24 Aug 2021 21:18:59 GMT
ENV COMPOSER_VERSION=2.1.6
# Tue, 24 Aug 2021 21:19:25 GMT
RUN set -eux;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   php -r "     \$signature = '4ac45767e5ec22652f0c1167cbbb8a2b0c708369153e328cad90147dafe50952';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.dev.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, dev public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   php -r "     \$signature = '57815ba27e54dc317ecc7cc5573090d087719ba68f3bb7234e5d42d084a14642';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.tags.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, tags public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   php -r "     \$signature = '756890a4488ce9024fc62c56153228907f1545c228516cbf63f885e036d37e9a59d27d63f46af1d4d07ee0f76181c7d3';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Tue, 24 Aug 2021 21:19:30 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Tue, 24 Aug 2021 21:19:41 GMT
WORKDIR /app
# Tue, 24 Aug 2021 21:19:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Aug 2021 21:19:54 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:0ff902055236f70c4694c806877243e1dd52c513825a2a3ecc7eba8f5202acc8`  
		Last Modified: Fri, 06 Aug 2021 18:29:33 GMT  
		Size: 2.8 MB (2811152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6ff25f38da82eae5b2405214e57c7c39a03ddb9e5eb9d04b31edf4dcc07669`  
		Last Modified: Sat, 07 Aug 2021 00:29:55 GMT  
		Size: 1.8 MB (1753673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af333e5ee6f8ffe8b982f0c46d826dbc17bbc35803e4c60443beea3af1ab1bc`  
		Last Modified: Sat, 07 Aug 2021 00:29:54 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c80d5e8e81136737bd0d714e4bbecc9480689bf7e1faf489f1ad332150d992`  
		Last Modified: Sat, 07 Aug 2021 00:29:54 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3881d096611c361e85cb37932cd5461bf9279391f0c70ee19fcd381ff21085e`  
		Last Modified: Sat, 07 Aug 2021 00:31:38 GMT  
		Size: 10.7 MB (10698207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e18e7693ac56c64a45d1f92442689618857bf7c14c191e66396672d9dfa21b`  
		Last Modified: Sat, 07 Aug 2021 00:31:36 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3d970e94ac55b458bd440157dd4ebeff987b330da614e503febc4bd8804775`  
		Last Modified: Sat, 07 Aug 2021 00:31:40 GMT  
		Size: 15.7 MB (15691529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa782a12845b2756bf1b9007a53bc921e39ff1b0ac1ffb35d5b919c3179a832`  
		Last Modified: Sat, 07 Aug 2021 00:31:36 GMT  
		Size: 2.3 KB (2265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7da2181c5829ba6c70625faed8cc46d740dbd874ad5ff767bcda1472cd96117`  
		Last Modified: Sat, 07 Aug 2021 00:31:36 GMT  
		Size: 17.8 KB (17789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac276ac2f4c0a0e73f0e42b9b5a0bd12def375f503eab6052cf273b3b833638`  
		Last Modified: Tue, 24 Aug 2021 21:21:57 GMT  
		Size: 35.3 MB (35291260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25dc797aed49df72b2b4541d50a84db213ca3c6413507b4ee2fe1aaf64f594d7`  
		Last Modified: Tue, 24 Aug 2021 21:21:49 GMT  
		Size: 19.3 KB (19337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c198f595078b7302fa896ff128d0142fb6988ff2c1f9bf88299a20a931bad67`  
		Last Modified: Tue, 24 Aug 2021 21:21:46 GMT  
		Size: 220.3 KB (220261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91916fb4190c07c62b255884c221d03896912255fe98a16b424225b8806c0d0`  
		Last Modified: Tue, 24 Aug 2021 21:21:45 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c4d72d716596010a50e5e8c552b84ca1a9fc6ed8142ea5270619d00cc7da74`  
		Last Modified: Tue, 24 Aug 2021 21:21:45 GMT  
		Size: 555.7 KB (555735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4488abafb8100aaa2fb9e88be3d3cb5e9fdeae6e00b2fbc58cd5a40e20fa20f9`  
		Last Modified: Tue, 24 Aug 2021 21:21:45 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d495b0afd069da8bae08e880354d822a682468073cad659e6df8261d1beb21ea`  
		Last Modified: Tue, 24 Aug 2021 21:21:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; s390x

```console
$ docker pull composer@sha256:88747956fa965d0c0279cb0da61672c80cd4f223c6a82dec1876e3e6d742791b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65973111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ac359bb248bfa007056c486df47b57127af66cb54433510c927f17979c5dc8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Aug 2021 17:41:30 GMT
ADD file:bdf19d63e9f8600d2fbe02435279b8df06fbcb5105e6b8eea778d8ef928e219a in / 
# Fri, 06 Aug 2021 17:41:31 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:04:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Aug 2021 19:04:44 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 06 Aug 2021 19:04:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Aug 2021 19:04:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Aug 2021 19:04:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 06 Aug 2021 19:04:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 19:04:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 19:04:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Aug 2021 19:12:31 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 06 Aug 2021 19:12:32 GMT
ENV PHP_VERSION=8.0.9
# Fri, 06 Aug 2021 19:12:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.9.tar.xz.asc
# Fri, 06 Aug 2021 19:12:33 GMT
ENV PHP_SHA256=71a01b2b56544e20e28696ad5b366e431a0984eaa39aa5e35426a4843e172010
# Fri, 06 Aug 2021 19:12:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 06 Aug 2021 19:12:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 20 Aug 2021 17:56:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 20 Aug 2021 17:56:54 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 20 Aug 2021 17:56:56 GMT
RUN docker-php-ext-enable sodium
# Fri, 20 Aug 2021 17:56:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 20 Aug 2021 17:56:57 GMT
CMD ["php" "-a"]
# Tue, 24 Aug 2021 21:41:34 GMT
RUN set -eux;   apk upgrade --no-cache;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Tue, 24 Aug 2021 21:41:37 GMT
RUN set -eux;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://raw.githubusercontent.com/mlocati/docker-php-extension-installer/edf2c4d40de3b86cc1a6e1877eaede05be016389/install-php-extensions;   echo 2c3e48c01d5346be2c6cdd8d6f0a754f107d1119960b3f9d7cad0cae3ac663fb3646eab890310f89aeb3066460fee712034c0f5537608996f9a9f5f413992528 /usr/local/bin/install-php-extensions | sha512sum --strict --check;   chmod +x /usr/local/bin/install-php-extensions
# Tue, 24 Aug 2021 21:42:05 GMT
RUN set -eux;   install-php-extensions     bz2     zip
# Tue, 24 Aug 2021 21:42:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Tue, 24 Aug 2021 21:42:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 24 Aug 2021 21:42:07 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 24 Aug 2021 21:42:07 GMT
ENV COMPOSER_VERSION=2.1.6
# Tue, 24 Aug 2021 21:42:10 GMT
RUN set -eux;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   php -r "     \$signature = '4ac45767e5ec22652f0c1167cbbb8a2b0c708369153e328cad90147dafe50952';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.dev.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, dev public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   php -r "     \$signature = '57815ba27e54dc317ecc7cc5573090d087719ba68f3bb7234e5d42d084a14642';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.tags.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, tags public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   php -r "     \$signature = '756890a4488ce9024fc62c56153228907f1545c228516cbf63f885e036d37e9a59d27d63f46af1d4d07ee0f76181c7d3';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Tue, 24 Aug 2021 21:42:10 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Tue, 24 Aug 2021 21:42:10 GMT
WORKDIR /app
# Tue, 24 Aug 2021 21:42:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Aug 2021 21:42:11 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:625f57562315453466f73bc9d8c96e678f8d4ea436b462d06c60fb217c6b3d38`  
		Last Modified: Fri, 06 Aug 2021 17:42:42 GMT  
		Size: 2.6 MB (2602036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2568987867095245025c394f06456a47a6c8bdaa6c96639c49ddb43f6bff047`  
		Last Modified: Fri, 20 Aug 2021 19:50:42 GMT  
		Size: 1.8 MB (1768133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd26dcb760c8a12fd1e292df471c9fde4aba0c4c70b845397a1dfe2e434b942b`  
		Last Modified: Fri, 20 Aug 2021 19:50:41 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba8a5b372f3024025b5c742c3ac12e1b59f6c09600dbc45c2ce807f5dfa3935`  
		Last Modified: Fri, 20 Aug 2021 19:50:41 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b01289b0e0cbd2f68fc4dc9b00076d28b24cb7fcb376ccc637d8d05f2caa7f8`  
		Last Modified: Fri, 20 Aug 2021 19:53:18 GMT  
		Size: 10.7 MB (10698211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ab29a7029877b44759e796b36194309d242f38ab25e5a0d359048b257fbb6a`  
		Last Modified: Fri, 20 Aug 2021 19:53:17 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c9e104995c049eabe5d86ec47e8c7edec5cae32307abab6439d25911080104`  
		Last Modified: Fri, 20 Aug 2021 19:53:21 GMT  
		Size: 14.0 MB (13989585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537aa271badc24dc085cd5e35e70b797fa4affbad15cbc2c9c22ccf744508e9a`  
		Last Modified: Fri, 20 Aug 2021 19:53:17 GMT  
		Size: 2.3 KB (2265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30125c692ceff78f7a1d446413796196185c70ecc66964cf103765330050c938`  
		Last Modified: Fri, 20 Aug 2021 19:53:17 GMT  
		Size: 17.8 KB (17796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f31ea9962b1f5692c46f256297e18335dea12be2f050cc46e1145059ad51d6`  
		Last Modified: Tue, 24 Aug 2021 21:42:56 GMT  
		Size: 36.1 MB (36104827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785d8f99e9501e402e43c3a675d1eb607b99842cc061b4c79be44d94ced766f3`  
		Last Modified: Tue, 24 Aug 2021 21:42:51 GMT  
		Size: 19.3 KB (19338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60c0fcc108b459c7fe268e250b6a167a48793caf01099047e8bcceea2209bce`  
		Last Modified: Tue, 24 Aug 2021 21:42:49 GMT  
		Size: 212.4 KB (212378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab9658f067fb3990ee32972c9eec8bab7714cd6a9a1fd9e36145107dd5a0590`  
		Last Modified: Tue, 24 Aug 2021 21:42:49 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5502a472e2914d56f8e82651f8e49724f0c91ab9d2c77555c2cf5fc30f3a35eb`  
		Last Modified: Tue, 24 Aug 2021 21:42:50 GMT  
		Size: 555.7 KB (555726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345cb3a7e8c898bcf966c1fed3f07f145edaf43b0e43e43b32374f6c45d0a2d0`  
		Last Modified: Tue, 24 Aug 2021 21:42:49 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b57ccbad306c75efcb12feacb5196d82f6e1a320e5ba1e91d6191ebf3564da6`  
		Last Modified: Tue, 24 Aug 2021 21:42:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
