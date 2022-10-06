## `redmine:4-passenger`

```console
$ docker pull redmine@sha256:08584854d87d06e0b42e7f30a205ceb441214f4b9d513dd0ec6653c1ac9e4298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:d79991fe6da55178577123e6e5c9de71a7e00a81978d9e202683f889ecba64f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234072120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802c7d8a54ce2d9562986355f98972e07c54d4e49bfde7609576b2abc1bf8ceb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 11:05:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 11:05:56 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 05 Oct 2022 11:05:56 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 11:33:37 GMT
ENV RUBY_MAJOR=2.7
# Wed, 05 Oct 2022 11:33:37 GMT
ENV RUBY_VERSION=2.7.6
# Wed, 05 Oct 2022 11:33:37 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Wed, 05 Oct 2022 11:35:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 05 Oct 2022 11:35:25 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 05 Oct 2022 11:35:25 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 05 Oct 2022 11:35:25 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 11:35:25 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 05 Oct 2022 11:35:26 GMT
CMD ["irb"]
# Thu, 06 Oct 2022 02:53:13 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 06 Oct 2022 02:53:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 02:53:39 GMT
ENV RAILS_ENV=production
# Thu, 06 Oct 2022 02:53:39 GMT
WORKDIR /usr/src/redmine
# Thu, 06 Oct 2022 02:53:39 GMT
ENV HOME=/home/redmine
# Thu, 06 Oct 2022 02:53:39 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 06 Oct 2022 02:53:39 GMT
ENV REDMINE_VERSION=4.2.8
# Thu, 06 Oct 2022 02:53:39 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.8.tar.gz
# Thu, 06 Oct 2022 02:53:40 GMT
ENV REDMINE_DOWNLOAD_SHA256=0b431c052d8fd36b93201dafaf3615cdb8d03460efcf2400e7d32662b2ab6272
# Thu, 06 Oct 2022 02:53:43 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 06 Oct 2022 02:54:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 06 Oct 2022 02:54:26 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 06 Oct 2022 02:54:26 GMT
COPY file:5ad924c6f87c91325ac6781766e5ad56444f0bea5780e13e8bed5000ee3cfc38 in / 
# Thu, 06 Oct 2022 02:54:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 06 Oct 2022 02:54:26 GMT
EXPOSE 3000
# Thu, 06 Oct 2022 02:54:26 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Thu, 06 Oct 2022 02:54:35 GMT
ENV PASSENGER_VERSION=6.0.15
# Thu, 06 Oct 2022 02:54:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 06 Oct 2022 02:54:53 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Thu, 06 Oct 2022 02:54:53 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Thu, 06 Oct 2022 02:54:53 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce28835af5d99b2e407697664a86ef4420610779f59f11955f011d80c295268`  
		Last Modified: Wed, 05 Oct 2022 11:40:48 GMT  
		Size: 10.0 MB (10019034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e8a8b49f5d9e9d09fd0704c037892ca133803d9adac1dc2657a4cab7037a50`  
		Last Modified: Wed, 05 Oct 2022 11:40:46 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc260f78004e8074ad3fa3609db727ff6f825db7116843b4a3480cd388f9cd97`  
		Last Modified: Wed, 05 Oct 2022 11:44:34 GMT  
		Size: 14.6 MB (14582391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d9bbf2db310a9719c9ca3269ff3a84b53d73202b8eba9be0e504622b1d4b4b`  
		Last Modified: Wed, 05 Oct 2022 11:44:32 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6100217c7be139fe73d10cf14899563bb327a02753b08177ab788f57263b7531`  
		Last Modified: Thu, 06 Oct 2022 02:56:21 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e76dc32a2607a6baadd0d324d9f633041f6b44182ff022f9330aa45cb0dd21`  
		Last Modified: Thu, 06 Oct 2022 02:56:36 GMT  
		Size: 102.0 MB (101992011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1d3e6bd53d2a5ee1c6ad237fd36193b3d1f9bd309fec63a509ba8f2d078a69`  
		Last Modified: Thu, 06 Oct 2022 02:56:19 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a982877333927957ea779ab1f8f954e337720bf32e5a88910ad2e06002163d5`  
		Last Modified: Thu, 06 Oct 2022 02:56:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc161cdfa277bf7626ae944f42a7e554817fbe112ed2e4f23199b98f92a11e6`  
		Last Modified: Thu, 06 Oct 2022 02:56:19 GMT  
		Size: 3.1 MB (3066588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c21fd3c7e9b9dd98c4db558e35185fec6b91db3f48d4bb82abe33419b33d51`  
		Last Modified: Thu, 06 Oct 2022 02:56:24 GMT  
		Size: 45.3 MB (45324964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:549f788bab9894cc31031c3ffd88c68d6e5728ac686a6e5cca7ba5c4c8b5168f`  
		Last Modified: Thu, 06 Oct 2022 02:56:19 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0f9fbd1aaf29f19a84a869ed822b6e34e61e6a7518b4ea98d51d782927b809`  
		Last Modified: Thu, 06 Oct 2022 02:57:01 GMT  
		Size: 22.1 MB (22115758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15035bbfe6d95767e0b5ac42a6eae7eb4d31de209d12c8afba1e418bb8b46bd`  
		Last Modified: Thu, 06 Oct 2022 02:56:59 GMT  
		Size: 5.5 MB (5546965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
