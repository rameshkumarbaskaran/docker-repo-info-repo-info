## `ruby:3-slim`

```console
$ docker pull ruby@sha256:f081349b9cabc3ec8736bf1b9bab4d81b1ed5b264bcc6eae839ae98069ab190e
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

### `ruby:3-slim` - linux; amd64

```console
$ docker pull ruby@sha256:2c234d82fae46f62aee5e0a70629ecc610129dbdfce54beece33aac7b5ac6132
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70180521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f3d97d2be485c2acdbc91a9538df69a8b1b64d300f32eb45a8409aae9138ec`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 17 Nov 2021 02:20:41 GMT
ADD file:a2405ebb9892d98be2eb585f6121864d12b3fd983ebf15e5f0b7486e106a79c6 in / 
# Wed, 17 Nov 2021 02:20:42 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 22:57:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 22:57:38 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 22:57:38 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 23:13:05 GMT
ENV RUBY_MAJOR=3.0
# Wed, 17 Nov 2021 23:13:05 GMT
ENV RUBY_VERSION=3.0.2
# Wed, 17 Nov 2021 23:13:05 GMT
ENV RUBY_DOWNLOAD_SHA256=570e7773100f625599575f363831166d91d49a1ab97d3ab6495af44774155c40
# Wed, 17 Nov 2021 23:16:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 23:16:40 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 23:16:40 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 23:16:40 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 23:16:41 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 23:16:42 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:eff15d958d664f0874d16aee393cc44387031ee0a68ef8542d0056c747f378e8`  
		Last Modified: Wed, 17 Nov 2021 02:25:45 GMT  
		Size: 31.4 MB (31370267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923e91ae3a1bbacb5718dae67504b37233828500a2c55e27513246d2f97cb59f`  
		Last Modified: Wed, 17 Nov 2021 23:49:26 GMT  
		Size: 10.0 MB (9987799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa5d3a4a15122ea002b0d58531a0065789f85699a9da4a744b6668dd2b8cc4a`  
		Last Modified: Wed, 17 Nov 2021 23:49:23 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c566ce3372eb0d4092ab911b1d5da4b042751a03051760f2aa0e9cdb0eea80`  
		Last Modified: Wed, 17 Nov 2021 23:50:45 GMT  
		Size: 28.8 MB (28822080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34ea7c79357428572c9df48e3f464c2cb5ae7427db164c75ee2354d8343a8a3`  
		Last Modified: Wed, 17 Nov 2021 23:50:42 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim` - linux; arm variant v5

```console
$ docker pull ruby@sha256:59ad7289f041540927688b7b0f87bb705dbc5bd0c415248f912ec882307f3689
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65671541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f99023b33e8b6b6509f72448d7215bcea2a12870ea5fec711f7a09c6bde42a8`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 17 Nov 2021 02:50:37 GMT
ADD file:738a04a17bdb9077594ad9a847333abe28216a7f04d3058718a5e21c236c24bb in / 
# Wed, 17 Nov 2021 02:50:38 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 20:42:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:42:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 20:42:40 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 21:03:22 GMT
ENV RUBY_MAJOR=3.0
# Wed, 24 Nov 2021 19:54:27 GMT
ENV RUBY_VERSION=3.0.3
# Wed, 24 Nov 2021 19:54:28 GMT
ENV RUBY_DOWNLOAD_SHA256=88cc7f0f021f15c4cd62b1f922e3a401697f7943551fe45b1fdf4f2417a17a9c
# Wed, 24 Nov 2021 19:59:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 24 Nov 2021 19:59:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 24 Nov 2021 19:59:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 24 Nov 2021 19:59:27 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Nov 2021 19:59:28 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 24 Nov 2021 19:59:29 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a960a56baa1baffbe2aa1e0c1fb02f9ee4816337d02fec259b312c409d77fafc`  
		Last Modified: Wed, 17 Nov 2021 03:06:09 GMT  
		Size: 28.9 MB (28911006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ec646f26ed3f05df453fb6e2e3b40c73e38a4b9291372a6d2a78ac858a1f8e`  
		Last Modified: Wed, 17 Nov 2021 21:58:39 GMT  
		Size: 8.6 MB (8630789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8864807b39306bec0dc767ff9c8e8466be8c6dd3add474b7200cfbe47d62aef`  
		Last Modified: Wed, 17 Nov 2021 21:58:31 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff12168a13df2c0525be1548cdc779e0686474607977f284487b25e27d25dcce`  
		Last Modified: Wed, 24 Nov 2021 20:50:56 GMT  
		Size: 28.1 MB (28129372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1ee1b23f1a17ed4cdb5fd45990859144618d54335d4fc3eb14b56457dbe240`  
		Last Modified: Wed, 24 Nov 2021 20:50:44 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim` - linux; arm variant v7

```console
$ docker pull ruby@sha256:b06b66a9a8fd5b22324daafbb35a604a9608c76b7cfe3ce2b6f62c0a4efc5c79
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62423916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d4f95a6028aad46c141c4d60818f49cb22df23dd0cd89e0cdae007d91241d2`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 17 Nov 2021 01:59:43 GMT
ADD file:cd2ac52107a2ea6657f23850a4b29366309eb39fa177321e0a9fd6d58562ae80 in / 
# Wed, 17 Nov 2021 01:59:44 GMT
CMD ["bash"]
# Thu, 18 Nov 2021 08:06:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 08:06:47 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 18 Nov 2021 08:06:48 GMT
ENV LANG=C.UTF-8
# Thu, 18 Nov 2021 08:26:54 GMT
ENV RUBY_MAJOR=3.0
# Thu, 18 Nov 2021 08:26:54 GMT
ENV RUBY_VERSION=3.0.2
# Thu, 18 Nov 2021 08:26:55 GMT
ENV RUBY_DOWNLOAD_SHA256=570e7773100f625599575f363831166d91d49a1ab97d3ab6495af44774155c40
# Thu, 18 Nov 2021 08:31:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 18 Nov 2021 08:31:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Nov 2021 08:31:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Nov 2021 08:31:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 08:31:24 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 18 Nov 2021 08:31:24 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:b6e5ca4da96841e58eb27c88695a059e5105fad5a066de803f4b94ae4002ba66`  
		Last Modified: Wed, 17 Nov 2021 02:15:13 GMT  
		Size: 26.6 MB (26573160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de383caf4b6be13cc84c3957ea84e71ae6941fee5c34724edbd3f02b6e259d21`  
		Last Modified: Thu, 18 Nov 2021 09:23:18 GMT  
		Size: 8.1 MB (8140722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd55bdd7b3881ee8276f46c323d72651e33492ec42f2ab279bd9b4b55726da8`  
		Last Modified: Thu, 18 Nov 2021 09:23:12 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee27d660bd60eda06080b57306c9cef8d2009a5a89a929c5b330e29b8d27bae5`  
		Last Modified: Thu, 18 Nov 2021 09:25:45 GMT  
		Size: 27.7 MB (27709661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668c0bae20e89b9b91c4315f57dd1904174bd92f64a34866d722b22499142a55`  
		Last Modified: Thu, 18 Nov 2021 09:25:34 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:015e154e6ef203008f41f6fd09b9104b367ed7dc64f838b770ff6975933bb136
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67670047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b8610e2d1a9712eefaf39011ba9c4a8cd503946fbc53d1ce0d317c7fb1f277a`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:15 GMT
ADD file:4203242b2b09a65239092c4780b59181da7b861b3c0be40810b3588aa200f72c in / 
# Wed, 17 Nov 2021 02:40:16 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:28:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:28:12 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:28:13 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:33:48 GMT
ENV RUBY_MAJOR=3.0
# Wed, 24 Nov 2021 19:46:48 GMT
ENV RUBY_VERSION=3.0.3
# Wed, 24 Nov 2021 19:46:48 GMT
ENV RUBY_DOWNLOAD_SHA256=88cc7f0f021f15c4cd62b1f922e3a401697f7943551fe45b1fdf4f2417a17a9c
# Wed, 24 Nov 2021 19:48:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 24 Nov 2021 19:48:56 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 24 Nov 2021 19:48:57 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 24 Nov 2021 19:48:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Nov 2021 19:48:59 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 24 Nov 2021 19:49:00 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:eb9a2845ed124d072b117aba4f0508e00c1ecd0d147dc324d14b00d24092046c`  
		Last Modified: Wed, 17 Nov 2021 02:47:17 GMT  
		Size: 30.1 MB (30056521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354e7c61b3570ed862ccf622879a565810a497b31d89dc9233ad74724113d49b`  
		Last Modified: Wed, 17 Nov 2021 09:51:20 GMT  
		Size: 9.0 MB (9033741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3178558649249287c5e43c28a587cbbeed84e6778a2b8067f094b1fd204fc4`  
		Last Modified: Wed, 17 Nov 2021 09:51:18 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c07607786573ca659cc4884de41ded15b66217121dab8182668487e56d7815`  
		Last Modified: Wed, 24 Nov 2021 20:27:38 GMT  
		Size: 28.6 MB (28579443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fc1c7201f2c399f1bfa8da45c9dc2843b14e24cf21c1cd1b00a0cf0cc11671`  
		Last Modified: Wed, 24 Nov 2021 20:27:35 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim` - linux; 386

```console
$ docker pull ruby@sha256:53221beb74b8f2f081e3c6a3d7c1c5ece97725061a323ede1808d770a13a1b6b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72562295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef3008c95da6015937c923a9c60cbe7300adecec57a322685e9d9d2bdecca36`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 17 Nov 2021 02:39:53 GMT
ADD file:ff018048717c0f5aa1730480d0bfea1c2bf94d6e2dae2d7cef46d05ffb0d93e1 in / 
# Wed, 17 Nov 2021 02:39:53 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 18:34:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 18:34:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 18:34:08 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 18:43:35 GMT
ENV RUBY_MAJOR=3.0
# Wed, 24 Nov 2021 19:44:38 GMT
ENV RUBY_VERSION=3.0.3
# Wed, 24 Nov 2021 19:44:38 GMT
ENV RUBY_DOWNLOAD_SHA256=88cc7f0f021f15c4cd62b1f922e3a401697f7943551fe45b1fdf4f2417a17a9c
# Wed, 24 Nov 2021 19:48:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 24 Nov 2021 19:48:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 24 Nov 2021 19:48:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 24 Nov 2021 19:48:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Nov 2021 19:48:02 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 24 Nov 2021 19:48:02 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0bae0e1d4cb1d56ffeb9d05de7a097d3157267eef07b6d8131344d99bd97c431`  
		Last Modified: Wed, 17 Nov 2021 02:47:49 GMT  
		Size: 32.4 MB (32380683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ce94587ba4d01f22979518292068728c3fe52b250995e88adf9de2750201e1`  
		Last Modified: Wed, 17 Nov 2021 19:16:43 GMT  
		Size: 12.0 MB (11991101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87eb951ef45c6f88babb7a5cc983a375ce043d6a24b9760459f4426f7504d49f`  
		Last Modified: Wed, 17 Nov 2021 19:16:37 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9a4aa7f77f9026ac7626f21171dfaf0a9c5a514f9c6729ce0a1e9bf69b9df3`  
		Last Modified: Wed, 24 Nov 2021 20:44:53 GMT  
		Size: 28.2 MB (28190136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217e80917bab24e7662a1d0d3baa9d4346877c53c67df68e0d58f1e092c0bc66`  
		Last Modified: Wed, 24 Nov 2021 20:44:50 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim` - linux; mips64le

```console
$ docker pull ruby@sha256:8163da1b3001122aabee1303e58bfb2d5b5626eb10be78f04c49091d5a62b425
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68414309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a01a6ce69461a53f367a028d5da39e4ed8b8f5db44e4a06977af1cbba55917`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 17 Nov 2021 02:10:13 GMT
ADD file:10bc783d286d0a800f59d5009e87ecb4651659c82cae1325132756c7c8b1dec0 in / 
# Wed, 17 Nov 2021 02:10:13 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 16:13:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 16:13:26 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 16:13:26 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 16:55:49 GMT
ENV RUBY_MAJOR=3.0
# Wed, 17 Nov 2021 16:55:50 GMT
ENV RUBY_VERSION=3.0.2
# Wed, 17 Nov 2021 16:55:50 GMT
ENV RUBY_DOWNLOAD_SHA256=570e7773100f625599575f363831166d91d49a1ab97d3ab6495af44774155c40
# Wed, 17 Nov 2021 17:05:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 17:05:54 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 17:05:54 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 17:05:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 17:05:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 17:05:57 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:08bca22fbffb4e58224e9e4f6a56f1ca5099c002b1aeb6181df63af308a3da58`  
		Last Modified: Wed, 17 Nov 2021 02:19:09 GMT  
		Size: 29.6 MB (29630388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf9364bca19730fd376cee2e644be3ca7680c6ae60f52294b4cc0851784e88`  
		Last Modified: Wed, 17 Nov 2021 18:32:15 GMT  
		Size: 9.8 MB (9828625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed77ad062c1a155ca0fa2a3b52915d62edd070b077612640175e4de19b11bf3`  
		Last Modified: Wed, 17 Nov 2021 18:32:05 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e618cf3d8d4af6ffe85a2e643501c55c8402bc9c7ec7175938227d6756b64567`  
		Last Modified: Wed, 17 Nov 2021 18:34:23 GMT  
		Size: 29.0 MB (28954954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188b27712f3893e16e880afb6d11c65189e21e5c22109f63d64277aa1db630dd`  
		Last Modified: Wed, 17 Nov 2021 18:34:11 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim` - linux; ppc64le

```console
$ docker pull ruby@sha256:d9a68703c37b728960e30401c25fe76ba34e4be5958bed34050c23f371a02e53
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75012388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8958a1844b0661c565d1e137eda53f8ff020e63045970e80bcfbb086800797ce`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 17 Nov 2021 03:28:22 GMT
ADD file:5ed330f0fe1328f694fcaefb961cf4da4d8a4ff03100b21af718b69316168706 in / 
# Wed, 17 Nov 2021 03:28:38 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 13:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 13:04:40 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 13:04:42 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 13:27:35 GMT
ENV RUBY_MAJOR=3.0
# Wed, 17 Nov 2021 13:27:37 GMT
ENV RUBY_VERSION=3.0.2
# Wed, 17 Nov 2021 13:27:40 GMT
ENV RUBY_DOWNLOAD_SHA256=570e7773100f625599575f363831166d91d49a1ab97d3ab6495af44774155c40
# Wed, 17 Nov 2021 13:33:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 13:33:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 13:33:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 13:33:34 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 13:33:42 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 13:33:44 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:258ff2a13858db8f51b65662e02137c0abcfd2528ca73e92b7a40061d938fb1e`  
		Last Modified: Wed, 17 Nov 2021 03:54:34 GMT  
		Size: 35.3 MB (35271382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6cd7d73cc9ef1ada2ee571fe603e1a6d6851c986db8d3bd27af6b84d4981f9a`  
		Last Modified: Wed, 17 Nov 2021 14:29:46 GMT  
		Size: 10.5 MB (10472208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735958df33ff056fdd4b0f8f8800361bb917843f910c8a6ae9da9d44f769d601`  
		Last Modified: Wed, 17 Nov 2021 14:29:30 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1373d5dff0c0d7699e8f6ee1540a2ee23928050a15a6dc477a7277bcc4ace818`  
		Last Modified: Wed, 17 Nov 2021 14:31:36 GMT  
		Size: 29.3 MB (29268422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac382e2eb368d119fd5a48194fd60451c04f6d0f89d965e574afff619e60e18`  
		Last Modified: Wed, 17 Nov 2021 14:31:32 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim` - linux; s390x

```console
$ docker pull ruby@sha256:4d0c2ab0a37871da68ba1b29eda1f6a7c9a6817c15ecd42f33db516cb75414c6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67764856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf658b6d7be277256c502b3ef3860afc54b0b224ac14d3ce7932804292d6f477`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 17 Nov 2021 02:42:27 GMT
ADD file:42f73dac307a6a5232e3100f3d3b36e8125f73a4ca504b106e60e2b66d242b2f in / 
# Wed, 17 Nov 2021 02:42:28 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:16:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:16:42 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:16:43 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:25:21 GMT
ENV RUBY_MAJOR=3.0
# Wed, 24 Nov 2021 19:48:23 GMT
ENV RUBY_VERSION=3.0.3
# Wed, 24 Nov 2021 19:48:23 GMT
ENV RUBY_DOWNLOAD_SHA256=88cc7f0f021f15c4cd62b1f922e3a401697f7943551fe45b1fdf4f2417a17a9c
# Wed, 24 Nov 2021 19:50:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 24 Nov 2021 19:50:13 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 24 Nov 2021 19:50:13 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 24 Nov 2021 19:50:13 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Nov 2021 19:50:14 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 24 Nov 2021 19:50:14 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:8d71e885edf612b507bbdcc48a970548d436b8709eeedfc2c98f6843a214b5e2`  
		Last Modified: Wed, 17 Nov 2021 02:48:25 GMT  
		Size: 29.7 MB (29650960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7077176d8f5d731b87cd83487f491fcf18ec48094f52c7499b92e6e3f0415ebf`  
		Last Modified: Wed, 17 Nov 2021 09:47:47 GMT  
		Size: 8.9 MB (8855851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21e3c54dccce6a6337d62e8ee58c18858d2fcb5d24cd3e37a94728eae22eb57`  
		Last Modified: Wed, 17 Nov 2021 09:47:46 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978b9e764a98d3ee263926a3f29428112cf981e336245173e1f37f311bbd7cdd`  
		Last Modified: Wed, 24 Nov 2021 20:23:15 GMT  
		Size: 29.3 MB (29257669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5cdca4aa750fc4d9bc3a335b28d385212e505f5912e2e753d9966f72d90772c`  
		Last Modified: Wed, 24 Nov 2021 20:23:13 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
