## `redmine:4-alpine`

```console
$ docker pull redmine@sha256:e78b6a12790aba92df824c5cfcd07ea719a86217a9132a54e30962ddeb8e7ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:4-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:4591d2cb1b742a1a214b8defbf9b7a048fb064dd47ceca8f31dc7418a76f036c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160340855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2d8c81f053475c784a6386488546d0783b218cee4d9699315fbfac6fe2a0488`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 10:39:43 GMT
RUN apk add --no-cache 		gmp-dev
# Thu, 01 Apr 2021 10:39:45 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 01 Apr 2021 10:39:45 GMT
ENV LANG=C.UTF-8
# Thu, 01 Apr 2021 10:55:16 GMT
ENV RUBY_MAJOR=2.6
# Thu, 01 Apr 2021 10:55:16 GMT
ENV RUBY_VERSION=2.6.6
# Thu, 01 Apr 2021 10:55:16 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Thu, 01 Apr 2021 10:58:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps 		$runDeps 		bzip2 		ca-certificates 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	! apk --no-network list --installed 		| grep -v '^[.]ruby-rundeps' 		| grep -i ruby 	; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 01 Apr 2021 10:58:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 01 Apr 2021 10:58:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 01 Apr 2021 10:58:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Apr 2021 10:58:22 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 01 Apr 2021 10:58:22 GMT
CMD ["irb"]
# Thu, 01 Apr 2021 11:20:51 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Thu, 01 Apr 2021 11:20:59 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Thu, 01 Apr 2021 11:21:00 GMT
ENV RAILS_ENV=production
# Thu, 01 Apr 2021 11:21:00 GMT
WORKDIR /usr/src/redmine
# Thu, 01 Apr 2021 11:21:01 GMT
ENV HOME=/home/redmine
# Thu, 01 Apr 2021 11:21:02 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 01 Apr 2021 11:21:02 GMT
ENV REDMINE_VERSION=4.1.2
# Thu, 01 Apr 2021 11:21:02 GMT
ENV REDMINE_DOWNLOAD_SHA256=7e22397351c53fe8fe4444c01c4e0640d9cefb17b9ac765b846df27627cd228e
# Thu, 01 Apr 2021 11:21:06 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 01 Apr 2021 11:21:06 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Thu, 01 Apr 2021 11:23:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Thu, 01 Apr 2021 11:23:23 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 01 Apr 2021 11:23:24 GMT
COPY file:74f57a1bf0a912dc2879462a72c1d654c2450fd1e1dad78bffaafda2974d3e97 in / 
# Thu, 01 Apr 2021 11:23:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 11:23:24 GMT
EXPOSE 3000
# Thu, 01 Apr 2021 11:23:24 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9df2de4dab84e51acacca9e65a3d9f7c9fa2f038bc11c2830bd9a97980823a0`  
		Last Modified: Thu, 01 Apr 2021 11:09:32 GMT  
		Size: 1.2 MB (1218696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc339b259bb6448a756fb9b42044f3450a7dcd6fc3bc0102a3cb6b7594daca19`  
		Last Modified: Thu, 01 Apr 2021 11:09:34 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93282e54ffe9d376600aeeb2f74a0fb3bceeb37320c82f2d03aca87810dd7015`  
		Last Modified: Thu, 01 Apr 2021 11:11:22 GMT  
		Size: 21.8 MB (21821527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b3fef3f12828604db70ff3107f5d3ea09f2ce65bad99ee2f8759e368a4da20`  
		Last Modified: Thu, 01 Apr 2021 11:11:19 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473c8af2fa1cb655a2418107b923d2e9b5e4f88dc6d4d51f22cbd7321e3f860c`  
		Last Modified: Thu, 01 Apr 2021 11:29:20 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1545713afae422d12217cbb14475dc704c47e234e14861ae6b02ac17b126aa82`  
		Last Modified: Thu, 01 Apr 2021 11:29:35 GMT  
		Size: 69.4 MB (69427755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a113e43a2f7f2b0620d99a422628afccb16148553ed65b1110a1639e0619f3`  
		Last Modified: Thu, 01 Apr 2021 11:29:17 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6253d17c10df40e4fd3c9d93622f2608d9c7c0b3b128d432142e868ffec4f4d8`  
		Last Modified: Thu, 01 Apr 2021 11:29:17 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269caa2b1810e5b3db53190208de03b97790c623c2083f351bed3b8a0c066423`  
		Last Modified: Thu, 01 Apr 2021 11:29:18 GMT  
		Size: 2.7 MB (2747603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ac8d3d4878198d4644ee5cf93a71fb472c9359c046e2832fc59e81dba6d65e`  
		Last Modified: Thu, 01 Apr 2021 11:29:24 GMT  
		Size: 62.3 MB (62309348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b554cbeb4d78e0b74b59935edd4146a581a781ba3327187af09745b8267714`  
		Last Modified: Thu, 01 Apr 2021 11:29:18 GMT  
		Size: 2.0 KB (2049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
