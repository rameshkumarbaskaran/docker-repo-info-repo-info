## `redmine:4-passenger`

```console
$ docker pull redmine@sha256:6f350957341f6682156d4639cca1ef3d3b2cb9631dc0568ff73339a2fcd274a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:4-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:55106a4132d9d09c3bcb68251e3c5f56cd76e5c78f07e89c8083165ebf450317
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.6 MB (232584837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e174ab6d33dbfe65f556b2db33960fc3a953e6829643daeee55fa68cc828795`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:40 GMT
ADD file:3c32f1cd03198e141dd233a7ffd13444157d4150ad917d548f3ee9bf5953ce22 in / 
# Fri, 12 Mar 2021 02:20:41 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 16:15:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 16:15:25 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 12 Mar 2021 16:15:25 GMT
ENV LANG=C.UTF-8
# Fri, 12 Mar 2021 16:54:09 GMT
ENV RUBY_MAJOR=2.6
# Fri, 12 Mar 2021 16:54:09 GMT
ENV RUBY_VERSION=2.6.6
# Fri, 12 Mar 2021 16:54:09 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Fri, 12 Mar 2021 16:58:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 12 Mar 2021 16:58:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 12 Mar 2021 16:58:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 12 Mar 2021 16:58:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Mar 2021 16:58:08 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 12 Mar 2021 16:58:09 GMT
CMD ["irb"]
# Sat, 13 Mar 2021 11:25:24 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sat, 13 Mar 2021 11:25:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 13 Mar 2021 11:26:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 13 Mar 2021 11:26:10 GMT
ENV RAILS_ENV=production
# Sat, 13 Mar 2021 11:26:10 GMT
WORKDIR /usr/src/redmine
# Sat, 13 Mar 2021 11:26:10 GMT
ENV HOME=/home/redmine
# Sat, 13 Mar 2021 11:26:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 23 Mar 2021 01:21:00 GMT
ENV REDMINE_VERSION=4.1.2
# Tue, 23 Mar 2021 01:21:01 GMT
ENV REDMINE_DOWNLOAD_SHA256=7e22397351c53fe8fe4444c01c4e0640d9cefb17b9ac765b846df27627cd228e
# Tue, 23 Mar 2021 01:21:05 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 23 Mar 2021 01:21:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 23 Mar 2021 01:21:54 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 23 Mar 2021 01:21:54 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Tue, 23 Mar 2021 01:21:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Mar 2021 01:21:54 GMT
EXPOSE 3000
# Tue, 23 Mar 2021 01:21:54 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Tue, 23 Mar 2021 01:22:01 GMT
ENV PASSENGER_VERSION=6.0.7
# Tue, 23 Mar 2021 01:22:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 23 Mar 2021 01:22:18 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Tue, 23 Mar 2021 01:22:18 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Tue, 23 Mar 2021 01:22:18 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:6f28985ad1843afd6fd4fe0b42a30bfab63c27d302362e7341e3316e8ba25ced`  
		Last Modified: Fri, 12 Mar 2021 02:26:11 GMT  
		Size: 27.1 MB (27101001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e107a7a87f0bef018b87876281cd0516873a19cbbf3096199a6606bec53876`  
		Last Modified: Fri, 12 Mar 2021 17:42:39 GMT  
		Size: 12.6 MB (12562047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc649c5e4067af82942bb37567506edd1dc2b2addebd0d8244a7436829c09bfd`  
		Last Modified: Fri, 12 Mar 2021 17:42:35 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3509f3d9aa5157d3f68a26293887b0cd18310e5c97c6afc7857f5628335a6a`  
		Last Modified: Fri, 12 Mar 2021 17:46:05 GMT  
		Size: 21.5 MB (21451355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81cb91e58715b6f3f2ba29dfc90f2e617754906d0458aa5a47ffd09c5d94815`  
		Last Modified: Fri, 12 Mar 2021 17:46:02 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1530eeb950297354ac7d718fb42da12073143a17b7dac4fc38aaf8adf4701196`  
		Last Modified: Sat, 13 Mar 2021 11:36:15 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5228d4e99e1330964f5a2e491d9eb93011c023dbc9be980ee32613fc372aa6f6`  
		Last Modified: Sat, 13 Mar 2021 11:36:32 GMT  
		Size: 93.1 MB (93114586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afe9dbbfbe396315cc68c5f1f68f92350b4bfdc091d6f926377b45d9f64e078`  
		Last Modified: Sat, 13 Mar 2021 11:36:15 GMT  
		Size: 1.4 MB (1369646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b2105c54489b2d574a9952101274e9c98d9a4cd43b0a49ef0e8451a0331b2cd`  
		Last Modified: Sat, 13 Mar 2021 11:36:12 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b20bdc7b333011a7d23a053bb68f2553abbfaa7d40bf143f5fe4d599c15f0b`  
		Last Modified: Sat, 13 Mar 2021 11:36:12 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7793db22d886748583fd68c22b385bb6b70a52f8ef5306a2f59ed0ea0f028b48`  
		Last Modified: Tue, 23 Mar 2021 01:28:12 GMT  
		Size: 2.7 MB (2746472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcb39d80c046ecdfa301a8818e92768e3f5d83a2c95d95ed055deda1f5f27ad`  
		Last Modified: Tue, 23 Mar 2021 01:28:16 GMT  
		Size: 49.4 MB (49360832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ac76d9ac9b003cb502dd7eee33ddc99dfa68761537118fa0a34835c494c0b0`  
		Last Modified: Tue, 23 Mar 2021 01:28:10 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9f7c0b6c70529a688ed96946367ac46fa749a08c4080c9804a0c38d1a32fbf`  
		Last Modified: Tue, 23 Mar 2021 01:28:37 GMT  
		Size: 20.0 MB (19952359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6a8bcd8bfd4b9e95a82ce1d0e06ce77440af4fb9f86c7fd6d1f0ac193a38d4`  
		Last Modified: Tue, 23 Mar 2021 01:28:35 GMT  
		Size: 4.9 MB (4922044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
