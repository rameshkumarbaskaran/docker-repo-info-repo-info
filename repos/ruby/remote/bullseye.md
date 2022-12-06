## `ruby:bullseye`

```console
$ docker pull ruby@sha256:afe3f824abb21acbac2626125fd0270b8c524c0b4a4c37d2a0399a2362a9c59d
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

### `ruby:bullseye` - linux; amd64

```console
$ docker pull ruby@sha256:5095f713abe888ea8e3b779422647ed92d668839bb50c5578dab032525bf08af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.1 MB (355133996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6d28bea2625f3168547e4d86baf1030f2f94ac3cadba2b3b13dffd32bcc7f20`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:41 GMT
ADD file:553d20b03d45305e58cde07e0c259421bba044155ac90b4559e5cc0b69093347 in / 
# Tue, 06 Dec 2022 01:20:41 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:13:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:13:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 06 Dec 2022 02:13:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:14:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 07:16:50 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 06 Dec 2022 07:16:50 GMT
ENV LANG=C.UTF-8
# Tue, 06 Dec 2022 07:26:28 GMT
ENV RUBY_MAJOR=3.1
# Tue, 06 Dec 2022 07:26:28 GMT
ENV RUBY_VERSION=3.1.3
# Tue, 06 Dec 2022 07:26:28 GMT
ENV RUBY_DOWNLOAD_SHA256=4ee161939826bcdfdafa757cf8e293a7f14e357f62be7144f040335cc8c7371a
# Tue, 06 Dec 2022 07:28:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 06 Dec 2022 07:28:29 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 06 Dec 2022 07:28:29 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 06 Dec 2022 07:28:29 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 07:28:30 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 06 Dec 2022 07:28:30 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:f2f58072e9ed1aa1b0143341c5ee83815c00ce47548309fa240155067ab0e698`  
		Last Modified: Tue, 06 Dec 2022 01:24:48 GMT  
		Size: 55.0 MB (55041342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8cfbf51e6e6869f1af2a1e7067b07fd6733036a333c9d29f743b0285e26037`  
		Last Modified: Tue, 06 Dec 2022 02:21:44 GMT  
		Size: 5.2 MB (5164910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3a609d15798d35c1484072876b7d22a316e98de6a097de33b9dade6a689cd1`  
		Last Modified: Tue, 06 Dec 2022 02:21:44 GMT  
		Size: 10.9 MB (10877423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094e7d9bb04ebf214ea8dc5a488995449684104ae8ad9603bf061cac0d18eb54`  
		Last Modified: Tue, 06 Dec 2022 02:22:02 GMT  
		Size: 54.6 MB (54587090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbfd734f3824a4390fe4be45f6a11a5543bca1023e4814d72460eaebc2eef89`  
		Last Modified: Tue, 06 Dec 2022 02:22:38 GMT  
		Size: 196.9 MB (196869178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2936016f200481588546702954935dd4177e48a7f3d8226bf483a49206e18c93`  
		Last Modified: Tue, 06 Dec 2022 07:53:37 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce016929bbe1642adb8607e8ea50ad41ce73375f2edcddcfee98dc18127221f`  
		Last Modified: Tue, 06 Dec 2022 07:54:36 GMT  
		Size: 32.6 MB (32593679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5c0c08cfdfe9df95b46d6f692876b34ef0aa6a14d32438c4d7bbbef7ec5fc1`  
		Last Modified: Tue, 06 Dec 2022 07:54:32 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:bullseye` - linux; arm variant v5

```console
$ docker pull ruby@sha256:4eeb1b999c3d65a2658c1d4e6039baf03c58b52f6244d856800220c9c0de8432
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.7 MB (326711844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b090edca654b1da4a1abfa34704b3394a631264a3c9c32389c137adbbf919a`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 06 Dec 2022 01:49:07 GMT
ADD file:92bc802977fb4abf65d3a11a702509aece192d088d815bf79a0e6bdb5a8b57c8 in / 
# Tue, 06 Dec 2022 01:49:08 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:16:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:16:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 06 Dec 2022 02:17:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:18:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 10:16:47 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 06 Dec 2022 10:16:47 GMT
ENV LANG=C.UTF-8
# Tue, 06 Dec 2022 10:22:11 GMT
ENV RUBY_MAJOR=3.1
# Tue, 06 Dec 2022 10:22:11 GMT
ENV RUBY_VERSION=3.1.3
# Tue, 06 Dec 2022 10:22:12 GMT
ENV RUBY_DOWNLOAD_SHA256=4ee161939826bcdfdafa757cf8e293a7f14e357f62be7144f040335cc8c7371a
# Tue, 06 Dec 2022 10:24:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 06 Dec 2022 10:24:40 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 06 Dec 2022 10:24:40 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 06 Dec 2022 10:24:40 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 10:24:41 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 06 Dec 2022 10:24:41 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0eeca4d47a0d9a966ac355f8eb8d728ca02c90f2db97fac6164fb9dd7eee639f`  
		Last Modified: Tue, 06 Dec 2022 01:54:02 GMT  
		Size: 52.5 MB (52544799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c330e998bf60345da71330a458334a9904ec525dcfd0b830b9ff405076e5e9f`  
		Last Modified: Tue, 06 Dec 2022 02:23:07 GMT  
		Size: 5.1 MB (5072274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a963630613496775b31748fdc26130adc20eebd435f6c83acf2d9901566ec2f5`  
		Last Modified: Tue, 06 Dec 2022 02:23:07 GMT  
		Size: 10.6 MB (10574287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e44d8829d6a73032763e8aefb6237c9972206128230789679a163bc113c6fbc`  
		Last Modified: Tue, 06 Dec 2022 02:23:32 GMT  
		Size: 52.3 MB (52322314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be2b372bdbc9c1a8b0e596c98992c98c67ccb38fd56fceaf2a27e9dbfb4ff1b`  
		Last Modified: Tue, 06 Dec 2022 02:24:14 GMT  
		Size: 175.0 MB (175043908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a920576475453b809a033826e5c5c824173b0c3583af7367ad4a90b20139a739`  
		Last Modified: Tue, 06 Dec 2022 10:39:54 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108473eefb627239b1f5b094b55c792a3becaff3ca7d0274f23557782d2d21d8`  
		Last Modified: Tue, 06 Dec 2022 10:40:40 GMT  
		Size: 31.2 MB (31153921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc88c49bb1726e7669bd6d275d1541e6cf4b3ccc2ab4cb3ddcfb37b993ab602`  
		Last Modified: Tue, 06 Dec 2022 10:40:36 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:bullseye` - linux; arm variant v7

```console
$ docker pull ruby@sha256:ac2093b9ee355697fb115bca0fb612032b42e26012b926a1aec558fed0383749
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314053388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc087cdddcb84a6dabb449cae6afe119e7c68d0b5ae1ec5f2ff75eac07704404`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:30 GMT
ADD file:72eaf12ec65c98e9cde1654b6adb2b3d19f7d81c13b12801c198f699252b7503 in / 
# Tue, 06 Dec 2022 00:58:31 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 09:49:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 09:49:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 06 Dec 2022 09:49:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 09:50:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 12:47:40 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 06 Dec 2022 12:47:40 GMT
ENV LANG=C.UTF-8
# Tue, 06 Dec 2022 12:57:53 GMT
ENV RUBY_MAJOR=3.1
# Tue, 06 Dec 2022 12:57:53 GMT
ENV RUBY_VERSION=3.1.3
# Tue, 06 Dec 2022 12:57:53 GMT
ENV RUBY_DOWNLOAD_SHA256=4ee161939826bcdfdafa757cf8e293a7f14e357f62be7144f040335cc8c7371a
# Tue, 06 Dec 2022 12:59:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 06 Dec 2022 12:59:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 06 Dec 2022 12:59:52 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 06 Dec 2022 12:59:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 12:59:53 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 06 Dec 2022 12:59:53 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:58e27900c24f1f8f5b6b5eacbc073583f2372b58e9f5678dfe171b496b9cd71e`  
		Last Modified: Tue, 06 Dec 2022 01:05:33 GMT  
		Size: 50.2 MB (50207085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3975e0b03a66ba4371cf2cae58e77e148d952679dd5fa1e322124604805fc6a2`  
		Last Modified: Tue, 06 Dec 2022 09:59:29 GMT  
		Size: 4.9 MB (4932853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806632ddd1d79b55318482c725338dc97649f22ca0ec8dbdf79cc8be451201eb`  
		Last Modified: Tue, 06 Dec 2022 09:59:30 GMT  
		Size: 10.2 MB (10218527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27a60e772b69f3ec8f0fa174be2d19682bdea3265044f5d56ef14d491b7457d`  
		Last Modified: Tue, 06 Dec 2022 09:59:52 GMT  
		Size: 50.3 MB (50343382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e04b2aeec198d646729a6325c306ec02ff477eb96ef1b46334c5c18a5a6917`  
		Last Modified: Tue, 06 Dec 2022 10:00:35 GMT  
		Size: 167.3 MB (167311847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17731434c347dda9bd9bbfec8eea7a73d5b421bf567dd6ff53d0e158be2aef4`  
		Last Modified: Tue, 06 Dec 2022 13:28:19 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bef28b3ca125f51964366e150fd4093f352f34c1faabf2ff20a5a2b56ea07ae`  
		Last Modified: Tue, 06 Dec 2022 13:29:48 GMT  
		Size: 31.0 MB (31039354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b741e108d9bab7eb1e12ff54ddb7c50e70351b020213117e84e6b61b7401cbf`  
		Last Modified: Tue, 06 Dec 2022 13:29:44 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:bullseye` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:030eaf505bc7d39bfe1c485762603a95b5d43277f98cd3334d85e84547073abb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.1 MB (346115259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6560307bd5048acc0b40b54ccf4838666437d3d9d9c16d8a935b2024cea7f69c`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:06 GMT
ADD file:b1e7652678bbfc9556636e77d79c947ff1436888e2929f9c5c3ddb42a50c1176 in / 
# Tue, 06 Dec 2022 01:40:07 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:04:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:05:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 06 Dec 2022 02:05:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:06:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 12:58:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 06 Dec 2022 12:58:44 GMT
ENV LANG=C.UTF-8
# Tue, 06 Dec 2022 13:06:03 GMT
ENV RUBY_MAJOR=3.1
# Tue, 06 Dec 2022 13:06:03 GMT
ENV RUBY_VERSION=3.1.3
# Tue, 06 Dec 2022 13:06:04 GMT
ENV RUBY_DOWNLOAD_SHA256=4ee161939826bcdfdafa757cf8e293a7f14e357f62be7144f040335cc8c7371a
# Tue, 06 Dec 2022 13:07:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 06 Dec 2022 13:07:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 06 Dec 2022 13:07:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 06 Dec 2022 13:07:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 13:07:31 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 06 Dec 2022 13:07:31 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:4948a51a9a3f176f30ac619014f4a2da453a943244eacb53096ee9742eb7cef1`  
		Last Modified: Tue, 06 Dec 2022 01:43:33 GMT  
		Size: 53.7 MB (53699146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4da1b3775b3318d613abab2fd069341bb11e4a0203d0711f880b6e7b63d9999`  
		Last Modified: Tue, 06 Dec 2022 02:11:52 GMT  
		Size: 5.2 MB (5151568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efc1b20f4359d8f8eee08a338da8190d7ad6f077920c5a52e6e90cc72cfe32a`  
		Last Modified: Tue, 06 Dec 2022 02:11:53 GMT  
		Size: 10.9 MB (10874189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c81e9b9b636d92370c81523d1cf3c317b12472aa823bfc41c2ca44b433b6434`  
		Last Modified: Tue, 06 Dec 2022 02:12:10 GMT  
		Size: 54.7 MB (54683580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169d1088f2f0583933252965d3d3949f75d046690274e18ee24c271371c2b4e6`  
		Last Modified: Tue, 06 Dec 2022 02:12:38 GMT  
		Size: 189.8 MB (189755391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c117cda25a7cc79bd632075f90c7c31cd905278a593a530926e3c38d5ebcac`  
		Last Modified: Tue, 06 Dec 2022 13:26:28 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4328c35ada9d517e05ed5f4cb4cbd1b1b5da9789f9fcf58e4d74a0a2c248f8`  
		Last Modified: Tue, 06 Dec 2022 13:27:26 GMT  
		Size: 32.0 MB (31951012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c7323a5fe9ff49c5e2b59f94bb9d866c4f61e967fc9073b445170742a3bc25`  
		Last Modified: Tue, 06 Dec 2022 13:27:24 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:bullseye` - linux; 386

```console
$ docker pull ruby@sha256:caacddf00060b02632d49c64b10de277f6135195579035cc04df7c3d8cb7ddaf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.7 MB (358736862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99a740870ad89e0b7d9b71ecd7318afb9328afea1b440c8263cdac1c9bb8351`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:11 GMT
ADD file:2962b9f6c2d1271d6b4d04e8eaf82fb990726e0593bbe685576851ef47447301 in / 
# Tue, 15 Nov 2022 01:41:11 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 07:03:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 07:03:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 15 Nov 2022 07:04:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 07:05:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 21:05:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 15 Nov 2022 21:05:18 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 21:09:59 GMT
ENV RUBY_MAJOR=3.1
# Fri, 25 Nov 2022 21:41:38 GMT
ENV RUBY_VERSION=3.1.3
# Fri, 25 Nov 2022 21:41:38 GMT
ENV RUBY_DOWNLOAD_SHA256=4ee161939826bcdfdafa757cf8e293a7f14e357f62be7144f040335cc8c7371a
# Fri, 25 Nov 2022 21:43:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 25 Nov 2022 21:43:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 25 Nov 2022 21:43:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 25 Nov 2022 21:43:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Nov 2022 21:43:37 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 25 Nov 2022 21:43:38 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:9c6907f3cae53506b5149dd6542c3e51b750fdf5adbe19d7e949974888503c1e`  
		Last Modified: Tue, 15 Nov 2022 01:46:36 GMT  
		Size: 56.0 MB (56020725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2336bc5de2024196f448b0076a64552ad91a769c80127a224f16c9a01fb8ff`  
		Last Modified: Tue, 15 Nov 2022 07:11:36 GMT  
		Size: 5.1 MB (5086828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be24ed5e811e8ae9e25d22e72f2576ffb0280f9f49e1656cdc09cfb11b66d6b5`  
		Last Modified: Tue, 15 Nov 2022 07:11:36 GMT  
		Size: 11.0 MB (11032596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788c522d11e2e9aea0bbbb34198dd62f693ab4ab7766284332dc210effc7357e`  
		Last Modified: Tue, 15 Nov 2022 07:11:56 GMT  
		Size: 55.9 MB (55924156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8faeb65e1f8e1dc13b5134e57d2e38f2ef54bac0a54aa8a3242f44b4d7beb78f`  
		Last Modified: Tue, 15 Nov 2022 07:12:35 GMT  
		Size: 199.8 MB (199769706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7194ab9aac5730e5f6583bccf1871d709c08c3373028406fc27035d2a2bd34df`  
		Last Modified: Tue, 15 Nov 2022 21:26:17 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4848db4b5ed27b3cea06602090f9bf1a0fe8850627005d587b8dddc3719f3a`  
		Last Modified: Fri, 25 Nov 2022 22:25:17 GMT  
		Size: 30.9 MB (30902510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be19e2a116d4f5928207e70bb649194eb3550d05a8fffdef75a694259b805934`  
		Last Modified: Fri, 25 Nov 2022 22:25:14 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:bullseye` - linux; mips64le

```console
$ docker pull ruby@sha256:6abb423edef6a650b3d60a56db0b993f5f42814b44c917814e982a71beb071ae
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.4 MB (333374755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c301c6804f7792a365eec757f2e9955e748cba7bbe2e79773f737af494d71f`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 15 Nov 2022 04:13:08 GMT
ADD file:65d4d16b7aebde0e13c3de84312e229b51904d161ba4ee74a427b6fe7c6dc6c9 in / 
# Tue, 15 Nov 2022 04:13:12 GMT
CMD ["bash"]
# Wed, 16 Nov 2022 02:12:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Nov 2022 02:12:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 16 Nov 2022 02:14:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Nov 2022 02:18:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Nov 2022 05:49:50 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 16 Nov 2022 05:49:56 GMT
ENV LANG=C.UTF-8
# Wed, 16 Nov 2022 06:15:40 GMT
ENV RUBY_MAJOR=3.1
# Fri, 25 Nov 2022 21:16:46 GMT
ENV RUBY_VERSION=3.1.3
# Fri, 25 Nov 2022 21:16:51 GMT
ENV RUBY_DOWNLOAD_SHA256=4ee161939826bcdfdafa757cf8e293a7f14e357f62be7144f040335cc8c7371a
# Fri, 25 Nov 2022 21:27:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 25 Nov 2022 21:27:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 25 Nov 2022 21:27:33 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 25 Nov 2022 21:27:39 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Nov 2022 21:27:47 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 25 Nov 2022 21:27:52 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ec4356bce7812bc703a76dd14989fc14f03913b2da506e0bdcfcecde9d90e7c3`  
		Last Modified: Tue, 15 Nov 2022 04:20:33 GMT  
		Size: 53.3 MB (53260363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80a6535eedbf12518e9b359dfc8738afc5b9728263ca9f95d8b79b809788832`  
		Last Modified: Wed, 16 Nov 2022 02:30:43 GMT  
		Size: 4.9 MB (4919324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828f0bab15c9a3054d6f2cf26d98a668e19adc16414e5cff4a165374c84263b3`  
		Last Modified: Wed, 16 Nov 2022 02:30:44 GMT  
		Size: 10.7 MB (10661751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed9f0db6bdbc67909778a6e527f854736a944838445138918bccf14341264f18`  
		Last Modified: Wed, 16 Nov 2022 02:31:32 GMT  
		Size: 53.3 MB (53307146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feb22b9935a3aa6fb95dcd52b01d0b29a227771aaf5c03215cbeb423b17f5c4c`  
		Last Modified: Wed, 16 Nov 2022 02:33:35 GMT  
		Size: 179.0 MB (178979462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c43f953cae62d76de5a4557f04a8b409476dd2ca70f0bf99f1ea6231ef94b7`  
		Last Modified: Wed, 16 Nov 2022 07:22:17 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9013dcae7e75eab6b8241926d79673673fafaa16466797a26a77dc11200c3b81`  
		Last Modified: Fri, 25 Nov 2022 22:22:26 GMT  
		Size: 32.2 MB (32246369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeef2a28c9d7caa94d07bdcdcd321fbadee162da103301c153fa8f3b109e6418`  
		Last Modified: Fri, 25 Nov 2022 22:22:12 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:bullseye` - linux; ppc64le

```console
$ docker pull ruby@sha256:404c19aa9a2ac43550daa4ed5d3611129392dadddd5109f37b57ecb740f4aca5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.8 MB (363759928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288b4ee2b854483d15af19de1a49ee1a7ed0b94f89c924ddb275e189dae72336`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 06 Dec 2022 01:17:38 GMT
ADD file:1a9427ec1dc5ca60bb760d16d5d76760f730c0c0eda8382a1d28a5e50535ad7a in / 
# Tue, 06 Dec 2022 01:17:41 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 06:39:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 06:39:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 06 Dec 2022 06:40:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 06:42:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 09:32:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 06 Dec 2022 09:32:22 GMT
ENV LANG=C.UTF-8
# Tue, 06 Dec 2022 09:39:51 GMT
ENV RUBY_MAJOR=3.1
# Tue, 06 Dec 2022 09:39:51 GMT
ENV RUBY_VERSION=3.1.3
# Tue, 06 Dec 2022 09:39:51 GMT
ENV RUBY_DOWNLOAD_SHA256=4ee161939826bcdfdafa757cf8e293a7f14e357f62be7144f040335cc8c7371a
# Tue, 06 Dec 2022 09:42:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 06 Dec 2022 09:42:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 06 Dec 2022 09:42:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 06 Dec 2022 09:42:47 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 09:42:48 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 06 Dec 2022 09:42:48 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ff7c811b7837034ee1579672c45bccdf29d765e735d05c933d69b7a21769ff65`  
		Last Modified: Tue, 06 Dec 2022 01:23:42 GMT  
		Size: 58.9 MB (58913134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec487f725efaf038a33e001df31cf2ba9579f05c1cfcc8fd8a0dfa458867fc6`  
		Last Modified: Tue, 06 Dec 2022 06:50:01 GMT  
		Size: 5.4 MB (5414492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02abe6959fd3ddd94f85209ae2b45c0eb2d03b0ad2804111aa14d05a614c9fa5`  
		Last Modified: Tue, 06 Dec 2022 06:50:03 GMT  
		Size: 11.6 MB (11630098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ac8f710264832d85cd36fb619c22c357eb687c5fb79309c62c1b2ae13f042e`  
		Last Modified: Tue, 06 Dec 2022 06:50:32 GMT  
		Size: 58.9 MB (58867231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95dc2573ecf658cef9d5eef2a63412ebb4533abd101c9ab32aa2bc786f61ef06`  
		Last Modified: Tue, 06 Dec 2022 06:51:30 GMT  
		Size: 196.2 MB (196200849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554c4d894301c06e1b6569212a263b4c0d940570f731cc55a6a64aecf6633698`  
		Last Modified: Tue, 06 Dec 2022 10:03:09 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b2163e8ed77780170227b4bb79df60163d6962ebc98ca6d26956832f964867`  
		Last Modified: Tue, 06 Dec 2022 10:04:03 GMT  
		Size: 32.7 MB (32733751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60447fa76bc64975ee0a4751f0f7c97537f17919ff7a1568a203493754f62578`  
		Last Modified: Tue, 06 Dec 2022 10:03:58 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:bullseye` - linux; s390x

```console
$ docker pull ruby@sha256:6b84d531fbe511e265489cf8832a5a9b76660326107422ff530790da65df2606
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.5 MB (328501864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8e7497f849322442850fb45947cf8bc437cfd93fed37bc232eefa9770d6bee`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 06 Dec 2022 01:42:37 GMT
ADD file:022ca98bcf37301887c0e5d24eebe36e6c81a037e13434cf887bb848aaabe291 in / 
# Tue, 06 Dec 2022 01:42:41 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:10:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:10:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 06 Dec 2022 02:10:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:12:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 08:56:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 06 Dec 2022 08:56:29 GMT
ENV LANG=C.UTF-8
# Tue, 06 Dec 2022 09:01:50 GMT
ENV RUBY_MAJOR=3.1
# Tue, 06 Dec 2022 09:01:50 GMT
ENV RUBY_VERSION=3.1.3
# Tue, 06 Dec 2022 09:01:50 GMT
ENV RUBY_DOWNLOAD_SHA256=4ee161939826bcdfdafa757cf8e293a7f14e357f62be7144f040335cc8c7371a
# Tue, 06 Dec 2022 09:03:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 06 Dec 2022 09:03:43 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 06 Dec 2022 09:03:43 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 06 Dec 2022 09:03:43 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 09:03:44 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 06 Dec 2022 09:03:44 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a3a57c761295cdc2f327925c14939b8b76fff91be8573eef2420cd05dcb39c1c`  
		Last Modified: Tue, 06 Dec 2022 01:48:26 GMT  
		Size: 53.3 MB (53272886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587cc63d90ef5602aa3e50c73c5e01e5f83cd19b5e9ded1d19a913bc8f19a7ed`  
		Last Modified: Tue, 06 Dec 2022 02:19:42 GMT  
		Size: 5.1 MB (5148499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fe2b4325313609b1f4ded814b8917f90ed49e7cd1ffea10a73bb804b76c493`  
		Last Modified: Tue, 06 Dec 2022 02:19:42 GMT  
		Size: 10.8 MB (10766834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902496b252058454f49571674e84f727a083e16651f498509d600e3849d036f0`  
		Last Modified: Tue, 06 Dec 2022 02:19:58 GMT  
		Size: 54.1 MB (54055700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c83818d38a18b44962d8db20a7a943c825de7724efb7937a3e692f265b0356c1`  
		Last Modified: Tue, 06 Dec 2022 02:20:26 GMT  
		Size: 172.8 MB (172833843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5429693fce0980bc19c8f4678745431c3903553a3672d7dff3baf3b433223715`  
		Last Modified: Tue, 06 Dec 2022 09:17:32 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba6161b005a91a2fac755554428b55b38d5c2efaa92f4c91a67dabe863c27ec`  
		Last Modified: Tue, 06 Dec 2022 09:18:04 GMT  
		Size: 32.4 MB (32423729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d20f9d9ac78ca73944b6dd28498d4e0482cd4031b043173ced585a371187ac`  
		Last Modified: Tue, 06 Dec 2022 09:18:01 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
