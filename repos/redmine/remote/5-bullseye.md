## `redmine:5-bullseye`

```console
$ docker pull redmine@sha256:7e8e70cf09b2d35810141759cddf4632b2c2ea45b43ae0b638f01a3ef510b518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `redmine:5-bullseye` - linux; amd64

```console
$ docker pull redmine@sha256:5abbe8bd2d4631e3b436cd8fdb04556266786003cae1a263c7a0114d4cf5547d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236916665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3fddac9e732f1d83783a0adeaa3c2a12c440a6032ac0a75e7d935c2be4152b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 10:34:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 10:34:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 28 May 2022 10:34:08 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 10:43:35 GMT
ENV RUBY_MAJOR=3.1
# Sat, 28 May 2022 10:43:35 GMT
ENV RUBY_VERSION=3.1.2
# Sat, 28 May 2022 10:43:35 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Sat, 28 May 2022 10:45:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 28 May 2022 10:45:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 28 May 2022 10:45:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 28 May 2022 10:45:56 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 10:45:56 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 28 May 2022 10:45:56 GMT
CMD ["irb"]
# Sun, 29 May 2022 04:38:27 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 29 May 2022 04:38:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Sun, 29 May 2022 04:38:53 GMT
ENV RAILS_ENV=production
# Sun, 29 May 2022 04:38:53 GMT
WORKDIR /usr/src/redmine
# Sun, 29 May 2022 04:38:53 GMT
ENV HOME=/home/redmine
# Sun, 29 May 2022 04:38:54 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 29 May 2022 04:38:54 GMT
ENV REDMINE_VERSION=5.0.1
# Sun, 29 May 2022 04:38:54 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.1.tar.gz
# Sun, 29 May 2022 04:38:54 GMT
ENV REDMINE_DOWNLOAD_SHA256=6916c5fe39d09e56921fe321464e3eb2d206d52075c61da7b8a89247e6908bb7
# Sun, 29 May 2022 04:38:57 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 29 May 2022 04:39:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 29 May 2022 04:39:31 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 29 May 2022 04:39:31 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Sun, 29 May 2022 04:39:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 29 May 2022 04:39:31 GMT
EXPOSE 3000
# Sun, 29 May 2022 04:39:32 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf9b45ce596a6f4f1faf8c7370d2ee41943867c82cc4debc7197b6bb6dae1550`  
		Last Modified: Sat, 28 May 2022 11:08:40 GMT  
		Size: 10.0 MB (9992042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa14af4873b6b12ce5ff7b71db99fce3804547617da6ff5963fef2ee59eb478`  
		Last Modified: Sat, 28 May 2022 11:08:38 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3867d746a4fbf4cc142f4d071e74abaaad3de01d5e2208fc390933d1ed9717f0`  
		Last Modified: Sat, 28 May 2022 11:10:03 GMT  
		Size: 32.4 MB (32436156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447bd70463773d3cfb97f47adf5bbff79770b29c3392cab677219fecfb448199`  
		Last Modified: Sat, 28 May 2022 11:10:00 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735e2b6da90f0ca41a3c6921f15013b101b5a5feb3a2e2a9092a407293df53b5`  
		Last Modified: Sun, 29 May 2022 04:41:57 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830cbedfe5986848a1026dd6e5d71cec44b30635629842fe82d3ce927d076756`  
		Last Modified: Sun, 29 May 2022 04:42:12 GMT  
		Size: 102.0 MB (102010134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9357bbb3b14655b32b25ddcbc4518bf6e283c3c5361f4d608dc9bb641df67945`  
		Last Modified: Sun, 29 May 2022 04:41:55 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b32a976cbf4665eb3359dd37350fc2fc583acf84082712a593f2ebfe2cdb47`  
		Last Modified: Sun, 29 May 2022 04:41:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4c9cad3d1147ca3e65a63ff38a10da11139d295a076078e125339452b40699`  
		Last Modified: Sun, 29 May 2022 04:41:55 GMT  
		Size: 3.1 MB (3127271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77e44f7780cff86b070f9a79d561dde739fc3b07e53e72ac7a3e3473d9cc07b`  
		Last Modified: Sun, 29 May 2022 04:42:01 GMT  
		Size: 58.0 MB (57967546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86cd31c7064f1450b144190f936dc73c73e30bc34bbc9bb142638fc6f454d608`  
		Last Modified: Sun, 29 May 2022 04:41:55 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:33c412207a138477000d4496ffd9e30f5e7005694ec90ad1800beaf099e3ad80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230800097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:692da3182d7d1ee1735bf7459d716c4ac9add5e787172ada3539d90c31b297c1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 28 May 2022 00:40:39 GMT
ADD file:55b4fe3115c684f545e4e4148c93745f12192976a08c37d090fcac708fb709a7 in / 
# Sat, 28 May 2022 00:40:39 GMT
CMD ["bash"]
# Sat, 28 May 2022 09:44:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 09:44:02 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 28 May 2022 09:44:03 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 09:50:36 GMT
ENV RUBY_MAJOR=3.1
# Sat, 28 May 2022 09:50:37 GMT
ENV RUBY_VERSION=3.1.2
# Sat, 28 May 2022 09:50:38 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Sat, 28 May 2022 09:53:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 28 May 2022 09:53:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 28 May 2022 09:53:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 28 May 2022 09:53:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 09:53:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 28 May 2022 09:53:20 GMT
CMD ["irb"]
# Sun, 29 May 2022 00:17:08 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 29 May 2022 00:17:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Sun, 29 May 2022 00:17:37 GMT
ENV RAILS_ENV=production
# Sun, 29 May 2022 00:17:38 GMT
WORKDIR /usr/src/redmine
# Sun, 29 May 2022 00:17:39 GMT
ENV HOME=/home/redmine
# Sun, 29 May 2022 00:17:41 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 29 May 2022 00:17:41 GMT
ENV REDMINE_VERSION=5.0.1
# Sun, 29 May 2022 00:17:42 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.1.tar.gz
# Sun, 29 May 2022 00:17:43 GMT
ENV REDMINE_DOWNLOAD_SHA256=6916c5fe39d09e56921fe321464e3eb2d206d52075c61da7b8a89247e6908bb7
# Sun, 29 May 2022 00:17:47 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 29 May 2022 00:18:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 29 May 2022 00:18:19 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 29 May 2022 00:18:20 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Sun, 29 May 2022 00:18:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 29 May 2022 00:18:22 GMT
EXPOSE 3000
# Sun, 29 May 2022 00:18:23 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:dc1f00a5d701e86e2cd2568b860c61b393d66be1341e7267d07e6e57448ceeba`  
		Last Modified: Sat, 28 May 2022 00:47:35 GMT  
		Size: 30.1 MB (30065728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5abc6c8ae3d2742ede1d048644d94b8645f342236c0e9285c55851606b981f`  
		Last Modified: Sat, 28 May 2022 10:08:21 GMT  
		Size: 9.0 MB (9035742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8466cad9c45d3ea149cf3b39478c4b52b84d589aaba5b3cd835d5edf07b84523`  
		Last Modified: Sat, 28 May 2022 10:08:19 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ced53c0cbdad2cee90635bdd19636f7b9adfa572a52d1202eb545557f48738e`  
		Last Modified: Sat, 28 May 2022 10:09:16 GMT  
		Size: 31.6 MB (31589514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf773e09993fb5be0af730ec37c2f0fafbadfd6d27b5452b9d48193923708fa`  
		Last Modified: Sat, 28 May 2022 10:09:13 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99cfb128e4b6f1cee2320eb667e7f94a5f2d3ee94fbd10a60865580721de61eb`  
		Last Modified: Sun, 29 May 2022 00:21:21 GMT  
		Size: 1.6 KB (1620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75221ada9d864eebf0dfbbcfe03fadb781dcc9e01ec3b8dea16a34d3a4569133`  
		Last Modified: Sun, 29 May 2022 00:21:36 GMT  
		Size: 99.8 MB (99799090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24103fe89391f0553c68c237bc0dbc35847e3eebd3ce6958a5e46c72b0eded39`  
		Last Modified: Sun, 29 May 2022 00:21:18 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e2f76be7c317e250fb9bba2c3a1fec17e908fec980cf2e41d4dc7b8c78e891`  
		Last Modified: Sun, 29 May 2022 00:21:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73711a77cb5cffa578dc4540d2c57d1f45f97d4403100db58e844866b5fa0f0`  
		Last Modified: Sun, 29 May 2022 00:21:19 GMT  
		Size: 3.1 MB (3127237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da0b39efaaa7e85f8d043bfd6c58537e79e8e0c9c49abcb9e4cfe118891f42d`  
		Last Modified: Sun, 29 May 2022 00:21:26 GMT  
		Size: 57.2 MB (57178760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:549e0460a2210f70eeda5f55bc7581e89ac570c61e45e90044531f78f996e572`  
		Last Modified: Sun, 29 May 2022 00:21:18 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:5-bullseye` - linux; 386

```console
$ docker pull redmine@sha256:169276e798c0bbf457dfa989807951ed4e934effaefc15b1022173b1c3ee304f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.6 MB (238606836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac560afb4cdb680cd510f7c843c460d7a5c46c5a7c0e2bc9545fbb687790c5f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 28 May 2022 00:39:33 GMT
ADD file:8320d7b95b9f68313e086faff974bb38977e0c9da4984afb6382eb0405742bde in / 
# Sat, 28 May 2022 00:39:33 GMT
CMD ["bash"]
# Sat, 28 May 2022 11:46:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 11:46:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 28 May 2022 11:46:08 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 11:55:55 GMT
ENV RUBY_MAJOR=3.1
# Sat, 28 May 2022 11:55:56 GMT
ENV RUBY_VERSION=3.1.2
# Sat, 28 May 2022 11:55:57 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Sat, 28 May 2022 11:58:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 28 May 2022 11:58:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 28 May 2022 11:58:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 28 May 2022 11:58:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 11:58:13 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 28 May 2022 11:58:14 GMT
CMD ["irb"]
# Sat, 28 May 2022 16:19:18 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sat, 28 May 2022 16:19:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 16:19:53 GMT
ENV RAILS_ENV=production
# Sat, 28 May 2022 16:19:53 GMT
WORKDIR /usr/src/redmine
# Sat, 28 May 2022 16:19:54 GMT
ENV HOME=/home/redmine
# Sat, 28 May 2022 16:19:55 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 28 May 2022 16:19:56 GMT
ENV REDMINE_VERSION=5.0.1
# Sat, 28 May 2022 16:19:57 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.1.tar.gz
# Sat, 28 May 2022 16:19:58 GMT
ENV REDMINE_DOWNLOAD_SHA256=6916c5fe39d09e56921fe321464e3eb2d206d52075c61da7b8a89247e6908bb7
# Sat, 28 May 2022 16:20:02 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 28 May 2022 16:20:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 28 May 2022 16:20:35 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 28 May 2022 16:20:37 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Sat, 28 May 2022 16:20:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 28 May 2022 16:20:38 GMT
EXPOSE 3000
# Sat, 28 May 2022 16:20:39 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5e7494d2ee6c81c73ce32f8bde3ea8658c6224c2cc22d7bb01df4bc3d42949aa`  
		Last Modified: Sat, 28 May 2022 00:46:43 GMT  
		Size: 32.4 MB (32390321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77e0b0b5fa1e4f477e1bb8385e0cdbd6d04d2ac97515c4fa775a3b36a7d86dd`  
		Last Modified: Sat, 28 May 2022 12:23:26 GMT  
		Size: 11.8 MB (11789286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e11d89791c88aa49aec29dd8e84b79c05a0de05236ad1f9152830b12c7ea020`  
		Last Modified: Sat, 28 May 2022 12:23:23 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979f3c85c3390b2765beca5c45c0f0cc66b012ad6b043831229a1600907fee27`  
		Last Modified: Sat, 28 May 2022 12:25:02 GMT  
		Size: 30.8 MB (30788960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7a08ff45ecc57fdd4a1e18e04cc97b1047212fb6e4e3c0c9e856d3682be9b1`  
		Last Modified: Sat, 28 May 2022 12:24:58 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b42ecc3fbde62537823a16a549a713b6f01ed231b1cef5d7b66ceaf0372d73`  
		Last Modified: Sat, 28 May 2022 16:23:39 GMT  
		Size: 1.6 KB (1619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18e1d5fb2ad55c898274468723887baf3c7f9e0d3a0d894b5cc1c49255f0fcc`  
		Last Modified: Sat, 28 May 2022 16:23:54 GMT  
		Size: 103.4 MB (103361686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5059a5ce961ff0e9ba2a0cd1c793627dde100430699e4498d77f8e29b4f92e85`  
		Last Modified: Sat, 28 May 2022 16:23:36 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b35fe5f12421e3cf710ea4ddc568242a477f04c1a4f7b0df4164534f9274284`  
		Last Modified: Sat, 28 May 2022 16:23:36 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e18f51eb0574312b3cd9a9ec2b7571d731b6b221a9637384e5dcb1425be17e1`  
		Last Modified: Sat, 28 May 2022 16:23:38 GMT  
		Size: 3.1 MB (3127235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db26596743afe7408911649fa8d3269d5812031b54ada35c0c52f1f195f15b5`  
		Last Modified: Sat, 28 May 2022 16:23:44 GMT  
		Size: 57.1 MB (57145329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb80f593537c853742e9f3d507f7c21289cfe818ee0a26ad89cd506b62af0f9`  
		Last Modified: Sat, 28 May 2022 16:23:36 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
