## `postgres:11-stretch`

```console
$ docker pull postgres@sha256:d038a996eee7f8726cb6a372ed6b9a63f92861bc37768d9eaf950463879833e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `postgres:11-stretch` - linux; amd64

```console
$ docker pull postgres@sha256:f0188c7381a57f4a9f14621c49189f7300196abbe20ad1b9658c547268fd86f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107452205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:954b4b6b154319b65307cf82394f84d6ba09a70f4878431c304369975ee06d86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 20 Apr 2022 04:45:25 GMT
ADD file:0fafb7f95dc18699227154856361058bc9aba65de2ff88bf55cc66363142a05e in / 
# Wed, 20 Apr 2022 04:45:25 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:57:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 20 Apr 2022 12:57:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 20 Apr 2022 12:57:27 GMT
ENV GOSU_VERSION=1.14
# Wed, 20 Apr 2022 12:57:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Apr 2022 12:57:44 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 20 Apr 2022 12:57:45 GMT
ENV LANG=en_US.utf8
# Wed, 20 Apr 2022 12:57:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:57:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Apr 2022 12:57:52 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 12:57:52 GMT
ENV PG_MAJOR=11
# Wed, 20 Apr 2022 12:57:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Wed, 20 Apr 2022 12:57:53 GMT
ENV PG_VERSION=11.15-1.pgdg90+1
# Wed, 20 Apr 2022 12:58:14 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						echo 'deb http://deb.debian.org/debian stretch-backports main' >> /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			apt-get install -y --no-install-recommends clang-6.0; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 20 Apr 2022 12:58:15 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 20 Apr 2022 12:58:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 20 Apr 2022 12:58:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 20 Apr 2022 12:58:16 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 20 Apr 2022 12:58:16 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 20 Apr 2022 12:58:16 GMT
COPY file:3cf28939740c4fc7f2787c08c792133ea7778bcbe5a7254c7efea56f5632f447 in /usr/local/bin/ 
# Wed, 20 Apr 2022 12:58:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Apr 2022 12:58:16 GMT
STOPSIGNAL SIGINT
# Wed, 20 Apr 2022 12:58:16 GMT
EXPOSE 5432
# Wed, 20 Apr 2022 12:58:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8bd3f5a20b90c0e84cc65ea4a9172a51b7b5c0b9a097fa88d7102cac91cddf2c`  
		Last Modified: Wed, 20 Apr 2022 04:52:27 GMT  
		Size: 22.6 MB (22567235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4778baaf8b12fff5e16c83bbae7eda62a939fbdc73e7af815229de1e2aeb7f`  
		Last Modified: Wed, 20 Apr 2022 13:02:12 GMT  
		Size: 4.5 MB (4504037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449d0cd2cc3c11359603f3e7277ed844bfa33b0763f9beae658b94c68d790b21`  
		Last Modified: Wed, 20 Apr 2022 13:02:11 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0babade0e92d01ba9cb4af0f8238f119bc682de990e53a26965cf3e7a3e0192f`  
		Last Modified: Wed, 20 Apr 2022 13:02:10 GMT  
		Size: 1.4 MB (1379583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13406c6552c3779e6e670ed7fc894b3b98f0fbc35113408a4d2d9d76bdac0702`  
		Last Modified: Wed, 20 Apr 2022 13:02:09 GMT  
		Size: 6.2 MB (6185762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044e726ba359254b2cf2c5bd28a2e7e006debeffe04cdfbdea578609745972b4`  
		Last Modified: Wed, 20 Apr 2022 13:02:08 GMT  
		Size: 1.2 MB (1249958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52525938cb44eae3135d009734d2acf121333ff51e4c56e90d885981257928b`  
		Last Modified: Wed, 20 Apr 2022 13:02:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c8bb0355f81195f313034c2de11abc6867cceb1e3d7a1456157e34a4398210`  
		Last Modified: Wed, 20 Apr 2022 13:02:08 GMT  
		Size: 5.6 KB (5585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08dd157d23ce2e6ae7b91086d60f6ad7cdb20be8cb0f6a7fc0efd00a4edf0545`  
		Last Modified: Wed, 20 Apr 2022 13:02:16 GMT  
		Size: 71.5 MB (71544728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cddbdd8b7736e648e337258674c4f150709bbf0d06519022f202ca5697db1e7`  
		Last Modified: Wed, 20 Apr 2022 13:02:05 GMT  
		Size: 8.3 KB (8324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5403b52c402e324d28825e09269a663e340a324bf63b23dee12fea19d0a820`  
		Last Modified: Wed, 20 Apr 2022 13:02:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13e8017d44a173b86ff9796b56b8a412bbed8d866c205e0177c2cd4f6c2562c`  
		Last Modified: Wed, 20 Apr 2022 13:02:05 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e882fa2d252bb75e37e1d8859cc4167c3d1c1f907264e20871da97c46ac6aa`  
		Last Modified: Wed, 20 Apr 2022 13:02:05 GMT  
		Size: 4.7 KB (4706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-stretch` - linux; arm variant v5

```console
$ docker pull postgres@sha256:1d1c0294ab3b76e464b93656fab1734fe85405765412d65e77f16ab8b123cc5a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71567300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:671d76425504d459908d344934f95773738ab106622cd2498bbe419a520702f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 20 Apr 2022 07:22:40 GMT
ADD file:8caa5e7ca2ab4b420bed155bd2190baa73ca3c4e9378db02b0c0cede15974d69 in / 
# Wed, 20 Apr 2022 07:22:41 GMT
CMD ["bash"]
# Thu, 21 Apr 2022 05:04:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 21 Apr 2022 05:04:52 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 21 Apr 2022 05:04:53 GMT
ENV GOSU_VERSION=1.14
# Thu, 21 Apr 2022 05:05:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Apr 2022 05:05:45 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 21 Apr 2022 05:05:45 GMT
ENV LANG=en_US.utf8
# Thu, 21 Apr 2022 05:05:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Apr 2022 05:05:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 21 Apr 2022 05:06:03 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 21 Apr 2022 05:06:04 GMT
ENV PG_MAJOR=11
# Thu, 21 Apr 2022 05:06:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Thu, 21 Apr 2022 05:06:05 GMT
ENV PG_VERSION=11.15-1.pgdg90+1
# Thu, 21 Apr 2022 05:32:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						echo 'deb http://deb.debian.org/debian stretch-backports main' >> /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			apt-get install -y --no-install-recommends clang-6.0; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Thu, 21 Apr 2022 05:33:01 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Thu, 21 Apr 2022 05:33:03 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 21 Apr 2022 05:33:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Apr 2022 05:33:05 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 21 Apr 2022 05:33:05 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Apr 2022 05:33:06 GMT
COPY file:3cf28939740c4fc7f2787c08c792133ea7778bcbe5a7254c7efea56f5632f447 in /usr/local/bin/ 
# Thu, 21 Apr 2022 05:33:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Apr 2022 05:33:07 GMT
STOPSIGNAL SIGINT
# Thu, 21 Apr 2022 05:33:07 GMT
EXPOSE 5432
# Thu, 21 Apr 2022 05:33:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2d96febf107fb8f8f8c5d8bd55514488bd2c5f9ca3c49cb1c015381d7aa816d6`  
		Last Modified: Wed, 20 Apr 2022 07:40:19 GMT  
		Size: 21.2 MB (21240552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9cd0b388029fbfa4d57c2ae64305c0a8c85323cf5385fef637d22359b031b0`  
		Last Modified: Thu, 21 Apr 2022 06:30:36 GMT  
		Size: 4.2 MB (4239488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d781ed8c92f5a9788a3d47a2251d2f520a385d125635abc18e10a98ef9addf2f`  
		Last Modified: Thu, 21 Apr 2022 06:30:33 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79bcb22951ec385fe3134b67da8c047efec0cebb84e85b00ac03ab3b1adb0471`  
		Last Modified: Thu, 21 Apr 2022 06:30:34 GMT  
		Size: 1.3 MB (1344469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e581a6b855f249872175b1cb60b7e3bba40c4856d9b59921c8bfd667c741db3b`  
		Last Modified: Thu, 21 Apr 2022 06:30:35 GMT  
		Size: 6.2 MB (6185799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4479ef4ec7ac6d1caa391282c84b04a842084fd150f26cf3d4e960ed1de5bed6`  
		Last Modified: Thu, 21 Apr 2022 06:30:32 GMT  
		Size: 1.2 MB (1194860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b314b61736c98f0f1494aa7ef45e038647271883795f2e42fbd812aa8901ee1`  
		Last Modified: Thu, 21 Apr 2022 06:30:31 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55aed70ec75a7cee1628c53e6263cacd11e9ae72c08c8e9e4a5800a290153f06`  
		Last Modified: Thu, 21 Apr 2022 06:30:31 GMT  
		Size: 5.6 KB (5585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e07a2731d46986ee2ef3f8e39e44b744339229022b0d9dd4c7e017c01201e0`  
		Last Modified: Thu, 21 Apr 2022 06:30:56 GMT  
		Size: 37.3 MB (37341236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40383ceeadc3978052b889d811519f13efef0eace5c4f3917c1c31c634b2a60`  
		Last Modified: Thu, 21 Apr 2022 06:30:29 GMT  
		Size: 8.3 KB (8327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187294f98c0092400473ca5da176ce3d177f663a737062d2eda9902e60ced6a6`  
		Last Modified: Thu, 21 Apr 2022 06:30:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4032c080004dcc14f7c4edfeab75ec09039eddea68e54b1b202120694901d92b`  
		Last Modified: Thu, 21 Apr 2022 06:30:30 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4109f200b0b5d0fcc88ec0d55a3a33f065ef8a84d0d53784a51e8e260b34bb56`  
		Last Modified: Thu, 21 Apr 2022 06:30:30 GMT  
		Size: 4.7 KB (4708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-stretch` - linux; arm variant v7

```console
$ docker pull postgres@sha256:9f57640c2a66859f35916a02d7d0e6b8a16c2eddc06b5fd9920361fa84c2c6fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68119228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df0219ba4744d01d2541c4fc34a32f3a6cdbfd69e69a1920d9eae7599f51bf31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 20 Apr 2022 13:33:51 GMT
ADD file:096692331564a30a9a9c6b24e681d99d68b54eeeabb7c5ac7d4073de06e050b2 in / 
# Wed, 20 Apr 2022 13:33:51 GMT
CMD ["bash"]
# Thu, 21 Apr 2022 08:36:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 21 Apr 2022 08:36:13 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 21 Apr 2022 08:36:14 GMT
ENV GOSU_VERSION=1.14
# Thu, 21 Apr 2022 08:36:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Apr 2022 08:37:00 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 21 Apr 2022 08:37:01 GMT
ENV LANG=en_US.utf8
# Thu, 21 Apr 2022 08:37:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Apr 2022 08:37:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 21 Apr 2022 08:37:16 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 21 Apr 2022 08:37:17 GMT
ENV PG_MAJOR=11
# Thu, 21 Apr 2022 08:37:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Thu, 21 Apr 2022 08:37:18 GMT
ENV PG_VERSION=11.15-1.pgdg90+1
# Thu, 21 Apr 2022 09:00:48 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						echo 'deb http://deb.debian.org/debian stretch-backports main' >> /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			apt-get install -y --no-install-recommends clang-6.0; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Thu, 21 Apr 2022 09:00:50 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Thu, 21 Apr 2022 09:00:51 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 21 Apr 2022 09:00:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Apr 2022 09:00:54 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 21 Apr 2022 09:00:54 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Apr 2022 09:00:54 GMT
COPY file:3cf28939740c4fc7f2787c08c792133ea7778bcbe5a7254c7efea56f5632f447 in /usr/local/bin/ 
# Thu, 21 Apr 2022 09:00:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Apr 2022 09:00:55 GMT
STOPSIGNAL SIGINT
# Thu, 21 Apr 2022 09:00:56 GMT
EXPOSE 5432
# Thu, 21 Apr 2022 09:00:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:08da560f0b65b004ba95f9a431d3ac51b8807b16ec6ef170e2e00dc55330246d`  
		Last Modified: Wed, 20 Apr 2022 13:51:07 GMT  
		Size: 19.4 MB (19359807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8b330e9f5f7b6093bd31383fc931a0fa0a7eb6042397b6e3dcc03bb15cea72`  
		Last Modified: Thu, 21 Apr 2022 09:55:38 GMT  
		Size: 3.9 MB (3875757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3277f4f87432620a37e3aa7a47954d3cf169efb2131a0d9fe8dfedc6ce3d461b`  
		Last Modified: Thu, 21 Apr 2022 09:55:35 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbcb6c15b947cd08ea74086c0d6dc455f6ead2fca72a83a758b6f334ac4ec413`  
		Last Modified: Thu, 21 Apr 2022 09:55:36 GMT  
		Size: 1.3 MB (1336118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f00177879e49a97a5b586558a0d87cf5440883302e19eb77df6459a90fd2e985`  
		Last Modified: Thu, 21 Apr 2022 09:55:38 GMT  
		Size: 6.2 MB (6185622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253fa72cc5d70cc9794fa2f8d288a2032b413110083f92161605f095310c6f1e`  
		Last Modified: Thu, 21 Apr 2022 09:55:34 GMT  
		Size: 1.1 MB (1097110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3662c97846d60d8e720bca2261af9de33a591425a77e04066500c29bf271aa47`  
		Last Modified: Thu, 21 Apr 2022 09:55:34 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f50c6456c2f66633a0f5f5b48def9ef146946eb2cb331352b1c1e081f45622`  
		Last Modified: Thu, 21 Apr 2022 09:55:34 GMT  
		Size: 5.6 KB (5585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a59c8844aac0da93670b7fea50ea3f0c33042653a21fb430e438522a6dd88b5`  
		Last Modified: Thu, 21 Apr 2022 09:55:56 GMT  
		Size: 36.2 MB (36243906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8586917aae944d6bf2b8d95ef710a8d8ebcffd883e6eb6c76c0d2c19b47f2db`  
		Last Modified: Thu, 21 Apr 2022 09:55:32 GMT  
		Size: 8.3 KB (8335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40016b7ebcdfd86d5e7dc810f9d7e2adb9d3a22f2a7e3cebe82ed2ffcf357bdb`  
		Last Modified: Thu, 21 Apr 2022 09:55:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca9babc502f777989476a5cf50f938cea5ffec856e38c2e20b04c6458b9a14d`  
		Last Modified: Thu, 21 Apr 2022 09:55:32 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5181c5489733346103a949723a4e3f939faa036630547edfe5ac0aff4c7f3074`  
		Last Modified: Thu, 21 Apr 2022 09:55:32 GMT  
		Size: 4.7 KB (4707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-stretch` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:21107fc0b02fd261be595f05d02c2fcbca8bb8cd957a1b3dfb214fcf94152f51
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70451408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348afa0933fbc88a88a80739f12594696a4d84004ae4d2f9d277566dfeca3c10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 20 Apr 2022 04:31:34 GMT
ADD file:02ad9214474cf0e6d278d7015dee30e6a8e24cdc699812f5fb3915491177e92b in / 
# Wed, 20 Apr 2022 04:31:34 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 11:07:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 20 Apr 2022 11:07:34 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 20 Apr 2022 11:07:35 GMT
ENV GOSU_VERSION=1.14
# Wed, 20 Apr 2022 11:07:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Apr 2022 11:07:54 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 20 Apr 2022 11:07:55 GMT
ENV LANG=en_US.utf8
# Wed, 20 Apr 2022 11:08:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 11:08:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Apr 2022 11:08:05 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 11:08:05 GMT
ENV PG_MAJOR=11
# Wed, 20 Apr 2022 11:08:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Wed, 20 Apr 2022 11:08:07 GMT
ENV PG_VERSION=11.15-1.pgdg90+1
# Wed, 20 Apr 2022 11:17:24 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						echo 'deb http://deb.debian.org/debian stretch-backports main' >> /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			apt-get install -y --no-install-recommends clang-6.0; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 20 Apr 2022 11:17:25 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 20 Apr 2022 11:17:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 20 Apr 2022 11:17:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 20 Apr 2022 11:17:28 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 20 Apr 2022 11:17:29 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 20 Apr 2022 11:17:31 GMT
COPY file:3cf28939740c4fc7f2787c08c792133ea7778bcbe5a7254c7efea56f5632f447 in /usr/local/bin/ 
# Wed, 20 Apr 2022 11:17:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Apr 2022 11:17:32 GMT
STOPSIGNAL SIGINT
# Wed, 20 Apr 2022 11:17:33 GMT
EXPOSE 5432
# Wed, 20 Apr 2022 11:17:34 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0fca491399855be4c9b780dca621b48440831235d7916e5695b876698df84db7`  
		Last Modified: Wed, 20 Apr 2022 04:40:05 GMT  
		Size: 20.4 MB (20424115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c744d15db685c637fde12480f30e06c2effc7938de38841c7735bdd5bb6a8f1e`  
		Last Modified: Wed, 20 Apr 2022 11:31:05 GMT  
		Size: 3.9 MB (3890921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6c33f314a5ab52cedea73b4f9ba749bd283456dbb20c7bb4bf33e7c924d478`  
		Last Modified: Wed, 20 Apr 2022 11:31:04 GMT  
		Size: 1.7 KB (1659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f60fadfe10dbd27e8e863baa874f54670a484a870b54fa264f3dd51ad5892ba`  
		Last Modified: Wed, 20 Apr 2022 11:31:04 GMT  
		Size: 1.3 MB (1307845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a1ede32b323841cc5ceb6dcda3d3f841a9cce450021b8941a156d9d8f87fb4`  
		Last Modified: Wed, 20 Apr 2022 11:31:03 GMT  
		Size: 6.2 MB (6182549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e38d8d4286e633f7fde253eac390d08acdf3cf58ba2682a6e52e8157e31f22`  
		Last Modified: Wed, 20 Apr 2022 11:31:02 GMT  
		Size: 1.0 MB (1007488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7163d72e4f9abf7d1ceb9ba3bb3ab90563b823a8fc6c592c6e0d1771e70933e`  
		Last Modified: Wed, 20 Apr 2022 11:31:02 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7895fcb718ed1d42408313ed75791c3b2c321327c71511f25dea819b6837d2fa`  
		Last Modified: Wed, 20 Apr 2022 11:31:02 GMT  
		Size: 5.5 KB (5526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72de8a8b94faf653c72e6cac187f9fe344cb5e236a50a7a7dd4519a830e0768c`  
		Last Modified: Wed, 20 Apr 2022 11:31:06 GMT  
		Size: 37.6 MB (37617861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f53206fc83d222cd68f233be30386e7a3438a4c134626ac116a31a23105224`  
		Last Modified: Wed, 20 Apr 2022 11:31:00 GMT  
		Size: 8.3 KB (8327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e117354ff51cdd2d1e0a1f83322bdeeb3ad5e8432ba4b4a89ddfd7b616609b`  
		Last Modified: Wed, 20 Apr 2022 11:30:59 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba13113858ec9512d7b90004b258abe510aad7d328fdb3657ddf982aedb5b66`  
		Last Modified: Wed, 20 Apr 2022 11:30:59 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7892415d1fa98b3b000af3ef390a1b8873bb7049f4be9762024a6a5c3f7c56df`  
		Last Modified: Wed, 20 Apr 2022 11:30:59 GMT  
		Size: 4.7 KB (4703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-stretch` - linux; 386

```console
$ docker pull postgres@sha256:a00998ec764925151d2d5499e79549942d4f840bd609a74457caeadd23f874c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110477954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa5c91a263220329c279a76a361b43f3203d3e525c93c6be2d1bc43606b0179`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 20 Apr 2022 07:40:12 GMT
ADD file:f1394937f911449ed9fb7103f2bfb5b299d7779e98c4f0f34bcee08f8c2bf5db in / 
# Wed, 20 Apr 2022 07:40:12 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 15:36:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 20 Apr 2022 15:36:54 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 20 Apr 2022 15:36:55 GMT
ENV GOSU_VERSION=1.14
# Wed, 20 Apr 2022 15:37:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Apr 2022 15:37:14 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 20 Apr 2022 15:37:15 GMT
ENV LANG=en_US.utf8
# Wed, 20 Apr 2022 15:37:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 15:37:21 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Apr 2022 15:37:25 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 15:37:26 GMT
ENV PG_MAJOR=11
# Wed, 20 Apr 2022 15:37:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Wed, 20 Apr 2022 15:37:28 GMT
ENV PG_VERSION=11.15-1.pgdg90+1
# Wed, 20 Apr 2022 15:37:53 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						echo 'deb http://deb.debian.org/debian stretch-backports main' >> /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			apt-get install -y --no-install-recommends clang-6.0; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 20 Apr 2022 15:37:53 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 20 Apr 2022 15:37:54 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 20 Apr 2022 15:37:55 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 20 Apr 2022 15:37:56 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 20 Apr 2022 15:37:57 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 20 Apr 2022 15:37:59 GMT
COPY file:3cf28939740c4fc7f2787c08c792133ea7778bcbe5a7254c7efea56f5632f447 in /usr/local/bin/ 
# Wed, 20 Apr 2022 15:37:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Apr 2022 15:38:00 GMT
STOPSIGNAL SIGINT
# Wed, 20 Apr 2022 15:38:01 GMT
EXPOSE 5432
# Wed, 20 Apr 2022 15:38:02 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:da9db5d720427742cbccdd8a4a37dfaa81873ab9db6de4935623ca79ce881ee4`  
		Last Modified: Wed, 20 Apr 2022 07:49:16 GMT  
		Size: 23.2 MB (23202179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a19a0baab9c5f1c86bebceffadbcfe7fd451c8a910f18c2babf36f705044186`  
		Last Modified: Wed, 20 Apr 2022 15:51:54 GMT  
		Size: 4.6 MB (4623970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e707671a934c17e1a8b262ee2286cfeb577284e94526e07df6c847ba6510027`  
		Last Modified: Wed, 20 Apr 2022 15:51:53 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bcfda53779c607adc87ed6a474a52b627a5a546de05abcb3fc1c21d6596901`  
		Last Modified: Wed, 20 Apr 2022 15:51:53 GMT  
		Size: 1.3 MB (1347001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa18a1672a13861ddd4a58cad34f8d9f3ca9a6d02d20d1972e36cc43a7f9d1f`  
		Last Modified: Wed, 20 Apr 2022 15:51:52 GMT  
		Size: 6.2 MB (6182757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d175adb3274101f49e7561af949e1d39138b019e12c6e52049f37dfb47643c11`  
		Last Modified: Wed, 20 Apr 2022 15:51:51 GMT  
		Size: 1.0 MB (1030583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1565349cbf96dddd687407d720f1a0781d814acaccecc9220c8d8b2c4dae517`  
		Last Modified: Wed, 20 Apr 2022 15:51:51 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d117f40047eba468fbabae95facae7abd5e112c59c768f1da23718648cb335c`  
		Last Modified: Wed, 20 Apr 2022 15:51:51 GMT  
		Size: 5.5 KB (5526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bdb30cd0e85e3c0da44110aaa6a987075b3d32ec4da5e84fc9e3615c130a91f`  
		Last Modified: Wed, 20 Apr 2022 15:52:00 GMT  
		Size: 74.1 MB (74070831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956c221e5240fc15c7111d90923b9554ce785f91a5f02e6623512dd837583ff5`  
		Last Modified: Wed, 20 Apr 2022 15:51:48 GMT  
		Size: 8.3 KB (8331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b088f1b77671e5e3b3bd28c8909d35ee32a68795df701869912fb19cf5f5286`  
		Last Modified: Wed, 20 Apr 2022 15:51:48 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6164a2c80bcbbf9059fe4651717d9e2a5614bfb2842124f770bf3ebab95bf6ff`  
		Last Modified: Wed, 20 Apr 2022 15:51:48 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ffc75306f03a606e587b186b3bb528333f975340211bbba857ad6777aa63ec2`  
		Last Modified: Wed, 20 Apr 2022 15:51:48 GMT  
		Size: 4.7 KB (4707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
