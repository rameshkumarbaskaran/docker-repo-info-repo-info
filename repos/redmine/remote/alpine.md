## `redmine:alpine`

```console
$ docker pull redmine@sha256:7c8e6be1a2ea046d919e18105b4136829d0ca613fd3120e1d4d750990a50d610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:alpine` - linux; amd64

```console
$ docker pull redmine@sha256:c7169f6bc7dfea247fdae21c295980568192822a5f8cc2ae053a24b3ff26b9e7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153958222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d8423aa17f3a38e691314bdcb868de9795737a032c65aa850a5c61c3da785f4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 28 Jan 2021 23:19:38 GMT
ADD file:0e2d487cd80773e947c8aae6daad3d565b7bb019a954af2b8bff188681c00d81 in / 
# Thu, 28 Jan 2021 23:19:38 GMT
CMD ["/bin/sh"]
# Fri, 29 Jan 2021 04:00:44 GMT
RUN apk add --no-cache 		gmp-dev
# Fri, 29 Jan 2021 04:00:45 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 29 Jan 2021 04:00:45 GMT
ENV LANG=C.UTF-8
# Fri, 29 Jan 2021 04:13:24 GMT
ENV RUBY_MAJOR=2.6
# Fri, 29 Jan 2021 04:13:24 GMT
ENV RUBY_VERSION=2.6.6
# Fri, 29 Jan 2021 04:13:24 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Fri, 29 Jan 2021 04:19:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps 		$runDeps 		bzip2 		ca-certificates 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	! apk --no-network list --installed 		| grep -v '^[.]ruby-rundeps' 		| grep -i ruby 	; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 29 Jan 2021 04:19:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 29 Jan 2021 04:19:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 29 Jan 2021 04:19:35 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 29 Jan 2021 04:19:36 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 29 Jan 2021 04:19:36 GMT
CMD ["irb"]
# Tue, 02 Feb 2021 23:22:47 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Tue, 02 Feb 2021 23:22:57 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Tue, 02 Feb 2021 23:22:57 GMT
ENV RAILS_ENV=production
# Tue, 02 Feb 2021 23:22:57 GMT
WORKDIR /usr/src/redmine
# Tue, 02 Feb 2021 23:22:57 GMT
ENV HOME=/home/redmine
# Tue, 02 Feb 2021 23:22:58 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 02 Feb 2021 23:22:59 GMT
ENV REDMINE_VERSION=4.1.1
# Tue, 02 Feb 2021 23:22:59 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Tue, 02 Feb 2021 23:23:02 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 02 Feb 2021 23:24:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Tue, 02 Feb 2021 23:24:46 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 02 Feb 2021 23:24:46 GMT
COPY file:74f57a1bf0a912dc2879462a72c1d654c2450fd1e1dad78bffaafda2974d3e97 in / 
# Tue, 02 Feb 2021 23:24:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Feb 2021 23:24:47 GMT
EXPOSE 3000
# Tue, 02 Feb 2021 23:24:47 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4c0d98bf9879488e0407f897d9dd4bf758555a78e39675e72b5124ccf12c2580`  
		Last Modified: Thu, 28 Jan 2021 23:20:08 GMT  
		Size: 2.8 MB (2811321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5fcc264663be41aa9be3fbaae8a22e5e4024ed1ee2e6516aa8f161d09dc6663`  
		Last Modified: Fri, 29 Jan 2021 04:27:16 GMT  
		Size: 1.2 MB (1218598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c151e279a03218da52c83a648956b26ffeeafb0f5f3f117977529f4b25ea5c6`  
		Last Modified: Fri, 29 Jan 2021 04:27:16 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45664617db5dc9f27e7f87326fad5c5544e45f6347211c9869f53e62e42dc96`  
		Last Modified: Fri, 29 Jan 2021 04:28:16 GMT  
		Size: 21.8 MB (21820505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020d8cafaa68f1d13c4a37044220956b836610fd4466a311a74f97d736c26fbd`  
		Last Modified: Fri, 29 Jan 2021 04:28:10 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8b4081d5defc0917eb817fbe03f2d013a658d946fc3596f3c2e658748aa52c`  
		Last Modified: Tue, 02 Feb 2021 23:28:03 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:967226f0efb3fe43a848ca3c0835b9c8782537e8862a900f345580a66a84b05e`  
		Last Modified: Tue, 02 Feb 2021 23:28:15 GMT  
		Size: 69.4 MB (69429652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8af5211b75642a5545bdfb5c018d9524cd455e0f605b12421422436dc86bdf`  
		Last Modified: Tue, 02 Feb 2021 23:28:02 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78cb04e5e680ef8241bc993b1e287fc6f5722a777f146aaf69461fd15074da15`  
		Last Modified: Tue, 02 Feb 2021 23:28:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef3bbe275e1cb580a0e7ab45af9dd57e58960d6246e24929d408ad5cd8ea03f`  
		Last Modified: Tue, 02 Feb 2021 23:28:03 GMT  
		Size: 2.7 MB (2740362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a87a0655b8bee3c668b60ba4fe46fe444f3b0f797f0b89097bf6efa16e2347`  
		Last Modified: Tue, 02 Feb 2021 23:28:10 GMT  
		Size: 55.9 MB (55933922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc024501071f77a671b9d0a90d9300d90bed37b5d0c2f58fe49bfd04ecf523f`  
		Last Modified: Tue, 02 Feb 2021 23:28:02 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
