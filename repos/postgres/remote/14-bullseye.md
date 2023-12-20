## `postgres:14-bullseye`

```console
$ docker pull postgres@sha256:88c77856db74a5854c947a5a6e629613ef6c70ca7edf795bd5e2c9368394afb4
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

### `postgres:14-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:0e13e271d98d489e4e2664302c3962ee98399e5176d33cfc11535abb7e9ff229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137704365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ccccaaa977e85500dbc563e5cc8ef7740b9a03986988d8882507e413fee4096`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Dec 2023 18:58:54 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
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
ENV PG_VERSION=14.10-1.pgdg110+1
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfda79428ddd54935d1d2a4ee65b09c6d361d27adfa63a620b45bedce6b4fc48`  
		Last Modified: Tue, 19 Dec 2023 03:48:29 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4979af18a390bc0c38816f6458983ebd114a1f7d02ca4f00eeb5846d035fe4`  
		Last Modified: Tue, 19 Dec 2023 03:48:30 GMT  
		Size: 4.2 MB (4207492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def6df620c20542a06adc476f7c9696e3bf7ab2a1bdd24c0cdf03abceb1df841`  
		Last Modified: Tue, 19 Dec 2023 03:48:30 GMT  
		Size: 1.5 MB (1472465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82700b620cfd5b458f5edb7d0670f72b3d6528ce348a0a5f7796b34e9536802b`  
		Last Modified: Tue, 19 Dec 2023 03:48:30 GMT  
		Size: 8.0 MB (8045275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1101f5ab8ed217eb7c8d602ef40692b1ad23b666692530817057d6140bca2710`  
		Last Modified: Tue, 19 Dec 2023 03:48:31 GMT  
		Size: 1.0 MB (1037446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443cdb0b30fa4cb4dac1cbff69fc86cefcc5e2b8d34d066fca0ed1583d23a0fa`  
		Last Modified: Tue, 19 Dec 2023 03:48:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9219d8c93830f3e8ae98b22da4ea23d7c4d9ce51349495ef17bf5852664e9ba`  
		Last Modified: Tue, 19 Dec 2023 03:48:31 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34064d088ec3323f285a96f171c126d10d903337287d99b0ffc1cd0850d2079e`  
		Last Modified: Tue, 19 Dec 2023 03:48:34 GMT  
		Size: 91.5 MB (91503518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d114f4f65ea85f660ef892c0b529fd8ecf8156635c0e5bf6ccab675918e5d3e2`  
		Last Modified: Tue, 19 Dec 2023 03:48:32 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca45e28205d3a1085e9605b7bd89f46cb56235d77a11c13aadfbd39a86688e89`  
		Last Modified: Tue, 19 Dec 2023 03:48:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13df1989f70a4e3e3ab0843aac7c1126cdf87650d7111285e31fd1099b016a29`  
		Last Modified: Tue, 19 Dec 2023 03:48:32 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f4b909eda5b8def94af101bbaf3b92931b47743b4d271c58b50bfd54b2ce1a`  
		Last Modified: Tue, 19 Dec 2023 03:48:33 GMT  
		Size: 5.3 KB (5340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4805fde52a8b62a5a75519635b567b59adc32502cb63e89c8fa3bcb8297d2b`  
		Last Modified: Tue, 19 Dec 2023 03:48:33 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:a575faf3691d4e78a85120b0f95584c718879f70dd61aec0c47ddb82ff170bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5013089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4476cdfc46df712f6ad2fa1707d4ca433cdeaf6dbc15eb3a18b0ba89d66d9a0`

```dockerfile
```

-	Layers:
	-	`sha256:6434275cf94e7583bde72f19e95e641df6ca35768a32510dd9f66453a5bfa8da`  
		Last Modified: Tue, 19 Dec 2023 03:48:30 GMT  
		Size: 5.0 MB (4959620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67191c14366f512e4246caeea5e80552468feb4e82184b1e7aed0e346979790a`  
		Last Modified: Tue, 19 Dec 2023 03:48:30 GMT  
		Size: 53.5 KB (53469 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; arm variant v5

```console
$ docker pull postgres@sha256:59fdd16a0f7b923d23c765b2d01fc3a9f564d24643f085430edfdd6b86f71be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130905493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ba85ae4024f23c4d757dbf6e20722b947b9e84d95f083e0530074e379cd6b13`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Dec 2023 18:58:54 GMT
ADD file:831966ecbc1ad85566dda1f3580cd9306cc099069cd418506e8befd03c296d1c in / 
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
ENV PG_VERSION=14.10-1.pgdg110+1
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:fdebea600ba5b47ddd94c41d9d687679a030fdad563a3490945a5433dae01d54`  
		Last Modified: Tue, 19 Dec 2023 01:59:22 GMT  
		Size: 28.9 MB (28921283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b17a06ffa3320ccfe76e7d2b9f21b851cfc9dcccfd09f4cfc8096e66f5bd4f`  
		Last Modified: Tue, 19 Dec 2023 16:42:05 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64af0b841280455247d46812890d54321f384070b68408a18d4d02da7e6bb5d3`  
		Last Modified: Tue, 19 Dec 2023 16:42:06 GMT  
		Size: 3.9 MB (3889288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9602b7a047953422b7834698dc7d5b4452af629e6e1b92b8bbb01c6e6f7190a`  
		Last Modified: Tue, 19 Dec 2023 16:42:06 GMT  
		Size: 1.4 MB (1449972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54be4f2ae1ebdf3ddb038261842efa004884d3e4e9b77d26369bd500cda63f41`  
		Last Modified: Tue, 19 Dec 2023 16:42:06 GMT  
		Size: 8.0 MB (8045165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50185ddccbcfb827a990b0eeed0c750ac97f28036caaabb8a704b4d67b877807`  
		Last Modified: Tue, 19 Dec 2023 16:42:07 GMT  
		Size: 1.0 MB (1033916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca75026c18e4b6ac67ce24fb9e13a24d957d8f63bda67ae7df31c9ac2652638`  
		Last Modified: Tue, 19 Dec 2023 16:42:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2b3931718a446aa856ab8719ed141597d7c66baebe8e141de92192607131ff`  
		Last Modified: Tue, 19 Dec 2023 16:42:07 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d7cfaef318f52c4db48e92344da25e52c349b706841ce754377dbaf8d0633b`  
		Last Modified: Tue, 19 Dec 2023 17:40:54 GMT  
		Size: 87.5 MB (87545572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7092f536407cb2212c66dd1f5f2af0b12dd2fc86b6f1e99347bfaeb30c7f5c`  
		Last Modified: Tue, 19 Dec 2023 17:40:47 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3000f7b161c4f1c604d02c23f7d59ab1131f9b6f1824b03f9150d084314c2568`  
		Last Modified: Tue, 19 Dec 2023 17:40:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8b60fb30cec611bb2f7b0f8042171670038936d4b5017a8e6bb0e1715c3da3`  
		Last Modified: Tue, 19 Dec 2023 17:40:46 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f1cd1b4edeb6918de31c1680101d66712c35099b5e9aec7d6929ba15136253`  
		Last Modified: Tue, 19 Dec 2023 17:40:48 GMT  
		Size: 5.3 KB (5343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57ff3564efaf50be4272565c98f443e2245038844e262c4a2de378509ed14cf`  
		Last Modified: Tue, 19 Dec 2023 17:40:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:7f237e3423c410e4ff489e684cef9c8e7b67c3681fc8510b160fac1f3df6f1f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 KB (53283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60912af1bf418edb3c3fe63be27eff82676455142747add21a7e91b8e09142c`

```dockerfile
```

-	Layers:
	-	`sha256:e93409506ecf10160734378bf49f868d763e162ac7cc833859a26bdd12f14703`  
		Last Modified: Tue, 19 Dec 2023 17:40:46 GMT  
		Size: 53.3 KB (53283 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:f9d727c1aeb3744afb8dab666a6a31f6edfbd25a4d626e672d7a8c17f4a84823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125549140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98018dcc6e86a1e467be05ff948a554eba93194dbba8b426c283e3f8f5202414`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Dec 2023 18:58:54 GMT
ADD file:496e70a34ff4dabb4eefdf40e4e2f0563bea0c120bb43206f8f52ab5a887b637 in / 
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
ENV PG_VERSION=14.10-1.pgdg110+1
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:19ccf4d6cc6956e4a5522352be94632923aa376a9939a4f45428a4f304c73bc8`  
		Last Modified: Tue, 19 Dec 2023 02:12:33 GMT  
		Size: 26.6 MB (26578972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d975cd1debbe8fce1375d195625188b9f85a471a910b6d8c377217e4f54240bc`  
		Last Modified: Wed, 20 Dec 2023 01:28:19 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d86d96042f9213936e10d11d3f3a5b77b7ed8bb79715d799246e22139ccc38`  
		Last Modified: Wed, 20 Dec 2023 01:28:20 GMT  
		Size: 3.5 MB (3509910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820362ca25b3fd548452179375f25141a0965ea348b5e5f62f0ff0ba701d19d6`  
		Last Modified: Wed, 20 Dec 2023 01:28:20 GMT  
		Size: 1.4 MB (1440039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f23acb7074c5a64b8c10374b51d158827d6fa2fd9bbd21c1cae139fdb7ed5b8`  
		Last Modified: Wed, 20 Dec 2023 01:28:20 GMT  
		Size: 8.0 MB (8045146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c4e8793a5636be6a84ad0e94cb4e0980394acd98b36e638f80efba48fbee2be`  
		Last Modified: Wed, 20 Dec 2023 01:28:21 GMT  
		Size: 907.8 KB (907762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747e5d151622f4cb39e0c5770448a33fac2b7e62d0a96e5fe9e74996fc3e0bbf`  
		Last Modified: Wed, 20 Dec 2023 01:28:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbef2e766eebb5bf2e7f06eafb08328fa8fa1f23fa48890f6fb0d983a47977fd`  
		Last Modified: Wed, 20 Dec 2023 01:28:21 GMT  
		Size: 3.1 KB (3146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658a8dddb1ca0f878a7f3c4a4efe8daecea0d95b7dd83cb92b712d7cd1f91534`  
		Last Modified: Wed, 20 Dec 2023 02:45:50 GMT  
		Size: 85.0 MB (85047003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28656cb616c498d70554c865f15d5ea0265edf917fa38f27be7d496e6abe8870`  
		Last Modified: Wed, 20 Dec 2023 02:45:47 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d910e376593a7914962891b3dbe17bcd91201ff4d17167e5641e82c18c80d109`  
		Last Modified: Wed, 20 Dec 2023 02:45:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c9ae47ecf7618a4ec88abedc3c51711341ac978282322366d46fed26b8341e`  
		Last Modified: Wed, 20 Dec 2023 02:45:47 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef424f303f118e2f96e79070336f891d5297b3ade9f5f8467bcf709de9baed4e`  
		Last Modified: Wed, 20 Dec 2023 02:45:48 GMT  
		Size: 5.3 KB (5343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fccdb0c99dc65e427308789dcdf80493b54ecb40f1ac4f34ed85f346c21f69`  
		Last Modified: Wed, 20 Dec 2023 02:45:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:c6469ccad1870e6d9f981a9860c32980ee5173bd8145556326e301b19f5acc56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5022093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1573838fd6945dd25de908b2318b4da8efe466c5ea7a68eb2f1d00932fb28e1d`

```dockerfile
```

-	Layers:
	-	`sha256:9165183c9781c0f08bf744f4f2a6299a78b7d8c4bff659ff55caa5de2cc79f15`  
		Last Modified: Wed, 20 Dec 2023 02:45:47 GMT  
		Size: 5.0 MB (4968603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1cb6974639922e0ea68623bb09095082d444cdda0aed2b67cdb2ca24d8a952a`  
		Last Modified: Wed, 20 Dec 2023 02:45:46 GMT  
		Size: 53.5 KB (53490 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:0a02163dd35f2e9ea1f90a899b38c1443b736bbe13265d0d9a242ac12910de1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132800384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d22ae02aeed28e56995ac810a68ebe2fa5cf65809a8cfba5855ece1563baf53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Dec 2023 18:58:54 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
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
ENV PG_VERSION=14.10-1.pgdg110+1
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9b3e0ef155ee9ac6cff3ab81490094ba2c0322bf56e42b285e96cdf9d6d5c8`  
		Last Modified: Wed, 20 Dec 2023 10:30:43 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7849d9f81828e73b2f2212806c12be7be87163fbe5caf5609da0e638a82e8876`  
		Last Modified: Wed, 20 Dec 2023 10:30:44 GMT  
		Size: 4.2 MB (4209437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d705468de86fde4f65fc552c39ad3bc74be6dce2396d9fdde6253ddc67c9e4b`  
		Last Modified: Wed, 20 Dec 2023 10:30:44 GMT  
		Size: 1.4 MB (1404417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2cfd5daf8d97ed2e60b3c100a683e3112b79c452246861053c179d0c086f915`  
		Last Modified: Wed, 20 Dec 2023 10:30:44 GMT  
		Size: 8.0 MB (8045185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a393a1ba0a4678c9533a6eaa2114c5c8913b5d0c4986ce122113e692a7c0770a`  
		Last Modified: Wed, 20 Dec 2023 10:30:45 GMT  
		Size: 1.0 MB (1025890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b0d4fea4115759a23af99ba309cd279d1bce3eacb9896c06895478e6a305e0`  
		Last Modified: Wed, 20 Dec 2023 10:30:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ceb9a3e309ce7fd2ac6f01ff37fe5f45f85d768ecd3ee0fc7641ae044ed7abf`  
		Last Modified: Wed, 20 Dec 2023 10:30:45 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d027bb68ed30660b5599098e7b93f84cf096d7284a1ea7806d8ac75c86b898`  
		Last Modified: Wed, 20 Dec 2023 10:34:14 GMT  
		Size: 88.0 MB (88031102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd937e358016d531ed18f947dce827e3bcef44ae8771db764aaef4ded6bb9c2`  
		Last Modified: Wed, 20 Dec 2023 10:34:11 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61ae1fc902e45fa986f2e4df37a881a027b726ca0a1a3756383c5e7000cb243`  
		Last Modified: Wed, 20 Dec 2023 10:34:11 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5a07a400ad0fb5eb9970f8a889df72d1c7b48dfcfb9452caf514b86037f15b`  
		Last Modified: Wed, 20 Dec 2023 10:34:12 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50113885f811ee6965ba153c98c604830284ddd1b2b4659b84593f64a3880e24`  
		Last Modified: Wed, 20 Dec 2023 10:34:12 GMT  
		Size: 5.3 KB (5341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5b4404df52b5f570d836f54dc646e9b1e0fea113c76c7d190530f716973f57`  
		Last Modified: Wed, 20 Dec 2023 10:34:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:31f9c4e3733f3a6b72e2c6cadf8842e42fa381395fb2ac3f5aff7c323d9b97d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5018558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bae1c86b09f41d39a14dc7256ac64b58e0a8affd8ca15594b0dd52f154fc818`

```dockerfile
```

-	Layers:
	-	`sha256:81d097e5e6594f1c574ba4c138610db9cdca7f594c0d1f1cd13985502d9ac215`  
		Last Modified: Wed, 20 Dec 2023 10:34:11 GMT  
		Size: 5.0 MB (4965251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d4a7c63c53953ec46c8594a7719e0c6039e9a293efd51a05418bed1effdb60d`  
		Last Modified: Wed, 20 Dec 2023 10:34:11 GMT  
		Size: 53.3 KB (53307 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:f31741b24028acf7d9c83ff682ae4b166fa08d758ad070c4863b0a1265c1e105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139680871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bfeb21d7b4d738a73c08279e4187f660e25990025b2c45a310f1f64f2566e7c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Dec 2023 18:58:54 GMT
ADD file:e9c344f1bffba57e46b30e3c70e4247dcf2e9d3e0484b2768f83ffd789bf3686 in / 
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
ENV PG_VERSION=14.10-1.pgdg110+1
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:e5808d881ded1b1deb8675903e6776c5a725d22c8a5c1061a96c74338f07591f`  
		Last Modified: Tue, 19 Dec 2023 01:44:31 GMT  
		Size: 32.4 MB (32402688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ac04d9679d1f312a8ecbc190881a9ef96ca376abff20f16546d500aa0bb98e`  
		Last Modified: Tue, 19 Dec 2023 03:59:38 GMT  
		Size: 1.7 KB (1679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f7d08679383a88fd8fe3a677c7f7a1e69b2a3a294fbdd60e6f0ec4bf9417e1`  
		Last Modified: Tue, 19 Dec 2023 03:59:38 GMT  
		Size: 4.6 MB (4607392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319fd3ca3ed75bb49bb2426481f91b98b0ff9fbcaf564965544d4c1370e3164d`  
		Last Modified: Tue, 19 Dec 2023 03:59:38 GMT  
		Size: 1.4 MB (1448264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9648b22e0aac6b502e6100f1c7063bb16cda866f8d9f5f62ae782fadf5975c68`  
		Last Modified: Tue, 19 Dec 2023 03:59:38 GMT  
		Size: 8.0 MB (8045097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2902baa82162c026f7099ff4f28c67bd7a659e7f0e96104e6e32fc94cd73a701`  
		Last Modified: Tue, 19 Dec 2023 03:59:39 GMT  
		Size: 1.0 MB (1027934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbaaf76c5dcd7fd06a9f0fd6bb4ff798d83050d44277440f5b9ae66d9b864f14`  
		Last Modified: Tue, 19 Dec 2023 03:48:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b392c20069b204d695e75f001aaa2069bfb82b57ed49c17d7af0e7b07175226e`  
		Last Modified: Tue, 19 Dec 2023 03:48:30 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5a856803bc0a6a6e6316871097f61845a492c3daf1e268ad10a34ccb4cc05b`  
		Last Modified: Tue, 19 Dec 2023 03:59:42 GMT  
		Size: 92.1 MB (92129197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a256ac6b6089b30d2953499e75c49269c2fe06fcc611852f457349cd6601e478`  
		Last Modified: Tue, 19 Dec 2023 03:59:39 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f1df67afa5343190639bb324c3407dad44953bba37f048a32e9b2b0c898e49`  
		Last Modified: Tue, 19 Dec 2023 03:59:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c338f612e62654463f364392c45466ad9e4a25754ee77b48c938e75db07830`  
		Last Modified: Tue, 19 Dec 2023 03:59:39 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d632b13b8a151bf1e21e1675abdfe83adead08c25f17c82f84595d8d5675055b`  
		Last Modified: Tue, 19 Dec 2023 03:59:40 GMT  
		Size: 5.3 KB (5345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c2111fefda781d4ad06bb7315447c72cfb1457ec6500b3ec12ce7b58654069`  
		Last Modified: Tue, 19 Dec 2023 03:59:40 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:f9ef1823e37429662e8fc1dd1dc504cd3adf1368987db0dc730fd204d7ee2e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 KB (53213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed561a8ba5a2ef54e35a8ecd8369efad16ce824a72d0145d7f64e26a8122854`

```dockerfile
```

-	Layers:
	-	`sha256:c62d6688d32505a6252d6095ce9428f3d8f643335eed4235b792d87ebcb7d35e`  
		Last Modified: Tue, 19 Dec 2023 03:59:38 GMT  
		Size: 53.2 KB (53213 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; mips64le

```console
$ docker pull postgres@sha256:5f39e3739341d01aa07e7c2121202decc12a8ac8dc6f0eea1c471b156f5e8b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132446949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95edc37b8bdbb19a7650062836b9e7ab4e58034b9f77bd75ec00b4489bbd7f9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Nov 2023 04:11:02 GMT
ADD file:09d1c4f0f5b78b81f635498ee58f6ab1843bca8a18549ecc39686f1c60b1951d in / 
# Tue, 21 Nov 2023 04:11:06 GMT
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
ENV PG_VERSION=14.10-1.pgdg110+1
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:a157b7f5d72df9473d33b22278cb42e4e06e22b99ac1864b7b586f36671f15bb`  
		Last Modified: Tue, 21 Nov 2023 04:22:02 GMT  
		Size: 29.6 MB (29636034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4f8a086f8ee2ae344567ef2236a8449ccd5d922d507e0b100f752d3d832ad7`  
		Last Modified: Thu, 14 Dec 2023 21:15:23 GMT  
		Size: 1.7 KB (1700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9598b461dfba72d8cea81900061cc0a770753537a3d21181d04234fe20baec7`  
		Last Modified: Thu, 14 Dec 2023 21:15:24 GMT  
		Size: 4.2 MB (4196376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8785524799966281da638a9eae6592091c22cf6809bdb30c5317f8ba4d1384`  
		Last Modified: Thu, 14 Dec 2023 21:15:24 GMT  
		Size: 1.4 MB (1359980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4c7a02d1de3ff39c2c81809ae917a73c2d379816f761509c4d26c366b6c05e`  
		Last Modified: Thu, 14 Dec 2023 21:15:24 GMT  
		Size: 8.0 MB (8045536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7a9a8c8efeb9396dd3d08f9d1597b6e64dff16cddde8a8b3af24fe3382efa3`  
		Last Modified: Thu, 14 Dec 2023 21:15:26 GMT  
		Size: 1.1 MB (1089547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a62a850af8981d83db60c8b09075c5df562171378fcb56af1094b6831b1d95d`  
		Last Modified: Thu, 14 Dec 2023 21:15:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee6ae6b998a33975bb7023e4ffe338e6c1d8419ece17204023e454e057903ec`  
		Last Modified: Thu, 14 Dec 2023 21:15:26 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af99e4f578699cb0f9b18e718bca0b1e2c559bdafff3182478ea46686eabe68`  
		Last Modified: Fri, 15 Dec 2023 03:02:05 GMT  
		Size: 88.1 MB (88099151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b43a3143017c4d9af5276e9012a7ae194db178d90226161b0670122a05d706`  
		Last Modified: Fri, 15 Dec 2023 03:01:56 GMT  
		Size: 9.5 KB (9535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e9cba12f7d9f29c717dd546e9365e3fc6f6290ef7c3ae13bfb244ffcd48ed4`  
		Last Modified: Fri, 15 Dec 2023 03:01:56 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49ead7f47e261af4a3bbb682a7fcffe2f4b26a41cab86c958b3f498e6a21fb9`  
		Last Modified: Fri, 15 Dec 2023 03:01:56 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cec1d151ea7b01eca0150171e6f0a97d80d9f7fd629caeedeb3c12706faba3`  
		Last Modified: Fri, 15 Dec 2023 03:01:58 GMT  
		Size: 5.3 KB (5344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96425fba0433fab89e8c0807a90329fbd959389aef9e9d14bd66e16eebc6a0d6`  
		Last Modified: Fri, 15 Dec 2023 03:01:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:d8cffdc68ae48731b597fa3cb2361f08ffd3e6776041f8a897060ba12b944548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 KB (53159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a1cfed9ab9a97dffebc9e18374b3e431e52fa0f032d1a3483b238e5fc47ba6`

```dockerfile
```

-	Layers:
	-	`sha256:e8e24323725e8c311e63b25b93b8b0c8a998e9720910f34f8e33ea506c0e2782`  
		Last Modified: Fri, 15 Dec 2023 03:01:56 GMT  
		Size: 53.2 KB (53159 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; ppc64le

```console
$ docker pull postgres@sha256:9e419884d44cf8bbe3f0274efda28f9764b4580d3cbffc6a34ffa0e4a6b4879a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146767812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86790e90d5f94b52516cf45b5eed7c40a849d1b3a9aacf4aff9d311b4eae544c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Dec 2023 18:58:54 GMT
ADD file:1cb772a6ad8ca6301624db3141029490564de7673bc0f2d4bedb5a1578ea85bd in / 
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
ENV PG_VERSION=14.10-1.pgdg110+1
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:c9f6fac7f65cfc65b7f8de8bc377b135ca95e45a3246cf2bd1bb90922679553e`  
		Last Modified: Tue, 19 Dec 2023 01:27:11 GMT  
		Size: 35.3 MB (35293807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7fa77be1c06eebaab6e02ca135f71c0c8c900a9bfed98cd23e39da26c26c34`  
		Last Modified: Wed, 20 Dec 2023 09:01:00 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef0e5cf4c01f1b8f34458d2012ac122c8b4cc9a5d5ea7d4137510eda62e607f`  
		Last Modified: Wed, 20 Dec 2023 09:01:01 GMT  
		Size: 5.0 MB (5016048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61bbfebffba13cdff519e4f0b9abc2102c29d2597c240e6ecb17457a29bf081`  
		Last Modified: Wed, 20 Dec 2023 09:01:01 GMT  
		Size: 1.4 MB (1394071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28350eee4b9c2b6fe04d507a3ced8c8d5cd2c1112c83bae82b3e336924b0a4ef`  
		Last Modified: Wed, 20 Dec 2023 09:01:01 GMT  
		Size: 8.0 MB (8045252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09104b53fce98bf90fc7eb20c572cdf2cd5e74c90ea71ac128ffdb5086daf6aa`  
		Last Modified: Wed, 20 Dec 2023 09:01:02 GMT  
		Size: 1.2 MB (1196989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d156ab180e54734b30092890f436441f05cddf7219f1878e3ced2cbf7b04d3`  
		Last Modified: Wed, 20 Dec 2023 09:01:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473612340ca822d62c53273e62832f0849b040d0bc0de8d0e479cf0d57d4baa1`  
		Last Modified: Wed, 20 Dec 2023 09:01:02 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e047ffc5431e2c055239303f7b36088ead7538add1fddf20456d203c82659c`  
		Last Modified: Wed, 20 Dec 2023 09:09:07 GMT  
		Size: 95.8 MB (95801335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0c1b07e0febea67691bc8dfe1af8bcf4321b37c3f861b5548fea2c6d8496ae`  
		Last Modified: Wed, 20 Dec 2023 09:09:04 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca5a723ad2b9064ed1f1e754b5009bb265c4f15c191cd5d58c1c96249017882`  
		Last Modified: Wed, 20 Dec 2023 09:09:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9787a315286a6ede6c6ccc6e131accc1340f355f0fc75eeda8d464796c46afa6`  
		Last Modified: Wed, 20 Dec 2023 09:09:05 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f3aa3185031091ceb303a043ba25c9dc7c75f6f2a72fa2eecf8f6b804ec10a`  
		Last Modified: Wed, 20 Dec 2023 09:09:05 GMT  
		Size: 5.3 KB (5340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a5c097e0a52f5e6bb39ccd27fec6e9eda97d61109085ba5649e140fe1b2da4`  
		Last Modified: Wed, 20 Dec 2023 09:09:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:53f6bb1635d887680a49ad14d330cf83967c4f129360c34266ccdd75b67e0d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5020103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8d165a821240b3e6747b3e6efe4bdd9860dcea57b4ca6b13adf89f478331145`

```dockerfile
```

-	Layers:
	-	`sha256:1b2776027ea62d5331e3bfe2379088643084065d3af5c1596d6c2ebdbd657a05`  
		Last Modified: Wed, 20 Dec 2023 09:09:04 GMT  
		Size: 5.0 MB (4966754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fc051faec7877f36a908fcc3a873a2f1ab0a9d786db17ec865ce706716f36b4`  
		Last Modified: Wed, 20 Dec 2023 09:09:03 GMT  
		Size: 53.3 KB (53349 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; s390x

```console
$ docker pull postgres@sha256:adecb9c7e72dc562b2f7ac56bab0551c1004e9b7502abf03090300c93063c61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141344252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e02d4a5827746fee3d8759440e443078c61399651e92baaf8e4186e2a489aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Dec 2023 18:58:54 GMT
ADD file:36a070457acddafcd6cdda22a3c41efcbd4e2b1694831eb74c8143520ebf1cf2 in / 
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
ENV PG_VERSION=14.10-1.pgdg110+1
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:eff2a4367cf88d5103011eba9299da2b4d173b0bde5dc0455020febf72b9b1c4`  
		Last Modified: Tue, 19 Dec 2023 01:48:08 GMT  
		Size: 29.7 MB (29657006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369b891674da655514f0ac3404da121a3bec6700dd18315ffb5d91ed3da8be9a`  
		Last Modified: Tue, 19 Dec 2023 15:41:43 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064d665dd7d5609c5bf35ea85d4109596b6642b979180ff8c81bc53c3af9ae12`  
		Last Modified: Tue, 19 Dec 2023 15:41:44 GMT  
		Size: 4.1 MB (4096145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e215fdd056d05b8a8144d5a854967c5f8580132804acb57abf6ddac7c22b635`  
		Last Modified: Tue, 19 Dec 2023 15:41:44 GMT  
		Size: 1.4 MB (1438319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9abe21501bcb9dbf5ee5b994d9a12fcf5c3460a2c01f3df43da24861e7c70dd`  
		Last Modified: Tue, 19 Dec 2023 15:41:44 GMT  
		Size: 8.1 MB (8099036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ba4a580fa6aa550dde22a6c2076af1f668a977d7be7d6053854f434207f058`  
		Last Modified: Tue, 19 Dec 2023 15:41:44 GMT  
		Size: 1.0 MB (1014312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f365b225a06eaf8e3d4fc6ea1cc6a0c176cd7e7264a8e8f00df8416989c89823`  
		Last Modified: Tue, 19 Dec 2023 15:41:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df5d1b90ef8f9b0489460d1e48b13f72bfee611d29c5cb9d9da167cace54921`  
		Last Modified: Tue, 19 Dec 2023 15:41:45 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad07ac2457bf897db8bf2f5776a415dfa5b81af6670900e371a9dbc7c1595571`  
		Last Modified: Tue, 19 Dec 2023 15:46:41 GMT  
		Size: 97.0 MB (97019132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee5fc1b2eee43ddc72156066f254f5c96fa6d10267f835db006fc4170fd72f5`  
		Last Modified: Tue, 19 Dec 2023 15:46:39 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33c4562d88fe2403bb6d5f5f75f08e5e3eac34e716ebcdc5fdcb10391b2e973`  
		Last Modified: Tue, 19 Dec 2023 15:46:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62862b0484cf83d0712bd86fac97a1dd32aa2ef17b2232edb8d92e5ab89bbe8e`  
		Last Modified: Tue, 19 Dec 2023 15:46:39 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d0b1741651a356f175b462d10b632e1f1db2e243d6c7995e2289af40da3e4e`  
		Last Modified: Tue, 19 Dec 2023 15:46:40 GMT  
		Size: 5.3 KB (5342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60545d3140a8b2e1b4514573ca4b544ac6dfc4dedd622e1f2d8c869b5ab69a3`  
		Last Modified: Tue, 19 Dec 2023 15:46:40 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:5bdd8b5cd5335f4e803c93ab812b970733e85506e22df1113a37c1fa7296d244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5011901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5797902c61c6b26ed557a27c19d7cf24206ec069ebe5fd423f725564f6140e4b`

```dockerfile
```

-	Layers:
	-	`sha256:687725ef0f9071e958e6f3a295140c1d83b800cde5eebf9b3a8a82a7facd776e`  
		Last Modified: Tue, 19 Dec 2023 15:46:38 GMT  
		Size: 5.0 MB (4958599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6818f91519f8e4667fd561d48778da2086070e9bf2ffbd631451f961b96c3d4c`  
		Last Modified: Tue, 19 Dec 2023 15:46:38 GMT  
		Size: 53.3 KB (53302 bytes)  
		MIME: application/vnd.in-toto+json
