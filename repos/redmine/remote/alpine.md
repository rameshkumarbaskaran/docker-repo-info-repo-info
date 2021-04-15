## `redmine:alpine`

```console
$ docker pull redmine@sha256:0018c15ea137a5c0c840886b8639991bf8ded38ca0dcdb5db7a93b466ae3e31d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:alpine` - linux; amd64

```console
$ docker pull redmine@sha256:d4ae3106475158681d4a9d54e12b6b06057f400b72a1ec39a5ef23439acfcf3d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164348722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c11c138047e0867375b6b8fbf8c705def2bab8b87a1e2eb18f12a35ffd5fae73`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 03:07:29 GMT
RUN apk add --no-cache 		gmp-dev
# Thu, 15 Apr 2021 03:07:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Apr 2021 03:07:31 GMT
ENV LANG=C.UTF-8
# Thu, 15 Apr 2021 03:16:27 GMT
ENV RUBY_MAJOR=2.7
# Thu, 15 Apr 2021 03:16:27 GMT
ENV RUBY_VERSION=2.7.3
# Thu, 15 Apr 2021 03:16:27 GMT
ENV RUBY_DOWNLOAD_SHA256=5e91d1650857d43cd6852e05ac54683351e9c301811ee0bef43a67c4605e7db1
# Thu, 15 Apr 2021 03:20:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps 		$runDeps 		bzip2 		ca-certificates 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	! apk --no-network list --installed 		| grep -v '^[.]ruby-rundeps' 		| grep -i ruby 	; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 15 Apr 2021 03:20:42 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 15 Apr 2021 03:20:42 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 15 Apr 2021 03:20:42 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Apr 2021 03:20:43 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 15 Apr 2021 03:20:44 GMT
CMD ["irb"]
# Thu, 15 Apr 2021 11:19:30 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Thu, 15 Apr 2021 11:19:38 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Thu, 15 Apr 2021 11:19:38 GMT
ENV RAILS_ENV=production
# Thu, 15 Apr 2021 11:19:38 GMT
WORKDIR /usr/src/redmine
# Thu, 15 Apr 2021 11:19:39 GMT
ENV HOME=/home/redmine
# Thu, 15 Apr 2021 11:19:39 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 15 Apr 2021 11:19:40 GMT
ENV REDMINE_VERSION=4.2.0
# Thu, 15 Apr 2021 11:19:40 GMT
ENV REDMINE_DOWNLOAD_SHA256=295864c580afa2a926e7a17f2ad10693f9b7a6d9f1ef523edb96b2368e7f07e5
# Thu, 15 Apr 2021 11:19:44 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 15 Apr 2021 11:19:44 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Thu, 15 Apr 2021 11:21:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Thu, 15 Apr 2021 11:21:52 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 15 Apr 2021 11:21:52 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Thu, 15 Apr 2021 11:21:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Apr 2021 11:21:52 GMT
EXPOSE 3000
# Thu, 15 Apr 2021 11:21:52 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a867505730167ce0636f0811cb765ebbde11bf979c1a9839f6915f2fc3b85b`  
		Last Modified: Thu, 15 Apr 2021 03:39:41 GMT  
		Size: 1.2 MB (1218679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c77620f6108dc0610cba72f77d68c271fb1b14cb0800a7a8b6aaeb8950fec9`  
		Last Modified: Thu, 15 Apr 2021 03:39:40 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b370d66bb9903810edd365042a2f34b7a59947c942741ab947cec1b00dc738d`  
		Last Modified: Thu, 15 Apr 2021 03:40:45 GMT  
		Size: 23.2 MB (23207774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f4ad4e4f54edfb60dcbf3da39a0d79bb818be470a76b7aa5d940214fd6817b`  
		Last Modified: Thu, 15 Apr 2021 03:40:41 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96959d1a5095e4a60de22e3f9a057b3ac9013783cd3642ed045d03953ab414a`  
		Last Modified: Thu, 15 Apr 2021 11:26:58 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ac3ca6f4adab090e4026eb85a902174b741eb493692e600fd0d9e29e28c4b4`  
		Last Modified: Thu, 15 Apr 2021 11:27:09 GMT  
		Size: 69.5 MB (69450457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5f104f57e5a15b32928cc9f51ede47614bf8990047b3d558faaf9348111e97`  
		Last Modified: Thu, 15 Apr 2021 11:26:56 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bbab1cfa0b4be11deac0768cce45610a950e2b83b0a2b88e3db05d0b785a891`  
		Last Modified: Thu, 15 Apr 2021 11:26:55 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe72b582c190099035974310c4de216f0f26f107467997592c704780a7d7bc8`  
		Last Modified: Thu, 15 Apr 2021 11:26:58 GMT  
		Size: 3.1 MB (3058278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a853a11bde6641ff670e67aa327f2f2fcc74a9f5f52e6a4adc68bd7f7fd4fc58`  
		Last Modified: Thu, 15 Apr 2021 11:27:03 GMT  
		Size: 64.6 MB (64597839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e14d041c23d04045712eeb4cf9c5e91e9560bc393a05f3b983689e60a9796b1d`  
		Last Modified: Thu, 15 Apr 2021 11:26:55 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
