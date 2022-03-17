<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `composer`

-	[`composer:1`](#composer1)
-	[`composer:1.10`](#composer110)
-	[`composer:1.10.25`](#composer11025)
-	[`composer:2`](#composer2)
-	[`composer:2.2`](#composer22)
-	[`composer:2.2.9`](#composer229)
-	[`composer:2.3`](#composer23)
-	[`composer:2.3.0-RC1`](#composer230-rc1)
-	[`composer:latest`](#composerlatest)

## `composer:1`

```console
$ docker pull composer@sha256:859e2699e66e8111ed3da99a5243c655320ef720b35cb1d4f4a1ac7eab02fbc3
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

### `composer:1` - linux; amd64

```console
$ docker pull composer@sha256:f5638759bd7404ac2476beb05944f8e8d034420637d91d701257c3ca70d9d866
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71492923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1e7fca3c4e94ca9e65eaeb1002bf92b77423c74b21949fbb3ed1d007a8f63e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 07:06:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 07:06:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 07:06:04 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 07:06:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 07:06:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 07:06:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 07:06:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 07:06:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 07:06:06 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:16:49 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:16:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:16:50 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:17:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:17:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:06:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 04:06:01 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:06:03 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 04:06:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 04:06:03 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 11:55:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 11:55:50 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 11:55:50 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 11:55:50 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Mar 2022 11:56:14 GMT
ENV COMPOSER_VERSION=1.10.25
# Fri, 11 Mar 2022 11:56:34 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 11 Mar 2022 11:56:34 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 11 Mar 2022 11:56:34 GMT
WORKDIR /app
# Fri, 11 Mar 2022 11:56:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Mar 2022 11:56:34 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7da25b2876b1c935b05d7e6efa3e8cd559d031cf30b246d7659ed438726acd`  
		Last Modified: Tue, 30 Nov 2021 09:03:50 GMT  
		Size: 1.7 MB (1709704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc599114627e3bd98e0204b93b161e03065bf9a228bb02ae202469655f12b8d`  
		Last Modified: Tue, 30 Nov 2021 09:03:48 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927a0b37a45a98d7d74a6d7d1567230eca834fb89417274557de7986d1f39401`  
		Last Modified: Tue, 30 Nov 2021 09:03:48 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e721f6667a5183c40af8377b3c611b535e9f4eaac41ad37954cc557c4d606dfd`  
		Last Modified: Fri, 18 Feb 2022 23:00:29 GMT  
		Size: 11.8 MB (11771990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdbed47885a29ebdc56f05207500027b26f268bdc5d034f8a6ca8fb34afab54`  
		Last Modified: Fri, 18 Feb 2022 23:00:28 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16135939cf41586188ad9ce6d0b22a1c609842cfcc8f7cb07b9e6db2730c2b37`  
		Last Modified: Fri, 11 Mar 2022 11:16:46 GMT  
		Size: 17.7 MB (17687791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb0fc4c5a6959679cb69633cfe546c6bda81fa74e7a34c9745aeb04921189c5`  
		Last Modified: Fri, 11 Mar 2022 11:16:43 GMT  
		Size: 2.3 KB (2301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37886f8b09348b24b4d10650f01acb3b0517e7d2a69a618c4c87bd1b4ba3df4`  
		Last Modified: Fri, 11 Mar 2022 11:16:43 GMT  
		Size: 18.8 KB (18777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b857d06f2e595fd88321d0fc2350c7811cf2c17127d1039997cb866237878e4d`  
		Last Modified: Fri, 11 Mar 2022 11:56:53 GMT  
		Size: 34.7 MB (34651834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f14b3f6c787d8ee1c2dc4cd24bfecab102e42b082163a5d45722d4e5e22780b`  
		Last Modified: Fri, 11 Mar 2022 11:56:47 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b4046f7f3839e25021c21a29bdef616aaecf6fe2efef00cb9e723b07c1fa04`  
		Last Modified: Fri, 11 Mar 2022 11:57:09 GMT  
		Size: 2.8 MB (2829297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c489b0403c80d314e19c8e77d840c36e3273d818af304b6e5f836cadde6ede1a`  
		Last Modified: Fri, 11 Mar 2022 11:57:09 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de1ba27ef7a7d6880190b1c6f003e5e3c60498f72bb0d72cd6b4d47b1c7b3d7`  
		Last Modified: Fri, 11 Mar 2022 11:57:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1` - linux; arm variant v6

```console
$ docker pull composer@sha256:4f21e5bfdaeae572970b3b192b4752da64ef79a71a33c22f6e96045a8f8133c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66556674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b414ae984d30c76134c2d299198808e896dc40b691774436cd02aeb40c460c4c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 03:20:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 03:20:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 03:20:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 03:20:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 03:20:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 03:20:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 03:20:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 03:20:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 03:20:12 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 19:50:06 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 19:50:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 19:50:07 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 19:50:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 19:50:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:16:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 01:16:18 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:16:21 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 01:16:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 01:16:22 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 04:31:45 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 04:31:47 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 04:31:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 04:31:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Mar 2022 04:32:57 GMT
ENV COMPOSER_VERSION=1.10.25
# Fri, 11 Mar 2022 04:33:44 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 11 Mar 2022 04:33:44 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 11 Mar 2022 04:33:45 GMT
WORKDIR /app
# Fri, 11 Mar 2022 04:33:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Mar 2022 04:33:46 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289be6d758ff0faa38d64732e5736031f2250cbf78d1ca4b32abba4accd6a3fa`  
		Last Modified: Tue, 30 Nov 2021 04:29:36 GMT  
		Size: 1.7 MB (1698826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0b442a0f679dba79aa838c408cf49916ca26d27e1252e26f3904d7c5b83d6c`  
		Last Modified: Tue, 30 Nov 2021 04:29:33 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef02b1cade59fbcc24c0ee972dd15d8caa89dda554cdb8aa742de1c6f3d5b7c`  
		Last Modified: Tue, 30 Nov 2021 04:29:33 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452d0467a92abee019a5ea9cdd7cf7b52fb629aa35a045df70339fb93b634760`  
		Last Modified: Fri, 18 Feb 2022 20:43:48 GMT  
		Size: 11.8 MB (11771982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e48b13f55f3236500af7e58ba05199b7acf9a4d62bc99270797ca5f5c1bc88`  
		Last Modified: Fri, 18 Feb 2022 20:43:45 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59c13e75cc1f96edac01b31ca5bf7f47552e1b3662911082d1926896e971fa4`  
		Last Modified: Fri, 11 Mar 2022 03:24:45 GMT  
		Size: 16.0 MB (16031967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0e34d07dc9c018a0df930e952b25876b7c0168a21c1a5a41e366c8103313b7`  
		Last Modified: Fri, 11 Mar 2022 03:24:38 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139e94b314f0a7968bb009c6b624a733bc8b17cde4cc3c5fb98883a957793045`  
		Last Modified: Fri, 11 Mar 2022 03:24:38 GMT  
		Size: 18.6 KB (18571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f789c188a53299f824e7c04be763e79c5b526773d8151b1e07b136bcde02fe78`  
		Last Modified: Fri, 11 Mar 2022 04:34:52 GMT  
		Size: 32.1 MB (32141861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ff5480814d31ae5b439e71effe3a89f8726a82b5f9531c24575c309aa5b802`  
		Last Modified: Fri, 11 Mar 2022 04:34:29 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92facbb1a4957cddaf566da64011ee52598071381194f8d44fe47bf2bbb50b3f`  
		Last Modified: Fri, 11 Mar 2022 04:35:14 GMT  
		Size: 2.3 MB (2256927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:630af3723d7e592eb6f804394e4d04c3549f182d275c09b132d9e1fdc634fb04`  
		Last Modified: Fri, 11 Mar 2022 04:35:12 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8636502aafbd0a60125e8497c7915d9d0bf759212f1c3a4cbc2fbbd1cf3430a`  
		Last Modified: Fri, 11 Mar 2022 04:35:12 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1` - linux; arm variant v7

```console
$ docker pull composer@sha256:7f86fa49eb9a1ba91d5a80e285931bd28ef593c1eb45834bdcd722941cdc0b01
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63906348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e207c06378f1c1096eaa51b835135b41112bb69f9f55c534aace74e778e26e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 05:27:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 05:27:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 05:27:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 05:27:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 05:27:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 05:27:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:27:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:27:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 05:27:21 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:43:09 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:43:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:43:09 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:43:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:43:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 02:43:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 02:43:15 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 02:43:17 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 02:43:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 02:43:18 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 12:13:42 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 12:13:44 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 12:13:44 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 12:13:45 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Mar 2022 12:14:45 GMT
ENV COMPOSER_VERSION=1.10.25
# Fri, 11 Mar 2022 12:15:30 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 11 Mar 2022 12:15:30 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 11 Mar 2022 12:15:30 GMT
WORKDIR /app
# Fri, 11 Mar 2022 12:15:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Mar 2022 12:15:31 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484fe107211badcebee7c4211e5ed91c7e5212cdd6d7edbb292a63ec60572bdd`  
		Last Modified: Tue, 30 Nov 2021 06:57:00 GMT  
		Size: 1.6 MB (1568802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93353d0a7113f37ba224b9ee296684e49f27c1c9440d3a3c5d310749213da97f`  
		Last Modified: Tue, 30 Nov 2021 06:56:59 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137db50a58959a68358c190d2a143088b82ab25d97cb889876fbc0728e446058`  
		Last Modified: Tue, 30 Nov 2021 06:57:00 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122d3a581986e22d7617f0ef2245bcb64b2a87ebcfe58b7b6d143561ce0cc8b2`  
		Last Modified: Fri, 18 Feb 2022 22:37:27 GMT  
		Size: 11.8 MB (11771980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc11ce0d4bdb5fcdda54f9da2a0eb1e4751b77e354a0dcdb827def3ff59f9f6`  
		Last Modified: Fri, 18 Feb 2022 22:37:24 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1951768145bebb84adba11b1ccd77c8d3802784df6c56f3ae141c103ac114c35`  
		Last Modified: Fri, 11 Mar 2022 07:38:53 GMT  
		Size: 15.0 MB (15034421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fdf84bb546f4d33ce7fff41672c1959df0ef457af702871c4ca3e4d585d8d87`  
		Last Modified: Fri, 11 Mar 2022 07:38:43 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164a1f0370d8b9c1f9c97a1a5aa3993986015fbe893874af94b911c5b8b06870`  
		Last Modified: Fri, 11 Mar 2022 07:38:43 GMT  
		Size: 18.6 KB (18569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b3d0ba165529b585fb1997f3fbc2d14dac5ccff866a44bff4b22578e6bd6aa`  
		Last Modified: Fri, 11 Mar 2022 12:16:34 GMT  
		Size: 30.5 MB (30471948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8e62f6bd555ee3d4b4ee22e2664dad7d5e0053556763e911676f59e8430be7`  
		Last Modified: Fri, 11 Mar 2022 12:16:14 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c31ec95994c481b8e8234264f74c04ac2a1ae130fda79d717e6797b68dc9d42`  
		Last Modified: Fri, 11 Mar 2022 12:16:55 GMT  
		Size: 2.6 MB (2600745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a341e1503d516c3e9c88b320a6ad29b6d9ece9e1ded7c02125e3702da21e64`  
		Last Modified: Fri, 11 Mar 2022 12:16:53 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33fb31ff07d44445af86b634a803d7ccc186bbe99f33dfdd48b3fd0078239eb5`  
		Last Modified: Fri, 11 Mar 2022 12:16:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:83c56285ff8eb518f9ab266bf271c7619276f973571aef19bccaa312cb08aa37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69583769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945191b7db8b3627f4a6e892617cf21b3e486fe70a945c5e344031c4960c6fd9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 02:50:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 02:50:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 02:50:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 02:50:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 02:50:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 02:50:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 02:50:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 02:50:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 02:50:54 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:18:23 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:18:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:18:25 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:19:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:19:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:18:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 03:18:52 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:18:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 03:18:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 03:18:55 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 10:35:18 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 10:35:18 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 10:35:19 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 10:35:20 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Mar 2022 10:35:57 GMT
ENV COMPOSER_VERSION=1.10.25
# Fri, 11 Mar 2022 10:36:18 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 11 Mar 2022 10:36:20 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 11 Mar 2022 10:36:20 GMT
WORKDIR /app
# Fri, 11 Mar 2022 10:36:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Mar 2022 10:36:22 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd720d9f53003155e4cfe3f1974fc0e4d74a622ea8c61cfccb00ee8b842c09b6`  
		Last Modified: Tue, 30 Nov 2021 03:59:34 GMT  
		Size: 1.7 MB (1708308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680efee530f3c970c3140b358d3dc583ded463f9adbadb737ca64c765cf997ee`  
		Last Modified: Tue, 30 Nov 2021 03:59:33 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643d01251bc949843dbd734a37e7cf28a01af4ea11443738b8b92d17e1e438de`  
		Last Modified: Tue, 30 Nov 2021 03:59:33 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbd0dff840aec18863650b4a5db905ad8e50c878c0d1f6c4c1634d0a4743ae4`  
		Last Modified: Fri, 18 Feb 2022 21:39:27 GMT  
		Size: 11.8 MB (11771755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6104c5a569f57122fffc091a5376f51c0848737cec9feaa9a82531e6c2da43`  
		Last Modified: Fri, 18 Feb 2022 21:39:26 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf59a8a0ffa368fdd033e0104d93a4b4913881c7f6bd86aaef35c541233a018`  
		Last Modified: Fri, 11 Mar 2022 09:48:26 GMT  
		Size: 17.5 MB (17546174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef08d98d3666360bd8cbe19dcb81037d75a8aca59ebcfd386287fccb05cc9aab`  
		Last Modified: Fri, 11 Mar 2022 09:48:22 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e7653a3be11ae60976b3f56b5349443e6c458f125a944ba93d234548413851`  
		Last Modified: Fri, 11 Mar 2022 09:48:22 GMT  
		Size: 18.5 KB (18487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f017cf68653c976946e3d237367accaca773a59fbfae998075a1dfc4d6703911`  
		Last Modified: Fri, 11 Mar 2022 10:36:49 GMT  
		Size: 33.0 MB (33001745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0c25578ca0b4f7b253053edcefd8aaea561ada9282ced6617c66749e3cbd4e`  
		Last Modified: Fri, 11 Mar 2022 10:36:44 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b586eafff52325e9f39efd9c19486cebb9dc9a3a4d20ee17e1ebd2a3820554ce`  
		Last Modified: Fri, 11 Mar 2022 10:37:08 GMT  
		Size: 2.8 MB (2816853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f2268389370e1433a3d445a5918610023d90a1443b7b8d141e73043e4ddae5`  
		Last Modified: Fri, 11 Mar 2022 10:37:08 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc81d75e6529449ebc2b76bdd907dde02366699d58f42a7149d183d22566ee3`  
		Last Modified: Fri, 11 Mar 2022 10:37:08 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1` - linux; 386

```console
$ docker pull composer@sha256:c87643b2205e7c8a45ebce904baf743f9dfd9f544e6d7e096c595420da670b71
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52868730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b302ca8a5899d1241f86c49731d5232d49169209f2d47604a6b494505b3dcd4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:53:48 GMT
ADD file:b9a17131c440053f2f67e127b447645f25fd7de2d6caca42f569cafab6291855 in / 
# Wed, 24 Nov 2021 20:53:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 05:59:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 05:59:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 05:59:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 05:59:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 05:59:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 05:59:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:59:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:59:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 05:59:11 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:49:36 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:49:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:49:37 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:50:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:50:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:42:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 04:42:32 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:42:33 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 04:42:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 04:42:33 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 14:29:16 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 14:29:16 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 14:29:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 14:29:17 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Mar 2022 14:29:50 GMT
ENV COMPOSER_VERSION=1.10.25
# Fri, 11 Mar 2022 14:30:12 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 11 Mar 2022 14:30:12 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 11 Mar 2022 14:30:13 GMT
WORKDIR /app
# Fri, 11 Mar 2022 14:30:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Mar 2022 14:30:13 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:e6889e0d66307a4b916fc844f2dcbc03245c63bc4189dd3e88126d9dcf2f9231`  
		Last Modified: Wed, 24 Nov 2021 20:54:48 GMT  
		Size: 2.8 MB (2827117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d6acd3b6e4278a7b3ef37d3525813808468237f086215b68594b244dbd1fba`  
		Last Modified: Tue, 30 Nov 2021 08:26:15 GMT  
		Size: 1.8 MB (1810453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc53af545b93519336bed63b8765255ac8280e27c8e3a17c336f92526b3f290`  
		Last Modified: Tue, 30 Nov 2021 08:26:14 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d406b6d62c3d67bec5f638d47d2b1b49c0ee41d80a791a1b90eaec776cf4fd`  
		Last Modified: Tue, 30 Nov 2021 08:26:13 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09947cbaa6ea94c09911bac9f42ad67e560858bcf313330c30a51d4e047debcc`  
		Last Modified: Fri, 18 Feb 2022 23:36:11 GMT  
		Size: 11.8 MB (11771980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418d95d8e7f7c7a6bca99de67f7268f3c2bd9f90ac05ded2056aca5dcfcf42f3`  
		Last Modified: Fri, 18 Feb 2022 23:36:09 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe93a8e5de6a995b340c34f3b0c9926bbfb8314a31f31edd9aeecf49431cee4`  
		Last Modified: Fri, 11 Mar 2022 11:59:00 GMT  
		Size: 18.0 MB (18045807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98142bd532dfb18d7144d8a1bf1c7a641e931c169b4d2e1863e890a7f1b8e42d`  
		Last Modified: Fri, 11 Mar 2022 11:58:55 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e86e6cc1686366ee83df3ef2c5f3a0405af922746fd6d7ad4fd411ce9a77da`  
		Last Modified: Fri, 11 Mar 2022 11:58:55 GMT  
		Size: 18.8 KB (18773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765d3379030a7d7c59596ec428386624a93faadc763120bcb58cd721522baa8e`  
		Last Modified: Fri, 11 Mar 2022 14:30:44 GMT  
		Size: 15.6 MB (15590818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efdf8175c4916376f3518dfce254d9d6655bbb9cdf549acdfc253419b6d70b0`  
		Last Modified: Fri, 11 Mar 2022 14:30:41 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4713d46f2407dd82fc1fc609c764d58fe738b0f82438ea110f5993116bd1af0`  
		Last Modified: Fri, 11 Mar 2022 14:31:05 GMT  
		Size: 2.8 MB (2798659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76b28c39a135ef18815bf9b6834143d7e2f9e8242f3eca4f4a8ae205e29721b`  
		Last Modified: Fri, 11 Mar 2022 14:31:04 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0e1e6491f2a4eac77a949f9b5f97e615b4075c0cd7cfc468d5c93f4166477c`  
		Last Modified: Fri, 11 Mar 2022 14:31:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1` - linux; ppc64le

```console
$ docker pull composer@sha256:238ccc50cecc665e0612428fd6335f2a5c87a2076bbe5c6cfb11ba837b89c009
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71644520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789d56056d1f6cc38eb4a7ace9e640c1f3df7b92f355d395bbe623a37c183e4c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:20:16 GMT
ADD file:57115dca2eb707f46b6301e75174e6aa316fb02ac28643b91429b75be51bd8c8 in / 
# Wed, 24 Nov 2021 20:20:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 06:02:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 06:03:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 06:03:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 06:03:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 06:03:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 06:03:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 06:03:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 06:04:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 06:04:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:19:05 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:19:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:19:10 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:19:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:19:44 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:41:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 03:41:38 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:41:46 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 03:41:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 03:41:52 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 10:53:22 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 10:53:41 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 10:53:45 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 10:53:51 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Mar 2022 10:55:39 GMT
ENV COMPOSER_VERSION=1.10.25
# Fri, 11 Mar 2022 10:56:33 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 11 Mar 2022 10:56:37 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 11 Mar 2022 10:56:44 GMT
WORKDIR /app
# Fri, 11 Mar 2022 10:56:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Mar 2022 10:56:51 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:159b5dcb1717c815c76ff5ea1db730e18e8609c9090238e43282856db9e71f47`  
		Last Modified: Wed, 24 Nov 2021 20:21:14 GMT  
		Size: 2.8 MB (2814780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603762061fb50079a4b6eb13347fd9a84cc1456d628cf781c89924a54bc419c1`  
		Last Modified: Tue, 30 Nov 2021 07:26:39 GMT  
		Size: 1.8 MB (1756276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645c08440cfaddc2735de2e28697acff0bc71db4cc7242494a44f92c94134e32`  
		Last Modified: Tue, 30 Nov 2021 07:26:39 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5de97a9a329d566f48c2edce253e4ccda6f021041e92326728b7499d13c823b`  
		Last Modified: Tue, 30 Nov 2021 07:26:39 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663cc53ab2317558b9afc14f317845ab71678d9014ef8f4b455b76a1f5ad13b4`  
		Last Modified: Fri, 18 Feb 2022 22:26:29 GMT  
		Size: 11.8 MB (11771981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01091fd3e45df20547a10229a30b96d8cf5998dafc5a5815700834ea2a1cca9`  
		Last Modified: Fri, 18 Feb 2022 22:26:27 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7c08f08c396228976e471a184d4a94d00e1ffcdd366553305de7177eec3bec`  
		Last Modified: Fri, 11 Mar 2022 09:52:14 GMT  
		Size: 18.4 MB (18353518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e767c5a126e3cb62dc8dfdb265ab1b5cfefbbb4955aa58b9ca20fd4e9a3cb5d`  
		Last Modified: Fri, 11 Mar 2022 09:52:10 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a598088569767a94973057cabf1fdeb7dee736eeb4881b2a7e6f18a0c0f2807`  
		Last Modified: Fri, 11 Mar 2022 09:52:10 GMT  
		Size: 18.6 KB (18564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865b388f98b32bac5bade9ff004270a55a0e68d686465a2830ad43a6e6c1e699`  
		Last Modified: Fri, 11 Mar 2022 10:57:32 GMT  
		Size: 33.9 MB (33902882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f226452b0c1667229ee85c065083d8341b4750406d4809c2849e36b27a77a35`  
		Last Modified: Fri, 11 Mar 2022 10:57:25 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1198f7cd9f3fe5c1e629d958a382c57eee946258b4563d653251eed3813d38`  
		Last Modified: Fri, 11 Mar 2022 10:57:54 GMT  
		Size: 3.0 MB (3021400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:294680a6356c69fd99f1419f5db70253c57416d30a27e27ca0720953e9b5fe3e`  
		Last Modified: Fri, 11 Mar 2022 10:57:53 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:869dd640d99702d97db4911680b749e57f83b781c12a540838645ac8724eff83`  
		Last Modified: Fri, 11 Mar 2022 10:57:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1` - linux; s390x

```console
$ docker pull composer@sha256:913e7c6f8a45fc70cbe004f26f2ed97362580042879089c88268ca56424bb38d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69771109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:336da1761462228de7b8ee649fb4e27c3b1d0ea178469480c298aa0f87a53143`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:41:23 GMT
ADD file:cd24c711a2ef431b3ff94f9a02bfc42f159bc60de1d0eceecafea4e8af02441d in / 
# Wed, 24 Nov 2021 20:41:23 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:50:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 04:50:01 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 04:50:02 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 04:50:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 04:50:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 04:50:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 04:50:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 04:50:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 04:50:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:08:01 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:08:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:08:02 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:09:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:09:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:35:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 01:35:50 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:35:51 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 01:35:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 01:35:52 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 05:02:45 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 05:02:47 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 05:02:47 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 05:02:47 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Mar 2022 05:03:10 GMT
ENV COMPOSER_VERSION=1.10.25
# Fri, 11 Mar 2022 05:03:23 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 11 Mar 2022 05:03:23 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 11 Mar 2022 05:03:23 GMT
WORKDIR /app
# Fri, 11 Mar 2022 05:03:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Mar 2022 05:03:23 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d6baca485f3d0f7c77221be60fbef5db014a5ef9d8f53db4a310c947c690d189`  
		Last Modified: Wed, 24 Nov 2021 20:42:15 GMT  
		Size: 2.6 MB (2605944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079fbafa3afc04920b17b503e5d173a44e68fa743eddc7a0eca5e81c7572b8a2`  
		Last Modified: Tue, 30 Nov 2021 08:33:50 GMT  
		Size: 1.8 MB (1771410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ea1ee8ecbda317521ca15da3d8e45a369d74d9b70a0070ebd705cb9aaf88a2`  
		Last Modified: Tue, 30 Nov 2021 08:33:49 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abad577e66a4ab93646ed4a4aefb0579d577932add0d28121e5aece37cfc08dd`  
		Last Modified: Tue, 30 Nov 2021 08:33:49 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac62d72c92f8b14f9b5873207ef984e63eff6fec607db9d4330d9c8129c2925`  
		Last Modified: Fri, 18 Feb 2022 21:13:54 GMT  
		Size: 11.8 MB (11771995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074272c815254eeab42d6bbeac5cb89869166aa437afdace2d9b24a9aa028c4f`  
		Last Modified: Fri, 18 Feb 2022 21:13:53 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a400f11df7f6a7553c85e98fc344489885d2289da563949d00c5280b943f9d0b`  
		Last Modified: Fri, 11 Mar 2022 04:03:48 GMT  
		Size: 16.4 MB (16381073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560e4e59acf6107ca6529fb1d607beb5fe7518052fc9e159c1a89111422d0ed9`  
		Last Modified: Fri, 11 Mar 2022 04:03:46 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93e829bfc7fd232613ba9a365a7a92259718f51bf2ce8df42cf435a15dcc38f`  
		Last Modified: Fri, 11 Mar 2022 04:03:46 GMT  
		Size: 18.6 KB (18598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86bb1285cae11648274513dd55a891e1ca7f14ee80070d95daeae0521db77da`  
		Last Modified: Fri, 11 Mar 2022 05:03:53 GMT  
		Size: 34.9 MB (34887464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e94752314a819cf5f190758a33d2f4d2a3dbde007de6249f275621e5ef423f8`  
		Last Modified: Fri, 11 Mar 2022 05:03:49 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e919933fb117495f8857498e48f4f793b4898536ce4a7cf910549dc1bc0e84`  
		Last Modified: Fri, 11 Mar 2022 05:04:05 GMT  
		Size: 2.3 MB (2329505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89e5c36618de7ab07d355c88e4f4d080e93a9f7db136e5aaedcf301b2563ad0`  
		Last Modified: Fri, 11 Mar 2022 05:04:05 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f621ebfc15dd872a14b0a4f35eb2671f18510efd54fb1361d97fd21da1d979e3`  
		Last Modified: Fri, 11 Mar 2022 05:04:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `composer:1.10`

```console
$ docker pull composer@sha256:859e2699e66e8111ed3da99a5243c655320ef720b35cb1d4f4a1ac7eab02fbc3
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

### `composer:1.10` - linux; amd64

```console
$ docker pull composer@sha256:f5638759bd7404ac2476beb05944f8e8d034420637d91d701257c3ca70d9d866
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71492923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1e7fca3c4e94ca9e65eaeb1002bf92b77423c74b21949fbb3ed1d007a8f63e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 07:06:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 07:06:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 07:06:04 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 07:06:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 07:06:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 07:06:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 07:06:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 07:06:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 07:06:06 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:16:49 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:16:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:16:50 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:17:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:17:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:06:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 04:06:01 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:06:03 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 04:06:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 04:06:03 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 11:55:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 11:55:50 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 11:55:50 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 11:55:50 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Mar 2022 11:56:14 GMT
ENV COMPOSER_VERSION=1.10.25
# Fri, 11 Mar 2022 11:56:34 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 11 Mar 2022 11:56:34 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 11 Mar 2022 11:56:34 GMT
WORKDIR /app
# Fri, 11 Mar 2022 11:56:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Mar 2022 11:56:34 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7da25b2876b1c935b05d7e6efa3e8cd559d031cf30b246d7659ed438726acd`  
		Last Modified: Tue, 30 Nov 2021 09:03:50 GMT  
		Size: 1.7 MB (1709704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc599114627e3bd98e0204b93b161e03065bf9a228bb02ae202469655f12b8d`  
		Last Modified: Tue, 30 Nov 2021 09:03:48 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927a0b37a45a98d7d74a6d7d1567230eca834fb89417274557de7986d1f39401`  
		Last Modified: Tue, 30 Nov 2021 09:03:48 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e721f6667a5183c40af8377b3c611b535e9f4eaac41ad37954cc557c4d606dfd`  
		Last Modified: Fri, 18 Feb 2022 23:00:29 GMT  
		Size: 11.8 MB (11771990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdbed47885a29ebdc56f05207500027b26f268bdc5d034f8a6ca8fb34afab54`  
		Last Modified: Fri, 18 Feb 2022 23:00:28 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16135939cf41586188ad9ce6d0b22a1c609842cfcc8f7cb07b9e6db2730c2b37`  
		Last Modified: Fri, 11 Mar 2022 11:16:46 GMT  
		Size: 17.7 MB (17687791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb0fc4c5a6959679cb69633cfe546c6bda81fa74e7a34c9745aeb04921189c5`  
		Last Modified: Fri, 11 Mar 2022 11:16:43 GMT  
		Size: 2.3 KB (2301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37886f8b09348b24b4d10650f01acb3b0517e7d2a69a618c4c87bd1b4ba3df4`  
		Last Modified: Fri, 11 Mar 2022 11:16:43 GMT  
		Size: 18.8 KB (18777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b857d06f2e595fd88321d0fc2350c7811cf2c17127d1039997cb866237878e4d`  
		Last Modified: Fri, 11 Mar 2022 11:56:53 GMT  
		Size: 34.7 MB (34651834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f14b3f6c787d8ee1c2dc4cd24bfecab102e42b082163a5d45722d4e5e22780b`  
		Last Modified: Fri, 11 Mar 2022 11:56:47 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b4046f7f3839e25021c21a29bdef616aaecf6fe2efef00cb9e723b07c1fa04`  
		Last Modified: Fri, 11 Mar 2022 11:57:09 GMT  
		Size: 2.8 MB (2829297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c489b0403c80d314e19c8e77d840c36e3273d818af304b6e5f836cadde6ede1a`  
		Last Modified: Fri, 11 Mar 2022 11:57:09 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de1ba27ef7a7d6880190b1c6f003e5e3c60498f72bb0d72cd6b4d47b1c7b3d7`  
		Last Modified: Fri, 11 Mar 2022 11:57:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.10` - linux; arm variant v6

```console
$ docker pull composer@sha256:4f21e5bfdaeae572970b3b192b4752da64ef79a71a33c22f6e96045a8f8133c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66556674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b414ae984d30c76134c2d299198808e896dc40b691774436cd02aeb40c460c4c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 03:20:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 03:20:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 03:20:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 03:20:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 03:20:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 03:20:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 03:20:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 03:20:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 03:20:12 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 19:50:06 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 19:50:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 19:50:07 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 19:50:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 19:50:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:16:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 01:16:18 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:16:21 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 01:16:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 01:16:22 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 04:31:45 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 04:31:47 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 04:31:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 04:31:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Mar 2022 04:32:57 GMT
ENV COMPOSER_VERSION=1.10.25
# Fri, 11 Mar 2022 04:33:44 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 11 Mar 2022 04:33:44 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 11 Mar 2022 04:33:45 GMT
WORKDIR /app
# Fri, 11 Mar 2022 04:33:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Mar 2022 04:33:46 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289be6d758ff0faa38d64732e5736031f2250cbf78d1ca4b32abba4accd6a3fa`  
		Last Modified: Tue, 30 Nov 2021 04:29:36 GMT  
		Size: 1.7 MB (1698826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0b442a0f679dba79aa838c408cf49916ca26d27e1252e26f3904d7c5b83d6c`  
		Last Modified: Tue, 30 Nov 2021 04:29:33 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef02b1cade59fbcc24c0ee972dd15d8caa89dda554cdb8aa742de1c6f3d5b7c`  
		Last Modified: Tue, 30 Nov 2021 04:29:33 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452d0467a92abee019a5ea9cdd7cf7b52fb629aa35a045df70339fb93b634760`  
		Last Modified: Fri, 18 Feb 2022 20:43:48 GMT  
		Size: 11.8 MB (11771982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e48b13f55f3236500af7e58ba05199b7acf9a4d62bc99270797ca5f5c1bc88`  
		Last Modified: Fri, 18 Feb 2022 20:43:45 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59c13e75cc1f96edac01b31ca5bf7f47552e1b3662911082d1926896e971fa4`  
		Last Modified: Fri, 11 Mar 2022 03:24:45 GMT  
		Size: 16.0 MB (16031967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0e34d07dc9c018a0df930e952b25876b7c0168a21c1a5a41e366c8103313b7`  
		Last Modified: Fri, 11 Mar 2022 03:24:38 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139e94b314f0a7968bb009c6b624a733bc8b17cde4cc3c5fb98883a957793045`  
		Last Modified: Fri, 11 Mar 2022 03:24:38 GMT  
		Size: 18.6 KB (18571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f789c188a53299f824e7c04be763e79c5b526773d8151b1e07b136bcde02fe78`  
		Last Modified: Fri, 11 Mar 2022 04:34:52 GMT  
		Size: 32.1 MB (32141861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ff5480814d31ae5b439e71effe3a89f8726a82b5f9531c24575c309aa5b802`  
		Last Modified: Fri, 11 Mar 2022 04:34:29 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92facbb1a4957cddaf566da64011ee52598071381194f8d44fe47bf2bbb50b3f`  
		Last Modified: Fri, 11 Mar 2022 04:35:14 GMT  
		Size: 2.3 MB (2256927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:630af3723d7e592eb6f804394e4d04c3549f182d275c09b132d9e1fdc634fb04`  
		Last Modified: Fri, 11 Mar 2022 04:35:12 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8636502aafbd0a60125e8497c7915d9d0bf759212f1c3a4cbc2fbbd1cf3430a`  
		Last Modified: Fri, 11 Mar 2022 04:35:12 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.10` - linux; arm variant v7

```console
$ docker pull composer@sha256:7f86fa49eb9a1ba91d5a80e285931bd28ef593c1eb45834bdcd722941cdc0b01
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63906348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e207c06378f1c1096eaa51b835135b41112bb69f9f55c534aace74e778e26e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 05:27:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 05:27:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 05:27:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 05:27:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 05:27:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 05:27:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:27:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:27:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 05:27:21 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:43:09 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:43:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:43:09 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:43:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:43:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 02:43:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 02:43:15 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 02:43:17 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 02:43:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 02:43:18 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 12:13:42 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 12:13:44 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 12:13:44 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 12:13:45 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Mar 2022 12:14:45 GMT
ENV COMPOSER_VERSION=1.10.25
# Fri, 11 Mar 2022 12:15:30 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 11 Mar 2022 12:15:30 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 11 Mar 2022 12:15:30 GMT
WORKDIR /app
# Fri, 11 Mar 2022 12:15:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Mar 2022 12:15:31 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484fe107211badcebee7c4211e5ed91c7e5212cdd6d7edbb292a63ec60572bdd`  
		Last Modified: Tue, 30 Nov 2021 06:57:00 GMT  
		Size: 1.6 MB (1568802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93353d0a7113f37ba224b9ee296684e49f27c1c9440d3a3c5d310749213da97f`  
		Last Modified: Tue, 30 Nov 2021 06:56:59 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137db50a58959a68358c190d2a143088b82ab25d97cb889876fbc0728e446058`  
		Last Modified: Tue, 30 Nov 2021 06:57:00 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122d3a581986e22d7617f0ef2245bcb64b2a87ebcfe58b7b6d143561ce0cc8b2`  
		Last Modified: Fri, 18 Feb 2022 22:37:27 GMT  
		Size: 11.8 MB (11771980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc11ce0d4bdb5fcdda54f9da2a0eb1e4751b77e354a0dcdb827def3ff59f9f6`  
		Last Modified: Fri, 18 Feb 2022 22:37:24 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1951768145bebb84adba11b1ccd77c8d3802784df6c56f3ae141c103ac114c35`  
		Last Modified: Fri, 11 Mar 2022 07:38:53 GMT  
		Size: 15.0 MB (15034421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fdf84bb546f4d33ce7fff41672c1959df0ef457af702871c4ca3e4d585d8d87`  
		Last Modified: Fri, 11 Mar 2022 07:38:43 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164a1f0370d8b9c1f9c97a1a5aa3993986015fbe893874af94b911c5b8b06870`  
		Last Modified: Fri, 11 Mar 2022 07:38:43 GMT  
		Size: 18.6 KB (18569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b3d0ba165529b585fb1997f3fbc2d14dac5ccff866a44bff4b22578e6bd6aa`  
		Last Modified: Fri, 11 Mar 2022 12:16:34 GMT  
		Size: 30.5 MB (30471948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8e62f6bd555ee3d4b4ee22e2664dad7d5e0053556763e911676f59e8430be7`  
		Last Modified: Fri, 11 Mar 2022 12:16:14 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c31ec95994c481b8e8234264f74c04ac2a1ae130fda79d717e6797b68dc9d42`  
		Last Modified: Fri, 11 Mar 2022 12:16:55 GMT  
		Size: 2.6 MB (2600745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a341e1503d516c3e9c88b320a6ad29b6d9ece9e1ded7c02125e3702da21e64`  
		Last Modified: Fri, 11 Mar 2022 12:16:53 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33fb31ff07d44445af86b634a803d7ccc186bbe99f33dfdd48b3fd0078239eb5`  
		Last Modified: Fri, 11 Mar 2022 12:16:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.10` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:83c56285ff8eb518f9ab266bf271c7619276f973571aef19bccaa312cb08aa37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69583769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945191b7db8b3627f4a6e892617cf21b3e486fe70a945c5e344031c4960c6fd9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 02:50:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 02:50:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 02:50:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 02:50:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 02:50:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 02:50:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 02:50:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 02:50:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 02:50:54 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:18:23 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:18:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:18:25 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:19:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:19:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:18:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 03:18:52 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:18:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 03:18:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 03:18:55 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 10:35:18 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 10:35:18 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 10:35:19 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 10:35:20 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Mar 2022 10:35:57 GMT
ENV COMPOSER_VERSION=1.10.25
# Fri, 11 Mar 2022 10:36:18 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 11 Mar 2022 10:36:20 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 11 Mar 2022 10:36:20 GMT
WORKDIR /app
# Fri, 11 Mar 2022 10:36:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Mar 2022 10:36:22 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd720d9f53003155e4cfe3f1974fc0e4d74a622ea8c61cfccb00ee8b842c09b6`  
		Last Modified: Tue, 30 Nov 2021 03:59:34 GMT  
		Size: 1.7 MB (1708308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680efee530f3c970c3140b358d3dc583ded463f9adbadb737ca64c765cf997ee`  
		Last Modified: Tue, 30 Nov 2021 03:59:33 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643d01251bc949843dbd734a37e7cf28a01af4ea11443738b8b92d17e1e438de`  
		Last Modified: Tue, 30 Nov 2021 03:59:33 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbd0dff840aec18863650b4a5db905ad8e50c878c0d1f6c4c1634d0a4743ae4`  
		Last Modified: Fri, 18 Feb 2022 21:39:27 GMT  
		Size: 11.8 MB (11771755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6104c5a569f57122fffc091a5376f51c0848737cec9feaa9a82531e6c2da43`  
		Last Modified: Fri, 18 Feb 2022 21:39:26 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf59a8a0ffa368fdd033e0104d93a4b4913881c7f6bd86aaef35c541233a018`  
		Last Modified: Fri, 11 Mar 2022 09:48:26 GMT  
		Size: 17.5 MB (17546174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef08d98d3666360bd8cbe19dcb81037d75a8aca59ebcfd386287fccb05cc9aab`  
		Last Modified: Fri, 11 Mar 2022 09:48:22 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e7653a3be11ae60976b3f56b5349443e6c458f125a944ba93d234548413851`  
		Last Modified: Fri, 11 Mar 2022 09:48:22 GMT  
		Size: 18.5 KB (18487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f017cf68653c976946e3d237367accaca773a59fbfae998075a1dfc4d6703911`  
		Last Modified: Fri, 11 Mar 2022 10:36:49 GMT  
		Size: 33.0 MB (33001745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0c25578ca0b4f7b253053edcefd8aaea561ada9282ced6617c66749e3cbd4e`  
		Last Modified: Fri, 11 Mar 2022 10:36:44 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b586eafff52325e9f39efd9c19486cebb9dc9a3a4d20ee17e1ebd2a3820554ce`  
		Last Modified: Fri, 11 Mar 2022 10:37:08 GMT  
		Size: 2.8 MB (2816853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f2268389370e1433a3d445a5918610023d90a1443b7b8d141e73043e4ddae5`  
		Last Modified: Fri, 11 Mar 2022 10:37:08 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc81d75e6529449ebc2b76bdd907dde02366699d58f42a7149d183d22566ee3`  
		Last Modified: Fri, 11 Mar 2022 10:37:08 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.10` - linux; 386

```console
$ docker pull composer@sha256:c87643b2205e7c8a45ebce904baf743f9dfd9f544e6d7e096c595420da670b71
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52868730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b302ca8a5899d1241f86c49731d5232d49169209f2d47604a6b494505b3dcd4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:53:48 GMT
ADD file:b9a17131c440053f2f67e127b447645f25fd7de2d6caca42f569cafab6291855 in / 
# Wed, 24 Nov 2021 20:53:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 05:59:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 05:59:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 05:59:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 05:59:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 05:59:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 05:59:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:59:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:59:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 05:59:11 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:49:36 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:49:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:49:37 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:50:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:50:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:42:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 04:42:32 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:42:33 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 04:42:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 04:42:33 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 14:29:16 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 14:29:16 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 14:29:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 14:29:17 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Mar 2022 14:29:50 GMT
ENV COMPOSER_VERSION=1.10.25
# Fri, 11 Mar 2022 14:30:12 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 11 Mar 2022 14:30:12 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 11 Mar 2022 14:30:13 GMT
WORKDIR /app
# Fri, 11 Mar 2022 14:30:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Mar 2022 14:30:13 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:e6889e0d66307a4b916fc844f2dcbc03245c63bc4189dd3e88126d9dcf2f9231`  
		Last Modified: Wed, 24 Nov 2021 20:54:48 GMT  
		Size: 2.8 MB (2827117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d6acd3b6e4278a7b3ef37d3525813808468237f086215b68594b244dbd1fba`  
		Last Modified: Tue, 30 Nov 2021 08:26:15 GMT  
		Size: 1.8 MB (1810453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc53af545b93519336bed63b8765255ac8280e27c8e3a17c336f92526b3f290`  
		Last Modified: Tue, 30 Nov 2021 08:26:14 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d406b6d62c3d67bec5f638d47d2b1b49c0ee41d80a791a1b90eaec776cf4fd`  
		Last Modified: Tue, 30 Nov 2021 08:26:13 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09947cbaa6ea94c09911bac9f42ad67e560858bcf313330c30a51d4e047debcc`  
		Last Modified: Fri, 18 Feb 2022 23:36:11 GMT  
		Size: 11.8 MB (11771980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418d95d8e7f7c7a6bca99de67f7268f3c2bd9f90ac05ded2056aca5dcfcf42f3`  
		Last Modified: Fri, 18 Feb 2022 23:36:09 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe93a8e5de6a995b340c34f3b0c9926bbfb8314a31f31edd9aeecf49431cee4`  
		Last Modified: Fri, 11 Mar 2022 11:59:00 GMT  
		Size: 18.0 MB (18045807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98142bd532dfb18d7144d8a1bf1c7a641e931c169b4d2e1863e890a7f1b8e42d`  
		Last Modified: Fri, 11 Mar 2022 11:58:55 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e86e6cc1686366ee83df3ef2c5f3a0405af922746fd6d7ad4fd411ce9a77da`  
		Last Modified: Fri, 11 Mar 2022 11:58:55 GMT  
		Size: 18.8 KB (18773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765d3379030a7d7c59596ec428386624a93faadc763120bcb58cd721522baa8e`  
		Last Modified: Fri, 11 Mar 2022 14:30:44 GMT  
		Size: 15.6 MB (15590818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efdf8175c4916376f3518dfce254d9d6655bbb9cdf549acdfc253419b6d70b0`  
		Last Modified: Fri, 11 Mar 2022 14:30:41 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4713d46f2407dd82fc1fc609c764d58fe738b0f82438ea110f5993116bd1af0`  
		Last Modified: Fri, 11 Mar 2022 14:31:05 GMT  
		Size: 2.8 MB (2798659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76b28c39a135ef18815bf9b6834143d7e2f9e8242f3eca4f4a8ae205e29721b`  
		Last Modified: Fri, 11 Mar 2022 14:31:04 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0e1e6491f2a4eac77a949f9b5f97e615b4075c0cd7cfc468d5c93f4166477c`  
		Last Modified: Fri, 11 Mar 2022 14:31:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.10` - linux; ppc64le

```console
$ docker pull composer@sha256:238ccc50cecc665e0612428fd6335f2a5c87a2076bbe5c6cfb11ba837b89c009
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71644520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789d56056d1f6cc38eb4a7ace9e640c1f3df7b92f355d395bbe623a37c183e4c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:20:16 GMT
ADD file:57115dca2eb707f46b6301e75174e6aa316fb02ac28643b91429b75be51bd8c8 in / 
# Wed, 24 Nov 2021 20:20:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 06:02:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 06:03:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 06:03:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 06:03:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 06:03:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 06:03:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 06:03:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 06:04:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 06:04:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:19:05 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:19:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:19:10 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:19:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:19:44 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:41:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 03:41:38 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:41:46 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 03:41:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 03:41:52 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 10:53:22 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 10:53:41 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 10:53:45 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 10:53:51 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Mar 2022 10:55:39 GMT
ENV COMPOSER_VERSION=1.10.25
# Fri, 11 Mar 2022 10:56:33 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 11 Mar 2022 10:56:37 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 11 Mar 2022 10:56:44 GMT
WORKDIR /app
# Fri, 11 Mar 2022 10:56:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Mar 2022 10:56:51 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:159b5dcb1717c815c76ff5ea1db730e18e8609c9090238e43282856db9e71f47`  
		Last Modified: Wed, 24 Nov 2021 20:21:14 GMT  
		Size: 2.8 MB (2814780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603762061fb50079a4b6eb13347fd9a84cc1456d628cf781c89924a54bc419c1`  
		Last Modified: Tue, 30 Nov 2021 07:26:39 GMT  
		Size: 1.8 MB (1756276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645c08440cfaddc2735de2e28697acff0bc71db4cc7242494a44f92c94134e32`  
		Last Modified: Tue, 30 Nov 2021 07:26:39 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5de97a9a329d566f48c2edce253e4ccda6f021041e92326728b7499d13c823b`  
		Last Modified: Tue, 30 Nov 2021 07:26:39 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663cc53ab2317558b9afc14f317845ab71678d9014ef8f4b455b76a1f5ad13b4`  
		Last Modified: Fri, 18 Feb 2022 22:26:29 GMT  
		Size: 11.8 MB (11771981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01091fd3e45df20547a10229a30b96d8cf5998dafc5a5815700834ea2a1cca9`  
		Last Modified: Fri, 18 Feb 2022 22:26:27 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7c08f08c396228976e471a184d4a94d00e1ffcdd366553305de7177eec3bec`  
		Last Modified: Fri, 11 Mar 2022 09:52:14 GMT  
		Size: 18.4 MB (18353518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e767c5a126e3cb62dc8dfdb265ab1b5cfefbbb4955aa58b9ca20fd4e9a3cb5d`  
		Last Modified: Fri, 11 Mar 2022 09:52:10 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a598088569767a94973057cabf1fdeb7dee736eeb4881b2a7e6f18a0c0f2807`  
		Last Modified: Fri, 11 Mar 2022 09:52:10 GMT  
		Size: 18.6 KB (18564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865b388f98b32bac5bade9ff004270a55a0e68d686465a2830ad43a6e6c1e699`  
		Last Modified: Fri, 11 Mar 2022 10:57:32 GMT  
		Size: 33.9 MB (33902882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f226452b0c1667229ee85c065083d8341b4750406d4809c2849e36b27a77a35`  
		Last Modified: Fri, 11 Mar 2022 10:57:25 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1198f7cd9f3fe5c1e629d958a382c57eee946258b4563d653251eed3813d38`  
		Last Modified: Fri, 11 Mar 2022 10:57:54 GMT  
		Size: 3.0 MB (3021400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:294680a6356c69fd99f1419f5db70253c57416d30a27e27ca0720953e9b5fe3e`  
		Last Modified: Fri, 11 Mar 2022 10:57:53 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:869dd640d99702d97db4911680b749e57f83b781c12a540838645ac8724eff83`  
		Last Modified: Fri, 11 Mar 2022 10:57:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.10` - linux; s390x

```console
$ docker pull composer@sha256:913e7c6f8a45fc70cbe004f26f2ed97362580042879089c88268ca56424bb38d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69771109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:336da1761462228de7b8ee649fb4e27c3b1d0ea178469480c298aa0f87a53143`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:41:23 GMT
ADD file:cd24c711a2ef431b3ff94f9a02bfc42f159bc60de1d0eceecafea4e8af02441d in / 
# Wed, 24 Nov 2021 20:41:23 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:50:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 04:50:01 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 04:50:02 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 04:50:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 04:50:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 04:50:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 04:50:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 04:50:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 04:50:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:08:01 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:08:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:08:02 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:09:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:09:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:35:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 01:35:50 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:35:51 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 01:35:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 01:35:52 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 05:02:45 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 05:02:47 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 05:02:47 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 05:02:47 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Mar 2022 05:03:10 GMT
ENV COMPOSER_VERSION=1.10.25
# Fri, 11 Mar 2022 05:03:23 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 11 Mar 2022 05:03:23 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 11 Mar 2022 05:03:23 GMT
WORKDIR /app
# Fri, 11 Mar 2022 05:03:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Mar 2022 05:03:23 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d6baca485f3d0f7c77221be60fbef5db014a5ef9d8f53db4a310c947c690d189`  
		Last Modified: Wed, 24 Nov 2021 20:42:15 GMT  
		Size: 2.6 MB (2605944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079fbafa3afc04920b17b503e5d173a44e68fa743eddc7a0eca5e81c7572b8a2`  
		Last Modified: Tue, 30 Nov 2021 08:33:50 GMT  
		Size: 1.8 MB (1771410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ea1ee8ecbda317521ca15da3d8e45a369d74d9b70a0070ebd705cb9aaf88a2`  
		Last Modified: Tue, 30 Nov 2021 08:33:49 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abad577e66a4ab93646ed4a4aefb0579d577932add0d28121e5aece37cfc08dd`  
		Last Modified: Tue, 30 Nov 2021 08:33:49 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac62d72c92f8b14f9b5873207ef984e63eff6fec607db9d4330d9c8129c2925`  
		Last Modified: Fri, 18 Feb 2022 21:13:54 GMT  
		Size: 11.8 MB (11771995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074272c815254eeab42d6bbeac5cb89869166aa437afdace2d9b24a9aa028c4f`  
		Last Modified: Fri, 18 Feb 2022 21:13:53 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a400f11df7f6a7553c85e98fc344489885d2289da563949d00c5280b943f9d0b`  
		Last Modified: Fri, 11 Mar 2022 04:03:48 GMT  
		Size: 16.4 MB (16381073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560e4e59acf6107ca6529fb1d607beb5fe7518052fc9e159c1a89111422d0ed9`  
		Last Modified: Fri, 11 Mar 2022 04:03:46 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93e829bfc7fd232613ba9a365a7a92259718f51bf2ce8df42cf435a15dcc38f`  
		Last Modified: Fri, 11 Mar 2022 04:03:46 GMT  
		Size: 18.6 KB (18598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86bb1285cae11648274513dd55a891e1ca7f14ee80070d95daeae0521db77da`  
		Last Modified: Fri, 11 Mar 2022 05:03:53 GMT  
		Size: 34.9 MB (34887464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e94752314a819cf5f190758a33d2f4d2a3dbde007de6249f275621e5ef423f8`  
		Last Modified: Fri, 11 Mar 2022 05:03:49 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e919933fb117495f8857498e48f4f793b4898536ce4a7cf910549dc1bc0e84`  
		Last Modified: Fri, 11 Mar 2022 05:04:05 GMT  
		Size: 2.3 MB (2329505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89e5c36618de7ab07d355c88e4f4d080e93a9f7db136e5aaedcf301b2563ad0`  
		Last Modified: Fri, 11 Mar 2022 05:04:05 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f621ebfc15dd872a14b0a4f35eb2671f18510efd54fb1361d97fd21da1d979e3`  
		Last Modified: Fri, 11 Mar 2022 05:04:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `composer:1.10.25`

```console
$ docker pull composer@sha256:859e2699e66e8111ed3da99a5243c655320ef720b35cb1d4f4a1ac7eab02fbc3
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

### `composer:1.10.25` - linux; amd64

```console
$ docker pull composer@sha256:f5638759bd7404ac2476beb05944f8e8d034420637d91d701257c3ca70d9d866
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71492923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1e7fca3c4e94ca9e65eaeb1002bf92b77423c74b21949fbb3ed1d007a8f63e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 07:06:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 07:06:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 07:06:04 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 07:06:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 07:06:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 07:06:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 07:06:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 07:06:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 07:06:06 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:16:49 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:16:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:16:50 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:17:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:17:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:06:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 04:06:01 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:06:03 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 04:06:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 04:06:03 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 11:55:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 11:55:50 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 11:55:50 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 11:55:50 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Mar 2022 11:56:14 GMT
ENV COMPOSER_VERSION=1.10.25
# Fri, 11 Mar 2022 11:56:34 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 11 Mar 2022 11:56:34 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 11 Mar 2022 11:56:34 GMT
WORKDIR /app
# Fri, 11 Mar 2022 11:56:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Mar 2022 11:56:34 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7da25b2876b1c935b05d7e6efa3e8cd559d031cf30b246d7659ed438726acd`  
		Last Modified: Tue, 30 Nov 2021 09:03:50 GMT  
		Size: 1.7 MB (1709704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc599114627e3bd98e0204b93b161e03065bf9a228bb02ae202469655f12b8d`  
		Last Modified: Tue, 30 Nov 2021 09:03:48 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927a0b37a45a98d7d74a6d7d1567230eca834fb89417274557de7986d1f39401`  
		Last Modified: Tue, 30 Nov 2021 09:03:48 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e721f6667a5183c40af8377b3c611b535e9f4eaac41ad37954cc557c4d606dfd`  
		Last Modified: Fri, 18 Feb 2022 23:00:29 GMT  
		Size: 11.8 MB (11771990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdbed47885a29ebdc56f05207500027b26f268bdc5d034f8a6ca8fb34afab54`  
		Last Modified: Fri, 18 Feb 2022 23:00:28 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16135939cf41586188ad9ce6d0b22a1c609842cfcc8f7cb07b9e6db2730c2b37`  
		Last Modified: Fri, 11 Mar 2022 11:16:46 GMT  
		Size: 17.7 MB (17687791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb0fc4c5a6959679cb69633cfe546c6bda81fa74e7a34c9745aeb04921189c5`  
		Last Modified: Fri, 11 Mar 2022 11:16:43 GMT  
		Size: 2.3 KB (2301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37886f8b09348b24b4d10650f01acb3b0517e7d2a69a618c4c87bd1b4ba3df4`  
		Last Modified: Fri, 11 Mar 2022 11:16:43 GMT  
		Size: 18.8 KB (18777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b857d06f2e595fd88321d0fc2350c7811cf2c17127d1039997cb866237878e4d`  
		Last Modified: Fri, 11 Mar 2022 11:56:53 GMT  
		Size: 34.7 MB (34651834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f14b3f6c787d8ee1c2dc4cd24bfecab102e42b082163a5d45722d4e5e22780b`  
		Last Modified: Fri, 11 Mar 2022 11:56:47 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b4046f7f3839e25021c21a29bdef616aaecf6fe2efef00cb9e723b07c1fa04`  
		Last Modified: Fri, 11 Mar 2022 11:57:09 GMT  
		Size: 2.8 MB (2829297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c489b0403c80d314e19c8e77d840c36e3273d818af304b6e5f836cadde6ede1a`  
		Last Modified: Fri, 11 Mar 2022 11:57:09 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de1ba27ef7a7d6880190b1c6f003e5e3c60498f72bb0d72cd6b4d47b1c7b3d7`  
		Last Modified: Fri, 11 Mar 2022 11:57:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.10.25` - linux; arm variant v6

```console
$ docker pull composer@sha256:4f21e5bfdaeae572970b3b192b4752da64ef79a71a33c22f6e96045a8f8133c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66556674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b414ae984d30c76134c2d299198808e896dc40b691774436cd02aeb40c460c4c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 03:20:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 03:20:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 03:20:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 03:20:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 03:20:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 03:20:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 03:20:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 03:20:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 03:20:12 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 19:50:06 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 19:50:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 19:50:07 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 19:50:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 19:50:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:16:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 01:16:18 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:16:21 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 01:16:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 01:16:22 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 04:31:45 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 04:31:47 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 04:31:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 04:31:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Mar 2022 04:32:57 GMT
ENV COMPOSER_VERSION=1.10.25
# Fri, 11 Mar 2022 04:33:44 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 11 Mar 2022 04:33:44 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 11 Mar 2022 04:33:45 GMT
WORKDIR /app
# Fri, 11 Mar 2022 04:33:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Mar 2022 04:33:46 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289be6d758ff0faa38d64732e5736031f2250cbf78d1ca4b32abba4accd6a3fa`  
		Last Modified: Tue, 30 Nov 2021 04:29:36 GMT  
		Size: 1.7 MB (1698826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0b442a0f679dba79aa838c408cf49916ca26d27e1252e26f3904d7c5b83d6c`  
		Last Modified: Tue, 30 Nov 2021 04:29:33 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef02b1cade59fbcc24c0ee972dd15d8caa89dda554cdb8aa742de1c6f3d5b7c`  
		Last Modified: Tue, 30 Nov 2021 04:29:33 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452d0467a92abee019a5ea9cdd7cf7b52fb629aa35a045df70339fb93b634760`  
		Last Modified: Fri, 18 Feb 2022 20:43:48 GMT  
		Size: 11.8 MB (11771982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e48b13f55f3236500af7e58ba05199b7acf9a4d62bc99270797ca5f5c1bc88`  
		Last Modified: Fri, 18 Feb 2022 20:43:45 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59c13e75cc1f96edac01b31ca5bf7f47552e1b3662911082d1926896e971fa4`  
		Last Modified: Fri, 11 Mar 2022 03:24:45 GMT  
		Size: 16.0 MB (16031967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0e34d07dc9c018a0df930e952b25876b7c0168a21c1a5a41e366c8103313b7`  
		Last Modified: Fri, 11 Mar 2022 03:24:38 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139e94b314f0a7968bb009c6b624a733bc8b17cde4cc3c5fb98883a957793045`  
		Last Modified: Fri, 11 Mar 2022 03:24:38 GMT  
		Size: 18.6 KB (18571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f789c188a53299f824e7c04be763e79c5b526773d8151b1e07b136bcde02fe78`  
		Last Modified: Fri, 11 Mar 2022 04:34:52 GMT  
		Size: 32.1 MB (32141861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ff5480814d31ae5b439e71effe3a89f8726a82b5f9531c24575c309aa5b802`  
		Last Modified: Fri, 11 Mar 2022 04:34:29 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92facbb1a4957cddaf566da64011ee52598071381194f8d44fe47bf2bbb50b3f`  
		Last Modified: Fri, 11 Mar 2022 04:35:14 GMT  
		Size: 2.3 MB (2256927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:630af3723d7e592eb6f804394e4d04c3549f182d275c09b132d9e1fdc634fb04`  
		Last Modified: Fri, 11 Mar 2022 04:35:12 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8636502aafbd0a60125e8497c7915d9d0bf759212f1c3a4cbc2fbbd1cf3430a`  
		Last Modified: Fri, 11 Mar 2022 04:35:12 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.10.25` - linux; arm variant v7

```console
$ docker pull composer@sha256:7f86fa49eb9a1ba91d5a80e285931bd28ef593c1eb45834bdcd722941cdc0b01
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63906348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e207c06378f1c1096eaa51b835135b41112bb69f9f55c534aace74e778e26e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 05:27:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 05:27:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 05:27:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 05:27:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 05:27:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 05:27:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:27:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:27:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 05:27:21 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:43:09 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:43:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:43:09 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:43:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:43:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 02:43:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 02:43:15 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 02:43:17 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 02:43:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 02:43:18 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 12:13:42 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 12:13:44 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 12:13:44 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 12:13:45 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Mar 2022 12:14:45 GMT
ENV COMPOSER_VERSION=1.10.25
# Fri, 11 Mar 2022 12:15:30 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 11 Mar 2022 12:15:30 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 11 Mar 2022 12:15:30 GMT
WORKDIR /app
# Fri, 11 Mar 2022 12:15:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Mar 2022 12:15:31 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484fe107211badcebee7c4211e5ed91c7e5212cdd6d7edbb292a63ec60572bdd`  
		Last Modified: Tue, 30 Nov 2021 06:57:00 GMT  
		Size: 1.6 MB (1568802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93353d0a7113f37ba224b9ee296684e49f27c1c9440d3a3c5d310749213da97f`  
		Last Modified: Tue, 30 Nov 2021 06:56:59 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137db50a58959a68358c190d2a143088b82ab25d97cb889876fbc0728e446058`  
		Last Modified: Tue, 30 Nov 2021 06:57:00 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122d3a581986e22d7617f0ef2245bcb64b2a87ebcfe58b7b6d143561ce0cc8b2`  
		Last Modified: Fri, 18 Feb 2022 22:37:27 GMT  
		Size: 11.8 MB (11771980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc11ce0d4bdb5fcdda54f9da2a0eb1e4751b77e354a0dcdb827def3ff59f9f6`  
		Last Modified: Fri, 18 Feb 2022 22:37:24 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1951768145bebb84adba11b1ccd77c8d3802784df6c56f3ae141c103ac114c35`  
		Last Modified: Fri, 11 Mar 2022 07:38:53 GMT  
		Size: 15.0 MB (15034421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fdf84bb546f4d33ce7fff41672c1959df0ef457af702871c4ca3e4d585d8d87`  
		Last Modified: Fri, 11 Mar 2022 07:38:43 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164a1f0370d8b9c1f9c97a1a5aa3993986015fbe893874af94b911c5b8b06870`  
		Last Modified: Fri, 11 Mar 2022 07:38:43 GMT  
		Size: 18.6 KB (18569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b3d0ba165529b585fb1997f3fbc2d14dac5ccff866a44bff4b22578e6bd6aa`  
		Last Modified: Fri, 11 Mar 2022 12:16:34 GMT  
		Size: 30.5 MB (30471948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8e62f6bd555ee3d4b4ee22e2664dad7d5e0053556763e911676f59e8430be7`  
		Last Modified: Fri, 11 Mar 2022 12:16:14 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c31ec95994c481b8e8234264f74c04ac2a1ae130fda79d717e6797b68dc9d42`  
		Last Modified: Fri, 11 Mar 2022 12:16:55 GMT  
		Size: 2.6 MB (2600745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a341e1503d516c3e9c88b320a6ad29b6d9ece9e1ded7c02125e3702da21e64`  
		Last Modified: Fri, 11 Mar 2022 12:16:53 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33fb31ff07d44445af86b634a803d7ccc186bbe99f33dfdd48b3fd0078239eb5`  
		Last Modified: Fri, 11 Mar 2022 12:16:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.10.25` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:83c56285ff8eb518f9ab266bf271c7619276f973571aef19bccaa312cb08aa37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69583769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945191b7db8b3627f4a6e892617cf21b3e486fe70a945c5e344031c4960c6fd9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 02:50:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 02:50:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 02:50:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 02:50:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 02:50:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 02:50:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 02:50:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 02:50:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 02:50:54 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:18:23 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:18:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:18:25 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:19:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:19:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:18:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 03:18:52 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:18:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 03:18:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 03:18:55 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 10:35:18 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 10:35:18 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 10:35:19 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 10:35:20 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Mar 2022 10:35:57 GMT
ENV COMPOSER_VERSION=1.10.25
# Fri, 11 Mar 2022 10:36:18 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 11 Mar 2022 10:36:20 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 11 Mar 2022 10:36:20 GMT
WORKDIR /app
# Fri, 11 Mar 2022 10:36:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Mar 2022 10:36:22 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd720d9f53003155e4cfe3f1974fc0e4d74a622ea8c61cfccb00ee8b842c09b6`  
		Last Modified: Tue, 30 Nov 2021 03:59:34 GMT  
		Size: 1.7 MB (1708308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680efee530f3c970c3140b358d3dc583ded463f9adbadb737ca64c765cf997ee`  
		Last Modified: Tue, 30 Nov 2021 03:59:33 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643d01251bc949843dbd734a37e7cf28a01af4ea11443738b8b92d17e1e438de`  
		Last Modified: Tue, 30 Nov 2021 03:59:33 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbd0dff840aec18863650b4a5db905ad8e50c878c0d1f6c4c1634d0a4743ae4`  
		Last Modified: Fri, 18 Feb 2022 21:39:27 GMT  
		Size: 11.8 MB (11771755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6104c5a569f57122fffc091a5376f51c0848737cec9feaa9a82531e6c2da43`  
		Last Modified: Fri, 18 Feb 2022 21:39:26 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf59a8a0ffa368fdd033e0104d93a4b4913881c7f6bd86aaef35c541233a018`  
		Last Modified: Fri, 11 Mar 2022 09:48:26 GMT  
		Size: 17.5 MB (17546174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef08d98d3666360bd8cbe19dcb81037d75a8aca59ebcfd386287fccb05cc9aab`  
		Last Modified: Fri, 11 Mar 2022 09:48:22 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e7653a3be11ae60976b3f56b5349443e6c458f125a944ba93d234548413851`  
		Last Modified: Fri, 11 Mar 2022 09:48:22 GMT  
		Size: 18.5 KB (18487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f017cf68653c976946e3d237367accaca773a59fbfae998075a1dfc4d6703911`  
		Last Modified: Fri, 11 Mar 2022 10:36:49 GMT  
		Size: 33.0 MB (33001745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0c25578ca0b4f7b253053edcefd8aaea561ada9282ced6617c66749e3cbd4e`  
		Last Modified: Fri, 11 Mar 2022 10:36:44 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b586eafff52325e9f39efd9c19486cebb9dc9a3a4d20ee17e1ebd2a3820554ce`  
		Last Modified: Fri, 11 Mar 2022 10:37:08 GMT  
		Size: 2.8 MB (2816853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f2268389370e1433a3d445a5918610023d90a1443b7b8d141e73043e4ddae5`  
		Last Modified: Fri, 11 Mar 2022 10:37:08 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc81d75e6529449ebc2b76bdd907dde02366699d58f42a7149d183d22566ee3`  
		Last Modified: Fri, 11 Mar 2022 10:37:08 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.10.25` - linux; 386

```console
$ docker pull composer@sha256:c87643b2205e7c8a45ebce904baf743f9dfd9f544e6d7e096c595420da670b71
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52868730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b302ca8a5899d1241f86c49731d5232d49169209f2d47604a6b494505b3dcd4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:53:48 GMT
ADD file:b9a17131c440053f2f67e127b447645f25fd7de2d6caca42f569cafab6291855 in / 
# Wed, 24 Nov 2021 20:53:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 05:59:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 05:59:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 05:59:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 05:59:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 05:59:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 05:59:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:59:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:59:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 05:59:11 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:49:36 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:49:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:49:37 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:50:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:50:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:42:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 04:42:32 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:42:33 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 04:42:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 04:42:33 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 14:29:16 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 14:29:16 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 14:29:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 14:29:17 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Mar 2022 14:29:50 GMT
ENV COMPOSER_VERSION=1.10.25
# Fri, 11 Mar 2022 14:30:12 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 11 Mar 2022 14:30:12 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 11 Mar 2022 14:30:13 GMT
WORKDIR /app
# Fri, 11 Mar 2022 14:30:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Mar 2022 14:30:13 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:e6889e0d66307a4b916fc844f2dcbc03245c63bc4189dd3e88126d9dcf2f9231`  
		Last Modified: Wed, 24 Nov 2021 20:54:48 GMT  
		Size: 2.8 MB (2827117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d6acd3b6e4278a7b3ef37d3525813808468237f086215b68594b244dbd1fba`  
		Last Modified: Tue, 30 Nov 2021 08:26:15 GMT  
		Size: 1.8 MB (1810453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc53af545b93519336bed63b8765255ac8280e27c8e3a17c336f92526b3f290`  
		Last Modified: Tue, 30 Nov 2021 08:26:14 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d406b6d62c3d67bec5f638d47d2b1b49c0ee41d80a791a1b90eaec776cf4fd`  
		Last Modified: Tue, 30 Nov 2021 08:26:13 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09947cbaa6ea94c09911bac9f42ad67e560858bcf313330c30a51d4e047debcc`  
		Last Modified: Fri, 18 Feb 2022 23:36:11 GMT  
		Size: 11.8 MB (11771980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418d95d8e7f7c7a6bca99de67f7268f3c2bd9f90ac05ded2056aca5dcfcf42f3`  
		Last Modified: Fri, 18 Feb 2022 23:36:09 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe93a8e5de6a995b340c34f3b0c9926bbfb8314a31f31edd9aeecf49431cee4`  
		Last Modified: Fri, 11 Mar 2022 11:59:00 GMT  
		Size: 18.0 MB (18045807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98142bd532dfb18d7144d8a1bf1c7a641e931c169b4d2e1863e890a7f1b8e42d`  
		Last Modified: Fri, 11 Mar 2022 11:58:55 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e86e6cc1686366ee83df3ef2c5f3a0405af922746fd6d7ad4fd411ce9a77da`  
		Last Modified: Fri, 11 Mar 2022 11:58:55 GMT  
		Size: 18.8 KB (18773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765d3379030a7d7c59596ec428386624a93faadc763120bcb58cd721522baa8e`  
		Last Modified: Fri, 11 Mar 2022 14:30:44 GMT  
		Size: 15.6 MB (15590818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efdf8175c4916376f3518dfce254d9d6655bbb9cdf549acdfc253419b6d70b0`  
		Last Modified: Fri, 11 Mar 2022 14:30:41 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4713d46f2407dd82fc1fc609c764d58fe738b0f82438ea110f5993116bd1af0`  
		Last Modified: Fri, 11 Mar 2022 14:31:05 GMT  
		Size: 2.8 MB (2798659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76b28c39a135ef18815bf9b6834143d7e2f9e8242f3eca4f4a8ae205e29721b`  
		Last Modified: Fri, 11 Mar 2022 14:31:04 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0e1e6491f2a4eac77a949f9b5f97e615b4075c0cd7cfc468d5c93f4166477c`  
		Last Modified: Fri, 11 Mar 2022 14:31:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.10.25` - linux; ppc64le

```console
$ docker pull composer@sha256:238ccc50cecc665e0612428fd6335f2a5c87a2076bbe5c6cfb11ba837b89c009
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71644520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789d56056d1f6cc38eb4a7ace9e640c1f3df7b92f355d395bbe623a37c183e4c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:20:16 GMT
ADD file:57115dca2eb707f46b6301e75174e6aa316fb02ac28643b91429b75be51bd8c8 in / 
# Wed, 24 Nov 2021 20:20:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 06:02:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 06:03:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 06:03:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 06:03:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 06:03:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 06:03:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 06:03:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 06:04:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 06:04:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:19:05 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:19:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:19:10 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:19:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:19:44 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:41:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 03:41:38 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:41:46 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 03:41:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 03:41:52 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 10:53:22 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 10:53:41 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 10:53:45 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 10:53:51 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Mar 2022 10:55:39 GMT
ENV COMPOSER_VERSION=1.10.25
# Fri, 11 Mar 2022 10:56:33 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 11 Mar 2022 10:56:37 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 11 Mar 2022 10:56:44 GMT
WORKDIR /app
# Fri, 11 Mar 2022 10:56:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Mar 2022 10:56:51 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:159b5dcb1717c815c76ff5ea1db730e18e8609c9090238e43282856db9e71f47`  
		Last Modified: Wed, 24 Nov 2021 20:21:14 GMT  
		Size: 2.8 MB (2814780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603762061fb50079a4b6eb13347fd9a84cc1456d628cf781c89924a54bc419c1`  
		Last Modified: Tue, 30 Nov 2021 07:26:39 GMT  
		Size: 1.8 MB (1756276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645c08440cfaddc2735de2e28697acff0bc71db4cc7242494a44f92c94134e32`  
		Last Modified: Tue, 30 Nov 2021 07:26:39 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5de97a9a329d566f48c2edce253e4ccda6f021041e92326728b7499d13c823b`  
		Last Modified: Tue, 30 Nov 2021 07:26:39 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663cc53ab2317558b9afc14f317845ab71678d9014ef8f4b455b76a1f5ad13b4`  
		Last Modified: Fri, 18 Feb 2022 22:26:29 GMT  
		Size: 11.8 MB (11771981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01091fd3e45df20547a10229a30b96d8cf5998dafc5a5815700834ea2a1cca9`  
		Last Modified: Fri, 18 Feb 2022 22:26:27 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7c08f08c396228976e471a184d4a94d00e1ffcdd366553305de7177eec3bec`  
		Last Modified: Fri, 11 Mar 2022 09:52:14 GMT  
		Size: 18.4 MB (18353518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e767c5a126e3cb62dc8dfdb265ab1b5cfefbbb4955aa58b9ca20fd4e9a3cb5d`  
		Last Modified: Fri, 11 Mar 2022 09:52:10 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a598088569767a94973057cabf1fdeb7dee736eeb4881b2a7e6f18a0c0f2807`  
		Last Modified: Fri, 11 Mar 2022 09:52:10 GMT  
		Size: 18.6 KB (18564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865b388f98b32bac5bade9ff004270a55a0e68d686465a2830ad43a6e6c1e699`  
		Last Modified: Fri, 11 Mar 2022 10:57:32 GMT  
		Size: 33.9 MB (33902882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f226452b0c1667229ee85c065083d8341b4750406d4809c2849e36b27a77a35`  
		Last Modified: Fri, 11 Mar 2022 10:57:25 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1198f7cd9f3fe5c1e629d958a382c57eee946258b4563d653251eed3813d38`  
		Last Modified: Fri, 11 Mar 2022 10:57:54 GMT  
		Size: 3.0 MB (3021400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:294680a6356c69fd99f1419f5db70253c57416d30a27e27ca0720953e9b5fe3e`  
		Last Modified: Fri, 11 Mar 2022 10:57:53 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:869dd640d99702d97db4911680b749e57f83b781c12a540838645ac8724eff83`  
		Last Modified: Fri, 11 Mar 2022 10:57:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.10.25` - linux; s390x

```console
$ docker pull composer@sha256:913e7c6f8a45fc70cbe004f26f2ed97362580042879089c88268ca56424bb38d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69771109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:336da1761462228de7b8ee649fb4e27c3b1d0ea178469480c298aa0f87a53143`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:41:23 GMT
ADD file:cd24c711a2ef431b3ff94f9a02bfc42f159bc60de1d0eceecafea4e8af02441d in / 
# Wed, 24 Nov 2021 20:41:23 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:50:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 04:50:01 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 04:50:02 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 04:50:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 04:50:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 04:50:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 04:50:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 04:50:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 04:50:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:08:01 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:08:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:08:02 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:09:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:09:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:35:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 01:35:50 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:35:51 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 01:35:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 01:35:52 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 05:02:45 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 05:02:47 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 05:02:47 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 05:02:47 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Mar 2022 05:03:10 GMT
ENV COMPOSER_VERSION=1.10.25
# Fri, 11 Mar 2022 05:03:23 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 11 Mar 2022 05:03:23 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 11 Mar 2022 05:03:23 GMT
WORKDIR /app
# Fri, 11 Mar 2022 05:03:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Mar 2022 05:03:23 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d6baca485f3d0f7c77221be60fbef5db014a5ef9d8f53db4a310c947c690d189`  
		Last Modified: Wed, 24 Nov 2021 20:42:15 GMT  
		Size: 2.6 MB (2605944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079fbafa3afc04920b17b503e5d173a44e68fa743eddc7a0eca5e81c7572b8a2`  
		Last Modified: Tue, 30 Nov 2021 08:33:50 GMT  
		Size: 1.8 MB (1771410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ea1ee8ecbda317521ca15da3d8e45a369d74d9b70a0070ebd705cb9aaf88a2`  
		Last Modified: Tue, 30 Nov 2021 08:33:49 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abad577e66a4ab93646ed4a4aefb0579d577932add0d28121e5aece37cfc08dd`  
		Last Modified: Tue, 30 Nov 2021 08:33:49 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac62d72c92f8b14f9b5873207ef984e63eff6fec607db9d4330d9c8129c2925`  
		Last Modified: Fri, 18 Feb 2022 21:13:54 GMT  
		Size: 11.8 MB (11771995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074272c815254eeab42d6bbeac5cb89869166aa437afdace2d9b24a9aa028c4f`  
		Last Modified: Fri, 18 Feb 2022 21:13:53 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a400f11df7f6a7553c85e98fc344489885d2289da563949d00c5280b943f9d0b`  
		Last Modified: Fri, 11 Mar 2022 04:03:48 GMT  
		Size: 16.4 MB (16381073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560e4e59acf6107ca6529fb1d607beb5fe7518052fc9e159c1a89111422d0ed9`  
		Last Modified: Fri, 11 Mar 2022 04:03:46 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93e829bfc7fd232613ba9a365a7a92259718f51bf2ce8df42cf435a15dcc38f`  
		Last Modified: Fri, 11 Mar 2022 04:03:46 GMT  
		Size: 18.6 KB (18598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86bb1285cae11648274513dd55a891e1ca7f14ee80070d95daeae0521db77da`  
		Last Modified: Fri, 11 Mar 2022 05:03:53 GMT  
		Size: 34.9 MB (34887464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e94752314a819cf5f190758a33d2f4d2a3dbde007de6249f275621e5ef423f8`  
		Last Modified: Fri, 11 Mar 2022 05:03:49 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e919933fb117495f8857498e48f4f793b4898536ce4a7cf910549dc1bc0e84`  
		Last Modified: Fri, 11 Mar 2022 05:04:05 GMT  
		Size: 2.3 MB (2329505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89e5c36618de7ab07d355c88e4f4d080e93a9f7db136e5aaedcf301b2563ad0`  
		Last Modified: Fri, 11 Mar 2022 05:04:05 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f621ebfc15dd872a14b0a4f35eb2671f18510efd54fb1361d97fd21da1d979e3`  
		Last Modified: Fri, 11 Mar 2022 05:04:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `composer:2`

```console
$ docker pull composer@sha256:761083bb446357e8ae40438dc32ec74992aaa3f295a5c76a2c19c0b5703d3c61
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

### `composer:2` - linux; amd64

```console
$ docker pull composer@sha256:326e28cdb766579a1e9088d0644f5fbd35fc3a21c4103a1f3e57b24dacfac220
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73039521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa6a91d32046c9419a0bdb982817ae30ee35f1a7a0cd9c13462581eba5ab3de2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 07:06:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 07:06:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 07:06:04 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 07:06:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 07:06:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 07:06:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 07:06:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 07:06:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 07:06:06 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:16:49 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:16:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:16:50 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:17:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:17:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:06:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 04:06:01 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:06:03 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 04:06:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 04:06:03 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 11:55:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 11:55:50 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 11:55:50 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 11:55:50 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 18:19:43 GMT
ENV COMPOSER_VERSION=2.2.9
# Wed, 16 Mar 2022 18:20:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 18:20:03 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 18:20:03 GMT
WORKDIR /app
# Wed, 16 Mar 2022 18:20:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 18:20:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7da25b2876b1c935b05d7e6efa3e8cd559d031cf30b246d7659ed438726acd`  
		Last Modified: Tue, 30 Nov 2021 09:03:50 GMT  
		Size: 1.7 MB (1709704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc599114627e3bd98e0204b93b161e03065bf9a228bb02ae202469655f12b8d`  
		Last Modified: Tue, 30 Nov 2021 09:03:48 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927a0b37a45a98d7d74a6d7d1567230eca834fb89417274557de7986d1f39401`  
		Last Modified: Tue, 30 Nov 2021 09:03:48 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e721f6667a5183c40af8377b3c611b535e9f4eaac41ad37954cc557c4d606dfd`  
		Last Modified: Fri, 18 Feb 2022 23:00:29 GMT  
		Size: 11.8 MB (11771990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdbed47885a29ebdc56f05207500027b26f268bdc5d034f8a6ca8fb34afab54`  
		Last Modified: Fri, 18 Feb 2022 23:00:28 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16135939cf41586188ad9ce6d0b22a1c609842cfcc8f7cb07b9e6db2730c2b37`  
		Last Modified: Fri, 11 Mar 2022 11:16:46 GMT  
		Size: 17.7 MB (17687791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb0fc4c5a6959679cb69633cfe546c6bda81fa74e7a34c9745aeb04921189c5`  
		Last Modified: Fri, 11 Mar 2022 11:16:43 GMT  
		Size: 2.3 KB (2301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37886f8b09348b24b4d10650f01acb3b0517e7d2a69a618c4c87bd1b4ba3df4`  
		Last Modified: Fri, 11 Mar 2022 11:16:43 GMT  
		Size: 18.8 KB (18777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b857d06f2e595fd88321d0fc2350c7811cf2c17127d1039997cb866237878e4d`  
		Last Modified: Fri, 11 Mar 2022 11:56:53 GMT  
		Size: 34.7 MB (34651834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f14b3f6c787d8ee1c2dc4cd24bfecab102e42b082163a5d45722d4e5e22780b`  
		Last Modified: Fri, 11 Mar 2022 11:56:47 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9614584564fb02a9e2f0e3d4654e34a4d5abecf123cc3ef1b490adce6ea509ac`  
		Last Modified: Wed, 16 Mar 2022 18:20:32 GMT  
		Size: 4.4 MB (4375884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2886923f9475c3d778e25d311f8c10e561f965b20bfba4273336a084abc32a5b`  
		Last Modified: Wed, 16 Mar 2022 18:20:30 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5a0cfeadcf4811a573924b6c4ba4df07e7e3c0267838f645a500ad5c2f7535`  
		Last Modified: Wed, 16 Mar 2022 18:20:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2` - linux; arm variant v6

```console
$ docker pull composer@sha256:b6e2de2d5fb63d8e0e314e6d15e1d8eafd7e743c35c9a70bbe4104779f3c9f6b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68400844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acbd8d6d516db4b6ee4c8870d6e9af74da75ab99c426a8109e947161e5ecb850`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 03:20:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 03:20:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 03:20:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 03:20:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 03:20:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 03:20:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 03:20:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 03:20:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 03:20:12 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 19:50:06 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 19:50:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 19:50:07 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 19:50:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 19:50:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:16:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 01:16:18 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:16:21 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 01:16:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 01:16:22 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 04:31:45 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 04:31:47 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 04:31:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 04:31:48 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 18:08:58 GMT
ENV COMPOSER_VERSION=2.2.9
# Wed, 16 Mar 2022 18:09:45 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 18:09:46 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 18:09:46 GMT
WORKDIR /app
# Wed, 16 Mar 2022 18:09:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 18:09:47 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289be6d758ff0faa38d64732e5736031f2250cbf78d1ca4b32abba4accd6a3fa`  
		Last Modified: Tue, 30 Nov 2021 04:29:36 GMT  
		Size: 1.7 MB (1698826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0b442a0f679dba79aa838c408cf49916ca26d27e1252e26f3904d7c5b83d6c`  
		Last Modified: Tue, 30 Nov 2021 04:29:33 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef02b1cade59fbcc24c0ee972dd15d8caa89dda554cdb8aa742de1c6f3d5b7c`  
		Last Modified: Tue, 30 Nov 2021 04:29:33 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452d0467a92abee019a5ea9cdd7cf7b52fb629aa35a045df70339fb93b634760`  
		Last Modified: Fri, 18 Feb 2022 20:43:48 GMT  
		Size: 11.8 MB (11771982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e48b13f55f3236500af7e58ba05199b7acf9a4d62bc99270797ca5f5c1bc88`  
		Last Modified: Fri, 18 Feb 2022 20:43:45 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59c13e75cc1f96edac01b31ca5bf7f47552e1b3662911082d1926896e971fa4`  
		Last Modified: Fri, 11 Mar 2022 03:24:45 GMT  
		Size: 16.0 MB (16031967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0e34d07dc9c018a0df930e952b25876b7c0168a21c1a5a41e366c8103313b7`  
		Last Modified: Fri, 11 Mar 2022 03:24:38 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139e94b314f0a7968bb009c6b624a733bc8b17cde4cc3c5fb98883a957793045`  
		Last Modified: Fri, 11 Mar 2022 03:24:38 GMT  
		Size: 18.6 KB (18571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f789c188a53299f824e7c04be763e79c5b526773d8151b1e07b136bcde02fe78`  
		Last Modified: Fri, 11 Mar 2022 04:34:52 GMT  
		Size: 32.1 MB (32141861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ff5480814d31ae5b439e71effe3a89f8726a82b5f9531c24575c309aa5b802`  
		Last Modified: Fri, 11 Mar 2022 04:34:29 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d9913925d9bc064600a02965ab181c57ee38bcf13ae2b8fca5f5ceb49a6f09`  
		Last Modified: Wed, 16 Mar 2022 18:11:06 GMT  
		Size: 4.1 MB (4101086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee747280ba0407bc5a9ac0a76248042a687be679e269721b28ee8720135d6e29`  
		Last Modified: Wed, 16 Mar 2022 18:11:03 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f7208db20f07db348936636dd910d9c20b944a6585b4a5250e9187492e5694`  
		Last Modified: Wed, 16 Mar 2022 18:11:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2` - linux; arm variant v7

```console
$ docker pull composer@sha256:8e7985450dd6157d802db9b8486af01981b5d6f0bfd0577437d32b7f6f98543f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65134499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c848ee419322351ac7186825962f5c9118465091a1f2cc0fd1ae0df13011133`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 05:27:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 05:27:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 05:27:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 05:27:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 05:27:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 05:27:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:27:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:27:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 05:27:21 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:43:09 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:43:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:43:09 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:43:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:43:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 02:43:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 02:43:15 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 02:43:17 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 02:43:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 02:43:18 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 12:13:42 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 12:13:44 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 12:13:44 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 12:13:45 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 17:58:36 GMT
ENV COMPOSER_VERSION=2.2.9
# Wed, 16 Mar 2022 17:59:22 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 17:59:22 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 17:59:23 GMT
WORKDIR /app
# Wed, 16 Mar 2022 17:59:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 17:59:24 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484fe107211badcebee7c4211e5ed91c7e5212cdd6d7edbb292a63ec60572bdd`  
		Last Modified: Tue, 30 Nov 2021 06:57:00 GMT  
		Size: 1.6 MB (1568802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93353d0a7113f37ba224b9ee296684e49f27c1c9440d3a3c5d310749213da97f`  
		Last Modified: Tue, 30 Nov 2021 06:56:59 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137db50a58959a68358c190d2a143088b82ab25d97cb889876fbc0728e446058`  
		Last Modified: Tue, 30 Nov 2021 06:57:00 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122d3a581986e22d7617f0ef2245bcb64b2a87ebcfe58b7b6d143561ce0cc8b2`  
		Last Modified: Fri, 18 Feb 2022 22:37:27 GMT  
		Size: 11.8 MB (11771980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc11ce0d4bdb5fcdda54f9da2a0eb1e4751b77e354a0dcdb827def3ff59f9f6`  
		Last Modified: Fri, 18 Feb 2022 22:37:24 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1951768145bebb84adba11b1ccd77c8d3802784df6c56f3ae141c103ac114c35`  
		Last Modified: Fri, 11 Mar 2022 07:38:53 GMT  
		Size: 15.0 MB (15034421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fdf84bb546f4d33ce7fff41672c1959df0ef457af702871c4ca3e4d585d8d87`  
		Last Modified: Fri, 11 Mar 2022 07:38:43 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164a1f0370d8b9c1f9c97a1a5aa3993986015fbe893874af94b911c5b8b06870`  
		Last Modified: Fri, 11 Mar 2022 07:38:43 GMT  
		Size: 18.6 KB (18569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b3d0ba165529b585fb1997f3fbc2d14dac5ccff866a44bff4b22578e6bd6aa`  
		Last Modified: Fri, 11 Mar 2022 12:16:34 GMT  
		Size: 30.5 MB (30471948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8e62f6bd555ee3d4b4ee22e2664dad7d5e0053556763e911676f59e8430be7`  
		Last Modified: Fri, 11 Mar 2022 12:16:14 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07eddbcbd7af52d2f868be4e78de819baaed038b501271a2500ac2fc4bba53b`  
		Last Modified: Wed, 16 Mar 2022 18:00:42 GMT  
		Size: 3.8 MB (3828887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbc1e6568bb9b37f50762a3378bd8a25055ac9fbaf11ec2d43c94234987698c`  
		Last Modified: Wed, 16 Mar 2022 18:00:40 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3da75e4905627fccb6521ac3f1c1b93c66ffbdb7a662f25ce6db75903277cf`  
		Last Modified: Wed, 16 Mar 2022 18:00:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:88ecf252d0fa4c6321e415dbda78934f3296272312613f11a68fcf0eaf357307
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71007032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5390a7677c7fd8300733ca205ed96ed73dd9de3e515d30be30a61725a621364f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 02:50:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 02:50:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 02:50:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 02:50:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 02:50:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 02:50:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 02:50:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 02:50:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 02:50:54 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:18:23 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:18:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:18:25 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:19:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:19:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:18:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 03:18:52 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:18:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 03:18:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 03:18:55 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 10:35:18 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 10:35:18 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 10:35:19 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 10:35:20 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 17:40:22 GMT
ENV COMPOSER_VERSION=2.2.9
# Wed, 16 Mar 2022 17:40:45 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 17:40:46 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 17:40:46 GMT
WORKDIR /app
# Wed, 16 Mar 2022 17:40:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 17:40:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd720d9f53003155e4cfe3f1974fc0e4d74a622ea8c61cfccb00ee8b842c09b6`  
		Last Modified: Tue, 30 Nov 2021 03:59:34 GMT  
		Size: 1.7 MB (1708308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680efee530f3c970c3140b358d3dc583ded463f9adbadb737ca64c765cf997ee`  
		Last Modified: Tue, 30 Nov 2021 03:59:33 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643d01251bc949843dbd734a37e7cf28a01af4ea11443738b8b92d17e1e438de`  
		Last Modified: Tue, 30 Nov 2021 03:59:33 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbd0dff840aec18863650b4a5db905ad8e50c878c0d1f6c4c1634d0a4743ae4`  
		Last Modified: Fri, 18 Feb 2022 21:39:27 GMT  
		Size: 11.8 MB (11771755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6104c5a569f57122fffc091a5376f51c0848737cec9feaa9a82531e6c2da43`  
		Last Modified: Fri, 18 Feb 2022 21:39:26 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf59a8a0ffa368fdd033e0104d93a4b4913881c7f6bd86aaef35c541233a018`  
		Last Modified: Fri, 11 Mar 2022 09:48:26 GMT  
		Size: 17.5 MB (17546174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef08d98d3666360bd8cbe19dcb81037d75a8aca59ebcfd386287fccb05cc9aab`  
		Last Modified: Fri, 11 Mar 2022 09:48:22 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e7653a3be11ae60976b3f56b5349443e6c458f125a944ba93d234548413851`  
		Last Modified: Fri, 11 Mar 2022 09:48:22 GMT  
		Size: 18.5 KB (18487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f017cf68653c976946e3d237367accaca773a59fbfae998075a1dfc4d6703911`  
		Last Modified: Fri, 11 Mar 2022 10:36:49 GMT  
		Size: 33.0 MB (33001745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0c25578ca0b4f7b253053edcefd8aaea561ada9282ced6617c66749e3cbd4e`  
		Last Modified: Fri, 11 Mar 2022 10:36:44 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f681d2af1a050fe7840d4cedae9568fa0ae020ab2860070fe7031503578ab40`  
		Last Modified: Wed, 16 Mar 2022 17:42:26 GMT  
		Size: 4.2 MB (4240106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94edf64a4261df8ee69484e617d69127d0c311998bad01d1e3e4556ff3dcc8ca`  
		Last Modified: Wed, 16 Mar 2022 17:42:25 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7a0434d0b212ef33c720406d8f0808fa9dda1fe4160e791da97681d4edaffc`  
		Last Modified: Wed, 16 Mar 2022 17:42:25 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2` - linux; 386

```console
$ docker pull composer@sha256:a2477b4f8e6288b6cfdd1cabc3eed000d8e511fe967addb5a379e5f5887db17b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.4 MB (54414804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d7adaf71922c61637b4fcc20a8d11cb2062b357ac1cb0149ed700ee5f50bb7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:53:48 GMT
ADD file:b9a17131c440053f2f67e127b447645f25fd7de2d6caca42f569cafab6291855 in / 
# Wed, 24 Nov 2021 20:53:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 05:59:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 05:59:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 05:59:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 05:59:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 05:59:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 05:59:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:59:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:59:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 05:59:11 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:49:36 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:49:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:49:37 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:50:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:50:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:42:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 04:42:32 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:42:33 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 04:42:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 04:42:33 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 14:29:16 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 14:29:16 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 14:29:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 14:29:17 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 17:39:59 GMT
ENV COMPOSER_VERSION=2.2.9
# Wed, 16 Mar 2022 17:40:24 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 17:40:26 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 17:40:27 GMT
WORKDIR /app
# Wed, 16 Mar 2022 17:40:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 17:40:27 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:e6889e0d66307a4b916fc844f2dcbc03245c63bc4189dd3e88126d9dcf2f9231`  
		Last Modified: Wed, 24 Nov 2021 20:54:48 GMT  
		Size: 2.8 MB (2827117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d6acd3b6e4278a7b3ef37d3525813808468237f086215b68594b244dbd1fba`  
		Last Modified: Tue, 30 Nov 2021 08:26:15 GMT  
		Size: 1.8 MB (1810453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc53af545b93519336bed63b8765255ac8280e27c8e3a17c336f92526b3f290`  
		Last Modified: Tue, 30 Nov 2021 08:26:14 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d406b6d62c3d67bec5f638d47d2b1b49c0ee41d80a791a1b90eaec776cf4fd`  
		Last Modified: Tue, 30 Nov 2021 08:26:13 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09947cbaa6ea94c09911bac9f42ad67e560858bcf313330c30a51d4e047debcc`  
		Last Modified: Fri, 18 Feb 2022 23:36:11 GMT  
		Size: 11.8 MB (11771980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418d95d8e7f7c7a6bca99de67f7268f3c2bd9f90ac05ded2056aca5dcfcf42f3`  
		Last Modified: Fri, 18 Feb 2022 23:36:09 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe93a8e5de6a995b340c34f3b0c9926bbfb8314a31f31edd9aeecf49431cee4`  
		Last Modified: Fri, 11 Mar 2022 11:59:00 GMT  
		Size: 18.0 MB (18045807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98142bd532dfb18d7144d8a1bf1c7a641e931c169b4d2e1863e890a7f1b8e42d`  
		Last Modified: Fri, 11 Mar 2022 11:58:55 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e86e6cc1686366ee83df3ef2c5f3a0405af922746fd6d7ad4fd411ce9a77da`  
		Last Modified: Fri, 11 Mar 2022 11:58:55 GMT  
		Size: 18.8 KB (18773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765d3379030a7d7c59596ec428386624a93faadc763120bcb58cd721522baa8e`  
		Last Modified: Fri, 11 Mar 2022 14:30:44 GMT  
		Size: 15.6 MB (15590818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efdf8175c4916376f3518dfce254d9d6655bbb9cdf549acdfc253419b6d70b0`  
		Last Modified: Fri, 11 Mar 2022 14:30:41 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66086ccb543f409dbb0372048314fc39072d900a3b36b3efaf8e886310fc456`  
		Last Modified: Wed, 16 Mar 2022 17:41:30 GMT  
		Size: 4.3 MB (4344725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977603e326a453ec883002a965684daaf1f2b8495410041064afb673231e6433`  
		Last Modified: Wed, 16 Mar 2022 17:41:28 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c4920c285cadc297fb006fb893ba20057f8f86ef9dac2afce0f0c2d331aa46`  
		Last Modified: Wed, 16 Mar 2022 17:41:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2` - linux; ppc64le

```console
$ docker pull composer@sha256:bce9ee868315f50bf13b33b49d5743c5bc838bc6730b13f13e1a67d939ab56fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73121143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a1d96d152754d33c266b566e0b7790f6bfb37ba43e15b6845c8354832816c8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:20:16 GMT
ADD file:57115dca2eb707f46b6301e75174e6aa316fb02ac28643b91429b75be51bd8c8 in / 
# Wed, 24 Nov 2021 20:20:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 06:02:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 06:03:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 06:03:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 06:03:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 06:03:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 06:03:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 06:03:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 06:04:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 06:04:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:19:05 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:19:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:19:10 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:19:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:19:44 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:41:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 03:41:38 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:41:46 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 03:41:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 03:41:52 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 10:53:22 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 10:53:41 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 10:53:45 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 10:53:51 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 18:29:39 GMT
ENV COMPOSER_VERSION=2.2.9
# Wed, 16 Mar 2022 18:30:52 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 18:31:59 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 18:32:57 GMT
WORKDIR /app
# Wed, 16 Mar 2022 18:34:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 18:35:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:159b5dcb1717c815c76ff5ea1db730e18e8609c9090238e43282856db9e71f47`  
		Last Modified: Wed, 24 Nov 2021 20:21:14 GMT  
		Size: 2.8 MB (2814780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603762061fb50079a4b6eb13347fd9a84cc1456d628cf781c89924a54bc419c1`  
		Last Modified: Tue, 30 Nov 2021 07:26:39 GMT  
		Size: 1.8 MB (1756276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645c08440cfaddc2735de2e28697acff0bc71db4cc7242494a44f92c94134e32`  
		Last Modified: Tue, 30 Nov 2021 07:26:39 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5de97a9a329d566f48c2edce253e4ccda6f021041e92326728b7499d13c823b`  
		Last Modified: Tue, 30 Nov 2021 07:26:39 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663cc53ab2317558b9afc14f317845ab71678d9014ef8f4b455b76a1f5ad13b4`  
		Last Modified: Fri, 18 Feb 2022 22:26:29 GMT  
		Size: 11.8 MB (11771981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01091fd3e45df20547a10229a30b96d8cf5998dafc5a5815700834ea2a1cca9`  
		Last Modified: Fri, 18 Feb 2022 22:26:27 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7c08f08c396228976e471a184d4a94d00e1ffcdd366553305de7177eec3bec`  
		Last Modified: Fri, 11 Mar 2022 09:52:14 GMT  
		Size: 18.4 MB (18353518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e767c5a126e3cb62dc8dfdb265ab1b5cfefbbb4955aa58b9ca20fd4e9a3cb5d`  
		Last Modified: Fri, 11 Mar 2022 09:52:10 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a598088569767a94973057cabf1fdeb7dee736eeb4881b2a7e6f18a0c0f2807`  
		Last Modified: Fri, 11 Mar 2022 09:52:10 GMT  
		Size: 18.6 KB (18564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865b388f98b32bac5bade9ff004270a55a0e68d686465a2830ad43a6e6c1e699`  
		Last Modified: Fri, 11 Mar 2022 10:57:32 GMT  
		Size: 33.9 MB (33902882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f226452b0c1667229ee85c065083d8341b4750406d4809c2849e36b27a77a35`  
		Last Modified: Fri, 11 Mar 2022 10:57:25 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5f6fd27e5c402548636d63962e13de0ced945c9a6943a67c408ef6c18e071d`  
		Last Modified: Wed, 16 Mar 2022 18:44:00 GMT  
		Size: 4.5 MB (4498013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3fba9e19771a5ee851139d0b6465620f9acd7ed4f74a85eaaf86547836919f`  
		Last Modified: Wed, 16 Mar 2022 18:43:59 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec711f0032b76a073691ea34ea9edbcaeffecf203ca1ad55d6d2e712cdc6e9a`  
		Last Modified: Wed, 16 Mar 2022 18:43:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2` - linux; s390x

```console
$ docker pull composer@sha256:4d6d35d1f21dd04ec59345df6103a538e2c87b72dba6bed4d4e510b75ce69301
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71633583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a7cdde9dd9c512ec61147343e6160697e2ce8a5ca240881238d801b6fad937`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:41:23 GMT
ADD file:cd24c711a2ef431b3ff94f9a02bfc42f159bc60de1d0eceecafea4e8af02441d in / 
# Wed, 24 Nov 2021 20:41:23 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:50:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 04:50:01 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 04:50:02 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 04:50:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 04:50:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 04:50:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 04:50:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 04:50:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 04:50:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:08:01 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:08:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:08:02 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:09:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:09:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:35:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 01:35:50 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:35:51 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 01:35:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 01:35:52 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 05:02:45 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 05:02:47 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 05:02:47 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 05:02:47 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 17:41:52 GMT
ENV COMPOSER_VERSION=2.2.9
# Wed, 16 Mar 2022 17:42:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 17:42:07 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 17:42:07 GMT
WORKDIR /app
# Wed, 16 Mar 2022 17:42:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 17:42:07 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d6baca485f3d0f7c77221be60fbef5db014a5ef9d8f53db4a310c947c690d189`  
		Last Modified: Wed, 24 Nov 2021 20:42:15 GMT  
		Size: 2.6 MB (2605944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079fbafa3afc04920b17b503e5d173a44e68fa743eddc7a0eca5e81c7572b8a2`  
		Last Modified: Tue, 30 Nov 2021 08:33:50 GMT  
		Size: 1.8 MB (1771410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ea1ee8ecbda317521ca15da3d8e45a369d74d9b70a0070ebd705cb9aaf88a2`  
		Last Modified: Tue, 30 Nov 2021 08:33:49 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abad577e66a4ab93646ed4a4aefb0579d577932add0d28121e5aece37cfc08dd`  
		Last Modified: Tue, 30 Nov 2021 08:33:49 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac62d72c92f8b14f9b5873207ef984e63eff6fec607db9d4330d9c8129c2925`  
		Last Modified: Fri, 18 Feb 2022 21:13:54 GMT  
		Size: 11.8 MB (11771995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074272c815254eeab42d6bbeac5cb89869166aa437afdace2d9b24a9aa028c4f`  
		Last Modified: Fri, 18 Feb 2022 21:13:53 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a400f11df7f6a7553c85e98fc344489885d2289da563949d00c5280b943f9d0b`  
		Last Modified: Fri, 11 Mar 2022 04:03:48 GMT  
		Size: 16.4 MB (16381073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560e4e59acf6107ca6529fb1d607beb5fe7518052fc9e159c1a89111422d0ed9`  
		Last Modified: Fri, 11 Mar 2022 04:03:46 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93e829bfc7fd232613ba9a365a7a92259718f51bf2ce8df42cf435a15dcc38f`  
		Last Modified: Fri, 11 Mar 2022 04:03:46 GMT  
		Size: 18.6 KB (18598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86bb1285cae11648274513dd55a891e1ca7f14ee80070d95daeae0521db77da`  
		Last Modified: Fri, 11 Mar 2022 05:03:53 GMT  
		Size: 34.9 MB (34887464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e94752314a819cf5f190758a33d2f4d2a3dbde007de6249f275621e5ef423f8`  
		Last Modified: Fri, 11 Mar 2022 05:03:49 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ffe7b695380f1c31a8200b263d206389b1cf9117d2a11fd0e6bfc24f1e942a`  
		Last Modified: Wed, 16 Mar 2022 17:42:49 GMT  
		Size: 4.2 MB (4191968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d40d17a09a360286b6e38702644ca38fb0c0726399c1ad778a4d9f6491eb518`  
		Last Modified: Wed, 16 Mar 2022 17:42:49 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8460fa71b15c5f0aa3bd56ccea29886a800bbb4642cb363ace43b94885fd7d`  
		Last Modified: Wed, 16 Mar 2022 17:42:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `composer:2.2`

```console
$ docker pull composer@sha256:761083bb446357e8ae40438dc32ec74992aaa3f295a5c76a2c19c0b5703d3c61
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

### `composer:2.2` - linux; amd64

```console
$ docker pull composer@sha256:326e28cdb766579a1e9088d0644f5fbd35fc3a21c4103a1f3e57b24dacfac220
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73039521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa6a91d32046c9419a0bdb982817ae30ee35f1a7a0cd9c13462581eba5ab3de2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 07:06:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 07:06:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 07:06:04 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 07:06:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 07:06:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 07:06:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 07:06:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 07:06:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 07:06:06 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:16:49 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:16:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:16:50 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:17:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:17:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:06:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 04:06:01 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:06:03 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 04:06:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 04:06:03 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 11:55:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 11:55:50 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 11:55:50 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 11:55:50 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 18:19:43 GMT
ENV COMPOSER_VERSION=2.2.9
# Wed, 16 Mar 2022 18:20:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 18:20:03 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 18:20:03 GMT
WORKDIR /app
# Wed, 16 Mar 2022 18:20:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 18:20:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7da25b2876b1c935b05d7e6efa3e8cd559d031cf30b246d7659ed438726acd`  
		Last Modified: Tue, 30 Nov 2021 09:03:50 GMT  
		Size: 1.7 MB (1709704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc599114627e3bd98e0204b93b161e03065bf9a228bb02ae202469655f12b8d`  
		Last Modified: Tue, 30 Nov 2021 09:03:48 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927a0b37a45a98d7d74a6d7d1567230eca834fb89417274557de7986d1f39401`  
		Last Modified: Tue, 30 Nov 2021 09:03:48 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e721f6667a5183c40af8377b3c611b535e9f4eaac41ad37954cc557c4d606dfd`  
		Last Modified: Fri, 18 Feb 2022 23:00:29 GMT  
		Size: 11.8 MB (11771990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdbed47885a29ebdc56f05207500027b26f268bdc5d034f8a6ca8fb34afab54`  
		Last Modified: Fri, 18 Feb 2022 23:00:28 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16135939cf41586188ad9ce6d0b22a1c609842cfcc8f7cb07b9e6db2730c2b37`  
		Last Modified: Fri, 11 Mar 2022 11:16:46 GMT  
		Size: 17.7 MB (17687791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb0fc4c5a6959679cb69633cfe546c6bda81fa74e7a34c9745aeb04921189c5`  
		Last Modified: Fri, 11 Mar 2022 11:16:43 GMT  
		Size: 2.3 KB (2301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37886f8b09348b24b4d10650f01acb3b0517e7d2a69a618c4c87bd1b4ba3df4`  
		Last Modified: Fri, 11 Mar 2022 11:16:43 GMT  
		Size: 18.8 KB (18777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b857d06f2e595fd88321d0fc2350c7811cf2c17127d1039997cb866237878e4d`  
		Last Modified: Fri, 11 Mar 2022 11:56:53 GMT  
		Size: 34.7 MB (34651834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f14b3f6c787d8ee1c2dc4cd24bfecab102e42b082163a5d45722d4e5e22780b`  
		Last Modified: Fri, 11 Mar 2022 11:56:47 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9614584564fb02a9e2f0e3d4654e34a4d5abecf123cc3ef1b490adce6ea509ac`  
		Last Modified: Wed, 16 Mar 2022 18:20:32 GMT  
		Size: 4.4 MB (4375884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2886923f9475c3d778e25d311f8c10e561f965b20bfba4273336a084abc32a5b`  
		Last Modified: Wed, 16 Mar 2022 18:20:30 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5a0cfeadcf4811a573924b6c4ba4df07e7e3c0267838f645a500ad5c2f7535`  
		Last Modified: Wed, 16 Mar 2022 18:20:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.2` - linux; arm variant v6

```console
$ docker pull composer@sha256:b6e2de2d5fb63d8e0e314e6d15e1d8eafd7e743c35c9a70bbe4104779f3c9f6b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68400844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acbd8d6d516db4b6ee4c8870d6e9af74da75ab99c426a8109e947161e5ecb850`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 03:20:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 03:20:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 03:20:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 03:20:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 03:20:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 03:20:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 03:20:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 03:20:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 03:20:12 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 19:50:06 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 19:50:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 19:50:07 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 19:50:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 19:50:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:16:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 01:16:18 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:16:21 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 01:16:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 01:16:22 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 04:31:45 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 04:31:47 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 04:31:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 04:31:48 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 18:08:58 GMT
ENV COMPOSER_VERSION=2.2.9
# Wed, 16 Mar 2022 18:09:45 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 18:09:46 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 18:09:46 GMT
WORKDIR /app
# Wed, 16 Mar 2022 18:09:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 18:09:47 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289be6d758ff0faa38d64732e5736031f2250cbf78d1ca4b32abba4accd6a3fa`  
		Last Modified: Tue, 30 Nov 2021 04:29:36 GMT  
		Size: 1.7 MB (1698826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0b442a0f679dba79aa838c408cf49916ca26d27e1252e26f3904d7c5b83d6c`  
		Last Modified: Tue, 30 Nov 2021 04:29:33 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef02b1cade59fbcc24c0ee972dd15d8caa89dda554cdb8aa742de1c6f3d5b7c`  
		Last Modified: Tue, 30 Nov 2021 04:29:33 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452d0467a92abee019a5ea9cdd7cf7b52fb629aa35a045df70339fb93b634760`  
		Last Modified: Fri, 18 Feb 2022 20:43:48 GMT  
		Size: 11.8 MB (11771982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e48b13f55f3236500af7e58ba05199b7acf9a4d62bc99270797ca5f5c1bc88`  
		Last Modified: Fri, 18 Feb 2022 20:43:45 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59c13e75cc1f96edac01b31ca5bf7f47552e1b3662911082d1926896e971fa4`  
		Last Modified: Fri, 11 Mar 2022 03:24:45 GMT  
		Size: 16.0 MB (16031967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0e34d07dc9c018a0df930e952b25876b7c0168a21c1a5a41e366c8103313b7`  
		Last Modified: Fri, 11 Mar 2022 03:24:38 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139e94b314f0a7968bb009c6b624a733bc8b17cde4cc3c5fb98883a957793045`  
		Last Modified: Fri, 11 Mar 2022 03:24:38 GMT  
		Size: 18.6 KB (18571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f789c188a53299f824e7c04be763e79c5b526773d8151b1e07b136bcde02fe78`  
		Last Modified: Fri, 11 Mar 2022 04:34:52 GMT  
		Size: 32.1 MB (32141861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ff5480814d31ae5b439e71effe3a89f8726a82b5f9531c24575c309aa5b802`  
		Last Modified: Fri, 11 Mar 2022 04:34:29 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d9913925d9bc064600a02965ab181c57ee38bcf13ae2b8fca5f5ceb49a6f09`  
		Last Modified: Wed, 16 Mar 2022 18:11:06 GMT  
		Size: 4.1 MB (4101086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee747280ba0407bc5a9ac0a76248042a687be679e269721b28ee8720135d6e29`  
		Last Modified: Wed, 16 Mar 2022 18:11:03 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f7208db20f07db348936636dd910d9c20b944a6585b4a5250e9187492e5694`  
		Last Modified: Wed, 16 Mar 2022 18:11:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.2` - linux; arm variant v7

```console
$ docker pull composer@sha256:8e7985450dd6157d802db9b8486af01981b5d6f0bfd0577437d32b7f6f98543f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65134499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c848ee419322351ac7186825962f5c9118465091a1f2cc0fd1ae0df13011133`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 05:27:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 05:27:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 05:27:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 05:27:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 05:27:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 05:27:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:27:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:27:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 05:27:21 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:43:09 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:43:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:43:09 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:43:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:43:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 02:43:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 02:43:15 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 02:43:17 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 02:43:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 02:43:18 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 12:13:42 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 12:13:44 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 12:13:44 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 12:13:45 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 17:58:36 GMT
ENV COMPOSER_VERSION=2.2.9
# Wed, 16 Mar 2022 17:59:22 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 17:59:22 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 17:59:23 GMT
WORKDIR /app
# Wed, 16 Mar 2022 17:59:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 17:59:24 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484fe107211badcebee7c4211e5ed91c7e5212cdd6d7edbb292a63ec60572bdd`  
		Last Modified: Tue, 30 Nov 2021 06:57:00 GMT  
		Size: 1.6 MB (1568802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93353d0a7113f37ba224b9ee296684e49f27c1c9440d3a3c5d310749213da97f`  
		Last Modified: Tue, 30 Nov 2021 06:56:59 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137db50a58959a68358c190d2a143088b82ab25d97cb889876fbc0728e446058`  
		Last Modified: Tue, 30 Nov 2021 06:57:00 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122d3a581986e22d7617f0ef2245bcb64b2a87ebcfe58b7b6d143561ce0cc8b2`  
		Last Modified: Fri, 18 Feb 2022 22:37:27 GMT  
		Size: 11.8 MB (11771980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc11ce0d4bdb5fcdda54f9da2a0eb1e4751b77e354a0dcdb827def3ff59f9f6`  
		Last Modified: Fri, 18 Feb 2022 22:37:24 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1951768145bebb84adba11b1ccd77c8d3802784df6c56f3ae141c103ac114c35`  
		Last Modified: Fri, 11 Mar 2022 07:38:53 GMT  
		Size: 15.0 MB (15034421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fdf84bb546f4d33ce7fff41672c1959df0ef457af702871c4ca3e4d585d8d87`  
		Last Modified: Fri, 11 Mar 2022 07:38:43 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164a1f0370d8b9c1f9c97a1a5aa3993986015fbe893874af94b911c5b8b06870`  
		Last Modified: Fri, 11 Mar 2022 07:38:43 GMT  
		Size: 18.6 KB (18569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b3d0ba165529b585fb1997f3fbc2d14dac5ccff866a44bff4b22578e6bd6aa`  
		Last Modified: Fri, 11 Mar 2022 12:16:34 GMT  
		Size: 30.5 MB (30471948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8e62f6bd555ee3d4b4ee22e2664dad7d5e0053556763e911676f59e8430be7`  
		Last Modified: Fri, 11 Mar 2022 12:16:14 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07eddbcbd7af52d2f868be4e78de819baaed038b501271a2500ac2fc4bba53b`  
		Last Modified: Wed, 16 Mar 2022 18:00:42 GMT  
		Size: 3.8 MB (3828887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbc1e6568bb9b37f50762a3378bd8a25055ac9fbaf11ec2d43c94234987698c`  
		Last Modified: Wed, 16 Mar 2022 18:00:40 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3da75e4905627fccb6521ac3f1c1b93c66ffbdb7a662f25ce6db75903277cf`  
		Last Modified: Wed, 16 Mar 2022 18:00:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:88ecf252d0fa4c6321e415dbda78934f3296272312613f11a68fcf0eaf357307
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71007032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5390a7677c7fd8300733ca205ed96ed73dd9de3e515d30be30a61725a621364f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 02:50:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 02:50:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 02:50:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 02:50:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 02:50:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 02:50:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 02:50:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 02:50:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 02:50:54 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:18:23 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:18:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:18:25 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:19:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:19:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:18:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 03:18:52 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:18:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 03:18:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 03:18:55 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 10:35:18 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 10:35:18 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 10:35:19 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 10:35:20 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 17:40:22 GMT
ENV COMPOSER_VERSION=2.2.9
# Wed, 16 Mar 2022 17:40:45 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 17:40:46 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 17:40:46 GMT
WORKDIR /app
# Wed, 16 Mar 2022 17:40:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 17:40:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd720d9f53003155e4cfe3f1974fc0e4d74a622ea8c61cfccb00ee8b842c09b6`  
		Last Modified: Tue, 30 Nov 2021 03:59:34 GMT  
		Size: 1.7 MB (1708308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680efee530f3c970c3140b358d3dc583ded463f9adbadb737ca64c765cf997ee`  
		Last Modified: Tue, 30 Nov 2021 03:59:33 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643d01251bc949843dbd734a37e7cf28a01af4ea11443738b8b92d17e1e438de`  
		Last Modified: Tue, 30 Nov 2021 03:59:33 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbd0dff840aec18863650b4a5db905ad8e50c878c0d1f6c4c1634d0a4743ae4`  
		Last Modified: Fri, 18 Feb 2022 21:39:27 GMT  
		Size: 11.8 MB (11771755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6104c5a569f57122fffc091a5376f51c0848737cec9feaa9a82531e6c2da43`  
		Last Modified: Fri, 18 Feb 2022 21:39:26 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf59a8a0ffa368fdd033e0104d93a4b4913881c7f6bd86aaef35c541233a018`  
		Last Modified: Fri, 11 Mar 2022 09:48:26 GMT  
		Size: 17.5 MB (17546174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef08d98d3666360bd8cbe19dcb81037d75a8aca59ebcfd386287fccb05cc9aab`  
		Last Modified: Fri, 11 Mar 2022 09:48:22 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e7653a3be11ae60976b3f56b5349443e6c458f125a944ba93d234548413851`  
		Last Modified: Fri, 11 Mar 2022 09:48:22 GMT  
		Size: 18.5 KB (18487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f017cf68653c976946e3d237367accaca773a59fbfae998075a1dfc4d6703911`  
		Last Modified: Fri, 11 Mar 2022 10:36:49 GMT  
		Size: 33.0 MB (33001745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0c25578ca0b4f7b253053edcefd8aaea561ada9282ced6617c66749e3cbd4e`  
		Last Modified: Fri, 11 Mar 2022 10:36:44 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f681d2af1a050fe7840d4cedae9568fa0ae020ab2860070fe7031503578ab40`  
		Last Modified: Wed, 16 Mar 2022 17:42:26 GMT  
		Size: 4.2 MB (4240106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94edf64a4261df8ee69484e617d69127d0c311998bad01d1e3e4556ff3dcc8ca`  
		Last Modified: Wed, 16 Mar 2022 17:42:25 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7a0434d0b212ef33c720406d8f0808fa9dda1fe4160e791da97681d4edaffc`  
		Last Modified: Wed, 16 Mar 2022 17:42:25 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.2` - linux; 386

```console
$ docker pull composer@sha256:a2477b4f8e6288b6cfdd1cabc3eed000d8e511fe967addb5a379e5f5887db17b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.4 MB (54414804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d7adaf71922c61637b4fcc20a8d11cb2062b357ac1cb0149ed700ee5f50bb7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:53:48 GMT
ADD file:b9a17131c440053f2f67e127b447645f25fd7de2d6caca42f569cafab6291855 in / 
# Wed, 24 Nov 2021 20:53:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 05:59:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 05:59:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 05:59:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 05:59:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 05:59:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 05:59:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:59:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:59:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 05:59:11 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:49:36 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:49:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:49:37 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:50:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:50:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:42:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 04:42:32 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:42:33 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 04:42:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 04:42:33 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 14:29:16 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 14:29:16 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 14:29:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 14:29:17 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 17:39:59 GMT
ENV COMPOSER_VERSION=2.2.9
# Wed, 16 Mar 2022 17:40:24 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 17:40:26 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 17:40:27 GMT
WORKDIR /app
# Wed, 16 Mar 2022 17:40:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 17:40:27 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:e6889e0d66307a4b916fc844f2dcbc03245c63bc4189dd3e88126d9dcf2f9231`  
		Last Modified: Wed, 24 Nov 2021 20:54:48 GMT  
		Size: 2.8 MB (2827117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d6acd3b6e4278a7b3ef37d3525813808468237f086215b68594b244dbd1fba`  
		Last Modified: Tue, 30 Nov 2021 08:26:15 GMT  
		Size: 1.8 MB (1810453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc53af545b93519336bed63b8765255ac8280e27c8e3a17c336f92526b3f290`  
		Last Modified: Tue, 30 Nov 2021 08:26:14 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d406b6d62c3d67bec5f638d47d2b1b49c0ee41d80a791a1b90eaec776cf4fd`  
		Last Modified: Tue, 30 Nov 2021 08:26:13 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09947cbaa6ea94c09911bac9f42ad67e560858bcf313330c30a51d4e047debcc`  
		Last Modified: Fri, 18 Feb 2022 23:36:11 GMT  
		Size: 11.8 MB (11771980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418d95d8e7f7c7a6bca99de67f7268f3c2bd9f90ac05ded2056aca5dcfcf42f3`  
		Last Modified: Fri, 18 Feb 2022 23:36:09 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe93a8e5de6a995b340c34f3b0c9926bbfb8314a31f31edd9aeecf49431cee4`  
		Last Modified: Fri, 11 Mar 2022 11:59:00 GMT  
		Size: 18.0 MB (18045807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98142bd532dfb18d7144d8a1bf1c7a641e931c169b4d2e1863e890a7f1b8e42d`  
		Last Modified: Fri, 11 Mar 2022 11:58:55 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e86e6cc1686366ee83df3ef2c5f3a0405af922746fd6d7ad4fd411ce9a77da`  
		Last Modified: Fri, 11 Mar 2022 11:58:55 GMT  
		Size: 18.8 KB (18773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765d3379030a7d7c59596ec428386624a93faadc763120bcb58cd721522baa8e`  
		Last Modified: Fri, 11 Mar 2022 14:30:44 GMT  
		Size: 15.6 MB (15590818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efdf8175c4916376f3518dfce254d9d6655bbb9cdf549acdfc253419b6d70b0`  
		Last Modified: Fri, 11 Mar 2022 14:30:41 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66086ccb543f409dbb0372048314fc39072d900a3b36b3efaf8e886310fc456`  
		Last Modified: Wed, 16 Mar 2022 17:41:30 GMT  
		Size: 4.3 MB (4344725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977603e326a453ec883002a965684daaf1f2b8495410041064afb673231e6433`  
		Last Modified: Wed, 16 Mar 2022 17:41:28 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c4920c285cadc297fb006fb893ba20057f8f86ef9dac2afce0f0c2d331aa46`  
		Last Modified: Wed, 16 Mar 2022 17:41:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.2` - linux; ppc64le

```console
$ docker pull composer@sha256:bce9ee868315f50bf13b33b49d5743c5bc838bc6730b13f13e1a67d939ab56fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73121143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a1d96d152754d33c266b566e0b7790f6bfb37ba43e15b6845c8354832816c8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:20:16 GMT
ADD file:57115dca2eb707f46b6301e75174e6aa316fb02ac28643b91429b75be51bd8c8 in / 
# Wed, 24 Nov 2021 20:20:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 06:02:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 06:03:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 06:03:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 06:03:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 06:03:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 06:03:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 06:03:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 06:04:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 06:04:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:19:05 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:19:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:19:10 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:19:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:19:44 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:41:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 03:41:38 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:41:46 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 03:41:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 03:41:52 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 10:53:22 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 10:53:41 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 10:53:45 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 10:53:51 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 18:29:39 GMT
ENV COMPOSER_VERSION=2.2.9
# Wed, 16 Mar 2022 18:30:52 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 18:31:59 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 18:32:57 GMT
WORKDIR /app
# Wed, 16 Mar 2022 18:34:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 18:35:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:159b5dcb1717c815c76ff5ea1db730e18e8609c9090238e43282856db9e71f47`  
		Last Modified: Wed, 24 Nov 2021 20:21:14 GMT  
		Size: 2.8 MB (2814780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603762061fb50079a4b6eb13347fd9a84cc1456d628cf781c89924a54bc419c1`  
		Last Modified: Tue, 30 Nov 2021 07:26:39 GMT  
		Size: 1.8 MB (1756276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645c08440cfaddc2735de2e28697acff0bc71db4cc7242494a44f92c94134e32`  
		Last Modified: Tue, 30 Nov 2021 07:26:39 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5de97a9a329d566f48c2edce253e4ccda6f021041e92326728b7499d13c823b`  
		Last Modified: Tue, 30 Nov 2021 07:26:39 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663cc53ab2317558b9afc14f317845ab71678d9014ef8f4b455b76a1f5ad13b4`  
		Last Modified: Fri, 18 Feb 2022 22:26:29 GMT  
		Size: 11.8 MB (11771981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01091fd3e45df20547a10229a30b96d8cf5998dafc5a5815700834ea2a1cca9`  
		Last Modified: Fri, 18 Feb 2022 22:26:27 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7c08f08c396228976e471a184d4a94d00e1ffcdd366553305de7177eec3bec`  
		Last Modified: Fri, 11 Mar 2022 09:52:14 GMT  
		Size: 18.4 MB (18353518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e767c5a126e3cb62dc8dfdb265ab1b5cfefbbb4955aa58b9ca20fd4e9a3cb5d`  
		Last Modified: Fri, 11 Mar 2022 09:52:10 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a598088569767a94973057cabf1fdeb7dee736eeb4881b2a7e6f18a0c0f2807`  
		Last Modified: Fri, 11 Mar 2022 09:52:10 GMT  
		Size: 18.6 KB (18564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865b388f98b32bac5bade9ff004270a55a0e68d686465a2830ad43a6e6c1e699`  
		Last Modified: Fri, 11 Mar 2022 10:57:32 GMT  
		Size: 33.9 MB (33902882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f226452b0c1667229ee85c065083d8341b4750406d4809c2849e36b27a77a35`  
		Last Modified: Fri, 11 Mar 2022 10:57:25 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5f6fd27e5c402548636d63962e13de0ced945c9a6943a67c408ef6c18e071d`  
		Last Modified: Wed, 16 Mar 2022 18:44:00 GMT  
		Size: 4.5 MB (4498013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3fba9e19771a5ee851139d0b6465620f9acd7ed4f74a85eaaf86547836919f`  
		Last Modified: Wed, 16 Mar 2022 18:43:59 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec711f0032b76a073691ea34ea9edbcaeffecf203ca1ad55d6d2e712cdc6e9a`  
		Last Modified: Wed, 16 Mar 2022 18:43:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.2` - linux; s390x

```console
$ docker pull composer@sha256:4d6d35d1f21dd04ec59345df6103a538e2c87b72dba6bed4d4e510b75ce69301
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71633583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a7cdde9dd9c512ec61147343e6160697e2ce8a5ca240881238d801b6fad937`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:41:23 GMT
ADD file:cd24c711a2ef431b3ff94f9a02bfc42f159bc60de1d0eceecafea4e8af02441d in / 
# Wed, 24 Nov 2021 20:41:23 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:50:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 04:50:01 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 04:50:02 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 04:50:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 04:50:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 04:50:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 04:50:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 04:50:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 04:50:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:08:01 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:08:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:08:02 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:09:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:09:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:35:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 01:35:50 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:35:51 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 01:35:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 01:35:52 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 05:02:45 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 05:02:47 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 05:02:47 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 05:02:47 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 17:41:52 GMT
ENV COMPOSER_VERSION=2.2.9
# Wed, 16 Mar 2022 17:42:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 17:42:07 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 17:42:07 GMT
WORKDIR /app
# Wed, 16 Mar 2022 17:42:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 17:42:07 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d6baca485f3d0f7c77221be60fbef5db014a5ef9d8f53db4a310c947c690d189`  
		Last Modified: Wed, 24 Nov 2021 20:42:15 GMT  
		Size: 2.6 MB (2605944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079fbafa3afc04920b17b503e5d173a44e68fa743eddc7a0eca5e81c7572b8a2`  
		Last Modified: Tue, 30 Nov 2021 08:33:50 GMT  
		Size: 1.8 MB (1771410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ea1ee8ecbda317521ca15da3d8e45a369d74d9b70a0070ebd705cb9aaf88a2`  
		Last Modified: Tue, 30 Nov 2021 08:33:49 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abad577e66a4ab93646ed4a4aefb0579d577932add0d28121e5aece37cfc08dd`  
		Last Modified: Tue, 30 Nov 2021 08:33:49 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac62d72c92f8b14f9b5873207ef984e63eff6fec607db9d4330d9c8129c2925`  
		Last Modified: Fri, 18 Feb 2022 21:13:54 GMT  
		Size: 11.8 MB (11771995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074272c815254eeab42d6bbeac5cb89869166aa437afdace2d9b24a9aa028c4f`  
		Last Modified: Fri, 18 Feb 2022 21:13:53 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a400f11df7f6a7553c85e98fc344489885d2289da563949d00c5280b943f9d0b`  
		Last Modified: Fri, 11 Mar 2022 04:03:48 GMT  
		Size: 16.4 MB (16381073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560e4e59acf6107ca6529fb1d607beb5fe7518052fc9e159c1a89111422d0ed9`  
		Last Modified: Fri, 11 Mar 2022 04:03:46 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93e829bfc7fd232613ba9a365a7a92259718f51bf2ce8df42cf435a15dcc38f`  
		Last Modified: Fri, 11 Mar 2022 04:03:46 GMT  
		Size: 18.6 KB (18598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86bb1285cae11648274513dd55a891e1ca7f14ee80070d95daeae0521db77da`  
		Last Modified: Fri, 11 Mar 2022 05:03:53 GMT  
		Size: 34.9 MB (34887464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e94752314a819cf5f190758a33d2f4d2a3dbde007de6249f275621e5ef423f8`  
		Last Modified: Fri, 11 Mar 2022 05:03:49 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ffe7b695380f1c31a8200b263d206389b1cf9117d2a11fd0e6bfc24f1e942a`  
		Last Modified: Wed, 16 Mar 2022 17:42:49 GMT  
		Size: 4.2 MB (4191968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d40d17a09a360286b6e38702644ca38fb0c0726399c1ad778a4d9f6491eb518`  
		Last Modified: Wed, 16 Mar 2022 17:42:49 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8460fa71b15c5f0aa3bd56ccea29886a800bbb4642cb363ace43b94885fd7d`  
		Last Modified: Wed, 16 Mar 2022 17:42:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `composer:2.2.9`

```console
$ docker pull composer@sha256:761083bb446357e8ae40438dc32ec74992aaa3f295a5c76a2c19c0b5703d3c61
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

### `composer:2.2.9` - linux; amd64

```console
$ docker pull composer@sha256:326e28cdb766579a1e9088d0644f5fbd35fc3a21c4103a1f3e57b24dacfac220
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73039521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa6a91d32046c9419a0bdb982817ae30ee35f1a7a0cd9c13462581eba5ab3de2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 07:06:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 07:06:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 07:06:04 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 07:06:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 07:06:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 07:06:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 07:06:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 07:06:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 07:06:06 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:16:49 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:16:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:16:50 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:17:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:17:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:06:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 04:06:01 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:06:03 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 04:06:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 04:06:03 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 11:55:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 11:55:50 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 11:55:50 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 11:55:50 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 18:19:43 GMT
ENV COMPOSER_VERSION=2.2.9
# Wed, 16 Mar 2022 18:20:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 18:20:03 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 18:20:03 GMT
WORKDIR /app
# Wed, 16 Mar 2022 18:20:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 18:20:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7da25b2876b1c935b05d7e6efa3e8cd559d031cf30b246d7659ed438726acd`  
		Last Modified: Tue, 30 Nov 2021 09:03:50 GMT  
		Size: 1.7 MB (1709704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc599114627e3bd98e0204b93b161e03065bf9a228bb02ae202469655f12b8d`  
		Last Modified: Tue, 30 Nov 2021 09:03:48 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927a0b37a45a98d7d74a6d7d1567230eca834fb89417274557de7986d1f39401`  
		Last Modified: Tue, 30 Nov 2021 09:03:48 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e721f6667a5183c40af8377b3c611b535e9f4eaac41ad37954cc557c4d606dfd`  
		Last Modified: Fri, 18 Feb 2022 23:00:29 GMT  
		Size: 11.8 MB (11771990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdbed47885a29ebdc56f05207500027b26f268bdc5d034f8a6ca8fb34afab54`  
		Last Modified: Fri, 18 Feb 2022 23:00:28 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16135939cf41586188ad9ce6d0b22a1c609842cfcc8f7cb07b9e6db2730c2b37`  
		Last Modified: Fri, 11 Mar 2022 11:16:46 GMT  
		Size: 17.7 MB (17687791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb0fc4c5a6959679cb69633cfe546c6bda81fa74e7a34c9745aeb04921189c5`  
		Last Modified: Fri, 11 Mar 2022 11:16:43 GMT  
		Size: 2.3 KB (2301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37886f8b09348b24b4d10650f01acb3b0517e7d2a69a618c4c87bd1b4ba3df4`  
		Last Modified: Fri, 11 Mar 2022 11:16:43 GMT  
		Size: 18.8 KB (18777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b857d06f2e595fd88321d0fc2350c7811cf2c17127d1039997cb866237878e4d`  
		Last Modified: Fri, 11 Mar 2022 11:56:53 GMT  
		Size: 34.7 MB (34651834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f14b3f6c787d8ee1c2dc4cd24bfecab102e42b082163a5d45722d4e5e22780b`  
		Last Modified: Fri, 11 Mar 2022 11:56:47 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9614584564fb02a9e2f0e3d4654e34a4d5abecf123cc3ef1b490adce6ea509ac`  
		Last Modified: Wed, 16 Mar 2022 18:20:32 GMT  
		Size: 4.4 MB (4375884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2886923f9475c3d778e25d311f8c10e561f965b20bfba4273336a084abc32a5b`  
		Last Modified: Wed, 16 Mar 2022 18:20:30 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5a0cfeadcf4811a573924b6c4ba4df07e7e3c0267838f645a500ad5c2f7535`  
		Last Modified: Wed, 16 Mar 2022 18:20:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.2.9` - linux; arm variant v6

```console
$ docker pull composer@sha256:b6e2de2d5fb63d8e0e314e6d15e1d8eafd7e743c35c9a70bbe4104779f3c9f6b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68400844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acbd8d6d516db4b6ee4c8870d6e9af74da75ab99c426a8109e947161e5ecb850`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 03:20:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 03:20:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 03:20:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 03:20:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 03:20:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 03:20:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 03:20:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 03:20:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 03:20:12 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 19:50:06 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 19:50:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 19:50:07 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 19:50:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 19:50:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:16:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 01:16:18 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:16:21 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 01:16:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 01:16:22 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 04:31:45 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 04:31:47 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 04:31:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 04:31:48 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 18:08:58 GMT
ENV COMPOSER_VERSION=2.2.9
# Wed, 16 Mar 2022 18:09:45 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 18:09:46 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 18:09:46 GMT
WORKDIR /app
# Wed, 16 Mar 2022 18:09:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 18:09:47 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289be6d758ff0faa38d64732e5736031f2250cbf78d1ca4b32abba4accd6a3fa`  
		Last Modified: Tue, 30 Nov 2021 04:29:36 GMT  
		Size: 1.7 MB (1698826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0b442a0f679dba79aa838c408cf49916ca26d27e1252e26f3904d7c5b83d6c`  
		Last Modified: Tue, 30 Nov 2021 04:29:33 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef02b1cade59fbcc24c0ee972dd15d8caa89dda554cdb8aa742de1c6f3d5b7c`  
		Last Modified: Tue, 30 Nov 2021 04:29:33 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452d0467a92abee019a5ea9cdd7cf7b52fb629aa35a045df70339fb93b634760`  
		Last Modified: Fri, 18 Feb 2022 20:43:48 GMT  
		Size: 11.8 MB (11771982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e48b13f55f3236500af7e58ba05199b7acf9a4d62bc99270797ca5f5c1bc88`  
		Last Modified: Fri, 18 Feb 2022 20:43:45 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59c13e75cc1f96edac01b31ca5bf7f47552e1b3662911082d1926896e971fa4`  
		Last Modified: Fri, 11 Mar 2022 03:24:45 GMT  
		Size: 16.0 MB (16031967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0e34d07dc9c018a0df930e952b25876b7c0168a21c1a5a41e366c8103313b7`  
		Last Modified: Fri, 11 Mar 2022 03:24:38 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139e94b314f0a7968bb009c6b624a733bc8b17cde4cc3c5fb98883a957793045`  
		Last Modified: Fri, 11 Mar 2022 03:24:38 GMT  
		Size: 18.6 KB (18571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f789c188a53299f824e7c04be763e79c5b526773d8151b1e07b136bcde02fe78`  
		Last Modified: Fri, 11 Mar 2022 04:34:52 GMT  
		Size: 32.1 MB (32141861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ff5480814d31ae5b439e71effe3a89f8726a82b5f9531c24575c309aa5b802`  
		Last Modified: Fri, 11 Mar 2022 04:34:29 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d9913925d9bc064600a02965ab181c57ee38bcf13ae2b8fca5f5ceb49a6f09`  
		Last Modified: Wed, 16 Mar 2022 18:11:06 GMT  
		Size: 4.1 MB (4101086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee747280ba0407bc5a9ac0a76248042a687be679e269721b28ee8720135d6e29`  
		Last Modified: Wed, 16 Mar 2022 18:11:03 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f7208db20f07db348936636dd910d9c20b944a6585b4a5250e9187492e5694`  
		Last Modified: Wed, 16 Mar 2022 18:11:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.2.9` - linux; arm variant v7

```console
$ docker pull composer@sha256:8e7985450dd6157d802db9b8486af01981b5d6f0bfd0577437d32b7f6f98543f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65134499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c848ee419322351ac7186825962f5c9118465091a1f2cc0fd1ae0df13011133`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 05:27:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 05:27:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 05:27:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 05:27:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 05:27:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 05:27:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:27:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:27:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 05:27:21 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:43:09 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:43:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:43:09 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:43:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:43:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 02:43:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 02:43:15 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 02:43:17 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 02:43:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 02:43:18 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 12:13:42 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 12:13:44 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 12:13:44 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 12:13:45 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 17:58:36 GMT
ENV COMPOSER_VERSION=2.2.9
# Wed, 16 Mar 2022 17:59:22 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 17:59:22 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 17:59:23 GMT
WORKDIR /app
# Wed, 16 Mar 2022 17:59:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 17:59:24 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484fe107211badcebee7c4211e5ed91c7e5212cdd6d7edbb292a63ec60572bdd`  
		Last Modified: Tue, 30 Nov 2021 06:57:00 GMT  
		Size: 1.6 MB (1568802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93353d0a7113f37ba224b9ee296684e49f27c1c9440d3a3c5d310749213da97f`  
		Last Modified: Tue, 30 Nov 2021 06:56:59 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137db50a58959a68358c190d2a143088b82ab25d97cb889876fbc0728e446058`  
		Last Modified: Tue, 30 Nov 2021 06:57:00 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122d3a581986e22d7617f0ef2245bcb64b2a87ebcfe58b7b6d143561ce0cc8b2`  
		Last Modified: Fri, 18 Feb 2022 22:37:27 GMT  
		Size: 11.8 MB (11771980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc11ce0d4bdb5fcdda54f9da2a0eb1e4751b77e354a0dcdb827def3ff59f9f6`  
		Last Modified: Fri, 18 Feb 2022 22:37:24 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1951768145bebb84adba11b1ccd77c8d3802784df6c56f3ae141c103ac114c35`  
		Last Modified: Fri, 11 Mar 2022 07:38:53 GMT  
		Size: 15.0 MB (15034421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fdf84bb546f4d33ce7fff41672c1959df0ef457af702871c4ca3e4d585d8d87`  
		Last Modified: Fri, 11 Mar 2022 07:38:43 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164a1f0370d8b9c1f9c97a1a5aa3993986015fbe893874af94b911c5b8b06870`  
		Last Modified: Fri, 11 Mar 2022 07:38:43 GMT  
		Size: 18.6 KB (18569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b3d0ba165529b585fb1997f3fbc2d14dac5ccff866a44bff4b22578e6bd6aa`  
		Last Modified: Fri, 11 Mar 2022 12:16:34 GMT  
		Size: 30.5 MB (30471948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8e62f6bd555ee3d4b4ee22e2664dad7d5e0053556763e911676f59e8430be7`  
		Last Modified: Fri, 11 Mar 2022 12:16:14 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07eddbcbd7af52d2f868be4e78de819baaed038b501271a2500ac2fc4bba53b`  
		Last Modified: Wed, 16 Mar 2022 18:00:42 GMT  
		Size: 3.8 MB (3828887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbc1e6568bb9b37f50762a3378bd8a25055ac9fbaf11ec2d43c94234987698c`  
		Last Modified: Wed, 16 Mar 2022 18:00:40 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3da75e4905627fccb6521ac3f1c1b93c66ffbdb7a662f25ce6db75903277cf`  
		Last Modified: Wed, 16 Mar 2022 18:00:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.2.9` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:88ecf252d0fa4c6321e415dbda78934f3296272312613f11a68fcf0eaf357307
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71007032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5390a7677c7fd8300733ca205ed96ed73dd9de3e515d30be30a61725a621364f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 02:50:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 02:50:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 02:50:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 02:50:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 02:50:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 02:50:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 02:50:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 02:50:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 02:50:54 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:18:23 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:18:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:18:25 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:19:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:19:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:18:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 03:18:52 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:18:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 03:18:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 03:18:55 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 10:35:18 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 10:35:18 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 10:35:19 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 10:35:20 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 17:40:22 GMT
ENV COMPOSER_VERSION=2.2.9
# Wed, 16 Mar 2022 17:40:45 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 17:40:46 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 17:40:46 GMT
WORKDIR /app
# Wed, 16 Mar 2022 17:40:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 17:40:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd720d9f53003155e4cfe3f1974fc0e4d74a622ea8c61cfccb00ee8b842c09b6`  
		Last Modified: Tue, 30 Nov 2021 03:59:34 GMT  
		Size: 1.7 MB (1708308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680efee530f3c970c3140b358d3dc583ded463f9adbadb737ca64c765cf997ee`  
		Last Modified: Tue, 30 Nov 2021 03:59:33 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643d01251bc949843dbd734a37e7cf28a01af4ea11443738b8b92d17e1e438de`  
		Last Modified: Tue, 30 Nov 2021 03:59:33 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbd0dff840aec18863650b4a5db905ad8e50c878c0d1f6c4c1634d0a4743ae4`  
		Last Modified: Fri, 18 Feb 2022 21:39:27 GMT  
		Size: 11.8 MB (11771755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6104c5a569f57122fffc091a5376f51c0848737cec9feaa9a82531e6c2da43`  
		Last Modified: Fri, 18 Feb 2022 21:39:26 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf59a8a0ffa368fdd033e0104d93a4b4913881c7f6bd86aaef35c541233a018`  
		Last Modified: Fri, 11 Mar 2022 09:48:26 GMT  
		Size: 17.5 MB (17546174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef08d98d3666360bd8cbe19dcb81037d75a8aca59ebcfd386287fccb05cc9aab`  
		Last Modified: Fri, 11 Mar 2022 09:48:22 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e7653a3be11ae60976b3f56b5349443e6c458f125a944ba93d234548413851`  
		Last Modified: Fri, 11 Mar 2022 09:48:22 GMT  
		Size: 18.5 KB (18487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f017cf68653c976946e3d237367accaca773a59fbfae998075a1dfc4d6703911`  
		Last Modified: Fri, 11 Mar 2022 10:36:49 GMT  
		Size: 33.0 MB (33001745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0c25578ca0b4f7b253053edcefd8aaea561ada9282ced6617c66749e3cbd4e`  
		Last Modified: Fri, 11 Mar 2022 10:36:44 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f681d2af1a050fe7840d4cedae9568fa0ae020ab2860070fe7031503578ab40`  
		Last Modified: Wed, 16 Mar 2022 17:42:26 GMT  
		Size: 4.2 MB (4240106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94edf64a4261df8ee69484e617d69127d0c311998bad01d1e3e4556ff3dcc8ca`  
		Last Modified: Wed, 16 Mar 2022 17:42:25 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7a0434d0b212ef33c720406d8f0808fa9dda1fe4160e791da97681d4edaffc`  
		Last Modified: Wed, 16 Mar 2022 17:42:25 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.2.9` - linux; 386

```console
$ docker pull composer@sha256:a2477b4f8e6288b6cfdd1cabc3eed000d8e511fe967addb5a379e5f5887db17b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.4 MB (54414804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d7adaf71922c61637b4fcc20a8d11cb2062b357ac1cb0149ed700ee5f50bb7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:53:48 GMT
ADD file:b9a17131c440053f2f67e127b447645f25fd7de2d6caca42f569cafab6291855 in / 
# Wed, 24 Nov 2021 20:53:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 05:59:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 05:59:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 05:59:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 05:59:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 05:59:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 05:59:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:59:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:59:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 05:59:11 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:49:36 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:49:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:49:37 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:50:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:50:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:42:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 04:42:32 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:42:33 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 04:42:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 04:42:33 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 14:29:16 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 14:29:16 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 14:29:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 14:29:17 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 17:39:59 GMT
ENV COMPOSER_VERSION=2.2.9
# Wed, 16 Mar 2022 17:40:24 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 17:40:26 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 17:40:27 GMT
WORKDIR /app
# Wed, 16 Mar 2022 17:40:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 17:40:27 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:e6889e0d66307a4b916fc844f2dcbc03245c63bc4189dd3e88126d9dcf2f9231`  
		Last Modified: Wed, 24 Nov 2021 20:54:48 GMT  
		Size: 2.8 MB (2827117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d6acd3b6e4278a7b3ef37d3525813808468237f086215b68594b244dbd1fba`  
		Last Modified: Tue, 30 Nov 2021 08:26:15 GMT  
		Size: 1.8 MB (1810453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc53af545b93519336bed63b8765255ac8280e27c8e3a17c336f92526b3f290`  
		Last Modified: Tue, 30 Nov 2021 08:26:14 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d406b6d62c3d67bec5f638d47d2b1b49c0ee41d80a791a1b90eaec776cf4fd`  
		Last Modified: Tue, 30 Nov 2021 08:26:13 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09947cbaa6ea94c09911bac9f42ad67e560858bcf313330c30a51d4e047debcc`  
		Last Modified: Fri, 18 Feb 2022 23:36:11 GMT  
		Size: 11.8 MB (11771980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418d95d8e7f7c7a6bca99de67f7268f3c2bd9f90ac05ded2056aca5dcfcf42f3`  
		Last Modified: Fri, 18 Feb 2022 23:36:09 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe93a8e5de6a995b340c34f3b0c9926bbfb8314a31f31edd9aeecf49431cee4`  
		Last Modified: Fri, 11 Mar 2022 11:59:00 GMT  
		Size: 18.0 MB (18045807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98142bd532dfb18d7144d8a1bf1c7a641e931c169b4d2e1863e890a7f1b8e42d`  
		Last Modified: Fri, 11 Mar 2022 11:58:55 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e86e6cc1686366ee83df3ef2c5f3a0405af922746fd6d7ad4fd411ce9a77da`  
		Last Modified: Fri, 11 Mar 2022 11:58:55 GMT  
		Size: 18.8 KB (18773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765d3379030a7d7c59596ec428386624a93faadc763120bcb58cd721522baa8e`  
		Last Modified: Fri, 11 Mar 2022 14:30:44 GMT  
		Size: 15.6 MB (15590818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efdf8175c4916376f3518dfce254d9d6655bbb9cdf549acdfc253419b6d70b0`  
		Last Modified: Fri, 11 Mar 2022 14:30:41 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66086ccb543f409dbb0372048314fc39072d900a3b36b3efaf8e886310fc456`  
		Last Modified: Wed, 16 Mar 2022 17:41:30 GMT  
		Size: 4.3 MB (4344725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977603e326a453ec883002a965684daaf1f2b8495410041064afb673231e6433`  
		Last Modified: Wed, 16 Mar 2022 17:41:28 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c4920c285cadc297fb006fb893ba20057f8f86ef9dac2afce0f0c2d331aa46`  
		Last Modified: Wed, 16 Mar 2022 17:41:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.2.9` - linux; ppc64le

```console
$ docker pull composer@sha256:bce9ee868315f50bf13b33b49d5743c5bc838bc6730b13f13e1a67d939ab56fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73121143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a1d96d152754d33c266b566e0b7790f6bfb37ba43e15b6845c8354832816c8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:20:16 GMT
ADD file:57115dca2eb707f46b6301e75174e6aa316fb02ac28643b91429b75be51bd8c8 in / 
# Wed, 24 Nov 2021 20:20:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 06:02:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 06:03:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 06:03:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 06:03:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 06:03:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 06:03:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 06:03:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 06:04:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 06:04:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:19:05 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:19:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:19:10 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:19:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:19:44 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:41:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 03:41:38 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:41:46 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 03:41:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 03:41:52 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 10:53:22 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 10:53:41 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 10:53:45 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 10:53:51 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 18:29:39 GMT
ENV COMPOSER_VERSION=2.2.9
# Wed, 16 Mar 2022 18:30:52 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 18:31:59 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 18:32:57 GMT
WORKDIR /app
# Wed, 16 Mar 2022 18:34:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 18:35:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:159b5dcb1717c815c76ff5ea1db730e18e8609c9090238e43282856db9e71f47`  
		Last Modified: Wed, 24 Nov 2021 20:21:14 GMT  
		Size: 2.8 MB (2814780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603762061fb50079a4b6eb13347fd9a84cc1456d628cf781c89924a54bc419c1`  
		Last Modified: Tue, 30 Nov 2021 07:26:39 GMT  
		Size: 1.8 MB (1756276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645c08440cfaddc2735de2e28697acff0bc71db4cc7242494a44f92c94134e32`  
		Last Modified: Tue, 30 Nov 2021 07:26:39 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5de97a9a329d566f48c2edce253e4ccda6f021041e92326728b7499d13c823b`  
		Last Modified: Tue, 30 Nov 2021 07:26:39 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663cc53ab2317558b9afc14f317845ab71678d9014ef8f4b455b76a1f5ad13b4`  
		Last Modified: Fri, 18 Feb 2022 22:26:29 GMT  
		Size: 11.8 MB (11771981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01091fd3e45df20547a10229a30b96d8cf5998dafc5a5815700834ea2a1cca9`  
		Last Modified: Fri, 18 Feb 2022 22:26:27 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7c08f08c396228976e471a184d4a94d00e1ffcdd366553305de7177eec3bec`  
		Last Modified: Fri, 11 Mar 2022 09:52:14 GMT  
		Size: 18.4 MB (18353518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e767c5a126e3cb62dc8dfdb265ab1b5cfefbbb4955aa58b9ca20fd4e9a3cb5d`  
		Last Modified: Fri, 11 Mar 2022 09:52:10 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a598088569767a94973057cabf1fdeb7dee736eeb4881b2a7e6f18a0c0f2807`  
		Last Modified: Fri, 11 Mar 2022 09:52:10 GMT  
		Size: 18.6 KB (18564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865b388f98b32bac5bade9ff004270a55a0e68d686465a2830ad43a6e6c1e699`  
		Last Modified: Fri, 11 Mar 2022 10:57:32 GMT  
		Size: 33.9 MB (33902882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f226452b0c1667229ee85c065083d8341b4750406d4809c2849e36b27a77a35`  
		Last Modified: Fri, 11 Mar 2022 10:57:25 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5f6fd27e5c402548636d63962e13de0ced945c9a6943a67c408ef6c18e071d`  
		Last Modified: Wed, 16 Mar 2022 18:44:00 GMT  
		Size: 4.5 MB (4498013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3fba9e19771a5ee851139d0b6465620f9acd7ed4f74a85eaaf86547836919f`  
		Last Modified: Wed, 16 Mar 2022 18:43:59 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec711f0032b76a073691ea34ea9edbcaeffecf203ca1ad55d6d2e712cdc6e9a`  
		Last Modified: Wed, 16 Mar 2022 18:43:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.2.9` - linux; s390x

```console
$ docker pull composer@sha256:4d6d35d1f21dd04ec59345df6103a538e2c87b72dba6bed4d4e510b75ce69301
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71633583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a7cdde9dd9c512ec61147343e6160697e2ce8a5ca240881238d801b6fad937`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:41:23 GMT
ADD file:cd24c711a2ef431b3ff94f9a02bfc42f159bc60de1d0eceecafea4e8af02441d in / 
# Wed, 24 Nov 2021 20:41:23 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:50:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 04:50:01 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 04:50:02 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 04:50:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 04:50:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 04:50:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 04:50:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 04:50:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 04:50:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:08:01 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:08:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:08:02 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:09:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:09:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:35:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 01:35:50 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:35:51 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 01:35:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 01:35:52 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 05:02:45 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 05:02:47 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 05:02:47 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 05:02:47 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 17:41:52 GMT
ENV COMPOSER_VERSION=2.2.9
# Wed, 16 Mar 2022 17:42:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 17:42:07 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 17:42:07 GMT
WORKDIR /app
# Wed, 16 Mar 2022 17:42:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 17:42:07 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d6baca485f3d0f7c77221be60fbef5db014a5ef9d8f53db4a310c947c690d189`  
		Last Modified: Wed, 24 Nov 2021 20:42:15 GMT  
		Size: 2.6 MB (2605944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079fbafa3afc04920b17b503e5d173a44e68fa743eddc7a0eca5e81c7572b8a2`  
		Last Modified: Tue, 30 Nov 2021 08:33:50 GMT  
		Size: 1.8 MB (1771410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ea1ee8ecbda317521ca15da3d8e45a369d74d9b70a0070ebd705cb9aaf88a2`  
		Last Modified: Tue, 30 Nov 2021 08:33:49 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abad577e66a4ab93646ed4a4aefb0579d577932add0d28121e5aece37cfc08dd`  
		Last Modified: Tue, 30 Nov 2021 08:33:49 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac62d72c92f8b14f9b5873207ef984e63eff6fec607db9d4330d9c8129c2925`  
		Last Modified: Fri, 18 Feb 2022 21:13:54 GMT  
		Size: 11.8 MB (11771995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074272c815254eeab42d6bbeac5cb89869166aa437afdace2d9b24a9aa028c4f`  
		Last Modified: Fri, 18 Feb 2022 21:13:53 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a400f11df7f6a7553c85e98fc344489885d2289da563949d00c5280b943f9d0b`  
		Last Modified: Fri, 11 Mar 2022 04:03:48 GMT  
		Size: 16.4 MB (16381073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560e4e59acf6107ca6529fb1d607beb5fe7518052fc9e159c1a89111422d0ed9`  
		Last Modified: Fri, 11 Mar 2022 04:03:46 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93e829bfc7fd232613ba9a365a7a92259718f51bf2ce8df42cf435a15dcc38f`  
		Last Modified: Fri, 11 Mar 2022 04:03:46 GMT  
		Size: 18.6 KB (18598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86bb1285cae11648274513dd55a891e1ca7f14ee80070d95daeae0521db77da`  
		Last Modified: Fri, 11 Mar 2022 05:03:53 GMT  
		Size: 34.9 MB (34887464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e94752314a819cf5f190758a33d2f4d2a3dbde007de6249f275621e5ef423f8`  
		Last Modified: Fri, 11 Mar 2022 05:03:49 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ffe7b695380f1c31a8200b263d206389b1cf9117d2a11fd0e6bfc24f1e942a`  
		Last Modified: Wed, 16 Mar 2022 17:42:49 GMT  
		Size: 4.2 MB (4191968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d40d17a09a360286b6e38702644ca38fb0c0726399c1ad778a4d9f6491eb518`  
		Last Modified: Wed, 16 Mar 2022 17:42:49 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8460fa71b15c5f0aa3bd56ccea29886a800bbb4642cb363ace43b94885fd7d`  
		Last Modified: Wed, 16 Mar 2022 17:42:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `composer:2.3`

```console
$ docker pull composer@sha256:f691c44b59c7f4020f6a3c9ecfee95832855d38b98db441e635401c7e24c2381
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

### `composer:2.3` - linux; amd64

```console
$ docker pull composer@sha256:13adf9cda806d3bed05301d3fd5c2cf3db117f7dc1f414ba62375137bcfd4e26
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73120606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:239dc2c47aa1e3173ae5189ec4d132441195fc178ad48c7a1cfedb6eef489d96`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 07:06:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 07:06:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 07:06:04 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 07:06:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 07:06:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 07:06:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 07:06:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 07:06:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 07:06:06 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:16:49 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:16:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:16:50 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:17:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:17:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:06:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 04:06:01 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:06:03 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 04:06:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 04:06:03 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 11:55:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 11:55:50 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 11:55:50 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 11:55:50 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 18:19:20 GMT
ENV COMPOSER_VERSION=2.3.0-RC1
# Wed, 16 Mar 2022 18:19:40 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 18:19:40 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 18:19:40 GMT
WORKDIR /app
# Wed, 16 Mar 2022 18:19:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 18:19:41 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7da25b2876b1c935b05d7e6efa3e8cd559d031cf30b246d7659ed438726acd`  
		Last Modified: Tue, 30 Nov 2021 09:03:50 GMT  
		Size: 1.7 MB (1709704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc599114627e3bd98e0204b93b161e03065bf9a228bb02ae202469655f12b8d`  
		Last Modified: Tue, 30 Nov 2021 09:03:48 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927a0b37a45a98d7d74a6d7d1567230eca834fb89417274557de7986d1f39401`  
		Last Modified: Tue, 30 Nov 2021 09:03:48 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e721f6667a5183c40af8377b3c611b535e9f4eaac41ad37954cc557c4d606dfd`  
		Last Modified: Fri, 18 Feb 2022 23:00:29 GMT  
		Size: 11.8 MB (11771990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdbed47885a29ebdc56f05207500027b26f268bdc5d034f8a6ca8fb34afab54`  
		Last Modified: Fri, 18 Feb 2022 23:00:28 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16135939cf41586188ad9ce6d0b22a1c609842cfcc8f7cb07b9e6db2730c2b37`  
		Last Modified: Fri, 11 Mar 2022 11:16:46 GMT  
		Size: 17.7 MB (17687791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb0fc4c5a6959679cb69633cfe546c6bda81fa74e7a34c9745aeb04921189c5`  
		Last Modified: Fri, 11 Mar 2022 11:16:43 GMT  
		Size: 2.3 KB (2301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37886f8b09348b24b4d10650f01acb3b0517e7d2a69a618c4c87bd1b4ba3df4`  
		Last Modified: Fri, 11 Mar 2022 11:16:43 GMT  
		Size: 18.8 KB (18777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b857d06f2e595fd88321d0fc2350c7811cf2c17127d1039997cb866237878e4d`  
		Last Modified: Fri, 11 Mar 2022 11:56:53 GMT  
		Size: 34.7 MB (34651834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f14b3f6c787d8ee1c2dc4cd24bfecab102e42b082163a5d45722d4e5e22780b`  
		Last Modified: Fri, 11 Mar 2022 11:56:47 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7463da7dd5067266aa956ad2ccf966a8f83a482f8ad754d59e8e182d465a28b6`  
		Last Modified: Wed, 16 Mar 2022 18:20:20 GMT  
		Size: 4.5 MB (4456970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70cb24765e134712e18ef93088ae8496c9a969bdfdf23df465cc63f67f8a7325`  
		Last Modified: Wed, 16 Mar 2022 18:20:19 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cafd35b0778ecd4e2f7bca8166ce5179d6d3df1acb73d9a39b1a9cc7b02dbd05`  
		Last Modified: Wed, 16 Mar 2022 18:20:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.3` - linux; arm variant v6

```console
$ docker pull composer@sha256:a45a61ed845032e912d1d9e3b58580ca794925c42eb4661b1acdddd5845ab9bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68484732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1e44520692b17c13a178081aef48422d98a92cbc27f9535231c99d8845a109`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 03:20:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 03:20:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 03:20:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 03:20:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 03:20:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 03:20:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 03:20:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 03:20:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 03:20:12 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 19:50:06 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 19:50:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 19:50:07 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 19:50:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 19:50:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:16:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 01:16:18 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:16:21 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 01:16:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 01:16:22 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 04:31:45 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 04:31:47 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 04:31:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 04:31:48 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 18:07:50 GMT
ENV COMPOSER_VERSION=2.3.0-RC1
# Wed, 16 Mar 2022 18:08:39 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 18:08:39 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 18:08:40 GMT
WORKDIR /app
# Wed, 16 Mar 2022 18:08:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 18:08:40 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289be6d758ff0faa38d64732e5736031f2250cbf78d1ca4b32abba4accd6a3fa`  
		Last Modified: Tue, 30 Nov 2021 04:29:36 GMT  
		Size: 1.7 MB (1698826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0b442a0f679dba79aa838c408cf49916ca26d27e1252e26f3904d7c5b83d6c`  
		Last Modified: Tue, 30 Nov 2021 04:29:33 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef02b1cade59fbcc24c0ee972dd15d8caa89dda554cdb8aa742de1c6f3d5b7c`  
		Last Modified: Tue, 30 Nov 2021 04:29:33 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452d0467a92abee019a5ea9cdd7cf7b52fb629aa35a045df70339fb93b634760`  
		Last Modified: Fri, 18 Feb 2022 20:43:48 GMT  
		Size: 11.8 MB (11771982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e48b13f55f3236500af7e58ba05199b7acf9a4d62bc99270797ca5f5c1bc88`  
		Last Modified: Fri, 18 Feb 2022 20:43:45 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59c13e75cc1f96edac01b31ca5bf7f47552e1b3662911082d1926896e971fa4`  
		Last Modified: Fri, 11 Mar 2022 03:24:45 GMT  
		Size: 16.0 MB (16031967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0e34d07dc9c018a0df930e952b25876b7c0168a21c1a5a41e366c8103313b7`  
		Last Modified: Fri, 11 Mar 2022 03:24:38 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139e94b314f0a7968bb009c6b624a733bc8b17cde4cc3c5fb98883a957793045`  
		Last Modified: Fri, 11 Mar 2022 03:24:38 GMT  
		Size: 18.6 KB (18571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f789c188a53299f824e7c04be763e79c5b526773d8151b1e07b136bcde02fe78`  
		Last Modified: Fri, 11 Mar 2022 04:34:52 GMT  
		Size: 32.1 MB (32141861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ff5480814d31ae5b439e71effe3a89f8726a82b5f9531c24575c309aa5b802`  
		Last Modified: Fri, 11 Mar 2022 04:34:29 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87eef11f36277453e95e5e04b4e0c53616adff7b16cfa2c3a0f202857b7cdbc6`  
		Last Modified: Wed, 16 Mar 2022 18:10:52 GMT  
		Size: 4.2 MB (4184974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d46200e0e59bf95c71d670370339aee5cc29dee1583f4d1a307c3028df712a33`  
		Last Modified: Wed, 16 Mar 2022 18:10:49 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e1e8f3e4f2e2082ceecfb446a7bafd2b394b8107b6cbe6fd388a6b7a9ac2a6`  
		Last Modified: Wed, 16 Mar 2022 18:10:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.3` - linux; arm variant v7

```console
$ docker pull composer@sha256:176559eaf4ee1a70a995cb261246e204f001515058ede16606807d03eed0b722
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65220498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a372e3bc4b555966f201b91f38ec9064daed92f4c6914061906ac627f5200845`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 05:27:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 05:27:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 05:27:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 05:27:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 05:27:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 05:27:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:27:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:27:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 05:27:21 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:43:09 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:43:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:43:09 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:43:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:43:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 02:43:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 02:43:15 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 02:43:17 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 02:43:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 02:43:18 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 12:13:42 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 12:13:44 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 12:13:44 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 12:13:45 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 17:57:36 GMT
ENV COMPOSER_VERSION=2.3.0-RC1
# Wed, 16 Mar 2022 17:58:24 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 17:58:24 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 17:58:25 GMT
WORKDIR /app
# Wed, 16 Mar 2022 17:58:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 17:58:25 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484fe107211badcebee7c4211e5ed91c7e5212cdd6d7edbb292a63ec60572bdd`  
		Last Modified: Tue, 30 Nov 2021 06:57:00 GMT  
		Size: 1.6 MB (1568802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93353d0a7113f37ba224b9ee296684e49f27c1c9440d3a3c5d310749213da97f`  
		Last Modified: Tue, 30 Nov 2021 06:56:59 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137db50a58959a68358c190d2a143088b82ab25d97cb889876fbc0728e446058`  
		Last Modified: Tue, 30 Nov 2021 06:57:00 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122d3a581986e22d7617f0ef2245bcb64b2a87ebcfe58b7b6d143561ce0cc8b2`  
		Last Modified: Fri, 18 Feb 2022 22:37:27 GMT  
		Size: 11.8 MB (11771980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc11ce0d4bdb5fcdda54f9da2a0eb1e4751b77e354a0dcdb827def3ff59f9f6`  
		Last Modified: Fri, 18 Feb 2022 22:37:24 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1951768145bebb84adba11b1ccd77c8d3802784df6c56f3ae141c103ac114c35`  
		Last Modified: Fri, 11 Mar 2022 07:38:53 GMT  
		Size: 15.0 MB (15034421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fdf84bb546f4d33ce7fff41672c1959df0ef457af702871c4ca3e4d585d8d87`  
		Last Modified: Fri, 11 Mar 2022 07:38:43 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164a1f0370d8b9c1f9c97a1a5aa3993986015fbe893874af94b911c5b8b06870`  
		Last Modified: Fri, 11 Mar 2022 07:38:43 GMT  
		Size: 18.6 KB (18569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b3d0ba165529b585fb1997f3fbc2d14dac5ccff866a44bff4b22578e6bd6aa`  
		Last Modified: Fri, 11 Mar 2022 12:16:34 GMT  
		Size: 30.5 MB (30471948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8e62f6bd555ee3d4b4ee22e2664dad7d5e0053556763e911676f59e8430be7`  
		Last Modified: Fri, 11 Mar 2022 12:16:14 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e40e45c71d84f5ec5e74972e923f2d45fa9bcc02e977c9c12491d8ae26c4e8`  
		Last Modified: Wed, 16 Mar 2022 18:00:26 GMT  
		Size: 3.9 MB (3914887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d321b06f6260068a245cb554aa80ae72d6e3036bbdb57227ac6beab5e8a78c4e`  
		Last Modified: Wed, 16 Mar 2022 18:00:24 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d58f09e6c5918a7284b18c452b80a0ac8236fdc5192119a56304b73092a89a`  
		Last Modified: Wed, 16 Mar 2022 18:00:24 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.3` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:d28a8980feeace3cd7606dcdacf1b8a637bdc4b2077fea0a3be12cdaea7cc197
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71088907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03c55046830d3e7325f4e8be8939f1928123c47197c9ba4112686a5833dfa57`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 02:50:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 02:50:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 02:50:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 02:50:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 02:50:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 02:50:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 02:50:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 02:50:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 02:50:54 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:18:23 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:18:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:18:25 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:19:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:19:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:18:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 03:18:52 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:18:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 03:18:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 03:18:55 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 10:35:18 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 10:35:18 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 10:35:19 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 10:35:20 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 17:39:38 GMT
ENV COMPOSER_VERSION=2.3.0-RC1
# Wed, 16 Mar 2022 17:40:04 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 17:40:06 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 17:40:06 GMT
WORKDIR /app
# Wed, 16 Mar 2022 17:40:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 17:40:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd720d9f53003155e4cfe3f1974fc0e4d74a622ea8c61cfccb00ee8b842c09b6`  
		Last Modified: Tue, 30 Nov 2021 03:59:34 GMT  
		Size: 1.7 MB (1708308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680efee530f3c970c3140b358d3dc583ded463f9adbadb737ca64c765cf997ee`  
		Last Modified: Tue, 30 Nov 2021 03:59:33 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643d01251bc949843dbd734a37e7cf28a01af4ea11443738b8b92d17e1e438de`  
		Last Modified: Tue, 30 Nov 2021 03:59:33 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbd0dff840aec18863650b4a5db905ad8e50c878c0d1f6c4c1634d0a4743ae4`  
		Last Modified: Fri, 18 Feb 2022 21:39:27 GMT  
		Size: 11.8 MB (11771755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6104c5a569f57122fffc091a5376f51c0848737cec9feaa9a82531e6c2da43`  
		Last Modified: Fri, 18 Feb 2022 21:39:26 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf59a8a0ffa368fdd033e0104d93a4b4913881c7f6bd86aaef35c541233a018`  
		Last Modified: Fri, 11 Mar 2022 09:48:26 GMT  
		Size: 17.5 MB (17546174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef08d98d3666360bd8cbe19dcb81037d75a8aca59ebcfd386287fccb05cc9aab`  
		Last Modified: Fri, 11 Mar 2022 09:48:22 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e7653a3be11ae60976b3f56b5349443e6c458f125a944ba93d234548413851`  
		Last Modified: Fri, 11 Mar 2022 09:48:22 GMT  
		Size: 18.5 KB (18487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f017cf68653c976946e3d237367accaca773a59fbfae998075a1dfc4d6703911`  
		Last Modified: Fri, 11 Mar 2022 10:36:49 GMT  
		Size: 33.0 MB (33001745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0c25578ca0b4f7b253053edcefd8aaea561ada9282ced6617c66749e3cbd4e`  
		Last Modified: Fri, 11 Mar 2022 10:36:44 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6876702c43cd7a3fcf9c3c043d76e94ae1182a6c283bb7de9143d0a36947dcf4`  
		Last Modified: Wed, 16 Mar 2022 17:42:10 GMT  
		Size: 4.3 MB (4321981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc3b74e160374ef1a5650d312c31101d1fcd742421137929930d57c87b35eba`  
		Last Modified: Wed, 16 Mar 2022 17:42:09 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01582158b58c9ca1a13fa39a128fdd435efd2c4e4c089d56aff5a41257e77e96`  
		Last Modified: Wed, 16 Mar 2022 17:42:09 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.3` - linux; 386

```console
$ docker pull composer@sha256:64695c071f587bb4cf9c86fd18cd5c5049bba07dbfc39381e4928644386a3edd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54495598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4abe65a4105a50156eabfc20967e6ceba3eeb0a7d7cf421a945ded8375a1de`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:53:48 GMT
ADD file:b9a17131c440053f2f67e127b447645f25fd7de2d6caca42f569cafab6291855 in / 
# Wed, 24 Nov 2021 20:53:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 05:59:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 05:59:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 05:59:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 05:59:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 05:59:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 05:59:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:59:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:59:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 05:59:11 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:49:36 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:49:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:49:37 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:50:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:50:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:42:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 04:42:32 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:42:33 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 04:42:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 04:42:33 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 14:29:16 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 14:29:16 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 14:29:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 14:29:17 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 17:39:18 GMT
ENV COMPOSER_VERSION=2.3.0-RC1
# Wed, 16 Mar 2022 17:39:50 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 17:39:51 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 17:39:52 GMT
WORKDIR /app
# Wed, 16 Mar 2022 17:39:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 17:39:52 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:e6889e0d66307a4b916fc844f2dcbc03245c63bc4189dd3e88126d9dcf2f9231`  
		Last Modified: Wed, 24 Nov 2021 20:54:48 GMT  
		Size: 2.8 MB (2827117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d6acd3b6e4278a7b3ef37d3525813808468237f086215b68594b244dbd1fba`  
		Last Modified: Tue, 30 Nov 2021 08:26:15 GMT  
		Size: 1.8 MB (1810453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc53af545b93519336bed63b8765255ac8280e27c8e3a17c336f92526b3f290`  
		Last Modified: Tue, 30 Nov 2021 08:26:14 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d406b6d62c3d67bec5f638d47d2b1b49c0ee41d80a791a1b90eaec776cf4fd`  
		Last Modified: Tue, 30 Nov 2021 08:26:13 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09947cbaa6ea94c09911bac9f42ad67e560858bcf313330c30a51d4e047debcc`  
		Last Modified: Fri, 18 Feb 2022 23:36:11 GMT  
		Size: 11.8 MB (11771980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418d95d8e7f7c7a6bca99de67f7268f3c2bd9f90ac05ded2056aca5dcfcf42f3`  
		Last Modified: Fri, 18 Feb 2022 23:36:09 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe93a8e5de6a995b340c34f3b0c9926bbfb8314a31f31edd9aeecf49431cee4`  
		Last Modified: Fri, 11 Mar 2022 11:59:00 GMT  
		Size: 18.0 MB (18045807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98142bd532dfb18d7144d8a1bf1c7a641e931c169b4d2e1863e890a7f1b8e42d`  
		Last Modified: Fri, 11 Mar 2022 11:58:55 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e86e6cc1686366ee83df3ef2c5f3a0405af922746fd6d7ad4fd411ce9a77da`  
		Last Modified: Fri, 11 Mar 2022 11:58:55 GMT  
		Size: 18.8 KB (18773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765d3379030a7d7c59596ec428386624a93faadc763120bcb58cd721522baa8e`  
		Last Modified: Fri, 11 Mar 2022 14:30:44 GMT  
		Size: 15.6 MB (15590818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efdf8175c4916376f3518dfce254d9d6655bbb9cdf549acdfc253419b6d70b0`  
		Last Modified: Fri, 11 Mar 2022 14:30:41 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fede22822a011094dfe627d213b08d1b00e3d825b21f76bf12fc6df942d87b8`  
		Last Modified: Wed, 16 Mar 2022 17:41:17 GMT  
		Size: 4.4 MB (4425519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ccd4cbdbfcf6c5b16da6c7a8d2570c559ba7f4f77465e1f8a61912de14a105d`  
		Last Modified: Wed, 16 Mar 2022 17:41:16 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2756b5f499130fac4c3646d3bfed07287f74a5a45cce498be8117b44388bcca3`  
		Last Modified: Wed, 16 Mar 2022 17:41:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.3` - linux; ppc64le

```console
$ docker pull composer@sha256:5b8aad76b10bcc450bcb7738cac6c30a40450e0431abeddba2767c3a12233fe7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73201769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6818afe79d299b01a84e1c99294952de05f93a13a6f0205af04a8de519733224`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:20:16 GMT
ADD file:57115dca2eb707f46b6301e75174e6aa316fb02ac28643b91429b75be51bd8c8 in / 
# Wed, 24 Nov 2021 20:20:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 06:02:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 06:03:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 06:03:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 06:03:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 06:03:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 06:03:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 06:03:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 06:04:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 06:04:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:19:05 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:19:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:19:10 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:19:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:19:44 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:41:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 03:41:38 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:41:46 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 03:41:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 03:41:52 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 10:53:22 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 10:53:41 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 10:53:45 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 10:53:51 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 18:22:10 GMT
ENV COMPOSER_VERSION=2.3.0-RC1
# Wed, 16 Mar 2022 18:24:23 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 18:25:42 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 18:27:03 GMT
WORKDIR /app
# Wed, 16 Mar 2022 18:28:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 18:29:18 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:159b5dcb1717c815c76ff5ea1db730e18e8609c9090238e43282856db9e71f47`  
		Last Modified: Wed, 24 Nov 2021 20:21:14 GMT  
		Size: 2.8 MB (2814780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603762061fb50079a4b6eb13347fd9a84cc1456d628cf781c89924a54bc419c1`  
		Last Modified: Tue, 30 Nov 2021 07:26:39 GMT  
		Size: 1.8 MB (1756276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645c08440cfaddc2735de2e28697acff0bc71db4cc7242494a44f92c94134e32`  
		Last Modified: Tue, 30 Nov 2021 07:26:39 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5de97a9a329d566f48c2edce253e4ccda6f021041e92326728b7499d13c823b`  
		Last Modified: Tue, 30 Nov 2021 07:26:39 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663cc53ab2317558b9afc14f317845ab71678d9014ef8f4b455b76a1f5ad13b4`  
		Last Modified: Fri, 18 Feb 2022 22:26:29 GMT  
		Size: 11.8 MB (11771981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01091fd3e45df20547a10229a30b96d8cf5998dafc5a5815700834ea2a1cca9`  
		Last Modified: Fri, 18 Feb 2022 22:26:27 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7c08f08c396228976e471a184d4a94d00e1ffcdd366553305de7177eec3bec`  
		Last Modified: Fri, 11 Mar 2022 09:52:14 GMT  
		Size: 18.4 MB (18353518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e767c5a126e3cb62dc8dfdb265ab1b5cfefbbb4955aa58b9ca20fd4e9a3cb5d`  
		Last Modified: Fri, 11 Mar 2022 09:52:10 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a598088569767a94973057cabf1fdeb7dee736eeb4881b2a7e6f18a0c0f2807`  
		Last Modified: Fri, 11 Mar 2022 09:52:10 GMT  
		Size: 18.6 KB (18564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865b388f98b32bac5bade9ff004270a55a0e68d686465a2830ad43a6e6c1e699`  
		Last Modified: Fri, 11 Mar 2022 10:57:32 GMT  
		Size: 33.9 MB (33902882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f226452b0c1667229ee85c065083d8341b4750406d4809c2849e36b27a77a35`  
		Last Modified: Fri, 11 Mar 2022 10:57:25 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bbcdda71a0a491a662d64e7cc58bcea9f0bfd8fb1989e80201b518b5add73d1`  
		Last Modified: Wed, 16 Mar 2022 18:42:54 GMT  
		Size: 4.6 MB (4578641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4a26306c68820dea6a3aad156e9689e69e82efc817a27cf0d7df5fb39389e9`  
		Last Modified: Wed, 16 Mar 2022 18:42:53 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bcacb1d616c0be20b193343888377fea92720874f6c52a95d1c14b1c18b98c5`  
		Last Modified: Wed, 16 Mar 2022 18:42:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.3` - linux; s390x

```console
$ docker pull composer@sha256:f0fe2462f04eef77425d91d0cb442694aba0ea8388060ebfc214cbc74cc2a408
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71713541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c901553796688d43018ff61e57cfb9872e88302b1c96eadced584ab198e4d2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:41:23 GMT
ADD file:cd24c711a2ef431b3ff94f9a02bfc42f159bc60de1d0eceecafea4e8af02441d in / 
# Wed, 24 Nov 2021 20:41:23 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:50:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 04:50:01 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 04:50:02 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 04:50:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 04:50:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 04:50:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 04:50:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 04:50:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 04:50:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:08:01 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:08:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:08:02 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:09:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:09:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:35:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 01:35:50 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:35:51 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 01:35:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 01:35:52 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 05:02:45 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 05:02:47 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 05:02:47 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 05:02:47 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 17:41:26 GMT
ENV COMPOSER_VERSION=2.3.0-RC1
# Wed, 16 Mar 2022 17:41:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 17:41:44 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 17:41:44 GMT
WORKDIR /app
# Wed, 16 Mar 2022 17:41:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 17:41:44 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d6baca485f3d0f7c77221be60fbef5db014a5ef9d8f53db4a310c947c690d189`  
		Last Modified: Wed, 24 Nov 2021 20:42:15 GMT  
		Size: 2.6 MB (2605944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079fbafa3afc04920b17b503e5d173a44e68fa743eddc7a0eca5e81c7572b8a2`  
		Last Modified: Tue, 30 Nov 2021 08:33:50 GMT  
		Size: 1.8 MB (1771410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ea1ee8ecbda317521ca15da3d8e45a369d74d9b70a0070ebd705cb9aaf88a2`  
		Last Modified: Tue, 30 Nov 2021 08:33:49 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abad577e66a4ab93646ed4a4aefb0579d577932add0d28121e5aece37cfc08dd`  
		Last Modified: Tue, 30 Nov 2021 08:33:49 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac62d72c92f8b14f9b5873207ef984e63eff6fec607db9d4330d9c8129c2925`  
		Last Modified: Fri, 18 Feb 2022 21:13:54 GMT  
		Size: 11.8 MB (11771995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074272c815254eeab42d6bbeac5cb89869166aa437afdace2d9b24a9aa028c4f`  
		Last Modified: Fri, 18 Feb 2022 21:13:53 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a400f11df7f6a7553c85e98fc344489885d2289da563949d00c5280b943f9d0b`  
		Last Modified: Fri, 11 Mar 2022 04:03:48 GMT  
		Size: 16.4 MB (16381073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560e4e59acf6107ca6529fb1d607beb5fe7518052fc9e159c1a89111422d0ed9`  
		Last Modified: Fri, 11 Mar 2022 04:03:46 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93e829bfc7fd232613ba9a365a7a92259718f51bf2ce8df42cf435a15dcc38f`  
		Last Modified: Fri, 11 Mar 2022 04:03:46 GMT  
		Size: 18.6 KB (18598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86bb1285cae11648274513dd55a891e1ca7f14ee80070d95daeae0521db77da`  
		Last Modified: Fri, 11 Mar 2022 05:03:53 GMT  
		Size: 34.9 MB (34887464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e94752314a819cf5f190758a33d2f4d2a3dbde007de6249f275621e5ef423f8`  
		Last Modified: Fri, 11 Mar 2022 05:03:49 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6e068cca1d92d784bda7bd8cd0952ef00e2aefaf1e3fab39b16fd9773ad7bf`  
		Last Modified: Wed, 16 Mar 2022 17:42:42 GMT  
		Size: 4.3 MB (4271928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4bffcc6f3947556ed17fc494a3b6e03f9fa4533fca0a1260f0cf1d0a6416b0`  
		Last Modified: Wed, 16 Mar 2022 17:42:41 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292b934853dce308e94a118ceddc2f552369eada3185093816c0753022ed4406`  
		Last Modified: Wed, 16 Mar 2022 17:42:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `composer:2.3.0-RC1`

```console
$ docker pull composer@sha256:f691c44b59c7f4020f6a3c9ecfee95832855d38b98db441e635401c7e24c2381
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

### `composer:2.3.0-RC1` - linux; amd64

```console
$ docker pull composer@sha256:13adf9cda806d3bed05301d3fd5c2cf3db117f7dc1f414ba62375137bcfd4e26
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73120606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:239dc2c47aa1e3173ae5189ec4d132441195fc178ad48c7a1cfedb6eef489d96`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 07:06:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 07:06:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 07:06:04 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 07:06:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 07:06:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 07:06:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 07:06:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 07:06:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 07:06:06 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:16:49 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:16:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:16:50 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:17:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:17:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:06:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 04:06:01 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:06:03 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 04:06:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 04:06:03 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 11:55:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 11:55:50 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 11:55:50 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 11:55:50 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 18:19:20 GMT
ENV COMPOSER_VERSION=2.3.0-RC1
# Wed, 16 Mar 2022 18:19:40 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 18:19:40 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 18:19:40 GMT
WORKDIR /app
# Wed, 16 Mar 2022 18:19:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 18:19:41 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7da25b2876b1c935b05d7e6efa3e8cd559d031cf30b246d7659ed438726acd`  
		Last Modified: Tue, 30 Nov 2021 09:03:50 GMT  
		Size: 1.7 MB (1709704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc599114627e3bd98e0204b93b161e03065bf9a228bb02ae202469655f12b8d`  
		Last Modified: Tue, 30 Nov 2021 09:03:48 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927a0b37a45a98d7d74a6d7d1567230eca834fb89417274557de7986d1f39401`  
		Last Modified: Tue, 30 Nov 2021 09:03:48 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e721f6667a5183c40af8377b3c611b535e9f4eaac41ad37954cc557c4d606dfd`  
		Last Modified: Fri, 18 Feb 2022 23:00:29 GMT  
		Size: 11.8 MB (11771990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdbed47885a29ebdc56f05207500027b26f268bdc5d034f8a6ca8fb34afab54`  
		Last Modified: Fri, 18 Feb 2022 23:00:28 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16135939cf41586188ad9ce6d0b22a1c609842cfcc8f7cb07b9e6db2730c2b37`  
		Last Modified: Fri, 11 Mar 2022 11:16:46 GMT  
		Size: 17.7 MB (17687791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb0fc4c5a6959679cb69633cfe546c6bda81fa74e7a34c9745aeb04921189c5`  
		Last Modified: Fri, 11 Mar 2022 11:16:43 GMT  
		Size: 2.3 KB (2301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37886f8b09348b24b4d10650f01acb3b0517e7d2a69a618c4c87bd1b4ba3df4`  
		Last Modified: Fri, 11 Mar 2022 11:16:43 GMT  
		Size: 18.8 KB (18777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b857d06f2e595fd88321d0fc2350c7811cf2c17127d1039997cb866237878e4d`  
		Last Modified: Fri, 11 Mar 2022 11:56:53 GMT  
		Size: 34.7 MB (34651834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f14b3f6c787d8ee1c2dc4cd24bfecab102e42b082163a5d45722d4e5e22780b`  
		Last Modified: Fri, 11 Mar 2022 11:56:47 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7463da7dd5067266aa956ad2ccf966a8f83a482f8ad754d59e8e182d465a28b6`  
		Last Modified: Wed, 16 Mar 2022 18:20:20 GMT  
		Size: 4.5 MB (4456970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70cb24765e134712e18ef93088ae8496c9a969bdfdf23df465cc63f67f8a7325`  
		Last Modified: Wed, 16 Mar 2022 18:20:19 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cafd35b0778ecd4e2f7bca8166ce5179d6d3df1acb73d9a39b1a9cc7b02dbd05`  
		Last Modified: Wed, 16 Mar 2022 18:20:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.3.0-RC1` - linux; arm variant v6

```console
$ docker pull composer@sha256:a45a61ed845032e912d1d9e3b58580ca794925c42eb4661b1acdddd5845ab9bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68484732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1e44520692b17c13a178081aef48422d98a92cbc27f9535231c99d8845a109`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 03:20:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 03:20:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 03:20:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 03:20:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 03:20:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 03:20:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 03:20:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 03:20:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 03:20:12 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 19:50:06 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 19:50:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 19:50:07 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 19:50:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 19:50:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:16:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 01:16:18 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:16:21 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 01:16:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 01:16:22 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 04:31:45 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 04:31:47 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 04:31:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 04:31:48 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 18:07:50 GMT
ENV COMPOSER_VERSION=2.3.0-RC1
# Wed, 16 Mar 2022 18:08:39 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 18:08:39 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 18:08:40 GMT
WORKDIR /app
# Wed, 16 Mar 2022 18:08:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 18:08:40 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289be6d758ff0faa38d64732e5736031f2250cbf78d1ca4b32abba4accd6a3fa`  
		Last Modified: Tue, 30 Nov 2021 04:29:36 GMT  
		Size: 1.7 MB (1698826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0b442a0f679dba79aa838c408cf49916ca26d27e1252e26f3904d7c5b83d6c`  
		Last Modified: Tue, 30 Nov 2021 04:29:33 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef02b1cade59fbcc24c0ee972dd15d8caa89dda554cdb8aa742de1c6f3d5b7c`  
		Last Modified: Tue, 30 Nov 2021 04:29:33 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452d0467a92abee019a5ea9cdd7cf7b52fb629aa35a045df70339fb93b634760`  
		Last Modified: Fri, 18 Feb 2022 20:43:48 GMT  
		Size: 11.8 MB (11771982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e48b13f55f3236500af7e58ba05199b7acf9a4d62bc99270797ca5f5c1bc88`  
		Last Modified: Fri, 18 Feb 2022 20:43:45 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59c13e75cc1f96edac01b31ca5bf7f47552e1b3662911082d1926896e971fa4`  
		Last Modified: Fri, 11 Mar 2022 03:24:45 GMT  
		Size: 16.0 MB (16031967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0e34d07dc9c018a0df930e952b25876b7c0168a21c1a5a41e366c8103313b7`  
		Last Modified: Fri, 11 Mar 2022 03:24:38 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139e94b314f0a7968bb009c6b624a733bc8b17cde4cc3c5fb98883a957793045`  
		Last Modified: Fri, 11 Mar 2022 03:24:38 GMT  
		Size: 18.6 KB (18571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f789c188a53299f824e7c04be763e79c5b526773d8151b1e07b136bcde02fe78`  
		Last Modified: Fri, 11 Mar 2022 04:34:52 GMT  
		Size: 32.1 MB (32141861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ff5480814d31ae5b439e71effe3a89f8726a82b5f9531c24575c309aa5b802`  
		Last Modified: Fri, 11 Mar 2022 04:34:29 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87eef11f36277453e95e5e04b4e0c53616adff7b16cfa2c3a0f202857b7cdbc6`  
		Last Modified: Wed, 16 Mar 2022 18:10:52 GMT  
		Size: 4.2 MB (4184974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d46200e0e59bf95c71d670370339aee5cc29dee1583f4d1a307c3028df712a33`  
		Last Modified: Wed, 16 Mar 2022 18:10:49 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e1e8f3e4f2e2082ceecfb446a7bafd2b394b8107b6cbe6fd388a6b7a9ac2a6`  
		Last Modified: Wed, 16 Mar 2022 18:10:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.3.0-RC1` - linux; arm variant v7

```console
$ docker pull composer@sha256:176559eaf4ee1a70a995cb261246e204f001515058ede16606807d03eed0b722
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65220498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a372e3bc4b555966f201b91f38ec9064daed92f4c6914061906ac627f5200845`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 05:27:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 05:27:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 05:27:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 05:27:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 05:27:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 05:27:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:27:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:27:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 05:27:21 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:43:09 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:43:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:43:09 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:43:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:43:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 02:43:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 02:43:15 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 02:43:17 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 02:43:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 02:43:18 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 12:13:42 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 12:13:44 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 12:13:44 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 12:13:45 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 17:57:36 GMT
ENV COMPOSER_VERSION=2.3.0-RC1
# Wed, 16 Mar 2022 17:58:24 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 17:58:24 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 17:58:25 GMT
WORKDIR /app
# Wed, 16 Mar 2022 17:58:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 17:58:25 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484fe107211badcebee7c4211e5ed91c7e5212cdd6d7edbb292a63ec60572bdd`  
		Last Modified: Tue, 30 Nov 2021 06:57:00 GMT  
		Size: 1.6 MB (1568802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93353d0a7113f37ba224b9ee296684e49f27c1c9440d3a3c5d310749213da97f`  
		Last Modified: Tue, 30 Nov 2021 06:56:59 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137db50a58959a68358c190d2a143088b82ab25d97cb889876fbc0728e446058`  
		Last Modified: Tue, 30 Nov 2021 06:57:00 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122d3a581986e22d7617f0ef2245bcb64b2a87ebcfe58b7b6d143561ce0cc8b2`  
		Last Modified: Fri, 18 Feb 2022 22:37:27 GMT  
		Size: 11.8 MB (11771980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc11ce0d4bdb5fcdda54f9da2a0eb1e4751b77e354a0dcdb827def3ff59f9f6`  
		Last Modified: Fri, 18 Feb 2022 22:37:24 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1951768145bebb84adba11b1ccd77c8d3802784df6c56f3ae141c103ac114c35`  
		Last Modified: Fri, 11 Mar 2022 07:38:53 GMT  
		Size: 15.0 MB (15034421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fdf84bb546f4d33ce7fff41672c1959df0ef457af702871c4ca3e4d585d8d87`  
		Last Modified: Fri, 11 Mar 2022 07:38:43 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164a1f0370d8b9c1f9c97a1a5aa3993986015fbe893874af94b911c5b8b06870`  
		Last Modified: Fri, 11 Mar 2022 07:38:43 GMT  
		Size: 18.6 KB (18569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b3d0ba165529b585fb1997f3fbc2d14dac5ccff866a44bff4b22578e6bd6aa`  
		Last Modified: Fri, 11 Mar 2022 12:16:34 GMT  
		Size: 30.5 MB (30471948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8e62f6bd555ee3d4b4ee22e2664dad7d5e0053556763e911676f59e8430be7`  
		Last Modified: Fri, 11 Mar 2022 12:16:14 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e40e45c71d84f5ec5e74972e923f2d45fa9bcc02e977c9c12491d8ae26c4e8`  
		Last Modified: Wed, 16 Mar 2022 18:00:26 GMT  
		Size: 3.9 MB (3914887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d321b06f6260068a245cb554aa80ae72d6e3036bbdb57227ac6beab5e8a78c4e`  
		Last Modified: Wed, 16 Mar 2022 18:00:24 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d58f09e6c5918a7284b18c452b80a0ac8236fdc5192119a56304b73092a89a`  
		Last Modified: Wed, 16 Mar 2022 18:00:24 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.3.0-RC1` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:d28a8980feeace3cd7606dcdacf1b8a637bdc4b2077fea0a3be12cdaea7cc197
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71088907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03c55046830d3e7325f4e8be8939f1928123c47197c9ba4112686a5833dfa57`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 02:50:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 02:50:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 02:50:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 02:50:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 02:50:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 02:50:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 02:50:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 02:50:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 02:50:54 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:18:23 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:18:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:18:25 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:19:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:19:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:18:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 03:18:52 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:18:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 03:18:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 03:18:55 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 10:35:18 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 10:35:18 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 10:35:19 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 10:35:20 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 17:39:38 GMT
ENV COMPOSER_VERSION=2.3.0-RC1
# Wed, 16 Mar 2022 17:40:04 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 17:40:06 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 17:40:06 GMT
WORKDIR /app
# Wed, 16 Mar 2022 17:40:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 17:40:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd720d9f53003155e4cfe3f1974fc0e4d74a622ea8c61cfccb00ee8b842c09b6`  
		Last Modified: Tue, 30 Nov 2021 03:59:34 GMT  
		Size: 1.7 MB (1708308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680efee530f3c970c3140b358d3dc583ded463f9adbadb737ca64c765cf997ee`  
		Last Modified: Tue, 30 Nov 2021 03:59:33 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643d01251bc949843dbd734a37e7cf28a01af4ea11443738b8b92d17e1e438de`  
		Last Modified: Tue, 30 Nov 2021 03:59:33 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbd0dff840aec18863650b4a5db905ad8e50c878c0d1f6c4c1634d0a4743ae4`  
		Last Modified: Fri, 18 Feb 2022 21:39:27 GMT  
		Size: 11.8 MB (11771755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6104c5a569f57122fffc091a5376f51c0848737cec9feaa9a82531e6c2da43`  
		Last Modified: Fri, 18 Feb 2022 21:39:26 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf59a8a0ffa368fdd033e0104d93a4b4913881c7f6bd86aaef35c541233a018`  
		Last Modified: Fri, 11 Mar 2022 09:48:26 GMT  
		Size: 17.5 MB (17546174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef08d98d3666360bd8cbe19dcb81037d75a8aca59ebcfd386287fccb05cc9aab`  
		Last Modified: Fri, 11 Mar 2022 09:48:22 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e7653a3be11ae60976b3f56b5349443e6c458f125a944ba93d234548413851`  
		Last Modified: Fri, 11 Mar 2022 09:48:22 GMT  
		Size: 18.5 KB (18487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f017cf68653c976946e3d237367accaca773a59fbfae998075a1dfc4d6703911`  
		Last Modified: Fri, 11 Mar 2022 10:36:49 GMT  
		Size: 33.0 MB (33001745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0c25578ca0b4f7b253053edcefd8aaea561ada9282ced6617c66749e3cbd4e`  
		Last Modified: Fri, 11 Mar 2022 10:36:44 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6876702c43cd7a3fcf9c3c043d76e94ae1182a6c283bb7de9143d0a36947dcf4`  
		Last Modified: Wed, 16 Mar 2022 17:42:10 GMT  
		Size: 4.3 MB (4321981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc3b74e160374ef1a5650d312c31101d1fcd742421137929930d57c87b35eba`  
		Last Modified: Wed, 16 Mar 2022 17:42:09 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01582158b58c9ca1a13fa39a128fdd435efd2c4e4c089d56aff5a41257e77e96`  
		Last Modified: Wed, 16 Mar 2022 17:42:09 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.3.0-RC1` - linux; 386

```console
$ docker pull composer@sha256:64695c071f587bb4cf9c86fd18cd5c5049bba07dbfc39381e4928644386a3edd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54495598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4abe65a4105a50156eabfc20967e6ceba3eeb0a7d7cf421a945ded8375a1de`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:53:48 GMT
ADD file:b9a17131c440053f2f67e127b447645f25fd7de2d6caca42f569cafab6291855 in / 
# Wed, 24 Nov 2021 20:53:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 05:59:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 05:59:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 05:59:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 05:59:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 05:59:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 05:59:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:59:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:59:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 05:59:11 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:49:36 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:49:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:49:37 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:50:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:50:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:42:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 04:42:32 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:42:33 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 04:42:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 04:42:33 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 14:29:16 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 14:29:16 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 14:29:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 14:29:17 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 17:39:18 GMT
ENV COMPOSER_VERSION=2.3.0-RC1
# Wed, 16 Mar 2022 17:39:50 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 17:39:51 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 17:39:52 GMT
WORKDIR /app
# Wed, 16 Mar 2022 17:39:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 17:39:52 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:e6889e0d66307a4b916fc844f2dcbc03245c63bc4189dd3e88126d9dcf2f9231`  
		Last Modified: Wed, 24 Nov 2021 20:54:48 GMT  
		Size: 2.8 MB (2827117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d6acd3b6e4278a7b3ef37d3525813808468237f086215b68594b244dbd1fba`  
		Last Modified: Tue, 30 Nov 2021 08:26:15 GMT  
		Size: 1.8 MB (1810453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc53af545b93519336bed63b8765255ac8280e27c8e3a17c336f92526b3f290`  
		Last Modified: Tue, 30 Nov 2021 08:26:14 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d406b6d62c3d67bec5f638d47d2b1b49c0ee41d80a791a1b90eaec776cf4fd`  
		Last Modified: Tue, 30 Nov 2021 08:26:13 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09947cbaa6ea94c09911bac9f42ad67e560858bcf313330c30a51d4e047debcc`  
		Last Modified: Fri, 18 Feb 2022 23:36:11 GMT  
		Size: 11.8 MB (11771980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418d95d8e7f7c7a6bca99de67f7268f3c2bd9f90ac05ded2056aca5dcfcf42f3`  
		Last Modified: Fri, 18 Feb 2022 23:36:09 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe93a8e5de6a995b340c34f3b0c9926bbfb8314a31f31edd9aeecf49431cee4`  
		Last Modified: Fri, 11 Mar 2022 11:59:00 GMT  
		Size: 18.0 MB (18045807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98142bd532dfb18d7144d8a1bf1c7a641e931c169b4d2e1863e890a7f1b8e42d`  
		Last Modified: Fri, 11 Mar 2022 11:58:55 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e86e6cc1686366ee83df3ef2c5f3a0405af922746fd6d7ad4fd411ce9a77da`  
		Last Modified: Fri, 11 Mar 2022 11:58:55 GMT  
		Size: 18.8 KB (18773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765d3379030a7d7c59596ec428386624a93faadc763120bcb58cd721522baa8e`  
		Last Modified: Fri, 11 Mar 2022 14:30:44 GMT  
		Size: 15.6 MB (15590818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efdf8175c4916376f3518dfce254d9d6655bbb9cdf549acdfc253419b6d70b0`  
		Last Modified: Fri, 11 Mar 2022 14:30:41 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fede22822a011094dfe627d213b08d1b00e3d825b21f76bf12fc6df942d87b8`  
		Last Modified: Wed, 16 Mar 2022 17:41:17 GMT  
		Size: 4.4 MB (4425519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ccd4cbdbfcf6c5b16da6c7a8d2570c559ba7f4f77465e1f8a61912de14a105d`  
		Last Modified: Wed, 16 Mar 2022 17:41:16 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2756b5f499130fac4c3646d3bfed07287f74a5a45cce498be8117b44388bcca3`  
		Last Modified: Wed, 16 Mar 2022 17:41:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.3.0-RC1` - linux; ppc64le

```console
$ docker pull composer@sha256:5b8aad76b10bcc450bcb7738cac6c30a40450e0431abeddba2767c3a12233fe7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73201769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6818afe79d299b01a84e1c99294952de05f93a13a6f0205af04a8de519733224`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:20:16 GMT
ADD file:57115dca2eb707f46b6301e75174e6aa316fb02ac28643b91429b75be51bd8c8 in / 
# Wed, 24 Nov 2021 20:20:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 06:02:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 06:03:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 06:03:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 06:03:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 06:03:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 06:03:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 06:03:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 06:04:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 06:04:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:19:05 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:19:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:19:10 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:19:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:19:44 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:41:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 03:41:38 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:41:46 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 03:41:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 03:41:52 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 10:53:22 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 10:53:41 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 10:53:45 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 10:53:51 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 18:22:10 GMT
ENV COMPOSER_VERSION=2.3.0-RC1
# Wed, 16 Mar 2022 18:24:23 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 18:25:42 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 18:27:03 GMT
WORKDIR /app
# Wed, 16 Mar 2022 18:28:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 18:29:18 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:159b5dcb1717c815c76ff5ea1db730e18e8609c9090238e43282856db9e71f47`  
		Last Modified: Wed, 24 Nov 2021 20:21:14 GMT  
		Size: 2.8 MB (2814780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603762061fb50079a4b6eb13347fd9a84cc1456d628cf781c89924a54bc419c1`  
		Last Modified: Tue, 30 Nov 2021 07:26:39 GMT  
		Size: 1.8 MB (1756276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645c08440cfaddc2735de2e28697acff0bc71db4cc7242494a44f92c94134e32`  
		Last Modified: Tue, 30 Nov 2021 07:26:39 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5de97a9a329d566f48c2edce253e4ccda6f021041e92326728b7499d13c823b`  
		Last Modified: Tue, 30 Nov 2021 07:26:39 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663cc53ab2317558b9afc14f317845ab71678d9014ef8f4b455b76a1f5ad13b4`  
		Last Modified: Fri, 18 Feb 2022 22:26:29 GMT  
		Size: 11.8 MB (11771981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01091fd3e45df20547a10229a30b96d8cf5998dafc5a5815700834ea2a1cca9`  
		Last Modified: Fri, 18 Feb 2022 22:26:27 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7c08f08c396228976e471a184d4a94d00e1ffcdd366553305de7177eec3bec`  
		Last Modified: Fri, 11 Mar 2022 09:52:14 GMT  
		Size: 18.4 MB (18353518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e767c5a126e3cb62dc8dfdb265ab1b5cfefbbb4955aa58b9ca20fd4e9a3cb5d`  
		Last Modified: Fri, 11 Mar 2022 09:52:10 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a598088569767a94973057cabf1fdeb7dee736eeb4881b2a7e6f18a0c0f2807`  
		Last Modified: Fri, 11 Mar 2022 09:52:10 GMT  
		Size: 18.6 KB (18564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865b388f98b32bac5bade9ff004270a55a0e68d686465a2830ad43a6e6c1e699`  
		Last Modified: Fri, 11 Mar 2022 10:57:32 GMT  
		Size: 33.9 MB (33902882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f226452b0c1667229ee85c065083d8341b4750406d4809c2849e36b27a77a35`  
		Last Modified: Fri, 11 Mar 2022 10:57:25 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bbcdda71a0a491a662d64e7cc58bcea9f0bfd8fb1989e80201b518b5add73d1`  
		Last Modified: Wed, 16 Mar 2022 18:42:54 GMT  
		Size: 4.6 MB (4578641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4a26306c68820dea6a3aad156e9689e69e82efc817a27cf0d7df5fb39389e9`  
		Last Modified: Wed, 16 Mar 2022 18:42:53 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bcacb1d616c0be20b193343888377fea92720874f6c52a95d1c14b1c18b98c5`  
		Last Modified: Wed, 16 Mar 2022 18:42:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.3.0-RC1` - linux; s390x

```console
$ docker pull composer@sha256:f0fe2462f04eef77425d91d0cb442694aba0ea8388060ebfc214cbc74cc2a408
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71713541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c901553796688d43018ff61e57cfb9872e88302b1c96eadced584ab198e4d2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:41:23 GMT
ADD file:cd24c711a2ef431b3ff94f9a02bfc42f159bc60de1d0eceecafea4e8af02441d in / 
# Wed, 24 Nov 2021 20:41:23 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:50:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 04:50:01 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 04:50:02 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 04:50:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 04:50:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 04:50:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 04:50:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 04:50:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 04:50:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:08:01 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:08:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:08:02 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:09:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:09:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:35:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 01:35:50 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:35:51 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 01:35:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 01:35:52 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 05:02:45 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 05:02:47 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 05:02:47 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 05:02:47 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 17:41:26 GMT
ENV COMPOSER_VERSION=2.3.0-RC1
# Wed, 16 Mar 2022 17:41:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 17:41:44 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 17:41:44 GMT
WORKDIR /app
# Wed, 16 Mar 2022 17:41:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 17:41:44 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d6baca485f3d0f7c77221be60fbef5db014a5ef9d8f53db4a310c947c690d189`  
		Last Modified: Wed, 24 Nov 2021 20:42:15 GMT  
		Size: 2.6 MB (2605944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079fbafa3afc04920b17b503e5d173a44e68fa743eddc7a0eca5e81c7572b8a2`  
		Last Modified: Tue, 30 Nov 2021 08:33:50 GMT  
		Size: 1.8 MB (1771410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ea1ee8ecbda317521ca15da3d8e45a369d74d9b70a0070ebd705cb9aaf88a2`  
		Last Modified: Tue, 30 Nov 2021 08:33:49 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abad577e66a4ab93646ed4a4aefb0579d577932add0d28121e5aece37cfc08dd`  
		Last Modified: Tue, 30 Nov 2021 08:33:49 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac62d72c92f8b14f9b5873207ef984e63eff6fec607db9d4330d9c8129c2925`  
		Last Modified: Fri, 18 Feb 2022 21:13:54 GMT  
		Size: 11.8 MB (11771995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074272c815254eeab42d6bbeac5cb89869166aa437afdace2d9b24a9aa028c4f`  
		Last Modified: Fri, 18 Feb 2022 21:13:53 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a400f11df7f6a7553c85e98fc344489885d2289da563949d00c5280b943f9d0b`  
		Last Modified: Fri, 11 Mar 2022 04:03:48 GMT  
		Size: 16.4 MB (16381073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560e4e59acf6107ca6529fb1d607beb5fe7518052fc9e159c1a89111422d0ed9`  
		Last Modified: Fri, 11 Mar 2022 04:03:46 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93e829bfc7fd232613ba9a365a7a92259718f51bf2ce8df42cf435a15dcc38f`  
		Last Modified: Fri, 11 Mar 2022 04:03:46 GMT  
		Size: 18.6 KB (18598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86bb1285cae11648274513dd55a891e1ca7f14ee80070d95daeae0521db77da`  
		Last Modified: Fri, 11 Mar 2022 05:03:53 GMT  
		Size: 34.9 MB (34887464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e94752314a819cf5f190758a33d2f4d2a3dbde007de6249f275621e5ef423f8`  
		Last Modified: Fri, 11 Mar 2022 05:03:49 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6e068cca1d92d784bda7bd8cd0952ef00e2aefaf1e3fab39b16fd9773ad7bf`  
		Last Modified: Wed, 16 Mar 2022 17:42:42 GMT  
		Size: 4.3 MB (4271928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4bffcc6f3947556ed17fc494a3b6e03f9fa4533fca0a1260f0cf1d0a6416b0`  
		Last Modified: Wed, 16 Mar 2022 17:42:41 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292b934853dce308e94a118ceddc2f552369eada3185093816c0753022ed4406`  
		Last Modified: Wed, 16 Mar 2022 17:42:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `composer:latest`

```console
$ docker pull composer@sha256:761083bb446357e8ae40438dc32ec74992aaa3f295a5c76a2c19c0b5703d3c61
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
$ docker pull composer@sha256:326e28cdb766579a1e9088d0644f5fbd35fc3a21c4103a1f3e57b24dacfac220
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73039521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa6a91d32046c9419a0bdb982817ae30ee35f1a7a0cd9c13462581eba5ab3de2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 07:06:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 07:06:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 07:06:04 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 07:06:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 07:06:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 07:06:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 07:06:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 07:06:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 07:06:06 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:16:49 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:16:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:16:50 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:17:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:17:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:06:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 04:06:01 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:06:03 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 04:06:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 04:06:03 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 11:55:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 11:55:50 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 11:55:50 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 11:55:50 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 18:19:43 GMT
ENV COMPOSER_VERSION=2.2.9
# Wed, 16 Mar 2022 18:20:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 18:20:03 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 18:20:03 GMT
WORKDIR /app
# Wed, 16 Mar 2022 18:20:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 18:20:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7da25b2876b1c935b05d7e6efa3e8cd559d031cf30b246d7659ed438726acd`  
		Last Modified: Tue, 30 Nov 2021 09:03:50 GMT  
		Size: 1.7 MB (1709704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc599114627e3bd98e0204b93b161e03065bf9a228bb02ae202469655f12b8d`  
		Last Modified: Tue, 30 Nov 2021 09:03:48 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927a0b37a45a98d7d74a6d7d1567230eca834fb89417274557de7986d1f39401`  
		Last Modified: Tue, 30 Nov 2021 09:03:48 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e721f6667a5183c40af8377b3c611b535e9f4eaac41ad37954cc557c4d606dfd`  
		Last Modified: Fri, 18 Feb 2022 23:00:29 GMT  
		Size: 11.8 MB (11771990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdbed47885a29ebdc56f05207500027b26f268bdc5d034f8a6ca8fb34afab54`  
		Last Modified: Fri, 18 Feb 2022 23:00:28 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16135939cf41586188ad9ce6d0b22a1c609842cfcc8f7cb07b9e6db2730c2b37`  
		Last Modified: Fri, 11 Mar 2022 11:16:46 GMT  
		Size: 17.7 MB (17687791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb0fc4c5a6959679cb69633cfe546c6bda81fa74e7a34c9745aeb04921189c5`  
		Last Modified: Fri, 11 Mar 2022 11:16:43 GMT  
		Size: 2.3 KB (2301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37886f8b09348b24b4d10650f01acb3b0517e7d2a69a618c4c87bd1b4ba3df4`  
		Last Modified: Fri, 11 Mar 2022 11:16:43 GMT  
		Size: 18.8 KB (18777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b857d06f2e595fd88321d0fc2350c7811cf2c17127d1039997cb866237878e4d`  
		Last Modified: Fri, 11 Mar 2022 11:56:53 GMT  
		Size: 34.7 MB (34651834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f14b3f6c787d8ee1c2dc4cd24bfecab102e42b082163a5d45722d4e5e22780b`  
		Last Modified: Fri, 11 Mar 2022 11:56:47 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9614584564fb02a9e2f0e3d4654e34a4d5abecf123cc3ef1b490adce6ea509ac`  
		Last Modified: Wed, 16 Mar 2022 18:20:32 GMT  
		Size: 4.4 MB (4375884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2886923f9475c3d778e25d311f8c10e561f965b20bfba4273336a084abc32a5b`  
		Last Modified: Wed, 16 Mar 2022 18:20:30 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5a0cfeadcf4811a573924b6c4ba4df07e7e3c0267838f645a500ad5c2f7535`  
		Last Modified: Wed, 16 Mar 2022 18:20:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; arm variant v6

```console
$ docker pull composer@sha256:b6e2de2d5fb63d8e0e314e6d15e1d8eafd7e743c35c9a70bbe4104779f3c9f6b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68400844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acbd8d6d516db4b6ee4c8870d6e9af74da75ab99c426a8109e947161e5ecb850`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 03:20:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 03:20:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 03:20:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 03:20:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 03:20:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 03:20:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 03:20:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 03:20:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 03:20:12 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 19:50:06 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 19:50:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 19:50:07 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 19:50:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 19:50:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:16:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 01:16:18 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:16:21 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 01:16:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 01:16:22 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 04:31:45 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 04:31:47 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 04:31:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 04:31:48 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 18:08:58 GMT
ENV COMPOSER_VERSION=2.2.9
# Wed, 16 Mar 2022 18:09:45 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 18:09:46 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 18:09:46 GMT
WORKDIR /app
# Wed, 16 Mar 2022 18:09:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 18:09:47 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289be6d758ff0faa38d64732e5736031f2250cbf78d1ca4b32abba4accd6a3fa`  
		Last Modified: Tue, 30 Nov 2021 04:29:36 GMT  
		Size: 1.7 MB (1698826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0b442a0f679dba79aa838c408cf49916ca26d27e1252e26f3904d7c5b83d6c`  
		Last Modified: Tue, 30 Nov 2021 04:29:33 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef02b1cade59fbcc24c0ee972dd15d8caa89dda554cdb8aa742de1c6f3d5b7c`  
		Last Modified: Tue, 30 Nov 2021 04:29:33 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452d0467a92abee019a5ea9cdd7cf7b52fb629aa35a045df70339fb93b634760`  
		Last Modified: Fri, 18 Feb 2022 20:43:48 GMT  
		Size: 11.8 MB (11771982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e48b13f55f3236500af7e58ba05199b7acf9a4d62bc99270797ca5f5c1bc88`  
		Last Modified: Fri, 18 Feb 2022 20:43:45 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59c13e75cc1f96edac01b31ca5bf7f47552e1b3662911082d1926896e971fa4`  
		Last Modified: Fri, 11 Mar 2022 03:24:45 GMT  
		Size: 16.0 MB (16031967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0e34d07dc9c018a0df930e952b25876b7c0168a21c1a5a41e366c8103313b7`  
		Last Modified: Fri, 11 Mar 2022 03:24:38 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139e94b314f0a7968bb009c6b624a733bc8b17cde4cc3c5fb98883a957793045`  
		Last Modified: Fri, 11 Mar 2022 03:24:38 GMT  
		Size: 18.6 KB (18571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f789c188a53299f824e7c04be763e79c5b526773d8151b1e07b136bcde02fe78`  
		Last Modified: Fri, 11 Mar 2022 04:34:52 GMT  
		Size: 32.1 MB (32141861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ff5480814d31ae5b439e71effe3a89f8726a82b5f9531c24575c309aa5b802`  
		Last Modified: Fri, 11 Mar 2022 04:34:29 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d9913925d9bc064600a02965ab181c57ee38bcf13ae2b8fca5f5ceb49a6f09`  
		Last Modified: Wed, 16 Mar 2022 18:11:06 GMT  
		Size: 4.1 MB (4101086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee747280ba0407bc5a9ac0a76248042a687be679e269721b28ee8720135d6e29`  
		Last Modified: Wed, 16 Mar 2022 18:11:03 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f7208db20f07db348936636dd910d9c20b944a6585b4a5250e9187492e5694`  
		Last Modified: Wed, 16 Mar 2022 18:11:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; arm variant v7

```console
$ docker pull composer@sha256:8e7985450dd6157d802db9b8486af01981b5d6f0bfd0577437d32b7f6f98543f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65134499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c848ee419322351ac7186825962f5c9118465091a1f2cc0fd1ae0df13011133`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 05:27:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 05:27:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 05:27:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 05:27:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 05:27:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 05:27:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:27:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:27:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 05:27:21 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:43:09 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:43:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:43:09 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:43:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:43:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 02:43:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 02:43:15 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 02:43:17 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 02:43:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 02:43:18 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 12:13:42 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 12:13:44 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 12:13:44 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 12:13:45 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 17:58:36 GMT
ENV COMPOSER_VERSION=2.2.9
# Wed, 16 Mar 2022 17:59:22 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 17:59:22 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 17:59:23 GMT
WORKDIR /app
# Wed, 16 Mar 2022 17:59:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 17:59:24 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484fe107211badcebee7c4211e5ed91c7e5212cdd6d7edbb292a63ec60572bdd`  
		Last Modified: Tue, 30 Nov 2021 06:57:00 GMT  
		Size: 1.6 MB (1568802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93353d0a7113f37ba224b9ee296684e49f27c1c9440d3a3c5d310749213da97f`  
		Last Modified: Tue, 30 Nov 2021 06:56:59 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137db50a58959a68358c190d2a143088b82ab25d97cb889876fbc0728e446058`  
		Last Modified: Tue, 30 Nov 2021 06:57:00 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122d3a581986e22d7617f0ef2245bcb64b2a87ebcfe58b7b6d143561ce0cc8b2`  
		Last Modified: Fri, 18 Feb 2022 22:37:27 GMT  
		Size: 11.8 MB (11771980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc11ce0d4bdb5fcdda54f9da2a0eb1e4751b77e354a0dcdb827def3ff59f9f6`  
		Last Modified: Fri, 18 Feb 2022 22:37:24 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1951768145bebb84adba11b1ccd77c8d3802784df6c56f3ae141c103ac114c35`  
		Last Modified: Fri, 11 Mar 2022 07:38:53 GMT  
		Size: 15.0 MB (15034421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fdf84bb546f4d33ce7fff41672c1959df0ef457af702871c4ca3e4d585d8d87`  
		Last Modified: Fri, 11 Mar 2022 07:38:43 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164a1f0370d8b9c1f9c97a1a5aa3993986015fbe893874af94b911c5b8b06870`  
		Last Modified: Fri, 11 Mar 2022 07:38:43 GMT  
		Size: 18.6 KB (18569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b3d0ba165529b585fb1997f3fbc2d14dac5ccff866a44bff4b22578e6bd6aa`  
		Last Modified: Fri, 11 Mar 2022 12:16:34 GMT  
		Size: 30.5 MB (30471948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8e62f6bd555ee3d4b4ee22e2664dad7d5e0053556763e911676f59e8430be7`  
		Last Modified: Fri, 11 Mar 2022 12:16:14 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07eddbcbd7af52d2f868be4e78de819baaed038b501271a2500ac2fc4bba53b`  
		Last Modified: Wed, 16 Mar 2022 18:00:42 GMT  
		Size: 3.8 MB (3828887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbc1e6568bb9b37f50762a3378bd8a25055ac9fbaf11ec2d43c94234987698c`  
		Last Modified: Wed, 16 Mar 2022 18:00:40 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3da75e4905627fccb6521ac3f1c1b93c66ffbdb7a662f25ce6db75903277cf`  
		Last Modified: Wed, 16 Mar 2022 18:00:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:88ecf252d0fa4c6321e415dbda78934f3296272312613f11a68fcf0eaf357307
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71007032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5390a7677c7fd8300733ca205ed96ed73dd9de3e515d30be30a61725a621364f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 02:50:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 02:50:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 02:50:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 02:50:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 02:50:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 02:50:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 02:50:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 02:50:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 02:50:54 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:18:23 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:18:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:18:25 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:19:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:19:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:18:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 03:18:52 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:18:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 03:18:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 03:18:55 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 10:35:18 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 10:35:18 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 10:35:19 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 10:35:20 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 17:40:22 GMT
ENV COMPOSER_VERSION=2.2.9
# Wed, 16 Mar 2022 17:40:45 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 17:40:46 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 17:40:46 GMT
WORKDIR /app
# Wed, 16 Mar 2022 17:40:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 17:40:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd720d9f53003155e4cfe3f1974fc0e4d74a622ea8c61cfccb00ee8b842c09b6`  
		Last Modified: Tue, 30 Nov 2021 03:59:34 GMT  
		Size: 1.7 MB (1708308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680efee530f3c970c3140b358d3dc583ded463f9adbadb737ca64c765cf997ee`  
		Last Modified: Tue, 30 Nov 2021 03:59:33 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643d01251bc949843dbd734a37e7cf28a01af4ea11443738b8b92d17e1e438de`  
		Last Modified: Tue, 30 Nov 2021 03:59:33 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbd0dff840aec18863650b4a5db905ad8e50c878c0d1f6c4c1634d0a4743ae4`  
		Last Modified: Fri, 18 Feb 2022 21:39:27 GMT  
		Size: 11.8 MB (11771755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6104c5a569f57122fffc091a5376f51c0848737cec9feaa9a82531e6c2da43`  
		Last Modified: Fri, 18 Feb 2022 21:39:26 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf59a8a0ffa368fdd033e0104d93a4b4913881c7f6bd86aaef35c541233a018`  
		Last Modified: Fri, 11 Mar 2022 09:48:26 GMT  
		Size: 17.5 MB (17546174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef08d98d3666360bd8cbe19dcb81037d75a8aca59ebcfd386287fccb05cc9aab`  
		Last Modified: Fri, 11 Mar 2022 09:48:22 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e7653a3be11ae60976b3f56b5349443e6c458f125a944ba93d234548413851`  
		Last Modified: Fri, 11 Mar 2022 09:48:22 GMT  
		Size: 18.5 KB (18487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f017cf68653c976946e3d237367accaca773a59fbfae998075a1dfc4d6703911`  
		Last Modified: Fri, 11 Mar 2022 10:36:49 GMT  
		Size: 33.0 MB (33001745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0c25578ca0b4f7b253053edcefd8aaea561ada9282ced6617c66749e3cbd4e`  
		Last Modified: Fri, 11 Mar 2022 10:36:44 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f681d2af1a050fe7840d4cedae9568fa0ae020ab2860070fe7031503578ab40`  
		Last Modified: Wed, 16 Mar 2022 17:42:26 GMT  
		Size: 4.2 MB (4240106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94edf64a4261df8ee69484e617d69127d0c311998bad01d1e3e4556ff3dcc8ca`  
		Last Modified: Wed, 16 Mar 2022 17:42:25 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7a0434d0b212ef33c720406d8f0808fa9dda1fe4160e791da97681d4edaffc`  
		Last Modified: Wed, 16 Mar 2022 17:42:25 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; 386

```console
$ docker pull composer@sha256:a2477b4f8e6288b6cfdd1cabc3eed000d8e511fe967addb5a379e5f5887db17b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.4 MB (54414804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d7adaf71922c61637b4fcc20a8d11cb2062b357ac1cb0149ed700ee5f50bb7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:53:48 GMT
ADD file:b9a17131c440053f2f67e127b447645f25fd7de2d6caca42f569cafab6291855 in / 
# Wed, 24 Nov 2021 20:53:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 05:59:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 05:59:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 05:59:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 05:59:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 05:59:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 05:59:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:59:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:59:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 05:59:11 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:49:36 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:49:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:49:37 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:50:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:50:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:42:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 04:42:32 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:42:33 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 04:42:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 04:42:33 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 14:29:16 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 14:29:16 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 14:29:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 14:29:17 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 17:39:59 GMT
ENV COMPOSER_VERSION=2.2.9
# Wed, 16 Mar 2022 17:40:24 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 17:40:26 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 17:40:27 GMT
WORKDIR /app
# Wed, 16 Mar 2022 17:40:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 17:40:27 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:e6889e0d66307a4b916fc844f2dcbc03245c63bc4189dd3e88126d9dcf2f9231`  
		Last Modified: Wed, 24 Nov 2021 20:54:48 GMT  
		Size: 2.8 MB (2827117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d6acd3b6e4278a7b3ef37d3525813808468237f086215b68594b244dbd1fba`  
		Last Modified: Tue, 30 Nov 2021 08:26:15 GMT  
		Size: 1.8 MB (1810453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc53af545b93519336bed63b8765255ac8280e27c8e3a17c336f92526b3f290`  
		Last Modified: Tue, 30 Nov 2021 08:26:14 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d406b6d62c3d67bec5f638d47d2b1b49c0ee41d80a791a1b90eaec776cf4fd`  
		Last Modified: Tue, 30 Nov 2021 08:26:13 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09947cbaa6ea94c09911bac9f42ad67e560858bcf313330c30a51d4e047debcc`  
		Last Modified: Fri, 18 Feb 2022 23:36:11 GMT  
		Size: 11.8 MB (11771980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418d95d8e7f7c7a6bca99de67f7268f3c2bd9f90ac05ded2056aca5dcfcf42f3`  
		Last Modified: Fri, 18 Feb 2022 23:36:09 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe93a8e5de6a995b340c34f3b0c9926bbfb8314a31f31edd9aeecf49431cee4`  
		Last Modified: Fri, 11 Mar 2022 11:59:00 GMT  
		Size: 18.0 MB (18045807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98142bd532dfb18d7144d8a1bf1c7a641e931c169b4d2e1863e890a7f1b8e42d`  
		Last Modified: Fri, 11 Mar 2022 11:58:55 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e86e6cc1686366ee83df3ef2c5f3a0405af922746fd6d7ad4fd411ce9a77da`  
		Last Modified: Fri, 11 Mar 2022 11:58:55 GMT  
		Size: 18.8 KB (18773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765d3379030a7d7c59596ec428386624a93faadc763120bcb58cd721522baa8e`  
		Last Modified: Fri, 11 Mar 2022 14:30:44 GMT  
		Size: 15.6 MB (15590818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efdf8175c4916376f3518dfce254d9d6655bbb9cdf549acdfc253419b6d70b0`  
		Last Modified: Fri, 11 Mar 2022 14:30:41 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66086ccb543f409dbb0372048314fc39072d900a3b36b3efaf8e886310fc456`  
		Last Modified: Wed, 16 Mar 2022 17:41:30 GMT  
		Size: 4.3 MB (4344725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977603e326a453ec883002a965684daaf1f2b8495410041064afb673231e6433`  
		Last Modified: Wed, 16 Mar 2022 17:41:28 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c4920c285cadc297fb006fb893ba20057f8f86ef9dac2afce0f0c2d331aa46`  
		Last Modified: Wed, 16 Mar 2022 17:41:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; ppc64le

```console
$ docker pull composer@sha256:bce9ee868315f50bf13b33b49d5743c5bc838bc6730b13f13e1a67d939ab56fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73121143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a1d96d152754d33c266b566e0b7790f6bfb37ba43e15b6845c8354832816c8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:20:16 GMT
ADD file:57115dca2eb707f46b6301e75174e6aa316fb02ac28643b91429b75be51bd8c8 in / 
# Wed, 24 Nov 2021 20:20:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 06:02:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 06:03:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 06:03:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 06:03:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 06:03:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 06:03:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 06:03:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 06:04:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 06:04:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:19:05 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:19:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:19:10 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:19:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:19:44 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:41:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 03:41:38 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:41:46 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 03:41:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 03:41:52 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 10:53:22 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 10:53:41 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 10:53:45 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 10:53:51 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 18:29:39 GMT
ENV COMPOSER_VERSION=2.2.9
# Wed, 16 Mar 2022 18:30:52 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 18:31:59 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 18:32:57 GMT
WORKDIR /app
# Wed, 16 Mar 2022 18:34:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 18:35:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:159b5dcb1717c815c76ff5ea1db730e18e8609c9090238e43282856db9e71f47`  
		Last Modified: Wed, 24 Nov 2021 20:21:14 GMT  
		Size: 2.8 MB (2814780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603762061fb50079a4b6eb13347fd9a84cc1456d628cf781c89924a54bc419c1`  
		Last Modified: Tue, 30 Nov 2021 07:26:39 GMT  
		Size: 1.8 MB (1756276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645c08440cfaddc2735de2e28697acff0bc71db4cc7242494a44f92c94134e32`  
		Last Modified: Tue, 30 Nov 2021 07:26:39 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5de97a9a329d566f48c2edce253e4ccda6f021041e92326728b7499d13c823b`  
		Last Modified: Tue, 30 Nov 2021 07:26:39 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663cc53ab2317558b9afc14f317845ab71678d9014ef8f4b455b76a1f5ad13b4`  
		Last Modified: Fri, 18 Feb 2022 22:26:29 GMT  
		Size: 11.8 MB (11771981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01091fd3e45df20547a10229a30b96d8cf5998dafc5a5815700834ea2a1cca9`  
		Last Modified: Fri, 18 Feb 2022 22:26:27 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7c08f08c396228976e471a184d4a94d00e1ffcdd366553305de7177eec3bec`  
		Last Modified: Fri, 11 Mar 2022 09:52:14 GMT  
		Size: 18.4 MB (18353518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e767c5a126e3cb62dc8dfdb265ab1b5cfefbbb4955aa58b9ca20fd4e9a3cb5d`  
		Last Modified: Fri, 11 Mar 2022 09:52:10 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a598088569767a94973057cabf1fdeb7dee736eeb4881b2a7e6f18a0c0f2807`  
		Last Modified: Fri, 11 Mar 2022 09:52:10 GMT  
		Size: 18.6 KB (18564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865b388f98b32bac5bade9ff004270a55a0e68d686465a2830ad43a6e6c1e699`  
		Last Modified: Fri, 11 Mar 2022 10:57:32 GMT  
		Size: 33.9 MB (33902882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f226452b0c1667229ee85c065083d8341b4750406d4809c2849e36b27a77a35`  
		Last Modified: Fri, 11 Mar 2022 10:57:25 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5f6fd27e5c402548636d63962e13de0ced945c9a6943a67c408ef6c18e071d`  
		Last Modified: Wed, 16 Mar 2022 18:44:00 GMT  
		Size: 4.5 MB (4498013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3fba9e19771a5ee851139d0b6465620f9acd7ed4f74a85eaaf86547836919f`  
		Last Modified: Wed, 16 Mar 2022 18:43:59 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec711f0032b76a073691ea34ea9edbcaeffecf203ca1ad55d6d2e712cdc6e9a`  
		Last Modified: Wed, 16 Mar 2022 18:43:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; s390x

```console
$ docker pull composer@sha256:4d6d35d1f21dd04ec59345df6103a538e2c87b72dba6bed4d4e510b75ce69301
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71633583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a7cdde9dd9c512ec61147343e6160697e2ce8a5ca240881238d801b6fad937`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 24 Nov 2021 20:41:23 GMT
ADD file:cd24c711a2ef431b3ff94f9a02bfc42f159bc60de1d0eceecafea4e8af02441d in / 
# Wed, 24 Nov 2021 20:41:23 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:50:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 04:50:01 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 04:50:02 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 04:50:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 04:50:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 04:50:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 04:50:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 04:50:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 04:50:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 18 Feb 2022 20:08:01 GMT
ENV PHP_VERSION=8.1.3
# Fri, 18 Feb 2022 20:08:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Fri, 18 Feb 2022 20:08:02 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Fri, 18 Feb 2022 20:09:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 18 Feb 2022 20:09:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:35:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 01:35:50 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 11 Mar 2022 01:35:51 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 01:35:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 01:35:52 GMT
CMD ["php" "-a"]
# Fri, 11 Mar 2022 05:02:45 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)
# Fri, 11 Mar 2022 05:02:47 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 11 Mar 2022 05:02:47 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Mar 2022 05:02:47 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 16 Mar 2022 17:41:52 GMT
ENV COMPOSER_VERSION=2.2.9
# Wed, 16 Mar 2022 17:42:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} +
# Wed, 16 Mar 2022 17:42:07 GMT
COPY file:2d86469921ea86d2c1e50443fd24d98471bd3c2db7341b80a83c2d9a80c7074e in /docker-entrypoint.sh 
# Wed, 16 Mar 2022 17:42:07 GMT
WORKDIR /app
# Wed, 16 Mar 2022 17:42:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 17:42:07 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d6baca485f3d0f7c77221be60fbef5db014a5ef9d8f53db4a310c947c690d189`  
		Last Modified: Wed, 24 Nov 2021 20:42:15 GMT  
		Size: 2.6 MB (2605944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079fbafa3afc04920b17b503e5d173a44e68fa743eddc7a0eca5e81c7572b8a2`  
		Last Modified: Tue, 30 Nov 2021 08:33:50 GMT  
		Size: 1.8 MB (1771410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ea1ee8ecbda317521ca15da3d8e45a369d74d9b70a0070ebd705cb9aaf88a2`  
		Last Modified: Tue, 30 Nov 2021 08:33:49 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abad577e66a4ab93646ed4a4aefb0579d577932add0d28121e5aece37cfc08dd`  
		Last Modified: Tue, 30 Nov 2021 08:33:49 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac62d72c92f8b14f9b5873207ef984e63eff6fec607db9d4330d9c8129c2925`  
		Last Modified: Fri, 18 Feb 2022 21:13:54 GMT  
		Size: 11.8 MB (11771995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074272c815254eeab42d6bbeac5cb89869166aa437afdace2d9b24a9aa028c4f`  
		Last Modified: Fri, 18 Feb 2022 21:13:53 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a400f11df7f6a7553c85e98fc344489885d2289da563949d00c5280b943f9d0b`  
		Last Modified: Fri, 11 Mar 2022 04:03:48 GMT  
		Size: 16.4 MB (16381073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560e4e59acf6107ca6529fb1d607beb5fe7518052fc9e159c1a89111422d0ed9`  
		Last Modified: Fri, 11 Mar 2022 04:03:46 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93e829bfc7fd232613ba9a365a7a92259718f51bf2ce8df42cf435a15dcc38f`  
		Last Modified: Fri, 11 Mar 2022 04:03:46 GMT  
		Size: 18.6 KB (18598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86bb1285cae11648274513dd55a891e1ca7f14ee80070d95daeae0521db77da`  
		Last Modified: Fri, 11 Mar 2022 05:03:53 GMT  
		Size: 34.9 MB (34887464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e94752314a819cf5f190758a33d2f4d2a3dbde007de6249f275621e5ef423f8`  
		Last Modified: Fri, 11 Mar 2022 05:03:49 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ffe7b695380f1c31a8200b263d206389b1cf9117d2a11fd0e6bfc24f1e942a`  
		Last Modified: Wed, 16 Mar 2022 17:42:49 GMT  
		Size: 4.2 MB (4191968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d40d17a09a360286b6e38702644ca38fb0c0726399c1ad778a4d9f6491eb518`  
		Last Modified: Wed, 16 Mar 2022 17:42:49 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8460fa71b15c5f0aa3bd56ccea29886a800bbb4642cb363ace43b94885fd7d`  
		Last Modified: Wed, 16 Mar 2022 17:42:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
