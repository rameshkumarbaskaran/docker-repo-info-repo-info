## `postgres:16beta2-bullseye`

```console
$ docker pull postgres@sha256:981a3295c2b929e069f70cfd95ad07a1417b13da56fec08f954de1b7f6644155
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `postgres:16beta2-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:853cd267d457860e9375cb5915f4f3d3ae6e45be957d63c6137cd8735d857c0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135969813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a28214b7fc157b9ad6c03600285148025c520858e1dd366226d64ec1fc5f128`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:33 GMT
ADD file:10af42ddb9f028c5418d370fe2b841aa61e81f37de1ffe76900a783ba3926646 in / 
# Mon, 12 Jun 2023 23:40:33 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 10:11:36 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 13 Jun 2023 10:11:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 10:11:42 GMT
ENV GOSU_VERSION=1.16
# Tue, 13 Jun 2023 10:11:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jun 2023 10:11:55 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 13 Jun 2023 10:11:55 GMT
ENV LANG=en_US.utf8
# Tue, 13 Jun 2023 10:11:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 10:11:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jun 2023 10:12:00 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 13 Jun 2023 10:12:00 GMT
ENV PG_MAJOR=16
# Tue, 13 Jun 2023 10:12:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Tue, 04 Jul 2023 00:43:38 GMT
ENV PG_VERSION=16~beta2-1.pgdg110+1
# Tue, 04 Jul 2023 00:43:57 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 04 Jul 2023 00:43:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 04 Jul 2023 00:43:59 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 04 Jul 2023 00:44:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Jul 2023 00:44:00 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 04 Jul 2023 00:44:00 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Jul 2023 00:44:00 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Tue, 04 Jul 2023 00:44:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jul 2023 00:44:00 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 00:44:00 GMT
EXPOSE 5432
# Tue, 04 Jul 2023 00:44:01 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:92ad4775570054c645678402c8b75eb489b8e05313c9ccd7867bb591266db4d8`  
		Last Modified: Mon, 12 Jun 2023 23:44:45 GMT  
		Size: 30.1 MB (30062834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10301e74546286e11f33711bbcca6589f2434199679b001c7ad555b3b515ca4a`  
		Last Modified: Tue, 13 Jun 2023 10:14:59 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a71409c6a84935ad1f398b0f7f12c942e6b302b760e441f753d3d2ba8e0121a`  
		Last Modified: Tue, 13 Jun 2023 10:14:59 GMT  
		Size: 4.4 MB (4416327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5467be1f7bdf544cccf59fd32edb7f8fb6c2aff362b6977a85334a230316cfa2`  
		Last Modified: Tue, 13 Jun 2023 10:14:59 GMT  
		Size: 1.4 MB (1403371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5eedf22017d702c77c2c7011ede83e92852e9010989903f2782a978fd39325`  
		Last Modified: Tue, 13 Jun 2023 10:14:58 GMT  
		Size: 8.0 MB (8045524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57dd01eb97330ee44bdcbe6e582c1f026738f9aa744ca2e3d6cb8f8fbecdeb8`  
		Last Modified: Tue, 13 Jun 2023 10:14:57 GMT  
		Size: 1.2 MB (1249286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c917251e7429ec9bf4e7f7cc8ed7779153a02d0f9ef736af5bf523075ab9b5`  
		Last Modified: Tue, 13 Jun 2023 10:14:57 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80c5d43a2da839a26d6f745f2f0eb5950fdcfb23f4d1f47bbee6e8fe612d788`  
		Last Modified: Tue, 13 Jun 2023 10:14:57 GMT  
		Size: 3.2 KB (3194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e186c2694af6d581faf53b7d6f1a5462ebe3d0522026411ed38a5ce57c0618b`  
		Last Modified: Tue, 04 Jul 2023 00:50:45 GMT  
		Size: 90.8 MB (90772293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5265cf9b41f50fa42f8b6f0a1ce2542f7c75f9cfed089b946f3abf547fd5e8c4`  
		Last Modified: Tue, 04 Jul 2023 00:50:36 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6e0e8828167f85f200175eb6c1fd09e8a0047ab63c52712a706aa1763c9e90`  
		Last Modified: Tue, 04 Jul 2023 00:50:36 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9be9ec7dc0b9b0554e03dc9af4d0678758639eb3ffc0355f963beeda0fd5ea7`  
		Last Modified: Tue, 04 Jul 2023 00:50:35 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4880d23e501972e2358d00f3a5dd7ebd59bd453951b94c0cf843915aa09a14`  
		Last Modified: Tue, 04 Jul 2023 00:50:35 GMT  
		Size: 4.8 KB (4786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
