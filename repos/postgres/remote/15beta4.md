## `postgres:15beta4`

```console
$ docker pull postgres@sha256:ba1b95cb605bc1dee049f44d78a84544b9e4cb39d82a9d5977501df9f072b949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `postgres:15beta4` - linux; amd64

```console
$ docker pull postgres@sha256:f2b4d06ac06f0f50236c39289edfd6701eb1313d2d17f3028c8df0c00f2b21db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139847500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af25b1739dd54ce94a080f618cff82c62bd41368315be13fa88dcea0e71881f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 11:43:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Sep 2022 11:43:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 13 Sep 2022 11:43:28 GMT
ENV GOSU_VERSION=1.14
# Tue, 13 Sep 2022 11:43:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Sep 2022 11:43:44 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 13 Sep 2022 11:43:44 GMT
ENV LANG=en_US.utf8
# Tue, 13 Sep 2022 11:43:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 11:43:48 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Sep 2022 11:43:50 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 13 Sep 2022 11:43:50 GMT
ENV PG_MAJOR=15
# Tue, 13 Sep 2022 11:43:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 13 Sep 2022 11:43:50 GMT
ENV PG_VERSION=15~beta4-1.pgdg110+1
# Tue, 13 Sep 2022 11:44:10 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 13 Sep 2022 11:44:11 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 13 Sep 2022 11:44:12 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 13 Sep 2022 11:44:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Sep 2022 11:44:13 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 13 Sep 2022 11:44:13 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Sep 2022 11:44:13 GMT
COPY file:925d466681c8349f58385c00a8caa567c76b695158aa04bf4ad2ac92604e11c7 in /usr/local/bin/ 
# Tue, 13 Sep 2022 11:44:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Sep 2022 11:44:13 GMT
STOPSIGNAL SIGINT
# Tue, 13 Sep 2022 11:44:13 GMT
EXPOSE 5432
# Tue, 13 Sep 2022 11:44:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc97844d0cd5332f8a27d4e812cb78fe28eb3a24d6447b298e11f4c1381ee04b`  
		Last Modified: Tue, 13 Sep 2022 11:47:19 GMT  
		Size: 4.4 MB (4414809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad9b1166fde5ac579a870942e64b1252b809a74ce2716537b2ec7d29211aa0e`  
		Last Modified: Tue, 13 Sep 2022 11:47:18 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286c4682b24df07908e721b97e0e931e7094b0822d4dd0623c48684960c892c0`  
		Last Modified: Tue, 13 Sep 2022 11:47:18 GMT  
		Size: 1.4 MB (1418427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3679a4a1a1adeb649c1019cdb9ba6be5f79b5035e1ec221fcf583033a34926`  
		Last Modified: Tue, 13 Sep 2022 11:47:17 GMT  
		Size: 8.0 MB (8045146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2e6cdc8503192834c8294003826329e7af061a1f47f07993501623d7ccedea`  
		Last Modified: Tue, 13 Sep 2022 11:47:16 GMT  
		Size: 1.3 MB (1261090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7dc70f54e874e4d3bfa632e989030d30740819b8c4612427817302aa8add51`  
		Last Modified: Tue, 13 Sep 2022 11:47:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a090c7442692840048d70c9acd1c55039a7f996487443a737aaa51ce10fea1d0`  
		Last Modified: Tue, 13 Sep 2022 11:47:15 GMT  
		Size: 3.2 KB (3190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7ec665aa98ab1db4d94e40d452a85ee6bd3da9a463a5d40afa1789fcfcd526`  
		Last Modified: Tue, 13 Sep 2022 11:47:27 GMT  
		Size: 93.3 MB (93283953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414b489f73a2d554a24f7d668809676cee043cccfd5860808522e955acb7330e`  
		Last Modified: Tue, 13 Sep 2022 11:47:13 GMT  
		Size: 9.8 KB (9793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced7c9a7b5e4ed1f7d3dc772c1253178bff7d00f9399059e925df9d1f4dc9dcf`  
		Last Modified: Tue, 13 Sep 2022 11:47:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15aa4c901bb2979fbd5881784fff246a21b65a3ca2f4ea96f17dafa6fdb697cf`  
		Last Modified: Tue, 13 Sep 2022 11:47:13 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30db2c620d2aaa1092c37a5cde8a761f395a444d79979baee14ea22a673c6e81`  
		Last Modified: Tue, 13 Sep 2022 11:47:13 GMT  
		Size: 4.7 KB (4696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15beta4` - linux; arm variant v5

```console
$ docker pull postgres@sha256:8f7c4c768f5834b9dcbf261cf3f641ddb17fea13e5728db3579ccb5129842bf8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133107798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66998d80e418b8b2bf63bdac77d01623f70536ee8277f29e2a15365754a9c38c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 13 Sep 2022 00:53:30 GMT
ADD file:539e23f1c3a625a612a5a59b3939e9692c86c3cfa4956d30f4802c9f34ffa29c in / 
# Tue, 13 Sep 2022 00:53:31 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 10:06:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Sep 2022 10:06:40 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 13 Sep 2022 10:06:41 GMT
ENV GOSU_VERSION=1.14
# Tue, 13 Sep 2022 10:06:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Sep 2022 10:07:03 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 13 Sep 2022 10:07:03 GMT
ENV LANG=en_US.utf8
# Tue, 13 Sep 2022 10:07:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 10:07:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Sep 2022 10:07:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 13 Sep 2022 10:07:12 GMT
ENV PG_MAJOR=15
# Tue, 13 Sep 2022 10:07:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 13 Sep 2022 10:07:12 GMT
ENV PG_VERSION=15~beta4-1.pgdg110+1
# Tue, 13 Sep 2022 10:23:31 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 13 Sep 2022 10:23:32 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 13 Sep 2022 10:23:33 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 13 Sep 2022 10:23:33 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Sep 2022 10:23:33 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 13 Sep 2022 10:23:34 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Sep 2022 10:23:34 GMT
COPY file:925d466681c8349f58385c00a8caa567c76b695158aa04bf4ad2ac92604e11c7 in /usr/local/bin/ 
# Tue, 13 Sep 2022 10:23:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Sep 2022 10:23:34 GMT
STOPSIGNAL SIGINT
# Tue, 13 Sep 2022 10:23:34 GMT
EXPOSE 5432
# Tue, 13 Sep 2022 10:23:34 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:705abbab4fcb3a8dfe046a2ae6c450328aa11d93911abce66d3bba8bc693cbd4`  
		Last Modified: Tue, 13 Sep 2022 01:01:07 GMT  
		Size: 28.9 MB (28905288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1473ec2d2fae6ea58e06f47026bc84a4c52d8be998f06a55f36c3b8fc5bc3630`  
		Last Modified: Tue, 13 Sep 2022 11:33:36 GMT  
		Size: 4.1 MB (4096406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:115d2357e6f4c9f60a0a412e2cb045e70d84aedfd3ec051dfd93b136694ae1ce`  
		Last Modified: Tue, 13 Sep 2022 11:33:35 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048179ecc8b14dbeb7717ba5299b577da5c0bf1938227556e2737c66f5947080`  
		Last Modified: Tue, 13 Sep 2022 11:33:31 GMT  
		Size: 1.4 MB (1382597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676d87db682267db7591e1b3a1823e0b135d80fff11c1aa7469b63b804913156`  
		Last Modified: Tue, 13 Sep 2022 11:33:32 GMT  
		Size: 8.0 MB (8045311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31972b2b9ab424ea306e63e00831f41bb2e97f0e2deab7310759b6cb7ad9f846`  
		Last Modified: Tue, 13 Sep 2022 11:33:28 GMT  
		Size: 1.3 MB (1257238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdbaccdb86dbf46a1e76d55b63099212255013aaea653036b606531113158da`  
		Last Modified: Tue, 13 Sep 2022 11:33:28 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf6954a7133b6508ce10bc39bced79981b9bf10785a032f4e2498dfe68d439f`  
		Last Modified: Tue, 13 Sep 2022 11:33:27 GMT  
		Size: 3.2 KB (3201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d5c716e36bed87a3ea8ee80456861e13e4cd34f8d781d042f75d95693e479c4`  
		Last Modified: Tue, 13 Sep 2022 11:33:46 GMT  
		Size: 89.4 MB (89400983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:182991d3597eb2fbffbdb38717b868da331b50928329f4e7e702de93145f7404`  
		Last Modified: Tue, 13 Sep 2022 11:33:25 GMT  
		Size: 9.8 KB (9801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d8c83c7cdfd770e6d3ed94369e0d68d157ae118e91c736ad52eb9287462738`  
		Last Modified: Tue, 13 Sep 2022 11:33:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddd9e7f06615ce3a8f6e9d5f0ea0009dca79d0abbd58fc89d895dbaf43647c7`  
		Last Modified: Tue, 13 Sep 2022 11:33:25 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7f48126aafaa839cf7de00a5e618e92d87736fa85193bf57281ab9d64ea42f`  
		Last Modified: Tue, 13 Sep 2022 11:33:25 GMT  
		Size: 4.7 KB (4703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15beta4` - linux; arm variant v7

```console
$ docker pull postgres@sha256:630fe562445384c95b929ab7177f459bf1f999e93df0064e8ecc2d22e2cf772c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127746870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c784089c8b1c8f7e5e314f4a9a16dbafa593dc545f14d179d604531e306262`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 13 Sep 2022 03:42:37 GMT
ADD file:04b0c48a2d326e2ac4255df4a6165508f0d29d8a32147fb8df6bf9504b8f6b09 in / 
# Tue, 13 Sep 2022 03:42:37 GMT
CMD ["bash"]
# Wed, 14 Sep 2022 00:24:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 14 Sep 2022 00:24:40 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 14 Sep 2022 00:24:40 GMT
ENV GOSU_VERSION=1.14
# Wed, 14 Sep 2022 00:24:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Sep 2022 00:25:00 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 14 Sep 2022 00:25:00 GMT
ENV LANG=en_US.utf8
# Wed, 14 Sep 2022 00:25:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Sep 2022 00:25:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Sep 2022 00:25:07 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 14 Sep 2022 00:25:08 GMT
ENV PG_MAJOR=15
# Wed, 14 Sep 2022 00:25:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 14 Sep 2022 00:25:08 GMT
ENV PG_VERSION=15~beta4-1.pgdg110+1
# Wed, 14 Sep 2022 00:40:44 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 14 Sep 2022 00:40:45 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 14 Sep 2022 00:40:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 14 Sep 2022 00:40:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 14 Sep 2022 00:40:47 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 14 Sep 2022 00:40:47 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 14 Sep 2022 00:40:47 GMT
COPY file:925d466681c8349f58385c00a8caa567c76b695158aa04bf4ad2ac92604e11c7 in /usr/local/bin/ 
# Wed, 14 Sep 2022 00:40:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Sep 2022 00:40:47 GMT
STOPSIGNAL SIGINT
# Wed, 14 Sep 2022 00:40:47 GMT
EXPOSE 5432
# Wed, 14 Sep 2022 00:40:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:43caeee1782255456dd3403ae8e6ba191802c3deb004ca68ce0420b30368995d`  
		Last Modified: Tue, 13 Sep 2022 03:49:46 GMT  
		Size: 26.6 MB (26567059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28c5f1f4a7f264140d6897290e775d2f0d10bc5cb5c70f525cad0e2c36461bf`  
		Last Modified: Wed, 14 Sep 2022 01:37:07 GMT  
		Size: 3.7 MB (3717189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403ab4abb4d86edeeada89bd507fe4be6de859914075df2091312af085cea350`  
		Last Modified: Wed, 14 Sep 2022 01:37:04 GMT  
		Size: 1.8 KB (1790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a610053bccfcb9fe766dc57ea9e8c36836ec0461b638b94e4cb95c15195e7611`  
		Last Modified: Wed, 14 Sep 2022 01:37:06 GMT  
		Size: 1.4 MB (1375368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b669083afc43e84aab8a6a6801022394cc720937bec0b5e893fae554e8ac58e`  
		Last Modified: Wed, 14 Sep 2022 01:37:06 GMT  
		Size: 8.0 MB (8045383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bdea36e070bd82675ac82c77aa141f22b52129d0b3278ac0dcc39f4f329a5ea`  
		Last Modified: Wed, 14 Sep 2022 01:37:02 GMT  
		Size: 1.1 MB (1131143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60663da00f89850635680936c774e5aebee8f30767469e05867e8d541d5e36d4`  
		Last Modified: Wed, 14 Sep 2022 01:37:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f486cc4a264b50bb8cf9b22c10481461a3fff73c218ce1373f5248618b805975`  
		Last Modified: Wed, 14 Sep 2022 01:37:01 GMT  
		Size: 3.2 KB (3196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd788c52a22b109e2840e1b3dd27838b8461d9f35560e1a6832df1a93b82587e`  
		Last Modified: Wed, 14 Sep 2022 01:37:21 GMT  
		Size: 86.9 MB (86890752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86821c9ffeff2cc348376e6f4a9a4c978dc12f30034a859c24bf83305a9a4ca`  
		Last Modified: Wed, 14 Sep 2022 01:36:58 GMT  
		Size: 9.8 KB (9806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e016711e1f1ae4930368e362720a3e8477ec0c10f8ee061019306a2a97eba194`  
		Last Modified: Wed, 14 Sep 2022 01:36:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adafaaa3ee00098553402b09223d20b64607b80832064a0a3e84fb013bbcac8e`  
		Last Modified: Wed, 14 Sep 2022 01:36:58 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02760b6d13856c3e92b5bda34c9edba988cff9f3beb3d30c31a3a7d8b56dd786`  
		Last Modified: Wed, 14 Sep 2022 01:36:58 GMT  
		Size: 4.7 KB (4705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15beta4` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:fd4e2115a282b1dd67ed1e18d2dab9b2de6e529f5500d4913945d5ecc46b495f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134478505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7708e84563f6362b649ce07588e2748f07860a492aa550f27db09bb8920f6a04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 12:09:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Sep 2022 12:09:33 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 13 Sep 2022 12:09:34 GMT
ENV GOSU_VERSION=1.14
# Tue, 13 Sep 2022 12:09:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Sep 2022 12:09:48 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 13 Sep 2022 12:09:49 GMT
ENV LANG=en_US.utf8
# Tue, 13 Sep 2022 12:09:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:09:54 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Sep 2022 12:09:56 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 13 Sep 2022 12:09:56 GMT
ENV PG_MAJOR=15
# Tue, 13 Sep 2022 12:09:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 13 Sep 2022 12:09:58 GMT
ENV PG_VERSION=15~beta4-1.pgdg110+1
# Tue, 13 Sep 2022 12:10:20 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 13 Sep 2022 12:10:21 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 13 Sep 2022 12:10:22 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 13 Sep 2022 12:10:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Sep 2022 12:10:24 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 13 Sep 2022 12:10:25 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Sep 2022 12:10:27 GMT
COPY file:925d466681c8349f58385c00a8caa567c76b695158aa04bf4ad2ac92604e11c7 in /usr/local/bin/ 
# Tue, 13 Sep 2022 12:10:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Sep 2022 12:10:28 GMT
STOPSIGNAL SIGINT
# Tue, 13 Sep 2022 12:10:29 GMT
EXPOSE 5432
# Tue, 13 Sep 2022 12:10:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab9a79a977206c3cbf88422f52bca0c52d8054d3b5129afb5048208169b6021`  
		Last Modified: Tue, 13 Sep 2022 12:15:54 GMT  
		Size: 4.2 MB (4209303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8116dc73cb3e7af97264617035a3061f7baeff0ab8d9757e37962be25f75d5be`  
		Last Modified: Tue, 13 Sep 2022 12:15:52 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ceb4515aa79b3b5efd648379c2189297a8674bd836b68512c0346882f5db6b`  
		Last Modified: Tue, 13 Sep 2022 12:15:52 GMT  
		Size: 1.3 MB (1346151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d6f7eceb1d7a0a11340e731336fad1666cac5d24546c9a32fa56ecbbd725de2`  
		Last Modified: Tue, 13 Sep 2022 12:15:51 GMT  
		Size: 8.0 MB (8043613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a94e4c3770522b5f3440cf4b0da47dd56c8f316f8451d6a0167f237592b998`  
		Last Modified: Tue, 13 Sep 2022 12:15:50 GMT  
		Size: 1.0 MB (1025889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5172abe7cf72ddd6e2807de44a843a6a096d9f0260586b2826b02b0b4a4c27a5`  
		Last Modified: Tue, 13 Sep 2022 12:15:50 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9577c9870fc566992ba5f9adb1b9d13e4a10731e5bd29d5eb0dc2624c0e89632`  
		Last Modified: Tue, 13 Sep 2022 12:15:50 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4492af986a4bf41556b86f1313134148939f6b119923f115a37748c6d66c8d`  
		Last Modified: Tue, 13 Sep 2022 12:16:00 GMT  
		Size: 89.8 MB (89779614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa8a7e8cba825e844cb6a97cf247e19997c9e24c93332dbcb027ae2893a0c99`  
		Last Modified: Tue, 13 Sep 2022 12:15:48 GMT  
		Size: 9.8 KB (9793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbf585f77da41e53cf4e43d187d0994884858f6f2a27f6f0e3a85264baab03b`  
		Last Modified: Tue, 13 Sep 2022 12:15:48 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2448aadac04b96dafd3f1c9896a734dc8d4750ecd493b01e2ad493ccdfc8e3`  
		Last Modified: Tue, 13 Sep 2022 12:15:48 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e14bff72566cb5ff96a38dbfa2ed10a0f84b9b1cf94f4c3d578eaa069e6c23b`  
		Last Modified: Tue, 13 Sep 2022 12:15:48 GMT  
		Size: 4.7 KB (4699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15beta4` - linux; 386

```console
$ docker pull postgres@sha256:d0eb81253bb5d3f549940fd76550df4d91d91d2e8a9d5bdfc843e36b89440fff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141482029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e4ca0a36a5096107e15826dad2920ee9049fd9afc1026a937f44d3c67a0bced`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 13 Sep 2022 01:39:44 GMT
ADD file:414dad8d6231b19eca031ae43d450f7b700460907f7319c029b542ab528c5f9b in / 
# Tue, 13 Sep 2022 01:39:45 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 12:02:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Sep 2022 12:02:47 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 13 Sep 2022 12:02:48 GMT
ENV GOSU_VERSION=1.14
# Tue, 13 Sep 2022 12:02:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Sep 2022 12:03:03 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 13 Sep 2022 12:03:03 GMT
ENV LANG=en_US.utf8
# Tue, 13 Sep 2022 12:03:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:03:08 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Sep 2022 12:03:10 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 13 Sep 2022 12:03:10 GMT
ENV PG_MAJOR=15
# Tue, 13 Sep 2022 12:03:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 13 Sep 2022 12:03:12 GMT
ENV PG_VERSION=15~beta4-1.pgdg110+1
# Tue, 13 Sep 2022 12:16:51 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 13 Sep 2022 12:16:52 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 13 Sep 2022 12:16:53 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 13 Sep 2022 12:16:54 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Sep 2022 12:16:55 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 13 Sep 2022 12:16:56 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Sep 2022 12:16:58 GMT
COPY file:925d466681c8349f58385c00a8caa567c76b695158aa04bf4ad2ac92604e11c7 in /usr/local/bin/ 
# Tue, 13 Sep 2022 12:16:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Sep 2022 12:16:59 GMT
STOPSIGNAL SIGINT
# Tue, 13 Sep 2022 12:17:00 GMT
EXPOSE 5432
# Tue, 13 Sep 2022 12:17:01 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:221c5dcdb82ed8982a21341b5c0cadf79cc338347a649dc99854a5697661d7aa`  
		Last Modified: Tue, 13 Sep 2022 01:45:21 GMT  
		Size: 32.4 MB (32383788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f0a870fc8bfe357c23de086822c98f07ba465420201ac5cb693ca9a4d06de8`  
		Last Modified: Tue, 13 Sep 2022 13:20:00 GMT  
		Size: 4.6 MB (4607313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c41f7904ff3e43fadda4dd24c8b4fd27c6081397205f4b38d28412f5fe6043`  
		Last Modified: Tue, 13 Sep 2022 13:19:59 GMT  
		Size: 1.6 KB (1642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e2d55a0b2621e587186d758b61fd9ff4d246f637dd0e12bb28c1254e06ebc8`  
		Last Modified: Tue, 13 Sep 2022 13:20:00 GMT  
		Size: 1.4 MB (1385104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f42dad64e06a2b8d35c4b4bf48cc97e12b01d745d7e6dc35f10796f180ba484`  
		Last Modified: Tue, 13 Sep 2022 13:19:59 GMT  
		Size: 8.0 MB (8043595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a82cba01ac82996430cc3f18a764a32ee7da7cbd7541017dc28f5106a17dcd2`  
		Last Modified: Tue, 13 Sep 2022 13:19:57 GMT  
		Size: 1.0 MB (1027932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123b51666727bbb6183ca07be40cc0c2a6f45647571196f9ffadaa1594d4c2cb`  
		Last Modified: Tue, 13 Sep 2022 13:19:57 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf1cd2af05515bffd495de139a8d2ebc81ea5e596b1dcd6c843937c8158b3e8`  
		Last Modified: Tue, 13 Sep 2022 13:19:57 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3423866b02591dc2b41154d2faa297b8edd9165e2f19f9d2bba388bf86b6044`  
		Last Modified: Tue, 13 Sep 2022 13:20:07 GMT  
		Size: 94.0 MB (94014589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953c056f6fdde9824997d8c6e4b286ddc5eda3eb019ccbc4384b9a798b56d0fa`  
		Last Modified: Tue, 13 Sep 2022 13:19:55 GMT  
		Size: 9.8 KB (9803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf4dc7ed68bd943b325bf35a937b30696a2ed11e07defc2e30d02907d506df2`  
		Last Modified: Tue, 13 Sep 2022 13:19:55 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbcb57d1d398fea7cbf2e7542778e9bd68e2fc46d5721e7cc4f4d5c027856cf3`  
		Last Modified: Tue, 13 Sep 2022 13:19:55 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be2fe714b458e6e540b4f95a123dab6b5e352cfc796d7522e132d13e9cb56e7a`  
		Last Modified: Tue, 13 Sep 2022 13:19:55 GMT  
		Size: 4.7 KB (4706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15beta4` - linux; mips64le

```console
$ docker pull postgres@sha256:4ee4960b7226cabccba524f6a7ebc268dce7b505cf6e0dd188a7fc0c9e50e23b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134203783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd3884630c350eddd79d6edbc45c2b1859d7475542b34b2e142cd81e473c483`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 13 Sep 2022 01:10:58 GMT
ADD file:91a8d8627a614ff3741d68216da46f13b393e52a70377b97ef317e4a00a3cac6 in / 
# Tue, 13 Sep 2022 01:11:02 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 14:43:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Sep 2022 14:43:41 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 13 Sep 2022 14:43:43 GMT
ENV GOSU_VERSION=1.14
# Tue, 13 Sep 2022 14:44:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Sep 2022 14:44:42 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 13 Sep 2022 14:44:44 GMT
ENV LANG=en_US.utf8
# Tue, 13 Sep 2022 14:45:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 14:45:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Sep 2022 14:45:13 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 13 Sep 2022 14:45:15 GMT
ENV PG_MAJOR=15
# Tue, 13 Sep 2022 14:45:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 13 Sep 2022 14:45:20 GMT
ENV PG_VERSION=15~beta4-1.pgdg110+1
# Tue, 13 Sep 2022 15:45:33 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 13 Sep 2022 15:45:39 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 13 Sep 2022 15:45:44 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 13 Sep 2022 15:45:48 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Sep 2022 15:45:53 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 13 Sep 2022 15:45:56 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Sep 2022 15:45:59 GMT
COPY file:925d466681c8349f58385c00a8caa567c76b695158aa04bf4ad2ac92604e11c7 in /usr/local/bin/ 
# Tue, 13 Sep 2022 15:46:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Sep 2022 15:46:05 GMT
STOPSIGNAL SIGINT
# Tue, 13 Sep 2022 15:46:08 GMT
EXPOSE 5432
# Tue, 13 Sep 2022 15:46:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:98abeb1446d0e9df6f48d5f72a70b36598cfc1091c9a5ca82690bedcf320e2b3`  
		Last Modified: Tue, 13 Sep 2022 01:18:50 GMT  
		Size: 29.6 MB (29627659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97bfec8b9e7b7d31f973cceb93302a65963ae06c983f73aa88bbce1bcda91bd3`  
		Last Modified: Tue, 13 Sep 2022 20:11:33 GMT  
		Size: 4.2 MB (4196148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f818ae51564eec798f33b9643cdf63f2e67db1ce94cc4e8f11d06d6b0bd244dd`  
		Last Modified: Tue, 13 Sep 2022 20:11:28 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87eb8ae023a2a2a3ba3afd27352d2bb49bed82b36c82f3f55ba4eaa5cb6afce7`  
		Last Modified: Tue, 13 Sep 2022 20:11:29 GMT  
		Size: 1.3 MB (1297998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54fe0e57811c0d58b207335b6db1a45fa595f879d54382c21f4463acdafdf8e9`  
		Last Modified: Tue, 13 Sep 2022 20:11:33 GMT  
		Size: 8.0 MB (8043916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129db0977d2d87b3e4b20a2d335b69d08125a2da8848bd1eca491b5232675516`  
		Last Modified: Tue, 13 Sep 2022 20:11:26 GMT  
		Size: 1.1 MB (1089436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a032ad6e000df14e3f28f5afd617a26e772099d06629b3704d6cce1eadd9f12e`  
		Last Modified: Tue, 13 Sep 2022 20:11:26 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2738c7bad762eae3b4d5e9dce760b8494ee1e61b2097505ec64604a5630f17e5`  
		Last Modified: Tue, 13 Sep 2022 20:11:25 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746a727e0884f5e738ff59f4783d660eee212726bb2ab7da5b8792ae0215f58c`  
		Last Modified: Tue, 13 Sep 2022 20:12:24 GMT  
		Size: 89.9 MB (89928919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9550701ca38dd6b8b6c22516424f4d37f724b19ec27bab7997b0d6b623c0a663`  
		Last Modified: Tue, 13 Sep 2022 20:11:23 GMT  
		Size: 9.8 KB (9801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d87b0de4d0329fa4174e412c06d71d55071ce46a1f2bfffe2836644cbad270`  
		Last Modified: Tue, 13 Sep 2022 20:11:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0327893c74048905f8f2f2b2392ec27e8f6181eb6c50a58801f64b85849a79b`  
		Last Modified: Tue, 13 Sep 2022 20:11:23 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a20a0d8c2d86e07e11f0a193d6bff8723e7917ffab666d4020d5590d3b608f`  
		Last Modified: Tue, 13 Sep 2022 20:11:23 GMT  
		Size: 4.7 KB (4700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15beta4` - linux; ppc64le

```console
$ docker pull postgres@sha256:faf0335856deb3c41faf61d83eeed7241689b01c2d77030a76c574f2df7fe4b9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.9 MB (148911040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a724abb61d20ffbec63831cd7699873061e6f45f748c7722b1a89aa6a49dbf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 13 Sep 2022 02:07:56 GMT
ADD file:8b05dcf5f16a2ae9169b27aa848b812e07cd30414e51e4d53df9a5f01cd4c1a4 in / 
# Tue, 13 Sep 2022 02:07:58 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 04:39:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Sep 2022 04:39:45 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 13 Sep 2022 04:39:45 GMT
ENV GOSU_VERSION=1.14
# Tue, 13 Sep 2022 04:40:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Sep 2022 04:40:11 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 13 Sep 2022 04:40:12 GMT
ENV LANG=en_US.utf8
# Tue, 13 Sep 2022 04:40:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 04:40:21 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Sep 2022 04:40:23 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 13 Sep 2022 04:40:23 GMT
ENV PG_MAJOR=15
# Tue, 13 Sep 2022 04:40:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 13 Sep 2022 04:40:24 GMT
ENV PG_VERSION=15~beta4-1.pgdg110+1
# Tue, 13 Sep 2022 04:40:58 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 13 Sep 2022 04:41:02 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 13 Sep 2022 04:41:04 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 13 Sep 2022 04:41:04 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Sep 2022 04:41:05 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 13 Sep 2022 04:41:05 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Sep 2022 04:41:06 GMT
COPY file:925d466681c8349f58385c00a8caa567c76b695158aa04bf4ad2ac92604e11c7 in /usr/local/bin/ 
# Tue, 13 Sep 2022 04:41:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Sep 2022 04:41:06 GMT
STOPSIGNAL SIGINT
# Tue, 13 Sep 2022 04:41:07 GMT
EXPOSE 5432
# Tue, 13 Sep 2022 04:41:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9716ed411387b5ba1ec8278e9fb108a44d8a09ffbbbfd1639f06c63f20364b45`  
		Last Modified: Tue, 13 Sep 2022 02:13:40 GMT  
		Size: 35.3 MB (35277392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d760532999259b7bfa2cdf2d83030d0460227573cd2fee4a032deee47980fd`  
		Last Modified: Tue, 13 Sep 2022 04:48:07 GMT  
		Size: 5.2 MB (5222745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a76fcf5dc8d66cb471a4a9535ce7905a7f7878f84f5c21d799576f03e3430`  
		Last Modified: Tue, 13 Sep 2022 04:48:04 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b646a6ec49b1b9b19fdb14e070642643bef65bcf8e1e2873da4beeba4e5a0f20`  
		Last Modified: Tue, 13 Sep 2022 04:48:05 GMT  
		Size: 1.3 MB (1317481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62baaf98fccbc00b9f522e3f0be6972e8d57a13f63bdb115b7517e4025e5946a`  
		Last Modified: Tue, 13 Sep 2022 04:48:05 GMT  
		Size: 8.0 MB (8045321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5210842b5295014274c6d2c2f82f143bef940d66ab5e819dae71b53b7ae4b521`  
		Last Modified: Tue, 13 Sep 2022 04:48:03 GMT  
		Size: 1.4 MB (1420088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d344d41fb859facb15c49d51fc175ac6646fb76a8ddb1a436a9af7b7f935f07`  
		Last Modified: Tue, 13 Sep 2022 04:48:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042ed1cfd24a80b9aeddc89a52abd532d0c30e73c690e7215014b98aad9c41b9`  
		Last Modified: Tue, 13 Sep 2022 04:48:02 GMT  
		Size: 3.2 KB (3202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37863472ba672d727b81629fcf36779bd19f7909de7f824ff5e2c774eaee54a8`  
		Last Modified: Tue, 13 Sep 2022 04:48:24 GMT  
		Size: 97.6 MB (97608035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6dd2f0851ffd15a5a5f6e59173130f2c484b5d5f73a7a78d4bab0e27011d53`  
		Last Modified: Tue, 13 Sep 2022 04:48:00 GMT  
		Size: 9.8 KB (9800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507e652c04e19b13f2bb8721cba49124978236da16322377d7259e00d026a67b`  
		Last Modified: Tue, 13 Sep 2022 04:48:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07dbad1888d86da918776a521210414d3804f1536ddb960b3633f340023beda9`  
		Last Modified: Tue, 13 Sep 2022 04:48:00 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6be5bc4c29fd39a07b55550c476c4714e4fa707e34a5348143a4bac29f3ce60`  
		Last Modified: Tue, 13 Sep 2022 04:48:00 GMT  
		Size: 4.7 KB (4699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15beta4` - linux; s390x

```console
$ docker pull postgres@sha256:dd6ac37e79d0f33f7e1604d18e28a64311423eef36a19927737536ef474ff6ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86681186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c010ca987dd2bec20fc08eb6ae5c8c01d142f2d81f98124785c484b2d01370d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 13 Sep 2022 00:48:07 GMT
ADD file:e8a6c2e8be5d9d1f83c1e280419014489438391a9feb7c77b6c21adbf0ec062b in / 
# Tue, 13 Sep 2022 00:48:08 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 04:33:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Sep 2022 04:33:47 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 13 Sep 2022 04:33:47 GMT
ENV GOSU_VERSION=1.14
# Tue, 13 Sep 2022 04:33:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Sep 2022 04:33:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 13 Sep 2022 04:34:00 GMT
ENV LANG=en_US.utf8
# Tue, 13 Sep 2022 04:34:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 04:34:04 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Sep 2022 04:34:05 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 13 Sep 2022 04:34:05 GMT
ENV PG_MAJOR=15
# Tue, 13 Sep 2022 04:34:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 13 Sep 2022 04:34:05 GMT
ENV PG_VERSION=15~beta4-1.pgdg110+1
# Tue, 13 Sep 2022 04:41:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 13 Sep 2022 04:41:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 13 Sep 2022 04:41:43 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 13 Sep 2022 04:41:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Sep 2022 04:41:44 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 13 Sep 2022 04:41:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Sep 2022 04:41:44 GMT
COPY file:925d466681c8349f58385c00a8caa567c76b695158aa04bf4ad2ac92604e11c7 in /usr/local/bin/ 
# Tue, 13 Sep 2022 04:41:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Sep 2022 04:41:45 GMT
STOPSIGNAL SIGINT
# Tue, 13 Sep 2022 04:41:45 GMT
EXPOSE 5432
# Tue, 13 Sep 2022 04:41:45 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c64715e5ebd39975a39b5cf2535772544c27713cbed678b0a21e73680fffaf72`  
		Last Modified: Tue, 13 Sep 2022 00:52:39 GMT  
		Size: 29.6 MB (29635080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a2068830ae611a283597929af8437a2aa35d8b999846f9a4e2304ee7f2d042`  
		Last Modified: Tue, 13 Sep 2022 05:19:44 GMT  
		Size: 4.3 MB (4302222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a990ac96165d07d23730e03b4d82364440c24000d67be76c265dddbcc935fa2`  
		Last Modified: Tue, 13 Sep 2022 05:19:44 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4491edcdeaca0a18f0823080d7b4aaba011f8d16ba9f10bcbe92f616076dd05`  
		Last Modified: Tue, 13 Sep 2022 05:19:44 GMT  
		Size: 1.4 MB (1381522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b776fb53c2e35f5a6d0ce3b54d0c4d27f588892d0322bbdff2afd8dc36f95a`  
		Last Modified: Tue, 13 Sep 2022 05:19:44 GMT  
		Size: 8.1 MB (8099067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbe99d062f06821ee92e324d42fe30cc662d5ff9d0a4c7b0870a606fb7cf945`  
		Last Modified: Tue, 13 Sep 2022 05:19:42 GMT  
		Size: 1.2 MB (1237896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c5e2d9f401fb21fddb497b067bbad8c03a6290f2b1a741a03f36fcce2de833`  
		Last Modified: Tue, 13 Sep 2022 05:19:42 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2b78a4b02e740d86d6d28a0732d2135ca780504d5b03effa18a2ada281fa75`  
		Last Modified: Tue, 13 Sep 2022 05:19:42 GMT  
		Size: 3.2 KB (3203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6067b0911d202e7f31dc433d0c2180a9e110aa63029a670b5ebda2942266923c`  
		Last Modified: Tue, 13 Sep 2022 05:19:47 GMT  
		Size: 42.0 MB (42005423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2307fe14a1e8d169b9a7d0dc19a4770076a9c59cc9a86d722373dbe922fc30fc`  
		Last Modified: Tue, 13 Sep 2022 05:19:41 GMT  
		Size: 9.8 KB (9797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a00ab0482da4631850dac1269f1eedb5c95bacf1c9d4742ac785556ed2f97ad6`  
		Last Modified: Tue, 13 Sep 2022 05:19:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274a56497c370617152f6a72aa720657abbbedd4ae2ab1069425f6b4371ceb9a`  
		Last Modified: Tue, 13 Sep 2022 05:19:41 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998fe75ab8d87c05945df7b1cc3410045f44318e93d0884882fec046381bb20`  
		Last Modified: Tue, 13 Sep 2022 05:19:41 GMT  
		Size: 4.7 KB (4701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
