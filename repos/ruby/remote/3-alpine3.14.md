## `ruby:3-alpine3.14`

```console
$ docker pull ruby@sha256:f2eaea3d084129111e32b10cd783e0199dad8776836d9c757a66ec490f68c762
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

### `ruby:3-alpine3.14` - linux; amd64

```console
$ docker pull ruby@sha256:cd5190c87df91dfe710c4dc2511c689e3b0e24f925e9ae79a51beae7a32544f0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (36028215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10057e6dcfd9b4226f513e512e2b929545528a55e83ca4a9beb532e9001b213a`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:23:39 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Sat, 13 Nov 2021 06:23:40 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 13 Nov 2021 06:23:40 GMT
ENV LANG=C.UTF-8
# Mon, 27 Dec 2021 20:37:00 GMT
ENV RUBY_MAJOR=3.1
# Sat, 19 Feb 2022 00:18:33 GMT
ENV RUBY_VERSION=3.1.1
# Sat, 19 Feb 2022 00:18:34 GMT
ENV RUBY_DOWNLOAD_SHA256=7aefaa6b78b076515d272ec59c4616707a54fc9f2391239737d5f10af7a16caa
# Sat, 19 Feb 2022 00:22:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 19 Feb 2022 00:22:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Feb 2022 00:22:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Feb 2022 00:22:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Feb 2022 00:22:54 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Feb 2022 00:22:54 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d879f3f436437a08f6fe04493886c06b5c32cc82d9660c92f01bca7a718b9229`  
		Last Modified: Sat, 13 Nov 2021 06:56:30 GMT  
		Size: 3.6 MB (3644036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e3e74a152df6a3f2e7e3d3bdf84e9663a2b05b13a837e543a49f04ccd2f3e7`  
		Last Modified: Sat, 13 Nov 2021 06:56:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc6e4ee9d8738e9942898ebf153107f388389d2431f6835326449df748956a5`  
		Last Modified: Sat, 19 Feb 2022 00:27:06 GMT  
		Size: 29.6 MB (29560803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c96aa68df86f836c5b4e956473db2b157a3403111e361d14dfbffec1a0e99d`  
		Last Modified: Sat, 19 Feb 2022 00:27:03 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-alpine3.14` - linux; arm variant v6

```console
$ docker pull ruby@sha256:8dcde14e98cb89736ab5de0f975a8a75c8237bfecbb65b126bfe6434f78f9b38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34194590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df9beb3514c785012936bed290bcc32d68bc2ab21193666c18755fe8b41074c0`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:33 GMT
ADD file:8f1611b9334907a82945fdb21e17ee41541ab95050fc199c60fca662759171a5 in / 
# Thu, 17 Mar 2022 14:32:33 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 22:20:16 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Thu, 17 Mar 2022 22:20:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 17 Mar 2022 22:20:19 GMT
ENV LANG=C.UTF-8
# Thu, 17 Mar 2022 22:20:19 GMT
ENV RUBY_MAJOR=3.1
# Thu, 17 Mar 2022 22:20:20 GMT
ENV RUBY_VERSION=3.1.1
# Thu, 17 Mar 2022 22:20:20 GMT
ENV RUBY_DOWNLOAD_SHA256=7aefaa6b78b076515d272ec59c4616707a54fc9f2391239737d5f10af7a16caa
# Thu, 17 Mar 2022 22:25:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 17 Mar 2022 22:25:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 17 Mar 2022 22:25:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 17 Mar 2022 22:25:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 22:25:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 17 Mar 2022 22:25:20 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:4025825e6ef43541c3a3e1ecb0092bc1b098e792051c7e338d6da54f66b19661`  
		Last Modified: Thu, 17 Mar 2022 14:34:09 GMT  
		Size: 2.6 MB (2629364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa7ee41666c49f7309988b19cc088b28aae7e7a12c2656ac8f3ee5d08d0615f`  
		Last Modified: Thu, 17 Mar 2022 22:42:17 GMT  
		Size: 3.4 MB (3409649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b4d5663c76bdf06a737e99902bebc4fabf88fdac9a2f6eb78ec711ed378e4b`  
		Last Modified: Thu, 17 Mar 2022 22:42:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3256ae53ccd6c49c2ba3d1c0416aabf5c21214996bac7c4817f0d08a531bc755`  
		Last Modified: Thu, 17 Mar 2022 22:42:28 GMT  
		Size: 28.2 MB (28155181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e0f6a11dd7d30ffc35ab6e2bd2f7364b974cd2dde88d417771f16365e26d43`  
		Last Modified: Thu, 17 Mar 2022 22:42:15 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-alpine3.14` - linux; arm variant v7

```console
$ docker pull ruby@sha256:55dcea0a2dfc767f2ba3613fc59bd80f98fc1769dff192f2c67c8ee5ed15f625
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33760096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b088af0dc9501664830c4986748c00292254878da926e06871c5a2647194a3f0`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 17:21:06 GMT
ADD file:c25fcf153ea349f64e08a1bd0756ce550f2a081ad56cc40c89027d85d1bc26da in / 
# Thu, 17 Mar 2022 17:21:06 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 12:51:23 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Fri, 18 Mar 2022 12:51:25 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 18 Mar 2022 12:51:25 GMT
ENV LANG=C.UTF-8
# Fri, 18 Mar 2022 12:51:26 GMT
ENV RUBY_MAJOR=3.1
# Fri, 18 Mar 2022 12:51:26 GMT
ENV RUBY_VERSION=3.1.1
# Fri, 18 Mar 2022 12:51:27 GMT
ENV RUBY_DOWNLOAD_SHA256=7aefaa6b78b076515d272ec59c4616707a54fc9f2391239737d5f10af7a16caa
# Fri, 18 Mar 2022 12:55:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 18 Mar 2022 12:55:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 18 Mar 2022 12:55:25 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 18 Mar 2022 12:55:25 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Mar 2022 12:55:27 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 18 Mar 2022 12:55:27 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:c3a1157c36d8d156f7664fa098212ab2149a64bcb59767cdf4595a86617c17fd`  
		Last Modified: Thu, 17 Mar 2022 17:22:45 GMT  
		Size: 2.4 MB (2430456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0131dad5781fb997af9b3f3e5063248a5c95bf495a4a106d4b5cc25176121051`  
		Last Modified: Fri, 18 Mar 2022 13:56:23 GMT  
		Size: 3.3 MB (3280076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf39a755d92a89f881e64fe80daa0410bb1effe4b633d8bcf688dc8a135957ba`  
		Last Modified: Fri, 18 Mar 2022 13:56:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398a43bfd78b5e5feff4329cf49933c95af1747ae63d9472de6ece86e1a2f9dc`  
		Last Modified: Fri, 18 Mar 2022 13:56:33 GMT  
		Size: 28.0 MB (28049169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd52b74aa0599ea459a2a3dab44b5da113eaa9dc3e555803e46666fd1554191`  
		Last Modified: Fri, 18 Mar 2022 13:56:20 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:0ef13640951665e27dbdddcd6d03cf4ffa2d76cd32d98564bfb85d98fc2ca488
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35255273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350ecbb383f2ae26b791261576cc3521a87da52ac87e34d19dbeff2923ec18fb`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 20:19:10 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Thu, 17 Mar 2022 20:19:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 17 Mar 2022 20:19:12 GMT
ENV LANG=C.UTF-8
# Thu, 17 Mar 2022 20:19:13 GMT
ENV RUBY_MAJOR=3.1
# Thu, 17 Mar 2022 20:19:14 GMT
ENV RUBY_VERSION=3.1.1
# Thu, 17 Mar 2022 20:19:15 GMT
ENV RUBY_DOWNLOAD_SHA256=7aefaa6b78b076515d272ec59c4616707a54fc9f2391239737d5f10af7a16caa
# Thu, 17 Mar 2022 20:21:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 17 Mar 2022 20:21:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 17 Mar 2022 20:21:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 17 Mar 2022 20:21:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 20:21:37 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 17 Mar 2022 20:21:38 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51423f003b4a30e1c802d94a05186a9e33c962bffbfcc00d8fa8be148e387cee`  
		Last Modified: Thu, 17 Mar 2022 20:52:53 GMT  
		Size: 3.6 MB (3619428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4c434ff7766b761a53f6b99d455bc705f3e6a44a015e5d6b257fbf4f325d09`  
		Last Modified: Thu, 17 Mar 2022 20:52:52 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb4686882251cdbc40b6b08bf4b37dca7c0a6bea4192b58eca4b68a9aea9a5f`  
		Last Modified: Thu, 17 Mar 2022 20:52:55 GMT  
		Size: 28.9 MB (28919621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c625d085c9e4dd81a067fc10ae2b2fd452be05b364c4c493a0981277039799`  
		Last Modified: Thu, 17 Mar 2022 20:52:52 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-alpine3.14` - linux; 386

```console
$ docker pull ruby@sha256:c3f549cf41a55de6b93d326c77257c6a3264b0a29f9a67e3a4f6457714fb8e6d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34661813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba18dcacd7f4468016bb41071cc1231466e23d40b3184d2b223f34e8387020a4`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 16:34:36 GMT
ADD file:5bb8a2cf301e0add52528df0f7f5c5b3c9b14495c5aa85c8fd628731fcd348aa in / 
# Thu, 17 Mar 2022 16:34:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 20:23:31 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Thu, 17 Mar 2022 20:23:32 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 17 Mar 2022 20:23:32 GMT
ENV LANG=C.UTF-8
# Thu, 17 Mar 2022 20:23:32 GMT
ENV RUBY_MAJOR=3.1
# Thu, 17 Mar 2022 20:23:32 GMT
ENV RUBY_VERSION=3.1.1
# Thu, 17 Mar 2022 20:23:33 GMT
ENV RUBY_DOWNLOAD_SHA256=7aefaa6b78b076515d272ec59c4616707a54fc9f2391239737d5f10af7a16caa
# Thu, 17 Mar 2022 20:30:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 17 Mar 2022 20:30:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 17 Mar 2022 20:30:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 17 Mar 2022 20:30:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 20:30:25 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 17 Mar 2022 20:30:25 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:8fd9b2c548e42517da6865245538c8f53b774738b4fd7cb2d57ad8716e71748c`  
		Last Modified: Thu, 17 Mar 2022 16:35:25 GMT  
		Size: 2.8 MB (2823782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111e777f2c589c1b7de07e0360ecf89ec180abeac113ed7b72ca322f759b9138`  
		Last Modified: Thu, 17 Mar 2022 21:33:27 GMT  
		Size: 3.7 MB (3670484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193935d828700aa3c494215322588e008649a1df651ec16e34abd66065187110`  
		Last Modified: Thu, 17 Mar 2022 21:33:25 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbc3cf5757aa3f550308e67785effa718f48ef68caa1a01ad2c07d4b8c6e01e`  
		Last Modified: Thu, 17 Mar 2022 21:33:32 GMT  
		Size: 28.2 MB (28167150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959e2e493a460bb2e6849458ecbe23b10b81cd46e00d79871932766c985d7328`  
		Last Modified: Thu, 17 Mar 2022 21:33:25 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-alpine3.14` - linux; ppc64le

```console
$ docker pull ruby@sha256:0353e9313b455c6ec4890faf7fdf19cd9c082a5653ec31c361869add952b5e83
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36214563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f0ea015021e9765577657d3477b8d07138fc857f0888eda7144a001553dbb4`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 18:18:43 GMT
ADD file:bf9c99d8209e0bed9fd3b62cbe691ebf3829d5a35e63e2b066f1f842577a6d24 in / 
# Thu, 17 Mar 2022 18:18:48 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 09:40:58 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Fri, 18 Mar 2022 09:41:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 18 Mar 2022 09:41:25 GMT
ENV LANG=C.UTF-8
# Fri, 18 Mar 2022 09:41:29 GMT
ENV RUBY_MAJOR=3.1
# Fri, 18 Mar 2022 09:41:36 GMT
ENV RUBY_VERSION=3.1.1
# Fri, 18 Mar 2022 09:41:47 GMT
ENV RUBY_DOWNLOAD_SHA256=7aefaa6b78b076515d272ec59c4616707a54fc9f2391239737d5f10af7a16caa
# Fri, 18 Mar 2022 09:45:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 18 Mar 2022 09:45:49 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 18 Mar 2022 09:46:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 18 Mar 2022 09:46:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Mar 2022 09:46:21 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 18 Mar 2022 09:46:25 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:8b7e8363a93630a772b70e3cf72231f43c62addae0ee8e507c61d43e3781c4e7`  
		Last Modified: Thu, 17 Mar 2022 18:20:01 GMT  
		Size: 2.8 MB (2817281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86cf52d077a554c3cd4b3aa3cb4e1d1c20b1c357cd938cae4b084a4714a8a089`  
		Last Modified: Fri, 18 Mar 2022 11:27:18 GMT  
		Size: 3.8 MB (3775778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4209069b24d0eda92bf61d4ceb466df42f8ba874c88b381be47a6eeeb29bb387`  
		Last Modified: Fri, 18 Mar 2022 11:27:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be31764945a62a6ae3f2fffa784cec565988ba13a24205ebe71765864c90a8b5`  
		Last Modified: Fri, 18 Mar 2022 11:27:22 GMT  
		Size: 29.6 MB (29621107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfedab97fe681da73f58fb225e72a88f27cd0df06540af369dd32af7b33b572`  
		Last Modified: Fri, 18 Mar 2022 11:27:17 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-alpine3.14` - linux; s390x

```console
$ docker pull ruby@sha256:911c621ea8cde2f5be4165145029e9a0225b88b882f55f01861e5ad956f518e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35713771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1162f272067fc13ac272bd707e06cc9b873c1737d3c9ff25bda7d8c431053672`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 14:35:54 GMT
ADD file:cd4f7409c75ce2e40b46bbdeca277e2c4500aab51e1a7b6fa518c60e371f0a33 in / 
# Thu, 17 Mar 2022 14:35:55 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 15:54:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Thu, 17 Mar 2022 15:54:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 17 Mar 2022 15:54:18 GMT
ENV LANG=C.UTF-8
# Thu, 17 Mar 2022 15:54:18 GMT
ENV RUBY_MAJOR=3.1
# Thu, 17 Mar 2022 15:54:18 GMT
ENV RUBY_VERSION=3.1.1
# Thu, 17 Mar 2022 15:54:18 GMT
ENV RUBY_DOWNLOAD_SHA256=7aefaa6b78b076515d272ec59c4616707a54fc9f2391239737d5f10af7a16caa
# Thu, 17 Mar 2022 15:56:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 17 Mar 2022 15:56:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 17 Mar 2022 15:56:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 17 Mar 2022 15:56:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 15:56:27 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 17 Mar 2022 15:56:27 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1a9a9eea18bd912112f7ed42a3730393bafbb84387ab6790fe9358d09100f3a3`  
		Last Modified: Thu, 17 Mar 2022 14:36:47 GMT  
		Size: 2.6 MB (2605208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8910ce04a166727ce411aec06b1373524ca416945226e3acb2474abbee12c9e3`  
		Last Modified: Thu, 17 Mar 2022 16:23:54 GMT  
		Size: 3.7 MB (3725160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7137af0e926acc7dda6c84b96aac684bb66eaeebf68fdbd21537312e7251a144`  
		Last Modified: Thu, 17 Mar 2022 16:23:53 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78462df056803918964a4bb0592d8167f11637b18b6395efa083cb8b1bd3b354`  
		Last Modified: Thu, 17 Mar 2022 16:23:56 GMT  
		Size: 29.4 MB (29383006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ebaeb4786a184de91e77ba7e6752e4a979f879e9327d382eb363fc8681a52f`  
		Last Modified: Thu, 17 Mar 2022 16:23:53 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
