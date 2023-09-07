## `redmine:bookworm`

```console
$ docker pull redmine@sha256:ae07b4a3be7b04b6b41ac5d91e9fc88e850088b4a6aec964f35ad07a58fbc4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redmine:bookworm` - linux; amd64

```console
$ docker pull redmine@sha256:e63a0fbeb74d31894e2d131caf91aca3d661cd893d270090ff147cad3e30b1d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.2 MB (264220432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eacfce31c57a7e10ff6701276b4bbe9e846a77e842f64a76a9286ce7a55e77d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 16 Aug 2023 00:59:46 GMT
ADD file:997f5a9b32407d96efac41a1cfafb318f77de077c8b5cd7065b6ec9796b4bf5e in / 
# Wed, 16 Aug 2023 00:59:47 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 06:23:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 06:23:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 16 Aug 2023 06:23:01 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 06:34:46 GMT
ENV RUBY_MAJOR=3.1
# Wed, 16 Aug 2023 06:34:46 GMT
ENV RUBY_VERSION=3.1.4
# Wed, 16 Aug 2023 06:34:46 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 16 Aug 2023 06:37:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 16 Aug 2023 06:37:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 16 Aug 2023 06:37:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 16 Aug 2023 06:37:10 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 06:37:11 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 16 Aug 2023 06:37:11 GMT
CMD ["irb"]
# Thu, 17 Aug 2023 02:39:34 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 17 Aug 2023 02:40:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 02:40:12 GMT
ENV RAILS_ENV=production
# Thu, 17 Aug 2023 02:40:12 GMT
WORKDIR /usr/src/redmine
# Thu, 17 Aug 2023 02:40:12 GMT
ENV HOME=/home/redmine
# Thu, 17 Aug 2023 02:40:12 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 17 Aug 2023 02:40:12 GMT
ENV REDMINE_VERSION=5.0.5
# Thu, 17 Aug 2023 02:40:13 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.5.tar.gz
# Thu, 17 Aug 2023 02:40:13 GMT
ENV REDMINE_DOWNLOAD_SHA256=a89ad1c4bb9bf025e6527c77ab18c8faf7749c94a975caf2cfdbba00eb12a481
# Thu, 17 Aug 2023 02:40:16 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 17 Aug 2023 02:40:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 17 Aug 2023 02:40:51 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 17 Aug 2023 02:40:51 GMT
COPY file:f61e8718e722eba56748d9a7e58011159861fb49784b1ad721746c1fc5735b6d in / 
# Thu, 17 Aug 2023 02:40:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 02:40:51 GMT
EXPOSE 3000
# Thu, 17 Aug 2023 02:40:51 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:52d2b7f179e32b4cbd579ee3c4958027988f9a8274850ab0c7c24661e3adaac5`  
		Last Modified: Wed, 16 Aug 2023 01:04:30 GMT  
		Size: 29.1 MB (29124563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a649bce6d85745cccdbba2d4155703eec18ebc265bb56c46a1ad597e93d465`  
		Last Modified: Wed, 16 Aug 2023 06:45:34 GMT  
		Size: 13.8 MB (13837097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5bd2a1b9e97791526a17f68154ed0658486096fd3bccb3c70c1db593298b2c`  
		Last Modified: Wed, 16 Aug 2023 06:45:32 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1b6cb643231e38ea3c680666a7ea7fa0481d3662aad772528a13af35360735`  
		Last Modified: Wed, 16 Aug 2023 06:46:59 GMT  
		Size: 32.9 MB (32921999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235c29bef2ab5fca0f5f0969123fd84593f2d57a3953bfe83b30273b8af73a60`  
		Last Modified: Wed, 16 Aug 2023 06:46:55 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e238c3029f01e391049202e5c0f9e3f2c5283a4a39014a61f9dd95f5636b6c14`  
		Last Modified: Thu, 17 Aug 2023 02:41:11 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36aa2f5e304c52976d97f676c389697762511f6c178b6ca31086d5bd1bd0088f`  
		Last Modified: Thu, 17 Aug 2023 02:41:27 GMT  
		Size: 123.1 MB (123082112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e9ecb8be9d43fd409232abe7c39f2ef12e2f58cd22b910eb9d2826b87ef05d`  
		Last Modified: Thu, 17 Aug 2023 02:41:09 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1400f4a6cea221ddf1a95b93e8fc50b4fa0684a765a3b51a0952c2e4f4bce084`  
		Last Modified: Thu, 17 Aug 2023 02:41:09 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ecfa0c4e52d57538501dcf6e2c9bdb7077ecce21fa68d4a90536e3abd4283c9`  
		Last Modified: Thu, 17 Aug 2023 02:41:10 GMT  
		Size: 3.1 MB (3144729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b64154a3f2e370afaa278d6a50bbce5eb7f57f1ca93715889a25cb1d691b3ad`  
		Last Modified: Thu, 17 Aug 2023 02:41:16 GMT  
		Size: 62.1 MB (62106079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14338333eeda97172f4d3b87f45eaed15abd05df32e4df6ec9142a8e34ca631b`  
		Last Modified: Thu, 17 Aug 2023 02:41:09 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:bookworm` - linux; arm variant v5

```console
$ docker pull redmine@sha256:8ac983bf2ce23e4bd18f3b19f2694231a519c4ab423240d36ca4b2c876d11bae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.1 MB (262065202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49cc1976c8aa850b944c61eff4527b736be4d069655e82f01131ed77858f4684`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 07 Sep 2023 00:48:30 GMT
ADD file:e7b77e5797ddb7e058507462fd5f5aad6864ba08ebc4a6c2743dae81ed0f445d in / 
# Thu, 07 Sep 2023 00:48:31 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 12:19:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 12:19:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 07 Sep 2023 12:19:20 GMT
ENV LANG=C.UTF-8
# Thu, 07 Sep 2023 12:38:42 GMT
ENV RUBY_MAJOR=3.1
# Thu, 07 Sep 2023 12:38:42 GMT
ENV RUBY_VERSION=3.1.4
# Thu, 07 Sep 2023 12:38:42 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Thu, 07 Sep 2023 12:40:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 07 Sep 2023 12:40:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 07 Sep 2023 12:40:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 07 Sep 2023 12:40:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 12:41:00 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 07 Sep 2023 12:41:00 GMT
CMD ["irb"]
# Thu, 07 Sep 2023 20:34:01 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 07 Sep 2023 20:35:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 20:35:02 GMT
ENV RAILS_ENV=production
# Thu, 07 Sep 2023 20:35:02 GMT
WORKDIR /usr/src/redmine
# Thu, 07 Sep 2023 20:35:02 GMT
ENV HOME=/home/redmine
# Thu, 07 Sep 2023 20:35:04 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 07 Sep 2023 20:35:04 GMT
ENV REDMINE_VERSION=5.0.5
# Thu, 07 Sep 2023 20:35:04 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.5.tar.gz
# Thu, 07 Sep 2023 20:35:04 GMT
ENV REDMINE_DOWNLOAD_SHA256=a89ad1c4bb9bf025e6527c77ab18c8faf7749c94a975caf2cfdbba00eb12a481
# Thu, 07 Sep 2023 20:35:08 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 07 Sep 2023 20:37:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 07 Sep 2023 20:37:11 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 07 Sep 2023 20:37:11 GMT
COPY file:f61e8718e722eba56748d9a7e58011159861fb49784b1ad721746c1fc5735b6d in / 
# Thu, 07 Sep 2023 20:37:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 20:37:12 GMT
EXPOSE 3000
# Thu, 07 Sep 2023 20:37:12 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d971e043cc5e8068fe39c736806d279b128c720a08d2e0d41002dcf027787939`  
		Last Modified: Thu, 07 Sep 2023 00:51:35 GMT  
		Size: 27.0 MB (26983530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3774359ea5b150341ff2a05389d3be3c78016cd9e4bcfb286a05e3c74a7681`  
		Last Modified: Thu, 07 Sep 2023 12:51:07 GMT  
		Size: 11.6 MB (11600813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308401a0bfae7969fe3a9a3602fb412f1a6d948e7b0c1453f5e3519c39e1a71d`  
		Last Modified: Thu, 07 Sep 2023 12:51:04 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25c94a239a3aef0a82d337638d890a74e0eb53a96478f2d5f017547ae40f74b`  
		Last Modified: Thu, 07 Sep 2023 12:53:29 GMT  
		Size: 31.7 MB (31715058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded2436db0923b0dde425d4135881d6340b6c437d9cf1ed4126b35d76cccbe66`  
		Last Modified: Thu, 07 Sep 2023 12:53:25 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c64be0cf502d8f7382545d3de981df99b3f5ad43cbc4abb539ff24eb85d2d369`  
		Last Modified: Thu, 07 Sep 2023 20:37:34 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a38ecbfeea7af6a1987997fdd9f180d23528e37c88255e2fd4a751cd7da3ae`  
		Last Modified: Thu, 07 Sep 2023 20:37:59 GMT  
		Size: 116.6 MB (116648909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8909cd8ef57ccb1251d27719e4eafb7cd20d73c02a7ec71d900c55a312adbf`  
		Last Modified: Thu, 07 Sep 2023 20:37:31 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd52239d69ceef66c9ea2f357067aab8a57f5fca050bae12dcfcaf87f51abb4d`  
		Last Modified: Thu, 07 Sep 2023 20:37:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f78fbb5d839e68732e22bf4e1101c464e0508b970cec1b29d39fde7a435c05`  
		Last Modified: Thu, 07 Sep 2023 20:37:33 GMT  
		Size: 3.1 MB (3144725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7455c2b08fdc50be8a2d95f693c2748e3e024bbcf47dc27f2559fe46c63ed57`  
		Last Modified: Thu, 07 Sep 2023 20:37:44 GMT  
		Size: 72.0 MB (71968324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf83c43e8701c86fc4d2b889755890fd0435aa9fe4b1bf84e1723a168e394e9`  
		Last Modified: Thu, 07 Sep 2023 20:37:32 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:bookworm` - linux; arm variant v7

```console
$ docker pull redmine@sha256:a3d2eff912aeab920793a597af5ead8fbfec7f17dcf56cb9b58e8100dde94352
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.2 MB (254213790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2df6ce6695373a093bd9d31a2aef65771ff2750bad29ab86a14d601301dac0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 16 Aug 2023 00:17:12 GMT
ADD file:45cc27bd11f601d2fef5d7494a1a6253287e6d22e108e39c0884761c7533cd9c in / 
# Wed, 16 Aug 2023 00:17:12 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 05:03:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 05:03:36 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 16 Aug 2023 05:03:36 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 05:13:11 GMT
ENV RUBY_MAJOR=3.1
# Wed, 16 Aug 2023 05:13:11 GMT
ENV RUBY_VERSION=3.1.4
# Wed, 16 Aug 2023 05:13:11 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 16 Aug 2023 05:15:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 16 Aug 2023 05:15:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 16 Aug 2023 05:15:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 16 Aug 2023 05:15:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 05:15:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 16 Aug 2023 05:15:20 GMT
CMD ["irb"]
# Wed, 16 Aug 2023 23:59:18 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 17 Aug 2023 00:00:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 00:00:03 GMT
ENV RAILS_ENV=production
# Thu, 17 Aug 2023 00:00:03 GMT
WORKDIR /usr/src/redmine
# Thu, 17 Aug 2023 00:00:03 GMT
ENV HOME=/home/redmine
# Thu, 17 Aug 2023 00:00:03 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 17 Aug 2023 00:00:03 GMT
ENV REDMINE_VERSION=5.0.5
# Thu, 17 Aug 2023 00:00:04 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.5.tar.gz
# Thu, 17 Aug 2023 00:00:04 GMT
ENV REDMINE_DOWNLOAD_SHA256=a89ad1c4bb9bf025e6527c77ab18c8faf7749c94a975caf2cfdbba00eb12a481
# Thu, 17 Aug 2023 00:00:07 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 17 Aug 2023 00:01:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 17 Aug 2023 00:01:52 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 17 Aug 2023 00:01:52 GMT
COPY file:f61e8718e722eba56748d9a7e58011159861fb49784b1ad721746c1fc5735b6d in / 
# Thu, 17 Aug 2023 00:01:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 00:01:52 GMT
EXPOSE 3000
# Thu, 17 Aug 2023 00:01:52 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a44aa9565b062e4216f7b39ce6c67dcc5376e10f76caec55bd3acd1cc8b76b75`  
		Last Modified: Wed, 16 Aug 2023 00:21:27 GMT  
		Size: 24.8 MB (24805419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e768fd12705fcc90ec510232b3b46d665763596c4c0f964ccf3aa80cfc1d1d0`  
		Last Modified: Wed, 16 Aug 2023 05:23:12 GMT  
		Size: 10.9 MB (10940956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb5ed6600bb293960e919f7fbcee0b4a2aa2350b6a594a88cd0e3d54d942db5`  
		Last Modified: Wed, 16 Aug 2023 05:23:10 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd07d8ad5104b836beb802ff2e01a458e576279111bdc87294f845dfbaec482`  
		Last Modified: Wed, 16 Aug 2023 05:24:29 GMT  
		Size: 31.6 MB (31558261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930cb4b8b33572c0cf581ebe4e7fb492619deb29f5aee468a545caa28fe098c5`  
		Last Modified: Wed, 16 Aug 2023 05:24:26 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c6f7a2a8202de4ebb80aa7d65ee8eba57ce8f15484bfc18dc1772df34f4595`  
		Last Modified: Thu, 17 Aug 2023 00:02:10 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff69a97ec343a34b3686fb58e1d9ee91396426b188812902faeda86cc54f711`  
		Last Modified: Thu, 17 Aug 2023 00:02:26 GMT  
		Size: 112.1 MB (112142298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb7d74e8d0a2e2249162e74d19254e332d5eb804eae833b0668fa038ccecfa4`  
		Last Modified: Thu, 17 Aug 2023 00:02:08 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0480aa59f1b6322a89156d21db7c802711f372456f1060b3dfbfefd83576554`  
		Last Modified: Thu, 17 Aug 2023 00:02:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b68ce6d929c4d207a3f99fd3888006c77f073921ed56ea2e72442d40a2a8f7`  
		Last Modified: Thu, 17 Aug 2023 00:02:09 GMT  
		Size: 3.1 MB (3144735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b74f46fc43e9f271dd9af0c6bd07725f7cd27fc9d84b830d83fda96c4fbcc9`  
		Last Modified: Thu, 17 Aug 2023 00:02:15 GMT  
		Size: 71.6 MB (71618272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:919bd05defae11da89a78ef26c77129b9bd2cb2b62a352d60bdb2ae9b41d2041`  
		Last Modified: Thu, 17 Aug 2023 00:02:08 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:bookworm` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:90e25c6c333e837070a6e7071e40258e44c4d5b59287e4657a2beb6ec418beae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.5 MB (259458340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e6b6073a12d932027ac5ef9ca3d286c0642ad5f4c43860e81c97de77b282180`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:39 GMT
ADD file:fb5c8f411c4a1e06c25ac32455221938386907d0b4782fc228ca67de63a7e9de in / 
# Thu, 07 Sep 2023 00:39:39 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 02:01:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 02:01:12 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 07 Sep 2023 02:01:12 GMT
ENV LANG=C.UTF-8
# Thu, 07 Sep 2023 02:11:16 GMT
ENV RUBY_MAJOR=3.1
# Thu, 07 Sep 2023 02:11:16 GMT
ENV RUBY_VERSION=3.1.4
# Thu, 07 Sep 2023 02:11:16 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Thu, 07 Sep 2023 02:13:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 07 Sep 2023 02:13:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 07 Sep 2023 02:13:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 07 Sep 2023 02:13:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 02:13:09 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 07 Sep 2023 02:13:09 GMT
CMD ["irb"]
# Thu, 07 Sep 2023 09:59:23 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 07 Sep 2023 09:59:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 09:59:56 GMT
ENV RAILS_ENV=production
# Thu, 07 Sep 2023 09:59:56 GMT
WORKDIR /usr/src/redmine
# Thu, 07 Sep 2023 09:59:56 GMT
ENV HOME=/home/redmine
# Thu, 07 Sep 2023 09:59:56 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 07 Sep 2023 09:59:57 GMT
ENV REDMINE_VERSION=5.0.5
# Thu, 07 Sep 2023 09:59:57 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.5.tar.gz
# Thu, 07 Sep 2023 09:59:57 GMT
ENV REDMINE_DOWNLOAD_SHA256=a89ad1c4bb9bf025e6527c77ab18c8faf7749c94a975caf2cfdbba00eb12a481
# Thu, 07 Sep 2023 10:00:00 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 07 Sep 2023 10:00:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 07 Sep 2023 10:00:29 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 07 Sep 2023 10:00:29 GMT
COPY file:f61e8718e722eba56748d9a7e58011159861fb49784b1ad721746c1fc5735b6d in / 
# Thu, 07 Sep 2023 10:00:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 10:00:29 GMT
EXPOSE 3000
# Thu, 07 Sep 2023 10:00:29 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:155eab17d86c47443adc8cebe7fc62c847c03db8cfb1ca53aa6276564fff23ef`  
		Last Modified: Thu, 07 Sep 2023 00:43:02 GMT  
		Size: 29.2 MB (29157149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:667e3e032097f038e21b5414c0491d40519643aade62f0f06e970c9b7cec9989`  
		Last Modified: Thu, 07 Sep 2023 02:20:00 GMT  
		Size: 12.7 MB (12683926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80490678eba591b01904277941acf2c62ed55bcfe53135c161ba1f7f5450898c`  
		Last Modified: Thu, 07 Sep 2023 02:19:58 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24f06e6eca30ad9e160ebe19a4f696d9da7f9c6df522a63244593091ef30bc0`  
		Last Modified: Thu, 07 Sep 2023 02:21:18 GMT  
		Size: 32.4 MB (32358885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5977a9e7ef06092fdf3d545fd3aac67d05e0b495906c6cc2a1d3e262258fd28`  
		Last Modified: Thu, 07 Sep 2023 02:21:15 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7b21991312281ed57a80ba67c4d44aa863b4e9a65ed6465f229ffb0b546048`  
		Last Modified: Thu, 07 Sep 2023 10:00:48 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05488ac21710ce3796f78eccbcebdfd3ff7b37942b88388612722e3ee0c1c794`  
		Last Modified: Thu, 07 Sep 2023 10:01:01 GMT  
		Size: 120.2 MB (120222616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d697c39495f278ff52e41e83181de8ab6ea80f0bb3a4d7cfa5d1d70d93621098`  
		Last Modified: Thu, 07 Sep 2023 10:00:46 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b06bff67efc78ad1fdf90ee3f59690839da2132aaceb911392c9cce204f22c8`  
		Last Modified: Thu, 07 Sep 2023 10:00:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ec222f809d750abba64f411922aa8e6e6a844974f13f80704d59d251677f1d`  
		Last Modified: Thu, 07 Sep 2023 10:00:47 GMT  
		Size: 3.1 MB (3144724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0006e71cc6607f41a06133942f80ec74fbbaca4845620e9dcd2d6a825f02ad`  
		Last Modified: Thu, 07 Sep 2023 10:00:52 GMT  
		Size: 61.9 MB (61887191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8869960d5ce127e545c40729d967a4ae9ce0953033776723c25731b621c3e373`  
		Last Modified: Thu, 07 Sep 2023 10:00:46 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:bookworm` - linux; 386

```console
$ docker pull redmine@sha256:2c8d73688affed55f1f50939b3a2c71cd05a753be78fdc1c064c67e7d5e749ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264765814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5c38ed2f8576cb2ab7472baa8a9d3e2466fc1edffeeca45e1aaf735b20e925`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:01 GMT
ADD file:ffdb2f26091492ac2e82793b461bb70da9ce1d68d219ec0db182b4510e82586b in / 
# Tue, 15 Aug 2023 23:39:01 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 08:06:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 08:06:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 16 Aug 2023 08:06:07 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 08:35:37 GMT
ENV RUBY_MAJOR=3.1
# Wed, 16 Aug 2023 08:35:37 GMT
ENV RUBY_VERSION=3.1.4
# Wed, 16 Aug 2023 08:35:37 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 16 Aug 2023 08:39:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 16 Aug 2023 08:39:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 16 Aug 2023 08:39:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 16 Aug 2023 08:39:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 08:39:29 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 16 Aug 2023 08:39:29 GMT
CMD ["irb"]
# Wed, 16 Aug 2023 16:13:16 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 16 Aug 2023 16:14:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 16:14:04 GMT
ENV RAILS_ENV=production
# Wed, 16 Aug 2023 16:14:04 GMT
WORKDIR /usr/src/redmine
# Wed, 16 Aug 2023 16:14:04 GMT
ENV HOME=/home/redmine
# Wed, 16 Aug 2023 16:14:04 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 16 Aug 2023 16:14:04 GMT
ENV REDMINE_VERSION=5.0.5
# Wed, 16 Aug 2023 16:14:04 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.5.tar.gz
# Wed, 16 Aug 2023 16:14:05 GMT
ENV REDMINE_DOWNLOAD_SHA256=a89ad1c4bb9bf025e6527c77ab18c8faf7749c94a975caf2cfdbba00eb12a481
# Wed, 16 Aug 2023 16:14:08 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 16 Aug 2023 16:15:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 16 Aug 2023 16:15:02 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 16 Aug 2023 16:15:02 GMT
COPY file:f61e8718e722eba56748d9a7e58011159861fb49784b1ad721746c1fc5735b6d in / 
# Wed, 16 Aug 2023 16:15:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Aug 2023 16:15:03 GMT
EXPOSE 3000
# Wed, 16 Aug 2023 16:15:03 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a12cc43de7614ac71c57865601eb4cedd27ce910b66c5091e07781b8547d5b0b`  
		Last Modified: Tue, 15 Aug 2023 23:43:26 GMT  
		Size: 30.1 MB (30141823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b2137ed48315aa5293610d58d3741d77437be1c7374799a0f52b1a5ba47ba3`  
		Last Modified: Wed, 16 Aug 2023 09:01:25 GMT  
		Size: 13.4 MB (13395855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8fffea98b804b53cd61cd051cf480a9564114ea368ed6a91de3dd5b486f2da`  
		Last Modified: Wed, 16 Aug 2023 09:01:21 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c003e1b629958a4cbdbcabe899be7e7fe21e784d9471f9d124b99712128542`  
		Last Modified: Wed, 16 Aug 2023 09:03:55 GMT  
		Size: 31.6 MB (31624337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36192c2f92da04d89b6f2c672afc0e8b66d80446f57a4008ab8fd5838aeee268`  
		Last Modified: Wed, 16 Aug 2023 09:03:51 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb68b6923a9c8e88e08009c4e0e914051fdb262e396c5c2776b07d6f41c9fd1`  
		Last Modified: Wed, 16 Aug 2023 16:15:30 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4acffe19d03f5770b37690d96055a7cc368670294bf03186490f7ccf554e1b2`  
		Last Modified: Wed, 16 Aug 2023 16:15:56 GMT  
		Size: 124.9 MB (124949067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e940b5ee52168ef7f32219d6a0f2e01e37635b01560eb82bc18a94cb4899096d`  
		Last Modified: Wed, 16 Aug 2023 16:15:27 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8502e67fed071e6670be41a3e51097946b6bb3b907b781d2ef78b122140c15bd`  
		Last Modified: Wed, 16 Aug 2023 16:15:27 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6ed22d57043c06f8b8bf69b30d8827360b326412517fb5c7643ecc404e3e50`  
		Last Modified: Wed, 16 Aug 2023 16:15:29 GMT  
		Size: 3.1 MB (3144730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4fb031d113e4be3da3f0e6f65f7943f29899d3a2140f4efa3efaeee6c53b013`  
		Last Modified: Wed, 16 Aug 2023 16:15:38 GMT  
		Size: 61.5 MB (61506155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe22708799cb93bee965330647da1364cdd50c709edde38f311b6b1292d0a417`  
		Last Modified: Wed, 16 Aug 2023 16:15:27 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:bookworm` - linux; ppc64le

```console
$ docker pull redmine@sha256:3e590e4e18fe7da753b337b5ae5897912090b8335a8a60f66f6594866de1666e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288868832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413cfd48ab3e6f4d7cfaab03e764e2ec5bad4d8f6197d6ea7ddd3c5bac0d1f99`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 16 Aug 2023 01:09:33 GMT
ADD file:9578bf6d6b33f2ba960ab9309642d1c9dcc131d7b9e6f818b8cc4b843fe3aec8 in / 
# Wed, 16 Aug 2023 01:09:35 GMT
CMD ["bash"]
# Thu, 17 Aug 2023 08:42:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 08:42:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 17 Aug 2023 08:42:33 GMT
ENV LANG=C.UTF-8
# Thu, 17 Aug 2023 09:14:53 GMT
ENV RUBY_MAJOR=3.1
# Thu, 17 Aug 2023 09:14:55 GMT
ENV RUBY_VERSION=3.1.4
# Thu, 17 Aug 2023 09:14:57 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Thu, 17 Aug 2023 09:26:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 17 Aug 2023 09:26:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 17 Aug 2023 09:26:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 17 Aug 2023 09:26:39 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 09:26:40 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 17 Aug 2023 09:26:43 GMT
CMD ["irb"]
# Thu, 17 Aug 2023 13:36:47 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 17 Aug 2023 13:38:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 13:38:18 GMT
ENV RAILS_ENV=production
# Thu, 17 Aug 2023 13:38:18 GMT
WORKDIR /usr/src/redmine
# Thu, 17 Aug 2023 13:38:18 GMT
ENV HOME=/home/redmine
# Thu, 17 Aug 2023 13:38:20 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 17 Aug 2023 13:38:20 GMT
ENV REDMINE_VERSION=5.0.5
# Thu, 17 Aug 2023 13:38:20 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.5.tar.gz
# Thu, 17 Aug 2023 13:38:20 GMT
ENV REDMINE_DOWNLOAD_SHA256=a89ad1c4bb9bf025e6527c77ab18c8faf7749c94a975caf2cfdbba00eb12a481
# Thu, 17 Aug 2023 13:38:25 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 17 Aug 2023 13:42:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 17 Aug 2023 13:42:05 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 17 Aug 2023 13:42:05 GMT
COPY file:f61e8718e722eba56748d9a7e58011159861fb49784b1ad721746c1fc5735b6d in / 
# Thu, 17 Aug 2023 13:42:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 13:42:05 GMT
EXPOSE 3000
# Thu, 17 Aug 2023 13:42:06 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0500920b409f06d69819525676ebf090702285435050f7b1f973c8c7b034ea7c`  
		Last Modified: Wed, 16 Aug 2023 01:15:59 GMT  
		Size: 33.1 MB (33119300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41d5a4f907e470b4dd3f4bf293fa92a86f29b1f62fe52c34492531aa52ce752`  
		Last Modified: Thu, 17 Aug 2023 09:59:35 GMT  
		Size: 14.6 MB (14564466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd440cac8b8e51d155b5e5c71ad679ba3b1dad8b9160b191f69099e2b38b89d`  
		Last Modified: Thu, 17 Aug 2023 09:59:31 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6323534ae448303e994f4cf3f249c10daf93d096b5a78ad3f22ac51334086d`  
		Last Modified: Thu, 17 Aug 2023 10:03:38 GMT  
		Size: 33.3 MB (33285273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b65f809622ce5ef68b00d2e16240bca212a444bd28e637d3c720357fed5f73`  
		Last Modified: Thu, 17 Aug 2023 10:03:32 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d5b35c21c4433ce413a82ffbed47383929d41d661b7209d5a6f6400cf10ab7`  
		Last Modified: Thu, 17 Aug 2023 13:42:32 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae5db696e9d4d6a741363d985e2d2a4f15ed8f1b3874ce0d263900547cbb35b`  
		Last Modified: Thu, 17 Aug 2023 13:43:03 GMT  
		Size: 129.9 MB (129854832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980b760616ea56b24e9e4b5a4ba4f78b852108b5d17c44eda87864ca9e3a069a`  
		Last Modified: Thu, 17 Aug 2023 13:42:29 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef95fabaf2c0693dfb3e8204b2141e2a612933b18d45007e91d73cf1600b9b1`  
		Last Modified: Thu, 17 Aug 2023 13:42:29 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca114f4e5958c44596f54a58646c0281fa3d948b058dec3b671ab7b3c17792b`  
		Last Modified: Thu, 17 Aug 2023 13:42:30 GMT  
		Size: 3.1 MB (3144718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:853c1446167f62a5f535b301b0aec183bac4ea046545d86c4d6844c8b5c1472b`  
		Last Modified: Thu, 17 Aug 2023 13:42:42 GMT  
		Size: 74.9 MB (74896393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d484ec4f1413c3abbdd0272c4b5c999ee726815b4a72825156dbf7172c3a63`  
		Last Modified: Thu, 17 Aug 2023 13:42:29 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:bookworm` - linux; s390x

```console
$ docker pull redmine@sha256:d52997180446f06a793b4b02f275febbd48af41c61b3d1c5b56b64a6171b6880
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.9 MB (267921862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2efe112883c410ed13a820d46b4fead98abea0579bc2aaae96ac736f80f999`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 07 Sep 2023 00:43:39 GMT
ADD file:2a617cce71dc34ce7b62d4b1da4b45cca574c219300ba2be25396630f80bb9cd in / 
# Thu, 07 Sep 2023 00:43:47 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 08:55:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 08:55:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 07 Sep 2023 08:55:09 GMT
ENV LANG=C.UTF-8
# Thu, 07 Sep 2023 09:14:15 GMT
ENV RUBY_MAJOR=3.1
# Thu, 07 Sep 2023 09:14:15 GMT
ENV RUBY_VERSION=3.1.4
# Thu, 07 Sep 2023 09:14:16 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Thu, 07 Sep 2023 09:18:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 07 Sep 2023 09:18:40 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 07 Sep 2023 09:18:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 07 Sep 2023 09:18:42 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 09:18:44 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 07 Sep 2023 09:18:45 GMT
CMD ["irb"]
# Thu, 07 Sep 2023 19:45:03 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 07 Sep 2023 19:46:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 19:47:02 GMT
ENV RAILS_ENV=production
# Thu, 07 Sep 2023 19:47:03 GMT
WORKDIR /usr/src/redmine
# Thu, 07 Sep 2023 19:47:03 GMT
ENV HOME=/home/redmine
# Thu, 07 Sep 2023 19:47:05 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 07 Sep 2023 19:47:05 GMT
ENV REDMINE_VERSION=5.0.5
# Thu, 07 Sep 2023 19:47:06 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.5.tar.gz
# Thu, 07 Sep 2023 19:47:06 GMT
ENV REDMINE_DOWNLOAD_SHA256=a89ad1c4bb9bf025e6527c77ab18c8faf7749c94a975caf2cfdbba00eb12a481
# Thu, 07 Sep 2023 19:47:13 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 07 Sep 2023 19:50:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 07 Sep 2023 19:50:16 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 07 Sep 2023 19:50:16 GMT
COPY file:f61e8718e722eba56748d9a7e58011159861fb49784b1ad721746c1fc5735b6d in / 
# Thu, 07 Sep 2023 19:50:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 19:50:17 GMT
EXPOSE 3000
# Thu, 07 Sep 2023 19:50:18 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:68043338ec5d8515f0dcc40f82eb11d30dd8539a1d30984e4b157df8779f6d53`  
		Last Modified: Thu, 07 Sep 2023 00:49:40 GMT  
		Size: 27.5 MB (27489648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722e7c27cf8173dfe3e461fc8445f102dec0f642cd4ae6ea7d6a84b73e482815`  
		Last Modified: Thu, 07 Sep 2023 09:37:16 GMT  
		Size: 12.0 MB (12021648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab5a3a3f1362e13afca4308287c2bb1f93e51a589cb5870fbbb7d3cce76fdb7`  
		Last Modified: Thu, 07 Sep 2023 09:37:14 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ac82a5c30d7c5d967b06f9df196f5a98352eac9543bc39d548c423d04f7936`  
		Last Modified: Thu, 07 Sep 2023 09:38:58 GMT  
		Size: 32.5 MB (32538950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ba3e2e1eb43dd9667620c5a70f1673edf9932965491b85b3e471e86622c30f`  
		Last Modified: Thu, 07 Sep 2023 09:38:55 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63bacc1c33b670aeb1953a9d5a4f90b410c8e213b4537c07015491538d0fc4ff`  
		Last Modified: Thu, 07 Sep 2023 19:50:47 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd6fb2827d6286fae52321d90573a2ed8de4ac056c7ff2344606f436a0decdc`  
		Last Modified: Thu, 07 Sep 2023 19:51:04 GMT  
		Size: 118.7 MB (118667327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a5b26cc5620784ec520e60b74b8f8e2622646ad58d07b918a294b0e3ed618c`  
		Last Modified: Thu, 07 Sep 2023 19:50:46 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593556fff82000773459016b86e51b28f3ed22f1ba71736ba77da4477b168503`  
		Last Modified: Thu, 07 Sep 2023 19:50:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a9a9c15cb09c4a45617a4f5685cc7c03cca0971c82fea68b25a75fb83fbd06`  
		Last Modified: Thu, 07 Sep 2023 19:50:47 GMT  
		Size: 3.1 MB (3144724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e063fe251e51d99739f146028208c3ed568b916b9fe0e86fdbb117f50cd61f`  
		Last Modified: Thu, 07 Sep 2023 19:50:54 GMT  
		Size: 74.1 MB (74055720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268b3691c33aedea3b2809d09b8d5ade686146bf5ceda455286ec5c67f2b302e`  
		Last Modified: Thu, 07 Sep 2023 19:50:46 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
