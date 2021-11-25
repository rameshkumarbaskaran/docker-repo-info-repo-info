## `ruby:3-slim-buster`

```console
$ docker pull ruby@sha256:0a2ea2931070d9ef741aee09ff196c9d7f52b40b37a359f79a2a448773510c6a
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

### `ruby:3-slim-buster` - linux; amd64

```console
$ docker pull ruby@sha256:2dad74d635e4278c326e9513aa8952e3fd90cf20a2199076fc7dfbbae1185ec0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68439545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c469ef4c26aaf24461ca2f74427d7b3745eea165a927312415bc855544e8a6e2`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 23:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 23:05:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 23:05:39 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 23:20:21 GMT
ENV RUBY_MAJOR=3.0
# Wed, 24 Nov 2021 21:11:33 GMT
ENV RUBY_VERSION=3.0.3
# Wed, 24 Nov 2021 21:11:33 GMT
ENV RUBY_DOWNLOAD_SHA256=88cc7f0f021f15c4cd62b1f922e3a401697f7943551fe45b1fdf4f2417a17a9c
# Wed, 24 Nov 2021 21:15:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 24 Nov 2021 21:15:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 24 Nov 2021 21:15:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 24 Nov 2021 21:15:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Nov 2021 21:15:10 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 24 Nov 2021 21:15:10 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d04e01f945ee4b2edd0451f178f17023c43f67737d0372eb309e5c83b9bc3e0`  
		Last Modified: Wed, 17 Nov 2021 23:49:59 GMT  
		Size: 12.6 MB (12565151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8272911037384bdfabca8cbdd7eebb7290e527e81caa0a3f775b71d09b39ca4e`  
		Last Modified: Wed, 17 Nov 2021 23:49:56 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d23ba77afbe1cdfad33b0eb7b7070ff4f6c4471cfd2aa261e1db63beae41c86`  
		Last Modified: Wed, 24 Nov 2021 22:03:47 GMT  
		Size: 28.7 MB (28720343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670bcfd0263996e9168d6ce83268cf9d0243be8669abd5b45303404e8b1698e8`  
		Last Modified: Wed, 24 Nov 2021 22:03:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim-buster` - linux; arm variant v5

```console
$ docker pull ruby@sha256:76ffcc2cfd9275457a254f4781a877377e84a946d25b9d81f060777d27419839
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (63018419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c572c83ce7696794c2b5131e83ce7bc4b7d206331457d661c6d4bfcb34ba54e3`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 17 Nov 2021 02:51:39 GMT
ADD file:e580d4d2066301375327ea51dd8db3af956e5a465495bf09d69d6deec9b0bfae in / 
# Wed, 17 Nov 2021 02:51:40 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 20:53:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:53:28 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 20:53:28 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 21:13:07 GMT
ENV RUBY_MAJOR=3.0
# Wed, 24 Nov 2021 20:04:26 GMT
ENV RUBY_VERSION=3.0.3
# Wed, 24 Nov 2021 20:04:27 GMT
ENV RUBY_DOWNLOAD_SHA256=88cc7f0f021f15c4cd62b1f922e3a401697f7943551fe45b1fdf4f2417a17a9c
# Wed, 24 Nov 2021 20:09:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 24 Nov 2021 20:09:25 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 24 Nov 2021 20:09:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 24 Nov 2021 20:09:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Nov 2021 20:09:28 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 24 Nov 2021 20:09:28 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:dba255a4b166bb02562ca152d0da236ba8f211de5bf9d79e35ee023b1fce203e`  
		Last Modified: Wed, 17 Nov 2021 03:07:41 GMT  
		Size: 24.9 MB (24886310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b58fbebb8e6e22b1601002ddb4252e30c3750edfb93b87424f6c1a971c665bf`  
		Last Modified: Wed, 17 Nov 2021 21:59:40 GMT  
		Size: 10.3 MB (10349405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484eb5c97eceafe50be8deba254566cb365fd68cb0baa2e5418ecece614c2728`  
		Last Modified: Wed, 17 Nov 2021 21:59:32 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5c36662f6cff7b68fb444b03026158262311f6216f1d9ed1065d4e280ae736`  
		Last Modified: Wed, 24 Nov 2021 20:52:18 GMT  
		Size: 27.8 MB (27782327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3c4fe68f44027f8740cc379d0b62b2b7a13dbbd3a0a0eab9c760960b084748`  
		Last Modified: Wed, 24 Nov 2021 20:52:06 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim-buster` - linux; arm variant v7

```console
$ docker pull ruby@sha256:c8f9384df33fea0322db635c936d998bfbdc7cfa130e92c50553af24f2f8b868
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60301616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adf6108bc2d9e429e771faee45ee398010bf4961d98a236062f71ac2c4105449`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:46 GMT
ADD file:4ac0de0d740f0c221cd4f912861a67009942fa5bdad24ac8b62c690dfa15024a in / 
# Wed, 17 Nov 2021 02:00:47 GMT
CMD ["bash"]
# Thu, 18 Nov 2021 08:17:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 08:17:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 18 Nov 2021 08:17:06 GMT
ENV LANG=C.UTF-8
# Thu, 18 Nov 2021 08:36:09 GMT
ENV RUBY_MAJOR=3.0
# Wed, 24 Nov 2021 20:20:14 GMT
ENV RUBY_VERSION=3.0.3
# Wed, 24 Nov 2021 20:20:15 GMT
ENV RUBY_DOWNLOAD_SHA256=88cc7f0f021f15c4cd62b1f922e3a401697f7943551fe45b1fdf4f2417a17a9c
# Wed, 24 Nov 2021 20:24:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 24 Nov 2021 20:24:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 24 Nov 2021 20:24:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 24 Nov 2021 20:24:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Nov 2021 20:24:55 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 24 Nov 2021 20:24:55 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7bd9e64406c6f3044bd15f89c367f07ec4eaafb1035a5c3ee2f7b138be68017f`  
		Last Modified: Wed, 17 Nov 2021 02:16:39 GMT  
		Size: 22.8 MB (22754359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c8e57706e11dcf2202a1ed28d022f7fe3daa306f06bf5311fee3d20b17f772`  
		Last Modified: Thu, 18 Nov 2021 09:24:19 GMT  
		Size: 9.9 MB (9872912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caad345207fbbb28e02d7546fe9ec9b203219b39a7b6fe1a2c55d63e665ce8dd`  
		Last Modified: Thu, 18 Nov 2021 09:24:12 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250d1aa78cc788b28179207120bf674b13a549053f87b8d83043c42410a7fb4f`  
		Last Modified: Wed, 24 Nov 2021 21:31:34 GMT  
		Size: 27.7 MB (27673970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b2207a1e4cf25ac74118995e05a55cf92f812633e02d238b10d11adf83ef17`  
		Last Modified: Wed, 24 Nov 2021 21:31:22 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim-buster` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:1d2d4170365023b3e0fec86d4eec7983b54dfc99afe033089bf285584b72071e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65424314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c350c2a3fb1b815b0aafb31460c4e7be86ed7b6d3484f11be993c4c08c9711a`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:31:02 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:36:20 GMT
ENV RUBY_MAJOR=3.0
# Wed, 24 Nov 2021 19:51:27 GMT
ENV RUBY_VERSION=3.0.3
# Wed, 24 Nov 2021 19:51:27 GMT
ENV RUBY_DOWNLOAD_SHA256=88cc7f0f021f15c4cd62b1f922e3a401697f7943551fe45b1fdf4f2417a17a9c
# Wed, 24 Nov 2021 19:53:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 24 Nov 2021 19:53:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 24 Nov 2021 19:53:27 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 24 Nov 2021 19:53:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Nov 2021 19:53:29 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 24 Nov 2021 19:53:30 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8443a8ec909433d7156b8dcbeaf77f4e53d6a44b253a3f03b95126547154d55`  
		Last Modified: Wed, 17 Nov 2021 09:51:43 GMT  
		Size: 11.3 MB (11261808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f57122fa0ffe176f788d35a4a8f12a76819fa3bab198ac16e26d2961047a1d`  
		Last Modified: Wed, 17 Nov 2021 09:51:41 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c254a118d6bb04ab744edfd05425ee1c632b217856dc0e31723696c62f7f8f`  
		Last Modified: Wed, 24 Nov 2021 20:28:34 GMT  
		Size: 28.2 MB (28239047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db8afc2dcf12cbec1d333dd41224020508d0769c9c3ea0cc4f54d9f39e46b5ae`  
		Last Modified: Wed, 24 Nov 2021 20:28:31 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim-buster` - linux; 386

```console
$ docker pull ruby@sha256:b8717cbc1bf8cb7653436924ff798d664f3a7b3f8fe0dfd22d66605dfd418ce5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73018973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2708ad2d39e607c494ead06bb7b2d3200528f1e826f7779bd1096ec9f40c3da`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 18:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 18:38:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 18:38:25 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 18:48:49 GMT
ENV RUBY_MAJOR=3.0
# Wed, 24 Nov 2021 19:51:27 GMT
ENV RUBY_VERSION=3.0.3
# Wed, 24 Nov 2021 19:51:27 GMT
ENV RUBY_DOWNLOAD_SHA256=88cc7f0f021f15c4cd62b1f922e3a401697f7943551fe45b1fdf4f2417a17a9c
# Wed, 24 Nov 2021 19:54:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 24 Nov 2021 19:54:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 24 Nov 2021 19:54:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 24 Nov 2021 19:54:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Nov 2021 19:54:47 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 24 Nov 2021 19:54:48 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1742b7e5e1e5bca675e7f251c9f6fe8778a1bb1548e5b418f8547277f14e2e33`  
		Last Modified: Wed, 17 Nov 2021 19:17:19 GMT  
		Size: 17.2 MB (17227026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ef5459771b89c49219d5c15641c7215faf156712422f01efee40ad955a52c5`  
		Last Modified: Wed, 17 Nov 2021 19:17:10 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14561a93ccc31872c1b17227c6bfe3b0dbb03298305011cb4ccf437570bd25e1`  
		Last Modified: Wed, 24 Nov 2021 20:45:52 GMT  
		Size: 28.0 MB (27987022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c543923a2c42b829af1cdd583cb818b15e4aac407a618ebacba7134af0bd1193`  
		Last Modified: Wed, 24 Nov 2021 20:45:48 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim-buster` - linux; mips64le

```console
$ docker pull ruby@sha256:1f1180b9161b1722b58bddf75e7688fa1e0e3d9a50bd4ed1f2a25dd52142d1d3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66367211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e8389049488139f3aecf0441df9844727949713d300d217c5dbbf874aed9e5d`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 17 Nov 2021 02:11:05 GMT
ADD file:442e2528f8dc5583975e61c403642ead88c26af80e5769940d11d2420eb6e56d in / 
# Wed, 17 Nov 2021 02:11:06 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 16:35:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 16:35:36 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 16:35:36 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 17:15:29 GMT
ENV RUBY_MAJOR=3.0
# Wed, 24 Nov 2021 20:44:55 GMT
ENV RUBY_VERSION=3.0.3
# Wed, 24 Nov 2021 20:44:56 GMT
ENV RUBY_DOWNLOAD_SHA256=88cc7f0f021f15c4cd62b1f922e3a401697f7943551fe45b1fdf4f2417a17a9c
# Wed, 24 Nov 2021 20:55:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 24 Nov 2021 20:55:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 24 Nov 2021 20:55:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 24 Nov 2021 20:55:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Nov 2021 20:55:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 24 Nov 2021 20:55:17 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:f95d3989b23de40aa9c78765869cf0e26ca2ed018dd048613fbc1f9df33d1bc1`  
		Last Modified: Wed, 17 Nov 2021 02:20:33 GMT  
		Size: 25.8 MB (25820129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0387eb2188479c5600182dbe9e6a018b1c28e8d45fc7ae629895f5dac10c1343`  
		Last Modified: Wed, 17 Nov 2021 18:33:14 GMT  
		Size: 11.6 MB (11629941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61b384cda69eefe9f4bd527c1b4034c6176331fa8f719efa3548aacd6c9b0b9`  
		Last Modified: Wed, 17 Nov 2021 18:33:03 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b173688028e9bf996f8dc0f45ca686c784b37cceee93f711aa446084aadeff97`  
		Last Modified: Wed, 24 Nov 2021 22:03:25 GMT  
		Size: 28.9 MB (28916798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cf9b73d50501dba50a9eee52262c03151b895de2972522bf3ee7314b3ca2cb`  
		Last Modified: Wed, 24 Nov 2021 22:03:13 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim-buster` - linux; ppc64le

```console
$ docker pull ruby@sha256:a0e9d42e9013d609ec03f8515d2146c18d022630d109e2cb2d0c3a5d9e8345ef
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72419238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f07e79cdcd4259865a537084208804e0649d200904c09284d455de14b9a475`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 17 Nov 2021 03:30:22 GMT
ADD file:c0f8b5d4d419bef7a494df5330ecf7bbea3cbb6462308ca0b2f26771f125dea0 in / 
# Wed, 17 Nov 2021 03:30:29 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 13:17:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 13:17:25 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 13:17:28 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 13:37:40 GMT
ENV RUBY_MAJOR=3.0
# Wed, 24 Nov 2021 23:04:58 GMT
ENV RUBY_VERSION=3.0.3
# Wed, 24 Nov 2021 23:05:00 GMT
ENV RUBY_DOWNLOAD_SHA256=88cc7f0f021f15c4cd62b1f922e3a401697f7943551fe45b1fdf4f2417a17a9c
# Wed, 24 Nov 2021 23:10:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 24 Nov 2021 23:10:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 24 Nov 2021 23:10:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 24 Nov 2021 23:10:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Nov 2021 23:10:13 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 24 Nov 2021 23:10:14 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:459de0a111d5c931674a5150ef4ae6bb1ffb1685380f4aafdba04a37d556c5de`  
		Last Modified: Wed, 17 Nov 2021 03:58:14 GMT  
		Size: 30.6 MB (30562278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e4a8cb8add512175dbaeb682e1d37722eb039847e94d43b2c548f6bf9f4566`  
		Last Modified: Wed, 17 Nov 2021 14:30:35 GMT  
		Size: 12.7 MB (12705482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02accf8c69e0fb54236daa23b1409d80e215845f8d744672e8be1de6353c73f4`  
		Last Modified: Wed, 17 Nov 2021 14:30:32 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07b4527295e454e5a2a4ee44a5ad02eee24c669dcb80e9848e485922f4e9b90`  
		Last Modified: Thu, 25 Nov 2021 00:16:07 GMT  
		Size: 29.2 MB (29151103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1841f8464a3e60519b62b1b1da03099be4f15295603171ebb268865521817e3e`  
		Last Modified: Thu, 25 Nov 2021 00:16:03 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim-buster` - linux; s390x

```console
$ docker pull ruby@sha256:0e9255471436787de782a5cf70d17d347b06081e5012e156b7d1b39e068604dd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65498519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2f1afe5cb483f38f31d20abe2b07c1d79636529edd8f25f1300dc2d7f37fa7`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 17 Nov 2021 02:42:59 GMT
ADD file:3ff5fbc9c53cf76aad0fe0e1a525cb0bc0d70e8f2a3d5741dfb8b3b8a9448ffd in / 
# Wed, 17 Nov 2021 02:43:00 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:21:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:21:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:21:07 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:29:15 GMT
ENV RUBY_MAJOR=3.0
# Wed, 24 Nov 2021 19:52:19 GMT
ENV RUBY_VERSION=3.0.3
# Wed, 24 Nov 2021 19:52:19 GMT
ENV RUBY_DOWNLOAD_SHA256=88cc7f0f021f15c4cd62b1f922e3a401697f7943551fe45b1fdf4f2417a17a9c
# Wed, 24 Nov 2021 19:54:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 24 Nov 2021 19:54:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 24 Nov 2021 19:54:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 24 Nov 2021 19:54:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Nov 2021 19:54:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 24 Nov 2021 19:54:05 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:b8b917e61b3be882db10e68210f73caf5cc788bfb07aec0a659e30f4796b476b`  
		Last Modified: Wed, 17 Nov 2021 02:49:01 GMT  
		Size: 25.8 MB (25769063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e574c6d046371657ec033b78bc3df865890056f711b30df7505d0128446e36`  
		Last Modified: Wed, 17 Nov 2021 09:48:11 GMT  
		Size: 10.8 MB (10815243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6bfb1613df50da70222f9b1cd395c4b509f6e6631cf6a13ce6c6b9c8c4cf181`  
		Last Modified: Wed, 17 Nov 2021 09:48:09 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d10ed9f5b5b21d85a904dfda49e7f931d714715e9e632b845a742866f666fa6`  
		Last Modified: Wed, 24 Nov 2021 20:23:49 GMT  
		Size: 28.9 MB (28913840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea0b9e711d00c550aecfb0887c16419d5069e854acae82fab2580b32c9b567f`  
		Last Modified: Wed, 24 Nov 2021 20:23:47 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
