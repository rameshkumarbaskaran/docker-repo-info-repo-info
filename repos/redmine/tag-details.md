<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `redmine`

-	[`redmine:4`](#redmine4)
-	[`redmine:4-alpine`](#redmine4-alpine)
-	[`redmine:4-passenger`](#redmine4-passenger)
-	[`redmine:4.0`](#redmine40)
-	[`redmine:4.0-alpine`](#redmine40-alpine)
-	[`redmine:4.0-passenger`](#redmine40-passenger)
-	[`redmine:4.0.9`](#redmine409)
-	[`redmine:4.0.9-alpine`](#redmine409-alpine)
-	[`redmine:4.0.9-passenger`](#redmine409-passenger)
-	[`redmine:4.1`](#redmine41)
-	[`redmine:4.1-alpine`](#redmine41-alpine)
-	[`redmine:4.1-passenger`](#redmine41-passenger)
-	[`redmine:4.1.5`](#redmine415)
-	[`redmine:4.1.5-alpine`](#redmine415-alpine)
-	[`redmine:4.1.5-passenger`](#redmine415-passenger)
-	[`redmine:4.2`](#redmine42)
-	[`redmine:4.2-alpine`](#redmine42-alpine)
-	[`redmine:4.2-passenger`](#redmine42-passenger)
-	[`redmine:4.2.3`](#redmine423)
-	[`redmine:4.2.3-alpine`](#redmine423-alpine)
-	[`redmine:4.2.3-passenger`](#redmine423-passenger)
-	[`redmine:alpine`](#redminealpine)
-	[`redmine:latest`](#redminelatest)
-	[`redmine:passenger`](#redminepassenger)

## `redmine:4`

```console
$ docker pull redmine@sha256:69caaf47721ed583465333ca9cbef1e39a54cfb0ca911c9eb5a65aa8b5ab698d
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

### `redmine:4` - linux; amd64

```console
$ docker pull redmine@sha256:23da6bbd8146ba5ebc6c565af6a4941d0a836fb5f2b3cf8281d954a84047c675
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195500650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777ff92e6fdbdb00a6ebcf1c2df29c52c4cbb171e418bcee49451b9df8ddf3b2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:20:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:20:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 15:20:38 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 15:27:24 GMT
ENV RUBY_MAJOR=2.7
# Tue, 12 Oct 2021 15:27:25 GMT
ENV RUBY_VERSION=2.7.4
# Tue, 12 Oct 2021 15:27:25 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Tue, 12 Oct 2021 15:30:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 15:30:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 15:30:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 15:30:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 15:30:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 15:30:34 GMT
CMD ["irb"]
# Tue, 12 Oct 2021 20:17:43 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 12 Oct 2021 20:18:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 20:18:13 GMT
ENV RAILS_ENV=production
# Tue, 12 Oct 2021 20:18:13 GMT
WORKDIR /usr/src/redmine
# Tue, 12 Oct 2021 20:18:14 GMT
ENV HOME=/home/redmine
# Tue, 12 Oct 2021 20:18:14 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 12 Oct 2021 20:18:15 GMT
ENV REDMINE_VERSION=4.2.3
# Tue, 12 Oct 2021 20:18:15 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Tue, 12 Oct 2021 20:18:19 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 12 Oct 2021 20:19:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Oct 2021 20:19:20 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 12 Oct 2021 20:19:20 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 12 Oct 2021 20:19:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 20:19:21 GMT
EXPOSE 3000
# Tue, 12 Oct 2021 20:19:21 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee6af487f217efc8e231b9857a8031fdf07ab0c8b30e539497893ec5287578b`  
		Last Modified: Tue, 12 Oct 2021 15:39:48 GMT  
		Size: 12.6 MB (12565186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48bb8449b0384f7addf4ec5d88d8ef088e25ca52f9299c1fca4bff3f5b2411d`  
		Last Modified: Tue, 12 Oct 2021 15:39:46 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4280126bdef2ed0df50609c224de8bcb7486f4ce6959104e588d7b147eb14f`  
		Last Modified: Tue, 12 Oct 2021 15:40:36 GMT  
		Size: 14.5 MB (14510184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4cc9067aac92ce406573f770322af2801a273925a95583e61e3ce6b568851a`  
		Last Modified: Tue, 12 Oct 2021 15:40:33 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf24873f395941528bd53ff8223d6b7799153cf8145e3b7158e496a8a4b9def`  
		Last Modified: Tue, 12 Oct 2021 20:27:17 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3deebb307eea15c0af224fa48dfa44ef5eb083d662d56e4eb24d97d503a2bb3f`  
		Last Modified: Tue, 12 Oct 2021 20:27:32 GMT  
		Size: 94.1 MB (94088542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799adc6ff62bdab4f48789fde71c3a76c4c1afa0e5288f175f5092a2e5867657`  
		Last Modified: Tue, 12 Oct 2021 20:27:14 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd34b5a0c4380ebac887ae883212d7ed6aa5e5fafbcfc5611ef03b072a3d34d`  
		Last Modified: Tue, 12 Oct 2021 20:27:15 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b355bfb624ca195d5b52d9a3257d514eff56e8b581bfd705949d266e7e1cad4`  
		Last Modified: Tue, 12 Oct 2021 20:27:15 GMT  
		Size: 3.1 MB (3063247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a87ccde718061b2b0d26691dacf79a140cd1b32f380e6c6d3a8f397be5156d44`  
		Last Modified: Tue, 12 Oct 2021 20:27:20 GMT  
		Size: 44.1 MB (44129736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e79252e1149fadd0907e406c69bd8e989028da830f9a410edb32ca9887a7d6`  
		Last Modified: Tue, 12 Oct 2021 20:27:15 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4` - linux; arm variant v5

```console
$ docker pull redmine@sha256:08f124ad97cbf3d78e62b390897fbd0a6e47f4901f4ce4f632d68de47d1236c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.0 MB (196991904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750dc7fdc53efaea0a675c5102c8cc3d6c8e5fb47e2bb056eae33416edf86f72`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 12 Oct 2021 00:51:32 GMT
ADD file:0d95eee31ffe3f4260263e4fac2a61123a4b98d2e7a67efcc7bfea338c54f41d in / 
# Tue, 12 Oct 2021 00:51:32 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 06:45:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 06:45:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 06:45:07 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 07:03:17 GMT
ENV RUBY_MAJOR=2.7
# Tue, 12 Oct 2021 07:03:17 GMT
ENV RUBY_VERSION=2.7.4
# Tue, 12 Oct 2021 07:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Tue, 12 Oct 2021 07:07:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 07:07:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 07:07:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 07:07:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 07:07:39 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 07:07:39 GMT
CMD ["irb"]
# Wed, 13 Oct 2021 03:05:01 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 13 Oct 2021 03:06:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 03:06:17 GMT
ENV RAILS_ENV=production
# Wed, 13 Oct 2021 03:06:19 GMT
WORKDIR /usr/src/redmine
# Wed, 13 Oct 2021 03:06:20 GMT
ENV HOME=/home/redmine
# Wed, 13 Oct 2021 03:06:23 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 13 Oct 2021 03:06:24 GMT
ENV REDMINE_VERSION=4.2.3
# Wed, 13 Oct 2021 03:06:25 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Wed, 13 Oct 2021 03:06:34 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 13 Oct 2021 03:13:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 13 Oct 2021 03:13:17 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 13 Oct 2021 03:13:19 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 13 Oct 2021 03:13:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Oct 2021 03:13:22 GMT
EXPOSE 3000
# Wed, 13 Oct 2021 03:13:23 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:175b083b22fb061f7d1894fe4916a2967ce636d47376da526d90d57c8f7efc60`  
		Last Modified: Tue, 12 Oct 2021 01:07:45 GMT  
		Size: 24.9 MB (24872704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed73113a2340f22427741647a89a1911c6dd067bde17833928c5d210ab93918`  
		Last Modified: Tue, 12 Oct 2021 07:31:54 GMT  
		Size: 10.3 MB (10349314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7a78f939d570718e0af30429b3118d94e3800937a469b3fca591fda6d0540e`  
		Last Modified: Tue, 12 Oct 2021 07:31:46 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854afe8d48105a800902d829046a9890cab76441d450aa59877c28405734daed`  
		Last Modified: Tue, 12 Oct 2021 07:33:59 GMT  
		Size: 13.9 MB (13871429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc97d908af060f6e00c4e7a607087a50b553e21e08c6a8c70274a3d81ea0b3ef`  
		Last Modified: Tue, 12 Oct 2021 07:33:51 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a08bb1308b5863e00403e1a34c4cb2a9aafa57091f2d1faa4936463e4f8de79`  
		Last Modified: Wed, 13 Oct 2021 03:32:03 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b177e5e016cce70192ebf1277d5a21559c74cf5aa60e6bff5dfb31a9d5767e8`  
		Last Modified: Wed, 13 Oct 2021 03:32:45 GMT  
		Size: 89.6 MB (89577077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa429c867c2a22535e2c33e168d8de14f69c6f13124dc7494d06630528d03c43`  
		Last Modified: Wed, 13 Oct 2021 03:32:01 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168fe406bb1360b18d49546d4af05cccf7fb548d99e4f4663d83dab19f23f4be`  
		Last Modified: Wed, 13 Oct 2021 03:32:01 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec2ee921f4dfd9c1a73cfe3b44b39e67f1af385494dd03e3fe1cbdc9c31aaf1`  
		Last Modified: Wed, 13 Oct 2021 03:32:04 GMT  
		Size: 3.1 MB (3063249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7892b495be3664dd078f8510b6b3222fec0b0eeceaaa8fcc540d7ced595ecf23`  
		Last Modified: Wed, 13 Oct 2021 03:32:21 GMT  
		Size: 55.3 MB (55253893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea12a2e245bbbc4585eb36f1a1709b9035c2beaac9e1be72d14f2bf9c84118e`  
		Last Modified: Wed, 13 Oct 2021 03:32:01 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4` - linux; arm variant v7

```console
$ docker pull redmine@sha256:900b0cad4acc6dc28f8f9e3279e4a10121c4d247bd540f66d7ff40fcdf914200
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.1 MB (190138732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88b04a543401c43e354aa169b439ad085b11a2b6acbde3b9a6a36f4307bec08`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 12 Oct 2021 01:29:42 GMT
ADD file:fe1eaa1b1d760b3d250cb4ac331d26a261fc569f1694bd34e146f00874dc87e5 in / 
# Tue, 12 Oct 2021 01:29:43 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 02:56:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 02:56:30 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 03:06:47 GMT
ENV RUBY_MAJOR=2.7
# Tue, 12 Oct 2021 03:06:47 GMT
ENV RUBY_VERSION=2.7.4
# Tue, 12 Oct 2021 03:06:47 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Tue, 12 Oct 2021 03:10:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 03:10:54 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 03:10:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 03:10:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 03:10:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 03:10:57 GMT
CMD ["irb"]
# Wed, 13 Oct 2021 06:34:38 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 13 Oct 2021 06:35:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 06:35:44 GMT
ENV RAILS_ENV=production
# Wed, 13 Oct 2021 06:35:45 GMT
WORKDIR /usr/src/redmine
# Wed, 13 Oct 2021 06:35:46 GMT
ENV HOME=/home/redmine
# Wed, 13 Oct 2021 06:35:48 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 13 Oct 2021 06:35:48 GMT
ENV REDMINE_VERSION=4.2.3
# Wed, 13 Oct 2021 06:35:49 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Wed, 13 Oct 2021 06:35:55 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 13 Oct 2021 06:41:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 13 Oct 2021 06:41:11 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 13 Oct 2021 06:41:11 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 13 Oct 2021 06:41:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Oct 2021 06:41:12 GMT
EXPOSE 3000
# Wed, 13 Oct 2021 06:41:13 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c0b5ba470cac8cfdae4633f5cddb3ba9350fe1d1b1507c4965a8224eb40e52c5`  
		Last Modified: Tue, 12 Oct 2021 01:45:52 GMT  
		Size: 22.7 MB (22739698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cdd321094894b78bc0792d96cf339ee9e4ce7ec18a14ea44b32cfbc809867b`  
		Last Modified: Tue, 12 Oct 2021 03:40:20 GMT  
		Size: 9.9 MB (9872904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c0e1a382b6eb02d552bdb97946d22f8b0d9b5f787b5d1b491fa3703e23d5ea`  
		Last Modified: Tue, 12 Oct 2021 03:40:13 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ab36f90d94f50bb2f0b4be72799049691d9d0f05aadbe4e5cba89a3989efd1`  
		Last Modified: Tue, 12 Oct 2021 03:41:56 GMT  
		Size: 13.8 MB (13767235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a22941e2b0ce8584f2fa791a8370a30bd3a202fa73a1dd64d00a85bf075916a`  
		Last Modified: Tue, 12 Oct 2021 03:41:49 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6828dc1bb7b47f9d60169ee81885096702049306577ce953096d5057c12e91af`  
		Last Modified: Wed, 13 Oct 2021 06:55:56 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e9962d77928a7fea0f4dd24c838a24f72da3eba59ed75e59a3557633655398`  
		Last Modified: Wed, 13 Oct 2021 06:56:52 GMT  
		Size: 85.6 MB (85590281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894593e78f4567729a26e4302a660a56ee7289a18398fb9ec5b526be2466b739`  
		Last Modified: Wed, 13 Oct 2021 06:55:55 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f705a0b143059f649ff99fd7d343002386794bfe675456f393697b71d9dbc5`  
		Last Modified: Wed, 13 Oct 2021 06:55:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14825a50627a0f65eec1cc695fb3896ea4d8a22a09fc112bc902fcbbdd53be02`  
		Last Modified: Wed, 13 Oct 2021 06:56:03 GMT  
		Size: 3.1 MB (3063246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f461661b0c3351479c43855bab9a39d5482ee87a52376bc2898c48b83ce9ada1`  
		Last Modified: Wed, 13 Oct 2021 06:56:20 GMT  
		Size: 55.1 MB (55101134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b2c0757c967dd445d6615d9fa9fcaac7b289a198fbad58001af82cc9edbbc8`  
		Last Modified: Wed, 13 Oct 2021 06:55:55 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:86d444c24d077794c0c2cc949e49527863c9ca44e518c17e370b02eb4000216a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.1 MB (202113715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42218f16d6dac2e546b0a2281ab4659b776bbf51ec6e4acfbede94911bc9dcdd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:31:02 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:41:19 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 09:41:20 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 09:41:21 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 09:43:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 09:43:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 09:43:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 09:43:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:43:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 09:43:17 GMT
CMD ["irb"]
# Wed, 17 Nov 2021 19:46:13 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 17 Nov 2021 19:46:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 19:46:40 GMT
ENV RAILS_ENV=production
# Wed, 17 Nov 2021 19:46:41 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Nov 2021 19:46:42 GMT
ENV HOME=/home/redmine
# Wed, 17 Nov 2021 19:46:44 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 17 Nov 2021 19:46:44 GMT
ENV REDMINE_VERSION=4.2.3
# Wed, 17 Nov 2021 19:46:45 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Wed, 17 Nov 2021 19:46:50 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 17 Nov 2021 19:49:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 19:49:37 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Nov 2021 19:49:38 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 17 Nov 2021 19:49:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 19:49:40 GMT
EXPOSE 3000
# Wed, 17 Nov 2021 19:49:41 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8443a8ec909433d7156b8dcbeaf77f4e53d6a44b253a3f03b95126547154d55`  
		Last Modified: Wed, 17 Nov 2021 09:51:43 GMT  
		Size: 11.3 MB (11261808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f57122fa0ffe176f788d35a4a8f12a76819fa3bab198ac16e26d2961047a1d`  
		Last Modified: Wed, 17 Nov 2021 09:51:41 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e74dfb7a4c0fdaf06af6628a5256217d8dc0d66250a1fbc0c123f00b986e22`  
		Last Modified: Wed, 17 Nov 2021 09:53:40 GMT  
		Size: 14.1 MB (14143923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb526ffb8eba3317294cf51375a464a78d261132b6b7491f254cf7a4a156682`  
		Last Modified: Wed, 17 Nov 2021 09:53:38 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21518ac2e5bab0f6dfc5e5d56cc37c2ddfe56b2be0f94f479a28844eda6b01df`  
		Last Modified: Wed, 17 Nov 2021 19:56:25 GMT  
		Size: 1.6 KB (1626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76248d3153c26ceb5416c50118694725c0c7d4ce7823824bd66101dc2c5a010d`  
		Last Modified: Wed, 17 Nov 2021 19:56:41 GMT  
		Size: 92.6 MB (92614747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31701ff7128027b1906c22a7653245cdb3cfac2d03494df00e25be248e743991`  
		Last Modified: Wed, 17 Nov 2021 19:56:23 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac4b0eb26c86bcfc93c2657dfbeb8e1d3ef40e8785866c46e13be70741ec74b`  
		Last Modified: Wed, 17 Nov 2021 19:56:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62ad39d6bc57963dc25a1ff3af302f01bf0d29bf1d984b097d829bcef8e71d3`  
		Last Modified: Wed, 17 Nov 2021 19:56:24 GMT  
		Size: 3.1 MB (3063387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c77a0ff1cda155087e0a1fd87440c1fd1f0de88ddcd0f7b027500ca9b1c5df9`  
		Last Modified: Wed, 17 Nov 2021 19:56:31 GMT  
		Size: 55.1 MB (55102701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8abe9431487572557c36e17868ec1e44d823b725205b047bd9b29f8cb63fea74`  
		Last Modified: Wed, 17 Nov 2021 19:56:23 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4` - linux; 386

```console
$ docker pull redmine@sha256:541bbc59f1f2165794af255e943fd64e76f231e68941d6e893fb057442a80b34
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.4 MB (201449024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df8a65a7d03b8eef85a6b4790bedd723f2249542a83c9e248f86e8bfe4ab2be`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 18:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 18:38:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 18:38:25 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 18:58:22 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 18:58:22 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 18:58:23 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 19:02:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 19:02:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 19:02:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 19:02:50 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 19:02:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 19:02:53 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 00:36:05 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 00:36:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 00:36:42 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 00:36:42 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 00:36:42 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 00:36:43 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 00:36:43 GMT
ENV REDMINE_VERSION=4.2.3
# Thu, 18 Nov 2021 00:36:44 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Thu, 18 Nov 2021 00:36:48 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 00:37:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 00:37:43 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 00:37:43 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 00:37:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 00:37:44 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 00:37:44 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1742b7e5e1e5bca675e7f251c9f6fe8778a1bb1548e5b418f8547277f14e2e33`  
		Last Modified: Wed, 17 Nov 2021 19:17:19 GMT  
		Size: 17.2 MB (17227026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ef5459771b89c49219d5c15641c7215faf156712422f01efee40ad955a52c5`  
		Last Modified: Wed, 17 Nov 2021 19:17:10 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b59002f4fc409c3fdcbd829fcc8f9d9186a49f4b1977b2c959714978bd07c75`  
		Last Modified: Wed, 17 Nov 2021 19:19:42 GMT  
		Size: 14.0 MB (13992752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1a3cc73f29df585791125514b63252077c65f4a1e212d1021c4e3020df3dd8`  
		Last Modified: Wed, 17 Nov 2021 19:19:39 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cff4a558af0642405c8aec1556aebdbaf4c9a86c0632d964e532934f76466c`  
		Last Modified: Thu, 18 Nov 2021 00:43:12 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700278801433da9ce13b80f7e86e2e5368cccf0e303e9862c537a154f05a540a`  
		Last Modified: Thu, 18 Nov 2021 00:43:36 GMT  
		Size: 95.7 MB (95702657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af28efd287aeb351d175e3c0f5ed184fa551cd1af7172bb7791a60a0537af9de`  
		Last Modified: Thu, 18 Nov 2021 00:43:09 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b8937baf10e23d531e21069ea81323b01572eee4aed6f64640685bb7ffaab8`  
		Last Modified: Thu, 18 Nov 2021 00:43:09 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95eb84ecf78a6f2698456d871cbe794d0bb45a6cece674d3d8251894cb1c1a01`  
		Last Modified: Thu, 18 Nov 2021 00:43:11 GMT  
		Size: 3.1 MB (3063250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676ab58b071fabf24debb26ce72f971b94290b362f51e44b6a19c2fe9b3371a9`  
		Last Modified: Thu, 18 Nov 2021 00:43:18 GMT  
		Size: 43.7 MB (43654553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e940c5fbe3e6915f01902f8855bf33b917442025553bce6ff1b11353827a7b58`  
		Last Modified: Thu, 18 Nov 2021 00:43:09 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4` - linux; ppc64le

```console
$ docker pull redmine@sha256:a4c48b2c0bbb76d20734a3239c5ff4486fb06902d9161041f74716b4da26ab4f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219642463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b21372e7251d350b037972153cf0703df9289044566d5c57094d019c86f77787`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 12 Oct 2021 01:26:46 GMT
ADD file:5526880c6f19a4b4231a8b2bd7cfc625d116764c4918eff6f0b55f8c1eb38e1a in / 
# Tue, 12 Oct 2021 01:26:50 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 18:23:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 18:24:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 18:24:11 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 18:52:55 GMT
ENV RUBY_MAJOR=2.7
# Tue, 12 Oct 2021 18:53:00 GMT
ENV RUBY_VERSION=2.7.4
# Tue, 12 Oct 2021 18:53:05 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Tue, 12 Oct 2021 18:59:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 18:59:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 18:59:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 18:59:42 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 18:59:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 18:59:55 GMT
CMD ["irb"]
# Thu, 14 Oct 2021 00:42:47 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 14 Oct 2021 00:46:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 Oct 2021 00:46:53 GMT
ENV RAILS_ENV=production
# Thu, 14 Oct 2021 00:46:59 GMT
WORKDIR /usr/src/redmine
# Thu, 14 Oct 2021 00:47:04 GMT
ENV HOME=/home/redmine
# Thu, 14 Oct 2021 00:47:16 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 14 Oct 2021 00:47:21 GMT
ENV REDMINE_VERSION=4.2.3
# Thu, 14 Oct 2021 00:47:24 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Thu, 14 Oct 2021 00:47:47 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 14 Oct 2021 00:52:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 Oct 2021 00:52:57 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 14 Oct 2021 00:53:09 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 14 Oct 2021 00:53:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Oct 2021 00:53:25 GMT
EXPOSE 3000
# Thu, 14 Oct 2021 00:53:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d69973af32573c07c8789c0f9c144a5c0b822a1e85b59db3ce9f8ebc489ce85d`  
		Last Modified: Tue, 12 Oct 2021 01:38:40 GMT  
		Size: 30.5 MB (30547197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f48a596ad1fccd3e24dcc1f65e362937ced6f5b5ab61b6eb49e8eda8a55b85`  
		Last Modified: Tue, 12 Oct 2021 19:30:52 GMT  
		Size: 12.7 MB (12705483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd72e7e6250a90b152d1d27efca928b2c1bfc949dfe1b2e9cf089acde024c098`  
		Last Modified: Tue, 12 Oct 2021 19:30:49 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421cf7b60e6ecf3d6ad60b357e419014d8f6ad271c958a247f07c42e24664d11`  
		Last Modified: Tue, 12 Oct 2021 19:32:25 GMT  
		Size: 15.0 MB (14997040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06540a2f04ef35b100c723361f0086cb3542d114ee0eea90d820e05137d9c5dc`  
		Last Modified: Tue, 12 Oct 2021 19:32:22 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2718e7a16edeab031c20f2c31cd9a6f1421c88037a4dfcf8b59604f89539cd11`  
		Last Modified: Thu, 14 Oct 2021 01:20:37 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a889dd8c5dd31d494ac35831e782d265b2bfe457db83677f7c047312896493`  
		Last Modified: Thu, 14 Oct 2021 01:21:41 GMT  
		Size: 101.3 MB (101327529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca7ef034d38ef39e783753bbb082ce26ec6fdd002cf9a68ce51058795ad8573`  
		Last Modified: Thu, 14 Oct 2021 01:20:32 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56232465c4db3849de029290c3113d2e54c170959078f1c6db79be04f25679d9`  
		Last Modified: Thu, 14 Oct 2021 01:20:32 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ee5c28f159c990af395a85aca6dd92d3e5df1db87f1d1b22dd971db191ffa0`  
		Last Modified: Thu, 14 Oct 2021 01:20:33 GMT  
		Size: 3.1 MB (3063245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8ea081b840509c49626aada5a751b15f06425894b1909de76d192b435f459d`  
		Last Modified: Thu, 14 Oct 2021 01:20:40 GMT  
		Size: 57.0 MB (56997726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33af764c7ef4e285b105b1dfdd393764172a828c880727596371b3d095e4fcd5`  
		Last Modified: Thu, 14 Oct 2021 01:20:32 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4` - linux; s390x

```console
$ docker pull redmine@sha256:49a1c1b85f8ccd222764c18d3694feaf0642800543699062e12064d13fecc636
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.9 MB (201879289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48dd54a6734cf67e04ecc514a8756a628f6b402e434e592dc8d1bf2a75b15627`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:42:59 GMT
ADD file:3ff5fbc9c53cf76aad0fe0e1a525cb0bc0d70e8f2a3d5741dfb8b3b8a9448ffd in / 
# Wed, 17 Nov 2021 02:43:00 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:21:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:21:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:21:07 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:35:52 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 09:35:52 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 09:35:52 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 09:37:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 09:37:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 09:37:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 09:37:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:37:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 09:37:16 GMT
CMD ["irb"]
# Wed, 17 Nov 2021 20:31:43 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 17 Nov 2021 20:32:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:32:10 GMT
ENV RAILS_ENV=production
# Wed, 17 Nov 2021 20:32:10 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Nov 2021 20:32:10 GMT
ENV HOME=/home/redmine
# Wed, 17 Nov 2021 20:32:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 17 Nov 2021 20:32:11 GMT
ENV REDMINE_VERSION=4.2.3
# Wed, 17 Nov 2021 20:32:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Wed, 17 Nov 2021 20:32:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 17 Nov 2021 20:34:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 20:34:07 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Nov 2021 20:34:08 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 17 Nov 2021 20:34:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 20:34:08 GMT
EXPOSE 3000
# Wed, 17 Nov 2021 20:34:08 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b8b917e61b3be882db10e68210f73caf5cc788bfb07aec0a659e30f4796b476b`  
		Last Modified: Wed, 17 Nov 2021 02:49:01 GMT  
		Size: 25.8 MB (25769063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e574c6d046371657ec033b78bc3df865890056f711b30df7505d0128446e36`  
		Last Modified: Wed, 17 Nov 2021 09:48:11 GMT  
		Size: 10.8 MB (10815243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6bfb1613df50da70222f9b1cd395c4b509f6e6631cf6a13ce6c6b9c8c4cf181`  
		Last Modified: Wed, 17 Nov 2021 09:48:09 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa70e45053269d04d1a7217aca754f0b1fd37826bacef60c3e79535af03de7e`  
		Last Modified: Wed, 17 Nov 2021 09:50:18 GMT  
		Size: 14.7 MB (14697150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f6665bc1be788124ffa49dc9aca2a874932441c39767aac3628a05b46b7f808`  
		Last Modified: Wed, 17 Nov 2021 09:50:16 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ad94a5ab88cff035b5e7ab928b3855131115a475ac3f69d13d3b648539b059`  
		Last Modified: Wed, 17 Nov 2021 20:39:22 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef81635c9981af53c3728bbbdf8957635a0b7afccb029ae985a6fe7e6ae527`  
		Last Modified: Wed, 17 Nov 2021 20:39:34 GMT  
		Size: 91.8 MB (91791039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8be6a475176385654d74664b9bc12bade950866233a6eb369175876849a61a9`  
		Last Modified: Wed, 17 Nov 2021 20:39:21 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d214f8c5411f63986c0d7ee3a9032324738c7b89be0432e0ff9616a27a72485f`  
		Last Modified: Wed, 17 Nov 2021 20:39:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a849b87f96d4317e30bb0352a51b94195d07907f8535be33300f0452e6808655`  
		Last Modified: Wed, 17 Nov 2021 20:39:21 GMT  
		Size: 3.1 MB (3063246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e05a462fbf41e321955f3c91b6791ba04c37145f855bda5355c75973c4705c2`  
		Last Modified: Wed, 17 Nov 2021 20:39:25 GMT  
		Size: 55.7 MB (55739301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f740e646b3a43cb2398040cad7d9e0ed87da62a1457bd92bcc4d0c5a0b8be27c`  
		Last Modified: Wed, 17 Nov 2021 20:39:21 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4-alpine`

```console
$ docker pull redmine@sha256:cf4ec4d559c84d289809ddc6554057e6522d3720200a340c70ba098c12202c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:518ba4effd92c427ef19922743eea649ed001436d8a66fe0de469abb2de00949
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (149044368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48a04de41bf1795abeee36effc817551b3de5069209d3ec827816281c81211a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:28:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Sat, 13 Nov 2021 06:28:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 13 Nov 2021 06:28:18 GMT
ENV LANG=C.UTF-8
# Sat, 13 Nov 2021 06:44:36 GMT
ENV RUBY_MAJOR=2.7
# Sat, 13 Nov 2021 06:44:36 GMT
ENV RUBY_VERSION=2.7.4
# Sat, 13 Nov 2021 06:44:37 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Sat, 13 Nov 2021 06:47:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 13 Nov 2021 06:47:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 13 Nov 2021 06:47:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 13 Nov 2021 06:47:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Nov 2021 06:47:56 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 13 Nov 2021 06:47:56 GMT
CMD ["irb"]
# Sat, 13 Nov 2021 14:28:59 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 13 Nov 2021 14:29:07 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Sat, 13 Nov 2021 14:29:07 GMT
ENV RAILS_ENV=production
# Sat, 13 Nov 2021 14:29:08 GMT
WORKDIR /usr/src/redmine
# Sat, 13 Nov 2021 14:29:08 GMT
ENV HOME=/home/redmine
# Sat, 13 Nov 2021 14:29:09 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 13 Nov 2021 14:29:09 GMT
ENV REDMINE_VERSION=4.2.3
# Sat, 13 Nov 2021 14:29:09 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Sat, 13 Nov 2021 14:29:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 13 Nov 2021 14:29:13 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 13 Nov 2021 14:31:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 13 Nov 2021 14:31:21 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 13 Nov 2021 14:31:22 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Sat, 13 Nov 2021 14:31:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Nov 2021 14:31:22 GMT
EXPOSE 3000
# Sat, 13 Nov 2021 14:31:22 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86e849bc66e37f2d898daa44d76330256a48635f1100e364c0f46206fca7b71`  
		Last Modified: Sat, 13 Nov 2021 06:56:48 GMT  
		Size: 3.6 MB (3582307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a2fc84ba5b32bce31936a6fdf8121f29d2eb485f8525795df7d32046e9f856`  
		Last Modified: Sat, 13 Nov 2021 06:56:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e81c0605571c3961987ae1ce872ebef2b5bcb439010c194e90b47282556c32d`  
		Last Modified: Sat, 13 Nov 2021 06:58:25 GMT  
		Size: 14.0 MB (13994126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2814005984530d27bc89e1c810fb8cb01371038a28bc3d85a1e95b710d9e043e`  
		Last Modified: Sat, 13 Nov 2021 06:58:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e171914095295d927972128e1f66156ce389cb697d40fc6d7ea68c919861015e`  
		Last Modified: Sat, 13 Nov 2021 14:36:45 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9802858485f172f49a49aa23ebc2ef97aa9a7dff598d4d6b18f27e107ae24436`  
		Last Modified: Sat, 13 Nov 2021 14:36:55 GMT  
		Size: 69.5 MB (69548252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5b29e3b352df46dbdcf96478507ab2ace06abee4b91e86cea6852a73067d98`  
		Last Modified: Sat, 13 Nov 2021 14:36:43 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd79647c11e0ebdbaa7b41c71d969403768f7950e69f1b9eda5545fe42e86b3`  
		Last Modified: Sat, 13 Nov 2021 14:36:42 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20504c29a1f01e91c83c2e1e82a90fb05c118bbf74d44fa621ec588a179bce4b`  
		Last Modified: Sat, 13 Nov 2021 14:36:43 GMT  
		Size: 3.1 MB (3064272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7d43b9df6162fdd2b107724ff288c851a49738e7e04fa16cd34fddde661b04`  
		Last Modified: Sat, 13 Nov 2021 14:36:48 GMT  
		Size: 56.0 MB (56029256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561c4b4d66001dcdc5ff09131812075d6a6d4f6430e175565724033921e826f1`  
		Last Modified: Sat, 13 Nov 2021 14:36:42 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4-passenger`

```console
$ docker pull redmine@sha256:0a2beba76e007d174f23a2648bb6286f22d459f02c4e52c079b233cc06019f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:5df4cc2cc1a71f5966a962dabe733bb283f5dcf2d5d79c9a624ca4d234f974b4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221663528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88e23cfd35a24f595790cf1434facb584b62ba6518a62473675f114c5bed8f2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:20:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:20:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 15:20:38 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 15:27:24 GMT
ENV RUBY_MAJOR=2.7
# Tue, 12 Oct 2021 15:27:25 GMT
ENV RUBY_VERSION=2.7.4
# Tue, 12 Oct 2021 15:27:25 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Tue, 12 Oct 2021 15:30:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 15:30:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 15:30:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 15:30:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 15:30:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 15:30:34 GMT
CMD ["irb"]
# Tue, 12 Oct 2021 20:17:43 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 12 Oct 2021 20:18:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 20:18:13 GMT
ENV RAILS_ENV=production
# Tue, 12 Oct 2021 20:18:13 GMT
WORKDIR /usr/src/redmine
# Tue, 12 Oct 2021 20:18:14 GMT
ENV HOME=/home/redmine
# Tue, 12 Oct 2021 20:18:14 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 12 Oct 2021 20:18:15 GMT
ENV REDMINE_VERSION=4.2.3
# Tue, 12 Oct 2021 20:18:15 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Tue, 12 Oct 2021 20:18:19 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 12 Oct 2021 20:19:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Oct 2021 20:19:20 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 12 Oct 2021 20:19:20 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 12 Oct 2021 20:19:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 20:19:21 GMT
EXPOSE 3000
# Tue, 12 Oct 2021 20:19:21 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Wed, 10 Nov 2021 03:46:11 GMT
ENV PASSENGER_VERSION=6.0.12
# Wed, 10 Nov 2021 03:46:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 10 Nov 2021 03:46:36 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Wed, 10 Nov 2021 03:46:36 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Wed, 10 Nov 2021 03:46:36 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee6af487f217efc8e231b9857a8031fdf07ab0c8b30e539497893ec5287578b`  
		Last Modified: Tue, 12 Oct 2021 15:39:48 GMT  
		Size: 12.6 MB (12565186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48bb8449b0384f7addf4ec5d88d8ef088e25ca52f9299c1fca4bff3f5b2411d`  
		Last Modified: Tue, 12 Oct 2021 15:39:46 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4280126bdef2ed0df50609c224de8bcb7486f4ce6959104e588d7b147eb14f`  
		Last Modified: Tue, 12 Oct 2021 15:40:36 GMT  
		Size: 14.5 MB (14510184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4cc9067aac92ce406573f770322af2801a273925a95583e61e3ce6b568851a`  
		Last Modified: Tue, 12 Oct 2021 15:40:33 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf24873f395941528bd53ff8223d6b7799153cf8145e3b7158e496a8a4b9def`  
		Last Modified: Tue, 12 Oct 2021 20:27:17 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3deebb307eea15c0af224fa48dfa44ef5eb083d662d56e4eb24d97d503a2bb3f`  
		Last Modified: Tue, 12 Oct 2021 20:27:32 GMT  
		Size: 94.1 MB (94088542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799adc6ff62bdab4f48789fde71c3a76c4c1afa0e5288f175f5092a2e5867657`  
		Last Modified: Tue, 12 Oct 2021 20:27:14 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd34b5a0c4380ebac887ae883212d7ed6aa5e5fafbcfc5611ef03b072a3d34d`  
		Last Modified: Tue, 12 Oct 2021 20:27:15 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b355bfb624ca195d5b52d9a3257d514eff56e8b581bfd705949d266e7e1cad4`  
		Last Modified: Tue, 12 Oct 2021 20:27:15 GMT  
		Size: 3.1 MB (3063247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a87ccde718061b2b0d26691dacf79a140cd1b32f380e6c6d3a8f397be5156d44`  
		Last Modified: Tue, 12 Oct 2021 20:27:20 GMT  
		Size: 44.1 MB (44129736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e79252e1149fadd0907e406c69bd8e989028da830f9a410edb32ca9887a7d6`  
		Last Modified: Tue, 12 Oct 2021 20:27:15 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a284a323be9f6611677ab116846d6c4dbf712313bcce34cf3e2c684501d18e10`  
		Last Modified: Wed, 10 Nov 2021 03:48:08 GMT  
		Size: 21.2 MB (21238255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebe82b2f5ac28b2b6826a4aec1e29a72892ccea15a741fc388f2c686094da69`  
		Last Modified: Wed, 10 Nov 2021 03:48:06 GMT  
		Size: 4.9 MB (4924623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.0`

```console
$ docker pull redmine@sha256:51fdc00adef6f903301c62ff2852fe8159c7276dd9cdd034e06e10d0ffae7963
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

### `redmine:4.0` - linux; amd64

```console
$ docker pull redmine@sha256:d05e6d530735e8d5881f9327bc659a02f02ce7f3ea58110618f15c69d39e9ffd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.1 MB (205079351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b7e713d64f6b3d4959f4e70f1d18cba600919a28f04615191c094a5f47f7e0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:20:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:20:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 15:20:38 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 15:34:09 GMT
ENV RUBY_MAJOR=2.6
# Tue, 12 Oct 2021 15:34:09 GMT
ENV RUBY_VERSION=2.6.8
# Tue, 12 Oct 2021 15:34:09 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Tue, 12 Oct 2021 15:37:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 15:37:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 15:37:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 15:37:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 15:37:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 15:37:06 GMT
CMD ["irb"]
# Tue, 12 Oct 2021 20:20:16 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 12 Oct 2021 20:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 20:23:19 GMT
ENV RAILS_ENV=production
# Tue, 12 Oct 2021 20:23:20 GMT
WORKDIR /usr/src/redmine
# Tue, 12 Oct 2021 20:23:20 GMT
ENV HOME=/home/redmine
# Tue, 12 Oct 2021 20:23:21 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 12 Oct 2021 20:23:21 GMT
ENV REDMINE_VERSION=4.0.9
# Tue, 12 Oct 2021 20:23:21 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Tue, 12 Oct 2021 20:23:25 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 12 Oct 2021 20:25:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Oct 2021 20:25:53 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 12 Oct 2021 20:25:54 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 12 Oct 2021 20:25:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 20:25:54 GMT
EXPOSE 3000
# Tue, 12 Oct 2021 20:25:54 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee6af487f217efc8e231b9857a8031fdf07ab0c8b30e539497893ec5287578b`  
		Last Modified: Tue, 12 Oct 2021 15:39:48 GMT  
		Size: 12.6 MB (12565186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48bb8449b0384f7addf4ec5d88d8ef088e25ca52f9299c1fca4bff3f5b2411d`  
		Last Modified: Tue, 12 Oct 2021 15:39:46 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fbc3e5ccddf2ccfcc978381549c751e1167cdf41ce60580404b33cb6fdd7aa5`  
		Last Modified: Tue, 12 Oct 2021 15:41:15 GMT  
		Size: 21.5 MB (21467885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b99a224b661061fbbe799d6efb95f01221754e6a73aec4d536865d1e304d63`  
		Last Modified: Tue, 12 Oct 2021 15:41:12 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b92be01811211d262d0872aabc77c74589ad10e263a5d091b7a77fc657edd4`  
		Last Modified: Tue, 12 Oct 2021 20:28:12 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5866c61464640233522ebdc402ab1639ef563ce15f4e766f0d2c9c46dbf47749`  
		Last Modified: Tue, 12 Oct 2021 20:29:14 GMT  
		Size: 81.2 MB (81200401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14796236954476acf9820e11bdeba8b19f45bff173cce221292a37501351dbfa`  
		Last Modified: Tue, 12 Oct 2021 20:28:54 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f04093222ab3c15896fea65f4415539848dfd324ae9899f30a662a277b53939`  
		Last Modified: Tue, 12 Oct 2021 20:28:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b703fd11a89eae2882c03999cd46f929263f1a53e9db14fca0d3a22402e65899`  
		Last Modified: Tue, 12 Oct 2021 20:28:55 GMT  
		Size: 2.5 MB (2542547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4dc91c4594f36a6f07f59f99aea2b24d308de0799bab28a2877ed2b560cbbef`  
		Last Modified: Tue, 12 Oct 2021 20:29:05 GMT  
		Size: 60.2 MB (60159580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474e32e03341c2aa37028e650008f2aef23216356cb3099c1fdd66d1190edfd9`  
		Last Modified: Tue, 12 Oct 2021 20:28:54 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0` - linux; arm variant v5

```console
$ docker pull redmine@sha256:76bde531fa51e9043ec26a480294be0bf2afa573b89eb6eee1c363d9b0061dae
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194735396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a62e304aa3370634bf65d28936336cbe23efb8ac202b18443990b1dae175e34`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 12 Oct 2021 00:51:32 GMT
ADD file:0d95eee31ffe3f4260263e4fac2a61123a4b98d2e7a67efcc7bfea338c54f41d in / 
# Tue, 12 Oct 2021 00:51:32 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 06:45:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 06:45:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 06:45:07 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 07:20:58 GMT
ENV RUBY_MAJOR=2.6
# Tue, 12 Oct 2021 07:20:58 GMT
ENV RUBY_VERSION=2.6.8
# Tue, 12 Oct 2021 07:20:59 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Tue, 12 Oct 2021 07:25:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 07:25:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 07:25:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 07:25:31 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 07:25:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 07:25:33 GMT
CMD ["irb"]
# Wed, 13 Oct 2021 03:13:47 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 13 Oct 2021 03:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 03:23:43 GMT
ENV RAILS_ENV=production
# Wed, 13 Oct 2021 03:23:44 GMT
WORKDIR /usr/src/redmine
# Wed, 13 Oct 2021 03:23:45 GMT
ENV HOME=/home/redmine
# Wed, 13 Oct 2021 03:23:47 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 13 Oct 2021 03:23:47 GMT
ENV REDMINE_VERSION=4.0.9
# Wed, 13 Oct 2021 03:23:48 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Wed, 13 Oct 2021 03:23:53 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 13 Oct 2021 03:30:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 13 Oct 2021 03:30:52 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 13 Oct 2021 03:30:54 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 13 Oct 2021 03:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Oct 2021 03:30:56 GMT
EXPOSE 3000
# Wed, 13 Oct 2021 03:30:57 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:175b083b22fb061f7d1894fe4916a2967ce636d47376da526d90d57c8f7efc60`  
		Last Modified: Tue, 12 Oct 2021 01:07:45 GMT  
		Size: 24.9 MB (24872704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed73113a2340f22427741647a89a1911c6dd067bde17833928c5d210ab93918`  
		Last Modified: Tue, 12 Oct 2021 07:31:54 GMT  
		Size: 10.3 MB (10349314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7a78f939d570718e0af30429b3118d94e3800937a469b3fca591fda6d0540e`  
		Last Modified: Tue, 12 Oct 2021 07:31:46 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee56be0d198078cdceb927f259d279ea37548abbdefb95d8056e7e15d8137f0`  
		Last Modified: Tue, 12 Oct 2021 07:35:42 GMT  
		Size: 20.7 MB (20733372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e080526cffc142b881616db7396494f86cda539f9b9c65296f73498b8f70f81`  
		Last Modified: Tue, 12 Oct 2021 07:35:32 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c030517df14ac43613f1cd4bf516123c442ce7a9e6f545e593cc52a6b40fd301`  
		Last Modified: Wed, 13 Oct 2021 03:33:10 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d678b665817d824792999b8bfe1097e772d539be20d87a21b7856e05e68b96fa`  
		Last Modified: Wed, 13 Oct 2021 03:34:44 GMT  
		Size: 77.0 MB (76964464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6268c5fac0a25fcda1e7b6e81b957c6ec41cd2a5e036ed031571f4d6c58f6b24`  
		Last Modified: Wed, 13 Oct 2021 03:34:07 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbaf21e0e9c72ebe28c5f11acc6887fd712ea95c2cd076725f01a2e89180c497`  
		Last Modified: Wed, 13 Oct 2021 03:34:06 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9804dc5e809a3c7310004b9c8e2d88e4a5a96fc1b4478080c2e4d4ce0585657b`  
		Last Modified: Wed, 13 Oct 2021 03:34:09 GMT  
		Size: 2.5 MB (2542539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:045d5a7b6ab1fa20d89537dbdd96653f63725bc98e85e648b81062fe647ca6c2`  
		Last Modified: Wed, 13 Oct 2021 03:34:29 GMT  
		Size: 59.3 MB (59268769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f02d814ee294160e2f9f09d190a6ed3a13b32c93990b2cb5ca48e819f88596`  
		Last Modified: Wed, 13 Oct 2021 03:34:07 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0` - linux; arm variant v7

```console
$ docker pull redmine@sha256:a4c280bbf76f9bba2834f9064504ed314608d46e14f36ced5448faaa80a44bc1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.1 MB (188068236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e8a6d08e93ea1d782be23860355520573e87862ab0ee514e619646b9cb223e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 12 Oct 2021 01:29:42 GMT
ADD file:fe1eaa1b1d760b3d250cb4ac331d26a261fc569f1694bd34e146f00874dc87e5 in / 
# Tue, 12 Oct 2021 01:29:43 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 02:56:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 02:56:30 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 03:29:09 GMT
ENV RUBY_MAJOR=2.6
# Tue, 12 Oct 2021 03:29:10 GMT
ENV RUBY_VERSION=2.6.8
# Tue, 12 Oct 2021 03:29:10 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Tue, 12 Oct 2021 03:33:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 03:33:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 03:33:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 03:33:31 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 03:33:33 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 03:33:33 GMT
CMD ["irb"]
# Wed, 13 Oct 2021 06:41:32 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 13 Oct 2021 06:49:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 06:49:21 GMT
ENV RAILS_ENV=production
# Wed, 13 Oct 2021 06:49:22 GMT
WORKDIR /usr/src/redmine
# Wed, 13 Oct 2021 06:49:22 GMT
ENV HOME=/home/redmine
# Wed, 13 Oct 2021 06:49:24 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 13 Oct 2021 06:49:25 GMT
ENV REDMINE_VERSION=4.0.9
# Wed, 13 Oct 2021 06:49:25 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Wed, 13 Oct 2021 06:49:31 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 13 Oct 2021 06:55:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 13 Oct 2021 06:55:07 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 13 Oct 2021 06:55:08 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 13 Oct 2021 06:55:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Oct 2021 06:55:08 GMT
EXPOSE 3000
# Wed, 13 Oct 2021 06:55:09 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c0b5ba470cac8cfdae4633f5cddb3ba9350fe1d1b1507c4965a8224eb40e52c5`  
		Last Modified: Tue, 12 Oct 2021 01:45:52 GMT  
		Size: 22.7 MB (22739698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cdd321094894b78bc0792d96cf339ee9e4ce7ec18a14ea44b32cfbc809867b`  
		Last Modified: Tue, 12 Oct 2021 03:40:20 GMT  
		Size: 9.9 MB (9872904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c0e1a382b6eb02d552bdb97946d22f8b0d9b5f787b5d1b491fa3703e23d5ea`  
		Last Modified: Tue, 12 Oct 2021 03:40:13 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c9c99e0177bf2b2564708b982b9c36357cd8d40692351ae3fb607492c43c90`  
		Last Modified: Tue, 12 Oct 2021 03:42:55 GMT  
		Size: 20.6 MB (20643669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb852a3aed1bbfa0863f056cd080fad5debc62aefa369421cb364fde8137ebf`  
		Last Modified: Tue, 12 Oct 2021 03:42:48 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1086d0917a940899c5d3bad3fc3feea5fe65219a792b2acd69cd9ada062a7b`  
		Last Modified: Wed, 13 Oct 2021 06:57:14 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb023e9c4cb9847d03887a1e74509d1006934f33f168f7767fa3d0cfbb8993a`  
		Last Modified: Wed, 13 Oct 2021 06:59:10 GMT  
		Size: 73.3 MB (73263173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0734a96aee601c48b488de39bdd899a39839fbaefdc1985bc857df450c198d`  
		Last Modified: Wed, 13 Oct 2021 06:58:22 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0517f5edd505304a5cef2b06581a9ef09936a60ee7a42294579ea2c03b3d56ac`  
		Last Modified: Wed, 13 Oct 2021 06:58:22 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdcbad9cf302ea0ce760081905d9900133ec90ce11fd39b09fbdf9c488257498`  
		Last Modified: Wed, 13 Oct 2021 06:58:26 GMT  
		Size: 2.5 MB (2542549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd922d77362506a9ce9e94dd73d4abe3e913ecce129f542af606401d53107264`  
		Last Modified: Wed, 13 Oct 2021 06:58:51 GMT  
		Size: 59.0 MB (59002007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32dd7573f2ae3e4eba3c72bbaed2d55ca28ac46b39bac2a652358df5ca161b6c`  
		Last Modified: Wed, 13 Oct 2021 06:58:22 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:e1640a145bf5840bf0b9e2ab84e9d93a0d24a18ed393b43f6be7a2f7b18fce0a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.4 MB (200438417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd7ec9b45c45b3a02a7ee54c69afa603f673991915570396bea1f1457a0e750`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:31:02 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:46:01 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 09:46:02 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 09:46:03 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 09:48:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 09:48:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 09:48:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 09:48:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:48:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 09:48:06 GMT
CMD ["irb"]
# Wed, 17 Nov 2021 19:49:55 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 17 Nov 2021 19:53:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 19:53:13 GMT
ENV RAILS_ENV=production
# Wed, 17 Nov 2021 19:53:14 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Nov 2021 19:53:15 GMT
ENV HOME=/home/redmine
# Wed, 17 Nov 2021 19:53:16 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 17 Nov 2021 19:53:17 GMT
ENV REDMINE_VERSION=4.0.9
# Wed, 17 Nov 2021 19:53:18 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Wed, 17 Nov 2021 19:53:22 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 17 Nov 2021 19:55:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 19:55:45 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Nov 2021 19:55:46 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 17 Nov 2021 19:55:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 19:55:47 GMT
EXPOSE 3000
# Wed, 17 Nov 2021 19:55:48 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8443a8ec909433d7156b8dcbeaf77f4e53d6a44b253a3f03b95126547154d55`  
		Last Modified: Wed, 17 Nov 2021 09:51:43 GMT  
		Size: 11.3 MB (11261808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f57122fa0ffe176f788d35a4a8f12a76819fa3bab198ac16e26d2961047a1d`  
		Last Modified: Wed, 17 Nov 2021 09:51:41 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16912dae180f72843a7e6b7dd25071e1090943354879adab903dcd984c8cee67`  
		Last Modified: Wed, 17 Nov 2021 09:54:26 GMT  
		Size: 21.1 MB (21095263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b73b9ee9aa5f816c4fb7665c7e19fe1663007ac1aacb74064aac56ece594983`  
		Last Modified: Wed, 17 Nov 2021 09:54:23 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb50985615235593da91e201ffe4b1db40feab50ab0a12b02a4c99191da4dfd`  
		Last Modified: Wed, 17 Nov 2021 19:57:02 GMT  
		Size: 1.6 KB (1625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde74bffacc846943dfa6d226151f2242bb938be3ad44c6dcdd0dae1d33a42b3`  
		Last Modified: Wed, 17 Nov 2021 19:57:42 GMT  
		Size: 79.8 MB (79758991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279493fe0772df535c0878e63b1b64fba2b226e69a69fe151989981e2e059753`  
		Last Modified: Wed, 17 Nov 2021 19:57:28 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55b03979292e18cc4dce62c30e68343071ed1073cddd16a31506b6a78a29155`  
		Last Modified: Wed, 17 Nov 2021 19:57:28 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd290e4917e62816eb06bb5841ee9c059f8d44144cff4fa97a200732d285904`  
		Last Modified: Wed, 17 Nov 2021 19:57:29 GMT  
		Size: 2.5 MB (2543981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23fdce25f1a772528d0357b38e56069cd549aa907ba49f53e6cbac362540eeef`  
		Last Modified: Wed, 17 Nov 2021 19:57:37 GMT  
		Size: 59.9 MB (59851226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa0e7224f51928ab8db5b08f76b818cc36d597e64ea832546f26380efc40f02`  
		Last Modified: Wed, 17 Nov 2021 19:57:28 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0` - linux; 386

```console
$ docker pull redmine@sha256:f1fe73108e092e98101c8561db5f30df576481a8663f6260f48c5d493362fc1e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210347648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2a96bb39dd0f782181d9ca3c863004466bb821cd3f4eacfd701fa18b69ab5e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 18:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 18:38:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 18:38:25 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 19:07:29 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 19:07:29 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 19:07:29 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 19:11:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 19:11:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 19:11:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 19:12:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 19:12:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 19:12:01 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 00:37:59 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 00:40:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 00:40:06 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 00:40:06 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 00:40:06 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 00:40:08 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 00:40:08 GMT
ENV REDMINE_VERSION=4.0.9
# Thu, 18 Nov 2021 00:40:08 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Thu, 18 Nov 2021 00:40:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 00:42:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 00:42:32 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 00:42:33 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 00:42:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 00:42:33 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 00:42:33 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1742b7e5e1e5bca675e7f251c9f6fe8778a1bb1548e5b418f8547277f14e2e33`  
		Last Modified: Wed, 17 Nov 2021 19:17:19 GMT  
		Size: 17.2 MB (17227026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ef5459771b89c49219d5c15641c7215faf156712422f01efee40ad955a52c5`  
		Last Modified: Wed, 17 Nov 2021 19:17:10 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8e5a4df5a8f121515c23ab2e470f17d64c6bb138b6c22dda592fcde5393ca4`  
		Last Modified: Wed, 17 Nov 2021 19:20:39 GMT  
		Size: 20.9 MB (20910059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955765ea073687d915724497fa422005e56011fcf7d74483d30fd502a0ae1992`  
		Last Modified: Wed, 17 Nov 2021 19:20:35 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114a479d47bf9ce3b07ffb880a448300b978f0dd2fb9b2cf257248dd29de5e84`  
		Last Modified: Thu, 18 Nov 2021 00:44:01 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7da47a96d23e66f0e9def04a7192dde8c3f9cd839282fda3efd121d97eda435`  
		Last Modified: Thu, 18 Nov 2021 00:45:17 GMT  
		Size: 82.6 MB (82599710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1928f566c831a396b46d1da2e213d7e2a8e77a2d900040af95c718d58cba7f60`  
		Last Modified: Thu, 18 Nov 2021 00:44:47 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a6707cbab4ac55df2d2037e249005c67725357318531f7673e1887b17fb300`  
		Last Modified: Thu, 18 Nov 2021 00:44:47 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d499e312e0f51e9de1e154f0944c20e8865d7114738e8b3ad6a65b07e1ce555`  
		Last Modified: Thu, 18 Nov 2021 00:44:49 GMT  
		Size: 2.5 MB (2542545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c34f6b79c0664ea6304fa45c671cc8239eba56a967c5c3f474672d335c96b7a`  
		Last Modified: Thu, 18 Nov 2021 00:45:03 GMT  
		Size: 59.3 MB (59259521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d6247c6cc7f7721a644ff15bf4633ab39ca26e5094d60356b696840bda35ec`  
		Last Modified: Thu, 18 Nov 2021 00:44:47 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0` - linux; ppc64le

```console
$ docker pull redmine@sha256:6aac498c44f600b672d9897703c3c41b214924e3fc233e7860fd8e545b136e77
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216469674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4da6045a34b42bbefc251f10d5f010773a1e6f3bcfc1555ea6958d409fbead`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 12 Oct 2021 01:26:46 GMT
ADD file:5526880c6f19a4b4231a8b2bd7cfc625d116764c4918eff6f0b55f8c1eb38e1a in / 
# Tue, 12 Oct 2021 01:26:50 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 18:23:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 18:24:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 18:24:11 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 19:17:28 GMT
ENV RUBY_MAJOR=2.6
# Tue, 12 Oct 2021 19:17:32 GMT
ENV RUBY_VERSION=2.6.8
# Tue, 12 Oct 2021 19:17:38 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Tue, 12 Oct 2021 19:25:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 19:25:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 19:26:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 19:26:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 19:26:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 19:26:22 GMT
CMD ["irb"]
# Thu, 14 Oct 2021 00:54:05 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 14 Oct 2021 01:07:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 Oct 2021 01:08:11 GMT
ENV RAILS_ENV=production
# Thu, 14 Oct 2021 01:08:23 GMT
WORKDIR /usr/src/redmine
# Thu, 14 Oct 2021 01:08:27 GMT
ENV HOME=/home/redmine
# Thu, 14 Oct 2021 01:08:42 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 14 Oct 2021 01:08:47 GMT
ENV REDMINE_VERSION=4.0.9
# Thu, 14 Oct 2021 01:08:56 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Thu, 14 Oct 2021 01:09:18 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 14 Oct 2021 01:19:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 Oct 2021 01:19:19 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 14 Oct 2021 01:19:23 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 14 Oct 2021 01:19:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Oct 2021 01:19:47 GMT
EXPOSE 3000
# Thu, 14 Oct 2021 01:19:52 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d69973af32573c07c8789c0f9c144a5c0b822a1e85b59db3ce9f8ebc489ce85d`  
		Last Modified: Tue, 12 Oct 2021 01:38:40 GMT  
		Size: 30.5 MB (30547197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f48a596ad1fccd3e24dcc1f65e362937ced6f5b5ab61b6eb49e8eda8a55b85`  
		Last Modified: Tue, 12 Oct 2021 19:30:52 GMT  
		Size: 12.7 MB (12705483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd72e7e6250a90b152d1d27efca928b2c1bfc949dfe1b2e9cf089acde024c098`  
		Last Modified: Tue, 12 Oct 2021 19:30:49 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03211df41d3c61789be71d89ebad2ce881638fb2a84c27562d7e3ff81f181458`  
		Last Modified: Tue, 12 Oct 2021 19:33:41 GMT  
		Size: 22.0 MB (21984973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c774747b6862c16e290d0508df2db39d1a24d4061e198d3567c877d14ca4bf8`  
		Last Modified: Tue, 12 Oct 2021 19:33:38 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d344e083cdb889978f1a8f40a20c569e9d02d096352f103edc1381edd38d39a`  
		Last Modified: Thu, 14 Oct 2021 01:22:07 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac438230a35738c21d025cb57c8c2c12a0694fc9dcafd9d3f1f1cc5d52cac12`  
		Last Modified: Thu, 14 Oct 2021 01:22:55 GMT  
		Size: 87.9 MB (87902632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96411f53dc60a5c0667e24e7007ead33f7a43d92b6c882aa193e719f58ed663`  
		Last Modified: Thu, 14 Oct 2021 01:22:36 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2634382c5d445a0bba90dc55ead78291350aad0aa956fe9f87bbaa4f73cdfed`  
		Last Modified: Thu, 14 Oct 2021 01:22:37 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e17f74adf31cae17cfb0a926e812563f2f59c5c7778cc5f8d84e26e09015218`  
		Last Modified: Thu, 14 Oct 2021 01:22:37 GMT  
		Size: 2.5 MB (2542548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce9fa655873ae250f6f495e0d5433626b0bba0c00566e89e82fcadc94703ea4`  
		Last Modified: Thu, 14 Oct 2021 01:22:45 GMT  
		Size: 60.8 MB (60782595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df59993b68006e819fad6adcd54c3e76dc6dc32f43f6b365d3a69aa8e22b1b35`  
		Last Modified: Thu, 14 Oct 2021 01:22:36 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0` - linux; s390x

```console
$ docker pull redmine@sha256:7a08ebb93b3b03597bf02476a2515778130f7bff1e3c33e8fcc00a1073ccfc31
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.3 MB (200291030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9aaeccdc23c9bbd5bb63a74995e35e24d80ec599e61878f1a15ad2fa1e82ea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:42:59 GMT
ADD file:3ff5fbc9c53cf76aad0fe0e1a525cb0bc0d70e8f2a3d5741dfb8b3b8a9448ffd in / 
# Wed, 17 Nov 2021 02:43:00 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:21:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:21:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:21:07 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:42:36 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 09:42:36 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 09:42:37 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 09:44:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 09:44:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 09:44:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 09:44:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:44:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 09:44:07 GMT
CMD ["irb"]
# Wed, 17 Nov 2021 20:34:19 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 17 Nov 2021 20:36:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:37:01 GMT
ENV RAILS_ENV=production
# Wed, 17 Nov 2021 20:37:01 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Nov 2021 20:37:01 GMT
ENV HOME=/home/redmine
# Wed, 17 Nov 2021 20:37:02 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 17 Nov 2021 20:37:02 GMT
ENV REDMINE_VERSION=4.0.9
# Wed, 17 Nov 2021 20:37:02 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Wed, 17 Nov 2021 20:37:04 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 17 Nov 2021 20:38:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 20:38:46 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Nov 2021 20:38:46 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 17 Nov 2021 20:38:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 20:38:46 GMT
EXPOSE 3000
# Wed, 17 Nov 2021 20:38:46 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b8b917e61b3be882db10e68210f73caf5cc788bfb07aec0a659e30f4796b476b`  
		Last Modified: Wed, 17 Nov 2021 02:49:01 GMT  
		Size: 25.8 MB (25769063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e574c6d046371657ec033b78bc3df865890056f711b30df7505d0128446e36`  
		Last Modified: Wed, 17 Nov 2021 09:48:11 GMT  
		Size: 10.8 MB (10815243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6bfb1613df50da70222f9b1cd395c4b509f6e6631cf6a13ce6c6b9c8c4cf181`  
		Last Modified: Wed, 17 Nov 2021 09:48:09 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37bdaf56dd9686cdaca63c3c8ebab2d6841412a36159619d65853daa75500716`  
		Last Modified: Wed, 17 Nov 2021 09:51:17 GMT  
		Size: 21.6 MB (21619852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80433d0a1bacd8eb06bb301d366ea459dbae5ce9a2bea94372bd52e0939584a0`  
		Last Modified: Wed, 17 Nov 2021 09:51:15 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e82306e7113526e6aa75620a186091a8a2139c7e63336bc2033df0329cda36e`  
		Last Modified: Wed, 17 Nov 2021 20:39:48 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085d5f5c7261748f638b0c30c5922b96cc7a7139c94d116b31323b1fe50f715c`  
		Last Modified: Wed, 17 Nov 2021 20:40:19 GMT  
		Size: 78.9 MB (78941825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdafcf9171e45387b8e26650c032636412a64ea71a82beb8da9aaadda5a038a`  
		Last Modified: Wed, 17 Nov 2021 20:40:08 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd65e98466ef8280e1eac2c5693840a60cd00682e5bbdafe9bde2b47edd7275`  
		Last Modified: Wed, 17 Nov 2021 20:40:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25e48155420ae67e64e5329514da95aeea977ad3762dff4bc8baacdb80a3058`  
		Last Modified: Wed, 17 Nov 2021 20:40:08 GMT  
		Size: 2.5 MB (2542547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d56cd02bb76bc97344bf358dd1335582e1460a561ab33d1c8dab2a5c27c2f66e`  
		Last Modified: Wed, 17 Nov 2021 20:40:14 GMT  
		Size: 60.6 MB (60598255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05981b15aac91be53d29f32192b2ad7af008afe472c8d7aab11db0049c3de996`  
		Last Modified: Wed, 17 Nov 2021 20:40:08 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.0-alpine`

```console
$ docker pull redmine@sha256:fa8ba213e2dfef7bfb98c3b2ca6af9917a9c0b9b15be67bb8c20499ac3d04aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.0-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:01887efbc27065bcc544e6ba80201b994e89e27280c7b25de2c280d6f1b33024
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.6 MB (153558063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4abb35ae9e45f8c5510f9bfe3efa808d3e893645c29b1b6aa08bae910bf2aa9a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:28:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Sat, 13 Nov 2021 06:28:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 13 Nov 2021 06:28:18 GMT
ENV LANG=C.UTF-8
# Sat, 13 Nov 2021 06:51:30 GMT
ENV RUBY_MAJOR=2.6
# Sat, 13 Nov 2021 06:51:30 GMT
ENV RUBY_VERSION=2.6.8
# Sat, 13 Nov 2021 06:51:31 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Sat, 13 Nov 2021 06:54:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 13 Nov 2021 06:54:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 13 Nov 2021 06:54:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 13 Nov 2021 06:54:45 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Nov 2021 06:54:45 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 13 Nov 2021 06:54:46 GMT
CMD ["irb"]
# Sat, 13 Nov 2021 14:31:40 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 13 Nov 2021 14:34:28 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				git 		mercurial 		openssh-client 		subversion 				ghostscript-fonts 		imagemagick6 	;
# Sat, 13 Nov 2021 14:34:29 GMT
ENV RAILS_ENV=production
# Sat, 13 Nov 2021 14:34:29 GMT
WORKDIR /usr/src/redmine
# Sat, 13 Nov 2021 14:34:29 GMT
ENV HOME=/home/redmine
# Sat, 13 Nov 2021 14:34:30 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 13 Nov 2021 14:34:30 GMT
ENV REDMINE_VERSION=4.0.9
# Sat, 13 Nov 2021 14:34:30 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Sat, 13 Nov 2021 14:34:34 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 13 Nov 2021 14:34:34 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 13 Nov 2021 14:36:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 		imagemagick6-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 13 Nov 2021 14:36:07 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 13 Nov 2021 14:36:07 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Sat, 13 Nov 2021 14:36:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Nov 2021 14:36:07 GMT
EXPOSE 3000
# Sat, 13 Nov 2021 14:36:08 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86e849bc66e37f2d898daa44d76330256a48635f1100e364c0f46206fca7b71`  
		Last Modified: Sat, 13 Nov 2021 06:56:48 GMT  
		Size: 3.6 MB (3582307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a2fc84ba5b32bce31936a6fdf8121f29d2eb485f8525795df7d32046e9f856`  
		Last Modified: Sat, 13 Nov 2021 06:56:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fd76747f3be3e4f4af1119b668fd5a9fa53725f84b429575cfb26c0d5f842a`  
		Last Modified: Sat, 13 Nov 2021 06:59:00 GMT  
		Size: 19.5 MB (19500293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bbfb1229cd3c27d4dd990a0daf591e427afbc679b854303415a9e9a01ff10b`  
		Last Modified: Sat, 13 Nov 2021 06:58:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c267c2d73515a2e4fbaac349e5a31212348b7d72b21f80611dac1923c5c68666`  
		Last Modified: Sat, 13 Nov 2021 14:37:15 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7ea963f3d5877eea0043f8a2b75f17680ff5a4d362c1a4fce8c8a67c347239`  
		Last Modified: Sat, 13 Nov 2021 14:37:49 GMT  
		Size: 66.2 MB (66199469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05071f335bb9135d55d21c80aaa3523ae388d93f1a98136404e7c91fa99fb524`  
		Last Modified: Sat, 13 Nov 2021 14:37:37 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a43db45233bb37a8a7df21efee11df06d119f141dd51e3c8672893a9bb6a654`  
		Last Modified: Sat, 13 Nov 2021 14:37:37 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb71bc10f9decb3a165b48fa2dae4aa79929b41c812f261a1ff1fee173510e8`  
		Last Modified: Sat, 13 Nov 2021 14:37:38 GMT  
		Size: 2.5 MB (2543762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d38dd936d4bdfa095bb3270305cfe38c97043649fdf48ba25879b221ebbb40`  
		Last Modified: Sat, 13 Nov 2021 14:37:43 GMT  
		Size: 58.9 MB (58906080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ac236fd681e485d4f3495d7195078b72db1997782784f2aca237835c80c236`  
		Last Modified: Sat, 13 Nov 2021 14:37:37 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.0-passenger`

```console
$ docker pull redmine@sha256:8f5dc49e7e8b0e12174df5fa85995971245c971765697ba9c8d5dfedbf1181c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.0-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:ab67f320b1123ca1304a82c786eae4039d20fd4c88b83296db005396040c20c2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231443403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f098d154d4397a6cf6ab16cf24d877414f42e3f0e229c0f85ebbc51d47fc41`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:20:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:20:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 15:20:38 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 15:34:09 GMT
ENV RUBY_MAJOR=2.6
# Tue, 12 Oct 2021 15:34:09 GMT
ENV RUBY_VERSION=2.6.8
# Tue, 12 Oct 2021 15:34:09 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Tue, 12 Oct 2021 15:37:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 15:37:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 15:37:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 15:37:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 15:37:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 15:37:06 GMT
CMD ["irb"]
# Tue, 12 Oct 2021 20:20:16 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 12 Oct 2021 20:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 20:23:19 GMT
ENV RAILS_ENV=production
# Tue, 12 Oct 2021 20:23:20 GMT
WORKDIR /usr/src/redmine
# Tue, 12 Oct 2021 20:23:20 GMT
ENV HOME=/home/redmine
# Tue, 12 Oct 2021 20:23:21 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 12 Oct 2021 20:23:21 GMT
ENV REDMINE_VERSION=4.0.9
# Tue, 12 Oct 2021 20:23:21 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Tue, 12 Oct 2021 20:23:25 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 12 Oct 2021 20:25:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Oct 2021 20:25:53 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 12 Oct 2021 20:25:54 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 12 Oct 2021 20:25:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 20:25:54 GMT
EXPOSE 3000
# Tue, 12 Oct 2021 20:25:54 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Wed, 10 Nov 2021 03:47:10 GMT
ENV PASSENGER_VERSION=6.0.12
# Wed, 10 Nov 2021 03:47:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 10 Nov 2021 03:47:29 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Wed, 10 Nov 2021 03:47:29 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Wed, 10 Nov 2021 03:47:29 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee6af487f217efc8e231b9857a8031fdf07ab0c8b30e539497893ec5287578b`  
		Last Modified: Tue, 12 Oct 2021 15:39:48 GMT  
		Size: 12.6 MB (12565186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48bb8449b0384f7addf4ec5d88d8ef088e25ca52f9299c1fca4bff3f5b2411d`  
		Last Modified: Tue, 12 Oct 2021 15:39:46 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fbc3e5ccddf2ccfcc978381549c751e1167cdf41ce60580404b33cb6fdd7aa5`  
		Last Modified: Tue, 12 Oct 2021 15:41:15 GMT  
		Size: 21.5 MB (21467885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b99a224b661061fbbe799d6efb95f01221754e6a73aec4d536865d1e304d63`  
		Last Modified: Tue, 12 Oct 2021 15:41:12 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b92be01811211d262d0872aabc77c74589ad10e263a5d091b7a77fc657edd4`  
		Last Modified: Tue, 12 Oct 2021 20:28:12 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5866c61464640233522ebdc402ab1639ef563ce15f4e766f0d2c9c46dbf47749`  
		Last Modified: Tue, 12 Oct 2021 20:29:14 GMT  
		Size: 81.2 MB (81200401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14796236954476acf9820e11bdeba8b19f45bff173cce221292a37501351dbfa`  
		Last Modified: Tue, 12 Oct 2021 20:28:54 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f04093222ab3c15896fea65f4415539848dfd324ae9899f30a662a277b53939`  
		Last Modified: Tue, 12 Oct 2021 20:28:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b703fd11a89eae2882c03999cd46f929263f1a53e9db14fca0d3a22402e65899`  
		Last Modified: Tue, 12 Oct 2021 20:28:55 GMT  
		Size: 2.5 MB (2542547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4dc91c4594f36a6f07f59f99aea2b24d308de0799bab28a2877ed2b560cbbef`  
		Last Modified: Tue, 12 Oct 2021 20:29:05 GMT  
		Size: 60.2 MB (60159580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474e32e03341c2aa37028e650008f2aef23216356cb3099c1fdd66d1190edfd9`  
		Last Modified: Tue, 12 Oct 2021 20:28:54 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d8b5222950710a3689bed3c7d25c043a60ee6308b734dd7e9e3fb1cd20aecf`  
		Last Modified: Wed, 10 Nov 2021 03:48:45 GMT  
		Size: 21.4 MB (21439436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0429cf4f74ed45039bbed5c5f537f08b624eb8bd977152cd098f2b290c2c5dd0`  
		Last Modified: Wed, 10 Nov 2021 03:48:43 GMT  
		Size: 4.9 MB (4924616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.0.9`

```console
$ docker pull redmine@sha256:51fdc00adef6f903301c62ff2852fe8159c7276dd9cdd034e06e10d0ffae7963
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

### `redmine:4.0.9` - linux; amd64

```console
$ docker pull redmine@sha256:d05e6d530735e8d5881f9327bc659a02f02ce7f3ea58110618f15c69d39e9ffd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.1 MB (205079351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b7e713d64f6b3d4959f4e70f1d18cba600919a28f04615191c094a5f47f7e0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:20:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:20:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 15:20:38 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 15:34:09 GMT
ENV RUBY_MAJOR=2.6
# Tue, 12 Oct 2021 15:34:09 GMT
ENV RUBY_VERSION=2.6.8
# Tue, 12 Oct 2021 15:34:09 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Tue, 12 Oct 2021 15:37:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 15:37:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 15:37:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 15:37:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 15:37:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 15:37:06 GMT
CMD ["irb"]
# Tue, 12 Oct 2021 20:20:16 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 12 Oct 2021 20:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 20:23:19 GMT
ENV RAILS_ENV=production
# Tue, 12 Oct 2021 20:23:20 GMT
WORKDIR /usr/src/redmine
# Tue, 12 Oct 2021 20:23:20 GMT
ENV HOME=/home/redmine
# Tue, 12 Oct 2021 20:23:21 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 12 Oct 2021 20:23:21 GMT
ENV REDMINE_VERSION=4.0.9
# Tue, 12 Oct 2021 20:23:21 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Tue, 12 Oct 2021 20:23:25 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 12 Oct 2021 20:25:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Oct 2021 20:25:53 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 12 Oct 2021 20:25:54 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 12 Oct 2021 20:25:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 20:25:54 GMT
EXPOSE 3000
# Tue, 12 Oct 2021 20:25:54 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee6af487f217efc8e231b9857a8031fdf07ab0c8b30e539497893ec5287578b`  
		Last Modified: Tue, 12 Oct 2021 15:39:48 GMT  
		Size: 12.6 MB (12565186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48bb8449b0384f7addf4ec5d88d8ef088e25ca52f9299c1fca4bff3f5b2411d`  
		Last Modified: Tue, 12 Oct 2021 15:39:46 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fbc3e5ccddf2ccfcc978381549c751e1167cdf41ce60580404b33cb6fdd7aa5`  
		Last Modified: Tue, 12 Oct 2021 15:41:15 GMT  
		Size: 21.5 MB (21467885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b99a224b661061fbbe799d6efb95f01221754e6a73aec4d536865d1e304d63`  
		Last Modified: Tue, 12 Oct 2021 15:41:12 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b92be01811211d262d0872aabc77c74589ad10e263a5d091b7a77fc657edd4`  
		Last Modified: Tue, 12 Oct 2021 20:28:12 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5866c61464640233522ebdc402ab1639ef563ce15f4e766f0d2c9c46dbf47749`  
		Last Modified: Tue, 12 Oct 2021 20:29:14 GMT  
		Size: 81.2 MB (81200401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14796236954476acf9820e11bdeba8b19f45bff173cce221292a37501351dbfa`  
		Last Modified: Tue, 12 Oct 2021 20:28:54 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f04093222ab3c15896fea65f4415539848dfd324ae9899f30a662a277b53939`  
		Last Modified: Tue, 12 Oct 2021 20:28:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b703fd11a89eae2882c03999cd46f929263f1a53e9db14fca0d3a22402e65899`  
		Last Modified: Tue, 12 Oct 2021 20:28:55 GMT  
		Size: 2.5 MB (2542547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4dc91c4594f36a6f07f59f99aea2b24d308de0799bab28a2877ed2b560cbbef`  
		Last Modified: Tue, 12 Oct 2021 20:29:05 GMT  
		Size: 60.2 MB (60159580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474e32e03341c2aa37028e650008f2aef23216356cb3099c1fdd66d1190edfd9`  
		Last Modified: Tue, 12 Oct 2021 20:28:54 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0.9` - linux; arm variant v5

```console
$ docker pull redmine@sha256:76bde531fa51e9043ec26a480294be0bf2afa573b89eb6eee1c363d9b0061dae
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194735396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a62e304aa3370634bf65d28936336cbe23efb8ac202b18443990b1dae175e34`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 12 Oct 2021 00:51:32 GMT
ADD file:0d95eee31ffe3f4260263e4fac2a61123a4b98d2e7a67efcc7bfea338c54f41d in / 
# Tue, 12 Oct 2021 00:51:32 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 06:45:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 06:45:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 06:45:07 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 07:20:58 GMT
ENV RUBY_MAJOR=2.6
# Tue, 12 Oct 2021 07:20:58 GMT
ENV RUBY_VERSION=2.6.8
# Tue, 12 Oct 2021 07:20:59 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Tue, 12 Oct 2021 07:25:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 07:25:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 07:25:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 07:25:31 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 07:25:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 07:25:33 GMT
CMD ["irb"]
# Wed, 13 Oct 2021 03:13:47 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 13 Oct 2021 03:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 03:23:43 GMT
ENV RAILS_ENV=production
# Wed, 13 Oct 2021 03:23:44 GMT
WORKDIR /usr/src/redmine
# Wed, 13 Oct 2021 03:23:45 GMT
ENV HOME=/home/redmine
# Wed, 13 Oct 2021 03:23:47 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 13 Oct 2021 03:23:47 GMT
ENV REDMINE_VERSION=4.0.9
# Wed, 13 Oct 2021 03:23:48 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Wed, 13 Oct 2021 03:23:53 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 13 Oct 2021 03:30:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 13 Oct 2021 03:30:52 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 13 Oct 2021 03:30:54 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 13 Oct 2021 03:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Oct 2021 03:30:56 GMT
EXPOSE 3000
# Wed, 13 Oct 2021 03:30:57 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:175b083b22fb061f7d1894fe4916a2967ce636d47376da526d90d57c8f7efc60`  
		Last Modified: Tue, 12 Oct 2021 01:07:45 GMT  
		Size: 24.9 MB (24872704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed73113a2340f22427741647a89a1911c6dd067bde17833928c5d210ab93918`  
		Last Modified: Tue, 12 Oct 2021 07:31:54 GMT  
		Size: 10.3 MB (10349314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7a78f939d570718e0af30429b3118d94e3800937a469b3fca591fda6d0540e`  
		Last Modified: Tue, 12 Oct 2021 07:31:46 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee56be0d198078cdceb927f259d279ea37548abbdefb95d8056e7e15d8137f0`  
		Last Modified: Tue, 12 Oct 2021 07:35:42 GMT  
		Size: 20.7 MB (20733372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e080526cffc142b881616db7396494f86cda539f9b9c65296f73498b8f70f81`  
		Last Modified: Tue, 12 Oct 2021 07:35:32 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c030517df14ac43613f1cd4bf516123c442ce7a9e6f545e593cc52a6b40fd301`  
		Last Modified: Wed, 13 Oct 2021 03:33:10 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d678b665817d824792999b8bfe1097e772d539be20d87a21b7856e05e68b96fa`  
		Last Modified: Wed, 13 Oct 2021 03:34:44 GMT  
		Size: 77.0 MB (76964464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6268c5fac0a25fcda1e7b6e81b957c6ec41cd2a5e036ed031571f4d6c58f6b24`  
		Last Modified: Wed, 13 Oct 2021 03:34:07 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbaf21e0e9c72ebe28c5f11acc6887fd712ea95c2cd076725f01a2e89180c497`  
		Last Modified: Wed, 13 Oct 2021 03:34:06 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9804dc5e809a3c7310004b9c8e2d88e4a5a96fc1b4478080c2e4d4ce0585657b`  
		Last Modified: Wed, 13 Oct 2021 03:34:09 GMT  
		Size: 2.5 MB (2542539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:045d5a7b6ab1fa20d89537dbdd96653f63725bc98e85e648b81062fe647ca6c2`  
		Last Modified: Wed, 13 Oct 2021 03:34:29 GMT  
		Size: 59.3 MB (59268769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f02d814ee294160e2f9f09d190a6ed3a13b32c93990b2cb5ca48e819f88596`  
		Last Modified: Wed, 13 Oct 2021 03:34:07 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0.9` - linux; arm variant v7

```console
$ docker pull redmine@sha256:a4c280bbf76f9bba2834f9064504ed314608d46e14f36ced5448faaa80a44bc1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.1 MB (188068236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e8a6d08e93ea1d782be23860355520573e87862ab0ee514e619646b9cb223e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 12 Oct 2021 01:29:42 GMT
ADD file:fe1eaa1b1d760b3d250cb4ac331d26a261fc569f1694bd34e146f00874dc87e5 in / 
# Tue, 12 Oct 2021 01:29:43 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 02:56:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 02:56:30 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 03:29:09 GMT
ENV RUBY_MAJOR=2.6
# Tue, 12 Oct 2021 03:29:10 GMT
ENV RUBY_VERSION=2.6.8
# Tue, 12 Oct 2021 03:29:10 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Tue, 12 Oct 2021 03:33:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 03:33:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 03:33:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 03:33:31 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 03:33:33 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 03:33:33 GMT
CMD ["irb"]
# Wed, 13 Oct 2021 06:41:32 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 13 Oct 2021 06:49:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 06:49:21 GMT
ENV RAILS_ENV=production
# Wed, 13 Oct 2021 06:49:22 GMT
WORKDIR /usr/src/redmine
# Wed, 13 Oct 2021 06:49:22 GMT
ENV HOME=/home/redmine
# Wed, 13 Oct 2021 06:49:24 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 13 Oct 2021 06:49:25 GMT
ENV REDMINE_VERSION=4.0.9
# Wed, 13 Oct 2021 06:49:25 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Wed, 13 Oct 2021 06:49:31 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 13 Oct 2021 06:55:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 13 Oct 2021 06:55:07 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 13 Oct 2021 06:55:08 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 13 Oct 2021 06:55:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Oct 2021 06:55:08 GMT
EXPOSE 3000
# Wed, 13 Oct 2021 06:55:09 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c0b5ba470cac8cfdae4633f5cddb3ba9350fe1d1b1507c4965a8224eb40e52c5`  
		Last Modified: Tue, 12 Oct 2021 01:45:52 GMT  
		Size: 22.7 MB (22739698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cdd321094894b78bc0792d96cf339ee9e4ce7ec18a14ea44b32cfbc809867b`  
		Last Modified: Tue, 12 Oct 2021 03:40:20 GMT  
		Size: 9.9 MB (9872904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c0e1a382b6eb02d552bdb97946d22f8b0d9b5f787b5d1b491fa3703e23d5ea`  
		Last Modified: Tue, 12 Oct 2021 03:40:13 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c9c99e0177bf2b2564708b982b9c36357cd8d40692351ae3fb607492c43c90`  
		Last Modified: Tue, 12 Oct 2021 03:42:55 GMT  
		Size: 20.6 MB (20643669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb852a3aed1bbfa0863f056cd080fad5debc62aefa369421cb364fde8137ebf`  
		Last Modified: Tue, 12 Oct 2021 03:42:48 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1086d0917a940899c5d3bad3fc3feea5fe65219a792b2acd69cd9ada062a7b`  
		Last Modified: Wed, 13 Oct 2021 06:57:14 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb023e9c4cb9847d03887a1e74509d1006934f33f168f7767fa3d0cfbb8993a`  
		Last Modified: Wed, 13 Oct 2021 06:59:10 GMT  
		Size: 73.3 MB (73263173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0734a96aee601c48b488de39bdd899a39839fbaefdc1985bc857df450c198d`  
		Last Modified: Wed, 13 Oct 2021 06:58:22 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0517f5edd505304a5cef2b06581a9ef09936a60ee7a42294579ea2c03b3d56ac`  
		Last Modified: Wed, 13 Oct 2021 06:58:22 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdcbad9cf302ea0ce760081905d9900133ec90ce11fd39b09fbdf9c488257498`  
		Last Modified: Wed, 13 Oct 2021 06:58:26 GMT  
		Size: 2.5 MB (2542549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd922d77362506a9ce9e94dd73d4abe3e913ecce129f542af606401d53107264`  
		Last Modified: Wed, 13 Oct 2021 06:58:51 GMT  
		Size: 59.0 MB (59002007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32dd7573f2ae3e4eba3c72bbaed2d55ca28ac46b39bac2a652358df5ca161b6c`  
		Last Modified: Wed, 13 Oct 2021 06:58:22 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0.9` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:e1640a145bf5840bf0b9e2ab84e9d93a0d24a18ed393b43f6be7a2f7b18fce0a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.4 MB (200438417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd7ec9b45c45b3a02a7ee54c69afa603f673991915570396bea1f1457a0e750`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:31:02 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:46:01 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 09:46:02 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 09:46:03 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 09:48:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 09:48:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 09:48:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 09:48:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:48:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 09:48:06 GMT
CMD ["irb"]
# Wed, 17 Nov 2021 19:49:55 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 17 Nov 2021 19:53:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 19:53:13 GMT
ENV RAILS_ENV=production
# Wed, 17 Nov 2021 19:53:14 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Nov 2021 19:53:15 GMT
ENV HOME=/home/redmine
# Wed, 17 Nov 2021 19:53:16 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 17 Nov 2021 19:53:17 GMT
ENV REDMINE_VERSION=4.0.9
# Wed, 17 Nov 2021 19:53:18 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Wed, 17 Nov 2021 19:53:22 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 17 Nov 2021 19:55:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 19:55:45 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Nov 2021 19:55:46 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 17 Nov 2021 19:55:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 19:55:47 GMT
EXPOSE 3000
# Wed, 17 Nov 2021 19:55:48 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8443a8ec909433d7156b8dcbeaf77f4e53d6a44b253a3f03b95126547154d55`  
		Last Modified: Wed, 17 Nov 2021 09:51:43 GMT  
		Size: 11.3 MB (11261808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f57122fa0ffe176f788d35a4a8f12a76819fa3bab198ac16e26d2961047a1d`  
		Last Modified: Wed, 17 Nov 2021 09:51:41 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16912dae180f72843a7e6b7dd25071e1090943354879adab903dcd984c8cee67`  
		Last Modified: Wed, 17 Nov 2021 09:54:26 GMT  
		Size: 21.1 MB (21095263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b73b9ee9aa5f816c4fb7665c7e19fe1663007ac1aacb74064aac56ece594983`  
		Last Modified: Wed, 17 Nov 2021 09:54:23 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb50985615235593da91e201ffe4b1db40feab50ab0a12b02a4c99191da4dfd`  
		Last Modified: Wed, 17 Nov 2021 19:57:02 GMT  
		Size: 1.6 KB (1625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde74bffacc846943dfa6d226151f2242bb938be3ad44c6dcdd0dae1d33a42b3`  
		Last Modified: Wed, 17 Nov 2021 19:57:42 GMT  
		Size: 79.8 MB (79758991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279493fe0772df535c0878e63b1b64fba2b226e69a69fe151989981e2e059753`  
		Last Modified: Wed, 17 Nov 2021 19:57:28 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55b03979292e18cc4dce62c30e68343071ed1073cddd16a31506b6a78a29155`  
		Last Modified: Wed, 17 Nov 2021 19:57:28 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd290e4917e62816eb06bb5841ee9c059f8d44144cff4fa97a200732d285904`  
		Last Modified: Wed, 17 Nov 2021 19:57:29 GMT  
		Size: 2.5 MB (2543981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23fdce25f1a772528d0357b38e56069cd549aa907ba49f53e6cbac362540eeef`  
		Last Modified: Wed, 17 Nov 2021 19:57:37 GMT  
		Size: 59.9 MB (59851226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa0e7224f51928ab8db5b08f76b818cc36d597e64ea832546f26380efc40f02`  
		Last Modified: Wed, 17 Nov 2021 19:57:28 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0.9` - linux; 386

```console
$ docker pull redmine@sha256:f1fe73108e092e98101c8561db5f30df576481a8663f6260f48c5d493362fc1e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210347648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2a96bb39dd0f782181d9ca3c863004466bb821cd3f4eacfd701fa18b69ab5e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 18:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 18:38:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 18:38:25 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 19:07:29 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 19:07:29 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 19:07:29 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 19:11:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 19:11:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 19:11:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 19:12:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 19:12:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 19:12:01 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 00:37:59 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 00:40:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 00:40:06 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 00:40:06 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 00:40:06 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 00:40:08 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 00:40:08 GMT
ENV REDMINE_VERSION=4.0.9
# Thu, 18 Nov 2021 00:40:08 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Thu, 18 Nov 2021 00:40:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 00:42:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 00:42:32 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 00:42:33 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 00:42:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 00:42:33 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 00:42:33 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1742b7e5e1e5bca675e7f251c9f6fe8778a1bb1548e5b418f8547277f14e2e33`  
		Last Modified: Wed, 17 Nov 2021 19:17:19 GMT  
		Size: 17.2 MB (17227026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ef5459771b89c49219d5c15641c7215faf156712422f01efee40ad955a52c5`  
		Last Modified: Wed, 17 Nov 2021 19:17:10 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8e5a4df5a8f121515c23ab2e470f17d64c6bb138b6c22dda592fcde5393ca4`  
		Last Modified: Wed, 17 Nov 2021 19:20:39 GMT  
		Size: 20.9 MB (20910059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955765ea073687d915724497fa422005e56011fcf7d74483d30fd502a0ae1992`  
		Last Modified: Wed, 17 Nov 2021 19:20:35 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114a479d47bf9ce3b07ffb880a448300b978f0dd2fb9b2cf257248dd29de5e84`  
		Last Modified: Thu, 18 Nov 2021 00:44:01 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7da47a96d23e66f0e9def04a7192dde8c3f9cd839282fda3efd121d97eda435`  
		Last Modified: Thu, 18 Nov 2021 00:45:17 GMT  
		Size: 82.6 MB (82599710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1928f566c831a396b46d1da2e213d7e2a8e77a2d900040af95c718d58cba7f60`  
		Last Modified: Thu, 18 Nov 2021 00:44:47 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a6707cbab4ac55df2d2037e249005c67725357318531f7673e1887b17fb300`  
		Last Modified: Thu, 18 Nov 2021 00:44:47 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d499e312e0f51e9de1e154f0944c20e8865d7114738e8b3ad6a65b07e1ce555`  
		Last Modified: Thu, 18 Nov 2021 00:44:49 GMT  
		Size: 2.5 MB (2542545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c34f6b79c0664ea6304fa45c671cc8239eba56a967c5c3f474672d335c96b7a`  
		Last Modified: Thu, 18 Nov 2021 00:45:03 GMT  
		Size: 59.3 MB (59259521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d6247c6cc7f7721a644ff15bf4633ab39ca26e5094d60356b696840bda35ec`  
		Last Modified: Thu, 18 Nov 2021 00:44:47 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0.9` - linux; ppc64le

```console
$ docker pull redmine@sha256:6aac498c44f600b672d9897703c3c41b214924e3fc233e7860fd8e545b136e77
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216469674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4da6045a34b42bbefc251f10d5f010773a1e6f3bcfc1555ea6958d409fbead`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 12 Oct 2021 01:26:46 GMT
ADD file:5526880c6f19a4b4231a8b2bd7cfc625d116764c4918eff6f0b55f8c1eb38e1a in / 
# Tue, 12 Oct 2021 01:26:50 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 18:23:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 18:24:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 18:24:11 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 19:17:28 GMT
ENV RUBY_MAJOR=2.6
# Tue, 12 Oct 2021 19:17:32 GMT
ENV RUBY_VERSION=2.6.8
# Tue, 12 Oct 2021 19:17:38 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Tue, 12 Oct 2021 19:25:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 19:25:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 19:26:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 19:26:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 19:26:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 19:26:22 GMT
CMD ["irb"]
# Thu, 14 Oct 2021 00:54:05 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 14 Oct 2021 01:07:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 Oct 2021 01:08:11 GMT
ENV RAILS_ENV=production
# Thu, 14 Oct 2021 01:08:23 GMT
WORKDIR /usr/src/redmine
# Thu, 14 Oct 2021 01:08:27 GMT
ENV HOME=/home/redmine
# Thu, 14 Oct 2021 01:08:42 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 14 Oct 2021 01:08:47 GMT
ENV REDMINE_VERSION=4.0.9
# Thu, 14 Oct 2021 01:08:56 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Thu, 14 Oct 2021 01:09:18 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 14 Oct 2021 01:19:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 Oct 2021 01:19:19 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 14 Oct 2021 01:19:23 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 14 Oct 2021 01:19:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Oct 2021 01:19:47 GMT
EXPOSE 3000
# Thu, 14 Oct 2021 01:19:52 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d69973af32573c07c8789c0f9c144a5c0b822a1e85b59db3ce9f8ebc489ce85d`  
		Last Modified: Tue, 12 Oct 2021 01:38:40 GMT  
		Size: 30.5 MB (30547197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f48a596ad1fccd3e24dcc1f65e362937ced6f5b5ab61b6eb49e8eda8a55b85`  
		Last Modified: Tue, 12 Oct 2021 19:30:52 GMT  
		Size: 12.7 MB (12705483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd72e7e6250a90b152d1d27efca928b2c1bfc949dfe1b2e9cf089acde024c098`  
		Last Modified: Tue, 12 Oct 2021 19:30:49 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03211df41d3c61789be71d89ebad2ce881638fb2a84c27562d7e3ff81f181458`  
		Last Modified: Tue, 12 Oct 2021 19:33:41 GMT  
		Size: 22.0 MB (21984973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c774747b6862c16e290d0508df2db39d1a24d4061e198d3567c877d14ca4bf8`  
		Last Modified: Tue, 12 Oct 2021 19:33:38 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d344e083cdb889978f1a8f40a20c569e9d02d096352f103edc1381edd38d39a`  
		Last Modified: Thu, 14 Oct 2021 01:22:07 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac438230a35738c21d025cb57c8c2c12a0694fc9dcafd9d3f1f1cc5d52cac12`  
		Last Modified: Thu, 14 Oct 2021 01:22:55 GMT  
		Size: 87.9 MB (87902632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96411f53dc60a5c0667e24e7007ead33f7a43d92b6c882aa193e719f58ed663`  
		Last Modified: Thu, 14 Oct 2021 01:22:36 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2634382c5d445a0bba90dc55ead78291350aad0aa956fe9f87bbaa4f73cdfed`  
		Last Modified: Thu, 14 Oct 2021 01:22:37 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e17f74adf31cae17cfb0a926e812563f2f59c5c7778cc5f8d84e26e09015218`  
		Last Modified: Thu, 14 Oct 2021 01:22:37 GMT  
		Size: 2.5 MB (2542548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce9fa655873ae250f6f495e0d5433626b0bba0c00566e89e82fcadc94703ea4`  
		Last Modified: Thu, 14 Oct 2021 01:22:45 GMT  
		Size: 60.8 MB (60782595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df59993b68006e819fad6adcd54c3e76dc6dc32f43f6b365d3a69aa8e22b1b35`  
		Last Modified: Thu, 14 Oct 2021 01:22:36 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0.9` - linux; s390x

```console
$ docker pull redmine@sha256:7a08ebb93b3b03597bf02476a2515778130f7bff1e3c33e8fcc00a1073ccfc31
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.3 MB (200291030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9aaeccdc23c9bbd5bb63a74995e35e24d80ec599e61878f1a15ad2fa1e82ea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:42:59 GMT
ADD file:3ff5fbc9c53cf76aad0fe0e1a525cb0bc0d70e8f2a3d5741dfb8b3b8a9448ffd in / 
# Wed, 17 Nov 2021 02:43:00 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:21:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:21:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:21:07 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:42:36 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 09:42:36 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 09:42:37 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 09:44:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 09:44:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 09:44:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 09:44:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:44:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 09:44:07 GMT
CMD ["irb"]
# Wed, 17 Nov 2021 20:34:19 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 17 Nov 2021 20:36:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:37:01 GMT
ENV RAILS_ENV=production
# Wed, 17 Nov 2021 20:37:01 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Nov 2021 20:37:01 GMT
ENV HOME=/home/redmine
# Wed, 17 Nov 2021 20:37:02 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 17 Nov 2021 20:37:02 GMT
ENV REDMINE_VERSION=4.0.9
# Wed, 17 Nov 2021 20:37:02 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Wed, 17 Nov 2021 20:37:04 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 17 Nov 2021 20:38:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 20:38:46 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Nov 2021 20:38:46 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 17 Nov 2021 20:38:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 20:38:46 GMT
EXPOSE 3000
# Wed, 17 Nov 2021 20:38:46 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b8b917e61b3be882db10e68210f73caf5cc788bfb07aec0a659e30f4796b476b`  
		Last Modified: Wed, 17 Nov 2021 02:49:01 GMT  
		Size: 25.8 MB (25769063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e574c6d046371657ec033b78bc3df865890056f711b30df7505d0128446e36`  
		Last Modified: Wed, 17 Nov 2021 09:48:11 GMT  
		Size: 10.8 MB (10815243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6bfb1613df50da70222f9b1cd395c4b509f6e6631cf6a13ce6c6b9c8c4cf181`  
		Last Modified: Wed, 17 Nov 2021 09:48:09 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37bdaf56dd9686cdaca63c3c8ebab2d6841412a36159619d65853daa75500716`  
		Last Modified: Wed, 17 Nov 2021 09:51:17 GMT  
		Size: 21.6 MB (21619852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80433d0a1bacd8eb06bb301d366ea459dbae5ce9a2bea94372bd52e0939584a0`  
		Last Modified: Wed, 17 Nov 2021 09:51:15 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e82306e7113526e6aa75620a186091a8a2139c7e63336bc2033df0329cda36e`  
		Last Modified: Wed, 17 Nov 2021 20:39:48 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085d5f5c7261748f638b0c30c5922b96cc7a7139c94d116b31323b1fe50f715c`  
		Last Modified: Wed, 17 Nov 2021 20:40:19 GMT  
		Size: 78.9 MB (78941825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdafcf9171e45387b8e26650c032636412a64ea71a82beb8da9aaadda5a038a`  
		Last Modified: Wed, 17 Nov 2021 20:40:08 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd65e98466ef8280e1eac2c5693840a60cd00682e5bbdafe9bde2b47edd7275`  
		Last Modified: Wed, 17 Nov 2021 20:40:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25e48155420ae67e64e5329514da95aeea977ad3762dff4bc8baacdb80a3058`  
		Last Modified: Wed, 17 Nov 2021 20:40:08 GMT  
		Size: 2.5 MB (2542547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d56cd02bb76bc97344bf358dd1335582e1460a561ab33d1c8dab2a5c27c2f66e`  
		Last Modified: Wed, 17 Nov 2021 20:40:14 GMT  
		Size: 60.6 MB (60598255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05981b15aac91be53d29f32192b2ad7af008afe472c8d7aab11db0049c3de996`  
		Last Modified: Wed, 17 Nov 2021 20:40:08 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.0.9-alpine`

```console
$ docker pull redmine@sha256:fa8ba213e2dfef7bfb98c3b2ca6af9917a9c0b9b15be67bb8c20499ac3d04aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.0.9-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:01887efbc27065bcc544e6ba80201b994e89e27280c7b25de2c280d6f1b33024
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.6 MB (153558063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4abb35ae9e45f8c5510f9bfe3efa808d3e893645c29b1b6aa08bae910bf2aa9a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:28:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Sat, 13 Nov 2021 06:28:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 13 Nov 2021 06:28:18 GMT
ENV LANG=C.UTF-8
# Sat, 13 Nov 2021 06:51:30 GMT
ENV RUBY_MAJOR=2.6
# Sat, 13 Nov 2021 06:51:30 GMT
ENV RUBY_VERSION=2.6.8
# Sat, 13 Nov 2021 06:51:31 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Sat, 13 Nov 2021 06:54:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 13 Nov 2021 06:54:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 13 Nov 2021 06:54:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 13 Nov 2021 06:54:45 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Nov 2021 06:54:45 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 13 Nov 2021 06:54:46 GMT
CMD ["irb"]
# Sat, 13 Nov 2021 14:31:40 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 13 Nov 2021 14:34:28 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				git 		mercurial 		openssh-client 		subversion 				ghostscript-fonts 		imagemagick6 	;
# Sat, 13 Nov 2021 14:34:29 GMT
ENV RAILS_ENV=production
# Sat, 13 Nov 2021 14:34:29 GMT
WORKDIR /usr/src/redmine
# Sat, 13 Nov 2021 14:34:29 GMT
ENV HOME=/home/redmine
# Sat, 13 Nov 2021 14:34:30 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 13 Nov 2021 14:34:30 GMT
ENV REDMINE_VERSION=4.0.9
# Sat, 13 Nov 2021 14:34:30 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Sat, 13 Nov 2021 14:34:34 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 13 Nov 2021 14:34:34 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 13 Nov 2021 14:36:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 		imagemagick6-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 13 Nov 2021 14:36:07 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 13 Nov 2021 14:36:07 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Sat, 13 Nov 2021 14:36:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Nov 2021 14:36:07 GMT
EXPOSE 3000
# Sat, 13 Nov 2021 14:36:08 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86e849bc66e37f2d898daa44d76330256a48635f1100e364c0f46206fca7b71`  
		Last Modified: Sat, 13 Nov 2021 06:56:48 GMT  
		Size: 3.6 MB (3582307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a2fc84ba5b32bce31936a6fdf8121f29d2eb485f8525795df7d32046e9f856`  
		Last Modified: Sat, 13 Nov 2021 06:56:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fd76747f3be3e4f4af1119b668fd5a9fa53725f84b429575cfb26c0d5f842a`  
		Last Modified: Sat, 13 Nov 2021 06:59:00 GMT  
		Size: 19.5 MB (19500293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bbfb1229cd3c27d4dd990a0daf591e427afbc679b854303415a9e9a01ff10b`  
		Last Modified: Sat, 13 Nov 2021 06:58:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c267c2d73515a2e4fbaac349e5a31212348b7d72b21f80611dac1923c5c68666`  
		Last Modified: Sat, 13 Nov 2021 14:37:15 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7ea963f3d5877eea0043f8a2b75f17680ff5a4d362c1a4fce8c8a67c347239`  
		Last Modified: Sat, 13 Nov 2021 14:37:49 GMT  
		Size: 66.2 MB (66199469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05071f335bb9135d55d21c80aaa3523ae388d93f1a98136404e7c91fa99fb524`  
		Last Modified: Sat, 13 Nov 2021 14:37:37 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a43db45233bb37a8a7df21efee11df06d119f141dd51e3c8672893a9bb6a654`  
		Last Modified: Sat, 13 Nov 2021 14:37:37 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb71bc10f9decb3a165b48fa2dae4aa79929b41c812f261a1ff1fee173510e8`  
		Last Modified: Sat, 13 Nov 2021 14:37:38 GMT  
		Size: 2.5 MB (2543762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d38dd936d4bdfa095bb3270305cfe38c97043649fdf48ba25879b221ebbb40`  
		Last Modified: Sat, 13 Nov 2021 14:37:43 GMT  
		Size: 58.9 MB (58906080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ac236fd681e485d4f3495d7195078b72db1997782784f2aca237835c80c236`  
		Last Modified: Sat, 13 Nov 2021 14:37:37 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.0.9-passenger`

```console
$ docker pull redmine@sha256:8f5dc49e7e8b0e12174df5fa85995971245c971765697ba9c8d5dfedbf1181c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.0.9-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:ab67f320b1123ca1304a82c786eae4039d20fd4c88b83296db005396040c20c2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231443403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f098d154d4397a6cf6ab16cf24d877414f42e3f0e229c0f85ebbc51d47fc41`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:20:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:20:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 15:20:38 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 15:34:09 GMT
ENV RUBY_MAJOR=2.6
# Tue, 12 Oct 2021 15:34:09 GMT
ENV RUBY_VERSION=2.6.8
# Tue, 12 Oct 2021 15:34:09 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Tue, 12 Oct 2021 15:37:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 15:37:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 15:37:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 15:37:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 15:37:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 15:37:06 GMT
CMD ["irb"]
# Tue, 12 Oct 2021 20:20:16 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 12 Oct 2021 20:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 20:23:19 GMT
ENV RAILS_ENV=production
# Tue, 12 Oct 2021 20:23:20 GMT
WORKDIR /usr/src/redmine
# Tue, 12 Oct 2021 20:23:20 GMT
ENV HOME=/home/redmine
# Tue, 12 Oct 2021 20:23:21 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 12 Oct 2021 20:23:21 GMT
ENV REDMINE_VERSION=4.0.9
# Tue, 12 Oct 2021 20:23:21 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Tue, 12 Oct 2021 20:23:25 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 12 Oct 2021 20:25:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Oct 2021 20:25:53 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 12 Oct 2021 20:25:54 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 12 Oct 2021 20:25:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 20:25:54 GMT
EXPOSE 3000
# Tue, 12 Oct 2021 20:25:54 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Wed, 10 Nov 2021 03:47:10 GMT
ENV PASSENGER_VERSION=6.0.12
# Wed, 10 Nov 2021 03:47:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 10 Nov 2021 03:47:29 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Wed, 10 Nov 2021 03:47:29 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Wed, 10 Nov 2021 03:47:29 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee6af487f217efc8e231b9857a8031fdf07ab0c8b30e539497893ec5287578b`  
		Last Modified: Tue, 12 Oct 2021 15:39:48 GMT  
		Size: 12.6 MB (12565186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48bb8449b0384f7addf4ec5d88d8ef088e25ca52f9299c1fca4bff3f5b2411d`  
		Last Modified: Tue, 12 Oct 2021 15:39:46 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fbc3e5ccddf2ccfcc978381549c751e1167cdf41ce60580404b33cb6fdd7aa5`  
		Last Modified: Tue, 12 Oct 2021 15:41:15 GMT  
		Size: 21.5 MB (21467885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b99a224b661061fbbe799d6efb95f01221754e6a73aec4d536865d1e304d63`  
		Last Modified: Tue, 12 Oct 2021 15:41:12 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b92be01811211d262d0872aabc77c74589ad10e263a5d091b7a77fc657edd4`  
		Last Modified: Tue, 12 Oct 2021 20:28:12 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5866c61464640233522ebdc402ab1639ef563ce15f4e766f0d2c9c46dbf47749`  
		Last Modified: Tue, 12 Oct 2021 20:29:14 GMT  
		Size: 81.2 MB (81200401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14796236954476acf9820e11bdeba8b19f45bff173cce221292a37501351dbfa`  
		Last Modified: Tue, 12 Oct 2021 20:28:54 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f04093222ab3c15896fea65f4415539848dfd324ae9899f30a662a277b53939`  
		Last Modified: Tue, 12 Oct 2021 20:28:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b703fd11a89eae2882c03999cd46f929263f1a53e9db14fca0d3a22402e65899`  
		Last Modified: Tue, 12 Oct 2021 20:28:55 GMT  
		Size: 2.5 MB (2542547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4dc91c4594f36a6f07f59f99aea2b24d308de0799bab28a2877ed2b560cbbef`  
		Last Modified: Tue, 12 Oct 2021 20:29:05 GMT  
		Size: 60.2 MB (60159580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474e32e03341c2aa37028e650008f2aef23216356cb3099c1fdd66d1190edfd9`  
		Last Modified: Tue, 12 Oct 2021 20:28:54 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d8b5222950710a3689bed3c7d25c043a60ee6308b734dd7e9e3fb1cd20aecf`  
		Last Modified: Wed, 10 Nov 2021 03:48:45 GMT  
		Size: 21.4 MB (21439436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0429cf4f74ed45039bbed5c5f537f08b624eb8bd977152cd098f2b290c2c5dd0`  
		Last Modified: Wed, 10 Nov 2021 03:48:43 GMT  
		Size: 4.9 MB (4924616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.1`

```console
$ docker pull redmine@sha256:63e3ffff6262d8d63a9062c1ac7221b81c87b96a1d910080fc40f04e067bfe90
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

### `redmine:4.1` - linux; amd64

```console
$ docker pull redmine@sha256:403c93eb007bd16cd277e19fc1459f180c7483fa4940fd5044a30acef53a8f01
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.7 MB (206668627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0da7de9c6f21204eac2ef99bfd1d097808059ad4f8daeb89898eb83deffb97c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:20:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:20:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 15:20:38 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 15:34:09 GMT
ENV RUBY_MAJOR=2.6
# Tue, 12 Oct 2021 15:34:09 GMT
ENV RUBY_VERSION=2.6.8
# Tue, 12 Oct 2021 15:34:09 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Tue, 12 Oct 2021 15:37:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 15:37:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 15:37:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 15:37:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 15:37:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 15:37:06 GMT
CMD ["irb"]
# Tue, 12 Oct 2021 20:20:16 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 12 Oct 2021 20:20:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 20:20:57 GMT
ENV RAILS_ENV=production
# Tue, 12 Oct 2021 20:20:57 GMT
WORKDIR /usr/src/redmine
# Tue, 12 Oct 2021 20:20:57 GMT
ENV HOME=/home/redmine
# Tue, 12 Oct 2021 20:20:59 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 12 Oct 2021 20:20:59 GMT
ENV REDMINE_VERSION=4.1.5
# Tue, 12 Oct 2021 20:20:59 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Tue, 12 Oct 2021 20:21:04 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 12 Oct 2021 20:22:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Oct 2021 20:22:14 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 12 Oct 2021 20:22:14 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 12 Oct 2021 20:22:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 20:22:15 GMT
EXPOSE 3000
# Tue, 12 Oct 2021 20:22:15 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee6af487f217efc8e231b9857a8031fdf07ab0c8b30e539497893ec5287578b`  
		Last Modified: Tue, 12 Oct 2021 15:39:48 GMT  
		Size: 12.6 MB (12565186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48bb8449b0384f7addf4ec5d88d8ef088e25ca52f9299c1fca4bff3f5b2411d`  
		Last Modified: Tue, 12 Oct 2021 15:39:46 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fbc3e5ccddf2ccfcc978381549c751e1167cdf41ce60580404b33cb6fdd7aa5`  
		Last Modified: Tue, 12 Oct 2021 15:41:15 GMT  
		Size: 21.5 MB (21467885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b99a224b661061fbbe799d6efb95f01221754e6a73aec4d536865d1e304d63`  
		Last Modified: Tue, 12 Oct 2021 15:41:12 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b92be01811211d262d0872aabc77c74589ad10e263a5d091b7a77fc657edd4`  
		Last Modified: Tue, 12 Oct 2021 20:28:12 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8617ac0503291a7bc25ab3e9ecadad7f36606e38768ec7dae57decbca32bc1ea`  
		Last Modified: Tue, 12 Oct 2021 20:28:29 GMT  
		Size: 94.1 MB (94088241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a76df102ee332891a671c026db6214352f68c057230bbdae139ea2227fe745`  
		Last Modified: Tue, 12 Oct 2021 20:28:10 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f353dd18278378e4d8216c008d56bc846a5a701d5a7730f60698a69cc659c8b`  
		Last Modified: Tue, 12 Oct 2021 20:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0888176d4f29df43b84ccec41ac92479f77bee993d76d41344d933ff075acec4`  
		Last Modified: Tue, 12 Oct 2021 20:28:11 GMT  
		Size: 2.7 MB (2749692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7edea4661341065395429e13204ddb02ce8e2608365b08a4b649071683624d43`  
		Last Modified: Tue, 12 Oct 2021 20:28:17 GMT  
		Size: 48.7 MB (48653871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3811deb43f4603834d18cf1fe5b28601cc92f816a4dbc984fe9858936d4f44a3`  
		Last Modified: Tue, 12 Oct 2021 20:28:10 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1` - linux; arm variant v5

```console
$ docker pull redmine@sha256:fd9a6ca83808905c079ff29662f81bb35330a8be3abbc339c2507c971852ea3b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.7 MB (210669047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fb4a19021b4eeca711ee785701e0df1d7d03e3e0871a30ad557c336a06e2ef`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 12 Oct 2021 00:51:32 GMT
ADD file:0d95eee31ffe3f4260263e4fac2a61123a4b98d2e7a67efcc7bfea338c54f41d in / 
# Tue, 12 Oct 2021 00:51:32 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 06:45:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 06:45:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 06:45:07 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 07:20:58 GMT
ENV RUBY_MAJOR=2.6
# Tue, 12 Oct 2021 07:20:58 GMT
ENV RUBY_VERSION=2.6.8
# Tue, 12 Oct 2021 07:20:59 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Tue, 12 Oct 2021 07:25:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 07:25:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 07:25:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 07:25:31 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 07:25:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 07:25:33 GMT
CMD ["irb"]
# Wed, 13 Oct 2021 03:13:47 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 13 Oct 2021 03:15:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 03:15:19 GMT
ENV RAILS_ENV=production
# Wed, 13 Oct 2021 03:15:21 GMT
WORKDIR /usr/src/redmine
# Wed, 13 Oct 2021 03:15:22 GMT
ENV HOME=/home/redmine
# Wed, 13 Oct 2021 03:15:27 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 13 Oct 2021 03:15:28 GMT
ENV REDMINE_VERSION=4.1.5
# Wed, 13 Oct 2021 03:15:29 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Wed, 13 Oct 2021 03:15:39 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 13 Oct 2021 03:22:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 13 Oct 2021 03:22:12 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 13 Oct 2021 03:22:13 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 13 Oct 2021 03:22:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Oct 2021 03:22:15 GMT
EXPOSE 3000
# Wed, 13 Oct 2021 03:22:16 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:175b083b22fb061f7d1894fe4916a2967ce636d47376da526d90d57c8f7efc60`  
		Last Modified: Tue, 12 Oct 2021 01:07:45 GMT  
		Size: 24.9 MB (24872704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed73113a2340f22427741647a89a1911c6dd067bde17833928c5d210ab93918`  
		Last Modified: Tue, 12 Oct 2021 07:31:54 GMT  
		Size: 10.3 MB (10349314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7a78f939d570718e0af30429b3118d94e3800937a469b3fca591fda6d0540e`  
		Last Modified: Tue, 12 Oct 2021 07:31:46 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee56be0d198078cdceb927f259d279ea37548abbdefb95d8056e7e15d8137f0`  
		Last Modified: Tue, 12 Oct 2021 07:35:42 GMT  
		Size: 20.7 MB (20733372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e080526cffc142b881616db7396494f86cda539f9b9c65296f73498b8f70f81`  
		Last Modified: Tue, 12 Oct 2021 07:35:32 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c030517df14ac43613f1cd4bf516123c442ce7a9e6f545e593cc52a6b40fd301`  
		Last Modified: Wed, 13 Oct 2021 03:33:10 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3897ec5e588606be8744330bf1c4d14efe3cb454ad1a7a28841648516085a681`  
		Last Modified: Wed, 13 Oct 2021 03:33:53 GMT  
		Size: 89.6 MB (89575164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14263ed54825c7939921f07b976fdeb8d1030283ae7629fb3cad48bcad63ef8b`  
		Last Modified: Wed, 13 Oct 2021 03:33:09 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42977913dd4d9c9fc4f9bbe0ec0c1cf86191be9b169e4625fd52638bd2d6990`  
		Last Modified: Wed, 13 Oct 2021 03:33:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fc078b0610e878e98fe32bd23535bba23460228cdb6d1c9342420cc1056fb1`  
		Last Modified: Wed, 13 Oct 2021 03:33:11 GMT  
		Size: 2.7 MB (2749695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8435301d2e3e6d0eb02ef7f3dfef10b39d778154c1dbca332274b48b117a3a9e`  
		Last Modified: Wed, 13 Oct 2021 03:33:31 GMT  
		Size: 62.4 MB (62384562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b775033255d5a1a789c784df094106b9b2489c0a159ff5d254d4e9c670b6084f`  
		Last Modified: Wed, 13 Oct 2021 03:33:09 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1` - linux; arm variant v7

```console
$ docker pull redmine@sha256:380b2a1bd20ab586d27fccfa9e704b5711d53271b5ae1ea0b553d0dff129aa5f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203851889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a22805d3ff7605300793419e632f413f2e1715dc0ccaf9dc46bb5cff553b7b9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 12 Oct 2021 01:29:42 GMT
ADD file:fe1eaa1b1d760b3d250cb4ac331d26a261fc569f1694bd34e146f00874dc87e5 in / 
# Tue, 12 Oct 2021 01:29:43 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 02:56:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 02:56:30 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 03:29:09 GMT
ENV RUBY_MAJOR=2.6
# Tue, 12 Oct 2021 03:29:10 GMT
ENV RUBY_VERSION=2.6.8
# Tue, 12 Oct 2021 03:29:10 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Tue, 12 Oct 2021 03:33:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 03:33:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 03:33:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 03:33:31 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 03:33:33 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 03:33:33 GMT
CMD ["irb"]
# Wed, 13 Oct 2021 06:41:32 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 13 Oct 2021 06:42:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 06:42:35 GMT
ENV RAILS_ENV=production
# Wed, 13 Oct 2021 06:42:36 GMT
WORKDIR /usr/src/redmine
# Wed, 13 Oct 2021 06:42:36 GMT
ENV HOME=/home/redmine
# Wed, 13 Oct 2021 06:42:38 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 13 Oct 2021 06:42:38 GMT
ENV REDMINE_VERSION=4.1.5
# Wed, 13 Oct 2021 06:42:39 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Wed, 13 Oct 2021 06:42:47 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 13 Oct 2021 06:48:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 13 Oct 2021 06:48:02 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 13 Oct 2021 06:48:03 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 13 Oct 2021 06:48:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Oct 2021 06:48:04 GMT
EXPOSE 3000
# Wed, 13 Oct 2021 06:48:04 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c0b5ba470cac8cfdae4633f5cddb3ba9350fe1d1b1507c4965a8224eb40e52c5`  
		Last Modified: Tue, 12 Oct 2021 01:45:52 GMT  
		Size: 22.7 MB (22739698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cdd321094894b78bc0792d96cf339ee9e4ce7ec18a14ea44b32cfbc809867b`  
		Last Modified: Tue, 12 Oct 2021 03:40:20 GMT  
		Size: 9.9 MB (9872904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c0e1a382b6eb02d552bdb97946d22f8b0d9b5f787b5d1b491fa3703e23d5ea`  
		Last Modified: Tue, 12 Oct 2021 03:40:13 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c9c99e0177bf2b2564708b982b9c36357cd8d40692351ae3fb607492c43c90`  
		Last Modified: Tue, 12 Oct 2021 03:42:55 GMT  
		Size: 20.6 MB (20643669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb852a3aed1bbfa0863f056cd080fad5debc62aefa369421cb364fde8137ebf`  
		Last Modified: Tue, 12 Oct 2021 03:42:48 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1086d0917a940899c5d3bad3fc3feea5fe65219a792b2acd69cd9ada062a7b`  
		Last Modified: Wed, 13 Oct 2021 06:57:14 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd9f426d70a745f2ddce33d8ac46330d64fcbed546853bad59d21f3534ca535`  
		Last Modified: Wed, 13 Oct 2021 06:58:10 GMT  
		Size: 85.6 MB (85590404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa3942a6e72dd3e213cd5889c3c17e56b4b1ff4c59a01feeab202d71714b219`  
		Last Modified: Wed, 13 Oct 2021 06:57:12 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706f62754dfee343ce1dbe89f0c2c61bc69c76aaabdfeec1b1dbb316c723f046`  
		Last Modified: Wed, 13 Oct 2021 06:57:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3afaba210f3f7cccc352f3a2bfb91fcfe93bbc146f42e038f0bf03d42a628754`  
		Last Modified: Wed, 13 Oct 2021 06:57:16 GMT  
		Size: 2.7 MB (2749696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e3e7f892fb877ae9658d4cf0c4c042302426527d05083af6384970cbeb8c12`  
		Last Modified: Wed, 13 Oct 2021 06:57:41 GMT  
		Size: 62.3 MB (62251280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a5677793c6ff5ebcc5d032b27aaef548b1be3fd53835a226127d26743d3d34`  
		Last Modified: Wed, 13 Oct 2021 06:57:13 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:b222b2102035ba87c72076afd3f971a910dd6cfa4627c0423b876748b40dea1e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.4 MB (216401827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871b1f794b4d0fcb638c8a57721a72acc701c347e2e647a928da47a7dc1c8c9c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:31:02 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:46:01 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 09:46:02 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 09:46:03 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 09:48:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 09:48:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 09:48:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 09:48:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:48:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 09:48:06 GMT
CMD ["irb"]
# Wed, 17 Nov 2021 19:49:55 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 17 Nov 2021 19:50:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 19:50:19 GMT
ENV RAILS_ENV=production
# Wed, 17 Nov 2021 19:50:20 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Nov 2021 19:50:21 GMT
ENV HOME=/home/redmine
# Wed, 17 Nov 2021 19:50:23 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 17 Nov 2021 19:50:23 GMT
ENV REDMINE_VERSION=4.1.5
# Wed, 17 Nov 2021 19:50:24 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Wed, 17 Nov 2021 19:50:28 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 17 Nov 2021 19:52:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 19:52:38 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Nov 2021 19:52:40 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 17 Nov 2021 19:52:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 19:52:41 GMT
EXPOSE 3000
# Wed, 17 Nov 2021 19:52:42 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8443a8ec909433d7156b8dcbeaf77f4e53d6a44b253a3f03b95126547154d55`  
		Last Modified: Wed, 17 Nov 2021 09:51:43 GMT  
		Size: 11.3 MB (11261808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f57122fa0ffe176f788d35a4a8f12a76819fa3bab198ac16e26d2961047a1d`  
		Last Modified: Wed, 17 Nov 2021 09:51:41 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16912dae180f72843a7e6b7dd25071e1090943354879adab903dcd984c8cee67`  
		Last Modified: Wed, 17 Nov 2021 09:54:26 GMT  
		Size: 21.1 MB (21095263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b73b9ee9aa5f816c4fb7665c7e19fe1663007ac1aacb74064aac56ece594983`  
		Last Modified: Wed, 17 Nov 2021 09:54:23 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb50985615235593da91e201ffe4b1db40feab50ab0a12b02a4c99191da4dfd`  
		Last Modified: Wed, 17 Nov 2021 19:57:02 GMT  
		Size: 1.6 KB (1625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b972b42f387b463ec4f85b98ff1de46778da88cde8db5210abd6cdb28fcfe996`  
		Last Modified: Wed, 17 Nov 2021 19:57:16 GMT  
		Size: 92.6 MB (92615309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d5c078974fd14c58f0b3b7716527a89b7fd62214cbd050a80d385982968927`  
		Last Modified: Wed, 17 Nov 2021 19:56:59 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302584afc613dd65a75b5bcda18ac7919a7c809a1df57148453b3f76954ed897`  
		Last Modified: Wed, 17 Nov 2021 19:56:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d073b657b29ddf797af445ca3996a8594b19899f364b2cc3d189f86a3fcf0deb`  
		Last Modified: Wed, 17 Nov 2021 19:57:00 GMT  
		Size: 2.7 MB (2749627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca343679f96ad8123399df85aad69f3174b5d405b2d11bf4804a0840974e2710`  
		Last Modified: Wed, 17 Nov 2021 19:57:10 GMT  
		Size: 62.8 MB (62752672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd1dcf76925b4813ce41dd25c0b93567defab250f8d74eac3e070f92b49c068`  
		Last Modified: Wed, 17 Nov 2021 19:56:59 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1` - linux; 386

```console
$ docker pull redmine@sha256:156a98e108ae32310750def5670b7f14ce4791c8fba4fc62b4389d126421ee10
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212332382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b8c8954f2416156578d6b917f84622fb2feacefa48597e8b97e216b5700b97`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 18:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 18:38:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 18:38:25 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 19:07:29 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 19:07:29 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 19:07:29 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 19:11:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 19:11:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 19:11:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 19:12:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 19:12:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 19:12:01 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 00:37:59 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 00:38:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 00:38:32 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 00:38:33 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 00:38:33 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 00:38:34 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 00:38:34 GMT
ENV REDMINE_VERSION=4.1.5
# Thu, 18 Nov 2021 00:38:34 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Thu, 18 Nov 2021 00:38:39 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 00:39:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 00:39:29 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 00:39:29 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 00:39:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 00:39:30 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 00:39:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1742b7e5e1e5bca675e7f251c9f6fe8778a1bb1548e5b418f8547277f14e2e33`  
		Last Modified: Wed, 17 Nov 2021 19:17:19 GMT  
		Size: 17.2 MB (17227026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ef5459771b89c49219d5c15641c7215faf156712422f01efee40ad955a52c5`  
		Last Modified: Wed, 17 Nov 2021 19:17:10 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8e5a4df5a8f121515c23ab2e470f17d64c6bb138b6c22dda592fcde5393ca4`  
		Last Modified: Wed, 17 Nov 2021 19:20:39 GMT  
		Size: 20.9 MB (20910059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955765ea073687d915724497fa422005e56011fcf7d74483d30fd502a0ae1992`  
		Last Modified: Wed, 17 Nov 2021 19:20:35 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114a479d47bf9ce3b07ffb880a448300b978f0dd2fb9b2cf257248dd29de5e84`  
		Last Modified: Thu, 18 Nov 2021 00:44:01 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ae5a388a1926cb6bd2604c7cd0f60a2b859f5e9fee54ab1e3c28cc3c479ab3`  
		Last Modified: Thu, 18 Nov 2021 00:44:34 GMT  
		Size: 95.7 MB (95703056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f35b4aed8fe029d1de9c2be5697656a92bf97140d97728899485277fc3dc043`  
		Last Modified: Thu, 18 Nov 2021 00:43:58 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b65826b08c9f8a035ad260f0b62525f5a8d4fb146976d525e46b4f75d06daad`  
		Last Modified: Thu, 18 Nov 2021 00:43:58 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb69ab7947819ba989edf4080ac113062525d4d969acf0cae72997265373542b`  
		Last Modified: Thu, 18 Nov 2021 00:44:01 GMT  
		Size: 2.7 MB (2749693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17daca5299618a3df09e55bfc7d4ca161dd7625f44b57e9168de012d0cba9bf`  
		Last Modified: Thu, 18 Nov 2021 00:44:13 GMT  
		Size: 47.9 MB (47933761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1076865c1e2494ca329b3cc9ff6da40aab3182b6dd6a011e88f0ac330903a38`  
		Last Modified: Thu, 18 Nov 2021 00:43:58 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1` - linux; ppc64le

```console
$ docker pull redmine@sha256:5044f07ac6e60e5b6a94218b4fa90ac3d73d57d97a26f2e2cf04d94e1a315f71
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234111493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2794e91b1bd4c9b3e213162f8b7cb1f15f81466089a83cfe972eccaae93c389`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 12 Oct 2021 01:26:46 GMT
ADD file:5526880c6f19a4b4231a8b2bd7cfc625d116764c4918eff6f0b55f8c1eb38e1a in / 
# Tue, 12 Oct 2021 01:26:50 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 18:23:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 18:24:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 18:24:11 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 19:17:28 GMT
ENV RUBY_MAJOR=2.6
# Tue, 12 Oct 2021 19:17:32 GMT
ENV RUBY_VERSION=2.6.8
# Tue, 12 Oct 2021 19:17:38 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Tue, 12 Oct 2021 19:25:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 19:25:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 19:26:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 19:26:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 19:26:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 19:26:22 GMT
CMD ["irb"]
# Thu, 14 Oct 2021 00:54:05 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 14 Oct 2021 00:57:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 Oct 2021 00:57:57 GMT
ENV RAILS_ENV=production
# Thu, 14 Oct 2021 00:58:08 GMT
WORKDIR /usr/src/redmine
# Thu, 14 Oct 2021 00:58:13 GMT
ENV HOME=/home/redmine
# Thu, 14 Oct 2021 00:58:31 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 14 Oct 2021 00:58:35 GMT
ENV REDMINE_VERSION=4.1.5
# Thu, 14 Oct 2021 00:58:40 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Thu, 14 Oct 2021 00:59:00 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 14 Oct 2021 01:04:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 Oct 2021 01:04:25 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 14 Oct 2021 01:04:27 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 14 Oct 2021 01:04:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Oct 2021 01:04:36 GMT
EXPOSE 3000
# Thu, 14 Oct 2021 01:04:45 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d69973af32573c07c8789c0f9c144a5c0b822a1e85b59db3ce9f8ebc489ce85d`  
		Last Modified: Tue, 12 Oct 2021 01:38:40 GMT  
		Size: 30.5 MB (30547197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f48a596ad1fccd3e24dcc1f65e362937ced6f5b5ab61b6eb49e8eda8a55b85`  
		Last Modified: Tue, 12 Oct 2021 19:30:52 GMT  
		Size: 12.7 MB (12705483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd72e7e6250a90b152d1d27efca928b2c1bfc949dfe1b2e9cf089acde024c098`  
		Last Modified: Tue, 12 Oct 2021 19:30:49 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03211df41d3c61789be71d89ebad2ce881638fb2a84c27562d7e3ff81f181458`  
		Last Modified: Tue, 12 Oct 2021 19:33:41 GMT  
		Size: 22.0 MB (21984973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c774747b6862c16e290d0508df2db39d1a24d4061e198d3567c877d14ca4bf8`  
		Last Modified: Tue, 12 Oct 2021 19:33:38 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d344e083cdb889978f1a8f40a20c569e9d02d096352f103edc1381edd38d39a`  
		Last Modified: Thu, 14 Oct 2021 01:22:07 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055091d203c828eda50c0fc58b4fc2380bb289903300ac48506d41b11e3e64f6`  
		Last Modified: Thu, 14 Oct 2021 01:22:24 GMT  
		Size: 101.3 MB (101326908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86aa33ed3b974244546104fc2f17c16cfc59c3961420d73a00dcdd428d919dbd`  
		Last Modified: Thu, 14 Oct 2021 01:22:00 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584682ab54558b6bba089db5b421b6d785c617bf43197cb9e72c61fc0c1cc4a8`  
		Last Modified: Thu, 14 Oct 2021 01:22:01 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f458104410b51d3994141d75dce44360cfa46fcc01e9f6d5cd2bea7491862f7`  
		Last Modified: Thu, 14 Oct 2021 01:22:02 GMT  
		Size: 2.7 MB (2749690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b0ff33ddbb28614d7a7634c41197a24124d710178ee5f90ae4375482059c7d9`  
		Last Modified: Thu, 14 Oct 2021 01:22:10 GMT  
		Size: 64.8 MB (64792996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc93cfdeb63ee31180bf5ef1dae43d601a4102973a3654b4999e7c17912a573d`  
		Last Modified: Thu, 14 Oct 2021 01:22:00 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1` - linux; s390x

```console
$ docker pull redmine@sha256:9826545cabb708f82a39645294fa6b4fe18682bb2a4ffb5ab0e03df343105640
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.2 MB (216222662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2c5a19ee3f59933d996cab7415a6e6c2b50b869db65a686da493239b6369795`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:42:59 GMT
ADD file:3ff5fbc9c53cf76aad0fe0e1a525cb0bc0d70e8f2a3d5741dfb8b3b8a9448ffd in / 
# Wed, 17 Nov 2021 02:43:00 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:21:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:21:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:21:07 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:42:36 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 09:42:36 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 09:42:37 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 09:44:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 09:44:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 09:44:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 09:44:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:44:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 09:44:07 GMT
CMD ["irb"]
# Wed, 17 Nov 2021 20:34:19 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 17 Nov 2021 20:34:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:34:43 GMT
ENV RAILS_ENV=production
# Wed, 17 Nov 2021 20:34:43 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Nov 2021 20:34:43 GMT
ENV HOME=/home/redmine
# Wed, 17 Nov 2021 20:34:44 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 17 Nov 2021 20:34:44 GMT
ENV REDMINE_VERSION=4.1.5
# Wed, 17 Nov 2021 20:34:44 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Wed, 17 Nov 2021 20:34:46 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 17 Nov 2021 20:36:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 20:36:25 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Nov 2021 20:36:25 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 17 Nov 2021 20:36:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 20:36:25 GMT
EXPOSE 3000
# Wed, 17 Nov 2021 20:36:25 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b8b917e61b3be882db10e68210f73caf5cc788bfb07aec0a659e30f4796b476b`  
		Last Modified: Wed, 17 Nov 2021 02:49:01 GMT  
		Size: 25.8 MB (25769063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e574c6d046371657ec033b78bc3df865890056f711b30df7505d0128446e36`  
		Last Modified: Wed, 17 Nov 2021 09:48:11 GMT  
		Size: 10.8 MB (10815243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6bfb1613df50da70222f9b1cd395c4b509f6e6631cf6a13ce6c6b9c8c4cf181`  
		Last Modified: Wed, 17 Nov 2021 09:48:09 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37bdaf56dd9686cdaca63c3c8ebab2d6841412a36159619d65853daa75500716`  
		Last Modified: Wed, 17 Nov 2021 09:51:17 GMT  
		Size: 21.6 MB (21619852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80433d0a1bacd8eb06bb301d366ea459dbae5ce9a2bea94372bd52e0939584a0`  
		Last Modified: Wed, 17 Nov 2021 09:51:15 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e82306e7113526e6aa75620a186091a8a2139c7e63336bc2033df0329cda36e`  
		Last Modified: Wed, 17 Nov 2021 20:39:48 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953e01eb8398b7e411547f900d6743483788b91446a4926c04d404495bcf814d`  
		Last Modified: Wed, 17 Nov 2021 20:40:00 GMT  
		Size: 91.8 MB (91791049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1786d101777e089e8f553bcd02e217229ae859817f642c2f4cc3ca482cc0037`  
		Last Modified: Wed, 17 Nov 2021 20:39:47 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c61376d40c4d7e02c177f7eac3f8f9f9d178c9cd308cd3149faf04c5b996a0c`  
		Last Modified: Wed, 17 Nov 2021 20:39:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724041fbce20361ad4bdeb17188bc355919db94cbb31d708760c028462b42b79`  
		Last Modified: Wed, 17 Nov 2021 20:39:47 GMT  
		Size: 2.7 MB (2749696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04445b75a0da224ae20d97016f3fea6736bd6b4f52e4495f86383539978fd06f`  
		Last Modified: Wed, 17 Nov 2021 20:39:52 GMT  
		Size: 63.5 MB (63473511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a50e8d09d481494c64c56360e2fe1c3ab6735d8af151d9d117a22d56114b82a`  
		Last Modified: Wed, 17 Nov 2021 20:39:46 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.1-alpine`

```console
$ docker pull redmine@sha256:6dbd35c35e023b696f652aa87bf1de330ef19513a1b85a00928f30244c701767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.1-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:fae3d2c173aad1c4ccf2ae887f62847716af5f908fa917fbac07b10913b45913
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (160030996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4714a18668c5842cac48a8a5bf13f3af01f3662dadbd9b44c49730c89b727d24`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:28:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Sat, 13 Nov 2021 06:28:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 13 Nov 2021 06:28:18 GMT
ENV LANG=C.UTF-8
# Sat, 13 Nov 2021 06:51:30 GMT
ENV RUBY_MAJOR=2.6
# Sat, 13 Nov 2021 06:51:30 GMT
ENV RUBY_VERSION=2.6.8
# Sat, 13 Nov 2021 06:51:31 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Sat, 13 Nov 2021 06:54:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 13 Nov 2021 06:54:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 13 Nov 2021 06:54:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 13 Nov 2021 06:54:45 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Nov 2021 06:54:45 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 13 Nov 2021 06:54:46 GMT
CMD ["irb"]
# Sat, 13 Nov 2021 14:31:40 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 13 Nov 2021 14:31:48 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Sat, 13 Nov 2021 14:31:48 GMT
ENV RAILS_ENV=production
# Sat, 13 Nov 2021 14:31:49 GMT
WORKDIR /usr/src/redmine
# Sat, 13 Nov 2021 14:31:49 GMT
ENV HOME=/home/redmine
# Sat, 13 Nov 2021 14:31:50 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 13 Nov 2021 14:31:50 GMT
ENV REDMINE_VERSION=4.1.5
# Sat, 13 Nov 2021 14:31:50 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Sat, 13 Nov 2021 14:31:54 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 13 Nov 2021 14:31:54 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 13 Nov 2021 14:34:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 13 Nov 2021 14:34:01 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 13 Nov 2021 14:34:01 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Sat, 13 Nov 2021 14:34:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Nov 2021 14:34:02 GMT
EXPOSE 3000
# Sat, 13 Nov 2021 14:34:02 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86e849bc66e37f2d898daa44d76330256a48635f1100e364c0f46206fca7b71`  
		Last Modified: Sat, 13 Nov 2021 06:56:48 GMT  
		Size: 3.6 MB (3582307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a2fc84ba5b32bce31936a6fdf8121f29d2eb485f8525795df7d32046e9f856`  
		Last Modified: Sat, 13 Nov 2021 06:56:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fd76747f3be3e4f4af1119b668fd5a9fa53725f84b429575cfb26c0d5f842a`  
		Last Modified: Sat, 13 Nov 2021 06:59:00 GMT  
		Size: 19.5 MB (19500293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bbfb1229cd3c27d4dd990a0daf591e427afbc679b854303415a9e9a01ff10b`  
		Last Modified: Sat, 13 Nov 2021 06:58:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c267c2d73515a2e4fbaac349e5a31212348b7d72b21f80611dac1923c5c68666`  
		Last Modified: Sat, 13 Nov 2021 14:37:15 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e62a0f0fc43b5aab817648e0aea8e8dcd39e0f5e7ee6ce76236ac5f49653e2`  
		Last Modified: Sat, 13 Nov 2021 14:37:25 GMT  
		Size: 69.5 MB (69547670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666ce34581c9e5eb65bc5ed69717166b196e1a17a8607e3721ae1b07c1cb90c8`  
		Last Modified: Sat, 13 Nov 2021 14:37:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a2fb4d61b7d1eb854991664d217dae48916bd3cf240c27f4fa2534973b40a5`  
		Last Modified: Sat, 13 Nov 2021 14:37:13 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6afa58a2a007900b48af7fe611027ca52ed3c1034ea34e75d6db8dddb5b18d1`  
		Last Modified: Sat, 13 Nov 2021 14:37:14 GMT  
		Size: 2.8 MB (2750433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a6c05fbcb5a65730f500ffa36488a9d0667133c3c4e784f88e4c8c966f946c`  
		Last Modified: Sat, 13 Nov 2021 14:37:19 GMT  
		Size: 61.8 MB (61824139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03693e88b691e6215bdd51b25ee8b9e56f1967a1ee89d59e4ecc12f354cbcb28`  
		Last Modified: Sat, 13 Nov 2021 14:37:13 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.1-passenger`

```console
$ docker pull redmine@sha256:d5a0a1c46c5bec1cf4b1e4fea37df3e3afe64ad7565b9654a0b8e63253f1664f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.1-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:b3b58664ca0f89c6644786cf4723d0e788734e3703b0fdd046165f5be908c80c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233029805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552964d89f045555c3d775895653aff55ca34c34ee435419b869aaf1f374b966`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:20:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:20:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 15:20:38 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 15:34:09 GMT
ENV RUBY_MAJOR=2.6
# Tue, 12 Oct 2021 15:34:09 GMT
ENV RUBY_VERSION=2.6.8
# Tue, 12 Oct 2021 15:34:09 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Tue, 12 Oct 2021 15:37:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 15:37:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 15:37:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 15:37:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 15:37:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 15:37:06 GMT
CMD ["irb"]
# Tue, 12 Oct 2021 20:20:16 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 12 Oct 2021 20:20:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 20:20:57 GMT
ENV RAILS_ENV=production
# Tue, 12 Oct 2021 20:20:57 GMT
WORKDIR /usr/src/redmine
# Tue, 12 Oct 2021 20:20:57 GMT
ENV HOME=/home/redmine
# Tue, 12 Oct 2021 20:20:59 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 12 Oct 2021 20:20:59 GMT
ENV REDMINE_VERSION=4.1.5
# Tue, 12 Oct 2021 20:20:59 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Tue, 12 Oct 2021 20:21:04 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 12 Oct 2021 20:22:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Oct 2021 20:22:14 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 12 Oct 2021 20:22:14 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 12 Oct 2021 20:22:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 20:22:15 GMT
EXPOSE 3000
# Tue, 12 Oct 2021 20:22:15 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Wed, 10 Nov 2021 03:46:43 GMT
ENV PASSENGER_VERSION=6.0.12
# Wed, 10 Nov 2021 03:47:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 10 Nov 2021 03:47:03 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Wed, 10 Nov 2021 03:47:03 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Wed, 10 Nov 2021 03:47:03 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee6af487f217efc8e231b9857a8031fdf07ab0c8b30e539497893ec5287578b`  
		Last Modified: Tue, 12 Oct 2021 15:39:48 GMT  
		Size: 12.6 MB (12565186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48bb8449b0384f7addf4ec5d88d8ef088e25ca52f9299c1fca4bff3f5b2411d`  
		Last Modified: Tue, 12 Oct 2021 15:39:46 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fbc3e5ccddf2ccfcc978381549c751e1167cdf41ce60580404b33cb6fdd7aa5`  
		Last Modified: Tue, 12 Oct 2021 15:41:15 GMT  
		Size: 21.5 MB (21467885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b99a224b661061fbbe799d6efb95f01221754e6a73aec4d536865d1e304d63`  
		Last Modified: Tue, 12 Oct 2021 15:41:12 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b92be01811211d262d0872aabc77c74589ad10e263a5d091b7a77fc657edd4`  
		Last Modified: Tue, 12 Oct 2021 20:28:12 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8617ac0503291a7bc25ab3e9ecadad7f36606e38768ec7dae57decbca32bc1ea`  
		Last Modified: Tue, 12 Oct 2021 20:28:29 GMT  
		Size: 94.1 MB (94088241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a76df102ee332891a671c026db6214352f68c057230bbdae139ea2227fe745`  
		Last Modified: Tue, 12 Oct 2021 20:28:10 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f353dd18278378e4d8216c008d56bc846a5a701d5a7730f60698a69cc659c8b`  
		Last Modified: Tue, 12 Oct 2021 20:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0888176d4f29df43b84ccec41ac92479f77bee993d76d41344d933ff075acec4`  
		Last Modified: Tue, 12 Oct 2021 20:28:11 GMT  
		Size: 2.7 MB (2749692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7edea4661341065395429e13204ddb02ce8e2608365b08a4b649071683624d43`  
		Last Modified: Tue, 12 Oct 2021 20:28:17 GMT  
		Size: 48.7 MB (48653871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3811deb43f4603834d18cf1fe5b28601cc92f816a4dbc984fe9858936d4f44a3`  
		Last Modified: Tue, 12 Oct 2021 20:28:10 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c90d10b267c49cba83436d1bad2aa20653bde9c3681fbe2277d43a2ef691e5d`  
		Last Modified: Wed, 10 Nov 2021 03:48:30 GMT  
		Size: 21.4 MB (21436536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff182f4aaf60af77237f70493b14e2c05a22437378c9d91850db63454081120`  
		Last Modified: Wed, 10 Nov 2021 03:48:28 GMT  
		Size: 4.9 MB (4924642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.1.5`

```console
$ docker pull redmine@sha256:63e3ffff6262d8d63a9062c1ac7221b81c87b96a1d910080fc40f04e067bfe90
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

### `redmine:4.1.5` - linux; amd64

```console
$ docker pull redmine@sha256:403c93eb007bd16cd277e19fc1459f180c7483fa4940fd5044a30acef53a8f01
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.7 MB (206668627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0da7de9c6f21204eac2ef99bfd1d097808059ad4f8daeb89898eb83deffb97c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:20:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:20:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 15:20:38 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 15:34:09 GMT
ENV RUBY_MAJOR=2.6
# Tue, 12 Oct 2021 15:34:09 GMT
ENV RUBY_VERSION=2.6.8
# Tue, 12 Oct 2021 15:34:09 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Tue, 12 Oct 2021 15:37:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 15:37:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 15:37:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 15:37:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 15:37:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 15:37:06 GMT
CMD ["irb"]
# Tue, 12 Oct 2021 20:20:16 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 12 Oct 2021 20:20:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 20:20:57 GMT
ENV RAILS_ENV=production
# Tue, 12 Oct 2021 20:20:57 GMT
WORKDIR /usr/src/redmine
# Tue, 12 Oct 2021 20:20:57 GMT
ENV HOME=/home/redmine
# Tue, 12 Oct 2021 20:20:59 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 12 Oct 2021 20:20:59 GMT
ENV REDMINE_VERSION=4.1.5
# Tue, 12 Oct 2021 20:20:59 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Tue, 12 Oct 2021 20:21:04 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 12 Oct 2021 20:22:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Oct 2021 20:22:14 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 12 Oct 2021 20:22:14 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 12 Oct 2021 20:22:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 20:22:15 GMT
EXPOSE 3000
# Tue, 12 Oct 2021 20:22:15 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee6af487f217efc8e231b9857a8031fdf07ab0c8b30e539497893ec5287578b`  
		Last Modified: Tue, 12 Oct 2021 15:39:48 GMT  
		Size: 12.6 MB (12565186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48bb8449b0384f7addf4ec5d88d8ef088e25ca52f9299c1fca4bff3f5b2411d`  
		Last Modified: Tue, 12 Oct 2021 15:39:46 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fbc3e5ccddf2ccfcc978381549c751e1167cdf41ce60580404b33cb6fdd7aa5`  
		Last Modified: Tue, 12 Oct 2021 15:41:15 GMT  
		Size: 21.5 MB (21467885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b99a224b661061fbbe799d6efb95f01221754e6a73aec4d536865d1e304d63`  
		Last Modified: Tue, 12 Oct 2021 15:41:12 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b92be01811211d262d0872aabc77c74589ad10e263a5d091b7a77fc657edd4`  
		Last Modified: Tue, 12 Oct 2021 20:28:12 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8617ac0503291a7bc25ab3e9ecadad7f36606e38768ec7dae57decbca32bc1ea`  
		Last Modified: Tue, 12 Oct 2021 20:28:29 GMT  
		Size: 94.1 MB (94088241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a76df102ee332891a671c026db6214352f68c057230bbdae139ea2227fe745`  
		Last Modified: Tue, 12 Oct 2021 20:28:10 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f353dd18278378e4d8216c008d56bc846a5a701d5a7730f60698a69cc659c8b`  
		Last Modified: Tue, 12 Oct 2021 20:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0888176d4f29df43b84ccec41ac92479f77bee993d76d41344d933ff075acec4`  
		Last Modified: Tue, 12 Oct 2021 20:28:11 GMT  
		Size: 2.7 MB (2749692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7edea4661341065395429e13204ddb02ce8e2608365b08a4b649071683624d43`  
		Last Modified: Tue, 12 Oct 2021 20:28:17 GMT  
		Size: 48.7 MB (48653871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3811deb43f4603834d18cf1fe5b28601cc92f816a4dbc984fe9858936d4f44a3`  
		Last Modified: Tue, 12 Oct 2021 20:28:10 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1.5` - linux; arm variant v5

```console
$ docker pull redmine@sha256:fd9a6ca83808905c079ff29662f81bb35330a8be3abbc339c2507c971852ea3b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.7 MB (210669047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fb4a19021b4eeca711ee785701e0df1d7d03e3e0871a30ad557c336a06e2ef`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 12 Oct 2021 00:51:32 GMT
ADD file:0d95eee31ffe3f4260263e4fac2a61123a4b98d2e7a67efcc7bfea338c54f41d in / 
# Tue, 12 Oct 2021 00:51:32 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 06:45:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 06:45:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 06:45:07 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 07:20:58 GMT
ENV RUBY_MAJOR=2.6
# Tue, 12 Oct 2021 07:20:58 GMT
ENV RUBY_VERSION=2.6.8
# Tue, 12 Oct 2021 07:20:59 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Tue, 12 Oct 2021 07:25:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 07:25:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 07:25:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 07:25:31 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 07:25:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 07:25:33 GMT
CMD ["irb"]
# Wed, 13 Oct 2021 03:13:47 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 13 Oct 2021 03:15:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 03:15:19 GMT
ENV RAILS_ENV=production
# Wed, 13 Oct 2021 03:15:21 GMT
WORKDIR /usr/src/redmine
# Wed, 13 Oct 2021 03:15:22 GMT
ENV HOME=/home/redmine
# Wed, 13 Oct 2021 03:15:27 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 13 Oct 2021 03:15:28 GMT
ENV REDMINE_VERSION=4.1.5
# Wed, 13 Oct 2021 03:15:29 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Wed, 13 Oct 2021 03:15:39 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 13 Oct 2021 03:22:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 13 Oct 2021 03:22:12 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 13 Oct 2021 03:22:13 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 13 Oct 2021 03:22:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Oct 2021 03:22:15 GMT
EXPOSE 3000
# Wed, 13 Oct 2021 03:22:16 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:175b083b22fb061f7d1894fe4916a2967ce636d47376da526d90d57c8f7efc60`  
		Last Modified: Tue, 12 Oct 2021 01:07:45 GMT  
		Size: 24.9 MB (24872704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed73113a2340f22427741647a89a1911c6dd067bde17833928c5d210ab93918`  
		Last Modified: Tue, 12 Oct 2021 07:31:54 GMT  
		Size: 10.3 MB (10349314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7a78f939d570718e0af30429b3118d94e3800937a469b3fca591fda6d0540e`  
		Last Modified: Tue, 12 Oct 2021 07:31:46 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee56be0d198078cdceb927f259d279ea37548abbdefb95d8056e7e15d8137f0`  
		Last Modified: Tue, 12 Oct 2021 07:35:42 GMT  
		Size: 20.7 MB (20733372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e080526cffc142b881616db7396494f86cda539f9b9c65296f73498b8f70f81`  
		Last Modified: Tue, 12 Oct 2021 07:35:32 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c030517df14ac43613f1cd4bf516123c442ce7a9e6f545e593cc52a6b40fd301`  
		Last Modified: Wed, 13 Oct 2021 03:33:10 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3897ec5e588606be8744330bf1c4d14efe3cb454ad1a7a28841648516085a681`  
		Last Modified: Wed, 13 Oct 2021 03:33:53 GMT  
		Size: 89.6 MB (89575164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14263ed54825c7939921f07b976fdeb8d1030283ae7629fb3cad48bcad63ef8b`  
		Last Modified: Wed, 13 Oct 2021 03:33:09 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42977913dd4d9c9fc4f9bbe0ec0c1cf86191be9b169e4625fd52638bd2d6990`  
		Last Modified: Wed, 13 Oct 2021 03:33:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fc078b0610e878e98fe32bd23535bba23460228cdb6d1c9342420cc1056fb1`  
		Last Modified: Wed, 13 Oct 2021 03:33:11 GMT  
		Size: 2.7 MB (2749695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8435301d2e3e6d0eb02ef7f3dfef10b39d778154c1dbca332274b48b117a3a9e`  
		Last Modified: Wed, 13 Oct 2021 03:33:31 GMT  
		Size: 62.4 MB (62384562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b775033255d5a1a789c784df094106b9b2489c0a159ff5d254d4e9c670b6084f`  
		Last Modified: Wed, 13 Oct 2021 03:33:09 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1.5` - linux; arm variant v7

```console
$ docker pull redmine@sha256:380b2a1bd20ab586d27fccfa9e704b5711d53271b5ae1ea0b553d0dff129aa5f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203851889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a22805d3ff7605300793419e632f413f2e1715dc0ccaf9dc46bb5cff553b7b9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 12 Oct 2021 01:29:42 GMT
ADD file:fe1eaa1b1d760b3d250cb4ac331d26a261fc569f1694bd34e146f00874dc87e5 in / 
# Tue, 12 Oct 2021 01:29:43 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 02:56:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 02:56:30 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 03:29:09 GMT
ENV RUBY_MAJOR=2.6
# Tue, 12 Oct 2021 03:29:10 GMT
ENV RUBY_VERSION=2.6.8
# Tue, 12 Oct 2021 03:29:10 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Tue, 12 Oct 2021 03:33:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 03:33:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 03:33:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 03:33:31 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 03:33:33 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 03:33:33 GMT
CMD ["irb"]
# Wed, 13 Oct 2021 06:41:32 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 13 Oct 2021 06:42:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 06:42:35 GMT
ENV RAILS_ENV=production
# Wed, 13 Oct 2021 06:42:36 GMT
WORKDIR /usr/src/redmine
# Wed, 13 Oct 2021 06:42:36 GMT
ENV HOME=/home/redmine
# Wed, 13 Oct 2021 06:42:38 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 13 Oct 2021 06:42:38 GMT
ENV REDMINE_VERSION=4.1.5
# Wed, 13 Oct 2021 06:42:39 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Wed, 13 Oct 2021 06:42:47 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 13 Oct 2021 06:48:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 13 Oct 2021 06:48:02 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 13 Oct 2021 06:48:03 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 13 Oct 2021 06:48:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Oct 2021 06:48:04 GMT
EXPOSE 3000
# Wed, 13 Oct 2021 06:48:04 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c0b5ba470cac8cfdae4633f5cddb3ba9350fe1d1b1507c4965a8224eb40e52c5`  
		Last Modified: Tue, 12 Oct 2021 01:45:52 GMT  
		Size: 22.7 MB (22739698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cdd321094894b78bc0792d96cf339ee9e4ce7ec18a14ea44b32cfbc809867b`  
		Last Modified: Tue, 12 Oct 2021 03:40:20 GMT  
		Size: 9.9 MB (9872904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c0e1a382b6eb02d552bdb97946d22f8b0d9b5f787b5d1b491fa3703e23d5ea`  
		Last Modified: Tue, 12 Oct 2021 03:40:13 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c9c99e0177bf2b2564708b982b9c36357cd8d40692351ae3fb607492c43c90`  
		Last Modified: Tue, 12 Oct 2021 03:42:55 GMT  
		Size: 20.6 MB (20643669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb852a3aed1bbfa0863f056cd080fad5debc62aefa369421cb364fde8137ebf`  
		Last Modified: Tue, 12 Oct 2021 03:42:48 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1086d0917a940899c5d3bad3fc3feea5fe65219a792b2acd69cd9ada062a7b`  
		Last Modified: Wed, 13 Oct 2021 06:57:14 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd9f426d70a745f2ddce33d8ac46330d64fcbed546853bad59d21f3534ca535`  
		Last Modified: Wed, 13 Oct 2021 06:58:10 GMT  
		Size: 85.6 MB (85590404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa3942a6e72dd3e213cd5889c3c17e56b4b1ff4c59a01feeab202d71714b219`  
		Last Modified: Wed, 13 Oct 2021 06:57:12 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706f62754dfee343ce1dbe89f0c2c61bc69c76aaabdfeec1b1dbb316c723f046`  
		Last Modified: Wed, 13 Oct 2021 06:57:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3afaba210f3f7cccc352f3a2bfb91fcfe93bbc146f42e038f0bf03d42a628754`  
		Last Modified: Wed, 13 Oct 2021 06:57:16 GMT  
		Size: 2.7 MB (2749696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e3e7f892fb877ae9658d4cf0c4c042302426527d05083af6384970cbeb8c12`  
		Last Modified: Wed, 13 Oct 2021 06:57:41 GMT  
		Size: 62.3 MB (62251280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a5677793c6ff5ebcc5d032b27aaef548b1be3fd53835a226127d26743d3d34`  
		Last Modified: Wed, 13 Oct 2021 06:57:13 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1.5` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:b222b2102035ba87c72076afd3f971a910dd6cfa4627c0423b876748b40dea1e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.4 MB (216401827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871b1f794b4d0fcb638c8a57721a72acc701c347e2e647a928da47a7dc1c8c9c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:31:02 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:46:01 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 09:46:02 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 09:46:03 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 09:48:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 09:48:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 09:48:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 09:48:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:48:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 09:48:06 GMT
CMD ["irb"]
# Wed, 17 Nov 2021 19:49:55 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 17 Nov 2021 19:50:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 19:50:19 GMT
ENV RAILS_ENV=production
# Wed, 17 Nov 2021 19:50:20 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Nov 2021 19:50:21 GMT
ENV HOME=/home/redmine
# Wed, 17 Nov 2021 19:50:23 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 17 Nov 2021 19:50:23 GMT
ENV REDMINE_VERSION=4.1.5
# Wed, 17 Nov 2021 19:50:24 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Wed, 17 Nov 2021 19:50:28 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 17 Nov 2021 19:52:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 19:52:38 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Nov 2021 19:52:40 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 17 Nov 2021 19:52:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 19:52:41 GMT
EXPOSE 3000
# Wed, 17 Nov 2021 19:52:42 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8443a8ec909433d7156b8dcbeaf77f4e53d6a44b253a3f03b95126547154d55`  
		Last Modified: Wed, 17 Nov 2021 09:51:43 GMT  
		Size: 11.3 MB (11261808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f57122fa0ffe176f788d35a4a8f12a76819fa3bab198ac16e26d2961047a1d`  
		Last Modified: Wed, 17 Nov 2021 09:51:41 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16912dae180f72843a7e6b7dd25071e1090943354879adab903dcd984c8cee67`  
		Last Modified: Wed, 17 Nov 2021 09:54:26 GMT  
		Size: 21.1 MB (21095263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b73b9ee9aa5f816c4fb7665c7e19fe1663007ac1aacb74064aac56ece594983`  
		Last Modified: Wed, 17 Nov 2021 09:54:23 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb50985615235593da91e201ffe4b1db40feab50ab0a12b02a4c99191da4dfd`  
		Last Modified: Wed, 17 Nov 2021 19:57:02 GMT  
		Size: 1.6 KB (1625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b972b42f387b463ec4f85b98ff1de46778da88cde8db5210abd6cdb28fcfe996`  
		Last Modified: Wed, 17 Nov 2021 19:57:16 GMT  
		Size: 92.6 MB (92615309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d5c078974fd14c58f0b3b7716527a89b7fd62214cbd050a80d385982968927`  
		Last Modified: Wed, 17 Nov 2021 19:56:59 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302584afc613dd65a75b5bcda18ac7919a7c809a1df57148453b3f76954ed897`  
		Last Modified: Wed, 17 Nov 2021 19:56:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d073b657b29ddf797af445ca3996a8594b19899f364b2cc3d189f86a3fcf0deb`  
		Last Modified: Wed, 17 Nov 2021 19:57:00 GMT  
		Size: 2.7 MB (2749627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca343679f96ad8123399df85aad69f3174b5d405b2d11bf4804a0840974e2710`  
		Last Modified: Wed, 17 Nov 2021 19:57:10 GMT  
		Size: 62.8 MB (62752672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd1dcf76925b4813ce41dd25c0b93567defab250f8d74eac3e070f92b49c068`  
		Last Modified: Wed, 17 Nov 2021 19:56:59 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1.5` - linux; 386

```console
$ docker pull redmine@sha256:156a98e108ae32310750def5670b7f14ce4791c8fba4fc62b4389d126421ee10
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212332382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b8c8954f2416156578d6b917f84622fb2feacefa48597e8b97e216b5700b97`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 18:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 18:38:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 18:38:25 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 19:07:29 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 19:07:29 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 19:07:29 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 19:11:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 19:11:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 19:11:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 19:12:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 19:12:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 19:12:01 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 00:37:59 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 00:38:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 00:38:32 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 00:38:33 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 00:38:33 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 00:38:34 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 00:38:34 GMT
ENV REDMINE_VERSION=4.1.5
# Thu, 18 Nov 2021 00:38:34 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Thu, 18 Nov 2021 00:38:39 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 00:39:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 00:39:29 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 00:39:29 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 00:39:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 00:39:30 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 00:39:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1742b7e5e1e5bca675e7f251c9f6fe8778a1bb1548e5b418f8547277f14e2e33`  
		Last Modified: Wed, 17 Nov 2021 19:17:19 GMT  
		Size: 17.2 MB (17227026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ef5459771b89c49219d5c15641c7215faf156712422f01efee40ad955a52c5`  
		Last Modified: Wed, 17 Nov 2021 19:17:10 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8e5a4df5a8f121515c23ab2e470f17d64c6bb138b6c22dda592fcde5393ca4`  
		Last Modified: Wed, 17 Nov 2021 19:20:39 GMT  
		Size: 20.9 MB (20910059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955765ea073687d915724497fa422005e56011fcf7d74483d30fd502a0ae1992`  
		Last Modified: Wed, 17 Nov 2021 19:20:35 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114a479d47bf9ce3b07ffb880a448300b978f0dd2fb9b2cf257248dd29de5e84`  
		Last Modified: Thu, 18 Nov 2021 00:44:01 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ae5a388a1926cb6bd2604c7cd0f60a2b859f5e9fee54ab1e3c28cc3c479ab3`  
		Last Modified: Thu, 18 Nov 2021 00:44:34 GMT  
		Size: 95.7 MB (95703056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f35b4aed8fe029d1de9c2be5697656a92bf97140d97728899485277fc3dc043`  
		Last Modified: Thu, 18 Nov 2021 00:43:58 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b65826b08c9f8a035ad260f0b62525f5a8d4fb146976d525e46b4f75d06daad`  
		Last Modified: Thu, 18 Nov 2021 00:43:58 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb69ab7947819ba989edf4080ac113062525d4d969acf0cae72997265373542b`  
		Last Modified: Thu, 18 Nov 2021 00:44:01 GMT  
		Size: 2.7 MB (2749693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17daca5299618a3df09e55bfc7d4ca161dd7625f44b57e9168de012d0cba9bf`  
		Last Modified: Thu, 18 Nov 2021 00:44:13 GMT  
		Size: 47.9 MB (47933761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1076865c1e2494ca329b3cc9ff6da40aab3182b6dd6a011e88f0ac330903a38`  
		Last Modified: Thu, 18 Nov 2021 00:43:58 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1.5` - linux; ppc64le

```console
$ docker pull redmine@sha256:5044f07ac6e60e5b6a94218b4fa90ac3d73d57d97a26f2e2cf04d94e1a315f71
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234111493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2794e91b1bd4c9b3e213162f8b7cb1f15f81466089a83cfe972eccaae93c389`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 12 Oct 2021 01:26:46 GMT
ADD file:5526880c6f19a4b4231a8b2bd7cfc625d116764c4918eff6f0b55f8c1eb38e1a in / 
# Tue, 12 Oct 2021 01:26:50 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 18:23:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 18:24:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 18:24:11 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 19:17:28 GMT
ENV RUBY_MAJOR=2.6
# Tue, 12 Oct 2021 19:17:32 GMT
ENV RUBY_VERSION=2.6.8
# Tue, 12 Oct 2021 19:17:38 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Tue, 12 Oct 2021 19:25:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 19:25:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 19:26:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 19:26:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 19:26:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 19:26:22 GMT
CMD ["irb"]
# Thu, 14 Oct 2021 00:54:05 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 14 Oct 2021 00:57:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 Oct 2021 00:57:57 GMT
ENV RAILS_ENV=production
# Thu, 14 Oct 2021 00:58:08 GMT
WORKDIR /usr/src/redmine
# Thu, 14 Oct 2021 00:58:13 GMT
ENV HOME=/home/redmine
# Thu, 14 Oct 2021 00:58:31 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 14 Oct 2021 00:58:35 GMT
ENV REDMINE_VERSION=4.1.5
# Thu, 14 Oct 2021 00:58:40 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Thu, 14 Oct 2021 00:59:00 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 14 Oct 2021 01:04:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 Oct 2021 01:04:25 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 14 Oct 2021 01:04:27 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 14 Oct 2021 01:04:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Oct 2021 01:04:36 GMT
EXPOSE 3000
# Thu, 14 Oct 2021 01:04:45 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d69973af32573c07c8789c0f9c144a5c0b822a1e85b59db3ce9f8ebc489ce85d`  
		Last Modified: Tue, 12 Oct 2021 01:38:40 GMT  
		Size: 30.5 MB (30547197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f48a596ad1fccd3e24dcc1f65e362937ced6f5b5ab61b6eb49e8eda8a55b85`  
		Last Modified: Tue, 12 Oct 2021 19:30:52 GMT  
		Size: 12.7 MB (12705483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd72e7e6250a90b152d1d27efca928b2c1bfc949dfe1b2e9cf089acde024c098`  
		Last Modified: Tue, 12 Oct 2021 19:30:49 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03211df41d3c61789be71d89ebad2ce881638fb2a84c27562d7e3ff81f181458`  
		Last Modified: Tue, 12 Oct 2021 19:33:41 GMT  
		Size: 22.0 MB (21984973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c774747b6862c16e290d0508df2db39d1a24d4061e198d3567c877d14ca4bf8`  
		Last Modified: Tue, 12 Oct 2021 19:33:38 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d344e083cdb889978f1a8f40a20c569e9d02d096352f103edc1381edd38d39a`  
		Last Modified: Thu, 14 Oct 2021 01:22:07 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055091d203c828eda50c0fc58b4fc2380bb289903300ac48506d41b11e3e64f6`  
		Last Modified: Thu, 14 Oct 2021 01:22:24 GMT  
		Size: 101.3 MB (101326908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86aa33ed3b974244546104fc2f17c16cfc59c3961420d73a00dcdd428d919dbd`  
		Last Modified: Thu, 14 Oct 2021 01:22:00 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584682ab54558b6bba089db5b421b6d785c617bf43197cb9e72c61fc0c1cc4a8`  
		Last Modified: Thu, 14 Oct 2021 01:22:01 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f458104410b51d3994141d75dce44360cfa46fcc01e9f6d5cd2bea7491862f7`  
		Last Modified: Thu, 14 Oct 2021 01:22:02 GMT  
		Size: 2.7 MB (2749690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b0ff33ddbb28614d7a7634c41197a24124d710178ee5f90ae4375482059c7d9`  
		Last Modified: Thu, 14 Oct 2021 01:22:10 GMT  
		Size: 64.8 MB (64792996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc93cfdeb63ee31180bf5ef1dae43d601a4102973a3654b4999e7c17912a573d`  
		Last Modified: Thu, 14 Oct 2021 01:22:00 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1.5` - linux; s390x

```console
$ docker pull redmine@sha256:9826545cabb708f82a39645294fa6b4fe18682bb2a4ffb5ab0e03df343105640
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.2 MB (216222662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2c5a19ee3f59933d996cab7415a6e6c2b50b869db65a686da493239b6369795`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:42:59 GMT
ADD file:3ff5fbc9c53cf76aad0fe0e1a525cb0bc0d70e8f2a3d5741dfb8b3b8a9448ffd in / 
# Wed, 17 Nov 2021 02:43:00 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:21:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:21:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:21:07 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:42:36 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 09:42:36 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 09:42:37 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 09:44:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 09:44:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 09:44:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 09:44:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:44:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 09:44:07 GMT
CMD ["irb"]
# Wed, 17 Nov 2021 20:34:19 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 17 Nov 2021 20:34:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:34:43 GMT
ENV RAILS_ENV=production
# Wed, 17 Nov 2021 20:34:43 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Nov 2021 20:34:43 GMT
ENV HOME=/home/redmine
# Wed, 17 Nov 2021 20:34:44 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 17 Nov 2021 20:34:44 GMT
ENV REDMINE_VERSION=4.1.5
# Wed, 17 Nov 2021 20:34:44 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Wed, 17 Nov 2021 20:34:46 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 17 Nov 2021 20:36:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 20:36:25 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Nov 2021 20:36:25 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 17 Nov 2021 20:36:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 20:36:25 GMT
EXPOSE 3000
# Wed, 17 Nov 2021 20:36:25 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b8b917e61b3be882db10e68210f73caf5cc788bfb07aec0a659e30f4796b476b`  
		Last Modified: Wed, 17 Nov 2021 02:49:01 GMT  
		Size: 25.8 MB (25769063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e574c6d046371657ec033b78bc3df865890056f711b30df7505d0128446e36`  
		Last Modified: Wed, 17 Nov 2021 09:48:11 GMT  
		Size: 10.8 MB (10815243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6bfb1613df50da70222f9b1cd395c4b509f6e6631cf6a13ce6c6b9c8c4cf181`  
		Last Modified: Wed, 17 Nov 2021 09:48:09 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37bdaf56dd9686cdaca63c3c8ebab2d6841412a36159619d65853daa75500716`  
		Last Modified: Wed, 17 Nov 2021 09:51:17 GMT  
		Size: 21.6 MB (21619852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80433d0a1bacd8eb06bb301d366ea459dbae5ce9a2bea94372bd52e0939584a0`  
		Last Modified: Wed, 17 Nov 2021 09:51:15 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e82306e7113526e6aa75620a186091a8a2139c7e63336bc2033df0329cda36e`  
		Last Modified: Wed, 17 Nov 2021 20:39:48 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953e01eb8398b7e411547f900d6743483788b91446a4926c04d404495bcf814d`  
		Last Modified: Wed, 17 Nov 2021 20:40:00 GMT  
		Size: 91.8 MB (91791049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1786d101777e089e8f553bcd02e217229ae859817f642c2f4cc3ca482cc0037`  
		Last Modified: Wed, 17 Nov 2021 20:39:47 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c61376d40c4d7e02c177f7eac3f8f9f9d178c9cd308cd3149faf04c5b996a0c`  
		Last Modified: Wed, 17 Nov 2021 20:39:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724041fbce20361ad4bdeb17188bc355919db94cbb31d708760c028462b42b79`  
		Last Modified: Wed, 17 Nov 2021 20:39:47 GMT  
		Size: 2.7 MB (2749696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04445b75a0da224ae20d97016f3fea6736bd6b4f52e4495f86383539978fd06f`  
		Last Modified: Wed, 17 Nov 2021 20:39:52 GMT  
		Size: 63.5 MB (63473511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a50e8d09d481494c64c56360e2fe1c3ab6735d8af151d9d117a22d56114b82a`  
		Last Modified: Wed, 17 Nov 2021 20:39:46 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.1.5-alpine`

```console
$ docker pull redmine@sha256:6dbd35c35e023b696f652aa87bf1de330ef19513a1b85a00928f30244c701767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.1.5-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:fae3d2c173aad1c4ccf2ae887f62847716af5f908fa917fbac07b10913b45913
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (160030996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4714a18668c5842cac48a8a5bf13f3af01f3662dadbd9b44c49730c89b727d24`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:28:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Sat, 13 Nov 2021 06:28:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 13 Nov 2021 06:28:18 GMT
ENV LANG=C.UTF-8
# Sat, 13 Nov 2021 06:51:30 GMT
ENV RUBY_MAJOR=2.6
# Sat, 13 Nov 2021 06:51:30 GMT
ENV RUBY_VERSION=2.6.8
# Sat, 13 Nov 2021 06:51:31 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Sat, 13 Nov 2021 06:54:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 13 Nov 2021 06:54:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 13 Nov 2021 06:54:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 13 Nov 2021 06:54:45 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Nov 2021 06:54:45 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 13 Nov 2021 06:54:46 GMT
CMD ["irb"]
# Sat, 13 Nov 2021 14:31:40 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 13 Nov 2021 14:31:48 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Sat, 13 Nov 2021 14:31:48 GMT
ENV RAILS_ENV=production
# Sat, 13 Nov 2021 14:31:49 GMT
WORKDIR /usr/src/redmine
# Sat, 13 Nov 2021 14:31:49 GMT
ENV HOME=/home/redmine
# Sat, 13 Nov 2021 14:31:50 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 13 Nov 2021 14:31:50 GMT
ENV REDMINE_VERSION=4.1.5
# Sat, 13 Nov 2021 14:31:50 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Sat, 13 Nov 2021 14:31:54 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 13 Nov 2021 14:31:54 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 13 Nov 2021 14:34:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 13 Nov 2021 14:34:01 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 13 Nov 2021 14:34:01 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Sat, 13 Nov 2021 14:34:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Nov 2021 14:34:02 GMT
EXPOSE 3000
# Sat, 13 Nov 2021 14:34:02 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86e849bc66e37f2d898daa44d76330256a48635f1100e364c0f46206fca7b71`  
		Last Modified: Sat, 13 Nov 2021 06:56:48 GMT  
		Size: 3.6 MB (3582307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a2fc84ba5b32bce31936a6fdf8121f29d2eb485f8525795df7d32046e9f856`  
		Last Modified: Sat, 13 Nov 2021 06:56:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fd76747f3be3e4f4af1119b668fd5a9fa53725f84b429575cfb26c0d5f842a`  
		Last Modified: Sat, 13 Nov 2021 06:59:00 GMT  
		Size: 19.5 MB (19500293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bbfb1229cd3c27d4dd990a0daf591e427afbc679b854303415a9e9a01ff10b`  
		Last Modified: Sat, 13 Nov 2021 06:58:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c267c2d73515a2e4fbaac349e5a31212348b7d72b21f80611dac1923c5c68666`  
		Last Modified: Sat, 13 Nov 2021 14:37:15 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e62a0f0fc43b5aab817648e0aea8e8dcd39e0f5e7ee6ce76236ac5f49653e2`  
		Last Modified: Sat, 13 Nov 2021 14:37:25 GMT  
		Size: 69.5 MB (69547670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666ce34581c9e5eb65bc5ed69717166b196e1a17a8607e3721ae1b07c1cb90c8`  
		Last Modified: Sat, 13 Nov 2021 14:37:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a2fb4d61b7d1eb854991664d217dae48916bd3cf240c27f4fa2534973b40a5`  
		Last Modified: Sat, 13 Nov 2021 14:37:13 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6afa58a2a007900b48af7fe611027ca52ed3c1034ea34e75d6db8dddb5b18d1`  
		Last Modified: Sat, 13 Nov 2021 14:37:14 GMT  
		Size: 2.8 MB (2750433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a6c05fbcb5a65730f500ffa36488a9d0667133c3c4e784f88e4c8c966f946c`  
		Last Modified: Sat, 13 Nov 2021 14:37:19 GMT  
		Size: 61.8 MB (61824139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03693e88b691e6215bdd51b25ee8b9e56f1967a1ee89d59e4ecc12f354cbcb28`  
		Last Modified: Sat, 13 Nov 2021 14:37:13 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.1.5-passenger`

```console
$ docker pull redmine@sha256:d5a0a1c46c5bec1cf4b1e4fea37df3e3afe64ad7565b9654a0b8e63253f1664f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.1.5-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:b3b58664ca0f89c6644786cf4723d0e788734e3703b0fdd046165f5be908c80c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233029805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552964d89f045555c3d775895653aff55ca34c34ee435419b869aaf1f374b966`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:20:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:20:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 15:20:38 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 15:34:09 GMT
ENV RUBY_MAJOR=2.6
# Tue, 12 Oct 2021 15:34:09 GMT
ENV RUBY_VERSION=2.6.8
# Tue, 12 Oct 2021 15:34:09 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Tue, 12 Oct 2021 15:37:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 15:37:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 15:37:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 15:37:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 15:37:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 15:37:06 GMT
CMD ["irb"]
# Tue, 12 Oct 2021 20:20:16 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 12 Oct 2021 20:20:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 20:20:57 GMT
ENV RAILS_ENV=production
# Tue, 12 Oct 2021 20:20:57 GMT
WORKDIR /usr/src/redmine
# Tue, 12 Oct 2021 20:20:57 GMT
ENV HOME=/home/redmine
# Tue, 12 Oct 2021 20:20:59 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 12 Oct 2021 20:20:59 GMT
ENV REDMINE_VERSION=4.1.5
# Tue, 12 Oct 2021 20:20:59 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Tue, 12 Oct 2021 20:21:04 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 12 Oct 2021 20:22:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Oct 2021 20:22:14 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 12 Oct 2021 20:22:14 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 12 Oct 2021 20:22:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 20:22:15 GMT
EXPOSE 3000
# Tue, 12 Oct 2021 20:22:15 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Wed, 10 Nov 2021 03:46:43 GMT
ENV PASSENGER_VERSION=6.0.12
# Wed, 10 Nov 2021 03:47:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 10 Nov 2021 03:47:03 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Wed, 10 Nov 2021 03:47:03 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Wed, 10 Nov 2021 03:47:03 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee6af487f217efc8e231b9857a8031fdf07ab0c8b30e539497893ec5287578b`  
		Last Modified: Tue, 12 Oct 2021 15:39:48 GMT  
		Size: 12.6 MB (12565186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48bb8449b0384f7addf4ec5d88d8ef088e25ca52f9299c1fca4bff3f5b2411d`  
		Last Modified: Tue, 12 Oct 2021 15:39:46 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fbc3e5ccddf2ccfcc978381549c751e1167cdf41ce60580404b33cb6fdd7aa5`  
		Last Modified: Tue, 12 Oct 2021 15:41:15 GMT  
		Size: 21.5 MB (21467885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b99a224b661061fbbe799d6efb95f01221754e6a73aec4d536865d1e304d63`  
		Last Modified: Tue, 12 Oct 2021 15:41:12 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b92be01811211d262d0872aabc77c74589ad10e263a5d091b7a77fc657edd4`  
		Last Modified: Tue, 12 Oct 2021 20:28:12 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8617ac0503291a7bc25ab3e9ecadad7f36606e38768ec7dae57decbca32bc1ea`  
		Last Modified: Tue, 12 Oct 2021 20:28:29 GMT  
		Size: 94.1 MB (94088241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a76df102ee332891a671c026db6214352f68c057230bbdae139ea2227fe745`  
		Last Modified: Tue, 12 Oct 2021 20:28:10 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f353dd18278378e4d8216c008d56bc846a5a701d5a7730f60698a69cc659c8b`  
		Last Modified: Tue, 12 Oct 2021 20:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0888176d4f29df43b84ccec41ac92479f77bee993d76d41344d933ff075acec4`  
		Last Modified: Tue, 12 Oct 2021 20:28:11 GMT  
		Size: 2.7 MB (2749692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7edea4661341065395429e13204ddb02ce8e2608365b08a4b649071683624d43`  
		Last Modified: Tue, 12 Oct 2021 20:28:17 GMT  
		Size: 48.7 MB (48653871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3811deb43f4603834d18cf1fe5b28601cc92f816a4dbc984fe9858936d4f44a3`  
		Last Modified: Tue, 12 Oct 2021 20:28:10 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c90d10b267c49cba83436d1bad2aa20653bde9c3681fbe2277d43a2ef691e5d`  
		Last Modified: Wed, 10 Nov 2021 03:48:30 GMT  
		Size: 21.4 MB (21436536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff182f4aaf60af77237f70493b14e2c05a22437378c9d91850db63454081120`  
		Last Modified: Wed, 10 Nov 2021 03:48:28 GMT  
		Size: 4.9 MB (4924642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.2`

```console
$ docker pull redmine@sha256:69caaf47721ed583465333ca9cbef1e39a54cfb0ca911c9eb5a65aa8b5ab698d
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

### `redmine:4.2` - linux; amd64

```console
$ docker pull redmine@sha256:23da6bbd8146ba5ebc6c565af6a4941d0a836fb5f2b3cf8281d954a84047c675
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195500650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777ff92e6fdbdb00a6ebcf1c2df29c52c4cbb171e418bcee49451b9df8ddf3b2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:20:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:20:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 15:20:38 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 15:27:24 GMT
ENV RUBY_MAJOR=2.7
# Tue, 12 Oct 2021 15:27:25 GMT
ENV RUBY_VERSION=2.7.4
# Tue, 12 Oct 2021 15:27:25 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Tue, 12 Oct 2021 15:30:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 15:30:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 15:30:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 15:30:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 15:30:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 15:30:34 GMT
CMD ["irb"]
# Tue, 12 Oct 2021 20:17:43 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 12 Oct 2021 20:18:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 20:18:13 GMT
ENV RAILS_ENV=production
# Tue, 12 Oct 2021 20:18:13 GMT
WORKDIR /usr/src/redmine
# Tue, 12 Oct 2021 20:18:14 GMT
ENV HOME=/home/redmine
# Tue, 12 Oct 2021 20:18:14 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 12 Oct 2021 20:18:15 GMT
ENV REDMINE_VERSION=4.2.3
# Tue, 12 Oct 2021 20:18:15 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Tue, 12 Oct 2021 20:18:19 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 12 Oct 2021 20:19:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Oct 2021 20:19:20 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 12 Oct 2021 20:19:20 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 12 Oct 2021 20:19:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 20:19:21 GMT
EXPOSE 3000
# Tue, 12 Oct 2021 20:19:21 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee6af487f217efc8e231b9857a8031fdf07ab0c8b30e539497893ec5287578b`  
		Last Modified: Tue, 12 Oct 2021 15:39:48 GMT  
		Size: 12.6 MB (12565186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48bb8449b0384f7addf4ec5d88d8ef088e25ca52f9299c1fca4bff3f5b2411d`  
		Last Modified: Tue, 12 Oct 2021 15:39:46 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4280126bdef2ed0df50609c224de8bcb7486f4ce6959104e588d7b147eb14f`  
		Last Modified: Tue, 12 Oct 2021 15:40:36 GMT  
		Size: 14.5 MB (14510184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4cc9067aac92ce406573f770322af2801a273925a95583e61e3ce6b568851a`  
		Last Modified: Tue, 12 Oct 2021 15:40:33 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf24873f395941528bd53ff8223d6b7799153cf8145e3b7158e496a8a4b9def`  
		Last Modified: Tue, 12 Oct 2021 20:27:17 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3deebb307eea15c0af224fa48dfa44ef5eb083d662d56e4eb24d97d503a2bb3f`  
		Last Modified: Tue, 12 Oct 2021 20:27:32 GMT  
		Size: 94.1 MB (94088542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799adc6ff62bdab4f48789fde71c3a76c4c1afa0e5288f175f5092a2e5867657`  
		Last Modified: Tue, 12 Oct 2021 20:27:14 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd34b5a0c4380ebac887ae883212d7ed6aa5e5fafbcfc5611ef03b072a3d34d`  
		Last Modified: Tue, 12 Oct 2021 20:27:15 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b355bfb624ca195d5b52d9a3257d514eff56e8b581bfd705949d266e7e1cad4`  
		Last Modified: Tue, 12 Oct 2021 20:27:15 GMT  
		Size: 3.1 MB (3063247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a87ccde718061b2b0d26691dacf79a140cd1b32f380e6c6d3a8f397be5156d44`  
		Last Modified: Tue, 12 Oct 2021 20:27:20 GMT  
		Size: 44.1 MB (44129736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e79252e1149fadd0907e406c69bd8e989028da830f9a410edb32ca9887a7d6`  
		Last Modified: Tue, 12 Oct 2021 20:27:15 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2` - linux; arm variant v5

```console
$ docker pull redmine@sha256:08f124ad97cbf3d78e62b390897fbd0a6e47f4901f4ce4f632d68de47d1236c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.0 MB (196991904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750dc7fdc53efaea0a675c5102c8cc3d6c8e5fb47e2bb056eae33416edf86f72`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 12 Oct 2021 00:51:32 GMT
ADD file:0d95eee31ffe3f4260263e4fac2a61123a4b98d2e7a67efcc7bfea338c54f41d in / 
# Tue, 12 Oct 2021 00:51:32 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 06:45:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 06:45:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 06:45:07 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 07:03:17 GMT
ENV RUBY_MAJOR=2.7
# Tue, 12 Oct 2021 07:03:17 GMT
ENV RUBY_VERSION=2.7.4
# Tue, 12 Oct 2021 07:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Tue, 12 Oct 2021 07:07:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 07:07:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 07:07:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 07:07:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 07:07:39 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 07:07:39 GMT
CMD ["irb"]
# Wed, 13 Oct 2021 03:05:01 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 13 Oct 2021 03:06:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 03:06:17 GMT
ENV RAILS_ENV=production
# Wed, 13 Oct 2021 03:06:19 GMT
WORKDIR /usr/src/redmine
# Wed, 13 Oct 2021 03:06:20 GMT
ENV HOME=/home/redmine
# Wed, 13 Oct 2021 03:06:23 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 13 Oct 2021 03:06:24 GMT
ENV REDMINE_VERSION=4.2.3
# Wed, 13 Oct 2021 03:06:25 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Wed, 13 Oct 2021 03:06:34 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 13 Oct 2021 03:13:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 13 Oct 2021 03:13:17 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 13 Oct 2021 03:13:19 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 13 Oct 2021 03:13:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Oct 2021 03:13:22 GMT
EXPOSE 3000
# Wed, 13 Oct 2021 03:13:23 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:175b083b22fb061f7d1894fe4916a2967ce636d47376da526d90d57c8f7efc60`  
		Last Modified: Tue, 12 Oct 2021 01:07:45 GMT  
		Size: 24.9 MB (24872704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed73113a2340f22427741647a89a1911c6dd067bde17833928c5d210ab93918`  
		Last Modified: Tue, 12 Oct 2021 07:31:54 GMT  
		Size: 10.3 MB (10349314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7a78f939d570718e0af30429b3118d94e3800937a469b3fca591fda6d0540e`  
		Last Modified: Tue, 12 Oct 2021 07:31:46 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854afe8d48105a800902d829046a9890cab76441d450aa59877c28405734daed`  
		Last Modified: Tue, 12 Oct 2021 07:33:59 GMT  
		Size: 13.9 MB (13871429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc97d908af060f6e00c4e7a607087a50b553e21e08c6a8c70274a3d81ea0b3ef`  
		Last Modified: Tue, 12 Oct 2021 07:33:51 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a08bb1308b5863e00403e1a34c4cb2a9aafa57091f2d1faa4936463e4f8de79`  
		Last Modified: Wed, 13 Oct 2021 03:32:03 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b177e5e016cce70192ebf1277d5a21559c74cf5aa60e6bff5dfb31a9d5767e8`  
		Last Modified: Wed, 13 Oct 2021 03:32:45 GMT  
		Size: 89.6 MB (89577077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa429c867c2a22535e2c33e168d8de14f69c6f13124dc7494d06630528d03c43`  
		Last Modified: Wed, 13 Oct 2021 03:32:01 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168fe406bb1360b18d49546d4af05cccf7fb548d99e4f4663d83dab19f23f4be`  
		Last Modified: Wed, 13 Oct 2021 03:32:01 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec2ee921f4dfd9c1a73cfe3b44b39e67f1af385494dd03e3fe1cbdc9c31aaf1`  
		Last Modified: Wed, 13 Oct 2021 03:32:04 GMT  
		Size: 3.1 MB (3063249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7892b495be3664dd078f8510b6b3222fec0b0eeceaaa8fcc540d7ced595ecf23`  
		Last Modified: Wed, 13 Oct 2021 03:32:21 GMT  
		Size: 55.3 MB (55253893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea12a2e245bbbc4585eb36f1a1709b9035c2beaac9e1be72d14f2bf9c84118e`  
		Last Modified: Wed, 13 Oct 2021 03:32:01 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2` - linux; arm variant v7

```console
$ docker pull redmine@sha256:900b0cad4acc6dc28f8f9e3279e4a10121c4d247bd540f66d7ff40fcdf914200
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.1 MB (190138732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88b04a543401c43e354aa169b439ad085b11a2b6acbde3b9a6a36f4307bec08`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 12 Oct 2021 01:29:42 GMT
ADD file:fe1eaa1b1d760b3d250cb4ac331d26a261fc569f1694bd34e146f00874dc87e5 in / 
# Tue, 12 Oct 2021 01:29:43 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 02:56:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 02:56:30 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 03:06:47 GMT
ENV RUBY_MAJOR=2.7
# Tue, 12 Oct 2021 03:06:47 GMT
ENV RUBY_VERSION=2.7.4
# Tue, 12 Oct 2021 03:06:47 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Tue, 12 Oct 2021 03:10:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 03:10:54 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 03:10:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 03:10:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 03:10:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 03:10:57 GMT
CMD ["irb"]
# Wed, 13 Oct 2021 06:34:38 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 13 Oct 2021 06:35:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 06:35:44 GMT
ENV RAILS_ENV=production
# Wed, 13 Oct 2021 06:35:45 GMT
WORKDIR /usr/src/redmine
# Wed, 13 Oct 2021 06:35:46 GMT
ENV HOME=/home/redmine
# Wed, 13 Oct 2021 06:35:48 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 13 Oct 2021 06:35:48 GMT
ENV REDMINE_VERSION=4.2.3
# Wed, 13 Oct 2021 06:35:49 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Wed, 13 Oct 2021 06:35:55 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 13 Oct 2021 06:41:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 13 Oct 2021 06:41:11 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 13 Oct 2021 06:41:11 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 13 Oct 2021 06:41:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Oct 2021 06:41:12 GMT
EXPOSE 3000
# Wed, 13 Oct 2021 06:41:13 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c0b5ba470cac8cfdae4633f5cddb3ba9350fe1d1b1507c4965a8224eb40e52c5`  
		Last Modified: Tue, 12 Oct 2021 01:45:52 GMT  
		Size: 22.7 MB (22739698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cdd321094894b78bc0792d96cf339ee9e4ce7ec18a14ea44b32cfbc809867b`  
		Last Modified: Tue, 12 Oct 2021 03:40:20 GMT  
		Size: 9.9 MB (9872904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c0e1a382b6eb02d552bdb97946d22f8b0d9b5f787b5d1b491fa3703e23d5ea`  
		Last Modified: Tue, 12 Oct 2021 03:40:13 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ab36f90d94f50bb2f0b4be72799049691d9d0f05aadbe4e5cba89a3989efd1`  
		Last Modified: Tue, 12 Oct 2021 03:41:56 GMT  
		Size: 13.8 MB (13767235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a22941e2b0ce8584f2fa791a8370a30bd3a202fa73a1dd64d00a85bf075916a`  
		Last Modified: Tue, 12 Oct 2021 03:41:49 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6828dc1bb7b47f9d60169ee81885096702049306577ce953096d5057c12e91af`  
		Last Modified: Wed, 13 Oct 2021 06:55:56 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e9962d77928a7fea0f4dd24c838a24f72da3eba59ed75e59a3557633655398`  
		Last Modified: Wed, 13 Oct 2021 06:56:52 GMT  
		Size: 85.6 MB (85590281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894593e78f4567729a26e4302a660a56ee7289a18398fb9ec5b526be2466b739`  
		Last Modified: Wed, 13 Oct 2021 06:55:55 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f705a0b143059f649ff99fd7d343002386794bfe675456f393697b71d9dbc5`  
		Last Modified: Wed, 13 Oct 2021 06:55:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14825a50627a0f65eec1cc695fb3896ea4d8a22a09fc112bc902fcbbdd53be02`  
		Last Modified: Wed, 13 Oct 2021 06:56:03 GMT  
		Size: 3.1 MB (3063246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f461661b0c3351479c43855bab9a39d5482ee87a52376bc2898c48b83ce9ada1`  
		Last Modified: Wed, 13 Oct 2021 06:56:20 GMT  
		Size: 55.1 MB (55101134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b2c0757c967dd445d6615d9fa9fcaac7b289a198fbad58001af82cc9edbbc8`  
		Last Modified: Wed, 13 Oct 2021 06:55:55 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:86d444c24d077794c0c2cc949e49527863c9ca44e518c17e370b02eb4000216a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.1 MB (202113715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42218f16d6dac2e546b0a2281ab4659b776bbf51ec6e4acfbede94911bc9dcdd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:31:02 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:41:19 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 09:41:20 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 09:41:21 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 09:43:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 09:43:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 09:43:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 09:43:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:43:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 09:43:17 GMT
CMD ["irb"]
# Wed, 17 Nov 2021 19:46:13 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 17 Nov 2021 19:46:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 19:46:40 GMT
ENV RAILS_ENV=production
# Wed, 17 Nov 2021 19:46:41 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Nov 2021 19:46:42 GMT
ENV HOME=/home/redmine
# Wed, 17 Nov 2021 19:46:44 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 17 Nov 2021 19:46:44 GMT
ENV REDMINE_VERSION=4.2.3
# Wed, 17 Nov 2021 19:46:45 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Wed, 17 Nov 2021 19:46:50 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 17 Nov 2021 19:49:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 19:49:37 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Nov 2021 19:49:38 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 17 Nov 2021 19:49:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 19:49:40 GMT
EXPOSE 3000
# Wed, 17 Nov 2021 19:49:41 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8443a8ec909433d7156b8dcbeaf77f4e53d6a44b253a3f03b95126547154d55`  
		Last Modified: Wed, 17 Nov 2021 09:51:43 GMT  
		Size: 11.3 MB (11261808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f57122fa0ffe176f788d35a4a8f12a76819fa3bab198ac16e26d2961047a1d`  
		Last Modified: Wed, 17 Nov 2021 09:51:41 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e74dfb7a4c0fdaf06af6628a5256217d8dc0d66250a1fbc0c123f00b986e22`  
		Last Modified: Wed, 17 Nov 2021 09:53:40 GMT  
		Size: 14.1 MB (14143923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb526ffb8eba3317294cf51375a464a78d261132b6b7491f254cf7a4a156682`  
		Last Modified: Wed, 17 Nov 2021 09:53:38 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21518ac2e5bab0f6dfc5e5d56cc37c2ddfe56b2be0f94f479a28844eda6b01df`  
		Last Modified: Wed, 17 Nov 2021 19:56:25 GMT  
		Size: 1.6 KB (1626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76248d3153c26ceb5416c50118694725c0c7d4ce7823824bd66101dc2c5a010d`  
		Last Modified: Wed, 17 Nov 2021 19:56:41 GMT  
		Size: 92.6 MB (92614747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31701ff7128027b1906c22a7653245cdb3cfac2d03494df00e25be248e743991`  
		Last Modified: Wed, 17 Nov 2021 19:56:23 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac4b0eb26c86bcfc93c2657dfbeb8e1d3ef40e8785866c46e13be70741ec74b`  
		Last Modified: Wed, 17 Nov 2021 19:56:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62ad39d6bc57963dc25a1ff3af302f01bf0d29bf1d984b097d829bcef8e71d3`  
		Last Modified: Wed, 17 Nov 2021 19:56:24 GMT  
		Size: 3.1 MB (3063387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c77a0ff1cda155087e0a1fd87440c1fd1f0de88ddcd0f7b027500ca9b1c5df9`  
		Last Modified: Wed, 17 Nov 2021 19:56:31 GMT  
		Size: 55.1 MB (55102701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8abe9431487572557c36e17868ec1e44d823b725205b047bd9b29f8cb63fea74`  
		Last Modified: Wed, 17 Nov 2021 19:56:23 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2` - linux; 386

```console
$ docker pull redmine@sha256:541bbc59f1f2165794af255e943fd64e76f231e68941d6e893fb057442a80b34
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.4 MB (201449024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df8a65a7d03b8eef85a6b4790bedd723f2249542a83c9e248f86e8bfe4ab2be`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 18:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 18:38:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 18:38:25 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 18:58:22 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 18:58:22 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 18:58:23 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 19:02:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 19:02:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 19:02:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 19:02:50 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 19:02:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 19:02:53 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 00:36:05 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 00:36:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 00:36:42 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 00:36:42 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 00:36:42 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 00:36:43 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 00:36:43 GMT
ENV REDMINE_VERSION=4.2.3
# Thu, 18 Nov 2021 00:36:44 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Thu, 18 Nov 2021 00:36:48 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 00:37:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 00:37:43 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 00:37:43 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 00:37:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 00:37:44 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 00:37:44 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1742b7e5e1e5bca675e7f251c9f6fe8778a1bb1548e5b418f8547277f14e2e33`  
		Last Modified: Wed, 17 Nov 2021 19:17:19 GMT  
		Size: 17.2 MB (17227026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ef5459771b89c49219d5c15641c7215faf156712422f01efee40ad955a52c5`  
		Last Modified: Wed, 17 Nov 2021 19:17:10 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b59002f4fc409c3fdcbd829fcc8f9d9186a49f4b1977b2c959714978bd07c75`  
		Last Modified: Wed, 17 Nov 2021 19:19:42 GMT  
		Size: 14.0 MB (13992752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1a3cc73f29df585791125514b63252077c65f4a1e212d1021c4e3020df3dd8`  
		Last Modified: Wed, 17 Nov 2021 19:19:39 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cff4a558af0642405c8aec1556aebdbaf4c9a86c0632d964e532934f76466c`  
		Last Modified: Thu, 18 Nov 2021 00:43:12 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700278801433da9ce13b80f7e86e2e5368cccf0e303e9862c537a154f05a540a`  
		Last Modified: Thu, 18 Nov 2021 00:43:36 GMT  
		Size: 95.7 MB (95702657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af28efd287aeb351d175e3c0f5ed184fa551cd1af7172bb7791a60a0537af9de`  
		Last Modified: Thu, 18 Nov 2021 00:43:09 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b8937baf10e23d531e21069ea81323b01572eee4aed6f64640685bb7ffaab8`  
		Last Modified: Thu, 18 Nov 2021 00:43:09 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95eb84ecf78a6f2698456d871cbe794d0bb45a6cece674d3d8251894cb1c1a01`  
		Last Modified: Thu, 18 Nov 2021 00:43:11 GMT  
		Size: 3.1 MB (3063250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676ab58b071fabf24debb26ce72f971b94290b362f51e44b6a19c2fe9b3371a9`  
		Last Modified: Thu, 18 Nov 2021 00:43:18 GMT  
		Size: 43.7 MB (43654553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e940c5fbe3e6915f01902f8855bf33b917442025553bce6ff1b11353827a7b58`  
		Last Modified: Thu, 18 Nov 2021 00:43:09 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2` - linux; ppc64le

```console
$ docker pull redmine@sha256:a4c48b2c0bbb76d20734a3239c5ff4486fb06902d9161041f74716b4da26ab4f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219642463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b21372e7251d350b037972153cf0703df9289044566d5c57094d019c86f77787`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 12 Oct 2021 01:26:46 GMT
ADD file:5526880c6f19a4b4231a8b2bd7cfc625d116764c4918eff6f0b55f8c1eb38e1a in / 
# Tue, 12 Oct 2021 01:26:50 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 18:23:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 18:24:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 18:24:11 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 18:52:55 GMT
ENV RUBY_MAJOR=2.7
# Tue, 12 Oct 2021 18:53:00 GMT
ENV RUBY_VERSION=2.7.4
# Tue, 12 Oct 2021 18:53:05 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Tue, 12 Oct 2021 18:59:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 18:59:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 18:59:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 18:59:42 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 18:59:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 18:59:55 GMT
CMD ["irb"]
# Thu, 14 Oct 2021 00:42:47 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 14 Oct 2021 00:46:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 Oct 2021 00:46:53 GMT
ENV RAILS_ENV=production
# Thu, 14 Oct 2021 00:46:59 GMT
WORKDIR /usr/src/redmine
# Thu, 14 Oct 2021 00:47:04 GMT
ENV HOME=/home/redmine
# Thu, 14 Oct 2021 00:47:16 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 14 Oct 2021 00:47:21 GMT
ENV REDMINE_VERSION=4.2.3
# Thu, 14 Oct 2021 00:47:24 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Thu, 14 Oct 2021 00:47:47 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 14 Oct 2021 00:52:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 Oct 2021 00:52:57 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 14 Oct 2021 00:53:09 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 14 Oct 2021 00:53:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Oct 2021 00:53:25 GMT
EXPOSE 3000
# Thu, 14 Oct 2021 00:53:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d69973af32573c07c8789c0f9c144a5c0b822a1e85b59db3ce9f8ebc489ce85d`  
		Last Modified: Tue, 12 Oct 2021 01:38:40 GMT  
		Size: 30.5 MB (30547197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f48a596ad1fccd3e24dcc1f65e362937ced6f5b5ab61b6eb49e8eda8a55b85`  
		Last Modified: Tue, 12 Oct 2021 19:30:52 GMT  
		Size: 12.7 MB (12705483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd72e7e6250a90b152d1d27efca928b2c1bfc949dfe1b2e9cf089acde024c098`  
		Last Modified: Tue, 12 Oct 2021 19:30:49 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421cf7b60e6ecf3d6ad60b357e419014d8f6ad271c958a247f07c42e24664d11`  
		Last Modified: Tue, 12 Oct 2021 19:32:25 GMT  
		Size: 15.0 MB (14997040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06540a2f04ef35b100c723361f0086cb3542d114ee0eea90d820e05137d9c5dc`  
		Last Modified: Tue, 12 Oct 2021 19:32:22 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2718e7a16edeab031c20f2c31cd9a6f1421c88037a4dfcf8b59604f89539cd11`  
		Last Modified: Thu, 14 Oct 2021 01:20:37 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a889dd8c5dd31d494ac35831e782d265b2bfe457db83677f7c047312896493`  
		Last Modified: Thu, 14 Oct 2021 01:21:41 GMT  
		Size: 101.3 MB (101327529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca7ef034d38ef39e783753bbb082ce26ec6fdd002cf9a68ce51058795ad8573`  
		Last Modified: Thu, 14 Oct 2021 01:20:32 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56232465c4db3849de029290c3113d2e54c170959078f1c6db79be04f25679d9`  
		Last Modified: Thu, 14 Oct 2021 01:20:32 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ee5c28f159c990af395a85aca6dd92d3e5df1db87f1d1b22dd971db191ffa0`  
		Last Modified: Thu, 14 Oct 2021 01:20:33 GMT  
		Size: 3.1 MB (3063245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8ea081b840509c49626aada5a751b15f06425894b1909de76d192b435f459d`  
		Last Modified: Thu, 14 Oct 2021 01:20:40 GMT  
		Size: 57.0 MB (56997726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33af764c7ef4e285b105b1dfdd393764172a828c880727596371b3d095e4fcd5`  
		Last Modified: Thu, 14 Oct 2021 01:20:32 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2` - linux; s390x

```console
$ docker pull redmine@sha256:49a1c1b85f8ccd222764c18d3694feaf0642800543699062e12064d13fecc636
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.9 MB (201879289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48dd54a6734cf67e04ecc514a8756a628f6b402e434e592dc8d1bf2a75b15627`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:42:59 GMT
ADD file:3ff5fbc9c53cf76aad0fe0e1a525cb0bc0d70e8f2a3d5741dfb8b3b8a9448ffd in / 
# Wed, 17 Nov 2021 02:43:00 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:21:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:21:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:21:07 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:35:52 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 09:35:52 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 09:35:52 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 09:37:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 09:37:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 09:37:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 09:37:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:37:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 09:37:16 GMT
CMD ["irb"]
# Wed, 17 Nov 2021 20:31:43 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 17 Nov 2021 20:32:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:32:10 GMT
ENV RAILS_ENV=production
# Wed, 17 Nov 2021 20:32:10 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Nov 2021 20:32:10 GMT
ENV HOME=/home/redmine
# Wed, 17 Nov 2021 20:32:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 17 Nov 2021 20:32:11 GMT
ENV REDMINE_VERSION=4.2.3
# Wed, 17 Nov 2021 20:32:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Wed, 17 Nov 2021 20:32:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 17 Nov 2021 20:34:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 20:34:07 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Nov 2021 20:34:08 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 17 Nov 2021 20:34:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 20:34:08 GMT
EXPOSE 3000
# Wed, 17 Nov 2021 20:34:08 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b8b917e61b3be882db10e68210f73caf5cc788bfb07aec0a659e30f4796b476b`  
		Last Modified: Wed, 17 Nov 2021 02:49:01 GMT  
		Size: 25.8 MB (25769063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e574c6d046371657ec033b78bc3df865890056f711b30df7505d0128446e36`  
		Last Modified: Wed, 17 Nov 2021 09:48:11 GMT  
		Size: 10.8 MB (10815243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6bfb1613df50da70222f9b1cd395c4b509f6e6631cf6a13ce6c6b9c8c4cf181`  
		Last Modified: Wed, 17 Nov 2021 09:48:09 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa70e45053269d04d1a7217aca754f0b1fd37826bacef60c3e79535af03de7e`  
		Last Modified: Wed, 17 Nov 2021 09:50:18 GMT  
		Size: 14.7 MB (14697150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f6665bc1be788124ffa49dc9aca2a874932441c39767aac3628a05b46b7f808`  
		Last Modified: Wed, 17 Nov 2021 09:50:16 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ad94a5ab88cff035b5e7ab928b3855131115a475ac3f69d13d3b648539b059`  
		Last Modified: Wed, 17 Nov 2021 20:39:22 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef81635c9981af53c3728bbbdf8957635a0b7afccb029ae985a6fe7e6ae527`  
		Last Modified: Wed, 17 Nov 2021 20:39:34 GMT  
		Size: 91.8 MB (91791039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8be6a475176385654d74664b9bc12bade950866233a6eb369175876849a61a9`  
		Last Modified: Wed, 17 Nov 2021 20:39:21 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d214f8c5411f63986c0d7ee3a9032324738c7b89be0432e0ff9616a27a72485f`  
		Last Modified: Wed, 17 Nov 2021 20:39:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a849b87f96d4317e30bb0352a51b94195d07907f8535be33300f0452e6808655`  
		Last Modified: Wed, 17 Nov 2021 20:39:21 GMT  
		Size: 3.1 MB (3063246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e05a462fbf41e321955f3c91b6791ba04c37145f855bda5355c75973c4705c2`  
		Last Modified: Wed, 17 Nov 2021 20:39:25 GMT  
		Size: 55.7 MB (55739301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f740e646b3a43cb2398040cad7d9e0ed87da62a1457bd92bcc4d0c5a0b8be27c`  
		Last Modified: Wed, 17 Nov 2021 20:39:21 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.2-alpine`

```console
$ docker pull redmine@sha256:cf4ec4d559c84d289809ddc6554057e6522d3720200a340c70ba098c12202c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.2-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:518ba4effd92c427ef19922743eea649ed001436d8a66fe0de469abb2de00949
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (149044368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48a04de41bf1795abeee36effc817551b3de5069209d3ec827816281c81211a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:28:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Sat, 13 Nov 2021 06:28:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 13 Nov 2021 06:28:18 GMT
ENV LANG=C.UTF-8
# Sat, 13 Nov 2021 06:44:36 GMT
ENV RUBY_MAJOR=2.7
# Sat, 13 Nov 2021 06:44:36 GMT
ENV RUBY_VERSION=2.7.4
# Sat, 13 Nov 2021 06:44:37 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Sat, 13 Nov 2021 06:47:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 13 Nov 2021 06:47:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 13 Nov 2021 06:47:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 13 Nov 2021 06:47:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Nov 2021 06:47:56 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 13 Nov 2021 06:47:56 GMT
CMD ["irb"]
# Sat, 13 Nov 2021 14:28:59 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 13 Nov 2021 14:29:07 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Sat, 13 Nov 2021 14:29:07 GMT
ENV RAILS_ENV=production
# Sat, 13 Nov 2021 14:29:08 GMT
WORKDIR /usr/src/redmine
# Sat, 13 Nov 2021 14:29:08 GMT
ENV HOME=/home/redmine
# Sat, 13 Nov 2021 14:29:09 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 13 Nov 2021 14:29:09 GMT
ENV REDMINE_VERSION=4.2.3
# Sat, 13 Nov 2021 14:29:09 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Sat, 13 Nov 2021 14:29:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 13 Nov 2021 14:29:13 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 13 Nov 2021 14:31:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 13 Nov 2021 14:31:21 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 13 Nov 2021 14:31:22 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Sat, 13 Nov 2021 14:31:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Nov 2021 14:31:22 GMT
EXPOSE 3000
# Sat, 13 Nov 2021 14:31:22 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86e849bc66e37f2d898daa44d76330256a48635f1100e364c0f46206fca7b71`  
		Last Modified: Sat, 13 Nov 2021 06:56:48 GMT  
		Size: 3.6 MB (3582307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a2fc84ba5b32bce31936a6fdf8121f29d2eb485f8525795df7d32046e9f856`  
		Last Modified: Sat, 13 Nov 2021 06:56:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e81c0605571c3961987ae1ce872ebef2b5bcb439010c194e90b47282556c32d`  
		Last Modified: Sat, 13 Nov 2021 06:58:25 GMT  
		Size: 14.0 MB (13994126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2814005984530d27bc89e1c810fb8cb01371038a28bc3d85a1e95b710d9e043e`  
		Last Modified: Sat, 13 Nov 2021 06:58:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e171914095295d927972128e1f66156ce389cb697d40fc6d7ea68c919861015e`  
		Last Modified: Sat, 13 Nov 2021 14:36:45 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9802858485f172f49a49aa23ebc2ef97aa9a7dff598d4d6b18f27e107ae24436`  
		Last Modified: Sat, 13 Nov 2021 14:36:55 GMT  
		Size: 69.5 MB (69548252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5b29e3b352df46dbdcf96478507ab2ace06abee4b91e86cea6852a73067d98`  
		Last Modified: Sat, 13 Nov 2021 14:36:43 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd79647c11e0ebdbaa7b41c71d969403768f7950e69f1b9eda5545fe42e86b3`  
		Last Modified: Sat, 13 Nov 2021 14:36:42 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20504c29a1f01e91c83c2e1e82a90fb05c118bbf74d44fa621ec588a179bce4b`  
		Last Modified: Sat, 13 Nov 2021 14:36:43 GMT  
		Size: 3.1 MB (3064272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7d43b9df6162fdd2b107724ff288c851a49738e7e04fa16cd34fddde661b04`  
		Last Modified: Sat, 13 Nov 2021 14:36:48 GMT  
		Size: 56.0 MB (56029256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561c4b4d66001dcdc5ff09131812075d6a6d4f6430e175565724033921e826f1`  
		Last Modified: Sat, 13 Nov 2021 14:36:42 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.2-passenger`

```console
$ docker pull redmine@sha256:0a2beba76e007d174f23a2648bb6286f22d459f02c4e52c079b233cc06019f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.2-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:5df4cc2cc1a71f5966a962dabe733bb283f5dcf2d5d79c9a624ca4d234f974b4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221663528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88e23cfd35a24f595790cf1434facb584b62ba6518a62473675f114c5bed8f2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:20:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:20:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 15:20:38 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 15:27:24 GMT
ENV RUBY_MAJOR=2.7
# Tue, 12 Oct 2021 15:27:25 GMT
ENV RUBY_VERSION=2.7.4
# Tue, 12 Oct 2021 15:27:25 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Tue, 12 Oct 2021 15:30:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 15:30:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 15:30:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 15:30:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 15:30:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 15:30:34 GMT
CMD ["irb"]
# Tue, 12 Oct 2021 20:17:43 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 12 Oct 2021 20:18:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 20:18:13 GMT
ENV RAILS_ENV=production
# Tue, 12 Oct 2021 20:18:13 GMT
WORKDIR /usr/src/redmine
# Tue, 12 Oct 2021 20:18:14 GMT
ENV HOME=/home/redmine
# Tue, 12 Oct 2021 20:18:14 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 12 Oct 2021 20:18:15 GMT
ENV REDMINE_VERSION=4.2.3
# Tue, 12 Oct 2021 20:18:15 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Tue, 12 Oct 2021 20:18:19 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 12 Oct 2021 20:19:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Oct 2021 20:19:20 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 12 Oct 2021 20:19:20 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 12 Oct 2021 20:19:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 20:19:21 GMT
EXPOSE 3000
# Tue, 12 Oct 2021 20:19:21 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Wed, 10 Nov 2021 03:46:11 GMT
ENV PASSENGER_VERSION=6.0.12
# Wed, 10 Nov 2021 03:46:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 10 Nov 2021 03:46:36 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Wed, 10 Nov 2021 03:46:36 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Wed, 10 Nov 2021 03:46:36 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee6af487f217efc8e231b9857a8031fdf07ab0c8b30e539497893ec5287578b`  
		Last Modified: Tue, 12 Oct 2021 15:39:48 GMT  
		Size: 12.6 MB (12565186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48bb8449b0384f7addf4ec5d88d8ef088e25ca52f9299c1fca4bff3f5b2411d`  
		Last Modified: Tue, 12 Oct 2021 15:39:46 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4280126bdef2ed0df50609c224de8bcb7486f4ce6959104e588d7b147eb14f`  
		Last Modified: Tue, 12 Oct 2021 15:40:36 GMT  
		Size: 14.5 MB (14510184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4cc9067aac92ce406573f770322af2801a273925a95583e61e3ce6b568851a`  
		Last Modified: Tue, 12 Oct 2021 15:40:33 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf24873f395941528bd53ff8223d6b7799153cf8145e3b7158e496a8a4b9def`  
		Last Modified: Tue, 12 Oct 2021 20:27:17 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3deebb307eea15c0af224fa48dfa44ef5eb083d662d56e4eb24d97d503a2bb3f`  
		Last Modified: Tue, 12 Oct 2021 20:27:32 GMT  
		Size: 94.1 MB (94088542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799adc6ff62bdab4f48789fde71c3a76c4c1afa0e5288f175f5092a2e5867657`  
		Last Modified: Tue, 12 Oct 2021 20:27:14 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd34b5a0c4380ebac887ae883212d7ed6aa5e5fafbcfc5611ef03b072a3d34d`  
		Last Modified: Tue, 12 Oct 2021 20:27:15 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b355bfb624ca195d5b52d9a3257d514eff56e8b581bfd705949d266e7e1cad4`  
		Last Modified: Tue, 12 Oct 2021 20:27:15 GMT  
		Size: 3.1 MB (3063247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a87ccde718061b2b0d26691dacf79a140cd1b32f380e6c6d3a8f397be5156d44`  
		Last Modified: Tue, 12 Oct 2021 20:27:20 GMT  
		Size: 44.1 MB (44129736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e79252e1149fadd0907e406c69bd8e989028da830f9a410edb32ca9887a7d6`  
		Last Modified: Tue, 12 Oct 2021 20:27:15 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a284a323be9f6611677ab116846d6c4dbf712313bcce34cf3e2c684501d18e10`  
		Last Modified: Wed, 10 Nov 2021 03:48:08 GMT  
		Size: 21.2 MB (21238255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebe82b2f5ac28b2b6826a4aec1e29a72892ccea15a741fc388f2c686094da69`  
		Last Modified: Wed, 10 Nov 2021 03:48:06 GMT  
		Size: 4.9 MB (4924623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.2.3`

```console
$ docker pull redmine@sha256:69caaf47721ed583465333ca9cbef1e39a54cfb0ca911c9eb5a65aa8b5ab698d
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

### `redmine:4.2.3` - linux; amd64

```console
$ docker pull redmine@sha256:23da6bbd8146ba5ebc6c565af6a4941d0a836fb5f2b3cf8281d954a84047c675
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195500650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777ff92e6fdbdb00a6ebcf1c2df29c52c4cbb171e418bcee49451b9df8ddf3b2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:20:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:20:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 15:20:38 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 15:27:24 GMT
ENV RUBY_MAJOR=2.7
# Tue, 12 Oct 2021 15:27:25 GMT
ENV RUBY_VERSION=2.7.4
# Tue, 12 Oct 2021 15:27:25 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Tue, 12 Oct 2021 15:30:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 15:30:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 15:30:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 15:30:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 15:30:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 15:30:34 GMT
CMD ["irb"]
# Tue, 12 Oct 2021 20:17:43 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 12 Oct 2021 20:18:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 20:18:13 GMT
ENV RAILS_ENV=production
# Tue, 12 Oct 2021 20:18:13 GMT
WORKDIR /usr/src/redmine
# Tue, 12 Oct 2021 20:18:14 GMT
ENV HOME=/home/redmine
# Tue, 12 Oct 2021 20:18:14 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 12 Oct 2021 20:18:15 GMT
ENV REDMINE_VERSION=4.2.3
# Tue, 12 Oct 2021 20:18:15 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Tue, 12 Oct 2021 20:18:19 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 12 Oct 2021 20:19:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Oct 2021 20:19:20 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 12 Oct 2021 20:19:20 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 12 Oct 2021 20:19:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 20:19:21 GMT
EXPOSE 3000
# Tue, 12 Oct 2021 20:19:21 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee6af487f217efc8e231b9857a8031fdf07ab0c8b30e539497893ec5287578b`  
		Last Modified: Tue, 12 Oct 2021 15:39:48 GMT  
		Size: 12.6 MB (12565186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48bb8449b0384f7addf4ec5d88d8ef088e25ca52f9299c1fca4bff3f5b2411d`  
		Last Modified: Tue, 12 Oct 2021 15:39:46 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4280126bdef2ed0df50609c224de8bcb7486f4ce6959104e588d7b147eb14f`  
		Last Modified: Tue, 12 Oct 2021 15:40:36 GMT  
		Size: 14.5 MB (14510184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4cc9067aac92ce406573f770322af2801a273925a95583e61e3ce6b568851a`  
		Last Modified: Tue, 12 Oct 2021 15:40:33 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf24873f395941528bd53ff8223d6b7799153cf8145e3b7158e496a8a4b9def`  
		Last Modified: Tue, 12 Oct 2021 20:27:17 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3deebb307eea15c0af224fa48dfa44ef5eb083d662d56e4eb24d97d503a2bb3f`  
		Last Modified: Tue, 12 Oct 2021 20:27:32 GMT  
		Size: 94.1 MB (94088542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799adc6ff62bdab4f48789fde71c3a76c4c1afa0e5288f175f5092a2e5867657`  
		Last Modified: Tue, 12 Oct 2021 20:27:14 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd34b5a0c4380ebac887ae883212d7ed6aa5e5fafbcfc5611ef03b072a3d34d`  
		Last Modified: Tue, 12 Oct 2021 20:27:15 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b355bfb624ca195d5b52d9a3257d514eff56e8b581bfd705949d266e7e1cad4`  
		Last Modified: Tue, 12 Oct 2021 20:27:15 GMT  
		Size: 3.1 MB (3063247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a87ccde718061b2b0d26691dacf79a140cd1b32f380e6c6d3a8f397be5156d44`  
		Last Modified: Tue, 12 Oct 2021 20:27:20 GMT  
		Size: 44.1 MB (44129736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e79252e1149fadd0907e406c69bd8e989028da830f9a410edb32ca9887a7d6`  
		Last Modified: Tue, 12 Oct 2021 20:27:15 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2.3` - linux; arm variant v5

```console
$ docker pull redmine@sha256:08f124ad97cbf3d78e62b390897fbd0a6e47f4901f4ce4f632d68de47d1236c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.0 MB (196991904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750dc7fdc53efaea0a675c5102c8cc3d6c8e5fb47e2bb056eae33416edf86f72`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 12 Oct 2021 00:51:32 GMT
ADD file:0d95eee31ffe3f4260263e4fac2a61123a4b98d2e7a67efcc7bfea338c54f41d in / 
# Tue, 12 Oct 2021 00:51:32 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 06:45:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 06:45:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 06:45:07 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 07:03:17 GMT
ENV RUBY_MAJOR=2.7
# Tue, 12 Oct 2021 07:03:17 GMT
ENV RUBY_VERSION=2.7.4
# Tue, 12 Oct 2021 07:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Tue, 12 Oct 2021 07:07:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 07:07:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 07:07:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 07:07:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 07:07:39 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 07:07:39 GMT
CMD ["irb"]
# Wed, 13 Oct 2021 03:05:01 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 13 Oct 2021 03:06:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 03:06:17 GMT
ENV RAILS_ENV=production
# Wed, 13 Oct 2021 03:06:19 GMT
WORKDIR /usr/src/redmine
# Wed, 13 Oct 2021 03:06:20 GMT
ENV HOME=/home/redmine
# Wed, 13 Oct 2021 03:06:23 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 13 Oct 2021 03:06:24 GMT
ENV REDMINE_VERSION=4.2.3
# Wed, 13 Oct 2021 03:06:25 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Wed, 13 Oct 2021 03:06:34 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 13 Oct 2021 03:13:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 13 Oct 2021 03:13:17 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 13 Oct 2021 03:13:19 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 13 Oct 2021 03:13:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Oct 2021 03:13:22 GMT
EXPOSE 3000
# Wed, 13 Oct 2021 03:13:23 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:175b083b22fb061f7d1894fe4916a2967ce636d47376da526d90d57c8f7efc60`  
		Last Modified: Tue, 12 Oct 2021 01:07:45 GMT  
		Size: 24.9 MB (24872704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed73113a2340f22427741647a89a1911c6dd067bde17833928c5d210ab93918`  
		Last Modified: Tue, 12 Oct 2021 07:31:54 GMT  
		Size: 10.3 MB (10349314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7a78f939d570718e0af30429b3118d94e3800937a469b3fca591fda6d0540e`  
		Last Modified: Tue, 12 Oct 2021 07:31:46 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854afe8d48105a800902d829046a9890cab76441d450aa59877c28405734daed`  
		Last Modified: Tue, 12 Oct 2021 07:33:59 GMT  
		Size: 13.9 MB (13871429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc97d908af060f6e00c4e7a607087a50b553e21e08c6a8c70274a3d81ea0b3ef`  
		Last Modified: Tue, 12 Oct 2021 07:33:51 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a08bb1308b5863e00403e1a34c4cb2a9aafa57091f2d1faa4936463e4f8de79`  
		Last Modified: Wed, 13 Oct 2021 03:32:03 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b177e5e016cce70192ebf1277d5a21559c74cf5aa60e6bff5dfb31a9d5767e8`  
		Last Modified: Wed, 13 Oct 2021 03:32:45 GMT  
		Size: 89.6 MB (89577077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa429c867c2a22535e2c33e168d8de14f69c6f13124dc7494d06630528d03c43`  
		Last Modified: Wed, 13 Oct 2021 03:32:01 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168fe406bb1360b18d49546d4af05cccf7fb548d99e4f4663d83dab19f23f4be`  
		Last Modified: Wed, 13 Oct 2021 03:32:01 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec2ee921f4dfd9c1a73cfe3b44b39e67f1af385494dd03e3fe1cbdc9c31aaf1`  
		Last Modified: Wed, 13 Oct 2021 03:32:04 GMT  
		Size: 3.1 MB (3063249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7892b495be3664dd078f8510b6b3222fec0b0eeceaaa8fcc540d7ced595ecf23`  
		Last Modified: Wed, 13 Oct 2021 03:32:21 GMT  
		Size: 55.3 MB (55253893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea12a2e245bbbc4585eb36f1a1709b9035c2beaac9e1be72d14f2bf9c84118e`  
		Last Modified: Wed, 13 Oct 2021 03:32:01 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2.3` - linux; arm variant v7

```console
$ docker pull redmine@sha256:900b0cad4acc6dc28f8f9e3279e4a10121c4d247bd540f66d7ff40fcdf914200
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.1 MB (190138732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88b04a543401c43e354aa169b439ad085b11a2b6acbde3b9a6a36f4307bec08`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 12 Oct 2021 01:29:42 GMT
ADD file:fe1eaa1b1d760b3d250cb4ac331d26a261fc569f1694bd34e146f00874dc87e5 in / 
# Tue, 12 Oct 2021 01:29:43 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 02:56:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 02:56:30 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 03:06:47 GMT
ENV RUBY_MAJOR=2.7
# Tue, 12 Oct 2021 03:06:47 GMT
ENV RUBY_VERSION=2.7.4
# Tue, 12 Oct 2021 03:06:47 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Tue, 12 Oct 2021 03:10:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 03:10:54 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 03:10:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 03:10:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 03:10:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 03:10:57 GMT
CMD ["irb"]
# Wed, 13 Oct 2021 06:34:38 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 13 Oct 2021 06:35:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 06:35:44 GMT
ENV RAILS_ENV=production
# Wed, 13 Oct 2021 06:35:45 GMT
WORKDIR /usr/src/redmine
# Wed, 13 Oct 2021 06:35:46 GMT
ENV HOME=/home/redmine
# Wed, 13 Oct 2021 06:35:48 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 13 Oct 2021 06:35:48 GMT
ENV REDMINE_VERSION=4.2.3
# Wed, 13 Oct 2021 06:35:49 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Wed, 13 Oct 2021 06:35:55 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 13 Oct 2021 06:41:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 13 Oct 2021 06:41:11 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 13 Oct 2021 06:41:11 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 13 Oct 2021 06:41:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Oct 2021 06:41:12 GMT
EXPOSE 3000
# Wed, 13 Oct 2021 06:41:13 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c0b5ba470cac8cfdae4633f5cddb3ba9350fe1d1b1507c4965a8224eb40e52c5`  
		Last Modified: Tue, 12 Oct 2021 01:45:52 GMT  
		Size: 22.7 MB (22739698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cdd321094894b78bc0792d96cf339ee9e4ce7ec18a14ea44b32cfbc809867b`  
		Last Modified: Tue, 12 Oct 2021 03:40:20 GMT  
		Size: 9.9 MB (9872904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c0e1a382b6eb02d552bdb97946d22f8b0d9b5f787b5d1b491fa3703e23d5ea`  
		Last Modified: Tue, 12 Oct 2021 03:40:13 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ab36f90d94f50bb2f0b4be72799049691d9d0f05aadbe4e5cba89a3989efd1`  
		Last Modified: Tue, 12 Oct 2021 03:41:56 GMT  
		Size: 13.8 MB (13767235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a22941e2b0ce8584f2fa791a8370a30bd3a202fa73a1dd64d00a85bf075916a`  
		Last Modified: Tue, 12 Oct 2021 03:41:49 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6828dc1bb7b47f9d60169ee81885096702049306577ce953096d5057c12e91af`  
		Last Modified: Wed, 13 Oct 2021 06:55:56 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e9962d77928a7fea0f4dd24c838a24f72da3eba59ed75e59a3557633655398`  
		Last Modified: Wed, 13 Oct 2021 06:56:52 GMT  
		Size: 85.6 MB (85590281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894593e78f4567729a26e4302a660a56ee7289a18398fb9ec5b526be2466b739`  
		Last Modified: Wed, 13 Oct 2021 06:55:55 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f705a0b143059f649ff99fd7d343002386794bfe675456f393697b71d9dbc5`  
		Last Modified: Wed, 13 Oct 2021 06:55:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14825a50627a0f65eec1cc695fb3896ea4d8a22a09fc112bc902fcbbdd53be02`  
		Last Modified: Wed, 13 Oct 2021 06:56:03 GMT  
		Size: 3.1 MB (3063246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f461661b0c3351479c43855bab9a39d5482ee87a52376bc2898c48b83ce9ada1`  
		Last Modified: Wed, 13 Oct 2021 06:56:20 GMT  
		Size: 55.1 MB (55101134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b2c0757c967dd445d6615d9fa9fcaac7b289a198fbad58001af82cc9edbbc8`  
		Last Modified: Wed, 13 Oct 2021 06:55:55 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2.3` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:86d444c24d077794c0c2cc949e49527863c9ca44e518c17e370b02eb4000216a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.1 MB (202113715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42218f16d6dac2e546b0a2281ab4659b776bbf51ec6e4acfbede94911bc9dcdd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:31:02 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:41:19 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 09:41:20 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 09:41:21 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 09:43:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 09:43:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 09:43:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 09:43:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:43:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 09:43:17 GMT
CMD ["irb"]
# Wed, 17 Nov 2021 19:46:13 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 17 Nov 2021 19:46:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 19:46:40 GMT
ENV RAILS_ENV=production
# Wed, 17 Nov 2021 19:46:41 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Nov 2021 19:46:42 GMT
ENV HOME=/home/redmine
# Wed, 17 Nov 2021 19:46:44 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 17 Nov 2021 19:46:44 GMT
ENV REDMINE_VERSION=4.2.3
# Wed, 17 Nov 2021 19:46:45 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Wed, 17 Nov 2021 19:46:50 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 17 Nov 2021 19:49:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 19:49:37 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Nov 2021 19:49:38 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 17 Nov 2021 19:49:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 19:49:40 GMT
EXPOSE 3000
# Wed, 17 Nov 2021 19:49:41 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8443a8ec909433d7156b8dcbeaf77f4e53d6a44b253a3f03b95126547154d55`  
		Last Modified: Wed, 17 Nov 2021 09:51:43 GMT  
		Size: 11.3 MB (11261808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f57122fa0ffe176f788d35a4a8f12a76819fa3bab198ac16e26d2961047a1d`  
		Last Modified: Wed, 17 Nov 2021 09:51:41 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e74dfb7a4c0fdaf06af6628a5256217d8dc0d66250a1fbc0c123f00b986e22`  
		Last Modified: Wed, 17 Nov 2021 09:53:40 GMT  
		Size: 14.1 MB (14143923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb526ffb8eba3317294cf51375a464a78d261132b6b7491f254cf7a4a156682`  
		Last Modified: Wed, 17 Nov 2021 09:53:38 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21518ac2e5bab0f6dfc5e5d56cc37c2ddfe56b2be0f94f479a28844eda6b01df`  
		Last Modified: Wed, 17 Nov 2021 19:56:25 GMT  
		Size: 1.6 KB (1626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76248d3153c26ceb5416c50118694725c0c7d4ce7823824bd66101dc2c5a010d`  
		Last Modified: Wed, 17 Nov 2021 19:56:41 GMT  
		Size: 92.6 MB (92614747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31701ff7128027b1906c22a7653245cdb3cfac2d03494df00e25be248e743991`  
		Last Modified: Wed, 17 Nov 2021 19:56:23 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac4b0eb26c86bcfc93c2657dfbeb8e1d3ef40e8785866c46e13be70741ec74b`  
		Last Modified: Wed, 17 Nov 2021 19:56:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62ad39d6bc57963dc25a1ff3af302f01bf0d29bf1d984b097d829bcef8e71d3`  
		Last Modified: Wed, 17 Nov 2021 19:56:24 GMT  
		Size: 3.1 MB (3063387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c77a0ff1cda155087e0a1fd87440c1fd1f0de88ddcd0f7b027500ca9b1c5df9`  
		Last Modified: Wed, 17 Nov 2021 19:56:31 GMT  
		Size: 55.1 MB (55102701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8abe9431487572557c36e17868ec1e44d823b725205b047bd9b29f8cb63fea74`  
		Last Modified: Wed, 17 Nov 2021 19:56:23 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2.3` - linux; 386

```console
$ docker pull redmine@sha256:541bbc59f1f2165794af255e943fd64e76f231e68941d6e893fb057442a80b34
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.4 MB (201449024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df8a65a7d03b8eef85a6b4790bedd723f2249542a83c9e248f86e8bfe4ab2be`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 18:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 18:38:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 18:38:25 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 18:58:22 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 18:58:22 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 18:58:23 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 19:02:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 19:02:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 19:02:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 19:02:50 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 19:02:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 19:02:53 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 00:36:05 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 00:36:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 00:36:42 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 00:36:42 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 00:36:42 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 00:36:43 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 00:36:43 GMT
ENV REDMINE_VERSION=4.2.3
# Thu, 18 Nov 2021 00:36:44 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Thu, 18 Nov 2021 00:36:48 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 00:37:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 00:37:43 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 00:37:43 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 00:37:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 00:37:44 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 00:37:44 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1742b7e5e1e5bca675e7f251c9f6fe8778a1bb1548e5b418f8547277f14e2e33`  
		Last Modified: Wed, 17 Nov 2021 19:17:19 GMT  
		Size: 17.2 MB (17227026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ef5459771b89c49219d5c15641c7215faf156712422f01efee40ad955a52c5`  
		Last Modified: Wed, 17 Nov 2021 19:17:10 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b59002f4fc409c3fdcbd829fcc8f9d9186a49f4b1977b2c959714978bd07c75`  
		Last Modified: Wed, 17 Nov 2021 19:19:42 GMT  
		Size: 14.0 MB (13992752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1a3cc73f29df585791125514b63252077c65f4a1e212d1021c4e3020df3dd8`  
		Last Modified: Wed, 17 Nov 2021 19:19:39 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cff4a558af0642405c8aec1556aebdbaf4c9a86c0632d964e532934f76466c`  
		Last Modified: Thu, 18 Nov 2021 00:43:12 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700278801433da9ce13b80f7e86e2e5368cccf0e303e9862c537a154f05a540a`  
		Last Modified: Thu, 18 Nov 2021 00:43:36 GMT  
		Size: 95.7 MB (95702657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af28efd287aeb351d175e3c0f5ed184fa551cd1af7172bb7791a60a0537af9de`  
		Last Modified: Thu, 18 Nov 2021 00:43:09 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b8937baf10e23d531e21069ea81323b01572eee4aed6f64640685bb7ffaab8`  
		Last Modified: Thu, 18 Nov 2021 00:43:09 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95eb84ecf78a6f2698456d871cbe794d0bb45a6cece674d3d8251894cb1c1a01`  
		Last Modified: Thu, 18 Nov 2021 00:43:11 GMT  
		Size: 3.1 MB (3063250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676ab58b071fabf24debb26ce72f971b94290b362f51e44b6a19c2fe9b3371a9`  
		Last Modified: Thu, 18 Nov 2021 00:43:18 GMT  
		Size: 43.7 MB (43654553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e940c5fbe3e6915f01902f8855bf33b917442025553bce6ff1b11353827a7b58`  
		Last Modified: Thu, 18 Nov 2021 00:43:09 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2.3` - linux; ppc64le

```console
$ docker pull redmine@sha256:a4c48b2c0bbb76d20734a3239c5ff4486fb06902d9161041f74716b4da26ab4f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219642463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b21372e7251d350b037972153cf0703df9289044566d5c57094d019c86f77787`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 12 Oct 2021 01:26:46 GMT
ADD file:5526880c6f19a4b4231a8b2bd7cfc625d116764c4918eff6f0b55f8c1eb38e1a in / 
# Tue, 12 Oct 2021 01:26:50 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 18:23:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 18:24:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 18:24:11 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 18:52:55 GMT
ENV RUBY_MAJOR=2.7
# Tue, 12 Oct 2021 18:53:00 GMT
ENV RUBY_VERSION=2.7.4
# Tue, 12 Oct 2021 18:53:05 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Tue, 12 Oct 2021 18:59:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 18:59:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 18:59:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 18:59:42 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 18:59:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 18:59:55 GMT
CMD ["irb"]
# Thu, 14 Oct 2021 00:42:47 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 14 Oct 2021 00:46:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 Oct 2021 00:46:53 GMT
ENV RAILS_ENV=production
# Thu, 14 Oct 2021 00:46:59 GMT
WORKDIR /usr/src/redmine
# Thu, 14 Oct 2021 00:47:04 GMT
ENV HOME=/home/redmine
# Thu, 14 Oct 2021 00:47:16 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 14 Oct 2021 00:47:21 GMT
ENV REDMINE_VERSION=4.2.3
# Thu, 14 Oct 2021 00:47:24 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Thu, 14 Oct 2021 00:47:47 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 14 Oct 2021 00:52:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 Oct 2021 00:52:57 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 14 Oct 2021 00:53:09 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 14 Oct 2021 00:53:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Oct 2021 00:53:25 GMT
EXPOSE 3000
# Thu, 14 Oct 2021 00:53:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d69973af32573c07c8789c0f9c144a5c0b822a1e85b59db3ce9f8ebc489ce85d`  
		Last Modified: Tue, 12 Oct 2021 01:38:40 GMT  
		Size: 30.5 MB (30547197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f48a596ad1fccd3e24dcc1f65e362937ced6f5b5ab61b6eb49e8eda8a55b85`  
		Last Modified: Tue, 12 Oct 2021 19:30:52 GMT  
		Size: 12.7 MB (12705483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd72e7e6250a90b152d1d27efca928b2c1bfc949dfe1b2e9cf089acde024c098`  
		Last Modified: Tue, 12 Oct 2021 19:30:49 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421cf7b60e6ecf3d6ad60b357e419014d8f6ad271c958a247f07c42e24664d11`  
		Last Modified: Tue, 12 Oct 2021 19:32:25 GMT  
		Size: 15.0 MB (14997040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06540a2f04ef35b100c723361f0086cb3542d114ee0eea90d820e05137d9c5dc`  
		Last Modified: Tue, 12 Oct 2021 19:32:22 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2718e7a16edeab031c20f2c31cd9a6f1421c88037a4dfcf8b59604f89539cd11`  
		Last Modified: Thu, 14 Oct 2021 01:20:37 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a889dd8c5dd31d494ac35831e782d265b2bfe457db83677f7c047312896493`  
		Last Modified: Thu, 14 Oct 2021 01:21:41 GMT  
		Size: 101.3 MB (101327529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca7ef034d38ef39e783753bbb082ce26ec6fdd002cf9a68ce51058795ad8573`  
		Last Modified: Thu, 14 Oct 2021 01:20:32 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56232465c4db3849de029290c3113d2e54c170959078f1c6db79be04f25679d9`  
		Last Modified: Thu, 14 Oct 2021 01:20:32 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ee5c28f159c990af395a85aca6dd92d3e5df1db87f1d1b22dd971db191ffa0`  
		Last Modified: Thu, 14 Oct 2021 01:20:33 GMT  
		Size: 3.1 MB (3063245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8ea081b840509c49626aada5a751b15f06425894b1909de76d192b435f459d`  
		Last Modified: Thu, 14 Oct 2021 01:20:40 GMT  
		Size: 57.0 MB (56997726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33af764c7ef4e285b105b1dfdd393764172a828c880727596371b3d095e4fcd5`  
		Last Modified: Thu, 14 Oct 2021 01:20:32 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2.3` - linux; s390x

```console
$ docker pull redmine@sha256:49a1c1b85f8ccd222764c18d3694feaf0642800543699062e12064d13fecc636
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.9 MB (201879289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48dd54a6734cf67e04ecc514a8756a628f6b402e434e592dc8d1bf2a75b15627`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:42:59 GMT
ADD file:3ff5fbc9c53cf76aad0fe0e1a525cb0bc0d70e8f2a3d5741dfb8b3b8a9448ffd in / 
# Wed, 17 Nov 2021 02:43:00 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:21:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:21:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:21:07 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:35:52 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 09:35:52 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 09:35:52 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 09:37:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 09:37:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 09:37:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 09:37:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:37:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 09:37:16 GMT
CMD ["irb"]
# Wed, 17 Nov 2021 20:31:43 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 17 Nov 2021 20:32:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:32:10 GMT
ENV RAILS_ENV=production
# Wed, 17 Nov 2021 20:32:10 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Nov 2021 20:32:10 GMT
ENV HOME=/home/redmine
# Wed, 17 Nov 2021 20:32:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 17 Nov 2021 20:32:11 GMT
ENV REDMINE_VERSION=4.2.3
# Wed, 17 Nov 2021 20:32:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Wed, 17 Nov 2021 20:32:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 17 Nov 2021 20:34:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 20:34:07 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Nov 2021 20:34:08 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 17 Nov 2021 20:34:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 20:34:08 GMT
EXPOSE 3000
# Wed, 17 Nov 2021 20:34:08 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b8b917e61b3be882db10e68210f73caf5cc788bfb07aec0a659e30f4796b476b`  
		Last Modified: Wed, 17 Nov 2021 02:49:01 GMT  
		Size: 25.8 MB (25769063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e574c6d046371657ec033b78bc3df865890056f711b30df7505d0128446e36`  
		Last Modified: Wed, 17 Nov 2021 09:48:11 GMT  
		Size: 10.8 MB (10815243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6bfb1613df50da70222f9b1cd395c4b509f6e6631cf6a13ce6c6b9c8c4cf181`  
		Last Modified: Wed, 17 Nov 2021 09:48:09 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa70e45053269d04d1a7217aca754f0b1fd37826bacef60c3e79535af03de7e`  
		Last Modified: Wed, 17 Nov 2021 09:50:18 GMT  
		Size: 14.7 MB (14697150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f6665bc1be788124ffa49dc9aca2a874932441c39767aac3628a05b46b7f808`  
		Last Modified: Wed, 17 Nov 2021 09:50:16 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ad94a5ab88cff035b5e7ab928b3855131115a475ac3f69d13d3b648539b059`  
		Last Modified: Wed, 17 Nov 2021 20:39:22 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef81635c9981af53c3728bbbdf8957635a0b7afccb029ae985a6fe7e6ae527`  
		Last Modified: Wed, 17 Nov 2021 20:39:34 GMT  
		Size: 91.8 MB (91791039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8be6a475176385654d74664b9bc12bade950866233a6eb369175876849a61a9`  
		Last Modified: Wed, 17 Nov 2021 20:39:21 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d214f8c5411f63986c0d7ee3a9032324738c7b89be0432e0ff9616a27a72485f`  
		Last Modified: Wed, 17 Nov 2021 20:39:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a849b87f96d4317e30bb0352a51b94195d07907f8535be33300f0452e6808655`  
		Last Modified: Wed, 17 Nov 2021 20:39:21 GMT  
		Size: 3.1 MB (3063246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e05a462fbf41e321955f3c91b6791ba04c37145f855bda5355c75973c4705c2`  
		Last Modified: Wed, 17 Nov 2021 20:39:25 GMT  
		Size: 55.7 MB (55739301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f740e646b3a43cb2398040cad7d9e0ed87da62a1457bd92bcc4d0c5a0b8be27c`  
		Last Modified: Wed, 17 Nov 2021 20:39:21 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.2.3-alpine`

```console
$ docker pull redmine@sha256:cf4ec4d559c84d289809ddc6554057e6522d3720200a340c70ba098c12202c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.2.3-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:518ba4effd92c427ef19922743eea649ed001436d8a66fe0de469abb2de00949
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (149044368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48a04de41bf1795abeee36effc817551b3de5069209d3ec827816281c81211a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:28:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Sat, 13 Nov 2021 06:28:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 13 Nov 2021 06:28:18 GMT
ENV LANG=C.UTF-8
# Sat, 13 Nov 2021 06:44:36 GMT
ENV RUBY_MAJOR=2.7
# Sat, 13 Nov 2021 06:44:36 GMT
ENV RUBY_VERSION=2.7.4
# Sat, 13 Nov 2021 06:44:37 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Sat, 13 Nov 2021 06:47:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 13 Nov 2021 06:47:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 13 Nov 2021 06:47:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 13 Nov 2021 06:47:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Nov 2021 06:47:56 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 13 Nov 2021 06:47:56 GMT
CMD ["irb"]
# Sat, 13 Nov 2021 14:28:59 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 13 Nov 2021 14:29:07 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Sat, 13 Nov 2021 14:29:07 GMT
ENV RAILS_ENV=production
# Sat, 13 Nov 2021 14:29:08 GMT
WORKDIR /usr/src/redmine
# Sat, 13 Nov 2021 14:29:08 GMT
ENV HOME=/home/redmine
# Sat, 13 Nov 2021 14:29:09 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 13 Nov 2021 14:29:09 GMT
ENV REDMINE_VERSION=4.2.3
# Sat, 13 Nov 2021 14:29:09 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Sat, 13 Nov 2021 14:29:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 13 Nov 2021 14:29:13 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 13 Nov 2021 14:31:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 13 Nov 2021 14:31:21 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 13 Nov 2021 14:31:22 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Sat, 13 Nov 2021 14:31:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Nov 2021 14:31:22 GMT
EXPOSE 3000
# Sat, 13 Nov 2021 14:31:22 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86e849bc66e37f2d898daa44d76330256a48635f1100e364c0f46206fca7b71`  
		Last Modified: Sat, 13 Nov 2021 06:56:48 GMT  
		Size: 3.6 MB (3582307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a2fc84ba5b32bce31936a6fdf8121f29d2eb485f8525795df7d32046e9f856`  
		Last Modified: Sat, 13 Nov 2021 06:56:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e81c0605571c3961987ae1ce872ebef2b5bcb439010c194e90b47282556c32d`  
		Last Modified: Sat, 13 Nov 2021 06:58:25 GMT  
		Size: 14.0 MB (13994126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2814005984530d27bc89e1c810fb8cb01371038a28bc3d85a1e95b710d9e043e`  
		Last Modified: Sat, 13 Nov 2021 06:58:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e171914095295d927972128e1f66156ce389cb697d40fc6d7ea68c919861015e`  
		Last Modified: Sat, 13 Nov 2021 14:36:45 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9802858485f172f49a49aa23ebc2ef97aa9a7dff598d4d6b18f27e107ae24436`  
		Last Modified: Sat, 13 Nov 2021 14:36:55 GMT  
		Size: 69.5 MB (69548252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5b29e3b352df46dbdcf96478507ab2ace06abee4b91e86cea6852a73067d98`  
		Last Modified: Sat, 13 Nov 2021 14:36:43 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd79647c11e0ebdbaa7b41c71d969403768f7950e69f1b9eda5545fe42e86b3`  
		Last Modified: Sat, 13 Nov 2021 14:36:42 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20504c29a1f01e91c83c2e1e82a90fb05c118bbf74d44fa621ec588a179bce4b`  
		Last Modified: Sat, 13 Nov 2021 14:36:43 GMT  
		Size: 3.1 MB (3064272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7d43b9df6162fdd2b107724ff288c851a49738e7e04fa16cd34fddde661b04`  
		Last Modified: Sat, 13 Nov 2021 14:36:48 GMT  
		Size: 56.0 MB (56029256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561c4b4d66001dcdc5ff09131812075d6a6d4f6430e175565724033921e826f1`  
		Last Modified: Sat, 13 Nov 2021 14:36:42 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.2.3-passenger`

```console
$ docker pull redmine@sha256:0a2beba76e007d174f23a2648bb6286f22d459f02c4e52c079b233cc06019f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.2.3-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:5df4cc2cc1a71f5966a962dabe733bb283f5dcf2d5d79c9a624ca4d234f974b4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221663528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88e23cfd35a24f595790cf1434facb584b62ba6518a62473675f114c5bed8f2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:20:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:20:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 15:20:38 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 15:27:24 GMT
ENV RUBY_MAJOR=2.7
# Tue, 12 Oct 2021 15:27:25 GMT
ENV RUBY_VERSION=2.7.4
# Tue, 12 Oct 2021 15:27:25 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Tue, 12 Oct 2021 15:30:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 15:30:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 15:30:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 15:30:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 15:30:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 15:30:34 GMT
CMD ["irb"]
# Tue, 12 Oct 2021 20:17:43 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 12 Oct 2021 20:18:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 20:18:13 GMT
ENV RAILS_ENV=production
# Tue, 12 Oct 2021 20:18:13 GMT
WORKDIR /usr/src/redmine
# Tue, 12 Oct 2021 20:18:14 GMT
ENV HOME=/home/redmine
# Tue, 12 Oct 2021 20:18:14 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 12 Oct 2021 20:18:15 GMT
ENV REDMINE_VERSION=4.2.3
# Tue, 12 Oct 2021 20:18:15 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Tue, 12 Oct 2021 20:18:19 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 12 Oct 2021 20:19:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Oct 2021 20:19:20 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 12 Oct 2021 20:19:20 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 12 Oct 2021 20:19:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 20:19:21 GMT
EXPOSE 3000
# Tue, 12 Oct 2021 20:19:21 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Wed, 10 Nov 2021 03:46:11 GMT
ENV PASSENGER_VERSION=6.0.12
# Wed, 10 Nov 2021 03:46:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 10 Nov 2021 03:46:36 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Wed, 10 Nov 2021 03:46:36 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Wed, 10 Nov 2021 03:46:36 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee6af487f217efc8e231b9857a8031fdf07ab0c8b30e539497893ec5287578b`  
		Last Modified: Tue, 12 Oct 2021 15:39:48 GMT  
		Size: 12.6 MB (12565186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48bb8449b0384f7addf4ec5d88d8ef088e25ca52f9299c1fca4bff3f5b2411d`  
		Last Modified: Tue, 12 Oct 2021 15:39:46 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4280126bdef2ed0df50609c224de8bcb7486f4ce6959104e588d7b147eb14f`  
		Last Modified: Tue, 12 Oct 2021 15:40:36 GMT  
		Size: 14.5 MB (14510184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4cc9067aac92ce406573f770322af2801a273925a95583e61e3ce6b568851a`  
		Last Modified: Tue, 12 Oct 2021 15:40:33 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf24873f395941528bd53ff8223d6b7799153cf8145e3b7158e496a8a4b9def`  
		Last Modified: Tue, 12 Oct 2021 20:27:17 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3deebb307eea15c0af224fa48dfa44ef5eb083d662d56e4eb24d97d503a2bb3f`  
		Last Modified: Tue, 12 Oct 2021 20:27:32 GMT  
		Size: 94.1 MB (94088542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799adc6ff62bdab4f48789fde71c3a76c4c1afa0e5288f175f5092a2e5867657`  
		Last Modified: Tue, 12 Oct 2021 20:27:14 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd34b5a0c4380ebac887ae883212d7ed6aa5e5fafbcfc5611ef03b072a3d34d`  
		Last Modified: Tue, 12 Oct 2021 20:27:15 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b355bfb624ca195d5b52d9a3257d514eff56e8b581bfd705949d266e7e1cad4`  
		Last Modified: Tue, 12 Oct 2021 20:27:15 GMT  
		Size: 3.1 MB (3063247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a87ccde718061b2b0d26691dacf79a140cd1b32f380e6c6d3a8f397be5156d44`  
		Last Modified: Tue, 12 Oct 2021 20:27:20 GMT  
		Size: 44.1 MB (44129736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e79252e1149fadd0907e406c69bd8e989028da830f9a410edb32ca9887a7d6`  
		Last Modified: Tue, 12 Oct 2021 20:27:15 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a284a323be9f6611677ab116846d6c4dbf712313bcce34cf3e2c684501d18e10`  
		Last Modified: Wed, 10 Nov 2021 03:48:08 GMT  
		Size: 21.2 MB (21238255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebe82b2f5ac28b2b6826a4aec1e29a72892ccea15a741fc388f2c686094da69`  
		Last Modified: Wed, 10 Nov 2021 03:48:06 GMT  
		Size: 4.9 MB (4924623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:alpine`

```console
$ docker pull redmine@sha256:cf4ec4d559c84d289809ddc6554057e6522d3720200a340c70ba098c12202c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:alpine` - linux; amd64

```console
$ docker pull redmine@sha256:518ba4effd92c427ef19922743eea649ed001436d8a66fe0de469abb2de00949
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (149044368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48a04de41bf1795abeee36effc817551b3de5069209d3ec827816281c81211a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:28:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Sat, 13 Nov 2021 06:28:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 13 Nov 2021 06:28:18 GMT
ENV LANG=C.UTF-8
# Sat, 13 Nov 2021 06:44:36 GMT
ENV RUBY_MAJOR=2.7
# Sat, 13 Nov 2021 06:44:36 GMT
ENV RUBY_VERSION=2.7.4
# Sat, 13 Nov 2021 06:44:37 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Sat, 13 Nov 2021 06:47:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 13 Nov 2021 06:47:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 13 Nov 2021 06:47:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 13 Nov 2021 06:47:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Nov 2021 06:47:56 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 13 Nov 2021 06:47:56 GMT
CMD ["irb"]
# Sat, 13 Nov 2021 14:28:59 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 13 Nov 2021 14:29:07 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Sat, 13 Nov 2021 14:29:07 GMT
ENV RAILS_ENV=production
# Sat, 13 Nov 2021 14:29:08 GMT
WORKDIR /usr/src/redmine
# Sat, 13 Nov 2021 14:29:08 GMT
ENV HOME=/home/redmine
# Sat, 13 Nov 2021 14:29:09 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 13 Nov 2021 14:29:09 GMT
ENV REDMINE_VERSION=4.2.3
# Sat, 13 Nov 2021 14:29:09 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Sat, 13 Nov 2021 14:29:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 13 Nov 2021 14:29:13 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 13 Nov 2021 14:31:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 13 Nov 2021 14:31:21 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 13 Nov 2021 14:31:22 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Sat, 13 Nov 2021 14:31:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Nov 2021 14:31:22 GMT
EXPOSE 3000
# Sat, 13 Nov 2021 14:31:22 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86e849bc66e37f2d898daa44d76330256a48635f1100e364c0f46206fca7b71`  
		Last Modified: Sat, 13 Nov 2021 06:56:48 GMT  
		Size: 3.6 MB (3582307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a2fc84ba5b32bce31936a6fdf8121f29d2eb485f8525795df7d32046e9f856`  
		Last Modified: Sat, 13 Nov 2021 06:56:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e81c0605571c3961987ae1ce872ebef2b5bcb439010c194e90b47282556c32d`  
		Last Modified: Sat, 13 Nov 2021 06:58:25 GMT  
		Size: 14.0 MB (13994126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2814005984530d27bc89e1c810fb8cb01371038a28bc3d85a1e95b710d9e043e`  
		Last Modified: Sat, 13 Nov 2021 06:58:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e171914095295d927972128e1f66156ce389cb697d40fc6d7ea68c919861015e`  
		Last Modified: Sat, 13 Nov 2021 14:36:45 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9802858485f172f49a49aa23ebc2ef97aa9a7dff598d4d6b18f27e107ae24436`  
		Last Modified: Sat, 13 Nov 2021 14:36:55 GMT  
		Size: 69.5 MB (69548252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5b29e3b352df46dbdcf96478507ab2ace06abee4b91e86cea6852a73067d98`  
		Last Modified: Sat, 13 Nov 2021 14:36:43 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd79647c11e0ebdbaa7b41c71d969403768f7950e69f1b9eda5545fe42e86b3`  
		Last Modified: Sat, 13 Nov 2021 14:36:42 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20504c29a1f01e91c83c2e1e82a90fb05c118bbf74d44fa621ec588a179bce4b`  
		Last Modified: Sat, 13 Nov 2021 14:36:43 GMT  
		Size: 3.1 MB (3064272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7d43b9df6162fdd2b107724ff288c851a49738e7e04fa16cd34fddde661b04`  
		Last Modified: Sat, 13 Nov 2021 14:36:48 GMT  
		Size: 56.0 MB (56029256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561c4b4d66001dcdc5ff09131812075d6a6d4f6430e175565724033921e826f1`  
		Last Modified: Sat, 13 Nov 2021 14:36:42 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:latest`

```console
$ docker pull redmine@sha256:69caaf47721ed583465333ca9cbef1e39a54cfb0ca911c9eb5a65aa8b5ab698d
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

### `redmine:latest` - linux; amd64

```console
$ docker pull redmine@sha256:23da6bbd8146ba5ebc6c565af6a4941d0a836fb5f2b3cf8281d954a84047c675
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195500650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777ff92e6fdbdb00a6ebcf1c2df29c52c4cbb171e418bcee49451b9df8ddf3b2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:20:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:20:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 15:20:38 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 15:27:24 GMT
ENV RUBY_MAJOR=2.7
# Tue, 12 Oct 2021 15:27:25 GMT
ENV RUBY_VERSION=2.7.4
# Tue, 12 Oct 2021 15:27:25 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Tue, 12 Oct 2021 15:30:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 15:30:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 15:30:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 15:30:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 15:30:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 15:30:34 GMT
CMD ["irb"]
# Tue, 12 Oct 2021 20:17:43 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 12 Oct 2021 20:18:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 20:18:13 GMT
ENV RAILS_ENV=production
# Tue, 12 Oct 2021 20:18:13 GMT
WORKDIR /usr/src/redmine
# Tue, 12 Oct 2021 20:18:14 GMT
ENV HOME=/home/redmine
# Tue, 12 Oct 2021 20:18:14 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 12 Oct 2021 20:18:15 GMT
ENV REDMINE_VERSION=4.2.3
# Tue, 12 Oct 2021 20:18:15 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Tue, 12 Oct 2021 20:18:19 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 12 Oct 2021 20:19:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Oct 2021 20:19:20 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 12 Oct 2021 20:19:20 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 12 Oct 2021 20:19:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 20:19:21 GMT
EXPOSE 3000
# Tue, 12 Oct 2021 20:19:21 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee6af487f217efc8e231b9857a8031fdf07ab0c8b30e539497893ec5287578b`  
		Last Modified: Tue, 12 Oct 2021 15:39:48 GMT  
		Size: 12.6 MB (12565186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48bb8449b0384f7addf4ec5d88d8ef088e25ca52f9299c1fca4bff3f5b2411d`  
		Last Modified: Tue, 12 Oct 2021 15:39:46 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4280126bdef2ed0df50609c224de8bcb7486f4ce6959104e588d7b147eb14f`  
		Last Modified: Tue, 12 Oct 2021 15:40:36 GMT  
		Size: 14.5 MB (14510184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4cc9067aac92ce406573f770322af2801a273925a95583e61e3ce6b568851a`  
		Last Modified: Tue, 12 Oct 2021 15:40:33 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf24873f395941528bd53ff8223d6b7799153cf8145e3b7158e496a8a4b9def`  
		Last Modified: Tue, 12 Oct 2021 20:27:17 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3deebb307eea15c0af224fa48dfa44ef5eb083d662d56e4eb24d97d503a2bb3f`  
		Last Modified: Tue, 12 Oct 2021 20:27:32 GMT  
		Size: 94.1 MB (94088542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799adc6ff62bdab4f48789fde71c3a76c4c1afa0e5288f175f5092a2e5867657`  
		Last Modified: Tue, 12 Oct 2021 20:27:14 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd34b5a0c4380ebac887ae883212d7ed6aa5e5fafbcfc5611ef03b072a3d34d`  
		Last Modified: Tue, 12 Oct 2021 20:27:15 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b355bfb624ca195d5b52d9a3257d514eff56e8b581bfd705949d266e7e1cad4`  
		Last Modified: Tue, 12 Oct 2021 20:27:15 GMT  
		Size: 3.1 MB (3063247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a87ccde718061b2b0d26691dacf79a140cd1b32f380e6c6d3a8f397be5156d44`  
		Last Modified: Tue, 12 Oct 2021 20:27:20 GMT  
		Size: 44.1 MB (44129736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e79252e1149fadd0907e406c69bd8e989028da830f9a410edb32ca9887a7d6`  
		Last Modified: Tue, 12 Oct 2021 20:27:15 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; arm variant v5

```console
$ docker pull redmine@sha256:08f124ad97cbf3d78e62b390897fbd0a6e47f4901f4ce4f632d68de47d1236c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.0 MB (196991904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750dc7fdc53efaea0a675c5102c8cc3d6c8e5fb47e2bb056eae33416edf86f72`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 12 Oct 2021 00:51:32 GMT
ADD file:0d95eee31ffe3f4260263e4fac2a61123a4b98d2e7a67efcc7bfea338c54f41d in / 
# Tue, 12 Oct 2021 00:51:32 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 06:45:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 06:45:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 06:45:07 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 07:03:17 GMT
ENV RUBY_MAJOR=2.7
# Tue, 12 Oct 2021 07:03:17 GMT
ENV RUBY_VERSION=2.7.4
# Tue, 12 Oct 2021 07:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Tue, 12 Oct 2021 07:07:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 07:07:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 07:07:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 07:07:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 07:07:39 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 07:07:39 GMT
CMD ["irb"]
# Wed, 13 Oct 2021 03:05:01 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 13 Oct 2021 03:06:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 03:06:17 GMT
ENV RAILS_ENV=production
# Wed, 13 Oct 2021 03:06:19 GMT
WORKDIR /usr/src/redmine
# Wed, 13 Oct 2021 03:06:20 GMT
ENV HOME=/home/redmine
# Wed, 13 Oct 2021 03:06:23 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 13 Oct 2021 03:06:24 GMT
ENV REDMINE_VERSION=4.2.3
# Wed, 13 Oct 2021 03:06:25 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Wed, 13 Oct 2021 03:06:34 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 13 Oct 2021 03:13:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 13 Oct 2021 03:13:17 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 13 Oct 2021 03:13:19 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 13 Oct 2021 03:13:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Oct 2021 03:13:22 GMT
EXPOSE 3000
# Wed, 13 Oct 2021 03:13:23 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:175b083b22fb061f7d1894fe4916a2967ce636d47376da526d90d57c8f7efc60`  
		Last Modified: Tue, 12 Oct 2021 01:07:45 GMT  
		Size: 24.9 MB (24872704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed73113a2340f22427741647a89a1911c6dd067bde17833928c5d210ab93918`  
		Last Modified: Tue, 12 Oct 2021 07:31:54 GMT  
		Size: 10.3 MB (10349314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7a78f939d570718e0af30429b3118d94e3800937a469b3fca591fda6d0540e`  
		Last Modified: Tue, 12 Oct 2021 07:31:46 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854afe8d48105a800902d829046a9890cab76441d450aa59877c28405734daed`  
		Last Modified: Tue, 12 Oct 2021 07:33:59 GMT  
		Size: 13.9 MB (13871429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc97d908af060f6e00c4e7a607087a50b553e21e08c6a8c70274a3d81ea0b3ef`  
		Last Modified: Tue, 12 Oct 2021 07:33:51 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a08bb1308b5863e00403e1a34c4cb2a9aafa57091f2d1faa4936463e4f8de79`  
		Last Modified: Wed, 13 Oct 2021 03:32:03 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b177e5e016cce70192ebf1277d5a21559c74cf5aa60e6bff5dfb31a9d5767e8`  
		Last Modified: Wed, 13 Oct 2021 03:32:45 GMT  
		Size: 89.6 MB (89577077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa429c867c2a22535e2c33e168d8de14f69c6f13124dc7494d06630528d03c43`  
		Last Modified: Wed, 13 Oct 2021 03:32:01 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168fe406bb1360b18d49546d4af05cccf7fb548d99e4f4663d83dab19f23f4be`  
		Last Modified: Wed, 13 Oct 2021 03:32:01 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec2ee921f4dfd9c1a73cfe3b44b39e67f1af385494dd03e3fe1cbdc9c31aaf1`  
		Last Modified: Wed, 13 Oct 2021 03:32:04 GMT  
		Size: 3.1 MB (3063249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7892b495be3664dd078f8510b6b3222fec0b0eeceaaa8fcc540d7ced595ecf23`  
		Last Modified: Wed, 13 Oct 2021 03:32:21 GMT  
		Size: 55.3 MB (55253893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea12a2e245bbbc4585eb36f1a1709b9035c2beaac9e1be72d14f2bf9c84118e`  
		Last Modified: Wed, 13 Oct 2021 03:32:01 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; arm variant v7

```console
$ docker pull redmine@sha256:900b0cad4acc6dc28f8f9e3279e4a10121c4d247bd540f66d7ff40fcdf914200
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.1 MB (190138732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88b04a543401c43e354aa169b439ad085b11a2b6acbde3b9a6a36f4307bec08`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 12 Oct 2021 01:29:42 GMT
ADD file:fe1eaa1b1d760b3d250cb4ac331d26a261fc569f1694bd34e146f00874dc87e5 in / 
# Tue, 12 Oct 2021 01:29:43 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 02:56:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 02:56:30 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 03:06:47 GMT
ENV RUBY_MAJOR=2.7
# Tue, 12 Oct 2021 03:06:47 GMT
ENV RUBY_VERSION=2.7.4
# Tue, 12 Oct 2021 03:06:47 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Tue, 12 Oct 2021 03:10:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 03:10:54 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 03:10:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 03:10:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 03:10:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 03:10:57 GMT
CMD ["irb"]
# Wed, 13 Oct 2021 06:34:38 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 13 Oct 2021 06:35:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 06:35:44 GMT
ENV RAILS_ENV=production
# Wed, 13 Oct 2021 06:35:45 GMT
WORKDIR /usr/src/redmine
# Wed, 13 Oct 2021 06:35:46 GMT
ENV HOME=/home/redmine
# Wed, 13 Oct 2021 06:35:48 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 13 Oct 2021 06:35:48 GMT
ENV REDMINE_VERSION=4.2.3
# Wed, 13 Oct 2021 06:35:49 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Wed, 13 Oct 2021 06:35:55 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 13 Oct 2021 06:41:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 13 Oct 2021 06:41:11 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 13 Oct 2021 06:41:11 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 13 Oct 2021 06:41:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Oct 2021 06:41:12 GMT
EXPOSE 3000
# Wed, 13 Oct 2021 06:41:13 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c0b5ba470cac8cfdae4633f5cddb3ba9350fe1d1b1507c4965a8224eb40e52c5`  
		Last Modified: Tue, 12 Oct 2021 01:45:52 GMT  
		Size: 22.7 MB (22739698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cdd321094894b78bc0792d96cf339ee9e4ce7ec18a14ea44b32cfbc809867b`  
		Last Modified: Tue, 12 Oct 2021 03:40:20 GMT  
		Size: 9.9 MB (9872904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c0e1a382b6eb02d552bdb97946d22f8b0d9b5f787b5d1b491fa3703e23d5ea`  
		Last Modified: Tue, 12 Oct 2021 03:40:13 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ab36f90d94f50bb2f0b4be72799049691d9d0f05aadbe4e5cba89a3989efd1`  
		Last Modified: Tue, 12 Oct 2021 03:41:56 GMT  
		Size: 13.8 MB (13767235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a22941e2b0ce8584f2fa791a8370a30bd3a202fa73a1dd64d00a85bf075916a`  
		Last Modified: Tue, 12 Oct 2021 03:41:49 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6828dc1bb7b47f9d60169ee81885096702049306577ce953096d5057c12e91af`  
		Last Modified: Wed, 13 Oct 2021 06:55:56 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e9962d77928a7fea0f4dd24c838a24f72da3eba59ed75e59a3557633655398`  
		Last Modified: Wed, 13 Oct 2021 06:56:52 GMT  
		Size: 85.6 MB (85590281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894593e78f4567729a26e4302a660a56ee7289a18398fb9ec5b526be2466b739`  
		Last Modified: Wed, 13 Oct 2021 06:55:55 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f705a0b143059f649ff99fd7d343002386794bfe675456f393697b71d9dbc5`  
		Last Modified: Wed, 13 Oct 2021 06:55:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14825a50627a0f65eec1cc695fb3896ea4d8a22a09fc112bc902fcbbdd53be02`  
		Last Modified: Wed, 13 Oct 2021 06:56:03 GMT  
		Size: 3.1 MB (3063246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f461661b0c3351479c43855bab9a39d5482ee87a52376bc2898c48b83ce9ada1`  
		Last Modified: Wed, 13 Oct 2021 06:56:20 GMT  
		Size: 55.1 MB (55101134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b2c0757c967dd445d6615d9fa9fcaac7b289a198fbad58001af82cc9edbbc8`  
		Last Modified: Wed, 13 Oct 2021 06:55:55 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:86d444c24d077794c0c2cc949e49527863c9ca44e518c17e370b02eb4000216a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.1 MB (202113715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42218f16d6dac2e546b0a2281ab4659b776bbf51ec6e4acfbede94911bc9dcdd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:31:02 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:41:19 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 09:41:20 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 09:41:21 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 09:43:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 09:43:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 09:43:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 09:43:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:43:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 09:43:17 GMT
CMD ["irb"]
# Wed, 17 Nov 2021 19:46:13 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 17 Nov 2021 19:46:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 19:46:40 GMT
ENV RAILS_ENV=production
# Wed, 17 Nov 2021 19:46:41 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Nov 2021 19:46:42 GMT
ENV HOME=/home/redmine
# Wed, 17 Nov 2021 19:46:44 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 17 Nov 2021 19:46:44 GMT
ENV REDMINE_VERSION=4.2.3
# Wed, 17 Nov 2021 19:46:45 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Wed, 17 Nov 2021 19:46:50 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 17 Nov 2021 19:49:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 19:49:37 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Nov 2021 19:49:38 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 17 Nov 2021 19:49:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 19:49:40 GMT
EXPOSE 3000
# Wed, 17 Nov 2021 19:49:41 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8443a8ec909433d7156b8dcbeaf77f4e53d6a44b253a3f03b95126547154d55`  
		Last Modified: Wed, 17 Nov 2021 09:51:43 GMT  
		Size: 11.3 MB (11261808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f57122fa0ffe176f788d35a4a8f12a76819fa3bab198ac16e26d2961047a1d`  
		Last Modified: Wed, 17 Nov 2021 09:51:41 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e74dfb7a4c0fdaf06af6628a5256217d8dc0d66250a1fbc0c123f00b986e22`  
		Last Modified: Wed, 17 Nov 2021 09:53:40 GMT  
		Size: 14.1 MB (14143923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb526ffb8eba3317294cf51375a464a78d261132b6b7491f254cf7a4a156682`  
		Last Modified: Wed, 17 Nov 2021 09:53:38 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21518ac2e5bab0f6dfc5e5d56cc37c2ddfe56b2be0f94f479a28844eda6b01df`  
		Last Modified: Wed, 17 Nov 2021 19:56:25 GMT  
		Size: 1.6 KB (1626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76248d3153c26ceb5416c50118694725c0c7d4ce7823824bd66101dc2c5a010d`  
		Last Modified: Wed, 17 Nov 2021 19:56:41 GMT  
		Size: 92.6 MB (92614747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31701ff7128027b1906c22a7653245cdb3cfac2d03494df00e25be248e743991`  
		Last Modified: Wed, 17 Nov 2021 19:56:23 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac4b0eb26c86bcfc93c2657dfbeb8e1d3ef40e8785866c46e13be70741ec74b`  
		Last Modified: Wed, 17 Nov 2021 19:56:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62ad39d6bc57963dc25a1ff3af302f01bf0d29bf1d984b097d829bcef8e71d3`  
		Last Modified: Wed, 17 Nov 2021 19:56:24 GMT  
		Size: 3.1 MB (3063387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c77a0ff1cda155087e0a1fd87440c1fd1f0de88ddcd0f7b027500ca9b1c5df9`  
		Last Modified: Wed, 17 Nov 2021 19:56:31 GMT  
		Size: 55.1 MB (55102701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8abe9431487572557c36e17868ec1e44d823b725205b047bd9b29f8cb63fea74`  
		Last Modified: Wed, 17 Nov 2021 19:56:23 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; 386

```console
$ docker pull redmine@sha256:541bbc59f1f2165794af255e943fd64e76f231e68941d6e893fb057442a80b34
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.4 MB (201449024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df8a65a7d03b8eef85a6b4790bedd723f2249542a83c9e248f86e8bfe4ab2be`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 18:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 18:38:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 18:38:25 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 18:58:22 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 18:58:22 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 18:58:23 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 19:02:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 19:02:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 19:02:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 19:02:50 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 19:02:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 19:02:53 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 00:36:05 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 00:36:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 00:36:42 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 00:36:42 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 00:36:42 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 00:36:43 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 00:36:43 GMT
ENV REDMINE_VERSION=4.2.3
# Thu, 18 Nov 2021 00:36:44 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Thu, 18 Nov 2021 00:36:48 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 00:37:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 00:37:43 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 00:37:43 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 00:37:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 00:37:44 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 00:37:44 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1742b7e5e1e5bca675e7f251c9f6fe8778a1bb1548e5b418f8547277f14e2e33`  
		Last Modified: Wed, 17 Nov 2021 19:17:19 GMT  
		Size: 17.2 MB (17227026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ef5459771b89c49219d5c15641c7215faf156712422f01efee40ad955a52c5`  
		Last Modified: Wed, 17 Nov 2021 19:17:10 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b59002f4fc409c3fdcbd829fcc8f9d9186a49f4b1977b2c959714978bd07c75`  
		Last Modified: Wed, 17 Nov 2021 19:19:42 GMT  
		Size: 14.0 MB (13992752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1a3cc73f29df585791125514b63252077c65f4a1e212d1021c4e3020df3dd8`  
		Last Modified: Wed, 17 Nov 2021 19:19:39 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cff4a558af0642405c8aec1556aebdbaf4c9a86c0632d964e532934f76466c`  
		Last Modified: Thu, 18 Nov 2021 00:43:12 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700278801433da9ce13b80f7e86e2e5368cccf0e303e9862c537a154f05a540a`  
		Last Modified: Thu, 18 Nov 2021 00:43:36 GMT  
		Size: 95.7 MB (95702657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af28efd287aeb351d175e3c0f5ed184fa551cd1af7172bb7791a60a0537af9de`  
		Last Modified: Thu, 18 Nov 2021 00:43:09 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b8937baf10e23d531e21069ea81323b01572eee4aed6f64640685bb7ffaab8`  
		Last Modified: Thu, 18 Nov 2021 00:43:09 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95eb84ecf78a6f2698456d871cbe794d0bb45a6cece674d3d8251894cb1c1a01`  
		Last Modified: Thu, 18 Nov 2021 00:43:11 GMT  
		Size: 3.1 MB (3063250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676ab58b071fabf24debb26ce72f971b94290b362f51e44b6a19c2fe9b3371a9`  
		Last Modified: Thu, 18 Nov 2021 00:43:18 GMT  
		Size: 43.7 MB (43654553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e940c5fbe3e6915f01902f8855bf33b917442025553bce6ff1b11353827a7b58`  
		Last Modified: Thu, 18 Nov 2021 00:43:09 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; ppc64le

```console
$ docker pull redmine@sha256:a4c48b2c0bbb76d20734a3239c5ff4486fb06902d9161041f74716b4da26ab4f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219642463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b21372e7251d350b037972153cf0703df9289044566d5c57094d019c86f77787`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 12 Oct 2021 01:26:46 GMT
ADD file:5526880c6f19a4b4231a8b2bd7cfc625d116764c4918eff6f0b55f8c1eb38e1a in / 
# Tue, 12 Oct 2021 01:26:50 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 18:23:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 18:24:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 18:24:11 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 18:52:55 GMT
ENV RUBY_MAJOR=2.7
# Tue, 12 Oct 2021 18:53:00 GMT
ENV RUBY_VERSION=2.7.4
# Tue, 12 Oct 2021 18:53:05 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Tue, 12 Oct 2021 18:59:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 18:59:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 18:59:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 18:59:42 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 18:59:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 18:59:55 GMT
CMD ["irb"]
# Thu, 14 Oct 2021 00:42:47 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 14 Oct 2021 00:46:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 Oct 2021 00:46:53 GMT
ENV RAILS_ENV=production
# Thu, 14 Oct 2021 00:46:59 GMT
WORKDIR /usr/src/redmine
# Thu, 14 Oct 2021 00:47:04 GMT
ENV HOME=/home/redmine
# Thu, 14 Oct 2021 00:47:16 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 14 Oct 2021 00:47:21 GMT
ENV REDMINE_VERSION=4.2.3
# Thu, 14 Oct 2021 00:47:24 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Thu, 14 Oct 2021 00:47:47 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 14 Oct 2021 00:52:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 Oct 2021 00:52:57 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 14 Oct 2021 00:53:09 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 14 Oct 2021 00:53:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Oct 2021 00:53:25 GMT
EXPOSE 3000
# Thu, 14 Oct 2021 00:53:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d69973af32573c07c8789c0f9c144a5c0b822a1e85b59db3ce9f8ebc489ce85d`  
		Last Modified: Tue, 12 Oct 2021 01:38:40 GMT  
		Size: 30.5 MB (30547197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f48a596ad1fccd3e24dcc1f65e362937ced6f5b5ab61b6eb49e8eda8a55b85`  
		Last Modified: Tue, 12 Oct 2021 19:30:52 GMT  
		Size: 12.7 MB (12705483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd72e7e6250a90b152d1d27efca928b2c1bfc949dfe1b2e9cf089acde024c098`  
		Last Modified: Tue, 12 Oct 2021 19:30:49 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421cf7b60e6ecf3d6ad60b357e419014d8f6ad271c958a247f07c42e24664d11`  
		Last Modified: Tue, 12 Oct 2021 19:32:25 GMT  
		Size: 15.0 MB (14997040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06540a2f04ef35b100c723361f0086cb3542d114ee0eea90d820e05137d9c5dc`  
		Last Modified: Tue, 12 Oct 2021 19:32:22 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2718e7a16edeab031c20f2c31cd9a6f1421c88037a4dfcf8b59604f89539cd11`  
		Last Modified: Thu, 14 Oct 2021 01:20:37 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a889dd8c5dd31d494ac35831e782d265b2bfe457db83677f7c047312896493`  
		Last Modified: Thu, 14 Oct 2021 01:21:41 GMT  
		Size: 101.3 MB (101327529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca7ef034d38ef39e783753bbb082ce26ec6fdd002cf9a68ce51058795ad8573`  
		Last Modified: Thu, 14 Oct 2021 01:20:32 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56232465c4db3849de029290c3113d2e54c170959078f1c6db79be04f25679d9`  
		Last Modified: Thu, 14 Oct 2021 01:20:32 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ee5c28f159c990af395a85aca6dd92d3e5df1db87f1d1b22dd971db191ffa0`  
		Last Modified: Thu, 14 Oct 2021 01:20:33 GMT  
		Size: 3.1 MB (3063245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8ea081b840509c49626aada5a751b15f06425894b1909de76d192b435f459d`  
		Last Modified: Thu, 14 Oct 2021 01:20:40 GMT  
		Size: 57.0 MB (56997726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33af764c7ef4e285b105b1dfdd393764172a828c880727596371b3d095e4fcd5`  
		Last Modified: Thu, 14 Oct 2021 01:20:32 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; s390x

```console
$ docker pull redmine@sha256:49a1c1b85f8ccd222764c18d3694feaf0642800543699062e12064d13fecc636
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.9 MB (201879289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48dd54a6734cf67e04ecc514a8756a628f6b402e434e592dc8d1bf2a75b15627`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:42:59 GMT
ADD file:3ff5fbc9c53cf76aad0fe0e1a525cb0bc0d70e8f2a3d5741dfb8b3b8a9448ffd in / 
# Wed, 17 Nov 2021 02:43:00 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:21:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:21:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:21:07 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:35:52 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 09:35:52 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 09:35:52 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 09:37:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 09:37:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 09:37:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 09:37:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:37:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 09:37:16 GMT
CMD ["irb"]
# Wed, 17 Nov 2021 20:31:43 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 17 Nov 2021 20:32:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:32:10 GMT
ENV RAILS_ENV=production
# Wed, 17 Nov 2021 20:32:10 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Nov 2021 20:32:10 GMT
ENV HOME=/home/redmine
# Wed, 17 Nov 2021 20:32:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 17 Nov 2021 20:32:11 GMT
ENV REDMINE_VERSION=4.2.3
# Wed, 17 Nov 2021 20:32:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Wed, 17 Nov 2021 20:32:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 17 Nov 2021 20:34:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 20:34:07 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Nov 2021 20:34:08 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 17 Nov 2021 20:34:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 20:34:08 GMT
EXPOSE 3000
# Wed, 17 Nov 2021 20:34:08 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b8b917e61b3be882db10e68210f73caf5cc788bfb07aec0a659e30f4796b476b`  
		Last Modified: Wed, 17 Nov 2021 02:49:01 GMT  
		Size: 25.8 MB (25769063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e574c6d046371657ec033b78bc3df865890056f711b30df7505d0128446e36`  
		Last Modified: Wed, 17 Nov 2021 09:48:11 GMT  
		Size: 10.8 MB (10815243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6bfb1613df50da70222f9b1cd395c4b509f6e6631cf6a13ce6c6b9c8c4cf181`  
		Last Modified: Wed, 17 Nov 2021 09:48:09 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa70e45053269d04d1a7217aca754f0b1fd37826bacef60c3e79535af03de7e`  
		Last Modified: Wed, 17 Nov 2021 09:50:18 GMT  
		Size: 14.7 MB (14697150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f6665bc1be788124ffa49dc9aca2a874932441c39767aac3628a05b46b7f808`  
		Last Modified: Wed, 17 Nov 2021 09:50:16 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ad94a5ab88cff035b5e7ab928b3855131115a475ac3f69d13d3b648539b059`  
		Last Modified: Wed, 17 Nov 2021 20:39:22 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef81635c9981af53c3728bbbdf8957635a0b7afccb029ae985a6fe7e6ae527`  
		Last Modified: Wed, 17 Nov 2021 20:39:34 GMT  
		Size: 91.8 MB (91791039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8be6a475176385654d74664b9bc12bade950866233a6eb369175876849a61a9`  
		Last Modified: Wed, 17 Nov 2021 20:39:21 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d214f8c5411f63986c0d7ee3a9032324738c7b89be0432e0ff9616a27a72485f`  
		Last Modified: Wed, 17 Nov 2021 20:39:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a849b87f96d4317e30bb0352a51b94195d07907f8535be33300f0452e6808655`  
		Last Modified: Wed, 17 Nov 2021 20:39:21 GMT  
		Size: 3.1 MB (3063246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e05a462fbf41e321955f3c91b6791ba04c37145f855bda5355c75973c4705c2`  
		Last Modified: Wed, 17 Nov 2021 20:39:25 GMT  
		Size: 55.7 MB (55739301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f740e646b3a43cb2398040cad7d9e0ed87da62a1457bd92bcc4d0c5a0b8be27c`  
		Last Modified: Wed, 17 Nov 2021 20:39:21 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:passenger`

```console
$ docker pull redmine@sha256:0a2beba76e007d174f23a2648bb6286f22d459f02c4e52c079b233cc06019f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:passenger` - linux; amd64

```console
$ docker pull redmine@sha256:5df4cc2cc1a71f5966a962dabe733bb283f5dcf2d5d79c9a624ca4d234f974b4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221663528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88e23cfd35a24f595790cf1434facb584b62ba6518a62473675f114c5bed8f2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:20:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:20:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Oct 2021 15:20:38 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 15:27:24 GMT
ENV RUBY_MAJOR=2.7
# Tue, 12 Oct 2021 15:27:25 GMT
ENV RUBY_VERSION=2.7.4
# Tue, 12 Oct 2021 15:27:25 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Tue, 12 Oct 2021 15:30:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Oct 2021 15:30:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Oct 2021 15:30:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Oct 2021 15:30:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 15:30:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Oct 2021 15:30:34 GMT
CMD ["irb"]
# Tue, 12 Oct 2021 20:17:43 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 12 Oct 2021 20:18:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 20:18:13 GMT
ENV RAILS_ENV=production
# Tue, 12 Oct 2021 20:18:13 GMT
WORKDIR /usr/src/redmine
# Tue, 12 Oct 2021 20:18:14 GMT
ENV HOME=/home/redmine
# Tue, 12 Oct 2021 20:18:14 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 12 Oct 2021 20:18:15 GMT
ENV REDMINE_VERSION=4.2.3
# Tue, 12 Oct 2021 20:18:15 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Tue, 12 Oct 2021 20:18:19 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 12 Oct 2021 20:19:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Oct 2021 20:19:20 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 12 Oct 2021 20:19:20 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 12 Oct 2021 20:19:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 20:19:21 GMT
EXPOSE 3000
# Tue, 12 Oct 2021 20:19:21 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Wed, 10 Nov 2021 03:46:11 GMT
ENV PASSENGER_VERSION=6.0.12
# Wed, 10 Nov 2021 03:46:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 10 Nov 2021 03:46:36 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Wed, 10 Nov 2021 03:46:36 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Wed, 10 Nov 2021 03:46:36 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee6af487f217efc8e231b9857a8031fdf07ab0c8b30e539497893ec5287578b`  
		Last Modified: Tue, 12 Oct 2021 15:39:48 GMT  
		Size: 12.6 MB (12565186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48bb8449b0384f7addf4ec5d88d8ef088e25ca52f9299c1fca4bff3f5b2411d`  
		Last Modified: Tue, 12 Oct 2021 15:39:46 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4280126bdef2ed0df50609c224de8bcb7486f4ce6959104e588d7b147eb14f`  
		Last Modified: Tue, 12 Oct 2021 15:40:36 GMT  
		Size: 14.5 MB (14510184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4cc9067aac92ce406573f770322af2801a273925a95583e61e3ce6b568851a`  
		Last Modified: Tue, 12 Oct 2021 15:40:33 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf24873f395941528bd53ff8223d6b7799153cf8145e3b7158e496a8a4b9def`  
		Last Modified: Tue, 12 Oct 2021 20:27:17 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3deebb307eea15c0af224fa48dfa44ef5eb083d662d56e4eb24d97d503a2bb3f`  
		Last Modified: Tue, 12 Oct 2021 20:27:32 GMT  
		Size: 94.1 MB (94088542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799adc6ff62bdab4f48789fde71c3a76c4c1afa0e5288f175f5092a2e5867657`  
		Last Modified: Tue, 12 Oct 2021 20:27:14 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd34b5a0c4380ebac887ae883212d7ed6aa5e5fafbcfc5611ef03b072a3d34d`  
		Last Modified: Tue, 12 Oct 2021 20:27:15 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b355bfb624ca195d5b52d9a3257d514eff56e8b581bfd705949d266e7e1cad4`  
		Last Modified: Tue, 12 Oct 2021 20:27:15 GMT  
		Size: 3.1 MB (3063247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a87ccde718061b2b0d26691dacf79a140cd1b32f380e6c6d3a8f397be5156d44`  
		Last Modified: Tue, 12 Oct 2021 20:27:20 GMT  
		Size: 44.1 MB (44129736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e79252e1149fadd0907e406c69bd8e989028da830f9a410edb32ca9887a7d6`  
		Last Modified: Tue, 12 Oct 2021 20:27:15 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a284a323be9f6611677ab116846d6c4dbf712313bcce34cf3e2c684501d18e10`  
		Last Modified: Wed, 10 Nov 2021 03:48:08 GMT  
		Size: 21.2 MB (21238255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebe82b2f5ac28b2b6826a4aec1e29a72892ccea15a741fc388f2c686094da69`  
		Last Modified: Wed, 10 Nov 2021 03:48:06 GMT  
		Size: 4.9 MB (4924623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
