## `ruby:3-slim-bullseye`

```console
$ docker pull ruby@sha256:a6f940b1fca8a057561ac86f431539df2e77b954370fa17348f5a5ec3cba1cad
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

### `ruby:3-slim-bullseye` - linux; amd64

```console
$ docker pull ruby@sha256:30b4cd94bde74b6e8306eaa89d5c0778a8309e3a16211cadd189a42f5c2fa116
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74039878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709708401a1622438fc5d3996315a1d3fb40bb9abd0dafedd9a41a7b52a44d1f`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 07:19:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 07:19:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 06 Dec 2022 07:19:07 GMT
ENV LANG=C.UTF-8
# Tue, 06 Dec 2022 07:28:36 GMT
ENV RUBY_MAJOR=3.1
# Tue, 06 Dec 2022 07:28:36 GMT
ENV RUBY_VERSION=3.1.3
# Tue, 06 Dec 2022 07:28:36 GMT
ENV RUBY_DOWNLOAD_SHA256=4ee161939826bcdfdafa757cf8e293a7f14e357f62be7144f040335cc8c7371a
# Tue, 06 Dec 2022 07:31:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 06 Dec 2022 07:31:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 06 Dec 2022 07:31:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 06 Dec 2022 07:31:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 07:31:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 06 Dec 2022 07:31:01 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38088d9956b40c7d776d5ee0a83ee896973fad2ed2e24c8457dfe6b2c1ae9942`  
		Last Modified: Tue, 06 Dec 2022 07:53:54 GMT  
		Size: 10.0 MB (10020445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d38057832a88023db4a7ac889f9422781f216f84e067edcae536466324692f`  
		Last Modified: Tue, 06 Dec 2022 07:53:52 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7dc7d4893198a277b328e9b5ea028f6d9b0ecd7d1818b1516d301749e422ff`  
		Last Modified: Tue, 06 Dec 2022 07:55:00 GMT  
		Size: 32.6 MB (32606207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542155ce77858af57ef566fd6546f83963e0c3ea667269abb0f27ee121074341`  
		Last Modified: Tue, 06 Dec 2022 07:54:56 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim-bullseye` - linux; arm variant v5

```console
$ docker pull ruby@sha256:c9f3270c40efb33b9dbd14e0e6c8af13509ac745baeafc6a1c1e2b982cfbe10e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68692917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f94d746cde23b086c1521a6b5859030bba7ed19554d648030471f80b563ea4`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 06 Dec 2022 01:49:26 GMT
ADD file:3333e32449573e158be62ea6948788daec95a151f49035d65db8d7cb72b42c53 in / 
# Tue, 06 Dec 2022 01:49:27 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:19:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 10:19:28 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 06 Dec 2022 10:19:28 GMT
ENV LANG=C.UTF-8
# Tue, 06 Dec 2022 10:24:54 GMT
ENV RUBY_MAJOR=3.1
# Tue, 06 Dec 2022 10:24:55 GMT
ENV RUBY_VERSION=3.1.3
# Tue, 06 Dec 2022 10:24:55 GMT
ENV RUBY_DOWNLOAD_SHA256=4ee161939826bcdfdafa757cf8e293a7f14e357f62be7144f040335cc8c7371a
# Tue, 06 Dec 2022 10:27:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 06 Dec 2022 10:27:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 06 Dec 2022 10:27:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 06 Dec 2022 10:27:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 10:27:49 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 06 Dec 2022 10:27:49 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:98c2ef299f89748b9c6075c728521ba8fe6e236fa46f50c465894cdb0ce69b35`  
		Last Modified: Tue, 06 Dec 2022 01:54:34 GMT  
		Size: 28.9 MB (28914353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07d1724c3beb96ef9e6fc89d62b5749a243e534faa8b2eb1fd03c295982eb37`  
		Last Modified: Tue, 06 Dec 2022 10:40:17 GMT  
		Size: 8.6 MB (8634335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fae12e7d2937a507e7bb217a500e7b36e65d8a7551d822aa88d07b5376fbef1`  
		Last Modified: Tue, 06 Dec 2022 10:40:15 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ea0e3fcb3a587b629f2f5cc6b196140a96891d7b49e6f07b332987169d03cb`  
		Last Modified: Tue, 06 Dec 2022 10:41:13 GMT  
		Size: 31.1 MB (31143887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3172a36f9ffa006e6f8ce76f491f472c24884fc7a4515a8716030adaa6490cc`  
		Last Modified: Tue, 06 Dec 2022 10:41:09 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim-bullseye` - linux; arm variant v7

```console
$ docker pull ruby@sha256:015906bedb96a84724be70f2d415c244e3a2473a77ef306b53d98f477d2a5eca
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65739248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30908da249fc5bce6753e5ecd2bbede56f7e798c43757049c4ff62ad293e38b3`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 12:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 12:50:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 06 Dec 2022 12:50:12 GMT
ENV LANG=C.UTF-8
# Tue, 06 Dec 2022 13:00:05 GMT
ENV RUBY_MAJOR=3.1
# Tue, 06 Dec 2022 13:00:05 GMT
ENV RUBY_VERSION=3.1.3
# Tue, 06 Dec 2022 13:00:05 GMT
ENV RUBY_DOWNLOAD_SHA256=4ee161939826bcdfdafa757cf8e293a7f14e357f62be7144f040335cc8c7371a
# Tue, 06 Dec 2022 13:02:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 06 Dec 2022 13:02:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 06 Dec 2022 13:02:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 06 Dec 2022 13:02:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 13:02:25 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 06 Dec 2022 13:02:25 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1829ddfbb7412785849a7bc642891c9941e4405c63bce3ed75b5baf09db48e53`  
		Last Modified: Tue, 06 Dec 2022 13:28:43 GMT  
		Size: 8.1 MB (8142816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d76deae3c66382a31903668fef3c6d6d1eec2332c431b39a892e65c133c4d3`  
		Last Modified: Tue, 06 Dec 2022 13:28:40 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e61666cd5577e332b7b95673f6a9e4c1866afff94adddb6956c4fe5502435a`  
		Last Modified: Tue, 06 Dec 2022 13:30:23 GMT  
		Size: 31.0 MB (31019743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c80fa884adb20fae43157bd05c90caed0703e3a8bef3787880ec7d8122b6eb`  
		Last Modified: Tue, 06 Dec 2022 13:30:18 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:eb6146c70ab31362336031885c2a445987021a2b3210aa5c577d8e21dd279f99
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71266805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33111851fbf35176652284c8ba2c547762870a0fa409f2555aadde0385e49378`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 13:00:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 13:00:27 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 06 Dec 2022 13:00:27 GMT
ENV LANG=C.UTF-8
# Tue, 06 Dec 2022 13:07:41 GMT
ENV RUBY_MAJOR=3.1
# Tue, 06 Dec 2022 13:07:41 GMT
ENV RUBY_VERSION=3.1.3
# Tue, 06 Dec 2022 13:07:41 GMT
ENV RUBY_DOWNLOAD_SHA256=4ee161939826bcdfdafa757cf8e293a7f14e357f62be7144f040335cc8c7371a
# Tue, 06 Dec 2022 13:09:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 06 Dec 2022 13:09:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 06 Dec 2022 13:09:23 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 06 Dec 2022 13:09:23 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 13:09:24 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 06 Dec 2022 13:09:24 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b35d881fa3be42425d38e36b65b32fe285d7d74b7a772e62b932aa139d3f0c`  
		Last Modified: Tue, 06 Dec 2022 13:26:45 GMT  
		Size: 9.2 MB (9242670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb3dfae78a18073ac38d4f8ef7719f44ea19e4e38b67d02f68c496b097fc41e`  
		Last Modified: Tue, 06 Dec 2022 13:26:43 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c67fe65949c57d7e42409c0e5da28aea12c8021cf8506d234fe260ea6d7872`  
		Last Modified: Tue, 06 Dec 2022 13:27:50 GMT  
		Size: 32.0 MB (31963442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7080b7370f3c7baf1e114a3951d2fd1998f680024fdd1d1f1479b5f6452698cd`  
		Last Modified: Tue, 06 Dec 2022 13:27:47 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim-bullseye` - linux; 386

```console
$ docker pull ruby@sha256:48305d3accdd3682fee1c8ad11a52fa30f74f406a9a45f99adc6e34b0b7f09e2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75130631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019a52b1d864bbeb76efa9f1ac3072bc0c2345a2220d1f7efd3b2e7f66ed7c93`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 06 Dec 2022 01:39:52 GMT
ADD file:3912079114d3e8e334fdf795a4793a492f37989804e1148b98fafbd4eaa00b7e in / 
# Tue, 06 Dec 2022 01:39:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 16:10:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 16:10:42 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 06 Dec 2022 16:10:42 GMT
ENV LANG=C.UTF-8
# Tue, 06 Dec 2022 16:20:30 GMT
ENV RUBY_MAJOR=3.1
# Tue, 06 Dec 2022 16:20:31 GMT
ENV RUBY_VERSION=3.1.3
# Tue, 06 Dec 2022 16:20:32 GMT
ENV RUBY_DOWNLOAD_SHA256=4ee161939826bcdfdafa757cf8e293a7f14e357f62be7144f040335cc8c7371a
# Tue, 06 Dec 2022 16:22:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 06 Dec 2022 16:22:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 06 Dec 2022 16:22:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 06 Dec 2022 16:22:49 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 16:22:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 06 Dec 2022 16:22:51 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:01cb95e209fce595702ddb2b5ed266e2a01b6687efe67d201d74a5aee9595995`  
		Last Modified: Tue, 06 Dec 2022 01:45:41 GMT  
		Size: 32.4 MB (32393046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca384dd6a73eee035883553041cebb38bc84a3d2d5c9843f7b1f933863fcb5f7`  
		Last Modified: Tue, 06 Dec 2022 16:47:37 GMT  
		Size: 11.8 MB (11788280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc77a7a274ce31f64644ada4ab011a7a40ec1276d0618cd07871bb859c2046db`  
		Last Modified: Tue, 06 Dec 2022 16:47:35 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c074e75f3a0d9af5df34dc5884935d2b5e01692efe51298e3b5fdbdd27b1fa32`  
		Last Modified: Tue, 06 Dec 2022 16:49:09 GMT  
		Size: 30.9 MB (30948964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b29fd04593371ba0c12c006c1ea55b74a1c3acb2ad1034d27d8c53de019065`  
		Last Modified: Tue, 06 Dec 2022 16:49:07 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim-bullseye` - linux; mips64le

```console
$ docker pull ruby@sha256:a8abf40a6094512e2a12415b56fd22057198fd53b1f780eb218d7f1e7ef92500
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71533904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20794f1c35ff7e8d90fec7c7699bcb58438dca4e26e0bde82d9e3e836a2a2f7d`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 06 Dec 2022 01:55:32 GMT
ADD file:d8937be4ad87f6bed7208bb29e2f735fd2a0b27daa20617862416d53a6b9ff89 in / 
# Tue, 06 Dec 2022 01:55:36 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 16:12:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 16:12:47 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 06 Dec 2022 16:12:50 GMT
ENV LANG=C.UTF-8
# Tue, 06 Dec 2022 16:26:30 GMT
ENV RUBY_MAJOR=3.1
# Tue, 06 Dec 2022 16:26:32 GMT
ENV RUBY_VERSION=3.1.3
# Tue, 06 Dec 2022 16:26:35 GMT
ENV RUBY_DOWNLOAD_SHA256=4ee161939826bcdfdafa757cf8e293a7f14e357f62be7144f040335cc8c7371a
# Tue, 06 Dec 2022 16:39:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 06 Dec 2022 16:39:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 06 Dec 2022 16:39:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 06 Dec 2022 16:39:34 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 16:39:39 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 06 Dec 2022 16:39:42 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:6311b5f9f3fe3987fe4883793179a21fe55ebdadf1eed52849d93fba8258d036`  
		Last Modified: Tue, 06 Dec 2022 02:03:40 GMT  
		Size: 29.6 MB (29635557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6031b414f82405f4beecd5f418439a78feece39952230b01f3967033b267e119`  
		Last Modified: Tue, 06 Dec 2022 17:03:28 GMT  
		Size: 9.6 MB (9628818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45b094f1056a5c8892628b5f021445516b367c556d676f9cb3a69ac48697fc6`  
		Last Modified: Tue, 06 Dec 2022 17:03:19 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b2397e02345698f22a7fa85f1fc98eb0ffd169bdf3ce9019a1b3f4409820425`  
		Last Modified: Tue, 06 Dec 2022 17:04:02 GMT  
		Size: 32.3 MB (32269189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe95949e93cf6b1d1e65c93214209210b0d11d7dde2d0dfe1a3d6e25b05fee5`  
		Last Modified: Tue, 06 Dec 2022 17:03:48 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim-bullseye` - linux; ppc64le

```console
$ docker pull ruby@sha256:8763e67641d88103a72619f1394cfec23b06d37d2aedf1423b971a3bf30cad82
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78539071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a28dd6df487db899cc3f4716d2d18ab19f7cab75f6012b15db91d0ebcb2f81a`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 06 Dec 2022 01:18:04 GMT
ADD file:2231a44ea52d93df58e23883ba6b6911d4c554f4c1d172d80fb21c751ddcbbfc in / 
# Tue, 06 Dec 2022 01:18:06 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 09:35:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 09:35:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 06 Dec 2022 09:35:48 GMT
ENV LANG=C.UTF-8
# Tue, 06 Dec 2022 09:43:01 GMT
ENV RUBY_MAJOR=3.1
# Tue, 06 Dec 2022 09:43:01 GMT
ENV RUBY_VERSION=3.1.3
# Tue, 06 Dec 2022 09:43:02 GMT
ENV RUBY_DOWNLOAD_SHA256=4ee161939826bcdfdafa757cf8e293a7f14e357f62be7144f040335cc8c7371a
# Tue, 06 Dec 2022 09:47:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 06 Dec 2022 09:47:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 06 Dec 2022 09:47:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 06 Dec 2022 09:47:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 09:47:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 06 Dec 2022 09:47:16 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1f72e1168976861c676bf86a6c149129baba7e13200e8b70e6f24dc2ac2797df`  
		Last Modified: Tue, 06 Dec 2022 01:24:18 GMT  
		Size: 35.3 MB (35285293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fcb5a302d4619db0220eecbb90cb7cf33297235cdec6cae64a7cb030cdeae4c`  
		Last Modified: Tue, 06 Dec 2022 10:03:35 GMT  
		Size: 10.5 MB (10478730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf885d002681bd6d3d6e8d2f966f5c691791a7ea93fa44205582b2fd53eb3a89`  
		Last Modified: Tue, 06 Dec 2022 10:03:31 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8309f6fcca41caa6d19a2210dac23646c13a8306fb49dabdaf33c547d089f6e0`  
		Last Modified: Tue, 06 Dec 2022 10:04:39 GMT  
		Size: 32.8 MB (32774673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78754ffb6dba7787a1ab454ece614e1ee04be6e99862c1fca7195b66c22c691a`  
		Last Modified: Tue, 06 Dec 2022 10:04:33 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim-bullseye` - linux; s390x

```console
$ docker pull ruby@sha256:80d56ff0b1bfdb311e8fb1133608b7922c53216052b68175616a91095f1aa09a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70939870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0617cfb216c5530ddebd7cc3fde226c30fc0753fd6c4e7d84401c85906d89df4`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 06 Dec 2022 01:43:03 GMT
ADD file:f9243ad65309c3c458bf646b21aced55c055f7601340b3bda80ec30ff2f62159 in / 
# Tue, 06 Dec 2022 01:43:06 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 08:59:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 08:59:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 06 Dec 2022 08:59:11 GMT
ENV LANG=C.UTF-8
# Tue, 06 Dec 2022 09:03:54 GMT
ENV RUBY_MAJOR=3.1
# Tue, 06 Dec 2022 09:03:54 GMT
ENV RUBY_VERSION=3.1.3
# Tue, 06 Dec 2022 09:03:54 GMT
ENV RUBY_DOWNLOAD_SHA256=4ee161939826bcdfdafa757cf8e293a7f14e357f62be7144f040335cc8c7371a
# Tue, 06 Dec 2022 09:06:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 06 Dec 2022 09:06:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 06 Dec 2022 09:06:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 06 Dec 2022 09:06:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 09:06:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 06 Dec 2022 09:06:15 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:66bc250ceea32b3e395aec7bb63aad4ac079791df67a2732692841e8dfacac94`  
		Last Modified: Tue, 06 Dec 2022 01:48:46 GMT  
		Size: 29.6 MB (29643886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcedca7090b02174d371584f338961ea7125b9eafcca16002f30da20b11fe038`  
		Last Modified: Tue, 06 Dec 2022 09:17:45 GMT  
		Size: 8.9 MB (8860458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c489d19258344bcdaa22006c6e90255a9dcd78995f94b04f8fb03ec6efdb33`  
		Last Modified: Tue, 06 Dec 2022 09:17:44 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b38e1050995be22b564523363bcb3d6624ad3aacbb4970a3c6e896e28ee1ca`  
		Last Modified: Tue, 06 Dec 2022 09:18:23 GMT  
		Size: 32.4 MB (32435153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d39abc91201a9a9a172da44c981f5f51eea49c8d6f482d7d11f4b43f83c484f`  
		Last Modified: Tue, 06 Dec 2022 09:18:21 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
