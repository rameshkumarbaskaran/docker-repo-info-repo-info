## `ruby:3-slim-buster`

```console
$ docker pull ruby@sha256:8cbb9ac959b28389ed930d281d52e2e8d0f03b32d9a75a133f5dd9f1ead0d439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `ruby:3-slim-buster` - linux; amd64

```console
$ docker pull ruby@sha256:f874b33afc33ed686f599a6f2a83f4bbe06ce01c2cbe16896b6a6e7a66af94c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71830540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d4503848f68b75f03bb9acacb7f90113075fe776cd50c70ce9a55363227455`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:12 GMT
ADD file:14c4aa7a136ce9eb1fae0ba0f394509990d44126be801a2713cf8722fbb2e6b9 in / 
# Tue, 25 Oct 2022 01:44:12 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:11:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:11:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 25 Oct 2022 08:11:43 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 08:17:13 GMT
ENV RUBY_MAJOR=3.1
# Tue, 25 Oct 2022 08:17:13 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 25 Oct 2022 08:17:13 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 25 Oct 2022 08:19:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 25 Oct 2022 08:19:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 25 Oct 2022 08:19:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 25 Oct 2022 08:19:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 08:19:37 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 25 Oct 2022 08:19:37 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:4500a762c54620411ae491a547c66b61d577c1369ecbf5a7e91b4e153181854b`  
		Last Modified: Tue, 25 Oct 2022 01:48:40 GMT  
		Size: 27.1 MB (27140832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf681d37229fc2ce443fafcc99d16666ff5cc5f4ffacc02f27b28898f91543c`  
		Last Modified: Tue, 25 Oct 2022 08:30:59 GMT  
		Size: 12.6 MB (12577225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25afc8c627b3745ec6923eb4d8eabdf8730788c708a298d749da870c35b13632`  
		Last Modified: Tue, 25 Oct 2022 08:30:57 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98bf3bdc54474e607a7f0da22fd8eec1ba042533c97e1aa22b8dc9389c3b363`  
		Last Modified: Tue, 25 Oct 2022 08:31:46 GMT  
		Size: 32.1 MB (32112108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777a0aedaeba5d39b44b29316b3dbca43840965a61014e24ebe97389539b7810`  
		Last Modified: Tue, 25 Oct 2022 08:31:43 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim-buster` - linux; arm variant v7

```console
$ docker pull ruby@sha256:594e0dcd62533c3710f33e855bd84b2f7e09a0dc988b0f6a87364babddff736d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63239582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab91cf99ca6ec1b9495edcd0be5832ff10f2825d239e062c22780411f5c678f`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 04 Oct 2022 23:59:18 GMT
ADD file:3cde948f83f960927e2aa8be792b46726d7c3cb7a5250167816f138165e1ed3f in / 
# Tue, 04 Oct 2022 23:59:18 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 04:25:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 04:25:34 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 06 Oct 2022 04:25:34 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 04:40:55 GMT
ENV RUBY_MAJOR=3.1
# Thu, 06 Oct 2022 04:40:55 GMT
ENV RUBY_VERSION=3.1.2
# Thu, 06 Oct 2022 04:40:56 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Thu, 06 Oct 2022 04:44:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 06 Oct 2022 04:44:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 06 Oct 2022 04:44:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 06 Oct 2022 04:44:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 04:44:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 06 Oct 2022 04:44:32 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:4d0206a59e12f0afd97e080863f8788c54ecd251e26b9e6dd5d6db4d56cef8cd`  
		Last Modified: Wed, 05 Oct 2022 00:06:03 GMT  
		Size: 22.7 MB (22746557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646b3b58a51c5dba987451ad9555639bf87bfdaaf524e591dd679935e0031a42`  
		Last Modified: Thu, 06 Oct 2022 05:14:55 GMT  
		Size: 9.9 MB (9874552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0debe0906a43ae2b2d9837a05ed8a63e4700330b5b6766a6d892f41405a25b`  
		Last Modified: Thu, 06 Oct 2022 05:14:52 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265c7307812a2351474dfcb9facd4324e45fb6ddc6f4db3b2bb88bac08244370`  
		Last Modified: Thu, 06 Oct 2022 05:16:52 GMT  
		Size: 30.6 MB (30618096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead44c6ca9c6defae67fd0735ee827a0c6cb02b282561845e671d932ec2a9a0a`  
		Last Modified: Thu, 06 Oct 2022 05:16:48 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim-buster` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:f867eedafd466a5fae65741eae315db3cdebce2c2310a62921e41ce7d82d7a69
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68546282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d842dc042723a59e3b7ddf01df6edf433a04a89f8557822031c488d3305e2473`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 04 Oct 2022 23:45:10 GMT
ADD file:5395cc8536f80a7cce6fbae552f35b892b152e1db2fce6274fc514d8fc77d7c9 in / 
# Tue, 04 Oct 2022 23:45:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 14:31:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 14:31:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 05 Oct 2022 14:31:49 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 14:41:06 GMT
ENV RUBY_MAJOR=3.1
# Wed, 05 Oct 2022 14:41:07 GMT
ENV RUBY_VERSION=3.1.2
# Wed, 05 Oct 2022 14:41:08 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Wed, 05 Oct 2022 14:43:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 05 Oct 2022 14:43:13 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 05 Oct 2022 14:43:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 05 Oct 2022 14:43:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 14:43:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 05 Oct 2022 14:43:17 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:2c1ba50780a9bc2b2a8f3d639ceca4285c97f51fd1c51c783fe34e150ff35e60`  
		Last Modified: Tue, 04 Oct 2022 23:51:14 GMT  
		Size: 25.9 MB (25911903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b65a97f37373f292f91933bd53735f2159306f3ba69731f557559c043eff22`  
		Last Modified: Wed, 05 Oct 2022 15:03:41 GMT  
		Size: 11.3 MB (11274783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea67b3f57c7fbb781041a6a2e1391d4746d5b4435e7929ce9fe93ebd140d96ea`  
		Last Modified: Wed, 05 Oct 2022 15:03:39 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce20e9824a6a75c4ecbe56f980de125fd68704ea24dd840c6d75f75a0b4a4051`  
		Last Modified: Wed, 05 Oct 2022 15:05:31 GMT  
		Size: 31.4 MB (31359254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc641a6b14d94228472f10a136754f8dd01c1caa4fcf5316f4b3f29fea4894d8`  
		Last Modified: Wed, 05 Oct 2022 15:05:28 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim-buster` - linux; 386

```console
$ docker pull ruby@sha256:1bf951ed90a6622df746c3c967cbdedc65918deeaa8b0b54540132606dc3cd1d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75776025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f23ef6b8cb87a91b8965e3551f0bacabe6a5130695c065294c6b2e1a955c16`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 04 Oct 2022 23:40:08 GMT
ADD file:b1ef7e7f4c48770bde0d19751bb1624a887b657a5a5ab5d453fd5365b3448618 in / 
# Tue, 04 Oct 2022 23:40:09 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:31:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:31:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 05 Oct 2022 13:31:19 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:40:51 GMT
ENV RUBY_MAJOR=3.1
# Wed, 05 Oct 2022 13:40:52 GMT
ENV RUBY_VERSION=3.1.2
# Wed, 05 Oct 2022 13:40:53 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Wed, 05 Oct 2022 13:43:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 05 Oct 2022 13:43:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 05 Oct 2022 13:43:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 05 Oct 2022 13:43:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 13:43:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 05 Oct 2022 13:43:06 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d1d1dd08a5009b10b72285f23ffd4c1978d3445cc3855d22f4112018b15a9420`  
		Last Modified: Tue, 04 Oct 2022 23:46:26 GMT  
		Size: 27.8 MB (27797501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460848fb534b4226b259b1ff3200bea4b19bb33b8653cb38348957cba449bd5f`  
		Last Modified: Wed, 05 Oct 2022 14:04:17 GMT  
		Size: 17.2 MB (17233243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a3fe548e0589d5c96a98d1b83714d8c94788f02a31ea97fb9ca6ef96be36c7`  
		Last Modified: Wed, 05 Oct 2022 14:04:14 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3ed95be465241e35886bccb14eaedd5cd161f7d52d94b3fe66af9b669d95e3`  
		Last Modified: Wed, 05 Oct 2022 14:06:02 GMT  
		Size: 30.7 MB (30744940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64cbad1ac4ef0417613bb2fae2cf338be5c289927732377c8b7d7099d662982f`  
		Last Modified: Wed, 05 Oct 2022 14:05:59 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
