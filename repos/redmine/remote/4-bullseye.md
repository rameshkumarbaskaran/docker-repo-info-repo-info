## `redmine:4-bullseye`

```console
$ docker pull redmine@sha256:d3d82ad64f9cbe3b59d50d43ddc0976e9b41991f794d2ff2c88d2b6f5ac1ce65
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

### `redmine:4-bullseye` - linux; amd64

```console
$ docker pull redmine@sha256:af50d424be7017b5b9b22e44f2bce155f821237808c83d4bafc2735c1be8010e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204910081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b04cb171d3322bbf7fe1ba4ae1062c1eecdc701e3f9ac35790aa8bf6b3e1509`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:27 GMT
ADD file:8b1e79f91081eb527b455431af58e823d8b84d9d0c8e5c47cb7bda7507954ae4 in / 
# Wed, 20 Apr 2022 04:43:27 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 13:48:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 13:48:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 20 Apr 2022 13:48:43 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 14:15:37 GMT
ENV RUBY_MAJOR=2.7
# Wed, 20 Apr 2022 14:15:37 GMT
ENV RUBY_VERSION=2.7.6
# Wed, 20 Apr 2022 14:15:37 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Wed, 20 Apr 2022 14:17:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 20 Apr 2022 14:17:25 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Apr 2022 14:17:25 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Apr 2022 14:17:25 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 14:17:26 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 20 Apr 2022 14:17:26 GMT
CMD ["irb"]
# Thu, 21 Apr 2022 11:26:57 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 21 Apr 2022 11:27:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Apr 2022 11:27:21 GMT
ENV RAILS_ENV=production
# Thu, 21 Apr 2022 11:27:21 GMT
WORKDIR /usr/src/redmine
# Thu, 21 Apr 2022 11:27:21 GMT
ENV HOME=/home/redmine
# Thu, 21 Apr 2022 11:27:21 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 21 Apr 2022 11:27:22 GMT
ENV REDMINE_VERSION=4.2.5
# Thu, 21 Apr 2022 11:27:22 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.5.tar.gz
# Thu, 21 Apr 2022 11:27:22 GMT
ENV REDMINE_DOWNLOAD_SHA256=d97084b0eaad7266056814a0c0aec2737f4d23b8f67ce90c01a79b2eb5605984
# Thu, 21 Apr 2022 11:27:25 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 21 Apr 2022 11:28:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 21 Apr 2022 11:28:08 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 21 Apr 2022 11:28:08 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 21 Apr 2022 11:28:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 21 Apr 2022 11:28:08 GMT
EXPOSE 3000
# Thu, 21 Apr 2022 11:28:08 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1fe172e4850f03bb45d41a20174112bc119fbfec42a650edbbd8491aee32e3c3`  
		Last Modified: Wed, 20 Apr 2022 04:48:27 GMT  
		Size: 31.4 MB (31378979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100f29d0fcb2fab0f4d2a795b239feee6df8580994413fe4272b407851faaf3a`  
		Last Modified: Wed, 20 Apr 2022 14:30:59 GMT  
		Size: 10.0 MB (9991861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:937a564b41a154323add828d5515056320d68a3f4b485a88b509260e1c231cad`  
		Last Modified: Wed, 20 Apr 2022 14:30:57 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cfeb9c3dee74234ac4b71e2f736ad3f6282a0b4d0195a164ee57443bd00865`  
		Last Modified: Wed, 20 Apr 2022 14:34:47 GMT  
		Size: 14.6 MB (14582235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0572da5ba7d563ae2a6590117a3b5fe2b9d3ef679881596352be9d3fee9cd3f7`  
		Last Modified: Wed, 20 Apr 2022 14:34:46 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa0e9cbb09c6302807accd36987658e91d1bba5d360ae11c215fa882e1b413e`  
		Last Modified: Thu, 21 Apr 2022 11:32:01 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89575b2f1e5806c2176322805c8b7263d9e95bb3b342219d6838caed7720c0e1`  
		Last Modified: Thu, 21 Apr 2022 11:32:16 GMT  
		Size: 102.0 MB (101987498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e6d7325613a7c9bf219b158d47ce17d6140d0e22102a40b464926ec59b5c5f`  
		Last Modified: Thu, 21 Apr 2022 11:31:59 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51116eea8af952e1428b747835d5ea1b7d66acad56e2f0f493429cfea757c84a`  
		Last Modified: Thu, 21 Apr 2022 11:31:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9b464156cd6d4234ee9633e1379437f8b578bf9cecf5663d869779e6304806a`  
		Last Modified: Thu, 21 Apr 2022 11:31:59 GMT  
		Size: 3.1 MB (3064905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d792d6585efa5be788ce5ea60bb6d29832b37a2e591278c6c5bf71febe1611f7`  
		Last Modified: Thu, 21 Apr 2022 11:32:04 GMT  
		Size: 43.9 MB (43900360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed95a2e288305ac9a5ee0b1304879d303c79a89218e426ba8374f1ff1087ffd`  
		Last Modified: Thu, 21 Apr 2022 11:31:59 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4-bullseye` - linux; arm variant v5

```console
$ docker pull redmine@sha256:e401a9e32adfc198a581cd1d7ab1d44134885db987201d79c79637c38af368fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206400147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb7cfae6edd4b4097b4007984dbe16e015cd0c2537da014d27720879476e3628`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:50:37 GMT
ADD file:6b9a30e6ef50a46e87cf9d7f5a491c7951fdb6dd6fab3c9d4a9c3c40f92b8db4 in / 
# Tue, 29 Mar 2022 00:50:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 23:44:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 23:44:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 29 Mar 2022 23:44:22 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 00:24:24 GMT
ENV RUBY_MAJOR=2.7
# Tue, 12 Apr 2022 19:34:33 GMT
ENV RUBY_VERSION=2.7.6
# Tue, 12 Apr 2022 19:34:33 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Tue, 12 Apr 2022 19:38:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Apr 2022 19:38:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Apr 2022 19:38:49 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Apr 2022 19:38:49 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Apr 2022 19:38:51 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Apr 2022 19:38:51 GMT
CMD ["irb"]
# Tue, 12 Apr 2022 20:41:35 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 12 Apr 2022 20:43:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Apr 2022 20:43:18 GMT
ENV RAILS_ENV=production
# Tue, 12 Apr 2022 20:43:20 GMT
WORKDIR /usr/src/redmine
# Tue, 12 Apr 2022 20:43:21 GMT
ENV HOME=/home/redmine
# Tue, 12 Apr 2022 20:43:24 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 12 Apr 2022 20:43:25 GMT
ENV REDMINE_VERSION=4.2.5
# Tue, 12 Apr 2022 20:43:26 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.5.tar.gz
# Tue, 12 Apr 2022 20:43:26 GMT
ENV REDMINE_DOWNLOAD_SHA256=d97084b0eaad7266056814a0c0aec2737f4d23b8f67ce90c01a79b2eb5605984
# Tue, 12 Apr 2022 20:43:35 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 12 Apr 2022 20:49:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Apr 2022 20:49:24 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 12 Apr 2022 20:49:24 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 12 Apr 2022 20:49:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 20:49:25 GMT
EXPOSE 3000
# Tue, 12 Apr 2022 20:49:26 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9a41aba0a099ec129c20f41f6370b97daa4c3d4d3edc76ea1863bc5f76f9e5e5`  
		Last Modified: Tue, 29 Mar 2022 01:05:21 GMT  
		Size: 28.9 MB (28920513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf44c7251b2b648f973f028009b225f6c08537764f423748cb086f75716c797`  
		Last Modified: Wed, 30 Mar 2022 01:01:08 GMT  
		Size: 8.6 MB (8633465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab9a3a54418b6eafc72c90d31b5f425c60b3b5f13be1f1407c1c9f1619eb964`  
		Last Modified: Wed, 30 Mar 2022 01:01:01 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408d666684811dce9f8d6ba2644d319bd9974b0730d9aeaec5cdc85bf24f2220`  
		Last Modified: Tue, 12 Apr 2022 20:16:34 GMT  
		Size: 13.9 MB (13912654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac7e1762f586074b9bc541d1432f6487c7b3b67e326413989710b6650948c5a`  
		Last Modified: Tue, 12 Apr 2022 20:16:27 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c169e11292d61e7f6706ee9847a638355279caf4fd9c115c4f9528f8fb3d5996`  
		Last Modified: Tue, 12 Apr 2022 20:58:43 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e869a297c88e66472b0566323a91ea0611d985b662bff2c825e19a4ecfb8508`  
		Last Modified: Tue, 12 Apr 2022 20:59:28 GMT  
		Size: 97.0 MB (96958379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ab61d73e37c973134229edc39cd98da837985d233994a0f136894abb049f73`  
		Last Modified: Tue, 12 Apr 2022 20:58:42 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba63231e057e6b050adc369553f7ce1507dffb3d6dc8fef1a730ed79cdf7729a`  
		Last Modified: Tue, 12 Apr 2022 20:58:42 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c19e7f2967737ae740f9664254b025fa4b725a146c190659ab8b1a46e63e25`  
		Last Modified: Tue, 12 Apr 2022 20:58:44 GMT  
		Size: 3.1 MB (3064889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d144ff52f74e4245cf13666a0fa0987dab55992addf434bd228e5a2217641c53`  
		Last Modified: Tue, 12 Apr 2022 20:59:00 GMT  
		Size: 54.9 MB (54906013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669728ef94432a156577a0462e519a62d2acfee55685944c217a4feac243ee75`  
		Last Modified: Tue, 12 Apr 2022 20:58:42 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4-bullseye` - linux; arm variant v7

```console
$ docker pull redmine@sha256:d7b70940893eb398f962c0a4164635eb9d9e9f1fa2b27c3d731f41bcf4b336f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.4 MB (199385512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c6f4e463e97be5e1fe6f5d199dcf3ed8597d8afb17ae07eff864d33c6ef366`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 02:18:34 GMT
ADD file:e1835d1a0c70a0335757f211893e5d12ddf797e489e10434c0982bdf9b234f67 in / 
# Tue, 29 Mar 2022 02:18:36 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 15:07:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 15:07:38 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 30 Mar 2022 15:07:38 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 15:46:36 GMT
ENV RUBY_MAJOR=2.7
# Tue, 12 Apr 2022 19:59:34 GMT
ENV RUBY_VERSION=2.7.6
# Tue, 12 Apr 2022 19:59:34 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Tue, 12 Apr 2022 20:03:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Apr 2022 20:03:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Apr 2022 20:03:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Apr 2022 20:03:39 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Apr 2022 20:03:40 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Apr 2022 20:03:41 GMT
CMD ["irb"]
# Wed, 13 Apr 2022 02:46:18 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 13 Apr 2022 02:47:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Apr 2022 02:47:28 GMT
ENV RAILS_ENV=production
# Wed, 13 Apr 2022 02:47:29 GMT
WORKDIR /usr/src/redmine
# Wed, 13 Apr 2022 02:47:29 GMT
ENV HOME=/home/redmine
# Wed, 13 Apr 2022 02:47:31 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 13 Apr 2022 02:47:31 GMT
ENV REDMINE_VERSION=4.2.5
# Wed, 13 Apr 2022 02:47:31 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.5.tar.gz
# Wed, 13 Apr 2022 02:47:32 GMT
ENV REDMINE_DOWNLOAD_SHA256=d97084b0eaad7266056814a0c0aec2737f4d23b8f67ce90c01a79b2eb5605984
# Wed, 13 Apr 2022 02:47:38 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 13 Apr 2022 02:52:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 13 Apr 2022 02:53:00 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 13 Apr 2022 02:53:00 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 13 Apr 2022 02:53:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Apr 2022 02:53:01 GMT
EXPOSE 3000
# Wed, 13 Apr 2022 02:53:02 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f98812e1a494a683a5b3dea593dd2ef305f5f732193044c147f22e44b00164bc`  
		Last Modified: Tue, 29 Mar 2022 02:34:13 GMT  
		Size: 26.6 MB (26575370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f688115dbd56a1fea4d640c931a8c2458750d03deb3a447bc7117990adf76eb5`  
		Last Modified: Wed, 30 Mar 2022 16:27:08 GMT  
		Size: 8.1 MB (8143596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c61f3a636f525c0fd50a0f7a8613b3d9ab7e850dcd61dfe7b3ff478e64d614`  
		Last Modified: Wed, 30 Mar 2022 16:27:01 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33fa850a2fc913bdc17876d006d9e90b86e16a370a229bb537864982e31c6d3a`  
		Last Modified: Tue, 12 Apr 2022 21:02:40 GMT  
		Size: 13.8 MB (13784716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9892a607e1aee3b76436dbef0cf9e903f62f0f7f18a0c3d3aebf546572e8a72e`  
		Last Modified: Tue, 12 Apr 2022 21:02:36 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ff27453d0692be110c16cf268a248e530dc750678ace8ba4749b2738795900`  
		Last Modified: Wed, 13 Apr 2022 03:17:24 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c84cb61d5a19da7f23600c21f0f792fe3d4f27f505a3cbb4d366e1ba6ad6c9`  
		Last Modified: Wed, 13 Apr 2022 03:18:25 GMT  
		Size: 93.1 MB (93107495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf9214862edd5b546515de34a711d1f6f6949f935387df2e1fdf7ad744ee743`  
		Last Modified: Wed, 13 Apr 2022 03:17:23 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ead86d17f4977b0c5a3fe047854cd08c7a3bb79350e7073befdac1073c58a6a`  
		Last Modified: Wed, 13 Apr 2022 03:17:22 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f362f470443533e024a2b2e682c0526d14a8d6f7202e57c654805816872425`  
		Last Modified: Wed, 13 Apr 2022 03:17:26 GMT  
		Size: 3.1 MB (3064892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a21d496647e1a455b0eb62652a8b0e83bad8527928fe5f3d247f860a8ced9dc`  
		Last Modified: Wed, 13 Apr 2022 03:17:46 GMT  
		Size: 54.7 MB (54705209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56afc89101046d83a1c2c31f8c7c36c3eb4b9658e2b5aadd4558e71f103dd3c6`  
		Last Modified: Wed, 13 Apr 2022 03:17:22 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4-bullseye` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:aef6210e04189cc56919a65ca7f67e2a447f7dce46fac1e3961a79b25e962ee1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.6 MB (211552548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8b9d1b68e6db727c272865cba43f664730fbae9541f8bd7a4f71aaf8007946`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:10 GMT
ADD file:84523b5820128293b713ef35d8db618921162250da1e4c72bf9923f34ad7d87d in / 
# Wed, 20 Apr 2022 04:29:11 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:24:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:24:12 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 20 Apr 2022 12:24:13 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 12:51:15 GMT
ENV RUBY_MAJOR=2.7
# Wed, 20 Apr 2022 12:51:15 GMT
ENV RUBY_VERSION=2.7.6
# Wed, 20 Apr 2022 12:51:16 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Wed, 20 Apr 2022 12:52:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 20 Apr 2022 12:52:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Apr 2022 12:52:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Apr 2022 12:53:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 12:53:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 20 Apr 2022 12:53:02 GMT
CMD ["irb"]
# Thu, 21 Apr 2022 10:36:06 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 21 Apr 2022 10:36:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Apr 2022 10:36:30 GMT
ENV RAILS_ENV=production
# Thu, 21 Apr 2022 10:36:30 GMT
WORKDIR /usr/src/redmine
# Thu, 21 Apr 2022 10:36:31 GMT
ENV HOME=/home/redmine
# Thu, 21 Apr 2022 10:36:33 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 21 Apr 2022 10:36:33 GMT
ENV REDMINE_VERSION=4.2.5
# Thu, 21 Apr 2022 10:36:34 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.5.tar.gz
# Thu, 21 Apr 2022 10:36:35 GMT
ENV REDMINE_DOWNLOAD_SHA256=d97084b0eaad7266056814a0c0aec2737f4d23b8f67ce90c01a79b2eb5605984
# Thu, 21 Apr 2022 10:36:39 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 21 Apr 2022 10:38:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 21 Apr 2022 10:38:34 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 21 Apr 2022 10:38:35 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 21 Apr 2022 10:38:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 21 Apr 2022 10:38:37 GMT
EXPOSE 3000
# Thu, 21 Apr 2022 10:38:38 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6d4a449ac69c579312443ded09f57c4894e7adb42f7406abd364f95982fafc59`  
		Last Modified: Wed, 20 Apr 2022 04:35:49 GMT  
		Size: 30.1 MB (30065801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5734698a68763af3eeed89465d52db65ca4efa009350fc647c54ffd1ed5a7fc3`  
		Last Modified: Wed, 20 Apr 2022 13:08:55 GMT  
		Size: 9.0 MB (9035208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b82eb8113ebf269b934093aaa14f76aaa065c7d1625dbc771b86c98db78224`  
		Last Modified: Wed, 20 Apr 2022 13:08:54 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f860af7eca1efb5e70e0a7b664858a2538e5ae46fa0dac1e5261e671574a945`  
		Last Modified: Wed, 20 Apr 2022 13:13:20 GMT  
		Size: 14.2 MB (14180790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca758e0d5ee8edab9efdd9cf251a507a1cf213d587db94b0d9d1066d2bdae8de`  
		Last Modified: Wed, 20 Apr 2022 13:13:18 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f7f7ac23d1148b1f3efe9bbe224fb3491f82ab9851bd292ace9c183d2958a7`  
		Last Modified: Thu, 21 Apr 2022 10:43:39 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31ccf88156d9f329bff026570c6ab66422c7cd0ab806662fd793febde481796`  
		Last Modified: Thu, 21 Apr 2022 10:43:55 GMT  
		Size: 99.8 MB (99761846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9127b1af70ff13d643d5dc1b1c4ec2518fe81722cb67b2dc9d5ed4405653084`  
		Last Modified: Thu, 21 Apr 2022 10:43:37 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d5f2437653ec540a7f825e31488d0f16322ac99524f46fb938388bf955fb59`  
		Last Modified: Thu, 21 Apr 2022 10:43:37 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e73c3b143d4a989c4bf865d070fa7ffaaf329994e8e1f03e66a92bcbb8f06cb`  
		Last Modified: Thu, 21 Apr 2022 10:43:38 GMT  
		Size: 3.1 MB (3065098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8eeed99db06f8ca00baa7bfdc90097064657a04e110f9b21c637402b976e894`  
		Last Modified: Thu, 21 Apr 2022 10:43:43 GMT  
		Size: 55.4 MB (55439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30ea1715cdfcdd885deff01287ccbe9318231f8576ecc058d35e2423a97c217`  
		Last Modified: Thu, 21 Apr 2022 10:43:38 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4-bullseye` - linux; 386

```console
$ docker pull redmine@sha256:2e9828ea7b540e3748be4094eec674a0c0707662a5cb3ac3af1024842be034b2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.1 MB (208081250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c6edf894d31f0ec2de78ec5122d74da912a01e0cc02ac87164259b01beee09`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 20 Apr 2022 07:37:35 GMT
ADD file:460761e2baaea91893a907ce122ff7d585ef5704f48c03454835986028a1d842 in / 
# Wed, 20 Apr 2022 07:37:35 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 16:24:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 16:24:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 20 Apr 2022 16:24:22 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 16:52:10 GMT
ENV RUBY_MAJOR=2.7
# Wed, 20 Apr 2022 16:52:11 GMT
ENV RUBY_VERSION=2.7.6
# Wed, 20 Apr 2022 16:52:12 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Wed, 20 Apr 2022 16:53:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 20 Apr 2022 16:53:56 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Apr 2022 16:53:57 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Apr 2022 16:53:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 16:53:59 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 20 Apr 2022 16:54:00 GMT
CMD ["irb"]
# Thu, 21 Apr 2022 01:43:08 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 21 Apr 2022 01:43:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Apr 2022 01:43:36 GMT
ENV RAILS_ENV=production
# Thu, 21 Apr 2022 01:43:36 GMT
WORKDIR /usr/src/redmine
# Thu, 21 Apr 2022 01:43:37 GMT
ENV HOME=/home/redmine
# Thu, 21 Apr 2022 01:43:38 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 21 Apr 2022 01:43:39 GMT
ENV REDMINE_VERSION=4.2.5
# Thu, 21 Apr 2022 01:43:40 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.5.tar.gz
# Thu, 21 Apr 2022 01:43:41 GMT
ENV REDMINE_DOWNLOAD_SHA256=d97084b0eaad7266056814a0c0aec2737f4d23b8f67ce90c01a79b2eb5605984
# Thu, 21 Apr 2022 01:43:45 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 21 Apr 2022 01:44:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 21 Apr 2022 01:44:29 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 21 Apr 2022 01:44:30 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 21 Apr 2022 01:44:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 21 Apr 2022 01:44:31 GMT
EXPOSE 3000
# Thu, 21 Apr 2022 01:44:32 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6e5c4eb151e267d273883db6e9aee3ff01be07e098ca33f0d1d65bb0e0416921`  
		Last Modified: Wed, 20 Apr 2022 07:44:54 GMT  
		Size: 32.4 MB (32389597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e787f8b5e599f4a476d61f4260ccf2e39d4b111e522c09a568d001e39609c57`  
		Last Modified: Wed, 20 Apr 2022 17:10:25 GMT  
		Size: 11.8 MB (11788338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9380efea8e48159ea8d3c83f8e49e563c8435940c2a8e956ba9c5bc548228d`  
		Last Modified: Wed, 20 Apr 2022 17:10:23 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ac1b66a57cca31239b561b495b9207755cbed66e96fe569456f517339e013b`  
		Last Modified: Wed, 20 Apr 2022 17:15:22 GMT  
		Size: 13.7 MB (13671123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1da3f09831e9726925ab290063179cdcab9d6fcf99ccd433e9a379a378ba8e3`  
		Last Modified: Wed, 20 Apr 2022 17:15:20 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0955e6e5f9c9df478361aa024cf219fbce47191ed90688c9463399205c877b`  
		Last Modified: Thu, 21 Apr 2022 01:48:53 GMT  
		Size: 1.6 KB (1615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e06d2a18669f6fc89ef838827d7f80287f3e6a63f3b412842abdf92372d6bbb`  
		Last Modified: Thu, 21 Apr 2022 01:49:08 GMT  
		Size: 103.3 MB (103322332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839dc2a4ef4acefc557005075f675efe4a08665667254cc4e7c975b265a1aed2`  
		Last Modified: Thu, 21 Apr 2022 01:48:50 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce550e7ab0172ceb6202688436fc6d1a6821da44d42c0f6a6574d9b5ea70226a`  
		Last Modified: Thu, 21 Apr 2022 01:48:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf1d5c12fe02601476335de50fc399d0758e81ca3994e344bf4cb9e181e099b`  
		Last Modified: Thu, 21 Apr 2022 01:48:51 GMT  
		Size: 3.1 MB (3065099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243ddd9a889978839384c66b65787bd115f4d3c5032e9a33216d1c91f2f1b3b4`  
		Last Modified: Thu, 21 Apr 2022 01:48:57 GMT  
		Size: 43.8 MB (43840741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84bf26f5b5b3623f9f88c99f54edc161acf250d17f60d550d3a8bb046cac708f`  
		Last Modified: Thu, 21 Apr 2022 01:48:50 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4-bullseye` - linux; ppc64le

```console
$ docker pull redmine@sha256:3e2e4b1e8681adb7237426d68edfc1f1e7532e4f418fe66986e7671a38cfd00a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.1 MB (228072652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f78ae8ba5fb635fe36b5d51b2105fdb8a611acb25de3c563e1cedd4b3673c4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:08 GMT
ADD file:e7ae113c10f322a9cffc46b62ba12820e270caaadaee3c5b907c801a37e1632c in / 
# Tue, 29 Mar 2022 00:22:11 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 20:15:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 20:15:40 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 29 Mar 2022 20:15:42 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 20:58:30 GMT
ENV RUBY_MAJOR=2.7
# Tue, 12 Apr 2022 20:12:29 GMT
ENV RUBY_VERSION=2.7.6
# Tue, 12 Apr 2022 20:12:31 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Tue, 12 Apr 2022 20:20:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Apr 2022 20:20:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Apr 2022 20:20:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Apr 2022 20:20:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Apr 2022 20:20:27 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Apr 2022 20:20:30 GMT
CMD ["irb"]
# Wed, 13 Apr 2022 01:24:44 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 13 Apr 2022 01:27:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Apr 2022 01:27:45 GMT
ENV RAILS_ENV=production
# Wed, 13 Apr 2022 01:27:49 GMT
WORKDIR /usr/src/redmine
# Wed, 13 Apr 2022 01:27:51 GMT
ENV HOME=/home/redmine
# Wed, 13 Apr 2022 01:27:55 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 13 Apr 2022 01:27:57 GMT
ENV REDMINE_VERSION=4.2.5
# Wed, 13 Apr 2022 01:27:59 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.5.tar.gz
# Wed, 13 Apr 2022 01:28:02 GMT
ENV REDMINE_DOWNLOAD_SHA256=d97084b0eaad7266056814a0c0aec2737f4d23b8f67ce90c01a79b2eb5605984
# Wed, 13 Apr 2022 01:28:09 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 13 Apr 2022 01:32:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 13 Apr 2022 01:32:43 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 13 Apr 2022 01:32:44 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 13 Apr 2022 01:32:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Apr 2022 01:32:49 GMT
EXPOSE 3000
# Wed, 13 Apr 2022 01:32:51 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ecc74bb8af5a048e1123af0e17d88ef3da1d10951ada79e8e1cc9c0a694245d3`  
		Last Modified: Tue, 29 Mar 2022 00:32:57 GMT  
		Size: 35.3 MB (35282506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f562a86188fb99fc4a0a625ba1095e72199d3ed24a320c53438ff2f86ff81d5`  
		Last Modified: Tue, 29 Mar 2022 21:50:59 GMT  
		Size: 10.5 MB (10476023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33bf06fdc797244697941f6f490e54db503199df283939fa0e50eba6c623bdc`  
		Last Modified: Tue, 29 Mar 2022 21:50:56 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0ca00880867b143bb071f94763e492839348ff5e13a7fa66fd02ed9bfafd49`  
		Last Modified: Tue, 12 Apr 2022 21:20:36 GMT  
		Size: 15.1 MB (15053209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a88f2184715f75a0e74cb1c91f4719d29c3f6a63c912a523a4fd41c6ef19c0`  
		Last Modified: Tue, 12 Apr 2022 21:20:33 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0270be0c415e5b8dc924f171ac38420f044e0c221db6112ecf2805a47be5564`  
		Last Modified: Wed, 13 Apr 2022 01:56:58 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:630f1b631ccb239a9469fc8d337ffb86896c5ef1463948a99d736a32c8316967`  
		Last Modified: Wed, 13 Apr 2022 01:57:18 GMT  
		Size: 107.5 MB (107488780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e2f2cc3233172cf851f8f5c18e493ee658fe4773653f17ab0619f6c16f4a67`  
		Last Modified: Wed, 13 Apr 2022 01:56:55 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9daaea0418a1046e37567bce5c7de35f597f5a293396b44a991989aca0e26f`  
		Last Modified: Wed, 13 Apr 2022 01:56:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f71e1f24cf0cd9ec54e6abcf2e8aa9792b7989fe1f53e3288f76f7e2067bd8`  
		Last Modified: Wed, 13 Apr 2022 01:56:56 GMT  
		Size: 3.1 MB (3064889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879d73f539a7d671dbcc07349cbad92854ada173a9f141e5eedbce5fee601918`  
		Last Modified: Wed, 13 Apr 2022 01:57:03 GMT  
		Size: 56.7 MB (56702992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c0dc5b9acc04c640e12ee377255e2771b09a26af747f49bc97107335771cb9`  
		Last Modified: Wed, 13 Apr 2022 01:56:55 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4-bullseye` - linux; s390x

```console
$ docker pull redmine@sha256:60425a3a9628e0596b0d03cdd6e437a0e4d8cdc274126db4ede770cf12cb197b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.4 MB (211368215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56d2fb4e19c016136321e39f8a5a870811752af03731dd7411cacb0705bf2ec9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 20 Apr 2022 08:39:37 GMT
ADD file:c3381330644d6d9fc585301395580b564cdf7c880fb2dc2d8e48992673184f7d in / 
# Wed, 20 Apr 2022 08:39:42 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 18:13:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 18:13:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 20 Apr 2022 18:13:12 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 18:53:55 GMT
ENV RUBY_MAJOR=2.7
# Wed, 20 Apr 2022 18:53:56 GMT
ENV RUBY_VERSION=2.7.6
# Wed, 20 Apr 2022 18:53:56 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Wed, 20 Apr 2022 18:57:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 20 Apr 2022 18:57:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Apr 2022 18:57:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Apr 2022 18:57:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 18:57:08 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 20 Apr 2022 18:57:09 GMT
CMD ["irb"]
# Thu, 21 Apr 2022 13:11:44 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 21 Apr 2022 13:12:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Apr 2022 13:12:15 GMT
ENV RAILS_ENV=production
# Thu, 21 Apr 2022 13:12:15 GMT
WORKDIR /usr/src/redmine
# Thu, 21 Apr 2022 13:12:15 GMT
ENV HOME=/home/redmine
# Thu, 21 Apr 2022 13:12:16 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 21 Apr 2022 13:12:16 GMT
ENV REDMINE_VERSION=4.2.5
# Thu, 21 Apr 2022 13:12:16 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.5.tar.gz
# Thu, 21 Apr 2022 13:12:16 GMT
ENV REDMINE_DOWNLOAD_SHA256=d97084b0eaad7266056814a0c0aec2737f4d23b8f67ce90c01a79b2eb5605984
# Thu, 21 Apr 2022 13:12:18 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 21 Apr 2022 13:13:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 21 Apr 2022 13:13:56 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 21 Apr 2022 13:13:56 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 21 Apr 2022 13:13:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 21 Apr 2022 13:13:56 GMT
EXPOSE 3000
# Thu, 21 Apr 2022 13:13:57 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3179e1eccb473ae22a70e8ac3e9ddb4660ebdfd977989d115bd4d322ecc12b89`  
		Last Modified: Wed, 20 Apr 2022 08:49:39 GMT  
		Size: 29.7 MB (29654805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3acae14916685d615d38c492277fcf961a43a1a66c11a325cde3a083984a2a`  
		Last Modified: Wed, 20 Apr 2022 19:21:05 GMT  
		Size: 8.9 MB (8860501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f463734a145aa6e47b22ef2abd3a4a6d4161f2d0d69a6e11ca34ea6eba02268`  
		Last Modified: Wed, 20 Apr 2022 19:21:03 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd061d15827da8bc6b40f2003e6d1b9a4348ec31a3af8a7387f1cbb2a550dab`  
		Last Modified: Wed, 20 Apr 2022 19:24:47 GMT  
		Size: 14.7 MB (14667111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb72ae416bde45b7d9c812144ff7b64cccf214f4b19a5113741d9aaf44d540ef`  
		Last Modified: Wed, 20 Apr 2022 19:24:45 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51788b726adf273267e2f10a89e8625fe588375a593fec4130d4b5d42de01bbd`  
		Last Modified: Thu, 21 Apr 2022 13:19:11 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:357bdf07c4f0d36bf591d3aa9327773947c1eed5495f98257214b92dc4ad4a71`  
		Last Modified: Thu, 21 Apr 2022 13:19:26 GMT  
		Size: 99.1 MB (99127979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b58574d56c5282be2feb74604818cd18bab1a867af2d74fef88f94dc42a43c`  
		Last Modified: Thu, 21 Apr 2022 13:19:09 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f411d956fc5d9bb744b7564a7a886f4ab354cd214224ca27af9a091823fcb8d`  
		Last Modified: Thu, 21 Apr 2022 13:19:09 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7656b032e53e56d1c6282f2e758e590897e34a0764582fed999271e1cfb3c6`  
		Last Modified: Thu, 21 Apr 2022 13:19:11 GMT  
		Size: 3.1 MB (3064898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13cc89adda6d81fb626bf83c3b4a0fbc025387ab0ad7ee5019fe23c27f811d3c`  
		Last Modified: Thu, 21 Apr 2022 13:19:14 GMT  
		Size: 56.0 MB (55988673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29c5af927877a5bc36fd690c4eec1c3f0ea6df29e920ab59f93bc8f92981a12`  
		Last Modified: Thu, 21 Apr 2022 13:19:10 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
