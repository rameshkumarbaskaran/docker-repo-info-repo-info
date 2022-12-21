## `ruby:2-slim-buster`

```console
$ docker pull ruby@sha256:8801e0e85e5ed00e89d7960c67835cd98db3070d2b415bf341e4c8209e522de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `ruby:2-slim-buster` - linux; amd64

```console
$ docker pull ruby@sha256:4fcd5a033b11c91b38c28550621d68da5fb72f00c907b17889f1c19d13545bbe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54274283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfd0fa4b24490741f5fdfee5c245162dc657c147640c5e0aae9a3e79a0ff601`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:52 GMT
ADD file:660e0093a3da49e4ca41260d09d585754ccb1eff8974c4b0dd4456b76ddbbc9a in / 
# Wed, 21 Dec 2022 01:20:52 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 10:11:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 10:11:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 21 Dec 2022 10:11:20 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 10:26:50 GMT
ENV RUBY_MAJOR=2.7
# Wed, 21 Dec 2022 10:26:50 GMT
ENV RUBY_VERSION=2.7.7
# Wed, 21 Dec 2022 10:26:50 GMT
ENV RUBY_DOWNLOAD_SHA256=b38dff2e1f8ce6e5b7d433f8758752987a6b2adfd9bc7571dbc42ea5d04e3e4c
# Wed, 21 Dec 2022 10:28:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 21 Dec 2022 10:28:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 21 Dec 2022 10:28:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 21 Dec 2022 10:28:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 10:28:42 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 21 Dec 2022 10:28:42 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:b52ebda398ed2c4602ea06056f78d45a59474ee4e2a020967251ba082424e7e2`  
		Last Modified: Wed, 21 Dec 2022 01:25:17 GMT  
		Size: 27.1 MB (27140331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a0731f8ed30e93285ab536619b2e29c352f6d83976575ded07c10778f8f677`  
		Last Modified: Wed, 21 Dec 2022 10:30:39 GMT  
		Size: 12.6 MB (12577165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d51d41214c6d8e5cf40ddd704242e1016ed0fa0ad3462a3ceba68dbaca4411c`  
		Last Modified: Wed, 21 Dec 2022 10:30:37 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc17dbe7f65adc6a2978c43a91bbb854f2581d2b4f8aa8e4f2c6162622d37b64`  
		Last Modified: Wed, 21 Dec 2022 10:32:30 GMT  
		Size: 14.6 MB (14556410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d75a4a93c459efd3292a5cce44f2a44794ec237a9301e526ae661c83b4d07d`  
		Last Modified: Wed, 21 Dec 2022 10:32:28 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-slim-buster` - linux; arm variant v7

```console
$ docker pull ruby@sha256:f6707e22372fe58971a0879644731951be2d8c0e9ca65b257ac393721d1767e7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46432309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76c73b37d7b8019d0c031a46866c508a0b4e1cc5fc09de764aa7dd1925edcc2`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 06 Dec 2022 00:59:27 GMT
ADD file:be297820b3c24f32c3d19e62f8aad3c9d2b37db08077869258a7d3aba92f555f in / 
# Tue, 06 Dec 2022 00:59:27 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 12:55:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 12:55:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 06 Dec 2022 12:55:08 GMT
ENV LANG=C.UTF-8
# Tue, 06 Dec 2022 13:22:25 GMT
ENV RUBY_MAJOR=2.7
# Tue, 06 Dec 2022 13:22:25 GMT
ENV RUBY_VERSION=2.7.7
# Tue, 06 Dec 2022 13:22:25 GMT
ENV RUBY_DOWNLOAD_SHA256=b38dff2e1f8ce6e5b7d433f8758752987a6b2adfd9bc7571dbc42ea5d04e3e4c
# Tue, 06 Dec 2022 13:24:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 06 Dec 2022 13:24:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 06 Dec 2022 13:24:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 06 Dec 2022 13:24:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 13:24:12 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 06 Dec 2022 13:24:12 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:f2a5c00904a21a940a9e4ec3efaca80bebbbf2775e4c9bbe0ce9c05e967335f0`  
		Last Modified: Tue, 06 Dec 2022 01:06:56 GMT  
		Size: 22.7 MB (22748937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e138850031fd06d42cd30fd7a9800276bfa6f28357072e3a6ed2893849733ed`  
		Last Modified: Tue, 06 Dec 2022 13:29:27 GMT  
		Size: 9.9 MB (9877008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a29ce59a259a2f82616b5ee3a6d2705c2295e56196f6ab7f454bc639bdb7c75`  
		Last Modified: Tue, 06 Dec 2022 13:29:24 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a851624f7da52cf7c2a3e3856367c88c772a3ca05c2b0f89a84f84dbbfb98ae`  
		Last Modified: Tue, 06 Dec 2022 13:34:03 GMT  
		Size: 13.8 MB (13806023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e997105958295bad6cb00ceb1721f2d60e5caa55cd82cec3a8190d478ddc783`  
		Last Modified: Tue, 06 Dec 2022 13:34:01 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-slim-buster` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:187d5b9c71f7cf89b4a38631e0a662b6f9a6dfb24706e6c4f6d41b075a0b4ad8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51597679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160d4b4f445eeb38dcc32c261d69be8c678a4214f2f427680766caf15b7c8031`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:34 GMT
ADD file:764288ad3920160093c500e1a7277f174a656030bbe3a0511e7925e84495b6ee in / 
# Tue, 06 Dec 2022 01:40:34 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 13:04:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 13:04:13 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 06 Dec 2022 13:04:13 GMT
ENV LANG=C.UTF-8
# Tue, 06 Dec 2022 13:23:39 GMT
ENV RUBY_MAJOR=2.7
# Tue, 06 Dec 2022 13:23:39 GMT
ENV RUBY_VERSION=2.7.7
# Tue, 06 Dec 2022 13:23:39 GMT
ENV RUBY_DOWNLOAD_SHA256=b38dff2e1f8ce6e5b7d433f8758752987a6b2adfd9bc7571dbc42ea5d04e3e4c
# Tue, 06 Dec 2022 13:24:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 06 Dec 2022 13:24:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 06 Dec 2022 13:24:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 06 Dec 2022 13:24:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 13:24:59 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 06 Dec 2022 13:24:59 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:b473b36a3d93c888196b326b1aad1f802bb6a9fa6fcbc5d2614d99a67899d587`  
		Last Modified: Tue, 06 Dec 2022 01:44:33 GMT  
		Size: 25.9 MB (25914951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d04e2ad874390894f69252214538009bbb7fb124c5bfc4bb0aebe7a7d5ef4c`  
		Last Modified: Tue, 06 Dec 2022 13:27:12 GMT  
		Size: 11.3 MB (11281771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0970f60b91a9552716ff454f0733e9956e99b038280f37d58d37b1cf27dc6b88`  
		Last Modified: Tue, 06 Dec 2022 13:27:10 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5249aeafea9c2993b5a8fb7d254a171c997c9ad2770b4a638690045b6e861e5e`  
		Last Modified: Tue, 06 Dec 2022 13:30:27 GMT  
		Size: 14.4 MB (14400584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449d04612932d05adfe44efbc2c373750b40b7b93657534f592c290b2ea946d6`  
		Last Modified: Tue, 06 Dec 2022 13:30:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-slim-buster` - linux; 386

```console
$ docker pull ruby@sha256:5e680622518f59242df31abb2016e2591a64ae6eda243bac90f987349683e39a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58855066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b55c569d926d2e173a4f52420dd6ec3543ed1774477b56823a0d60bedfbd90b`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:45 GMT
ADD file:48a2a0e6cb166df412bb4f6ad30537c66bc6be97ce4c8fc582fd5ac8c6129b5a in / 
# Wed, 21 Dec 2022 01:39:46 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 06:46:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 06:46:40 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 21 Dec 2022 06:46:41 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 07:01:51 GMT
ENV RUBY_MAJOR=2.7
# Wed, 21 Dec 2022 07:01:52 GMT
ENV RUBY_VERSION=2.7.7
# Wed, 21 Dec 2022 07:01:53 GMT
ENV RUBY_DOWNLOAD_SHA256=b38dff2e1f8ce6e5b7d433f8758752987a6b2adfd9bc7571dbc42ea5d04e3e4c
# Wed, 21 Dec 2022 07:03:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 21 Dec 2022 07:03:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 21 Dec 2022 07:03:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 21 Dec 2022 07:03:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 07:03:37 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 21 Dec 2022 07:03:38 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:9099d8a02dc0a7901931d2811fa3078b18ecd3a40a156cbcfd91629126463f80`  
		Last Modified: Wed, 21 Dec 2022 01:45:34 GMT  
		Size: 27.8 MB (27798412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d81f06faaaa5c3748d9a1bc50ee0d30fd8158ba214b2670ffa0f44a7464618`  
		Last Modified: Wed, 21 Dec 2022 07:07:09 GMT  
		Size: 17.2 MB (17238286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f1cfcc30ecb2465e850f75f09d4547488a1e5a190387b2b01ce1939c594f89`  
		Last Modified: Wed, 21 Dec 2022 07:07:06 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781ae6636762a59c542018632d0625e5f53702ff450ece8c8e5f40e3abaff75c`  
		Last Modified: Wed, 21 Dec 2022 07:10:06 GMT  
		Size: 13.8 MB (13818024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f464840675914601d39536c13c0aa398b4b6367abfd19173905a2d0ac4edf66`  
		Last Modified: Wed, 21 Dec 2022 07:10:03 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
