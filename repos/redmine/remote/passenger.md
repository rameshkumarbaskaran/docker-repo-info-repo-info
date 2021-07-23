## `redmine:passenger`

```console
$ docker pull redmine@sha256:4198d395967db00ec073ed9d714c41b00472e77e49b0dcae51f259d9b78dbc48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:passenger` - linux; amd64

```console
$ docker pull redmine@sha256:43a77f34a70b4e12264df8bff7377b5ae47895166cfd156a903cb28b641fec29
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.5 MB (221526503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0604330a8f415b11297aee811ea898c9a092e3255eb53a843e412e37469ba9d2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 17:20:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 17:20:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 17:20:06 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 17:25:56 GMT
ENV RUBY_MAJOR=2.7
# Thu, 22 Jul 2021 17:25:56 GMT
ENV RUBY_VERSION=2.7.4
# Thu, 22 Jul 2021 17:25:56 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Thu, 22 Jul 2021 17:28:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 17:28:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 17:28:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 17:28:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 17:28:25 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 17:28:25 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 11:03:34 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 11:04:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 11:04:03 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 11:04:03 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 11:04:03 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 11:04:04 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Fri, 23 Jul 2021 11:04:04 GMT
ENV REDMINE_VERSION=4.2.1
# Fri, 23 Jul 2021 11:04:04 GMT
ENV REDMINE_DOWNLOAD_SHA256=ad4109c3425f1cfe4c8961f6ae6494c76e20d81ed946caa1e297d9eda13b41b4
# Fri, 23 Jul 2021 11:04:08 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Fri, 23 Jul 2021 11:04:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 23 Jul 2021 11:04:49 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 23 Jul 2021 11:04:49 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Fri, 23 Jul 2021 11:04:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Jul 2021 11:04:49 GMT
EXPOSE 3000
# Fri, 23 Jul 2021 11:04:49 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Fri, 23 Jul 2021 11:04:59 GMT
ENV PASSENGER_VERSION=6.0.10
# Fri, 23 Jul 2021 11:05:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 23 Jul 2021 11:05:16 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Fri, 23 Jul 2021 11:05:17 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Fri, 23 Jul 2021 11:05:17 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603cdcbaa70592c67c84ffc51d232163508c6c3480916880fdb7820e7c9b9c17`  
		Last Modified: Thu, 22 Jul 2021 17:41:27 GMT  
		Size: 12.6 MB (12562773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d872ffd3f2a7e6eabea705393351362003a0c6bdee8956d5a53f73dd0b40be`  
		Last Modified: Thu, 22 Jul 2021 17:41:25 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e582c090726ff249b7e30253c7f0c11aa2cd14282a8b6cd0e8055c8615e5586`  
		Last Modified: Thu, 22 Jul 2021 17:42:40 GMT  
		Size: 14.5 MB (14509812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6f96a83aedee46aef2be1d4f73cc6990dc7e756981b022462100ac16fad345`  
		Last Modified: Thu, 22 Jul 2021 17:42:38 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9466f2ac94d013cc74523ee4ad44d9720c72baa51d8aecc2afcba41c3754be44`  
		Last Modified: Fri, 23 Jul 2021 11:10:32 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbad6372ccefa1ce14b5eefe2fe718c0cd234b40bf9a70e3d02e131a9dd65d26`  
		Last Modified: Fri, 23 Jul 2021 11:10:45 GMT  
		Size: 94.1 MB (94087869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b93724991108aa18238773a3122f3fcd80f69331610c0a7f00656f690ac7692`  
		Last Modified: Fri, 23 Jul 2021 11:10:29 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19466676666dc7f1a145b5b2534855e6f32c152cd3da118bc5536badc24da33d`  
		Last Modified: Fri, 23 Jul 2021 11:10:29 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc48a22ec231d5048d556cd637291655083a29acb695b0073039d36315929da`  
		Last Modified: Fri, 23 Jul 2021 11:10:29 GMT  
		Size: 3.1 MB (3058677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe00b1336ee6986b3f2923502d082ce45ebccea58e21f85ddd12812be6796e1f`  
		Last Modified: Fri, 23 Jul 2021 11:10:33 GMT  
		Size: 44.1 MB (44106755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606fe342d55cb9155ec0d7a14a371258946d43b0b4e3df44e3f1bbe9b166a5ef`  
		Last Modified: Fri, 23 Jul 2021 11:10:29 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8e911f2db9cefa3945c1c8bbcc4e9dc79575560305045da7e987dfa48fa522`  
		Last Modified: Fri, 23 Jul 2021 11:11:07 GMT  
		Size: 21.1 MB (21131293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab210a34ab4fa48ee042162c1b27897332d05666f95bb001a39f2d04a7df605`  
		Last Modified: Fri, 23 Jul 2021 11:11:05 GMT  
		Size: 4.9 MB (4919283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
