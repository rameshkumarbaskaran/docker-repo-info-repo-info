## `redmine:5-bullseye`

```console
$ docker pull redmine@sha256:fe7b741ec1f8071863ad594fb70fb83d4fbda3bcfb9bcc42e7214b42413e3d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `redmine:5-bullseye` - linux; amd64

```console
$ docker pull redmine@sha256:fc968cde3e0f03471a305847ef822bcdfa88c6bd13cb0b5495dd9bdd77a838ce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 MB (236215780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b57b06ab59213be653724a40b187da5df53a2c40456b0f462756c31e3aefa3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:18 GMT
ADD file:966d3669b40f5fbaecee1ecbeb58debe19001076da5d94717080d55efbc25971 in / 
# Tue, 29 Mar 2022 00:22:19 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 10:28:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 10:28:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 29 Mar 2022 10:28:51 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 10:28:51 GMT
ENV RUBY_MAJOR=3.1
# Tue, 12 Apr 2022 18:22:38 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 12 Apr 2022 18:22:38 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 12 Apr 2022 18:24:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Apr 2022 18:24:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Apr 2022 18:24:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Apr 2022 18:24:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Apr 2022 18:25:00 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Apr 2022 18:25:00 GMT
CMD ["irb"]
# Tue, 12 Apr 2022 19:53:03 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 12 Apr 2022 19:53:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Apr 2022 19:53:30 GMT
ENV RAILS_ENV=production
# Tue, 12 Apr 2022 19:53:30 GMT
WORKDIR /usr/src/redmine
# Tue, 12 Apr 2022 19:53:30 GMT
ENV HOME=/home/redmine
# Tue, 12 Apr 2022 19:53:31 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 12 Apr 2022 19:53:31 GMT
ENV REDMINE_VERSION=5.0.0
# Tue, 12 Apr 2022 19:53:31 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.0.tar.gz
# Tue, 12 Apr 2022 19:53:31 GMT
ENV REDMINE_DOWNLOAD_SHA256=7e840dec846646dae52fff5c631b135d1c915d6e03ea6f01ca8f12ad35803bef
# Tue, 12 Apr 2022 19:53:34 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 12 Apr 2022 19:54:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Apr 2022 19:54:05 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 12 Apr 2022 19:54:05 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 12 Apr 2022 19:54:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 19:54:06 GMT
EXPOSE 3000
# Tue, 12 Apr 2022 19:54:06 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c229119241af7b23b121052a1cae4c03e0a477a72ea6a7f463ad7623ff8f274b`  
		Last Modified: Tue, 29 Mar 2022 00:27:16 GMT  
		Size: 31.4 MB (31378457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14a196c62ee705bf37cfab91ea1d171f7b636ffd65269877b758f726189872e`  
		Last Modified: Tue, 29 Mar 2022 11:19:01 GMT  
		Size: 10.0 MB (9990916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365bbf24384cc62b2e96112071ead0fb9d34bb8f42158306d2b628b641fc0068`  
		Last Modified: Tue, 29 Mar 2022 11:18:59 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8784bbb4c7ec0168d6c466e23dac93bd30b1448a26aed635fd4049e2ad800bac`  
		Last Modified: Tue, 12 Apr 2022 19:14:08 GMT  
		Size: 32.4 MB (32435682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4692036d56896f8c38296e16c51dd6b2032285fc66bb8e8ef2a8600c5ce315`  
		Last Modified: Tue, 12 Apr 2022 19:14:05 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef29ac2f7559a0dc10853f7f8173e4ed005e605fee64089cb6ba875caa7a6d3`  
		Last Modified: Tue, 12 Apr 2022 20:05:50 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a5fde2c67ec894695edb96e6ce4961e98582693ad567f019ab040a3612fcfc`  
		Last Modified: Tue, 12 Apr 2022 20:06:06 GMT  
		Size: 102.0 MB (102011120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71e445157243c793b63da3a7495cab37c31c9e5701f23167b69b9423cf52b28`  
		Last Modified: Tue, 12 Apr 2022 20:05:48 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177d8fd2127562f86be51b1ce28eefa7ac5d47c38dbe218b2ea4a65af2c7f6e9`  
		Last Modified: Tue, 12 Apr 2022 20:05:48 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e127743aeaf0a5b14a7a2862a73674c0e9ba559e4bf639380a7e5232b0037f5`  
		Last Modified: Tue, 12 Apr 2022 20:05:49 GMT  
		Size: 3.1 MB (3126578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c9f52f48b369b69d80f42a2ec3e3723a5ba960381ecc651f65d55090462ef1`  
		Last Modified: Tue, 12 Apr 2022 20:05:55 GMT  
		Size: 57.3 MB (57268783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9360059bb68ef816713f108b2244639b97b14a1b0f878b42188d2c71b71548c4`  
		Last Modified: Tue, 12 Apr 2022 20:05:48 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:9863f001e3283b172b3c73df9f389ae069ef3e7d527a83ed803bdc992d4ce338
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.1 MB (230129395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8383bbef3df480b3f89f93ce1cd427d95d3c77348cf86ecd2ae1c20f246ab170`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:17 GMT
ADD file:e95289cd39de0f389d09cda9edf8476d5da371bc68d76e820c5e1c310dc54baf in / 
# Tue, 29 Mar 2022 00:43:17 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 01:04:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 01:04:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 30 Mar 2022 01:04:40 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 01:04:41 GMT
ENV RUBY_MAJOR=3.1
# Tue, 12 Apr 2022 18:43:27 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 12 Apr 2022 18:43:28 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 12 Apr 2022 18:45:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Apr 2022 18:45:40 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Apr 2022 18:45:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Apr 2022 18:45:42 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Apr 2022 18:45:43 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Apr 2022 18:45:44 GMT
CMD ["irb"]
# Tue, 12 Apr 2022 21:44:32 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 12 Apr 2022 21:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Apr 2022 21:45:00 GMT
ENV RAILS_ENV=production
# Tue, 12 Apr 2022 21:45:01 GMT
WORKDIR /usr/src/redmine
# Tue, 12 Apr 2022 21:45:02 GMT
ENV HOME=/home/redmine
# Tue, 12 Apr 2022 21:45:04 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 12 Apr 2022 21:45:04 GMT
ENV REDMINE_VERSION=5.0.0
# Tue, 12 Apr 2022 21:45:05 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.0.tar.gz
# Tue, 12 Apr 2022 21:45:06 GMT
ENV REDMINE_DOWNLOAD_SHA256=7e840dec846646dae52fff5c631b135d1c915d6e03ea6f01ca8f12ad35803bef
# Tue, 12 Apr 2022 21:45:10 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 12 Apr 2022 21:45:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Apr 2022 21:45:41 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 12 Apr 2022 21:45:42 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 12 Apr 2022 21:45:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 21:45:44 GMT
EXPOSE 3000
# Tue, 12 Apr 2022 21:45:45 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2203022c5aa978ec114a15a7cdc2c323c65922d3b0a8eab11d50811bb9ae1cfb`  
		Last Modified: Tue, 29 Mar 2022 00:50:04 GMT  
		Size: 30.1 MB (30064311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6f29ca162065ee9762bc3cc495618ef13e2942009a5b8aef07e4da875edb31`  
		Last Modified: Wed, 30 Mar 2022 02:04:44 GMT  
		Size: 9.0 MB (9035255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9987e0079ca5ec9f2ced5c365ab9fb5b01fac470fb359dee0903acbeca51dd16`  
		Last Modified: Wed, 30 Mar 2022 02:04:42 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b48196e433ad9b3a1e904929f0f9daa120f843a3eab5baf46d167e78676331e2`  
		Last Modified: Tue, 12 Apr 2022 19:38:16 GMT  
		Size: 31.6 MB (31589118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27b69cce8ce2ad547e2a433ab3fa14a46d8f28acc3535d1fb6f361ba7892f73`  
		Last Modified: Tue, 12 Apr 2022 19:38:10 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731156e1e1b3fa28b8eab32d98d903eaf0fa34d5254881b5b96dc019bd3239e0`  
		Last Modified: Tue, 12 Apr 2022 22:01:27 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85afeb3928338767f16551065dd99415ec79117586eab382e44f013010fb87f0`  
		Last Modified: Tue, 12 Apr 2022 22:01:42 GMT  
		Size: 99.8 MB (99799816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0812e0716af04057e08525cc9fec0ab3988c5f28ca4be44cfd4742b4739380c2`  
		Last Modified: Tue, 12 Apr 2022 22:01:24 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c54fb00a95a031c5c2f6d00a7b824a89b04a942494e2fa209ae983ee928b32f`  
		Last Modified: Tue, 12 Apr 2022 22:01:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5360485bfdedaf5ce050b03dc916b846856c8efb4a3b606ef803a422821f1ec3`  
		Last Modified: Tue, 12 Apr 2022 22:01:25 GMT  
		Size: 3.1 MB (3126569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce7275838dfd924419e1692713f47e55d9e7c0e26103c8e2f16fb63a33f61f3`  
		Last Modified: Tue, 12 Apr 2022 22:01:31 GMT  
		Size: 56.5 MB (56510299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86bfe024ecd092002477c13bcf9fd328850f735da84e9078e801c460556cb57a`  
		Last Modified: Tue, 12 Apr 2022 22:01:24 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:5-bullseye` - linux; 386

```console
$ docker pull redmine@sha256:a5ca385bfd9c773939c781abaf19d26147069651d34b99fb9f778a9b7bc7b8b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.9 MB (237942205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d50aacef237d8a7aae46206338b545e49d59a8225e7ba547d937bf48d75c22`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:42:01 GMT
ADD file:d093057c080a13cc4370d0e786857751004b8cd3c93368742512abbee4f1de83 in / 
# Tue, 29 Mar 2022 00:42:01 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 09:57:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 09:57:26 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 29 Mar 2022 09:57:26 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 09:57:27 GMT
ENV RUBY_MAJOR=3.1
# Tue, 12 Apr 2022 18:41:46 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 12 Apr 2022 18:41:47 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 12 Apr 2022 18:44:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Apr 2022 18:44:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Apr 2022 18:44:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Apr 2022 18:44:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Apr 2022 18:44:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Apr 2022 18:44:06 GMT
CMD ["irb"]
# Tue, 12 Apr 2022 21:39:01 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 12 Apr 2022 21:39:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Apr 2022 21:39:39 GMT
ENV RAILS_ENV=production
# Tue, 12 Apr 2022 21:39:39 GMT
WORKDIR /usr/src/redmine
# Tue, 12 Apr 2022 21:39:40 GMT
ENV HOME=/home/redmine
# Tue, 12 Apr 2022 21:39:41 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 12 Apr 2022 21:39:42 GMT
ENV REDMINE_VERSION=5.0.0
# Tue, 12 Apr 2022 21:39:43 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.0.tar.gz
# Tue, 12 Apr 2022 21:39:44 GMT
ENV REDMINE_DOWNLOAD_SHA256=7e840dec846646dae52fff5c631b135d1c915d6e03ea6f01ca8f12ad35803bef
# Tue, 12 Apr 2022 21:39:49 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 12 Apr 2022 21:40:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Apr 2022 21:40:24 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 12 Apr 2022 21:40:25 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 12 Apr 2022 21:40:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 21:40:26 GMT
EXPOSE 3000
# Tue, 12 Apr 2022 21:40:27 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:fec59da75229f638ca2878278d3859a1a8b73a20d5c0c043354eb37129ebb8bf`  
		Last Modified: Tue, 29 Mar 2022 00:49:10 GMT  
		Size: 32.4 MB (32389518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97056a7b1dd6e578c21e2af25f613c64cfd3f6709ea95ef1a5f57b3582aa3a2d`  
		Last Modified: Tue, 29 Mar 2022 10:38:06 GMT  
		Size: 11.8 MB (11788492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69a680da3ca1ea5bb12eb18b3ec7db1c4d6bc215a757ea067a4325dd39766a8`  
		Last Modified: Tue, 29 Mar 2022 10:38:04 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da219e907bb936e188388b3c9f546ad95595e9a4982aaac4fe207140865c946c`  
		Last Modified: Tue, 12 Apr 2022 19:35:56 GMT  
		Size: 30.8 MB (30787794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9864a2e7c8a2bc4d371746851b3f7ad54010b29f11a4b755f52186fc4d028046`  
		Last Modified: Tue, 12 Apr 2022 19:35:53 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bda0d50db9e76c1b8973c0b494bd2ad708e6d06da20714dac26ee443c1595ff`  
		Last Modified: Tue, 12 Apr 2022 21:53:14 GMT  
		Size: 1.6 KB (1615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671d4361fe1d1f4f06fa0aa474733a25f40edc56e1b1870d915858feb2a04f63`  
		Last Modified: Tue, 12 Apr 2022 21:53:33 GMT  
		Size: 103.4 MB (103362087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ad5529867aaa51440ff7e14c36259d64ccecc0a850e95ee4df92a4d2be7726`  
		Last Modified: Tue, 12 Apr 2022 21:53:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df96eb9e7728d958b54dbff55d3b76f0bb390784a99101540dfa637cd7ea0445`  
		Last Modified: Tue, 12 Apr 2022 21:53:12 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd80043a46296596fd678717a8e9b1441541890cfe51ef17574886a9bf338911`  
		Last Modified: Tue, 12 Apr 2022 21:53:13 GMT  
		Size: 3.1 MB (3126583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07baa9c8d48a4667d696dbaaf9a36e5aa63edd6dcc31a4e0cb36a9afba08a6b8`  
		Last Modified: Tue, 12 Apr 2022 21:53:20 GMT  
		Size: 56.5 MB (56483713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0df5ef29d131e3bfd5a3ea7948c07ff0be23b9c73e73257ae13d0008433edf0`  
		Last Modified: Tue, 12 Apr 2022 21:53:12 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
