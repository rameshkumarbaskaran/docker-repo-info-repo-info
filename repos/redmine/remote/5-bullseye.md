## `redmine:5-bullseye`

```console
$ docker pull redmine@sha256:111a9c74c03bd34177e75d5ccde9af0c4fc3760dd1efc31045ee7311b059d36c
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

### `redmine:5-bullseye` - linux; amd64

```console
$ docker pull redmine@sha256:26ed292e30ef92b7200192d01ba964b88266f36ac288f75bc63bd55668106428
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 MB (237041138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc28c5d18648ded35d26ca41838853157f53003dd000ca90e6803d2bcb3f9a4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 09:02:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 09:02:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 15 Nov 2022 09:02:08 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 09:07:54 GMT
ENV RUBY_MAJOR=3.1
# Tue, 15 Nov 2022 09:07:55 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 15 Nov 2022 09:07:55 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 15 Nov 2022 09:10:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 15 Nov 2022 09:10:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 15 Nov 2022 09:10:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 15 Nov 2022 09:10:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 09:10:20 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 15 Nov 2022 09:10:20 GMT
CMD ["irb"]
# Tue, 15 Nov 2022 09:26:40 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 15 Nov 2022 09:27:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 09:27:12 GMT
ENV RAILS_ENV=production
# Tue, 15 Nov 2022 09:27:13 GMT
WORKDIR /usr/src/redmine
# Tue, 15 Nov 2022 09:27:13 GMT
ENV HOME=/home/redmine
# Tue, 15 Nov 2022 09:27:13 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 15 Nov 2022 09:27:13 GMT
ENV REDMINE_VERSION=5.0.3
# Tue, 15 Nov 2022 09:27:13 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.3.tar.gz
# Tue, 15 Nov 2022 09:27:14 GMT
ENV REDMINE_DOWNLOAD_SHA256=594068014b2c5eceb3510bfd8786b8d7bc837896912a95cbb24dd76941d36ca0
# Tue, 15 Nov 2022 09:27:17 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 15 Nov 2022 09:27:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 15 Nov 2022 09:27:50 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 15 Nov 2022 09:27:50 GMT
COPY file:f61e8718e722eba56748d9a7e58011159861fb49784b1ad721746c1fc5735b6d in / 
# Tue, 15 Nov 2022 09:27:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 15 Nov 2022 09:27:50 GMT
EXPOSE 3000
# Tue, 15 Nov 2022 09:27:51 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824cc1987b4c3d3fdb89192cea3fd492e595844522888b2bdfb7bc0e15d9c38f`  
		Last Modified: Tue, 15 Nov 2022 09:24:02 GMT  
		Size: 10.0 MB (10020448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e7129cddea3dc930d634f547f58a869e692c5ea4b3183760620cfc8ec67fb7`  
		Last Modified: Tue, 15 Nov 2022 09:24:00 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ebe3be8da43ad18f7bb4ed7711959328c6c9bc23c874d0f827fe9afc3b5e24`  
		Last Modified: Tue, 15 Nov 2022 09:24:38 GMT  
		Size: 32.4 MB (32436969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea2535835d7dbc570141035d49ce6acfad3726f456824892ea3fb88fc120278`  
		Last Modified: Tue, 15 Nov 2022 09:24:34 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66b686a2992c4925e7a214caeab3300e321b7a09dc6ae8f5c4840aa9379e3bd`  
		Last Modified: Tue, 15 Nov 2022 09:30:24 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be4d09540aa8d0a9709718e827e5b254414d99d4d1d5ec23d520071944f9ee6`  
		Last Modified: Tue, 15 Nov 2022 09:30:39 GMT  
		Size: 102.0 MB (102023896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876658288fc3cbcec7a0d4ee83eb0ccfec7a5be4afbc7b0e1990543b9b68fd41`  
		Last Modified: Tue, 15 Nov 2022 09:30:22 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429dd14d23bbf669ba4ae905c749ce390f376bd34e2f04e1e571929821478c89`  
		Last Modified: Tue, 15 Nov 2022 09:30:22 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcfc56ee84785dc51b19b64f19555ce2f1eab5bc9437f5a435841b620afb6a9`  
		Last Modified: Tue, 15 Nov 2022 09:30:23 GMT  
		Size: 3.1 MB (3141779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ea11528bbcafd483bb16e42d4a59458112c46d1cc735aed8a75c6f9624743d`  
		Last Modified: Tue, 15 Nov 2022 09:30:28 GMT  
		Size: 58.0 MB (58000968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:decc661f1394554726b9dce061be0a226caaea62e561403dd8328ec75978acab`  
		Last Modified: Tue, 15 Nov 2022 09:30:22 GMT  
		Size: 2.0 KB (2011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:5-bullseye` - linux; arm variant v5

```console
$ docker pull redmine@sha256:99307deb4da30427f00e7e2e668f05c8ab5cbb2823718cc04f37949382b2c08a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (236049396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986a46ca3228d756750480cd3f029c208d43bafb53768284c374325fe2e8e1bc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 25 Oct 2022 03:06:35 GMT
ADD file:015ddb23f9ceec681c3a46b6d48671071fd41c5d56a957f6c96b50b1fc089a36 in / 
# Tue, 25 Oct 2022 03:06:38 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 12:48:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 12:48:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 25 Oct 2022 12:48:17 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 12:53:31 GMT
ENV RUBY_MAJOR=3.1
# Tue, 25 Oct 2022 12:53:31 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 25 Oct 2022 12:53:31 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 25 Oct 2022 12:55:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 25 Oct 2022 12:55:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 25 Oct 2022 12:55:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 25 Oct 2022 12:56:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 12:56:00 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 25 Oct 2022 12:56:00 GMT
CMD ["irb"]
# Tue, 25 Oct 2022 20:21:00 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 25 Oct 2022 20:21:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 20:21:56 GMT
ENV RAILS_ENV=production
# Tue, 25 Oct 2022 20:21:56 GMT
WORKDIR /usr/src/redmine
# Tue, 25 Oct 2022 20:21:57 GMT
ENV HOME=/home/redmine
# Tue, 25 Oct 2022 20:21:59 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 25 Oct 2022 20:21:59 GMT
ENV REDMINE_VERSION=5.0.3
# Tue, 25 Oct 2022 20:22:00 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.3.tar.gz
# Tue, 25 Oct 2022 20:22:00 GMT
ENV REDMINE_DOWNLOAD_SHA256=594068014b2c5eceb3510bfd8786b8d7bc837896912a95cbb24dd76941d36ca0
# Tue, 25 Oct 2022 20:22:05 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 25 Oct 2022 20:24:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 25 Oct 2022 20:24:46 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 25 Oct 2022 20:24:46 GMT
COPY file:f61e8718e722eba56748d9a7e58011159861fb49784b1ad721746c1fc5735b6d in / 
# Tue, 25 Oct 2022 20:24:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 20:24:47 GMT
EXPOSE 3000
# Tue, 25 Oct 2022 20:24:47 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0df644382ba7fd23e9e4166ec2a03ec88b6cc5f640fb45413ecd913ceb901e41`  
		Last Modified: Tue, 25 Oct 2022 03:11:52 GMT  
		Size: 28.9 MB (28918513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb8878514b1d3807eebc837597853d4df1b5b19e2d418cb119b178fa0afe447`  
		Last Modified: Tue, 25 Oct 2022 13:09:11 GMT  
		Size: 8.6 MB (8634124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bbf97e342baae0445611bf7913370d311cf21dbe54d624486a95fd45fd918d`  
		Last Modified: Tue, 25 Oct 2022 13:09:09 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cdd4410f0c7bed557a0020ae65d97016e349ec506866d9baddd694318e782da`  
		Last Modified: Tue, 25 Oct 2022 13:10:16 GMT  
		Size: 31.0 MB (30986004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff721e1dedc201a2223900a473c969b49b6030d70238f8e6089181557b588853`  
		Last Modified: Tue, 25 Oct 2022 13:10:12 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f371948c930003c74388bf276f98965b5ff128d911a44bcc8e7bb528b922f5e`  
		Last Modified: Tue, 25 Oct 2022 20:30:01 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76c45e6e3d888515b96b2da24e0aec498bd9c7455f6a7953eaffc104ec0c82b`  
		Last Modified: Tue, 25 Oct 2022 20:30:25 GMT  
		Size: 97.0 MB (96989968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c75ad72e961ae05e5208da53ea5246de716509f9c9317fba15ee8db8f47f98`  
		Last Modified: Tue, 25 Oct 2022 20:29:58 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265a3afe66ff8ee3db80667473424e6d608f7944619b1549f638b6d9c31647bb`  
		Last Modified: Tue, 25 Oct 2022 20:29:58 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bec1a63c81a3288c4c9298af66bf3c62084ccaf5aadacf629ccf5328ea4262`  
		Last Modified: Tue, 25 Oct 2022 20:30:00 GMT  
		Size: 3.1 MB (3141318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46cdbd86ab76c1f4b1651145ce4d1d5ec390b086ebe0ff4bd4cb1c3018ef545`  
		Last Modified: Tue, 25 Oct 2022 20:30:13 GMT  
		Size: 67.4 MB (67375115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54723016a6cbb047d810c4a4e37e9b6a8c6f5c4aae73595fd481e72dc53c90d0`  
		Last Modified: Tue, 25 Oct 2022 20:29:59 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:5-bullseye` - linux; arm variant v7

```console
$ docker pull redmine@sha256:746c1ea9b843a16e7f4f9a4b12fb88d607c01b91f39958f6375a40e003465a83
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228860696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f398b2bdc467ac2b64cfe1da71fea3725561966256c6d69264529f3b1ec1932`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Nov 2022 03:43:25 GMT
ADD file:1b5c939bd2a35667d7fc44c3009a56ed92a932f512a73df1617dec6ccbd6e6b1 in / 
# Tue, 15 Nov 2022 03:43:26 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 10:40:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 10:40:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 15 Nov 2022 10:40:58 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 10:46:44 GMT
ENV RUBY_MAJOR=3.1
# Tue, 15 Nov 2022 10:46:44 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 15 Nov 2022 10:46:44 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 15 Nov 2022 10:49:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 15 Nov 2022 10:49:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 15 Nov 2022 10:49:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 15 Nov 2022 10:49:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 10:49:06 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 15 Nov 2022 10:49:06 GMT
CMD ["irb"]
# Tue, 15 Nov 2022 11:10:59 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 15 Nov 2022 11:11:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 11:11:32 GMT
ENV RAILS_ENV=production
# Tue, 15 Nov 2022 11:11:32 GMT
WORKDIR /usr/src/redmine
# Tue, 15 Nov 2022 11:11:32 GMT
ENV HOME=/home/redmine
# Tue, 15 Nov 2022 11:11:33 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 15 Nov 2022 11:11:33 GMT
ENV REDMINE_VERSION=5.0.3
# Tue, 15 Nov 2022 11:11:33 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.3.tar.gz
# Tue, 15 Nov 2022 11:11:33 GMT
ENV REDMINE_DOWNLOAD_SHA256=594068014b2c5eceb3510bfd8786b8d7bc837896912a95cbb24dd76941d36ca0
# Tue, 15 Nov 2022 11:11:36 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 15 Nov 2022 11:13:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 15 Nov 2022 11:13:29 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 15 Nov 2022 11:13:29 GMT
COPY file:f61e8718e722eba56748d9a7e58011159861fb49784b1ad721746c1fc5735b6d in / 
# Tue, 15 Nov 2022 11:13:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 15 Nov 2022 11:13:30 GMT
EXPOSE 3000
# Tue, 15 Nov 2022 11:13:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:fd18d0201d0ce0c5e103902d894f5d601fc5dde76688aa7dae786840141d23e4`  
		Last Modified: Tue, 15 Nov 2022 03:50:11 GMT  
		Size: 26.6 MB (26576195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f882748051d83dfb7f7453eeae956b960128447af5d1008295343c9993eb850`  
		Last Modified: Tue, 15 Nov 2022 11:07:13 GMT  
		Size: 8.1 MB (8142757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b303dec2f3fb882d25d0bd1ba1514dae7537c52955b36b8e35ab34bec8868a`  
		Last Modified: Tue, 15 Nov 2022 11:07:11 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403f56f4d1c68bc8b46225b8dadf17f2c61351bd4c0073fabee3d8f879dd043d`  
		Last Modified: Tue, 15 Nov 2022 11:08:02 GMT  
		Size: 30.8 MB (30848936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41a84ea6c480831479df4c6b67b2958abfcaf4405c82223ceeb09345d4ac2d4`  
		Last Modified: Tue, 15 Nov 2022 11:07:58 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250dfd5c2481c0e66e9967142b7efa8222aa65e2f6ff2c7cc407c9021a140bd1`  
		Last Modified: Tue, 15 Nov 2022 11:17:53 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f970287dd4b04fb728f2b39d2afa470d2aa0a38b9e28b37825d5ae36127932`  
		Last Modified: Tue, 15 Nov 2022 11:18:10 GMT  
		Size: 93.1 MB (93134583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516ac86668cd8342fc3b97a102cbc2fe8ac2a99f97f41a1accca52014a352e79`  
		Last Modified: Tue, 15 Nov 2022 11:17:51 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abe7867462e037a5c96c96ab126e60c4cb854c4f4bcde7eaa640bf762b50ace`  
		Last Modified: Tue, 15 Nov 2022 11:17:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a223b6f2c1d20e1fdd7bdf74572bf421610bc7aed72d31cbf187f27748c9ff1c`  
		Last Modified: Tue, 15 Nov 2022 11:17:52 GMT  
		Size: 3.1 MB (3141305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598bd9f613d388155485d62edb94b2032bbd1a002c128a0201e010c05b3f5882`  
		Last Modified: Tue, 15 Nov 2022 11:18:01 GMT  
		Size: 67.0 MB (67012574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d584e5496acd4e70590221c7206f27751f4cbc90a134c7d37ae384f4550e70`  
		Last Modified: Tue, 15 Nov 2022 11:17:51 GMT  
		Size: 2.0 KB (2011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:54070872ca04fd9652d1ba49b4f578ad34ba298d9cc46c0c548113c1e86b4709
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231603693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b08d646bd583ed701b3c4eacc20451b52261b0607995e9e1560c536249b3108`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 22:15:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 22:15:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 25 Oct 2022 22:15:31 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 22:26:39 GMT
ENV RUBY_MAJOR=3.1
# Tue, 25 Oct 2022 22:26:39 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 25 Oct 2022 22:26:39 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 25 Oct 2022 22:28:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 25 Oct 2022 22:28:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 25 Oct 2022 22:28:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 25 Oct 2022 22:28:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 22:28:23 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 25 Oct 2022 22:28:23 GMT
CMD ["irb"]
# Wed, 26 Oct 2022 14:39:02 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 26 Oct 2022 14:39:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 14:39:34 GMT
ENV RAILS_ENV=production
# Wed, 26 Oct 2022 14:39:34 GMT
WORKDIR /usr/src/redmine
# Wed, 26 Oct 2022 14:39:34 GMT
ENV HOME=/home/redmine
# Wed, 26 Oct 2022 14:39:35 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 26 Oct 2022 14:39:35 GMT
ENV REDMINE_VERSION=5.0.3
# Wed, 26 Oct 2022 14:39:35 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.3.tar.gz
# Wed, 26 Oct 2022 14:39:35 GMT
ENV REDMINE_DOWNLOAD_SHA256=594068014b2c5eceb3510bfd8786b8d7bc837896912a95cbb24dd76941d36ca0
# Wed, 26 Oct 2022 14:39:38 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 26 Oct 2022 14:40:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 26 Oct 2022 14:40:04 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 26 Oct 2022 14:40:04 GMT
COPY file:f61e8718e722eba56748d9a7e58011159861fb49784b1ad721746c1fc5735b6d in / 
# Wed, 26 Oct 2022 14:40:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Oct 2022 14:40:04 GMT
EXPOSE 3000
# Wed, 26 Oct 2022 14:40:04 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063764f8706735e58f1173e19b75a66b7aafaff2ff74c483e194837b641d92ee`  
		Last Modified: Tue, 25 Oct 2022 22:57:20 GMT  
		Size: 9.2 MB (9242198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875312304788404d45c14695c9bd2289be5a252600bc79d1c951d3d9f759d52a`  
		Last Modified: Tue, 25 Oct 2022 22:57:18 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c06a6db0c560639b24e5055de836513b1af340697312f3041e464682ebb2e16`  
		Last Modified: Tue, 25 Oct 2022 22:58:55 GMT  
		Size: 31.8 MB (31805840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbeb8641669b49ec4cd0ad9d4fd4750822eb6d05dc93255d953cbf1d2f8ecec`  
		Last Modified: Tue, 25 Oct 2022 22:58:53 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ea3210e4cce30777c7e734947e40b1936bd68cfc801514e165e5f1d36b1cb4`  
		Last Modified: Wed, 26 Oct 2022 14:45:57 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c8a7142c381ec65965e81fc1e927a70aa44e64b580aa5cbec5d17b705e7afc`  
		Last Modified: Wed, 26 Oct 2022 14:46:08 GMT  
		Size: 99.8 MB (99798062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cad6f31e8f6fa17af3aef462f0b6c06613af4ecea78f13ccad321e760a4c760`  
		Last Modified: Wed, 26 Oct 2022 14:45:54 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c864e5fb57fe37761c970c6751c03535bc746eb629a50da026d8d22554478019`  
		Last Modified: Wed, 26 Oct 2022 14:45:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0660c679340d0ddeb5f4dbf93d5373cb0a56ec0633ab539e4ae041fa534b25f`  
		Last Modified: Wed, 26 Oct 2022 14:45:54 GMT  
		Size: 3.1 MB (3141784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba180fb31198ecf6f658ca258b586bdd2658e3595f24c66aac97144549293678`  
		Last Modified: Wed, 26 Oct 2022 14:45:59 GMT  
		Size: 57.5 MB (57547433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200fc4711c8b0ea77aaa24b922447961a3f1cf550f632056b2374481f26b6ac7`  
		Last Modified: Wed, 26 Oct 2022 14:45:54 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:5-bullseye` - linux; 386

```console
$ docker pull redmine@sha256:87cc95e72da5da83bc3b9523d36e2f38d9ad4e5908762db746d2b3d2c06df8f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.7 MB (238728041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b191c23d257bdb9f84be3a27097a64870696420de66baf13c92807e3a591829`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 25 Oct 2022 02:22:34 GMT
ADD file:14adaece72e410cf04ac21a101e5b530aab1d5e5a189a2be72d195ec0ac5e6d4 in / 
# Tue, 25 Oct 2022 02:22:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:45:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 10:45:23 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 25 Oct 2022 10:45:23 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 10:55:11 GMT
ENV RUBY_MAJOR=3.1
# Tue, 25 Oct 2022 10:55:12 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 25 Oct 2022 10:55:13 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 25 Oct 2022 10:57:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 25 Oct 2022 10:57:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 25 Oct 2022 10:57:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 25 Oct 2022 10:57:29 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 10:57:30 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 25 Oct 2022 10:57:31 GMT
CMD ["irb"]
# Tue, 25 Oct 2022 22:17:40 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 25 Oct 2022 22:18:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 22:18:10 GMT
ENV RAILS_ENV=production
# Tue, 25 Oct 2022 22:18:11 GMT
WORKDIR /usr/src/redmine
# Tue, 25 Oct 2022 22:18:11 GMT
ENV HOME=/home/redmine
# Tue, 25 Oct 2022 22:18:12 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 25 Oct 2022 22:18:13 GMT
ENV REDMINE_VERSION=5.0.3
# Tue, 25 Oct 2022 22:18:14 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.3.tar.gz
# Tue, 25 Oct 2022 22:18:15 GMT
ENV REDMINE_DOWNLOAD_SHA256=594068014b2c5eceb3510bfd8786b8d7bc837896912a95cbb24dd76941d36ca0
# Tue, 25 Oct 2022 22:18:19 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 25 Oct 2022 22:18:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 25 Oct 2022 22:18:53 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 25 Oct 2022 22:18:54 GMT
COPY file:f61e8718e722eba56748d9a7e58011159861fb49784b1ad721746c1fc5735b6d in / 
# Tue, 25 Oct 2022 22:18:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 22:18:56 GMT
EXPOSE 3000
# Tue, 25 Oct 2022 22:18:57 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3c83067056c0f1bc4e162249831ac686f3a9a9c64c5366b903581580de8fcac2`  
		Last Modified: Tue, 25 Oct 2022 02:28:26 GMT  
		Size: 32.4 MB (32396384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70e06e1f52f31b6d348c85e99f80633cde53bd2e97c9bb01652f352e2b60cbc`  
		Last Modified: Tue, 25 Oct 2022 11:22:42 GMT  
		Size: 11.8 MB (11788294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75868c2e1989c0872e21c1b2b5ad75c8eef8c37abf94a178fc87ff208cc27ce8`  
		Last Modified: Tue, 25 Oct 2022 11:22:39 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f89b1bc013acd65e721956343170316bebca8e9e52f0561485c23e4bd9a956`  
		Last Modified: Tue, 25 Oct 2022 11:24:09 GMT  
		Size: 30.8 MB (30789217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95899ab50199444d3c5463233808329425b4050302be91ba8153fbb9a75aafc0`  
		Last Modified: Tue, 25 Oct 2022 11:24:06 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a00201eb09c5c9a9e640f5a5225d304fbf1e74ff8773abd54a1ca46a9ecc00e`  
		Last Modified: Tue, 25 Oct 2022 22:21:56 GMT  
		Size: 1.6 KB (1614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f88c428ad1097d78dd0669c0e1ab6eb38d10e57a028851d5b1ab5e34476fc69`  
		Last Modified: Tue, 25 Oct 2022 22:22:11 GMT  
		Size: 103.4 MB (103355655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6379c3354db569c3bf22fa05be6c9c8acb15226e800c811fb6d4fc4bb05f2a95`  
		Last Modified: Tue, 25 Oct 2022 22:21:54 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27a0c2c54054ea5241e81fc2cc4c1e4e8cedf75322970813881c8ce11076fce`  
		Last Modified: Tue, 25 Oct 2022 22:21:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1ea0887b30b9c48aa6cf2cde51f22dfe1fbe2dad95bb0aba54a04bc07010d5`  
		Last Modified: Tue, 25 Oct 2022 22:21:55 GMT  
		Size: 3.1 MB (3141529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13968cd2a08aa4499990b40078d9313152701c2acf580235af4686695a7b688d`  
		Last Modified: Tue, 25 Oct 2022 22:22:01 GMT  
		Size: 57.3 MB (57252726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ec8e0743f890dc86bb746812e1294a18ab0ddaab6530a11f50b95e42d739d3`  
		Last Modified: Tue, 25 Oct 2022 22:21:54 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:5-bullseye` - linux; ppc64le

```console
$ docker pull redmine@sha256:c66ec1560af93112cd9e2db7aafb2441a1c2836f0a8a0f10c197a25f983c7349
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259082300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a6fd4b5b7072c33a67e885f161ff6d19f500068f3990a04e2193a6c7236792`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Nov 2022 05:18:45 GMT
ADD file:520926164fdc762143905745329e568c67289232bec450e48645d82a4613dccf in / 
# Tue, 15 Nov 2022 05:18:47 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 10:19:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 10:19:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 15 Nov 2022 10:19:06 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 10:24:15 GMT
ENV RUBY_MAJOR=3.1
# Tue, 15 Nov 2022 10:24:16 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 15 Nov 2022 10:24:16 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 15 Nov 2022 10:28:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 15 Nov 2022 10:28:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 15 Nov 2022 10:28:23 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 15 Nov 2022 10:28:23 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 10:28:24 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 15 Nov 2022 10:28:25 GMT
CMD ["irb"]
# Tue, 15 Nov 2022 10:41:55 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 15 Nov 2022 10:43:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 10:43:06 GMT
ENV RAILS_ENV=production
# Tue, 15 Nov 2022 10:43:06 GMT
WORKDIR /usr/src/redmine
# Tue, 15 Nov 2022 10:43:07 GMT
ENV HOME=/home/redmine
# Tue, 15 Nov 2022 10:43:08 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 15 Nov 2022 10:43:08 GMT
ENV REDMINE_VERSION=5.0.3
# Tue, 15 Nov 2022 10:43:08 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.3.tar.gz
# Tue, 15 Nov 2022 10:43:09 GMT
ENV REDMINE_DOWNLOAD_SHA256=594068014b2c5eceb3510bfd8786b8d7bc837896912a95cbb24dd76941d36ca0
# Tue, 15 Nov 2022 10:43:14 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 15 Nov 2022 10:46:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 15 Nov 2022 10:46:26 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 15 Nov 2022 10:46:27 GMT
COPY file:f61e8718e722eba56748d9a7e58011159861fb49784b1ad721746c1fc5735b6d in / 
# Tue, 15 Nov 2022 10:46:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 15 Nov 2022 10:46:27 GMT
EXPOSE 3000
# Tue, 15 Nov 2022 10:46:28 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c57913b7d0318ef1a47f0348ce54d9865316776aa1ffb2c7871b1473b3d29407`  
		Last Modified: Tue, 15 Nov 2022 05:24:22 GMT  
		Size: 35.3 MB (35285140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65dfdc42736e7b5d86d42ae43d2d3d33bc51229341c90465b349f23bff5995b0`  
		Last Modified: Tue, 15 Nov 2022 10:39:26 GMT  
		Size: 10.5 MB (10478766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b7377b9eeeaf50b9e7c6d3d2d0ff8b424dd9b359398fdddb5109d0166a4f36`  
		Last Modified: Tue, 15 Nov 2022 10:39:23 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3cd0a799bcbafa9836c5e62603df4d384e3844d4074b59953c8d5d61ab47f41`  
		Last Modified: Tue, 15 Nov 2022 10:40:00 GMT  
		Size: 32.6 MB (32601421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d973a09caa88914eede9d04488761e13555f8b3bb3fde9b4297945382f1fc40e`  
		Last Modified: Tue, 15 Nov 2022 10:39:54 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e7f8ce3cfe6202cb1821e26a11a48d29c3c95e52b31443d7f8e6a969e12d99`  
		Last Modified: Tue, 15 Nov 2022 10:52:58 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8982c4cab89d042b4e631c5075bc60a7808049d28f8403bf3361970a8e8d553`  
		Last Modified: Tue, 15 Nov 2022 10:53:26 GMT  
		Size: 107.5 MB (107520078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9aeb8e3c4378f8420e0d703bb8f21d50b3640551361131d60666c8994e33cd0`  
		Last Modified: Tue, 15 Nov 2022 10:52:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61dde01a3ae394e87fb681cb4e7077b009d40ffa9227652e12ff5ecb0301436`  
		Last Modified: Tue, 15 Nov 2022 10:52:56 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5c38153f00f8ae6f3d7c1a226b897b46d6d70de6864d5fe439408d38055d45`  
		Last Modified: Tue, 15 Nov 2022 10:52:58 GMT  
		Size: 3.1 MB (3141781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9624098257750d90f2cd83d75664bc0882412d447a62b557bb0516e854f32a8`  
		Last Modified: Tue, 15 Nov 2022 10:53:09 GMT  
		Size: 70.1 MB (70050660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa559862e29369dde537ebbe342f4e11e9b86a499e87da1c808d90645555eea`  
		Last Modified: Tue, 15 Nov 2022 10:52:56 GMT  
		Size: 2.0 KB (2012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:5-bullseye` - linux; s390x

```console
$ docker pull redmine@sha256:eb083d7b18002f4762859d5d994ab4ac666f4c532de08cffc97a9d16b1c7a4c4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.8 MB (242789656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca3591679d69344646b5858892841e6bc0b80e7b25a1e03d3dd152f2e631800f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 25 Oct 2022 01:14:42 GMT
ADD file:1bb8efa7f80e494b9d2831490a7e74810350c1f9ee2d100596d2e1cb4c62f529 in / 
# Tue, 25 Oct 2022 01:14:44 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:58:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:58:35 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 25 Oct 2022 06:58:35 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:03:03 GMT
ENV RUBY_MAJOR=3.1
# Tue, 25 Oct 2022 07:03:03 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 25 Oct 2022 07:03:04 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 25 Oct 2022 07:05:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 25 Oct 2022 07:05:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 25 Oct 2022 07:05:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 25 Oct 2022 07:05:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 07:05:02 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 25 Oct 2022 07:05:02 GMT
CMD ["irb"]
# Tue, 25 Oct 2022 16:43:42 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 25 Oct 2022 16:44:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 16:44:47 GMT
ENV RAILS_ENV=production
# Tue, 25 Oct 2022 16:44:48 GMT
WORKDIR /usr/src/redmine
# Tue, 25 Oct 2022 16:44:48 GMT
ENV HOME=/home/redmine
# Tue, 25 Oct 2022 16:44:50 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 25 Oct 2022 16:44:50 GMT
ENV REDMINE_VERSION=5.0.3
# Tue, 25 Oct 2022 16:44:51 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.3.tar.gz
# Tue, 25 Oct 2022 16:44:51 GMT
ENV REDMINE_DOWNLOAD_SHA256=594068014b2c5eceb3510bfd8786b8d7bc837896912a95cbb24dd76941d36ca0
# Tue, 25 Oct 2022 16:44:56 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 25 Oct 2022 16:46:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 25 Oct 2022 16:46:27 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 25 Oct 2022 16:46:27 GMT
COPY file:f61e8718e722eba56748d9a7e58011159861fb49784b1ad721746c1fc5735b6d in / 
# Tue, 25 Oct 2022 16:46:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 16:46:28 GMT
EXPOSE 3000
# Tue, 25 Oct 2022 16:46:28 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:abc14eb2518761d53b91fc564a31b657914f96b531f99a74ac8268f0717b007e`  
		Last Modified: Tue, 25 Oct 2022 01:19:01 GMT  
		Size: 29.7 MB (29650722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54cf0cb053a47824f826d014123eea7c0eedc8b80d6d4d38ad7920f2cf985f3`  
		Last Modified: Tue, 25 Oct 2022 07:15:14 GMT  
		Size: 8.9 MB (8860379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14b826a0c36d14090956db9ed252fc402ab22f27d480edfaeec98791997a103`  
		Last Modified: Tue, 25 Oct 2022 07:15:13 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8059e3324a1c51cb572d9d211a5dadc2b04f910d5700f6d67becf49f2d7cf4`  
		Last Modified: Tue, 25 Oct 2022 07:15:55 GMT  
		Size: 32.3 MB (32250631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a416257be052fff2fa8385c8755170c6142c33e6fc8cc09c6a3b38c90229b6`  
		Last Modified: Tue, 25 Oct 2022 07:15:53 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd628f7ce1475deb803bd22004133b72a0f4dfc40db91aed259611db72c8e4e1`  
		Last Modified: Tue, 25 Oct 2022 16:52:01 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293bd720c3cf2472682db473259b697c5fb3ce2139875188e32f491d4af9b16d`  
		Last Modified: Tue, 25 Oct 2022 16:51:59 GMT  
		Size: 99.2 MB (99155641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075e8bc43ce48020196a97936c2d47c2bdb19cdc0f587a04a64e8a21878664fc`  
		Last Modified: Tue, 25 Oct 2022 16:51:36 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb01b5b347aeb98ed6874fa809991b876a3642bcc6af97f84832aef97d219ef3`  
		Last Modified: Tue, 25 Oct 2022 16:51:36 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eced509f4cd96f57fd727077cf7ad16ea910109e8ce9e2d51462aae4cc84f0b3`  
		Last Modified: Tue, 25 Oct 2022 16:51:37 GMT  
		Size: 3.1 MB (3141788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649cae46f58fd9e3b931c772b67f8343672cd95924b3da19a69afbb1cd29d4e0`  
		Last Modified: Tue, 25 Oct 2022 16:51:44 GMT  
		Size: 69.7 MB (69726033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a181df6cb65c1f12b1b8a080e1ee175000d0bd7cee557519955d3b91c892270`  
		Last Modified: Tue, 25 Oct 2022 16:51:36 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
