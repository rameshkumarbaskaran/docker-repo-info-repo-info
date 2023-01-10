## `ruby:alpine3.17`

```console
$ docker pull ruby@sha256:5c10172a44b9f8a7aa746cc2a89fd0c2c9bcbf1091517b394be8d6517d977118
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

### `ruby:alpine3.17` - linux; amd64

```console
$ docker pull ruby@sha256:4d2e65aa2d501107d242640d474ab7b85f8ba23eee902ea06207a49050e6f609
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.4 MB (38350423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b2790cc26d38362a5d045143511b468e1b8e6e11d41979b5c8318fed69e024`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:20 GMT
ADD file:e4d600fc4c9c293efe360be7b30ee96579925d1b4634c94332e2ec73f7d8eca1 in / 
# Mon, 09 Jan 2023 17:05:20 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 19:54:23 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Mon, 09 Jan 2023 19:54:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Mon, 09 Jan 2023 19:54:24 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jan 2023 19:54:24 GMT
ENV RUBY_MAJOR=3.2
# Mon, 09 Jan 2023 19:54:24 GMT
ENV RUBY_VERSION=3.2.0
# Mon, 09 Jan 2023 19:54:24 GMT
ENV RUBY_DOWNLOAD_SHA256=d2f4577306e6dd932259693233141e5c3ec13622c95b75996541b8d5b68b28b4
# Mon, 09 Jan 2023 19:57:11 GMT
RUN set -eux; 		yjit=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64 | aarch64) yjit=1 ;; 	esac; 	apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 		${yjit:+rust} 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${yjit:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Mon, 09 Jan 2023 19:57:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 09 Jan 2023 19:57:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 09 Jan 2023 19:57:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jan 2023 19:57:12 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Mon, 09 Jan 2023 19:57:12 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:8921db27df2831fa6eaa85321205a2470c669b855f3ec95d5a3c2b46de0442c9`  
		Last Modified: Mon, 09 Jan 2023 17:05:45 GMT  
		Size: 3.4 MB (3370628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a42b0282dbbad7379e192de066c3810a9e0f547212714ec411cb517deb7a80e`  
		Last Modified: Mon, 09 Jan 2023 20:01:53 GMT  
		Size: 4.1 MB (4125415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad130fc941d9a980b2cf3172a04f2f2e2b3e66eae0b42b52439229b09cae885`  
		Last Modified: Mon, 09 Jan 2023 20:01:52 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafb61f9055a5e68709a799fc4ce19403040016298e2890165b0f63f165cd90a`  
		Last Modified: Mon, 09 Jan 2023 20:01:55 GMT  
		Size: 30.9 MB (30853984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a766c950a068d4b43d3d1b3d9ef28d212f0cea1eb5f8e16264df9010593ed828`  
		Last Modified: Mon, 09 Jan 2023 20:01:52 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:alpine3.17` - linux; arm variant v6

```console
$ docker pull ruby@sha256:896a0ff70d82ed43fbf41c36c5b9ca9abfab7722d872f34e3c29d247e209ba58
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35114511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029483cb1576d7fca2b3643cf2b6617465bd03f96f22f0e3064f83f6a4381752`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 09 Jan 2023 17:04:54 GMT
ADD file:b15fd8e9f996815394e25f20c8459bfb4c2a8c4074592d6f4c75f4fe79ce537e in / 
# Mon, 09 Jan 2023 17:04:55 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 20:53:18 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Mon, 09 Jan 2023 20:53:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Mon, 09 Jan 2023 20:53:19 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jan 2023 20:53:19 GMT
ENV RUBY_MAJOR=3.2
# Mon, 09 Jan 2023 20:53:19 GMT
ENV RUBY_VERSION=3.2.0
# Mon, 09 Jan 2023 20:53:19 GMT
ENV RUBY_DOWNLOAD_SHA256=d2f4577306e6dd932259693233141e5c3ec13622c95b75996541b8d5b68b28b4
# Mon, 09 Jan 2023 20:55:44 GMT
RUN set -eux; 		yjit=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64 | aarch64) yjit=1 ;; 	esac; 	apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 		${yjit:+rust} 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${yjit:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Mon, 09 Jan 2023 20:55:45 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 09 Jan 2023 20:55:45 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 09 Jan 2023 20:55:45 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jan 2023 20:55:45 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Mon, 09 Jan 2023 20:55:45 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0269c10e600f3a375f36ddabdbd264ce9503a455f0d0969ce8a00f24eaecc032`  
		Last Modified: Mon, 09 Jan 2023 17:05:45 GMT  
		Size: 3.1 MB (3107243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43162e1690ffc799389269d054f1d6ef84bf57728ad167cbfe493a38489936b`  
		Last Modified: Mon, 09 Jan 2023 20:59:56 GMT  
		Size: 3.9 MB (3867470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7614a360bfe1275c7f6a9310af1a02934b5611aad1eb9131b2314cc74f837806`  
		Last Modified: Mon, 09 Jan 2023 20:59:55 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16aa0c9a5039b707e6cb08c0663362f9217680c4a24e2ed65c10d2d06d174653`  
		Last Modified: Mon, 09 Jan 2023 20:59:59 GMT  
		Size: 28.1 MB (28139462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514723b41ad1496a643ea4aadd4f7b39f52487fa39d623b11877a5c95edbc2c0`  
		Last Modified: Mon, 09 Jan 2023 20:59:55 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:alpine3.17` - linux; arm variant v7

```console
$ docker pull ruby@sha256:24afaa15a495696a7a9b0757e072bfb8ade76e446e983878dfb41f458bbae403
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34603007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba304cab45ff2cfc8592c4c0a55779de2cf8d76fb9f7e3fbbbaf2e8869e59bd6`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 09 Jan 2023 17:06:27 GMT
ADD file:4696f25d0f019b27457c55b3b128b70bf153f38e3e4eb5bdfc21058543313e94 in / 
# Mon, 09 Jan 2023 17:06:27 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 22:18:47 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Mon, 09 Jan 2023 22:18:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Mon, 09 Jan 2023 22:18:48 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jan 2023 22:18:48 GMT
ENV RUBY_MAJOR=3.2
# Mon, 09 Jan 2023 22:18:48 GMT
ENV RUBY_VERSION=3.2.0
# Mon, 09 Jan 2023 22:18:48 GMT
ENV RUBY_DOWNLOAD_SHA256=d2f4577306e6dd932259693233141e5c3ec13622c95b75996541b8d5b68b28b4
# Mon, 09 Jan 2023 22:21:22 GMT
RUN set -eux; 		yjit=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64 | aarch64) yjit=1 ;; 	esac; 	apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 		${yjit:+rust} 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${yjit:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Mon, 09 Jan 2023 22:21:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 09 Jan 2023 22:21:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 09 Jan 2023 22:21:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jan 2023 22:21:23 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Mon, 09 Jan 2023 22:21:23 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:c527615e4ffa2d5b9b777fd469b3b5ba7c1b1e9201c065be2c43569de48a3754`  
		Last Modified: Mon, 09 Jan 2023 17:07:17 GMT  
		Size: 2.9 MB (2865208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d609bd8ca36796fdb350d43448ff7d5e6b54792ccd1e9da60c6d3542aa9dff7`  
		Last Modified: Mon, 09 Jan 2023 22:30:08 GMT  
		Size: 3.7 MB (3722447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bce405ce66f81ac761b08d53171c01b50363f6b554de0748ad8c6c95dc2e7d0`  
		Last Modified: Mon, 09 Jan 2023 22:30:07 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c900db4af0faea4de9c3d0a4e484561987f816188ec5114a1504d262ebb985fe`  
		Last Modified: Mon, 09 Jan 2023 22:30:11 GMT  
		Size: 28.0 MB (28015019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf42f2cc3fdce772ec6e4fabb6faf2c568d94c49d9dbc9be7e617569e9c3da2`  
		Last Modified: Mon, 09 Jan 2023 22:30:07 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:alpine3.17` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:e23a41da4fc1986b0faeda04fff07e0775bbf479d00cb7e0291200ebb0e0c8fd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38222440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d117055c07670e134c13b68466da536af6f4eb5bb1dfa2cd1878b4c96bad4d1`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 09 Jan 2023 17:04:48 GMT
ADD file:3080f19f39259a4b77cc53975de0184c78d4335ceb9ffb77a2838d0539ad6f85 in / 
# Mon, 09 Jan 2023 17:04:49 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 21:47:34 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Mon, 09 Jan 2023 21:47:35 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Mon, 09 Jan 2023 21:47:35 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jan 2023 21:47:35 GMT
ENV RUBY_MAJOR=3.2
# Mon, 09 Jan 2023 21:47:35 GMT
ENV RUBY_VERSION=3.2.0
# Mon, 09 Jan 2023 21:47:35 GMT
ENV RUBY_DOWNLOAD_SHA256=d2f4577306e6dd932259693233141e5c3ec13622c95b75996541b8d5b68b28b4
# Mon, 09 Jan 2023 21:49:26 GMT
RUN set -eux; 		yjit=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64 | aarch64) yjit=1 ;; 	esac; 	apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 		${yjit:+rust} 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${yjit:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Mon, 09 Jan 2023 21:49:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 09 Jan 2023 21:49:27 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 09 Jan 2023 21:49:27 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jan 2023 21:49:27 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Mon, 09 Jan 2023 21:49:27 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a9eaa45ef418e883481a13c7d84fa9904f2ec56789c52a87ba5a9e6483f2b74f`  
		Last Modified: Mon, 09 Jan 2023 17:05:12 GMT  
		Size: 3.3 MB (3259241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf5c9e38ca85a871cd5915903dfe84ebc0fec0d5d6d90a48a3eaa8ace204db0`  
		Last Modified: Mon, 09 Jan 2023 21:53:35 GMT  
		Size: 4.1 MB (4118554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a27817408f785817764246761ebbabd5f87eff34e21a6a790d1dd9087c623d`  
		Last Modified: Mon, 09 Jan 2023 21:53:34 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40a287f1f6e9978470419eb8e1176db32d138ccfe927d9ff363d1b43e69370a`  
		Last Modified: Mon, 09 Jan 2023 21:53:36 GMT  
		Size: 30.8 MB (30844250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d80c0b46353568d26098df9b185d6fc3f515fc766c58f584990cc841f961964`  
		Last Modified: Mon, 09 Jan 2023 21:53:34 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:alpine3.17` - linux; 386

```console
$ docker pull ruby@sha256:244ca4a0cf2ce3c118f25499f4073b6af6394001fae5feab1606817397ddd69d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 MB (35502975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:214dd52fda229c25494ebd839f01303c744c9c03d0f251f956396880ed668ba3`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:00 GMT
ADD file:d03619a0ef81726c34189e849b80cc92da908eb36e116f28275d5765e6d0919a in / 
# Mon, 09 Jan 2023 17:05:00 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 18:56:31 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Mon, 09 Jan 2023 18:56:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Mon, 09 Jan 2023 18:56:32 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jan 2023 18:56:33 GMT
ENV RUBY_MAJOR=3.2
# Mon, 09 Jan 2023 18:56:34 GMT
ENV RUBY_VERSION=3.2.0
# Mon, 09 Jan 2023 18:56:35 GMT
ENV RUBY_DOWNLOAD_SHA256=d2f4577306e6dd932259693233141e5c3ec13622c95b75996541b8d5b68b28b4
# Mon, 09 Jan 2023 18:58:48 GMT
RUN set -eux; 		yjit=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64 | aarch64) yjit=1 ;; 	esac; 	apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 		${yjit:+rust} 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${yjit:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Mon, 09 Jan 2023 18:58:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 09 Jan 2023 18:58:49 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 09 Jan 2023 18:58:50 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jan 2023 18:58:51 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Mon, 09 Jan 2023 18:58:52 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:40e5b0b2e2bde18974628cadecd8a2f190f45f06c32846c16885d69b2908bf68`  
		Last Modified: Mon, 09 Jan 2023 17:05:42 GMT  
		Size: 3.4 MB (3408318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c9c57df57560cc8f64daf736201a376fd2df113f7da865ebb989d1326a313f`  
		Last Modified: Mon, 09 Jan 2023 19:05:42 GMT  
		Size: 4.2 MB (4195596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99681824fa99ec52c88cdeccca7673dec8b4ac2e9c25584af5d7e5d7913d61e0`  
		Last Modified: Mon, 09 Jan 2023 19:05:41 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a22c82f463bf7de9d2a3484614ff356f5bf4f97e9a80311d10cd3d00b92159`  
		Last Modified: Mon, 09 Jan 2023 19:05:44 GMT  
		Size: 27.9 MB (27898726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93746088f07f822331c4de9ebab000aa10e5c73c7084625aad77faa83d2942e9`  
		Last Modified: Mon, 09 Jan 2023 19:05:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:alpine3.17` - linux; ppc64le

```console
$ docker pull ruby@sha256:a7d01ea8cc45e5814cbb8c99a209425181fdabbccd26c8d692a01609191be259
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36941411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac7d8f3ad1194c67622390a20623be4e7e05dc58669c40cdc2e4b2fb842094a5`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:13 GMT
ADD file:9a1d27fdc0c915f387f2446c85193d5215b18020b313114f0bf2799efcc1baae in / 
# Mon, 09 Jan 2023 17:05:13 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 23:34:26 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Mon, 09 Jan 2023 23:34:27 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Mon, 09 Jan 2023 23:34:28 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jan 2023 23:34:28 GMT
ENV RUBY_MAJOR=3.2
# Mon, 09 Jan 2023 23:34:28 GMT
ENV RUBY_VERSION=3.2.0
# Mon, 09 Jan 2023 23:34:29 GMT
ENV RUBY_DOWNLOAD_SHA256=d2f4577306e6dd932259693233141e5c3ec13622c95b75996541b8d5b68b28b4
# Mon, 09 Jan 2023 23:37:28 GMT
RUN set -eux; 		yjit=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64 | aarch64) yjit=1 ;; 	esac; 	apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 		${yjit:+rust} 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${yjit:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Mon, 09 Jan 2023 23:37:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 09 Jan 2023 23:37:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 09 Jan 2023 23:37:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jan 2023 23:37:31 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Mon, 09 Jan 2023 23:37:32 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:f45bfda3aa14e255d9eb4c9a108eb3d8c6721946b4aa2e5808e5092242344a1c`  
		Last Modified: Mon, 09 Jan 2023 17:05:56 GMT  
		Size: 3.4 MB (3384562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20ef579abd4a2b77df65a27b74633fe78cbbbce453930bb66e1a473995cd1f2`  
		Last Modified: Mon, 09 Jan 2023 23:44:02 GMT  
		Size: 4.3 MB (4281390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0a54701c6b7430606b94f213df46d9050c3ade78f5b819d8e5b859a6b49ad4`  
		Last Modified: Mon, 09 Jan 2023 23:44:01 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823dee5af282f611b34cbf4257bdd242472f5f24cbaa84e694dd05873353a16c`  
		Last Modified: Mon, 09 Jan 2023 23:44:05 GMT  
		Size: 29.3 MB (29275064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5becd44c92a7dba73d4b6d5302940c675ef3c15cd008c2bd88e395b9292c5b34`  
		Last Modified: Mon, 09 Jan 2023 23:44:01 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:alpine3.17` - linux; s390x

```console
$ docker pull ruby@sha256:6f5c4fb715353aed6da939055bee963080b1a3ffc4d93680258dde22e6b52fa7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36069645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cfc2b16fa520ddbe1a529a44a0d2820e36a95ead0a0757b1b6fbc32916598df`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:44 GMT
ADD file:eabe7c3c368e65478b53ac35c1daf3b703f2bca4ecdab2d080a65e8b981d7d4a in / 
# Mon, 09 Jan 2023 17:05:46 GMT
CMD ["/bin/sh"]
# Tue, 10 Jan 2023 01:19:40 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Tue, 10 Jan 2023 01:19:44 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 10 Jan 2023 01:19:44 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jan 2023 01:19:45 GMT
ENV RUBY_MAJOR=3.2
# Tue, 10 Jan 2023 01:19:46 GMT
ENV RUBY_VERSION=3.2.0
# Tue, 10 Jan 2023 01:19:46 GMT
ENV RUBY_DOWNLOAD_SHA256=d2f4577306e6dd932259693233141e5c3ec13622c95b75996541b8d5b68b28b4
# Tue, 10 Jan 2023 01:23:22 GMT
RUN set -eux; 		yjit=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64 | aarch64) yjit=1 ;; 	esac; 	apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 		${yjit:+rust} 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${yjit:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 10 Jan 2023 01:23:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 10 Jan 2023 01:23:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 10 Jan 2023 01:23:27 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Jan 2023 01:23:29 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 10 Jan 2023 01:23:29 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ae982806674c51a962c0fdd6e19f464ebd673df529c5cfb7c1d049e0b618d384`  
		Last Modified: Mon, 09 Jan 2023 17:06:50 GMT  
		Size: 3.2 MB (3170744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a95549b153f94bfaf426b09c01250a778ab12cd982ee1b121d350deb19c7f7`  
		Last Modified: Tue, 10 Jan 2023 01:31:13 GMT  
		Size: 4.2 MB (4199057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33f69ba5453143d2ba2c1d02bb9cf5f399eba8fd8643c92d08d1368317dec4e`  
		Last Modified: Tue, 10 Jan 2023 01:31:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74b85ff317f084ff892be032fee46942770c56a1b86e6c9b61862e53d22d514`  
		Last Modified: Tue, 10 Jan 2023 01:31:15 GMT  
		Size: 28.7 MB (28699450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772906dfdb90654d2780adc6c1f52cac9aac02d1a6243b74b9e9ebab834abe53`  
		Last Modified: Tue, 10 Jan 2023 01:31:12 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
