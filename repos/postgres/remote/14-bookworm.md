## `postgres:14-bookworm`

```console
$ docker pull postgres@sha256:b230cf7ed2525c578568fd33049b2b06aafed5dec00ffaa7a1972926a6243a8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `postgres:14-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:eaf356ba0881b33ba62f9e5e3a2aa60a1fb519468401445905229d3ac90a184f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.7 MB (149680391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c071c4234da39aa769b81969773f52899c41560e2f36343e75c4062ee3dde417`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Dec 2023 18:58:54 GMT
ADD file:ac3cd70031d35e46d86b876934946ffc8756de4de065fbc926dce642dac07ff3 in / 
# Mon, 11 Dec 2023 18:58:54 GMT
CMD ["bash"]
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV GOSU_VERSION=1.16
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV LANG=en_US.utf8
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PG_MAJOR=14
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PG_VERSION=14.10-1.pgdg120+1
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 11 Dec 2023 18:58:54 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 11 Dec 2023 18:58:54 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Dec 2023 18:58:54 GMT
STOPSIGNAL SIGINT
# Mon, 11 Dec 2023 18:58:54 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 11 Dec 2023 18:58:54 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:af107e978371b6cd6339127a05502c5eacd1e6b0e9eb7b2f4aa7b6fc87e2dd81`  
		Last Modified: Tue, 19 Dec 2023 01:24:59 GMT  
		Size: 29.1 MB (29125963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a726894d830e44fafcf77ee432810165e5669af82ddd72c06915c225a739aa71`  
		Last Modified: Tue, 19 Dec 2023 03:48:30 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c21c16fd9d779eac5e4c8099d376329ceeb1d4529524981c8888fe1c61ad730`  
		Last Modified: Tue, 19 Dec 2023 03:48:31 GMT  
		Size: 4.4 MB (4422579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521a66cbf5a28d9c6a6af2645729c03efbf0c2cc155a5de8b51789f30ce3ec63`  
		Last Modified: Tue, 19 Dec 2023 03:48:31 GMT  
		Size: 1.4 MB (1445247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abf98c2ddd3ed75f49935763aac327080ce0aa01c3f656d3e16818bfbf6cdbb`  
		Last Modified: Tue, 19 Dec 2023 03:48:32 GMT  
		Size: 8.1 MB (8065477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cc9552931ac6be870a3aad7409cda07e6678563d957caa847e7dc7f779ab1a`  
		Last Modified: Tue, 19 Dec 2023 03:48:32 GMT  
		Size: 1.2 MB (1195125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443cdb0b30fa4cb4dac1cbff69fc86cefcc5e2b8d34d066fca0ed1583d23a0fa`  
		Last Modified: Tue, 19 Dec 2023 03:48:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9219d8c93830f3e8ae98b22da4ea23d7c4d9ce51349495ef17bf5852664e9ba`  
		Last Modified: Tue, 19 Dec 2023 03:48:31 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c625ef496de69634f0ba06e7ef2c672ecc1aae9d9f45f2558e78f3e03f3f68cb`  
		Last Modified: Tue, 19 Dec 2023 03:48:36 GMT  
		Size: 105.4 MB (105406219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9caa61a753721da39251bf25997e9ea41d4ae61dfae0796385939eb5df1a8496`  
		Last Modified: Tue, 19 Dec 2023 03:48:33 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de07da787140572437ba3bab4b9a80d696fc9717f6cee6bec0821ff5a6df3e8e`  
		Last Modified: Tue, 19 Dec 2023 03:48:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a843a63a7b37941d8296ec0688b26d498fd26c53346bb21abf70760bc672abef`  
		Last Modified: Tue, 19 Dec 2023 03:48:33 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c934d807fbdb6d56d126fab411ec2262cba847105143deb084e5f003138b627b`  
		Last Modified: Tue, 19 Dec 2023 03:48:33 GMT  
		Size: 5.3 KB (5341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae0ca2fd85a18cc191670670a4cca7e8d82e81e691e7380fd28a464261b65d3`  
		Last Modified: Tue, 19 Dec 2023 03:48:31 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:a5c1fe883f9e2387b19aab304413cc26ee5ec400b3a4fc58be9581d2dc0c807e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4901929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90897d5364350706ef339d89e85855c43c6e4672b2a6d65205af642e9dd213f`

```dockerfile
```

-	Layers:
	-	`sha256:0ceecc2a3e4a6b104e38bdbec9f1d0688ba2ff749f175b55ea6d661b66672231`  
		Last Modified: Tue, 19 Dec 2023 03:48:31 GMT  
		Size: 4.8 MB (4847860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33cdfd42e7f2071db24b69639219fae65d0366d2645f9a9e557329a37ed02499`  
		Last Modified: Tue, 19 Dec 2023 03:48:30 GMT  
		Size: 54.1 KB (54069 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:75d13efef5852884c1aa39a4088ac47776097abf5b05f08bd7c5ec0f9bd86b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142360758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d49a1d046d919c3a7ac8e656711ad790a5c61e3be0cfc98174e24a5187f6d359`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Dec 2023 18:58:54 GMT
ADD file:9503ab966c9dd707eeccc7c2f633bccc94c199f8714ec4ff2c8b54dde3dbabf9 in / 
# Mon, 11 Dec 2023 18:58:54 GMT
CMD ["bash"]
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV GOSU_VERSION=1.16
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV LANG=en_US.utf8
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PG_MAJOR=14
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PG_VERSION=14.10-1.pgdg120+1
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 11 Dec 2023 18:58:54 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 11 Dec 2023 18:58:54 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Dec 2023 18:58:54 GMT
STOPSIGNAL SIGINT
# Mon, 11 Dec 2023 18:58:54 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 11 Dec 2023 18:58:54 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1ae9a2844c8c70942d2220553689b62e841cc706d77284fbfedbd770080fd699`  
		Last Modified: Tue, 19 Dec 2023 01:58:33 GMT  
		Size: 26.9 MB (26885440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8562258818e323a73ddb0c31f9aad6745d00db79840d539c874bbe443ae0cb0b`  
		Last Modified: Tue, 19 Dec 2023 16:26:27 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f4ae0ebcef3a24a1c7aa8bcccd14716057287082db75d3aedc37080803cc1d`  
		Last Modified: Tue, 19 Dec 2023 16:26:28 GMT  
		Size: 4.0 MB (4040554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c0d447effabeb85c059668474bc364967fc416cc6a4d3ba8c090b415ceb457`  
		Last Modified: Tue, 19 Dec 2023 16:26:28 GMT  
		Size: 1.4 MB (1422861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99854b875aacbbf2a16f6731d087ffe2d0b84954569e0c122f04909d943e3939`  
		Last Modified: Tue, 19 Dec 2023 16:26:28 GMT  
		Size: 8.1 MB (8065640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782fd948b1e3069939f324a104c412ea1910036f8eb13f230cca450c5ba9cdd0`  
		Last Modified: Tue, 19 Dec 2023 16:26:29 GMT  
		Size: 1.2 MB (1193959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa79161bb2d9691a29e379f6b2eb196735dd890ab77403002bb96f59beacb4be`  
		Last Modified: Tue, 19 Dec 2023 16:26:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3255b24598010853a039785388b60e37ff974670724c6e0e7c42bee395330c`  
		Last Modified: Tue, 19 Dec 2023 16:26:29 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb67c4aff0dc8812a8818528e90496912a1cfe97ba53df34ddf5725e71a7c239`  
		Last Modified: Tue, 19 Dec 2023 17:26:43 GMT  
		Size: 100.7 MB (100732517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f7c8fd10ff5899a8526ec85b20edf5ff21656f8f53a364f34909d8fcc4c563`  
		Last Modified: Tue, 19 Dec 2023 17:26:40 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab49638278d41add4f1a815c20458198f0ea5f961ca71a4b35df51e24a9cf68`  
		Last Modified: Tue, 19 Dec 2023 17:26:40 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4fd7fc6fa7b3a0e3ba50c6a8bb5125aa21f9337356888380b4439ecccdae58`  
		Last Modified: Tue, 19 Dec 2023 17:26:40 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401d7783cea9b5ee69f08b156d3774a76a432679e206c9abb1d3dd9f64b37c94`  
		Last Modified: Tue, 19 Dec 2023 17:26:41 GMT  
		Size: 5.3 KB (5344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b1cc27dc481beb52485316f4b22b14f83e7ff3988332e6c036908e6241d965`  
		Last Modified: Tue, 19 Dec 2023 17:26:41 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:a90f6f85cfa99e0a95fd0307390f7c61d12d3b55f1765e868a120a4cd36e47f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 KB (53899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d771c8593f02da0d680352ea2a2e834246e46494e3993eb32bbc4d6a409d64da`

```dockerfile
```

-	Layers:
	-	`sha256:704e69523d6fd88ab6b8fde881f245d31b64a168cbceb85882c0f9d84a317525`  
		Last Modified: Tue, 19 Dec 2023 17:26:39 GMT  
		Size: 53.9 KB (53899 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:3a33d738059930a725f866a7201504042cb8f1eb30a0b7f6057e1998139dc0d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137243682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c97e2fe179c5142396cfce64a1b24ca2342b0185e9027ee5d9bed5366629b2f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Dec 2023 18:58:54 GMT
ADD file:aef112919e7924ad6da32181b1df5099cd692680c104118da3a24cd4dfe55a1d in / 
# Mon, 11 Dec 2023 18:58:54 GMT
CMD ["bash"]
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV GOSU_VERSION=1.16
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV LANG=en_US.utf8
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PG_MAJOR=14
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PG_VERSION=14.10-1.pgdg120+1
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 11 Dec 2023 18:58:54 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 11 Dec 2023 18:58:54 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Dec 2023 18:58:54 GMT
STOPSIGNAL SIGINT
# Mon, 11 Dec 2023 18:58:54 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 11 Dec 2023 18:58:54 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:65ab19615c01a3b542f77fadb3bd27872b6a20cba3e9269fb951de36d8fa6805`  
		Last Modified: Tue, 19 Dec 2023 02:11:52 GMT  
		Size: 24.7 MB (24718157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491d66ed0c94e899a5fd8e5a17a823c75c97acb78b022a4f1fdac35cb1688063`  
		Last Modified: Wed, 20 Dec 2023 01:13:17 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d9841dd36b3428442ba7fb32c59874b12e4a913bbc1d92a55300ed75d5f53b`  
		Last Modified: Wed, 20 Dec 2023 01:13:18 GMT  
		Size: 3.6 MB (3645079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d8a15ede0519349a881b91b9b96be2358adfd88816c373b2b947f475a273e0`  
		Last Modified: Wed, 20 Dec 2023 01:13:18 GMT  
		Size: 1.4 MB (1412614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078f642eb031b757d7dc6ef483b17874da5ec5bf14bd5e29acb9fda0de45c76c`  
		Last Modified: Wed, 20 Dec 2023 01:13:18 GMT  
		Size: 8.1 MB (8065544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4b511b462c52b818854af4278675e64df006061696a543843fc98f44098bf5`  
		Last Modified: Wed, 20 Dec 2023 01:13:19 GMT  
		Size: 1.1 MB (1065970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb117e925b8690854d00f5198ec0f5d8e81f1517466c6505d067afead7998f0`  
		Last Modified: Wed, 20 Dec 2023 01:13:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7929050c974d6ee5dff991b59fa83b4139419f18a4ae1202b40ea74f2a055776`  
		Last Modified: Wed, 20 Dec 2023 01:13:19 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38018b7b1963e1364e70d7228b65acade9cd469ad6975144993b977e6a0ae31`  
		Last Modified: Wed, 20 Dec 2023 02:32:47 GMT  
		Size: 98.3 MB (98316532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516cfe91018a4823d0ad4a6b559c68fcac1fc1a967eef1a59545c659c23c9aaf`  
		Last Modified: Wed, 20 Dec 2023 02:32:44 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca27c5b14212cccdc3fb0fb674ead68da579d1400349857f3256767c664e963`  
		Last Modified: Wed, 20 Dec 2023 02:32:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8884cf22c5a941f364b7096b0af002e8c6e922cdef38dcbc39455b16c9e58ddb`  
		Last Modified: Wed, 20 Dec 2023 02:32:44 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f7b06ccbf7bd74f9da5fd5feccdd7601e84d1420dceb4a37921bc31480c089`  
		Last Modified: Wed, 20 Dec 2023 02:32:45 GMT  
		Size: 5.3 KB (5342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107d064ba9053185e0c2f865a072d25c18ee9099f0cf7c1f5988c07343f2c765`  
		Last Modified: Wed, 20 Dec 2023 02:32:45 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:5bb71930be7e34ace432c1a139ea7765a6a2d144c221e8e092e857285c5b8bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4914023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e9bd23fd8e1282fcf27a2adc8698353123387087a54f77433cb0f9d88a918f`

```dockerfile
```

-	Layers:
	-	`sha256:01dcf60c9f069f34b1a235509a69bfa3947bc4611e81e3fc4f9b121e53a7daee`  
		Last Modified: Wed, 20 Dec 2023 02:32:44 GMT  
		Size: 4.9 MB (4859914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce2731b825785dbc96c1da361e090d644a041156d8df627091efd26abd84017d`  
		Last Modified: Wed, 20 Dec 2023 02:32:43 GMT  
		Size: 54.1 KB (54109 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:e69ace4a0c93c46d62e5557cb6f8c5c675e525f84e2c680f8b45acd4f1584284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147876901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c81bb6a03fab27da74c6bcc934d175ed98dc3bf558d1e5b8839c72b77b21066`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Dec 2023 18:58:54 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Mon, 11 Dec 2023 18:58:54 GMT
CMD ["bash"]
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV GOSU_VERSION=1.16
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV LANG=en_US.utf8
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PG_MAJOR=14
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PG_VERSION=14.10-1.pgdg120+1
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 11 Dec 2023 18:58:54 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 11 Dec 2023 18:58:54 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Dec 2023 18:58:54 GMT
STOPSIGNAL SIGINT
# Mon, 11 Dec 2023 18:58:54 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 11 Dec 2023 18:58:54 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b20a3ade36a25ede5711ca425e17b9c06dd6a996c7084ef14a3e7f52ef03cc`  
		Last Modified: Wed, 20 Dec 2023 10:29:30 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfccb87eabcdc328dd48eccec9fc46fe2d7049796739e5d9d7696465a8fcc8d7`  
		Last Modified: Wed, 20 Dec 2023 10:29:30 GMT  
		Size: 4.4 MB (4383813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b36c21cfca38559826970ba921ac3ca6d83a9f0acd859f38ecc40f5bad4862`  
		Last Modified: Wed, 20 Dec 2023 10:29:30 GMT  
		Size: 1.4 MB (1377190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6773915c6e660566ecca8808639ff7cd4cc8301fcfd298aa48ec9135776a793`  
		Last Modified: Wed, 20 Dec 2023 10:29:31 GMT  
		Size: 8.1 MB (8065557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1622bae22c2f18d06f4adaccf2e2986b3cca09314426407fd0a05fbe6f9644`  
		Last Modified: Wed, 20 Dec 2023 10:29:31 GMT  
		Size: 1.1 MB (1107698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa0f3ae7f2701e958ef878fe4f68ffe4061c74157e5f3423787e98c3efbf7bd`  
		Last Modified: Wed, 20 Dec 2023 10:29:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e24ee29327e85e5a71cef65752487904a4d91896410fc7729aa06657d13570`  
		Last Modified: Wed, 20 Dec 2023 10:29:31 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fa4bbe48ceb9c019837656f1c91178d50944fd8c703ad0c965b22883154ada`  
		Last Modified: Wed, 20 Dec 2023 10:33:29 GMT  
		Size: 103.8 MB (103765591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce9d744dc3dcd000fc728bb237497c4751709f6a63dbfca3356b54292b40013`  
		Last Modified: Wed, 20 Dec 2023 10:33:26 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4da248f654e78dda663279e8cd1a997a34fbd6b1ba16a2d7d5f3a0a5ade5c`  
		Last Modified: Wed, 20 Dec 2023 10:33:26 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49607664d59944052bd7435cfae2f5d10f2f569bee5411b6cac8507392a311ef`  
		Last Modified: Wed, 20 Dec 2023 10:33:26 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124e1a742f37d637c3bc126faaf3690aa8325be19d992eaeb2883eee040af1e4`  
		Last Modified: Wed, 20 Dec 2023 10:33:27 GMT  
		Size: 5.3 KB (5340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a47ea26fa4457837199ccf5987bbadfde5828f3aba0c1fcbfc5c9154da3f0d`  
		Last Modified: Wed, 20 Dec 2023 10:33:27 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:f6acbce6e3bcbf40f89d6a6cca325aaf1f93d5ff8909da03519213ea1bb4c05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4907432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3977392653b3ceb2c6b36c293da902e910ce5d37168dd03598307959fd72355`

```dockerfile
```

-	Layers:
	-	`sha256:d6f4dac427147e7e6142910a4afd6a926471f884be0c4594b6bb7cc0fc65d0e8`  
		Last Modified: Wed, 20 Dec 2023 10:33:26 GMT  
		Size: 4.9 MB (4853520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0561da6d1479cf6dd5f48ab52933ad9ec0dca8ce55dcd5897a4441a5f864f835`  
		Last Modified: Wed, 20 Dec 2023 10:33:26 GMT  
		Size: 53.9 KB (53912 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:747fb65ddccc02400bab2b09c648198fa9d21f6053713ba2ea200e2312f60257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157070801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13525eb020b0694872db36ff41801df2eb43382d2531bed7eff3572008734b50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Dec 2023 18:58:54 GMT
ADD file:6f4083d57ea9644b5a827e67b0725087a15aa428272ec223ab968bf8b4623e42 in / 
# Mon, 11 Dec 2023 18:58:54 GMT
CMD ["bash"]
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV GOSU_VERSION=1.16
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV LANG=en_US.utf8
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PG_MAJOR=14
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PG_VERSION=14.10-1.pgdg120+1
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 11 Dec 2023 18:58:54 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 11 Dec 2023 18:58:54 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Dec 2023 18:58:54 GMT
STOPSIGNAL SIGINT
# Mon, 11 Dec 2023 18:58:54 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 11 Dec 2023 18:58:54 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8d4aad22fb6a12b8cc7a78d338dfb9bc2bd6d621517b374e446f2915833ea883`  
		Last Modified: Tue, 19 Dec 2023 01:43:45 GMT  
		Size: 30.1 MB (30143863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43125588b79237af0725363c5b18fe798b47bb5b9a4f13ae02965548827dd3b2`  
		Last Modified: Tue, 19 Dec 2023 04:00:31 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f127d77f7581c72dfc7ba5049c86256ae47eef03899038344ee15afdac5ab13`  
		Last Modified: Tue, 19 Dec 2023 04:00:31 GMT  
		Size: 4.8 MB (4844479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1726ecd4206596ea20d25bda52977ddc8201c7c468943a70d4bba36a3fd18bb`  
		Last Modified: Tue, 19 Dec 2023 04:00:31 GMT  
		Size: 1.4 MB (1420923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724a27ee6356ddb65547e11bf62f7f2a67f5c3783eb8623cdbfeddd36445877f`  
		Last Modified: Tue, 19 Dec 2023 04:00:32 GMT  
		Size: 8.1 MB (8065513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a440f8783ff538099757353966e24228797697a366d4949878039b4672ea8b`  
		Last Modified: Tue, 19 Dec 2023 04:00:32 GMT  
		Size: 1.1 MB (1136183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922cb6c7306d9b1e832ee4d877f351bedae78847a0ac1e4033cd9ef8581910e3`  
		Last Modified: Tue, 19 Dec 2023 04:00:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85a86c46d0d8790d603c8d408959e5d5c65f33939216db2e956e79c8e7a4e57`  
		Last Modified: Tue, 19 Dec 2023 04:00:32 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5bc5b585fc13ca7208ac90e2691ccac908963918a2504e9c57a52be0fecd093`  
		Last Modified: Tue, 19 Dec 2023 04:00:36 GMT  
		Size: 111.4 MB (111440052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce015750f1b7cc1d95bf43e5d6c367bff8f33913c89be1995b51c635ed50ef3`  
		Last Modified: Tue, 19 Dec 2023 04:00:33 GMT  
		Size: 9.5 KB (9535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f1df67afa5343190639bb324c3407dad44953bba37f048a32e9b2b0c898e49`  
		Last Modified: Tue, 19 Dec 2023 03:59:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbcb2ff51938719d9ec40a428e0959dbaa0da0b52eb10e72be85e9b7dbd37fd`  
		Last Modified: Tue, 19 Dec 2023 04:00:33 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bde3f3227cbddd6f8667ab7d6af1ea61d0235c24fc41ed1640b091af13bdd7`  
		Last Modified: Tue, 19 Dec 2023 04:00:33 GMT  
		Size: 5.3 KB (5342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8e85b3b4e2a69b0f878bf725f3ceb7cfa19cad36855bd727a602174ad4ca21`  
		Last Modified: Tue, 19 Dec 2023 04:00:34 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:16e7f4cb25bdf1a256c49d4285b3f6b4c1d1aba7681c0ac228091029fc7d25d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 KB (53802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fa381f9aa3074afbf8f497f521d61ea45a4e6965b2f8fe7bc22b2637c7105c`

```dockerfile
```

-	Layers:
	-	`sha256:30bc256cae74ee46edc8ac79c8a0590f149dbdda6ebce56d3b9cb90bdd8ef38a`  
		Last Modified: Tue, 19 Dec 2023 04:00:31 GMT  
		Size: 53.8 KB (53802 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:af43925cc153c12b486aaa5a7fc3c6381cb638b26b6475fa95cc1a33364b78c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148411420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31603c8a09bdb5b6bec87b8250636e0a49f0b7e7ea3f6804fdfb59456fe0908f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Nov 2023 04:09:50 GMT
ADD file:e093749192323dc72b60a8440ddba26c415586f618b5e107fa264ba5eb2ca7ba in / 
# Tue, 21 Nov 2023 04:09:54 GMT
CMD ["bash"]
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV GOSU_VERSION=1.16
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV LANG=en_US.utf8
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PG_MAJOR=14
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PG_VERSION=14.10-1.pgdg120+1
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 11 Dec 2023 18:58:54 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 11 Dec 2023 18:58:54 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Dec 2023 18:58:54 GMT
STOPSIGNAL SIGINT
# Mon, 11 Dec 2023 18:58:54 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 11 Dec 2023 18:58:54 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ebdff2138fee4a3ec27560ab1353dc51c12c2608ff721f5db3d24104872b702a`  
		Last Modified: Tue, 21 Nov 2023 04:20:35 GMT  
		Size: 29.1 MB (29141984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4751a8f9b59a5399e8b7e17a8be8bd1625be1d6a0119af4e4f4deb6f4c3e856`  
		Last Modified: Thu, 14 Dec 2023 20:03:34 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c439e1dc19d9efa184022d403ffe5199332a3f236c9e3c9f931beffd070b6c17`  
		Last Modified: Thu, 14 Dec 2023 20:03:35 GMT  
		Size: 4.4 MB (4355741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9891d8c32f1da206d01d7b8bde5296280f1be1832a5c938e8ad2405a66aeec7e`  
		Last Modified: Thu, 14 Dec 2023 20:03:35 GMT  
		Size: 1.3 MB (1335986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c4f29ac4e15a964e96f7ded128008abe69fdc2ac40aafb04240722a3ae91e0`  
		Last Modified: Thu, 14 Dec 2023 20:03:35 GMT  
		Size: 8.1 MB (8068091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710ac456ce453f1bf35a8525549a6259c6b252a4ae9147e99118e79053b92bc5`  
		Last Modified: Thu, 14 Dec 2023 20:03:36 GMT  
		Size: 1.2 MB (1181602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4671931e28db772abb5ccf8c6ff2e9f6c6556bba599062db0869c9e54dbd4ca`  
		Last Modified: Thu, 14 Dec 2023 20:03:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc7cffc84f4bce14c6144f372f6d93cd140aac3c7d9495ae2d2b6e033d8bf56`  
		Last Modified: Thu, 14 Dec 2023 20:03:37 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf6cff55080a05e44c7897196f44646f2b1ef9ad833b40e7b902491769bd75d`  
		Last Modified: Fri, 15 Dec 2023 01:55:44 GMT  
		Size: 104.3 MB (104308214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825dfb132ef3543f76c5d56f022539c955c7b77049302288fd5f534ee43c2f69`  
		Last Modified: Fri, 15 Dec 2023 01:55:34 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b754462e3716e08fec2ab5d466650b964009c244174acb9b3baf7e032dfb2125`  
		Last Modified: Fri, 15 Dec 2023 01:55:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f10a477dfc14b348bee0cb15698fa1342b1ad02dd21a20d5a8e6b5fd0320dd`  
		Last Modified: Fri, 15 Dec 2023 01:55:33 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040b319edb804ca65de03403c298172174e01fb67705279dfcaa468845e40ea7`  
		Last Modified: Fri, 15 Dec 2023 01:55:34 GMT  
		Size: 5.3 KB (5348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6115c3c98b3d701729253d082c60434950de0d51f8915f5fbb35da455bcbc25`  
		Last Modified: Fri, 15 Dec 2023 01:55:35 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:6c76287c5a5fefc74ff8d676f3a466a599822eb15d139616d5334c66306fac2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 KB (53777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2881fbda2446e2a779941c0cb5adc81235745bdbd28b3cf316e9eef61aa0aa`

```dockerfile
```

-	Layers:
	-	`sha256:c78229e8fc4ac3d94f6158aabef95aad0476f7acbaa4d5f78c174fee8c348c2b`  
		Last Modified: Fri, 15 Dec 2023 01:55:33 GMT  
		Size: 53.8 KB (53777 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:2ef22aca7f9d979768d531d9049206d0a19213a006f2ee6a0081ba855ac1710e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.9 MB (161917305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732f48d526fce9a1acf51fb86b844cf57a5de187b9e19ecdba9051dd19aa666b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Dec 2023 18:58:54 GMT
ADD file:ca1db68689e0b0388337ba450ad2c8e79c159c6b78f5aa6d3ff2b89b8d7edc93 in / 
# Mon, 11 Dec 2023 18:58:54 GMT
CMD ["bash"]
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV GOSU_VERSION=1.16
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV LANG=en_US.utf8
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PG_MAJOR=14
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PG_VERSION=14.10-1.pgdg120+1
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 11 Dec 2023 18:58:54 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 11 Dec 2023 18:58:54 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Dec 2023 18:58:54 GMT
STOPSIGNAL SIGINT
# Mon, 11 Dec 2023 18:58:54 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 11 Dec 2023 18:58:54 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:fc9b8f5eec3aa37ab3aace05165427479352f290d53904cea87dca6349633a09`  
		Last Modified: Tue, 19 Dec 2023 01:26:19 GMT  
		Size: 33.1 MB (33120558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9123c1be0352633684d0467d97a5ccd6ffb116db15f9856c78ed6e5aecb40b`  
		Last Modified: Wed, 20 Dec 2023 08:46:29 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ea8e7835738d6f93d9b2d157269ccaa0b534765db5e3d987c35dec7d09705e`  
		Last Modified: Wed, 20 Dec 2023 08:46:30 GMT  
		Size: 5.2 MB (5239209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da248ed325d9dcf838bf69172703afdc62d68530f83ffeb320842dca7ce89a5`  
		Last Modified: Wed, 20 Dec 2023 08:46:29 GMT  
		Size: 1.4 MB (1367714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8f40e8722080e27e4e515cb17b0e3261336494f817cd05ccedc08364ace0ad`  
		Last Modified: Wed, 20 Dec 2023 08:46:30 GMT  
		Size: 8.1 MB (8065588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2708167ad18b1b2b26e3d52daf2264bdf5f2f3af823d5850ddb041fa666b8f37`  
		Last Modified: Wed, 20 Dec 2023 08:46:30 GMT  
		Size: 1.3 MB (1282761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ea6f96ac68e2991b141ab823cbdef3416b8a3280bb0b16b0ed058c32f0e96e`  
		Last Modified: Wed, 20 Dec 2023 08:46:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3ece2039d34790a18606f054695ea6bc2206a56b9f8c105616c07d52e7dc5e`  
		Last Modified: Wed, 20 Dec 2023 08:46:31 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a72be8316f56637bbc2837e14e9703febe2beeecad985521067f2eababda8fc`  
		Last Modified: Wed, 20 Dec 2023 09:07:35 GMT  
		Size: 112.8 MB (112821689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51bd5be1eb9b005ec5801127ec5144024b9fed9911271b0d840f522c9ad4208`  
		Last Modified: Wed, 20 Dec 2023 09:07:31 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf5c8441b7deb7fecccbdc25fecccc897f30bf9ab4a90b27607402031fc2dd2`  
		Last Modified: Wed, 20 Dec 2023 09:07:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35cb5457f930fe3390fc0c6c9a7851d509064962064d6123aacf7a679ebb06b5`  
		Last Modified: Wed, 20 Dec 2023 09:07:31 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27ecb76d583c6598114743e6cb4d6ea135b553058d3aba6c0f916a888f36b80`  
		Last Modified: Wed, 20 Dec 2023 09:07:32 GMT  
		Size: 5.3 KB (5341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba69443ba4aa114c4236fa965a6a8a61f4237f18cb57eee8aea3c0a1e021361`  
		Last Modified: Wed, 20 Dec 2023 09:07:32 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:63b3ef9017fec5a930dce3931440d33bd4a29cb8249a34d323e7cca56029c986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4909051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68151a545db6ee77f4cfb233a949577ec357dd00b6c50773f70e9b3e02b4d66`

```dockerfile
```

-	Layers:
	-	`sha256:791172e9b3c6d8f75bd523cccfca7cb9718dd4b5cfeaa58e9bfc95f827d91035`  
		Last Modified: Wed, 20 Dec 2023 09:07:31 GMT  
		Size: 4.9 MB (4855089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ff051277026a43444242f8bebd36ee01e02b279200e44ae7ca4f0683ee25c1f`  
		Last Modified: Wed, 20 Dec 2023 09:07:30 GMT  
		Size: 54.0 KB (53962 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:d4f3f41de8647a66fefaa60c6c9f2c8073bbfcaf608345c80edc1633f5d1124f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155372246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a4a246f8d136eb3480acd6434e93886e080868bf8d5cb2af2db2dd4e0c266c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Dec 2023 18:58:54 GMT
ADD file:f06f12fa5a93afc3a79ac4371d24b0a471a5a1818cf34c1d90004c8f410914b9 in / 
# Mon, 11 Dec 2023 18:58:54 GMT
CMD ["bash"]
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV GOSU_VERSION=1.16
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV LANG=en_US.utf8
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PG_MAJOR=14
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PG_VERSION=14.10-1.pgdg120+1
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 11 Dec 2023 18:58:54 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 11 Dec 2023 18:58:54 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Dec 2023 18:58:54 GMT
STOPSIGNAL SIGINT
# Mon, 11 Dec 2023 18:58:54 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 11 Dec 2023 18:58:54 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bc6b1888979d3ceb063da848b2034e980e2c2613642159c1e856550b79aa620c`  
		Last Modified: Tue, 19 Dec 2023 01:47:38 GMT  
		Size: 27.5 MB (27491874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6967509bd16206b93c3024f4b68e0387925ab9e31847a1cbfcc4c1ff13958cce`  
		Last Modified: Tue, 19 Dec 2023 15:40:14 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b029f3a94337efef121f2a62bcb3207d562255d93b008f938975d3e7341c028`  
		Last Modified: Tue, 19 Dec 2023 15:40:14 GMT  
		Size: 4.3 MB (4278319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0130828c9e9eb5f4fdc3f80ae613ce551343a40f3b3237bdfe57541e7adc158`  
		Last Modified: Tue, 19 Dec 2023 15:40:14 GMT  
		Size: 1.4 MB (1411097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4772c8242ecee0922c4c63cbb8858ca706eef5887ba301ff848d1179d8ec52a0`  
		Last Modified: Tue, 19 Dec 2023 15:40:14 GMT  
		Size: 8.1 MB (8119621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec250ac8f0ae714c6024fa4447a831539d2ad20613d4987efe2d55c8064d0d37`  
		Last Modified: Tue, 19 Dec 2023 15:40:15 GMT  
		Size: 1.1 MB (1095673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25eb5ab009ec175249d042171d140b44d0e9692d98c60fcbf82f5e8690abb003`  
		Last Modified: Tue, 19 Dec 2023 15:40:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd33cdca52e6775ff1c5ae66240871a35ccf4e9101f7d0c3b2d1b5b86ad52d6c`  
		Last Modified: Tue, 19 Dec 2023 15:40:15 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb568b18a6869b29787f288ab3a6bf69624b71ea6d8d29fa159b39f0da96964`  
		Last Modified: Tue, 19 Dec 2023 15:45:37 GMT  
		Size: 113.0 MB (112955880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1149cabacb0c4996651dfd49d4394c31bca7f260edc7aabfcefdef9054a349`  
		Last Modified: Tue, 19 Dec 2023 15:45:35 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929b6bc70e511bb6d7110e549130f0a0fa4d33928be3c2652afbb2ab777691e4`  
		Last Modified: Tue, 19 Dec 2023 15:45:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24eaaa18c51fcc5dd6c693b171ae9d8bb718c80615d2e276353eeb6e0690ed7`  
		Last Modified: Tue, 19 Dec 2023 15:45:35 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af0962f593b211432b162948153df9f22b038bca1df39bc084eeb67bd1c7cae`  
		Last Modified: Tue, 19 Dec 2023 15:45:36 GMT  
		Size: 5.3 KB (5340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5c94ceb9356e5f758582d279c59b5999c1163497738960f0cdf624d7f33ea9`  
		Last Modified: Tue, 19 Dec 2023 15:45:36 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:272d7933e8135d3bd2978782c596fd90327e75bc5d142fc6930ee1a6ca9d662c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4900944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f6da458749fca7282720070debe0f7273f1abca7d2354bd480d1956c1c490b`

```dockerfile
```

-	Layers:
	-	`sha256:68bc5661bdbc0687f6ee0bd3d689705c8fff6a4b6b37e5ad8039229afa140e46`  
		Last Modified: Tue, 19 Dec 2023 15:45:35 GMT  
		Size: 4.8 MB (4847042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93ce80ef718e7e108b25e66ba5cd6ad3f7a069872c84db201aebbcdafe528034`  
		Last Modified: Tue, 19 Dec 2023 15:45:34 GMT  
		Size: 53.9 KB (53902 bytes)  
		MIME: application/vnd.in-toto+json
