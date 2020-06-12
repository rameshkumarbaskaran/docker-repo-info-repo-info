<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mariadb`

-	[`mariadb:10`](#mariadb10)
-	[`mariadb:10.1`](#mariadb101)
-	[`mariadb:10.1.45`](#mariadb10145)
-	[`mariadb:10.1.45-bionic`](#mariadb10145-bionic)
-	[`mariadb:10.1-bionic`](#mariadb101-bionic)
-	[`mariadb:10.2`](#mariadb102)
-	[`mariadb:10.2.32`](#mariadb10232)
-	[`mariadb:10.2.32-bionic`](#mariadb10232-bionic)
-	[`mariadb:10.2-bionic`](#mariadb102-bionic)
-	[`mariadb:10.3`](#mariadb103)
-	[`mariadb:10.3.23`](#mariadb10323)
-	[`mariadb:10.3.23-focal`](#mariadb10323-focal)
-	[`mariadb:10.3-focal`](#mariadb103-focal)
-	[`mariadb:10.4`](#mariadb104)
-	[`mariadb:10.4.13`](#mariadb10413)
-	[`mariadb:10.4.13-focal`](#mariadb10413-focal)
-	[`mariadb:10.4-focal`](#mariadb104-focal)
-	[`mariadb:10.5`](#mariadb105)
-	[`mariadb:10.5.3`](#mariadb1053)
-	[`mariadb:10.5.3-focal`](#mariadb1053-focal)
-	[`mariadb:10.5-focal`](#mariadb105-focal)
-	[`mariadb:10-focal`](#mariadb10-focal)
-	[`mariadb:focal`](#mariadbfocal)
-	[`mariadb:latest`](#mariadblatest)
-	[`mariadb:rc`](#mariadbrc)
-	[`mariadb:rc-focal`](#mariadbrc-focal)

## `mariadb:10`

```console
$ docker pull mariadb@sha256:3ce8368efbf25059a1b7d2ff1df9f1cdb52fcd272eb2b906599e8613971379bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10` - linux; amd64

```console
$ docker pull mariadb@sha256:b0fe725e9008b651ee0577383887728879986580d1e0a809dc263a04d1c40907
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123544564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41c9d63e23e3408f9615c5519ef1a540874e867460268af29993862155376a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:25:03 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:25:22 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:25:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:25:23 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:25:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:25:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:25:24 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:25:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d075a6a30ab84cd85dbfe7ff6b7ff4b1da51420bb6502fbbcd165a6362314d89`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d12c1b8c73e8aaa38978b59b62c4a6d88faaf072f8dd8170cc20c995ea6182`  
		Last Modified: Fri, 12 Jun 2020 18:27:01 GMT  
		Size: 86.9 MB (86868588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10938405ff505cbefc2abf93e72607642d6d13d611bf1df914c7ccc62f2010fa`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 4.9 KB (4851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3656315d96d9326a97929d688679e34d594759499e9f6e6652ce44a70d285c64`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:8c7b8ef0282a747aa0e686f5c2d3b68f050f8d5aebc51884681057f3d6bab5af
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121139407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227094abd47e39aba82a11a0d4aff3492e3733207529c4fb90f4d1fa8299d10c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 00:18:16 GMT
ADD file:e9947aff2dfa8f220d4b25dc0770aff8d9ffc08482e52f54833f39e1c3ec08bf in / 
# Fri, 24 Apr 2020 00:18:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 00:18:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:18:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:18:29 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:53:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:53:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:53:46 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:54:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:54:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:54:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:54:14 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:54:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:55:26 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:55:26 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:55:28 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:56:18 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:56:20 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:56:21 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:56:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:56:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:56:24 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:56:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c2d76ba33f8d52087147ce28d8f03c08f69677591e3e10db810bf76a6e09427`  
		Last Modified: Fri, 24 Apr 2020 00:22:00 GMT  
		Size: 27.2 MB (27158644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92d4cfc71d3821474946021fdbf241a74992a84c6269c3e9a052ce7fc56cece`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 32.3 KB (32326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63063bfe137200b3c8d1ee8d819124352c20ee8c189a0388f461ec66bb759310`  
		Last Modified: Fri, 24 Apr 2020 00:21:53 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38385900086ffa7d7cb9c3bbeabaf2176d7d7958ebf0736d2a01773a830201ee`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0959e86d4d132b0e91456f1d1ecc3b1d6518d720b7ee82926559fd34800d7b53`  
		Last Modified: Fri, 12 Jun 2020 18:58:18 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f37953089cdddf8b409b61f0f30de595d96483dd0ce38463384dd5d201b70f`  
		Last Modified: Fri, 12 Jun 2020 18:58:19 GMT  
		Size: 5.5 MB (5456917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab7a5713dbb2830a805d0b68dae96ce4dd827b086473a3d785f76b37d885fe1`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 1.3 MB (1258973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0614221a0d602714b38672c572d4071df43a41223dab9b1c81ab45ea5bc9c9`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e232435757d992d57a40890acb9528958726ef62b7f400e4ef7c3b7d97c234c`  
		Last Modified: Fri, 12 Jun 2020 18:58:16 GMT  
		Size: 1.3 MB (1263367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb430a3947464ff3d178d412e9047e4b67e2cc3a09923dd4b84596fa57403d66`  
		Last Modified: Fri, 12 Jun 2020 18:58:15 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c366377b87f5bd2fac450a70e60f1eb72d08d295b001fe3744ab2ce6aba51c50`  
		Last Modified: Fri, 12 Jun 2020 18:58:52 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2724d7dec4121bbe85b94aa2443356afd739e9b04e6adfc6f42b6b6e905a95f7`  
		Last Modified: Fri, 12 Jun 2020 18:59:19 GMT  
		Size: 86.0 MB (85958453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c46e43e925893ef88759184e58a70d17f45392e6524dfddf0d68becb6077b9`  
		Last Modified: Fri, 12 Jun 2020 18:58:52 GMT  
		Size: 4.9 KB (4851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d77187f1fde12afc91b5b14093343ab71bc1d97ed7e79c60e4722d5c39ea0ca`  
		Last Modified: Fri, 12 Jun 2020 18:58:53 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a1705f7fecaefda698c2cf024327bca91cb8f66f2103614ae4d050f3ae194a4e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133498155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d3057995bde70b21d4b3cf61e8df037115877ab7f95cdf5326e78e3c2020c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:56:35 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:56:46 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:57:04 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 19:02:53 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 19:03:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 19:03:18 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 19:03:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 19:03:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 19:04:08 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 19:04:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03b359a03f81831c2fd57d9416ebc819388fd8574d85ad8898645d72f66c3c7`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09607cc66ed45e59b9ecfd2ed2dde55ce5b8e9b80729c7e1e9afa3c8d8e417ec`  
		Last Modified: Fri, 12 Jun 2020 19:14:23 GMT  
		Size: 91.0 MB (90987667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4bd398a89880ad4c07dbeb3afa3e02a724fbc012f4713549758f5ea6f58a11`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dfb689374ca4c43f6019d271c2cd0aa592a343710516129428cebb3c3cb9e3`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.1`

```console
$ docker pull mariadb@sha256:71d9a83b9ce7bccd14eeefb272037eaea38de3b71c972d77df68efb30a962ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.1` - linux; amd64

```console
$ docker pull mariadb@sha256:f5d667508a4e81b80e16a17e4992069cc51275f3b89f99e08d2ce977ee8309db
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113187713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad20783a626b1fe3239b83ea2bc12842cbab5929696a13c52a7e4d7f7d3c1e49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:00 GMT
ADD file:c3e6bb316dfa6b81dd4478aaa310df532883b1c0a14edeec3f63d641980c1789 in / 
# Fri, 24 Apr 2020 01:07:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 20:07:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 20:07:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:07:25 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 20:07:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 20:07:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 20:07:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:07:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 20:07:43 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 20:10:08 GMT
ENV MARIADB_MAJOR=10.1
# Wed, 13 May 2020 20:51:55 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Wed, 13 May 2020 20:51:56 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 20:52:31 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 20:52:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:21:50 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:21:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:21:51 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:23884877105a7ff84a910895cd044061a4561385ff6c36480ee080b76ec0e771`  
		Last Modified: Sat, 04 Apr 2020 12:21:10 GMT  
		Size: 26.7 MB (26689802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc38caa0f5b94141276220daaf428892096e4afd24b05668cd188311e00a635f`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 35.4 KB (35367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2910811b6c4227c2f42aaea9a3dd5f53b1d469f67e2cf7e601f631b119b61ff7`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36505266dcc64eeb1010bd2112e6f73981e1a8246e4f6d4e287763b57f101b0b`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69dcc78e96eb792fb67240a5ff4db2c3e3cb1ff55f97df2bddba0706fb5f6e6`  
		Last Modified: Fri, 24 Apr 2020 20:10:59 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222f44c5392d7a36df5eb58bb790223d332bd187fc56f006ecd66ad762f740e8`  
		Last Modified: Fri, 24 Apr 2020 20:10:59 GMT  
		Size: 4.8 MB (4807438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc64ea97b9cf087977c9a7972347db33f40487bcdd29abb41e7acf4c265335a`  
		Last Modified: Fri, 24 Apr 2020 20:10:58 GMT  
		Size: 1.3 MB (1326271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9912a149de6b3da2628c28ecfbd75992cda34df498d3634e6145bfdf1832a1a2`  
		Last Modified: Fri, 24 Apr 2020 20:10:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef6cf5b569752da3539a3b0c377a2a4f64e90f26eb7c89d405cf0168c923106`  
		Last Modified: Fri, 24 Apr 2020 20:10:57 GMT  
		Size: 929.2 KB (929212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a05be3688e04bf9961d4912e2dd86ff9832e72ec8c6b2d34c053e87ccf991a6`  
		Last Modified: Fri, 24 Apr 2020 20:10:57 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b4846a5211cc19dffa385f6714141c9e4065ea1b8272f2d1b588919011e3bd`  
		Last Modified: Wed, 13 May 2020 21:44:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c708c0ebee78df6312129e0d725d9170751f26045dadf8a29d284a923fe4aa4f`  
		Last Modified: Wed, 13 May 2020 21:44:48 GMT  
		Size: 79.4 MB (79386150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6485241d1dd9a47ea4347f8c032f9900c3fcc01b13802f80428807c69edda7a`  
		Last Modified: Fri, 29 May 2020 00:22:34 GMT  
		Size: 4.8 KB (4848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ab70faee57e501347812c3016018fdb049c752cc1352f893deecea9950b218`  
		Last Modified: Fri, 29 May 2020 00:22:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:65d8699feaa5976ee9351a972b09a9dcd17ae3748f97da3bfe5a33bac7683fa7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.8 MB (105804343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee5218a31ee4eff81de0a40e5aa28c3a92fcb5596f2914cd718a47f0bb5b51d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 00:16:45 GMT
ADD file:bd5b3470601aa4a28132ec60a8b1c33516d09a1391864fe1dbf82a4030397fd1 in / 
# Fri, 24 Apr 2020 00:16:54 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 00:16:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:17:03 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:17:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 15:47:33 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 15:47:50 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 15:47:51 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 15:48:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 15:48:10 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 15:48:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 15:48:23 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 15:48:25 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 15:52:49 GMT
ENV MARIADB_MAJOR=10.1
# Wed, 13 May 2020 20:49:52 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Wed, 13 May 2020 20:49:54 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 20:50:57 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 20:51:00 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:41:03 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:41:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:41:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:41:06 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:41:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c2cd007b69f7e5f37c851aa689e0e617fbaa3fe3e470f714337a03e569b7f434`  
		Last Modified: Sun, 05 Apr 2020 20:25:25 GMT  
		Size: 23.7 MB (23720401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c087f8bf83d28baa9c53fc5cfb0dfc79d5062cfad77563076553b04259e822f`  
		Last Modified: Fri, 24 Apr 2020 00:21:16 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474b5c43e9a24e1958763941a17a7cac60b13460a47f2ae9067ec03ceadab33a`  
		Last Modified: Fri, 24 Apr 2020 00:21:15 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7083e6591d76b9a6c13497a6a89bfbae3e7eb2eb31bec366bec3884c8e4517ce`  
		Last Modified: Fri, 24 Apr 2020 00:21:15 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340e908aa186ab7f11f80142d1c3a5bd2f7dbec25f58366dda5f22f44e06423c`  
		Last Modified: Fri, 24 Apr 2020 15:54:13 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f46da80a1eb3c07ecc7bb3784555bd9d502290a55fe1a3fe968f7446af3128`  
		Last Modified: Fri, 24 Apr 2020 15:54:14 GMT  
		Size: 4.4 MB (4393199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9374369ce5226b7dd75e6aae1665b5dd86552811ba35823b717d507c63063a0a`  
		Last Modified: Fri, 24 Apr 2020 15:54:13 GMT  
		Size: 1.3 MB (1262945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65d1839f1c97b9a6854699dfa28e745e6e8790a326818902165e646d97e8182`  
		Last Modified: Fri, 24 Apr 2020 15:54:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ac11fc4bc1dcef89d539dcbef6f8683a59c653edbf6b6b8674aaaf8b2b8c4b`  
		Last Modified: Fri, 24 Apr 2020 15:54:12 GMT  
		Size: 920.8 KB (920766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cf075dcf71cf7ff1c9ab8fa8b58253be69db20633df6da9c5ea5cf7b48b385`  
		Last Modified: Fri, 24 Apr 2020 15:54:11 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7968e8131541efc5e72522abdd8c094b9619e86b7642f20bbfcc9522790c06f7`  
		Last Modified: Wed, 13 May 2020 20:54:02 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbff971dc2e308bfb3e161a340d655fd9e631763dea02e60558c5c89dbe4e02`  
		Last Modified: Wed, 13 May 2020 20:55:24 GMT  
		Size: 75.5 MB (75458297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860b1eacccdefb29e8077566f4c9c5c6a58890d3692fccb302fb1f451a6cfa52`  
		Last Modified: Fri, 29 May 2020 00:42:09 GMT  
		Size: 4.9 KB (4851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3202d23d7160445948175e254bd9182f9976a70221f940f94237fbf0804c43aa`  
		Last Modified: Fri, 29 May 2020 00:42:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1` - linux; ppc64le

```console
$ docker pull mariadb@sha256:85e25546584603d8decb3fe84f4f278753887cfa8e00949394e686b0f64bfb04
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118193171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77eea4aa235dc181ba3d212c6f42b0477f587cae986ea50d2d75d261588a06d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:42:30 GMT
ADD file:726a32203fbcaae787c10740754e38dcb186778893e6d078db3cba0f49ee6b3c in / 
# Thu, 23 Apr 2020 20:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:42:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:42:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:42:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 11:56:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 11:57:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:58:10 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 11:59:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 11:59:14 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 11:59:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:59:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 11:59:54 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 12:12:55 GMT
ENV MARIADB_MAJOR=10.1
# Wed, 13 May 2020 21:31:40 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Wed, 13 May 2020 21:31:45 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 21:33:35 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 21:33:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:19:04 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:19:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:19:26 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:19:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:beed3bd0a281cacead564771f079ed9ee8b272a2ed0e28f533e188f3d21fee6e`  
		Last Modified: Mon, 06 Apr 2020 15:40:20 GMT  
		Size: 30.4 MB (30400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae14d2411b83450b8afe92058b998540c56ec42f1ddd7581e8e9fe629c442f89`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82678240be3a5c783512ff7336f2b10837ae126958bc6bd1b476a8d039c08771`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307ad4f24078fd763b41ec7c1772f2fd5238fed1bae36c5d42d28ec9adbffb9`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e050ed2928ca970f92a55e32757c9a2bed2d12719ac1f8ffe473007ebfb5627a`  
		Last Modified: Fri, 24 Apr 2020 12:16:35 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f165cd342f0a2ae619a609d6874d38864a5cd9a56cdfc8876d139942c86b00b`  
		Last Modified: Fri, 24 Apr 2020 12:16:39 GMT  
		Size: 5.6 MB (5628683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5783ab2db059c111e57346fcb3db7da7d24c0be81aad5b27e670d5f0d2340fd8`  
		Last Modified: Fri, 24 Apr 2020 12:16:34 GMT  
		Size: 1.2 MB (1246415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3659f23141b0ba1d73e5c6f1922b480865fa378174eccf526a7280c40ad370d2`  
		Last Modified: Fri, 24 Apr 2020 12:16:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ad047e312e9236cb8b8743456d6e073c71c56ffa4f21e1af8769ad6726c805`  
		Last Modified: Fri, 24 Apr 2020 12:16:31 GMT  
		Size: 931.5 KB (931523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22944a8e89f53e83da58e8806dc3c4be25b3a2754635c108fc327c6ddb42789b`  
		Last Modified: Fri, 24 Apr 2020 12:16:31 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac17121903157faf437d6a4f6226aedb91205bbbb4fe4716d7701dfcdede225d`  
		Last Modified: Wed, 13 May 2020 21:39:21 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a3a841d422b4bcc462480b87ddbfcb3b42dba96389f930c4b97da6ed5c0e6b`  
		Last Modified: Wed, 13 May 2020 21:40:05 GMT  
		Size: 79.9 MB (79937498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16dfdeed66ae409ce46eda9a632a3039fad2a639aa54c0edd3efa1ce8c2b2037`  
		Last Modified: Fri, 29 May 2020 00:21:33 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533d9aec94715e1d14f6608baaee3dec819d3b3900f25264fd029f31c88133b7`  
		Last Modified: Fri, 29 May 2020 00:21:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.1.45`

```console
$ docker pull mariadb@sha256:71d9a83b9ce7bccd14eeefb272037eaea38de3b71c972d77df68efb30a962ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.1.45` - linux; amd64

```console
$ docker pull mariadb@sha256:f5d667508a4e81b80e16a17e4992069cc51275f3b89f99e08d2ce977ee8309db
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113187713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad20783a626b1fe3239b83ea2bc12842cbab5929696a13c52a7e4d7f7d3c1e49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:00 GMT
ADD file:c3e6bb316dfa6b81dd4478aaa310df532883b1c0a14edeec3f63d641980c1789 in / 
# Fri, 24 Apr 2020 01:07:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 20:07:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 20:07:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:07:25 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 20:07:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 20:07:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 20:07:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:07:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 20:07:43 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 20:10:08 GMT
ENV MARIADB_MAJOR=10.1
# Wed, 13 May 2020 20:51:55 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Wed, 13 May 2020 20:51:56 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 20:52:31 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 20:52:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:21:50 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:21:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:21:51 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:23884877105a7ff84a910895cd044061a4561385ff6c36480ee080b76ec0e771`  
		Last Modified: Sat, 04 Apr 2020 12:21:10 GMT  
		Size: 26.7 MB (26689802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc38caa0f5b94141276220daaf428892096e4afd24b05668cd188311e00a635f`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 35.4 KB (35367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2910811b6c4227c2f42aaea9a3dd5f53b1d469f67e2cf7e601f631b119b61ff7`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36505266dcc64eeb1010bd2112e6f73981e1a8246e4f6d4e287763b57f101b0b`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69dcc78e96eb792fb67240a5ff4db2c3e3cb1ff55f97df2bddba0706fb5f6e6`  
		Last Modified: Fri, 24 Apr 2020 20:10:59 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222f44c5392d7a36df5eb58bb790223d332bd187fc56f006ecd66ad762f740e8`  
		Last Modified: Fri, 24 Apr 2020 20:10:59 GMT  
		Size: 4.8 MB (4807438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc64ea97b9cf087977c9a7972347db33f40487bcdd29abb41e7acf4c265335a`  
		Last Modified: Fri, 24 Apr 2020 20:10:58 GMT  
		Size: 1.3 MB (1326271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9912a149de6b3da2628c28ecfbd75992cda34df498d3634e6145bfdf1832a1a2`  
		Last Modified: Fri, 24 Apr 2020 20:10:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef6cf5b569752da3539a3b0c377a2a4f64e90f26eb7c89d405cf0168c923106`  
		Last Modified: Fri, 24 Apr 2020 20:10:57 GMT  
		Size: 929.2 KB (929212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a05be3688e04bf9961d4912e2dd86ff9832e72ec8c6b2d34c053e87ccf991a6`  
		Last Modified: Fri, 24 Apr 2020 20:10:57 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b4846a5211cc19dffa385f6714141c9e4065ea1b8272f2d1b588919011e3bd`  
		Last Modified: Wed, 13 May 2020 21:44:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c708c0ebee78df6312129e0d725d9170751f26045dadf8a29d284a923fe4aa4f`  
		Last Modified: Wed, 13 May 2020 21:44:48 GMT  
		Size: 79.4 MB (79386150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6485241d1dd9a47ea4347f8c032f9900c3fcc01b13802f80428807c69edda7a`  
		Last Modified: Fri, 29 May 2020 00:22:34 GMT  
		Size: 4.8 KB (4848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ab70faee57e501347812c3016018fdb049c752cc1352f893deecea9950b218`  
		Last Modified: Fri, 29 May 2020 00:22:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1.45` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:65d8699feaa5976ee9351a972b09a9dcd17ae3748f97da3bfe5a33bac7683fa7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.8 MB (105804343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee5218a31ee4eff81de0a40e5aa28c3a92fcb5596f2914cd718a47f0bb5b51d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 00:16:45 GMT
ADD file:bd5b3470601aa4a28132ec60a8b1c33516d09a1391864fe1dbf82a4030397fd1 in / 
# Fri, 24 Apr 2020 00:16:54 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 00:16:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:17:03 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:17:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 15:47:33 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 15:47:50 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 15:47:51 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 15:48:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 15:48:10 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 15:48:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 15:48:23 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 15:48:25 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 15:52:49 GMT
ENV MARIADB_MAJOR=10.1
# Wed, 13 May 2020 20:49:52 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Wed, 13 May 2020 20:49:54 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 20:50:57 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 20:51:00 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:41:03 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:41:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:41:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:41:06 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:41:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c2cd007b69f7e5f37c851aa689e0e617fbaa3fe3e470f714337a03e569b7f434`  
		Last Modified: Sun, 05 Apr 2020 20:25:25 GMT  
		Size: 23.7 MB (23720401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c087f8bf83d28baa9c53fc5cfb0dfc79d5062cfad77563076553b04259e822f`  
		Last Modified: Fri, 24 Apr 2020 00:21:16 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474b5c43e9a24e1958763941a17a7cac60b13460a47f2ae9067ec03ceadab33a`  
		Last Modified: Fri, 24 Apr 2020 00:21:15 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7083e6591d76b9a6c13497a6a89bfbae3e7eb2eb31bec366bec3884c8e4517ce`  
		Last Modified: Fri, 24 Apr 2020 00:21:15 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340e908aa186ab7f11f80142d1c3a5bd2f7dbec25f58366dda5f22f44e06423c`  
		Last Modified: Fri, 24 Apr 2020 15:54:13 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f46da80a1eb3c07ecc7bb3784555bd9d502290a55fe1a3fe968f7446af3128`  
		Last Modified: Fri, 24 Apr 2020 15:54:14 GMT  
		Size: 4.4 MB (4393199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9374369ce5226b7dd75e6aae1665b5dd86552811ba35823b717d507c63063a0a`  
		Last Modified: Fri, 24 Apr 2020 15:54:13 GMT  
		Size: 1.3 MB (1262945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65d1839f1c97b9a6854699dfa28e745e6e8790a326818902165e646d97e8182`  
		Last Modified: Fri, 24 Apr 2020 15:54:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ac11fc4bc1dcef89d539dcbef6f8683a59c653edbf6b6b8674aaaf8b2b8c4b`  
		Last Modified: Fri, 24 Apr 2020 15:54:12 GMT  
		Size: 920.8 KB (920766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cf075dcf71cf7ff1c9ab8fa8b58253be69db20633df6da9c5ea5cf7b48b385`  
		Last Modified: Fri, 24 Apr 2020 15:54:11 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7968e8131541efc5e72522abdd8c094b9619e86b7642f20bbfcc9522790c06f7`  
		Last Modified: Wed, 13 May 2020 20:54:02 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbff971dc2e308bfb3e161a340d655fd9e631763dea02e60558c5c89dbe4e02`  
		Last Modified: Wed, 13 May 2020 20:55:24 GMT  
		Size: 75.5 MB (75458297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860b1eacccdefb29e8077566f4c9c5c6a58890d3692fccb302fb1f451a6cfa52`  
		Last Modified: Fri, 29 May 2020 00:42:09 GMT  
		Size: 4.9 KB (4851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3202d23d7160445948175e254bd9182f9976a70221f940f94237fbf0804c43aa`  
		Last Modified: Fri, 29 May 2020 00:42:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1.45` - linux; ppc64le

```console
$ docker pull mariadb@sha256:85e25546584603d8decb3fe84f4f278753887cfa8e00949394e686b0f64bfb04
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118193171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77eea4aa235dc181ba3d212c6f42b0477f587cae986ea50d2d75d261588a06d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:42:30 GMT
ADD file:726a32203fbcaae787c10740754e38dcb186778893e6d078db3cba0f49ee6b3c in / 
# Thu, 23 Apr 2020 20:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:42:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:42:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:42:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 11:56:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 11:57:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:58:10 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 11:59:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 11:59:14 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 11:59:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:59:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 11:59:54 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 12:12:55 GMT
ENV MARIADB_MAJOR=10.1
# Wed, 13 May 2020 21:31:40 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Wed, 13 May 2020 21:31:45 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 21:33:35 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 21:33:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:19:04 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:19:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:19:26 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:19:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:beed3bd0a281cacead564771f079ed9ee8b272a2ed0e28f533e188f3d21fee6e`  
		Last Modified: Mon, 06 Apr 2020 15:40:20 GMT  
		Size: 30.4 MB (30400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae14d2411b83450b8afe92058b998540c56ec42f1ddd7581e8e9fe629c442f89`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82678240be3a5c783512ff7336f2b10837ae126958bc6bd1b476a8d039c08771`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307ad4f24078fd763b41ec7c1772f2fd5238fed1bae36c5d42d28ec9adbffb9`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e050ed2928ca970f92a55e32757c9a2bed2d12719ac1f8ffe473007ebfb5627a`  
		Last Modified: Fri, 24 Apr 2020 12:16:35 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f165cd342f0a2ae619a609d6874d38864a5cd9a56cdfc8876d139942c86b00b`  
		Last Modified: Fri, 24 Apr 2020 12:16:39 GMT  
		Size: 5.6 MB (5628683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5783ab2db059c111e57346fcb3db7da7d24c0be81aad5b27e670d5f0d2340fd8`  
		Last Modified: Fri, 24 Apr 2020 12:16:34 GMT  
		Size: 1.2 MB (1246415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3659f23141b0ba1d73e5c6f1922b480865fa378174eccf526a7280c40ad370d2`  
		Last Modified: Fri, 24 Apr 2020 12:16:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ad047e312e9236cb8b8743456d6e073c71c56ffa4f21e1af8769ad6726c805`  
		Last Modified: Fri, 24 Apr 2020 12:16:31 GMT  
		Size: 931.5 KB (931523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22944a8e89f53e83da58e8806dc3c4be25b3a2754635c108fc327c6ddb42789b`  
		Last Modified: Fri, 24 Apr 2020 12:16:31 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac17121903157faf437d6a4f6226aedb91205bbbb4fe4716d7701dfcdede225d`  
		Last Modified: Wed, 13 May 2020 21:39:21 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a3a841d422b4bcc462480b87ddbfcb3b42dba96389f930c4b97da6ed5c0e6b`  
		Last Modified: Wed, 13 May 2020 21:40:05 GMT  
		Size: 79.9 MB (79937498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16dfdeed66ae409ce46eda9a632a3039fad2a639aa54c0edd3efa1ce8c2b2037`  
		Last Modified: Fri, 29 May 2020 00:21:33 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533d9aec94715e1d14f6608baaee3dec819d3b3900f25264fd029f31c88133b7`  
		Last Modified: Fri, 29 May 2020 00:21:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.1.45-bionic`

```console
$ docker pull mariadb@sha256:71d9a83b9ce7bccd14eeefb272037eaea38de3b71c972d77df68efb30a962ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.1.45-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:f5d667508a4e81b80e16a17e4992069cc51275f3b89f99e08d2ce977ee8309db
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113187713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad20783a626b1fe3239b83ea2bc12842cbab5929696a13c52a7e4d7f7d3c1e49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:00 GMT
ADD file:c3e6bb316dfa6b81dd4478aaa310df532883b1c0a14edeec3f63d641980c1789 in / 
# Fri, 24 Apr 2020 01:07:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 20:07:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 20:07:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:07:25 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 20:07:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 20:07:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 20:07:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:07:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 20:07:43 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 20:10:08 GMT
ENV MARIADB_MAJOR=10.1
# Wed, 13 May 2020 20:51:55 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Wed, 13 May 2020 20:51:56 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 20:52:31 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 20:52:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:21:50 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:21:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:21:51 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:23884877105a7ff84a910895cd044061a4561385ff6c36480ee080b76ec0e771`  
		Last Modified: Sat, 04 Apr 2020 12:21:10 GMT  
		Size: 26.7 MB (26689802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc38caa0f5b94141276220daaf428892096e4afd24b05668cd188311e00a635f`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 35.4 KB (35367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2910811b6c4227c2f42aaea9a3dd5f53b1d469f67e2cf7e601f631b119b61ff7`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36505266dcc64eeb1010bd2112e6f73981e1a8246e4f6d4e287763b57f101b0b`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69dcc78e96eb792fb67240a5ff4db2c3e3cb1ff55f97df2bddba0706fb5f6e6`  
		Last Modified: Fri, 24 Apr 2020 20:10:59 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222f44c5392d7a36df5eb58bb790223d332bd187fc56f006ecd66ad762f740e8`  
		Last Modified: Fri, 24 Apr 2020 20:10:59 GMT  
		Size: 4.8 MB (4807438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc64ea97b9cf087977c9a7972347db33f40487bcdd29abb41e7acf4c265335a`  
		Last Modified: Fri, 24 Apr 2020 20:10:58 GMT  
		Size: 1.3 MB (1326271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9912a149de6b3da2628c28ecfbd75992cda34df498d3634e6145bfdf1832a1a2`  
		Last Modified: Fri, 24 Apr 2020 20:10:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef6cf5b569752da3539a3b0c377a2a4f64e90f26eb7c89d405cf0168c923106`  
		Last Modified: Fri, 24 Apr 2020 20:10:57 GMT  
		Size: 929.2 KB (929212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a05be3688e04bf9961d4912e2dd86ff9832e72ec8c6b2d34c053e87ccf991a6`  
		Last Modified: Fri, 24 Apr 2020 20:10:57 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b4846a5211cc19dffa385f6714141c9e4065ea1b8272f2d1b588919011e3bd`  
		Last Modified: Wed, 13 May 2020 21:44:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c708c0ebee78df6312129e0d725d9170751f26045dadf8a29d284a923fe4aa4f`  
		Last Modified: Wed, 13 May 2020 21:44:48 GMT  
		Size: 79.4 MB (79386150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6485241d1dd9a47ea4347f8c032f9900c3fcc01b13802f80428807c69edda7a`  
		Last Modified: Fri, 29 May 2020 00:22:34 GMT  
		Size: 4.8 KB (4848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ab70faee57e501347812c3016018fdb049c752cc1352f893deecea9950b218`  
		Last Modified: Fri, 29 May 2020 00:22:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1.45-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:65d8699feaa5976ee9351a972b09a9dcd17ae3748f97da3bfe5a33bac7683fa7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.8 MB (105804343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee5218a31ee4eff81de0a40e5aa28c3a92fcb5596f2914cd718a47f0bb5b51d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 00:16:45 GMT
ADD file:bd5b3470601aa4a28132ec60a8b1c33516d09a1391864fe1dbf82a4030397fd1 in / 
# Fri, 24 Apr 2020 00:16:54 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 00:16:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:17:03 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:17:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 15:47:33 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 15:47:50 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 15:47:51 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 15:48:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 15:48:10 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 15:48:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 15:48:23 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 15:48:25 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 15:52:49 GMT
ENV MARIADB_MAJOR=10.1
# Wed, 13 May 2020 20:49:52 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Wed, 13 May 2020 20:49:54 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 20:50:57 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 20:51:00 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:41:03 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:41:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:41:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:41:06 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:41:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c2cd007b69f7e5f37c851aa689e0e617fbaa3fe3e470f714337a03e569b7f434`  
		Last Modified: Sun, 05 Apr 2020 20:25:25 GMT  
		Size: 23.7 MB (23720401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c087f8bf83d28baa9c53fc5cfb0dfc79d5062cfad77563076553b04259e822f`  
		Last Modified: Fri, 24 Apr 2020 00:21:16 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474b5c43e9a24e1958763941a17a7cac60b13460a47f2ae9067ec03ceadab33a`  
		Last Modified: Fri, 24 Apr 2020 00:21:15 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7083e6591d76b9a6c13497a6a89bfbae3e7eb2eb31bec366bec3884c8e4517ce`  
		Last Modified: Fri, 24 Apr 2020 00:21:15 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340e908aa186ab7f11f80142d1c3a5bd2f7dbec25f58366dda5f22f44e06423c`  
		Last Modified: Fri, 24 Apr 2020 15:54:13 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f46da80a1eb3c07ecc7bb3784555bd9d502290a55fe1a3fe968f7446af3128`  
		Last Modified: Fri, 24 Apr 2020 15:54:14 GMT  
		Size: 4.4 MB (4393199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9374369ce5226b7dd75e6aae1665b5dd86552811ba35823b717d507c63063a0a`  
		Last Modified: Fri, 24 Apr 2020 15:54:13 GMT  
		Size: 1.3 MB (1262945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65d1839f1c97b9a6854699dfa28e745e6e8790a326818902165e646d97e8182`  
		Last Modified: Fri, 24 Apr 2020 15:54:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ac11fc4bc1dcef89d539dcbef6f8683a59c653edbf6b6b8674aaaf8b2b8c4b`  
		Last Modified: Fri, 24 Apr 2020 15:54:12 GMT  
		Size: 920.8 KB (920766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cf075dcf71cf7ff1c9ab8fa8b58253be69db20633df6da9c5ea5cf7b48b385`  
		Last Modified: Fri, 24 Apr 2020 15:54:11 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7968e8131541efc5e72522abdd8c094b9619e86b7642f20bbfcc9522790c06f7`  
		Last Modified: Wed, 13 May 2020 20:54:02 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbff971dc2e308bfb3e161a340d655fd9e631763dea02e60558c5c89dbe4e02`  
		Last Modified: Wed, 13 May 2020 20:55:24 GMT  
		Size: 75.5 MB (75458297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860b1eacccdefb29e8077566f4c9c5c6a58890d3692fccb302fb1f451a6cfa52`  
		Last Modified: Fri, 29 May 2020 00:42:09 GMT  
		Size: 4.9 KB (4851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3202d23d7160445948175e254bd9182f9976a70221f940f94237fbf0804c43aa`  
		Last Modified: Fri, 29 May 2020 00:42:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1.45-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:85e25546584603d8decb3fe84f4f278753887cfa8e00949394e686b0f64bfb04
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118193171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77eea4aa235dc181ba3d212c6f42b0477f587cae986ea50d2d75d261588a06d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:42:30 GMT
ADD file:726a32203fbcaae787c10740754e38dcb186778893e6d078db3cba0f49ee6b3c in / 
# Thu, 23 Apr 2020 20:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:42:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:42:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:42:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 11:56:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 11:57:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:58:10 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 11:59:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 11:59:14 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 11:59:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:59:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 11:59:54 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 12:12:55 GMT
ENV MARIADB_MAJOR=10.1
# Wed, 13 May 2020 21:31:40 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Wed, 13 May 2020 21:31:45 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 21:33:35 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 21:33:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:19:04 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:19:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:19:26 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:19:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:beed3bd0a281cacead564771f079ed9ee8b272a2ed0e28f533e188f3d21fee6e`  
		Last Modified: Mon, 06 Apr 2020 15:40:20 GMT  
		Size: 30.4 MB (30400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae14d2411b83450b8afe92058b998540c56ec42f1ddd7581e8e9fe629c442f89`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82678240be3a5c783512ff7336f2b10837ae126958bc6bd1b476a8d039c08771`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307ad4f24078fd763b41ec7c1772f2fd5238fed1bae36c5d42d28ec9adbffb9`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e050ed2928ca970f92a55e32757c9a2bed2d12719ac1f8ffe473007ebfb5627a`  
		Last Modified: Fri, 24 Apr 2020 12:16:35 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f165cd342f0a2ae619a609d6874d38864a5cd9a56cdfc8876d139942c86b00b`  
		Last Modified: Fri, 24 Apr 2020 12:16:39 GMT  
		Size: 5.6 MB (5628683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5783ab2db059c111e57346fcb3db7da7d24c0be81aad5b27e670d5f0d2340fd8`  
		Last Modified: Fri, 24 Apr 2020 12:16:34 GMT  
		Size: 1.2 MB (1246415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3659f23141b0ba1d73e5c6f1922b480865fa378174eccf526a7280c40ad370d2`  
		Last Modified: Fri, 24 Apr 2020 12:16:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ad047e312e9236cb8b8743456d6e073c71c56ffa4f21e1af8769ad6726c805`  
		Last Modified: Fri, 24 Apr 2020 12:16:31 GMT  
		Size: 931.5 KB (931523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22944a8e89f53e83da58e8806dc3c4be25b3a2754635c108fc327c6ddb42789b`  
		Last Modified: Fri, 24 Apr 2020 12:16:31 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac17121903157faf437d6a4f6226aedb91205bbbb4fe4716d7701dfcdede225d`  
		Last Modified: Wed, 13 May 2020 21:39:21 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a3a841d422b4bcc462480b87ddbfcb3b42dba96389f930c4b97da6ed5c0e6b`  
		Last Modified: Wed, 13 May 2020 21:40:05 GMT  
		Size: 79.9 MB (79937498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16dfdeed66ae409ce46eda9a632a3039fad2a639aa54c0edd3efa1ce8c2b2037`  
		Last Modified: Fri, 29 May 2020 00:21:33 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533d9aec94715e1d14f6608baaee3dec819d3b3900f25264fd029f31c88133b7`  
		Last Modified: Fri, 29 May 2020 00:21:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.1-bionic`

```console
$ docker pull mariadb@sha256:71d9a83b9ce7bccd14eeefb272037eaea38de3b71c972d77df68efb30a962ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.1-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:f5d667508a4e81b80e16a17e4992069cc51275f3b89f99e08d2ce977ee8309db
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113187713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad20783a626b1fe3239b83ea2bc12842cbab5929696a13c52a7e4d7f7d3c1e49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:00 GMT
ADD file:c3e6bb316dfa6b81dd4478aaa310df532883b1c0a14edeec3f63d641980c1789 in / 
# Fri, 24 Apr 2020 01:07:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 20:07:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 20:07:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:07:25 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 20:07:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 20:07:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 20:07:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:07:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 20:07:43 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 20:10:08 GMT
ENV MARIADB_MAJOR=10.1
# Wed, 13 May 2020 20:51:55 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Wed, 13 May 2020 20:51:56 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 20:52:31 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 20:52:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:21:50 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:21:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:21:51 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:23884877105a7ff84a910895cd044061a4561385ff6c36480ee080b76ec0e771`  
		Last Modified: Sat, 04 Apr 2020 12:21:10 GMT  
		Size: 26.7 MB (26689802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc38caa0f5b94141276220daaf428892096e4afd24b05668cd188311e00a635f`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 35.4 KB (35367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2910811b6c4227c2f42aaea9a3dd5f53b1d469f67e2cf7e601f631b119b61ff7`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36505266dcc64eeb1010bd2112e6f73981e1a8246e4f6d4e287763b57f101b0b`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69dcc78e96eb792fb67240a5ff4db2c3e3cb1ff55f97df2bddba0706fb5f6e6`  
		Last Modified: Fri, 24 Apr 2020 20:10:59 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222f44c5392d7a36df5eb58bb790223d332bd187fc56f006ecd66ad762f740e8`  
		Last Modified: Fri, 24 Apr 2020 20:10:59 GMT  
		Size: 4.8 MB (4807438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc64ea97b9cf087977c9a7972347db33f40487bcdd29abb41e7acf4c265335a`  
		Last Modified: Fri, 24 Apr 2020 20:10:58 GMT  
		Size: 1.3 MB (1326271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9912a149de6b3da2628c28ecfbd75992cda34df498d3634e6145bfdf1832a1a2`  
		Last Modified: Fri, 24 Apr 2020 20:10:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef6cf5b569752da3539a3b0c377a2a4f64e90f26eb7c89d405cf0168c923106`  
		Last Modified: Fri, 24 Apr 2020 20:10:57 GMT  
		Size: 929.2 KB (929212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a05be3688e04bf9961d4912e2dd86ff9832e72ec8c6b2d34c053e87ccf991a6`  
		Last Modified: Fri, 24 Apr 2020 20:10:57 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b4846a5211cc19dffa385f6714141c9e4065ea1b8272f2d1b588919011e3bd`  
		Last Modified: Wed, 13 May 2020 21:44:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c708c0ebee78df6312129e0d725d9170751f26045dadf8a29d284a923fe4aa4f`  
		Last Modified: Wed, 13 May 2020 21:44:48 GMT  
		Size: 79.4 MB (79386150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6485241d1dd9a47ea4347f8c032f9900c3fcc01b13802f80428807c69edda7a`  
		Last Modified: Fri, 29 May 2020 00:22:34 GMT  
		Size: 4.8 KB (4848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ab70faee57e501347812c3016018fdb049c752cc1352f893deecea9950b218`  
		Last Modified: Fri, 29 May 2020 00:22:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:65d8699feaa5976ee9351a972b09a9dcd17ae3748f97da3bfe5a33bac7683fa7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.8 MB (105804343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee5218a31ee4eff81de0a40e5aa28c3a92fcb5596f2914cd718a47f0bb5b51d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 00:16:45 GMT
ADD file:bd5b3470601aa4a28132ec60a8b1c33516d09a1391864fe1dbf82a4030397fd1 in / 
# Fri, 24 Apr 2020 00:16:54 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 00:16:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:17:03 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:17:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 15:47:33 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 15:47:50 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 15:47:51 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 15:48:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 15:48:10 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 15:48:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 15:48:23 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 15:48:25 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 15:52:49 GMT
ENV MARIADB_MAJOR=10.1
# Wed, 13 May 2020 20:49:52 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Wed, 13 May 2020 20:49:54 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 20:50:57 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 20:51:00 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:41:03 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:41:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:41:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:41:06 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:41:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c2cd007b69f7e5f37c851aa689e0e617fbaa3fe3e470f714337a03e569b7f434`  
		Last Modified: Sun, 05 Apr 2020 20:25:25 GMT  
		Size: 23.7 MB (23720401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c087f8bf83d28baa9c53fc5cfb0dfc79d5062cfad77563076553b04259e822f`  
		Last Modified: Fri, 24 Apr 2020 00:21:16 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474b5c43e9a24e1958763941a17a7cac60b13460a47f2ae9067ec03ceadab33a`  
		Last Modified: Fri, 24 Apr 2020 00:21:15 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7083e6591d76b9a6c13497a6a89bfbae3e7eb2eb31bec366bec3884c8e4517ce`  
		Last Modified: Fri, 24 Apr 2020 00:21:15 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340e908aa186ab7f11f80142d1c3a5bd2f7dbec25f58366dda5f22f44e06423c`  
		Last Modified: Fri, 24 Apr 2020 15:54:13 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f46da80a1eb3c07ecc7bb3784555bd9d502290a55fe1a3fe968f7446af3128`  
		Last Modified: Fri, 24 Apr 2020 15:54:14 GMT  
		Size: 4.4 MB (4393199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9374369ce5226b7dd75e6aae1665b5dd86552811ba35823b717d507c63063a0a`  
		Last Modified: Fri, 24 Apr 2020 15:54:13 GMT  
		Size: 1.3 MB (1262945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65d1839f1c97b9a6854699dfa28e745e6e8790a326818902165e646d97e8182`  
		Last Modified: Fri, 24 Apr 2020 15:54:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ac11fc4bc1dcef89d539dcbef6f8683a59c653edbf6b6b8674aaaf8b2b8c4b`  
		Last Modified: Fri, 24 Apr 2020 15:54:12 GMT  
		Size: 920.8 KB (920766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cf075dcf71cf7ff1c9ab8fa8b58253be69db20633df6da9c5ea5cf7b48b385`  
		Last Modified: Fri, 24 Apr 2020 15:54:11 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7968e8131541efc5e72522abdd8c094b9619e86b7642f20bbfcc9522790c06f7`  
		Last Modified: Wed, 13 May 2020 20:54:02 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbff971dc2e308bfb3e161a340d655fd9e631763dea02e60558c5c89dbe4e02`  
		Last Modified: Wed, 13 May 2020 20:55:24 GMT  
		Size: 75.5 MB (75458297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860b1eacccdefb29e8077566f4c9c5c6a58890d3692fccb302fb1f451a6cfa52`  
		Last Modified: Fri, 29 May 2020 00:42:09 GMT  
		Size: 4.9 KB (4851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3202d23d7160445948175e254bd9182f9976a70221f940f94237fbf0804c43aa`  
		Last Modified: Fri, 29 May 2020 00:42:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:85e25546584603d8decb3fe84f4f278753887cfa8e00949394e686b0f64bfb04
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118193171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77eea4aa235dc181ba3d212c6f42b0477f587cae986ea50d2d75d261588a06d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:42:30 GMT
ADD file:726a32203fbcaae787c10740754e38dcb186778893e6d078db3cba0f49ee6b3c in / 
# Thu, 23 Apr 2020 20:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:42:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:42:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:42:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 11:56:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 11:57:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:58:10 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 11:59:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 11:59:14 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 11:59:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:59:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 11:59:54 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 12:12:55 GMT
ENV MARIADB_MAJOR=10.1
# Wed, 13 May 2020 21:31:40 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Wed, 13 May 2020 21:31:45 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 21:33:35 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 21:33:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:19:04 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:19:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:19:26 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:19:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:beed3bd0a281cacead564771f079ed9ee8b272a2ed0e28f533e188f3d21fee6e`  
		Last Modified: Mon, 06 Apr 2020 15:40:20 GMT  
		Size: 30.4 MB (30400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae14d2411b83450b8afe92058b998540c56ec42f1ddd7581e8e9fe629c442f89`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82678240be3a5c783512ff7336f2b10837ae126958bc6bd1b476a8d039c08771`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307ad4f24078fd763b41ec7c1772f2fd5238fed1bae36c5d42d28ec9adbffb9`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e050ed2928ca970f92a55e32757c9a2bed2d12719ac1f8ffe473007ebfb5627a`  
		Last Modified: Fri, 24 Apr 2020 12:16:35 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f165cd342f0a2ae619a609d6874d38864a5cd9a56cdfc8876d139942c86b00b`  
		Last Modified: Fri, 24 Apr 2020 12:16:39 GMT  
		Size: 5.6 MB (5628683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5783ab2db059c111e57346fcb3db7da7d24c0be81aad5b27e670d5f0d2340fd8`  
		Last Modified: Fri, 24 Apr 2020 12:16:34 GMT  
		Size: 1.2 MB (1246415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3659f23141b0ba1d73e5c6f1922b480865fa378174eccf526a7280c40ad370d2`  
		Last Modified: Fri, 24 Apr 2020 12:16:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ad047e312e9236cb8b8743456d6e073c71c56ffa4f21e1af8769ad6726c805`  
		Last Modified: Fri, 24 Apr 2020 12:16:31 GMT  
		Size: 931.5 KB (931523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22944a8e89f53e83da58e8806dc3c4be25b3a2754635c108fc327c6ddb42789b`  
		Last Modified: Fri, 24 Apr 2020 12:16:31 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac17121903157faf437d6a4f6226aedb91205bbbb4fe4716d7701dfcdede225d`  
		Last Modified: Wed, 13 May 2020 21:39:21 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a3a841d422b4bcc462480b87ddbfcb3b42dba96389f930c4b97da6ed5c0e6b`  
		Last Modified: Wed, 13 May 2020 21:40:05 GMT  
		Size: 79.9 MB (79937498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16dfdeed66ae409ce46eda9a632a3039fad2a639aa54c0edd3efa1ce8c2b2037`  
		Last Modified: Fri, 29 May 2020 00:21:33 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533d9aec94715e1d14f6608baaee3dec819d3b3900f25264fd029f31c88133b7`  
		Last Modified: Fri, 29 May 2020 00:21:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2`

```console
$ docker pull mariadb@sha256:ddff0c0d1a84d07af72f3e8e78f03452ef90b758843e004ffdce528aa0b11928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2` - linux; amd64

```console
$ docker pull mariadb@sha256:eb1f6c4a4a01985d20283423421817c1a201e85de1192c6bed681dfee3664af3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (108996232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a144d514f6729156a6491a1806310f5e2d93042b24d921d8ba4bca7fc5e979c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:00 GMT
ADD file:c3e6bb316dfa6b81dd4478aaa310df532883b1c0a14edeec3f63d641980c1789 in / 
# Fri, 24 Apr 2020 01:07:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 20:07:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 20:07:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:07:25 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 20:07:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 20:07:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 20:07:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:07:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 20:07:43 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 20:09:29 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 13 May 2020 20:51:21 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Wed, 13 May 2020 20:51:22 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 20:51:47 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 20:51:47 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:21:44 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:21:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:21:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:21:46 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:21:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:23884877105a7ff84a910895cd044061a4561385ff6c36480ee080b76ec0e771`  
		Last Modified: Sat, 04 Apr 2020 12:21:10 GMT  
		Size: 26.7 MB (26689802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc38caa0f5b94141276220daaf428892096e4afd24b05668cd188311e00a635f`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 35.4 KB (35367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2910811b6c4227c2f42aaea9a3dd5f53b1d469f67e2cf7e601f631b119b61ff7`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36505266dcc64eeb1010bd2112e6f73981e1a8246e4f6d4e287763b57f101b0b`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69dcc78e96eb792fb67240a5ff4db2c3e3cb1ff55f97df2bddba0706fb5f6e6`  
		Last Modified: Fri, 24 Apr 2020 20:10:59 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222f44c5392d7a36df5eb58bb790223d332bd187fc56f006ecd66ad762f740e8`  
		Last Modified: Fri, 24 Apr 2020 20:10:59 GMT  
		Size: 4.8 MB (4807438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc64ea97b9cf087977c9a7972347db33f40487bcdd29abb41e7acf4c265335a`  
		Last Modified: Fri, 24 Apr 2020 20:10:58 GMT  
		Size: 1.3 MB (1326271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9912a149de6b3da2628c28ecfbd75992cda34df498d3634e6145bfdf1832a1a2`  
		Last Modified: Fri, 24 Apr 2020 20:10:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef6cf5b569752da3539a3b0c377a2a4f64e90f26eb7c89d405cf0168c923106`  
		Last Modified: Fri, 24 Apr 2020 20:10:57 GMT  
		Size: 929.2 KB (929212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a05be3688e04bf9961d4912e2dd86ff9832e72ec8c6b2d34c053e87ccf991a6`  
		Last Modified: Fri, 24 Apr 2020 20:10:57 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a1edf2a8459b3c38e04a5cdabd6030f22e09bb2f653d0e57020e1e77b530ea`  
		Last Modified: Wed, 13 May 2020 21:44:09 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4954c91ebe442c8d5c4bbcfb190d71bc2adc03debcf88573e9d55e9abaf0e9`  
		Last Modified: Wed, 13 May 2020 21:44:25 GMT  
		Size: 75.2 MB (75194669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae91c8217271570b6c43609f856cee367ae34cf2106fb9a589bc7698e52ba11`  
		Last Modified: Fri, 29 May 2020 00:22:25 GMT  
		Size: 4.8 KB (4846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ec0680735c5ff37d37fa985b1970c8fa5d17887fb1d8f72e9cdb6310e8f20a`  
		Last Modified: Fri, 29 May 2020 00:22:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:9449e7cd6f24e5f05d9ed73ca0d7b91e08f01cb543e53c07ea26492c8193c1b5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104077523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21aeeecb24c278756509b9b729346302aa2e6394c0e8cff15b0eeddf20d7ae56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 00:16:45 GMT
ADD file:bd5b3470601aa4a28132ec60a8b1c33516d09a1391864fe1dbf82a4030397fd1 in / 
# Fri, 24 Apr 2020 00:16:54 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 00:16:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:17:03 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:17:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 15:47:33 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 15:47:50 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 15:47:51 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 15:48:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 15:48:10 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 15:48:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 15:48:23 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 15:48:25 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 15:51:52 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 13 May 2020 20:47:48 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Wed, 13 May 2020 20:47:51 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 20:48:56 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 20:49:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:40:51 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:40:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:40:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:40:55 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:40:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c2cd007b69f7e5f37c851aa689e0e617fbaa3fe3e470f714337a03e569b7f434`  
		Last Modified: Sun, 05 Apr 2020 20:25:25 GMT  
		Size: 23.7 MB (23720401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c087f8bf83d28baa9c53fc5cfb0dfc79d5062cfad77563076553b04259e822f`  
		Last Modified: Fri, 24 Apr 2020 00:21:16 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474b5c43e9a24e1958763941a17a7cac60b13460a47f2ae9067ec03ceadab33a`  
		Last Modified: Fri, 24 Apr 2020 00:21:15 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7083e6591d76b9a6c13497a6a89bfbae3e7eb2eb31bec366bec3884c8e4517ce`  
		Last Modified: Fri, 24 Apr 2020 00:21:15 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340e908aa186ab7f11f80142d1c3a5bd2f7dbec25f58366dda5f22f44e06423c`  
		Last Modified: Fri, 24 Apr 2020 15:54:13 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f46da80a1eb3c07ecc7bb3784555bd9d502290a55fe1a3fe968f7446af3128`  
		Last Modified: Fri, 24 Apr 2020 15:54:14 GMT  
		Size: 4.4 MB (4393199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9374369ce5226b7dd75e6aae1665b5dd86552811ba35823b717d507c63063a0a`  
		Last Modified: Fri, 24 Apr 2020 15:54:13 GMT  
		Size: 1.3 MB (1262945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65d1839f1c97b9a6854699dfa28e745e6e8790a326818902165e646d97e8182`  
		Last Modified: Fri, 24 Apr 2020 15:54:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ac11fc4bc1dcef89d539dcbef6f8683a59c653edbf6b6b8674aaaf8b2b8c4b`  
		Last Modified: Fri, 24 Apr 2020 15:54:12 GMT  
		Size: 920.8 KB (920766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cf075dcf71cf7ff1c9ab8fa8b58253be69db20633df6da9c5ea5cf7b48b385`  
		Last Modified: Fri, 24 Apr 2020 15:54:11 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fba07a52f8c704b1aa302b5ca0154248b0d53474b9390afaa8de78e0ba3184`  
		Last Modified: Wed, 13 May 2020 20:53:29 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1442a0493fb5d092510edc3fafc58adb80c8ef3967ab64a8eeff4c9503f225e8`  
		Last Modified: Wed, 13 May 2020 20:53:52 GMT  
		Size: 73.7 MB (73731474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37eb11d1cd80a2cd32017f4726ba043ee47136d9476079d56dfe1429a21951b`  
		Last Modified: Fri, 29 May 2020 00:42:01 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25526a0ca962ab63af8cc7be2e24000fe22c4417b289c4eff1110e2fd672f628`  
		Last Modified: Fri, 29 May 2020 00:42:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2` - linux; ppc64le

```console
$ docker pull mariadb@sha256:5c36761b92100924e7ac536939ac4137c013ae05b8cdeee7b462a956d7bc80cb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116238898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93cecc321cebccae35ecb8359bb9daea184ed336e8226b517019f2218f1f9dd8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:42:30 GMT
ADD file:726a32203fbcaae787c10740754e38dcb186778893e6d078db3cba0f49ee6b3c in / 
# Thu, 23 Apr 2020 20:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:42:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:42:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:42:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 11:56:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 11:57:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:58:10 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 11:59:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 11:59:14 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 11:59:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:59:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 11:59:54 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 12:09:45 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 13 May 2020 21:29:28 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Wed, 13 May 2020 21:29:36 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 21:31:04 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 21:31:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:18:34 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:18:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:18:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:18:49 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:beed3bd0a281cacead564771f079ed9ee8b272a2ed0e28f533e188f3d21fee6e`  
		Last Modified: Mon, 06 Apr 2020 15:40:20 GMT  
		Size: 30.4 MB (30400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae14d2411b83450b8afe92058b998540c56ec42f1ddd7581e8e9fe629c442f89`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82678240be3a5c783512ff7336f2b10837ae126958bc6bd1b476a8d039c08771`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307ad4f24078fd763b41ec7c1772f2fd5238fed1bae36c5d42d28ec9adbffb9`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e050ed2928ca970f92a55e32757c9a2bed2d12719ac1f8ffe473007ebfb5627a`  
		Last Modified: Fri, 24 Apr 2020 12:16:35 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f165cd342f0a2ae619a609d6874d38864a5cd9a56cdfc8876d139942c86b00b`  
		Last Modified: Fri, 24 Apr 2020 12:16:39 GMT  
		Size: 5.6 MB (5628683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5783ab2db059c111e57346fcb3db7da7d24c0be81aad5b27e670d5f0d2340fd8`  
		Last Modified: Fri, 24 Apr 2020 12:16:34 GMT  
		Size: 1.2 MB (1246415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3659f23141b0ba1d73e5c6f1922b480865fa378174eccf526a7280c40ad370d2`  
		Last Modified: Fri, 24 Apr 2020 12:16:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ad047e312e9236cb8b8743456d6e073c71c56ffa4f21e1af8769ad6726c805`  
		Last Modified: Fri, 24 Apr 2020 12:16:31 GMT  
		Size: 931.5 KB (931523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22944a8e89f53e83da58e8806dc3c4be25b3a2754635c108fc327c6ddb42789b`  
		Last Modified: Fri, 24 Apr 2020 12:16:31 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dfeebe25cc02ad3288ff3f03a92be19ef8664c7907b436859177684da5e508`  
		Last Modified: Wed, 13 May 2020 21:38:23 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145af634d57422884d13c0715874a0329aa049813e46d8a3ebace3333d997f67`  
		Last Modified: Wed, 13 May 2020 21:39:02 GMT  
		Size: 78.0 MB (77983227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a739aee0daaa14a73304a5a190b76705b8b2a5a6a3ff501b4b983bbcc2926f4`  
		Last Modified: Fri, 29 May 2020 00:21:16 GMT  
		Size: 4.8 KB (4849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c100b735d3acd167ca7325abc2eecd2cb3e3753090746bc73aada056882ff2b1`  
		Last Modified: Fri, 29 May 2020 00:21:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.32`

```console
$ docker pull mariadb@sha256:ddff0c0d1a84d07af72f3e8e78f03452ef90b758843e004ffdce528aa0b11928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2.32` - linux; amd64

```console
$ docker pull mariadb@sha256:eb1f6c4a4a01985d20283423421817c1a201e85de1192c6bed681dfee3664af3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (108996232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a144d514f6729156a6491a1806310f5e2d93042b24d921d8ba4bca7fc5e979c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:00 GMT
ADD file:c3e6bb316dfa6b81dd4478aaa310df532883b1c0a14edeec3f63d641980c1789 in / 
# Fri, 24 Apr 2020 01:07:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 20:07:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 20:07:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:07:25 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 20:07:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 20:07:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 20:07:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:07:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 20:07:43 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 20:09:29 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 13 May 2020 20:51:21 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Wed, 13 May 2020 20:51:22 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 20:51:47 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 20:51:47 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:21:44 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:21:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:21:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:21:46 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:21:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:23884877105a7ff84a910895cd044061a4561385ff6c36480ee080b76ec0e771`  
		Last Modified: Sat, 04 Apr 2020 12:21:10 GMT  
		Size: 26.7 MB (26689802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc38caa0f5b94141276220daaf428892096e4afd24b05668cd188311e00a635f`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 35.4 KB (35367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2910811b6c4227c2f42aaea9a3dd5f53b1d469f67e2cf7e601f631b119b61ff7`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36505266dcc64eeb1010bd2112e6f73981e1a8246e4f6d4e287763b57f101b0b`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69dcc78e96eb792fb67240a5ff4db2c3e3cb1ff55f97df2bddba0706fb5f6e6`  
		Last Modified: Fri, 24 Apr 2020 20:10:59 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222f44c5392d7a36df5eb58bb790223d332bd187fc56f006ecd66ad762f740e8`  
		Last Modified: Fri, 24 Apr 2020 20:10:59 GMT  
		Size: 4.8 MB (4807438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc64ea97b9cf087977c9a7972347db33f40487bcdd29abb41e7acf4c265335a`  
		Last Modified: Fri, 24 Apr 2020 20:10:58 GMT  
		Size: 1.3 MB (1326271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9912a149de6b3da2628c28ecfbd75992cda34df498d3634e6145bfdf1832a1a2`  
		Last Modified: Fri, 24 Apr 2020 20:10:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef6cf5b569752da3539a3b0c377a2a4f64e90f26eb7c89d405cf0168c923106`  
		Last Modified: Fri, 24 Apr 2020 20:10:57 GMT  
		Size: 929.2 KB (929212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a05be3688e04bf9961d4912e2dd86ff9832e72ec8c6b2d34c053e87ccf991a6`  
		Last Modified: Fri, 24 Apr 2020 20:10:57 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a1edf2a8459b3c38e04a5cdabd6030f22e09bb2f653d0e57020e1e77b530ea`  
		Last Modified: Wed, 13 May 2020 21:44:09 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4954c91ebe442c8d5c4bbcfb190d71bc2adc03debcf88573e9d55e9abaf0e9`  
		Last Modified: Wed, 13 May 2020 21:44:25 GMT  
		Size: 75.2 MB (75194669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae91c8217271570b6c43609f856cee367ae34cf2106fb9a589bc7698e52ba11`  
		Last Modified: Fri, 29 May 2020 00:22:25 GMT  
		Size: 4.8 KB (4846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ec0680735c5ff37d37fa985b1970c8fa5d17887fb1d8f72e9cdb6310e8f20a`  
		Last Modified: Fri, 29 May 2020 00:22:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.32` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:9449e7cd6f24e5f05d9ed73ca0d7b91e08f01cb543e53c07ea26492c8193c1b5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104077523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21aeeecb24c278756509b9b729346302aa2e6394c0e8cff15b0eeddf20d7ae56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 00:16:45 GMT
ADD file:bd5b3470601aa4a28132ec60a8b1c33516d09a1391864fe1dbf82a4030397fd1 in / 
# Fri, 24 Apr 2020 00:16:54 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 00:16:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:17:03 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:17:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 15:47:33 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 15:47:50 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 15:47:51 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 15:48:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 15:48:10 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 15:48:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 15:48:23 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 15:48:25 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 15:51:52 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 13 May 2020 20:47:48 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Wed, 13 May 2020 20:47:51 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 20:48:56 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 20:49:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:40:51 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:40:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:40:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:40:55 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:40:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c2cd007b69f7e5f37c851aa689e0e617fbaa3fe3e470f714337a03e569b7f434`  
		Last Modified: Sun, 05 Apr 2020 20:25:25 GMT  
		Size: 23.7 MB (23720401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c087f8bf83d28baa9c53fc5cfb0dfc79d5062cfad77563076553b04259e822f`  
		Last Modified: Fri, 24 Apr 2020 00:21:16 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474b5c43e9a24e1958763941a17a7cac60b13460a47f2ae9067ec03ceadab33a`  
		Last Modified: Fri, 24 Apr 2020 00:21:15 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7083e6591d76b9a6c13497a6a89bfbae3e7eb2eb31bec366bec3884c8e4517ce`  
		Last Modified: Fri, 24 Apr 2020 00:21:15 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340e908aa186ab7f11f80142d1c3a5bd2f7dbec25f58366dda5f22f44e06423c`  
		Last Modified: Fri, 24 Apr 2020 15:54:13 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f46da80a1eb3c07ecc7bb3784555bd9d502290a55fe1a3fe968f7446af3128`  
		Last Modified: Fri, 24 Apr 2020 15:54:14 GMT  
		Size: 4.4 MB (4393199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9374369ce5226b7dd75e6aae1665b5dd86552811ba35823b717d507c63063a0a`  
		Last Modified: Fri, 24 Apr 2020 15:54:13 GMT  
		Size: 1.3 MB (1262945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65d1839f1c97b9a6854699dfa28e745e6e8790a326818902165e646d97e8182`  
		Last Modified: Fri, 24 Apr 2020 15:54:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ac11fc4bc1dcef89d539dcbef6f8683a59c653edbf6b6b8674aaaf8b2b8c4b`  
		Last Modified: Fri, 24 Apr 2020 15:54:12 GMT  
		Size: 920.8 KB (920766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cf075dcf71cf7ff1c9ab8fa8b58253be69db20633df6da9c5ea5cf7b48b385`  
		Last Modified: Fri, 24 Apr 2020 15:54:11 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fba07a52f8c704b1aa302b5ca0154248b0d53474b9390afaa8de78e0ba3184`  
		Last Modified: Wed, 13 May 2020 20:53:29 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1442a0493fb5d092510edc3fafc58adb80c8ef3967ab64a8eeff4c9503f225e8`  
		Last Modified: Wed, 13 May 2020 20:53:52 GMT  
		Size: 73.7 MB (73731474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37eb11d1cd80a2cd32017f4726ba043ee47136d9476079d56dfe1429a21951b`  
		Last Modified: Fri, 29 May 2020 00:42:01 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25526a0ca962ab63af8cc7be2e24000fe22c4417b289c4eff1110e2fd672f628`  
		Last Modified: Fri, 29 May 2020 00:42:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.32` - linux; ppc64le

```console
$ docker pull mariadb@sha256:5c36761b92100924e7ac536939ac4137c013ae05b8cdeee7b462a956d7bc80cb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116238898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93cecc321cebccae35ecb8359bb9daea184ed336e8226b517019f2218f1f9dd8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:42:30 GMT
ADD file:726a32203fbcaae787c10740754e38dcb186778893e6d078db3cba0f49ee6b3c in / 
# Thu, 23 Apr 2020 20:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:42:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:42:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:42:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 11:56:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 11:57:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:58:10 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 11:59:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 11:59:14 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 11:59:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:59:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 11:59:54 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 12:09:45 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 13 May 2020 21:29:28 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Wed, 13 May 2020 21:29:36 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 21:31:04 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 21:31:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:18:34 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:18:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:18:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:18:49 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:beed3bd0a281cacead564771f079ed9ee8b272a2ed0e28f533e188f3d21fee6e`  
		Last Modified: Mon, 06 Apr 2020 15:40:20 GMT  
		Size: 30.4 MB (30400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae14d2411b83450b8afe92058b998540c56ec42f1ddd7581e8e9fe629c442f89`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82678240be3a5c783512ff7336f2b10837ae126958bc6bd1b476a8d039c08771`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307ad4f24078fd763b41ec7c1772f2fd5238fed1bae36c5d42d28ec9adbffb9`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e050ed2928ca970f92a55e32757c9a2bed2d12719ac1f8ffe473007ebfb5627a`  
		Last Modified: Fri, 24 Apr 2020 12:16:35 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f165cd342f0a2ae619a609d6874d38864a5cd9a56cdfc8876d139942c86b00b`  
		Last Modified: Fri, 24 Apr 2020 12:16:39 GMT  
		Size: 5.6 MB (5628683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5783ab2db059c111e57346fcb3db7da7d24c0be81aad5b27e670d5f0d2340fd8`  
		Last Modified: Fri, 24 Apr 2020 12:16:34 GMT  
		Size: 1.2 MB (1246415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3659f23141b0ba1d73e5c6f1922b480865fa378174eccf526a7280c40ad370d2`  
		Last Modified: Fri, 24 Apr 2020 12:16:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ad047e312e9236cb8b8743456d6e073c71c56ffa4f21e1af8769ad6726c805`  
		Last Modified: Fri, 24 Apr 2020 12:16:31 GMT  
		Size: 931.5 KB (931523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22944a8e89f53e83da58e8806dc3c4be25b3a2754635c108fc327c6ddb42789b`  
		Last Modified: Fri, 24 Apr 2020 12:16:31 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dfeebe25cc02ad3288ff3f03a92be19ef8664c7907b436859177684da5e508`  
		Last Modified: Wed, 13 May 2020 21:38:23 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145af634d57422884d13c0715874a0329aa049813e46d8a3ebace3333d997f67`  
		Last Modified: Wed, 13 May 2020 21:39:02 GMT  
		Size: 78.0 MB (77983227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a739aee0daaa14a73304a5a190b76705b8b2a5a6a3ff501b4b983bbcc2926f4`  
		Last Modified: Fri, 29 May 2020 00:21:16 GMT  
		Size: 4.8 KB (4849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c100b735d3acd167ca7325abc2eecd2cb3e3753090746bc73aada056882ff2b1`  
		Last Modified: Fri, 29 May 2020 00:21:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.32-bionic`

```console
$ docker pull mariadb@sha256:ddff0c0d1a84d07af72f3e8e78f03452ef90b758843e004ffdce528aa0b11928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2.32-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:eb1f6c4a4a01985d20283423421817c1a201e85de1192c6bed681dfee3664af3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (108996232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a144d514f6729156a6491a1806310f5e2d93042b24d921d8ba4bca7fc5e979c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:00 GMT
ADD file:c3e6bb316dfa6b81dd4478aaa310df532883b1c0a14edeec3f63d641980c1789 in / 
# Fri, 24 Apr 2020 01:07:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 20:07:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 20:07:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:07:25 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 20:07:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 20:07:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 20:07:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:07:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 20:07:43 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 20:09:29 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 13 May 2020 20:51:21 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Wed, 13 May 2020 20:51:22 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 20:51:47 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 20:51:47 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:21:44 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:21:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:21:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:21:46 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:21:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:23884877105a7ff84a910895cd044061a4561385ff6c36480ee080b76ec0e771`  
		Last Modified: Sat, 04 Apr 2020 12:21:10 GMT  
		Size: 26.7 MB (26689802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc38caa0f5b94141276220daaf428892096e4afd24b05668cd188311e00a635f`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 35.4 KB (35367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2910811b6c4227c2f42aaea9a3dd5f53b1d469f67e2cf7e601f631b119b61ff7`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36505266dcc64eeb1010bd2112e6f73981e1a8246e4f6d4e287763b57f101b0b`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69dcc78e96eb792fb67240a5ff4db2c3e3cb1ff55f97df2bddba0706fb5f6e6`  
		Last Modified: Fri, 24 Apr 2020 20:10:59 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222f44c5392d7a36df5eb58bb790223d332bd187fc56f006ecd66ad762f740e8`  
		Last Modified: Fri, 24 Apr 2020 20:10:59 GMT  
		Size: 4.8 MB (4807438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc64ea97b9cf087977c9a7972347db33f40487bcdd29abb41e7acf4c265335a`  
		Last Modified: Fri, 24 Apr 2020 20:10:58 GMT  
		Size: 1.3 MB (1326271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9912a149de6b3da2628c28ecfbd75992cda34df498d3634e6145bfdf1832a1a2`  
		Last Modified: Fri, 24 Apr 2020 20:10:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef6cf5b569752da3539a3b0c377a2a4f64e90f26eb7c89d405cf0168c923106`  
		Last Modified: Fri, 24 Apr 2020 20:10:57 GMT  
		Size: 929.2 KB (929212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a05be3688e04bf9961d4912e2dd86ff9832e72ec8c6b2d34c053e87ccf991a6`  
		Last Modified: Fri, 24 Apr 2020 20:10:57 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a1edf2a8459b3c38e04a5cdabd6030f22e09bb2f653d0e57020e1e77b530ea`  
		Last Modified: Wed, 13 May 2020 21:44:09 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4954c91ebe442c8d5c4bbcfb190d71bc2adc03debcf88573e9d55e9abaf0e9`  
		Last Modified: Wed, 13 May 2020 21:44:25 GMT  
		Size: 75.2 MB (75194669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae91c8217271570b6c43609f856cee367ae34cf2106fb9a589bc7698e52ba11`  
		Last Modified: Fri, 29 May 2020 00:22:25 GMT  
		Size: 4.8 KB (4846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ec0680735c5ff37d37fa985b1970c8fa5d17887fb1d8f72e9cdb6310e8f20a`  
		Last Modified: Fri, 29 May 2020 00:22:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.32-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:9449e7cd6f24e5f05d9ed73ca0d7b91e08f01cb543e53c07ea26492c8193c1b5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104077523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21aeeecb24c278756509b9b729346302aa2e6394c0e8cff15b0eeddf20d7ae56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 00:16:45 GMT
ADD file:bd5b3470601aa4a28132ec60a8b1c33516d09a1391864fe1dbf82a4030397fd1 in / 
# Fri, 24 Apr 2020 00:16:54 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 00:16:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:17:03 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:17:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 15:47:33 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 15:47:50 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 15:47:51 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 15:48:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 15:48:10 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 15:48:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 15:48:23 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 15:48:25 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 15:51:52 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 13 May 2020 20:47:48 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Wed, 13 May 2020 20:47:51 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 20:48:56 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 20:49:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:40:51 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:40:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:40:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:40:55 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:40:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c2cd007b69f7e5f37c851aa689e0e617fbaa3fe3e470f714337a03e569b7f434`  
		Last Modified: Sun, 05 Apr 2020 20:25:25 GMT  
		Size: 23.7 MB (23720401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c087f8bf83d28baa9c53fc5cfb0dfc79d5062cfad77563076553b04259e822f`  
		Last Modified: Fri, 24 Apr 2020 00:21:16 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474b5c43e9a24e1958763941a17a7cac60b13460a47f2ae9067ec03ceadab33a`  
		Last Modified: Fri, 24 Apr 2020 00:21:15 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7083e6591d76b9a6c13497a6a89bfbae3e7eb2eb31bec366bec3884c8e4517ce`  
		Last Modified: Fri, 24 Apr 2020 00:21:15 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340e908aa186ab7f11f80142d1c3a5bd2f7dbec25f58366dda5f22f44e06423c`  
		Last Modified: Fri, 24 Apr 2020 15:54:13 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f46da80a1eb3c07ecc7bb3784555bd9d502290a55fe1a3fe968f7446af3128`  
		Last Modified: Fri, 24 Apr 2020 15:54:14 GMT  
		Size: 4.4 MB (4393199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9374369ce5226b7dd75e6aae1665b5dd86552811ba35823b717d507c63063a0a`  
		Last Modified: Fri, 24 Apr 2020 15:54:13 GMT  
		Size: 1.3 MB (1262945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65d1839f1c97b9a6854699dfa28e745e6e8790a326818902165e646d97e8182`  
		Last Modified: Fri, 24 Apr 2020 15:54:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ac11fc4bc1dcef89d539dcbef6f8683a59c653edbf6b6b8674aaaf8b2b8c4b`  
		Last Modified: Fri, 24 Apr 2020 15:54:12 GMT  
		Size: 920.8 KB (920766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cf075dcf71cf7ff1c9ab8fa8b58253be69db20633df6da9c5ea5cf7b48b385`  
		Last Modified: Fri, 24 Apr 2020 15:54:11 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fba07a52f8c704b1aa302b5ca0154248b0d53474b9390afaa8de78e0ba3184`  
		Last Modified: Wed, 13 May 2020 20:53:29 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1442a0493fb5d092510edc3fafc58adb80c8ef3967ab64a8eeff4c9503f225e8`  
		Last Modified: Wed, 13 May 2020 20:53:52 GMT  
		Size: 73.7 MB (73731474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37eb11d1cd80a2cd32017f4726ba043ee47136d9476079d56dfe1429a21951b`  
		Last Modified: Fri, 29 May 2020 00:42:01 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25526a0ca962ab63af8cc7be2e24000fe22c4417b289c4eff1110e2fd672f628`  
		Last Modified: Fri, 29 May 2020 00:42:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.32-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:5c36761b92100924e7ac536939ac4137c013ae05b8cdeee7b462a956d7bc80cb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116238898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93cecc321cebccae35ecb8359bb9daea184ed336e8226b517019f2218f1f9dd8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:42:30 GMT
ADD file:726a32203fbcaae787c10740754e38dcb186778893e6d078db3cba0f49ee6b3c in / 
# Thu, 23 Apr 2020 20:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:42:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:42:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:42:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 11:56:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 11:57:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:58:10 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 11:59:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 11:59:14 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 11:59:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:59:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 11:59:54 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 12:09:45 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 13 May 2020 21:29:28 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Wed, 13 May 2020 21:29:36 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 21:31:04 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 21:31:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:18:34 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:18:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:18:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:18:49 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:beed3bd0a281cacead564771f079ed9ee8b272a2ed0e28f533e188f3d21fee6e`  
		Last Modified: Mon, 06 Apr 2020 15:40:20 GMT  
		Size: 30.4 MB (30400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae14d2411b83450b8afe92058b998540c56ec42f1ddd7581e8e9fe629c442f89`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82678240be3a5c783512ff7336f2b10837ae126958bc6bd1b476a8d039c08771`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307ad4f24078fd763b41ec7c1772f2fd5238fed1bae36c5d42d28ec9adbffb9`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e050ed2928ca970f92a55e32757c9a2bed2d12719ac1f8ffe473007ebfb5627a`  
		Last Modified: Fri, 24 Apr 2020 12:16:35 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f165cd342f0a2ae619a609d6874d38864a5cd9a56cdfc8876d139942c86b00b`  
		Last Modified: Fri, 24 Apr 2020 12:16:39 GMT  
		Size: 5.6 MB (5628683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5783ab2db059c111e57346fcb3db7da7d24c0be81aad5b27e670d5f0d2340fd8`  
		Last Modified: Fri, 24 Apr 2020 12:16:34 GMT  
		Size: 1.2 MB (1246415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3659f23141b0ba1d73e5c6f1922b480865fa378174eccf526a7280c40ad370d2`  
		Last Modified: Fri, 24 Apr 2020 12:16:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ad047e312e9236cb8b8743456d6e073c71c56ffa4f21e1af8769ad6726c805`  
		Last Modified: Fri, 24 Apr 2020 12:16:31 GMT  
		Size: 931.5 KB (931523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22944a8e89f53e83da58e8806dc3c4be25b3a2754635c108fc327c6ddb42789b`  
		Last Modified: Fri, 24 Apr 2020 12:16:31 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dfeebe25cc02ad3288ff3f03a92be19ef8664c7907b436859177684da5e508`  
		Last Modified: Wed, 13 May 2020 21:38:23 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145af634d57422884d13c0715874a0329aa049813e46d8a3ebace3333d997f67`  
		Last Modified: Wed, 13 May 2020 21:39:02 GMT  
		Size: 78.0 MB (77983227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a739aee0daaa14a73304a5a190b76705b8b2a5a6a3ff501b4b983bbcc2926f4`  
		Last Modified: Fri, 29 May 2020 00:21:16 GMT  
		Size: 4.8 KB (4849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c100b735d3acd167ca7325abc2eecd2cb3e3753090746bc73aada056882ff2b1`  
		Last Modified: Fri, 29 May 2020 00:21:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2-bionic`

```console
$ docker pull mariadb@sha256:ddff0c0d1a84d07af72f3e8e78f03452ef90b758843e004ffdce528aa0b11928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:eb1f6c4a4a01985d20283423421817c1a201e85de1192c6bed681dfee3664af3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (108996232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a144d514f6729156a6491a1806310f5e2d93042b24d921d8ba4bca7fc5e979c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:00 GMT
ADD file:c3e6bb316dfa6b81dd4478aaa310df532883b1c0a14edeec3f63d641980c1789 in / 
# Fri, 24 Apr 2020 01:07:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 20:07:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 20:07:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:07:25 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 20:07:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 20:07:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 20:07:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:07:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 20:07:43 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 20:09:29 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 13 May 2020 20:51:21 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Wed, 13 May 2020 20:51:22 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 20:51:47 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 20:51:47 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:21:44 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:21:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:21:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:21:46 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:21:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:23884877105a7ff84a910895cd044061a4561385ff6c36480ee080b76ec0e771`  
		Last Modified: Sat, 04 Apr 2020 12:21:10 GMT  
		Size: 26.7 MB (26689802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc38caa0f5b94141276220daaf428892096e4afd24b05668cd188311e00a635f`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 35.4 KB (35367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2910811b6c4227c2f42aaea9a3dd5f53b1d469f67e2cf7e601f631b119b61ff7`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36505266dcc64eeb1010bd2112e6f73981e1a8246e4f6d4e287763b57f101b0b`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69dcc78e96eb792fb67240a5ff4db2c3e3cb1ff55f97df2bddba0706fb5f6e6`  
		Last Modified: Fri, 24 Apr 2020 20:10:59 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222f44c5392d7a36df5eb58bb790223d332bd187fc56f006ecd66ad762f740e8`  
		Last Modified: Fri, 24 Apr 2020 20:10:59 GMT  
		Size: 4.8 MB (4807438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc64ea97b9cf087977c9a7972347db33f40487bcdd29abb41e7acf4c265335a`  
		Last Modified: Fri, 24 Apr 2020 20:10:58 GMT  
		Size: 1.3 MB (1326271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9912a149de6b3da2628c28ecfbd75992cda34df498d3634e6145bfdf1832a1a2`  
		Last Modified: Fri, 24 Apr 2020 20:10:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef6cf5b569752da3539a3b0c377a2a4f64e90f26eb7c89d405cf0168c923106`  
		Last Modified: Fri, 24 Apr 2020 20:10:57 GMT  
		Size: 929.2 KB (929212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a05be3688e04bf9961d4912e2dd86ff9832e72ec8c6b2d34c053e87ccf991a6`  
		Last Modified: Fri, 24 Apr 2020 20:10:57 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a1edf2a8459b3c38e04a5cdabd6030f22e09bb2f653d0e57020e1e77b530ea`  
		Last Modified: Wed, 13 May 2020 21:44:09 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4954c91ebe442c8d5c4bbcfb190d71bc2adc03debcf88573e9d55e9abaf0e9`  
		Last Modified: Wed, 13 May 2020 21:44:25 GMT  
		Size: 75.2 MB (75194669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae91c8217271570b6c43609f856cee367ae34cf2106fb9a589bc7698e52ba11`  
		Last Modified: Fri, 29 May 2020 00:22:25 GMT  
		Size: 4.8 KB (4846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ec0680735c5ff37d37fa985b1970c8fa5d17887fb1d8f72e9cdb6310e8f20a`  
		Last Modified: Fri, 29 May 2020 00:22:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:9449e7cd6f24e5f05d9ed73ca0d7b91e08f01cb543e53c07ea26492c8193c1b5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104077523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21aeeecb24c278756509b9b729346302aa2e6394c0e8cff15b0eeddf20d7ae56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 00:16:45 GMT
ADD file:bd5b3470601aa4a28132ec60a8b1c33516d09a1391864fe1dbf82a4030397fd1 in / 
# Fri, 24 Apr 2020 00:16:54 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 00:16:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:17:03 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:17:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 15:47:33 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 15:47:50 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 15:47:51 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 15:48:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 15:48:10 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 15:48:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 15:48:23 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 15:48:25 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 15:51:52 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 13 May 2020 20:47:48 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Wed, 13 May 2020 20:47:51 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 20:48:56 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 20:49:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:40:51 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:40:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:40:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:40:55 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:40:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c2cd007b69f7e5f37c851aa689e0e617fbaa3fe3e470f714337a03e569b7f434`  
		Last Modified: Sun, 05 Apr 2020 20:25:25 GMT  
		Size: 23.7 MB (23720401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c087f8bf83d28baa9c53fc5cfb0dfc79d5062cfad77563076553b04259e822f`  
		Last Modified: Fri, 24 Apr 2020 00:21:16 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474b5c43e9a24e1958763941a17a7cac60b13460a47f2ae9067ec03ceadab33a`  
		Last Modified: Fri, 24 Apr 2020 00:21:15 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7083e6591d76b9a6c13497a6a89bfbae3e7eb2eb31bec366bec3884c8e4517ce`  
		Last Modified: Fri, 24 Apr 2020 00:21:15 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340e908aa186ab7f11f80142d1c3a5bd2f7dbec25f58366dda5f22f44e06423c`  
		Last Modified: Fri, 24 Apr 2020 15:54:13 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f46da80a1eb3c07ecc7bb3784555bd9d502290a55fe1a3fe968f7446af3128`  
		Last Modified: Fri, 24 Apr 2020 15:54:14 GMT  
		Size: 4.4 MB (4393199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9374369ce5226b7dd75e6aae1665b5dd86552811ba35823b717d507c63063a0a`  
		Last Modified: Fri, 24 Apr 2020 15:54:13 GMT  
		Size: 1.3 MB (1262945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65d1839f1c97b9a6854699dfa28e745e6e8790a326818902165e646d97e8182`  
		Last Modified: Fri, 24 Apr 2020 15:54:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ac11fc4bc1dcef89d539dcbef6f8683a59c653edbf6b6b8674aaaf8b2b8c4b`  
		Last Modified: Fri, 24 Apr 2020 15:54:12 GMT  
		Size: 920.8 KB (920766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cf075dcf71cf7ff1c9ab8fa8b58253be69db20633df6da9c5ea5cf7b48b385`  
		Last Modified: Fri, 24 Apr 2020 15:54:11 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fba07a52f8c704b1aa302b5ca0154248b0d53474b9390afaa8de78e0ba3184`  
		Last Modified: Wed, 13 May 2020 20:53:29 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1442a0493fb5d092510edc3fafc58adb80c8ef3967ab64a8eeff4c9503f225e8`  
		Last Modified: Wed, 13 May 2020 20:53:52 GMT  
		Size: 73.7 MB (73731474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37eb11d1cd80a2cd32017f4726ba043ee47136d9476079d56dfe1429a21951b`  
		Last Modified: Fri, 29 May 2020 00:42:01 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25526a0ca962ab63af8cc7be2e24000fe22c4417b289c4eff1110e2fd672f628`  
		Last Modified: Fri, 29 May 2020 00:42:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:5c36761b92100924e7ac536939ac4137c013ae05b8cdeee7b462a956d7bc80cb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116238898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93cecc321cebccae35ecb8359bb9daea184ed336e8226b517019f2218f1f9dd8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:42:30 GMT
ADD file:726a32203fbcaae787c10740754e38dcb186778893e6d078db3cba0f49ee6b3c in / 
# Thu, 23 Apr 2020 20:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:42:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:42:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:42:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 11:56:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 11:57:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:58:10 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 11:59:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 11:59:14 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 11:59:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:59:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 11:59:54 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 12:09:45 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 13 May 2020 21:29:28 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Wed, 13 May 2020 21:29:36 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 21:31:04 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 21:31:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:18:34 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:18:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:18:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:18:49 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:beed3bd0a281cacead564771f079ed9ee8b272a2ed0e28f533e188f3d21fee6e`  
		Last Modified: Mon, 06 Apr 2020 15:40:20 GMT  
		Size: 30.4 MB (30400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae14d2411b83450b8afe92058b998540c56ec42f1ddd7581e8e9fe629c442f89`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82678240be3a5c783512ff7336f2b10837ae126958bc6bd1b476a8d039c08771`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307ad4f24078fd763b41ec7c1772f2fd5238fed1bae36c5d42d28ec9adbffb9`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e050ed2928ca970f92a55e32757c9a2bed2d12719ac1f8ffe473007ebfb5627a`  
		Last Modified: Fri, 24 Apr 2020 12:16:35 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f165cd342f0a2ae619a609d6874d38864a5cd9a56cdfc8876d139942c86b00b`  
		Last Modified: Fri, 24 Apr 2020 12:16:39 GMT  
		Size: 5.6 MB (5628683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5783ab2db059c111e57346fcb3db7da7d24c0be81aad5b27e670d5f0d2340fd8`  
		Last Modified: Fri, 24 Apr 2020 12:16:34 GMT  
		Size: 1.2 MB (1246415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3659f23141b0ba1d73e5c6f1922b480865fa378174eccf526a7280c40ad370d2`  
		Last Modified: Fri, 24 Apr 2020 12:16:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ad047e312e9236cb8b8743456d6e073c71c56ffa4f21e1af8769ad6726c805`  
		Last Modified: Fri, 24 Apr 2020 12:16:31 GMT  
		Size: 931.5 KB (931523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22944a8e89f53e83da58e8806dc3c4be25b3a2754635c108fc327c6ddb42789b`  
		Last Modified: Fri, 24 Apr 2020 12:16:31 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dfeebe25cc02ad3288ff3f03a92be19ef8664c7907b436859177684da5e508`  
		Last Modified: Wed, 13 May 2020 21:38:23 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145af634d57422884d13c0715874a0329aa049813e46d8a3ebace3333d997f67`  
		Last Modified: Wed, 13 May 2020 21:39:02 GMT  
		Size: 78.0 MB (77983227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a739aee0daaa14a73304a5a190b76705b8b2a5a6a3ff501b4b983bbcc2926f4`  
		Last Modified: Fri, 29 May 2020 00:21:16 GMT  
		Size: 4.8 KB (4849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c100b735d3acd167ca7325abc2eecd2cb3e3753090746bc73aada056882ff2b1`  
		Last Modified: Fri, 29 May 2020 00:21:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3`

```console
$ docker pull mariadb@sha256:e2df41d1e138062e37ec493b25ffeb9e181267d0948507af7670c6a4a91ad91b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3` - linux; amd64

```console
$ docker pull mariadb@sha256:91436c443be256515804695e3e4bb10c63da53b874a24a5fa1fcc58a134d5f03
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119186637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e6eec5b8a160e797d9496acc941ad5862888dd3e9886c4025bc35a34d19c85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:25:31 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 12 Jun 2020 18:25:31 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Fri, 12 Jun 2020 18:25:32 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:25:57 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:25:57 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:25:58 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:25:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:25:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:25:59 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:25:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c589be17d1ce856007eb81ff3b231e335f96a58eb63481253b453db7f6beaa`  
		Last Modified: Fri, 12 Jun 2020 18:27:09 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64145edf74b26c97e82a91fdfb45dca3ce0bb054ec1ba9bb9fd8b591fe6e8d60`  
		Last Modified: Fri, 12 Jun 2020 18:27:31 GMT  
		Size: 82.5 MB (82510657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e760ac9383651d4f5e8d2d2b9952fe03f09e2754a5aa5c9a244dc9adbde1ba`  
		Last Modified: Fri, 12 Jun 2020 18:27:09 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf4a7d63a16d9790172e0fd5999a0c6a9a9ef2059def2b3b0b89020f42dbca7`  
		Last Modified: Fri, 12 Jun 2020 18:27:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:5e3709d9954ef9e65221bb2db0d049aa275fe37188b5673d732fd1ddcf17444c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116834517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a42b10f1c10b75256028bd380d91ec797db1e65a8e2a69ff8d55bba87030e27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 00:18:16 GMT
ADD file:e9947aff2dfa8f220d4b25dc0770aff8d9ffc08482e52f54833f39e1c3ec08bf in / 
# Fri, 24 Apr 2020 00:18:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 00:18:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:18:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:18:29 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:53:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:53:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:53:46 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:54:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:54:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:54:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:54:14 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:54:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:56:33 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 12 Jun 2020 18:56:33 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Fri, 12 Jun 2020 18:56:35 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:57:37 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:57:39 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:57:40 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:57:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:57:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:57:44 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:57:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c2d76ba33f8d52087147ce28d8f03c08f69677591e3e10db810bf76a6e09427`  
		Last Modified: Fri, 24 Apr 2020 00:22:00 GMT  
		Size: 27.2 MB (27158644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92d4cfc71d3821474946021fdbf241a74992a84c6269c3e9a052ce7fc56cece`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 32.3 KB (32326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63063bfe137200b3c8d1ee8d819124352c20ee8c189a0388f461ec66bb759310`  
		Last Modified: Fri, 24 Apr 2020 00:21:53 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38385900086ffa7d7cb9c3bbeabaf2176d7d7958ebf0736d2a01773a830201ee`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0959e86d4d132b0e91456f1d1ecc3b1d6518d720b7ee82926559fd34800d7b53`  
		Last Modified: Fri, 12 Jun 2020 18:58:18 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f37953089cdddf8b409b61f0f30de595d96483dd0ce38463384dd5d201b70f`  
		Last Modified: Fri, 12 Jun 2020 18:58:19 GMT  
		Size: 5.5 MB (5456917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab7a5713dbb2830a805d0b68dae96ce4dd827b086473a3d785f76b37d885fe1`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 1.3 MB (1258973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0614221a0d602714b38672c572d4071df43a41223dab9b1c81ab45ea5bc9c9`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e232435757d992d57a40890acb9528958726ef62b7f400e4ef7c3b7d97c234c`  
		Last Modified: Fri, 12 Jun 2020 18:58:16 GMT  
		Size: 1.3 MB (1263367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb430a3947464ff3d178d412e9047e4b67e2cc3a09923dd4b84596fa57403d66`  
		Last Modified: Fri, 12 Jun 2020 18:58:15 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feaa6f99281846ec5fd74544b56bac9996727c1290950f3bc5000e2d2ad8c8aa`  
		Last Modified: Fri, 12 Jun 2020 18:59:38 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e2b01c4828d87323e2c9610adda5a1fc6634fb675e2f5a3d5ecd8ca3612e06`  
		Last Modified: Fri, 12 Jun 2020 19:00:04 GMT  
		Size: 81.7 MB (81653557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad1529830449e58339e41a675e4801f7dae04a42b5e9af979eaeb4468502ce9`  
		Last Modified: Fri, 12 Jun 2020 18:59:38 GMT  
		Size: 4.9 KB (4856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee589be907fa4c2b253fa268684f1e7f1212815bd0d000499ef19c7b64fd737a`  
		Last Modified: Fri, 12 Jun 2020 18:59:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; ppc64le

```console
$ docker pull mariadb@sha256:1df4e1ece3cc05b9beec65be935b9cca6ce678cedcd1874c0a2c22217a38eda4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (129048351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a469296cf72ff7286030b3e5166c79524fa0703bb766a11f44b772b5ece0053`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 19:04:51 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 12 Jun 2020 19:05:05 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Fri, 12 Jun 2020 19:05:25 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 19:11:12 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 19:11:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 19:11:27 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 19:11:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 19:11:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 19:12:00 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 19:12:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3e3684e96a3273ea708e45edce664e0bd43d8c982c92d03a51588c6a24eb0f`  
		Last Modified: Fri, 12 Jun 2020 19:14:52 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10f969e78ca7b123018dc731e9a741d6561b2192e4089d101fe72f7449b088a`  
		Last Modified: Fri, 12 Jun 2020 19:15:12 GMT  
		Size: 86.5 MB (86537862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c80fc2592043d6d3771e008c7ae87e5b1b8b37765333729601521f21aeae90`  
		Last Modified: Fri, 12 Jun 2020 19:14:51 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6dbf7a2967109ac5529a53c507be0a0a24c7df5e1cbefd878f94ea6f6c6430`  
		Last Modified: Fri, 12 Jun 2020 19:14:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.23`

```console
$ docker pull mariadb@sha256:e2df41d1e138062e37ec493b25ffeb9e181267d0948507af7670c6a4a91ad91b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.23` - linux; amd64

```console
$ docker pull mariadb@sha256:91436c443be256515804695e3e4bb10c63da53b874a24a5fa1fcc58a134d5f03
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119186637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e6eec5b8a160e797d9496acc941ad5862888dd3e9886c4025bc35a34d19c85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:25:31 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 12 Jun 2020 18:25:31 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Fri, 12 Jun 2020 18:25:32 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:25:57 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:25:57 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:25:58 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:25:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:25:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:25:59 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:25:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c589be17d1ce856007eb81ff3b231e335f96a58eb63481253b453db7f6beaa`  
		Last Modified: Fri, 12 Jun 2020 18:27:09 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64145edf74b26c97e82a91fdfb45dca3ce0bb054ec1ba9bb9fd8b591fe6e8d60`  
		Last Modified: Fri, 12 Jun 2020 18:27:31 GMT  
		Size: 82.5 MB (82510657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e760ac9383651d4f5e8d2d2b9952fe03f09e2754a5aa5c9a244dc9adbde1ba`  
		Last Modified: Fri, 12 Jun 2020 18:27:09 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf4a7d63a16d9790172e0fd5999a0c6a9a9ef2059def2b3b0b89020f42dbca7`  
		Last Modified: Fri, 12 Jun 2020 18:27:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.23` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:5e3709d9954ef9e65221bb2db0d049aa275fe37188b5673d732fd1ddcf17444c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116834517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a42b10f1c10b75256028bd380d91ec797db1e65a8e2a69ff8d55bba87030e27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 00:18:16 GMT
ADD file:e9947aff2dfa8f220d4b25dc0770aff8d9ffc08482e52f54833f39e1c3ec08bf in / 
# Fri, 24 Apr 2020 00:18:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 00:18:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:18:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:18:29 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:53:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:53:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:53:46 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:54:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:54:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:54:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:54:14 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:54:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:56:33 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 12 Jun 2020 18:56:33 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Fri, 12 Jun 2020 18:56:35 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:57:37 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:57:39 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:57:40 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:57:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:57:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:57:44 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:57:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c2d76ba33f8d52087147ce28d8f03c08f69677591e3e10db810bf76a6e09427`  
		Last Modified: Fri, 24 Apr 2020 00:22:00 GMT  
		Size: 27.2 MB (27158644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92d4cfc71d3821474946021fdbf241a74992a84c6269c3e9a052ce7fc56cece`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 32.3 KB (32326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63063bfe137200b3c8d1ee8d819124352c20ee8c189a0388f461ec66bb759310`  
		Last Modified: Fri, 24 Apr 2020 00:21:53 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38385900086ffa7d7cb9c3bbeabaf2176d7d7958ebf0736d2a01773a830201ee`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0959e86d4d132b0e91456f1d1ecc3b1d6518d720b7ee82926559fd34800d7b53`  
		Last Modified: Fri, 12 Jun 2020 18:58:18 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f37953089cdddf8b409b61f0f30de595d96483dd0ce38463384dd5d201b70f`  
		Last Modified: Fri, 12 Jun 2020 18:58:19 GMT  
		Size: 5.5 MB (5456917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab7a5713dbb2830a805d0b68dae96ce4dd827b086473a3d785f76b37d885fe1`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 1.3 MB (1258973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0614221a0d602714b38672c572d4071df43a41223dab9b1c81ab45ea5bc9c9`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e232435757d992d57a40890acb9528958726ef62b7f400e4ef7c3b7d97c234c`  
		Last Modified: Fri, 12 Jun 2020 18:58:16 GMT  
		Size: 1.3 MB (1263367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb430a3947464ff3d178d412e9047e4b67e2cc3a09923dd4b84596fa57403d66`  
		Last Modified: Fri, 12 Jun 2020 18:58:15 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feaa6f99281846ec5fd74544b56bac9996727c1290950f3bc5000e2d2ad8c8aa`  
		Last Modified: Fri, 12 Jun 2020 18:59:38 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e2b01c4828d87323e2c9610adda5a1fc6634fb675e2f5a3d5ecd8ca3612e06`  
		Last Modified: Fri, 12 Jun 2020 19:00:04 GMT  
		Size: 81.7 MB (81653557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad1529830449e58339e41a675e4801f7dae04a42b5e9af979eaeb4468502ce9`  
		Last Modified: Fri, 12 Jun 2020 18:59:38 GMT  
		Size: 4.9 KB (4856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee589be907fa4c2b253fa268684f1e7f1212815bd0d000499ef19c7b64fd737a`  
		Last Modified: Fri, 12 Jun 2020 18:59:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.23` - linux; ppc64le

```console
$ docker pull mariadb@sha256:1df4e1ece3cc05b9beec65be935b9cca6ce678cedcd1874c0a2c22217a38eda4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (129048351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a469296cf72ff7286030b3e5166c79524fa0703bb766a11f44b772b5ece0053`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 19:04:51 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 12 Jun 2020 19:05:05 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Fri, 12 Jun 2020 19:05:25 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 19:11:12 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 19:11:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 19:11:27 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 19:11:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 19:11:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 19:12:00 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 19:12:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3e3684e96a3273ea708e45edce664e0bd43d8c982c92d03a51588c6a24eb0f`  
		Last Modified: Fri, 12 Jun 2020 19:14:52 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10f969e78ca7b123018dc731e9a741d6561b2192e4089d101fe72f7449b088a`  
		Last Modified: Fri, 12 Jun 2020 19:15:12 GMT  
		Size: 86.5 MB (86537862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c80fc2592043d6d3771e008c7ae87e5b1b8b37765333729601521f21aeae90`  
		Last Modified: Fri, 12 Jun 2020 19:14:51 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6dbf7a2967109ac5529a53c507be0a0a24c7df5e1cbefd878f94ea6f6c6430`  
		Last Modified: Fri, 12 Jun 2020 19:14:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.23-focal`

```console
$ docker pull mariadb@sha256:e2df41d1e138062e37ec493b25ffeb9e181267d0948507af7670c6a4a91ad91b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.23-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:91436c443be256515804695e3e4bb10c63da53b874a24a5fa1fcc58a134d5f03
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119186637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e6eec5b8a160e797d9496acc941ad5862888dd3e9886c4025bc35a34d19c85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:25:31 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 12 Jun 2020 18:25:31 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Fri, 12 Jun 2020 18:25:32 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:25:57 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:25:57 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:25:58 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:25:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:25:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:25:59 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:25:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c589be17d1ce856007eb81ff3b231e335f96a58eb63481253b453db7f6beaa`  
		Last Modified: Fri, 12 Jun 2020 18:27:09 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64145edf74b26c97e82a91fdfb45dca3ce0bb054ec1ba9bb9fd8b591fe6e8d60`  
		Last Modified: Fri, 12 Jun 2020 18:27:31 GMT  
		Size: 82.5 MB (82510657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e760ac9383651d4f5e8d2d2b9952fe03f09e2754a5aa5c9a244dc9adbde1ba`  
		Last Modified: Fri, 12 Jun 2020 18:27:09 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf4a7d63a16d9790172e0fd5999a0c6a9a9ef2059def2b3b0b89020f42dbca7`  
		Last Modified: Fri, 12 Jun 2020 18:27:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.23-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:5e3709d9954ef9e65221bb2db0d049aa275fe37188b5673d732fd1ddcf17444c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116834517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a42b10f1c10b75256028bd380d91ec797db1e65a8e2a69ff8d55bba87030e27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 00:18:16 GMT
ADD file:e9947aff2dfa8f220d4b25dc0770aff8d9ffc08482e52f54833f39e1c3ec08bf in / 
# Fri, 24 Apr 2020 00:18:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 00:18:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:18:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:18:29 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:53:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:53:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:53:46 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:54:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:54:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:54:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:54:14 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:54:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:56:33 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 12 Jun 2020 18:56:33 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Fri, 12 Jun 2020 18:56:35 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:57:37 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:57:39 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:57:40 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:57:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:57:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:57:44 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:57:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c2d76ba33f8d52087147ce28d8f03c08f69677591e3e10db810bf76a6e09427`  
		Last Modified: Fri, 24 Apr 2020 00:22:00 GMT  
		Size: 27.2 MB (27158644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92d4cfc71d3821474946021fdbf241a74992a84c6269c3e9a052ce7fc56cece`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 32.3 KB (32326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63063bfe137200b3c8d1ee8d819124352c20ee8c189a0388f461ec66bb759310`  
		Last Modified: Fri, 24 Apr 2020 00:21:53 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38385900086ffa7d7cb9c3bbeabaf2176d7d7958ebf0736d2a01773a830201ee`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0959e86d4d132b0e91456f1d1ecc3b1d6518d720b7ee82926559fd34800d7b53`  
		Last Modified: Fri, 12 Jun 2020 18:58:18 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f37953089cdddf8b409b61f0f30de595d96483dd0ce38463384dd5d201b70f`  
		Last Modified: Fri, 12 Jun 2020 18:58:19 GMT  
		Size: 5.5 MB (5456917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab7a5713dbb2830a805d0b68dae96ce4dd827b086473a3d785f76b37d885fe1`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 1.3 MB (1258973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0614221a0d602714b38672c572d4071df43a41223dab9b1c81ab45ea5bc9c9`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e232435757d992d57a40890acb9528958726ef62b7f400e4ef7c3b7d97c234c`  
		Last Modified: Fri, 12 Jun 2020 18:58:16 GMT  
		Size: 1.3 MB (1263367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb430a3947464ff3d178d412e9047e4b67e2cc3a09923dd4b84596fa57403d66`  
		Last Modified: Fri, 12 Jun 2020 18:58:15 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feaa6f99281846ec5fd74544b56bac9996727c1290950f3bc5000e2d2ad8c8aa`  
		Last Modified: Fri, 12 Jun 2020 18:59:38 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e2b01c4828d87323e2c9610adda5a1fc6634fb675e2f5a3d5ecd8ca3612e06`  
		Last Modified: Fri, 12 Jun 2020 19:00:04 GMT  
		Size: 81.7 MB (81653557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad1529830449e58339e41a675e4801f7dae04a42b5e9af979eaeb4468502ce9`  
		Last Modified: Fri, 12 Jun 2020 18:59:38 GMT  
		Size: 4.9 KB (4856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee589be907fa4c2b253fa268684f1e7f1212815bd0d000499ef19c7b64fd737a`  
		Last Modified: Fri, 12 Jun 2020 18:59:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.23-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:1df4e1ece3cc05b9beec65be935b9cca6ce678cedcd1874c0a2c22217a38eda4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (129048351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a469296cf72ff7286030b3e5166c79524fa0703bb766a11f44b772b5ece0053`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 19:04:51 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 12 Jun 2020 19:05:05 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Fri, 12 Jun 2020 19:05:25 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 19:11:12 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 19:11:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 19:11:27 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 19:11:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 19:11:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 19:12:00 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 19:12:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3e3684e96a3273ea708e45edce664e0bd43d8c982c92d03a51588c6a24eb0f`  
		Last Modified: Fri, 12 Jun 2020 19:14:52 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10f969e78ca7b123018dc731e9a741d6561b2192e4089d101fe72f7449b088a`  
		Last Modified: Fri, 12 Jun 2020 19:15:12 GMT  
		Size: 86.5 MB (86537862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c80fc2592043d6d3771e008c7ae87e5b1b8b37765333729601521f21aeae90`  
		Last Modified: Fri, 12 Jun 2020 19:14:51 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6dbf7a2967109ac5529a53c507be0a0a24c7df5e1cbefd878f94ea6f6c6430`  
		Last Modified: Fri, 12 Jun 2020 19:14:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3-focal`

```console
$ docker pull mariadb@sha256:e2df41d1e138062e37ec493b25ffeb9e181267d0948507af7670c6a4a91ad91b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:91436c443be256515804695e3e4bb10c63da53b874a24a5fa1fcc58a134d5f03
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119186637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e6eec5b8a160e797d9496acc941ad5862888dd3e9886c4025bc35a34d19c85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:25:31 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 12 Jun 2020 18:25:31 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Fri, 12 Jun 2020 18:25:32 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:25:57 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:25:57 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:25:58 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:25:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:25:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:25:59 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:25:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c589be17d1ce856007eb81ff3b231e335f96a58eb63481253b453db7f6beaa`  
		Last Modified: Fri, 12 Jun 2020 18:27:09 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64145edf74b26c97e82a91fdfb45dca3ce0bb054ec1ba9bb9fd8b591fe6e8d60`  
		Last Modified: Fri, 12 Jun 2020 18:27:31 GMT  
		Size: 82.5 MB (82510657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e760ac9383651d4f5e8d2d2b9952fe03f09e2754a5aa5c9a244dc9adbde1ba`  
		Last Modified: Fri, 12 Jun 2020 18:27:09 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf4a7d63a16d9790172e0fd5999a0c6a9a9ef2059def2b3b0b89020f42dbca7`  
		Last Modified: Fri, 12 Jun 2020 18:27:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:5e3709d9954ef9e65221bb2db0d049aa275fe37188b5673d732fd1ddcf17444c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116834517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a42b10f1c10b75256028bd380d91ec797db1e65a8e2a69ff8d55bba87030e27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 00:18:16 GMT
ADD file:e9947aff2dfa8f220d4b25dc0770aff8d9ffc08482e52f54833f39e1c3ec08bf in / 
# Fri, 24 Apr 2020 00:18:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 00:18:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:18:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:18:29 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:53:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:53:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:53:46 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:54:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:54:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:54:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:54:14 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:54:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:56:33 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 12 Jun 2020 18:56:33 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Fri, 12 Jun 2020 18:56:35 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:57:37 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:57:39 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:57:40 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:57:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:57:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:57:44 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:57:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c2d76ba33f8d52087147ce28d8f03c08f69677591e3e10db810bf76a6e09427`  
		Last Modified: Fri, 24 Apr 2020 00:22:00 GMT  
		Size: 27.2 MB (27158644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92d4cfc71d3821474946021fdbf241a74992a84c6269c3e9a052ce7fc56cece`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 32.3 KB (32326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63063bfe137200b3c8d1ee8d819124352c20ee8c189a0388f461ec66bb759310`  
		Last Modified: Fri, 24 Apr 2020 00:21:53 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38385900086ffa7d7cb9c3bbeabaf2176d7d7958ebf0736d2a01773a830201ee`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0959e86d4d132b0e91456f1d1ecc3b1d6518d720b7ee82926559fd34800d7b53`  
		Last Modified: Fri, 12 Jun 2020 18:58:18 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f37953089cdddf8b409b61f0f30de595d96483dd0ce38463384dd5d201b70f`  
		Last Modified: Fri, 12 Jun 2020 18:58:19 GMT  
		Size: 5.5 MB (5456917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab7a5713dbb2830a805d0b68dae96ce4dd827b086473a3d785f76b37d885fe1`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 1.3 MB (1258973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0614221a0d602714b38672c572d4071df43a41223dab9b1c81ab45ea5bc9c9`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e232435757d992d57a40890acb9528958726ef62b7f400e4ef7c3b7d97c234c`  
		Last Modified: Fri, 12 Jun 2020 18:58:16 GMT  
		Size: 1.3 MB (1263367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb430a3947464ff3d178d412e9047e4b67e2cc3a09923dd4b84596fa57403d66`  
		Last Modified: Fri, 12 Jun 2020 18:58:15 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feaa6f99281846ec5fd74544b56bac9996727c1290950f3bc5000e2d2ad8c8aa`  
		Last Modified: Fri, 12 Jun 2020 18:59:38 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e2b01c4828d87323e2c9610adda5a1fc6634fb675e2f5a3d5ecd8ca3612e06`  
		Last Modified: Fri, 12 Jun 2020 19:00:04 GMT  
		Size: 81.7 MB (81653557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad1529830449e58339e41a675e4801f7dae04a42b5e9af979eaeb4468502ce9`  
		Last Modified: Fri, 12 Jun 2020 18:59:38 GMT  
		Size: 4.9 KB (4856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee589be907fa4c2b253fa268684f1e7f1212815bd0d000499ef19c7b64fd737a`  
		Last Modified: Fri, 12 Jun 2020 18:59:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:1df4e1ece3cc05b9beec65be935b9cca6ce678cedcd1874c0a2c22217a38eda4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (129048351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a469296cf72ff7286030b3e5166c79524fa0703bb766a11f44b772b5ece0053`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 19:04:51 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 12 Jun 2020 19:05:05 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Fri, 12 Jun 2020 19:05:25 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 19:11:12 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 19:11:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 19:11:27 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 19:11:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 19:11:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 19:12:00 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 19:12:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3e3684e96a3273ea708e45edce664e0bd43d8c982c92d03a51588c6a24eb0f`  
		Last Modified: Fri, 12 Jun 2020 19:14:52 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10f969e78ca7b123018dc731e9a741d6561b2192e4089d101fe72f7449b088a`  
		Last Modified: Fri, 12 Jun 2020 19:15:12 GMT  
		Size: 86.5 MB (86537862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c80fc2592043d6d3771e008c7ae87e5b1b8b37765333729601521f21aeae90`  
		Last Modified: Fri, 12 Jun 2020 19:14:51 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6dbf7a2967109ac5529a53c507be0a0a24c7df5e1cbefd878f94ea6f6c6430`  
		Last Modified: Fri, 12 Jun 2020 19:14:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4`

```console
$ docker pull mariadb@sha256:3ce8368efbf25059a1b7d2ff1df9f1cdb52fcd272eb2b906599e8613971379bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4` - linux; amd64

```console
$ docker pull mariadb@sha256:b0fe725e9008b651ee0577383887728879986580d1e0a809dc263a04d1c40907
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123544564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41c9d63e23e3408f9615c5519ef1a540874e867460268af29993862155376a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:25:03 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:25:22 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:25:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:25:23 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:25:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:25:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:25:24 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:25:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d075a6a30ab84cd85dbfe7ff6b7ff4b1da51420bb6502fbbcd165a6362314d89`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d12c1b8c73e8aaa38978b59b62c4a6d88faaf072f8dd8170cc20c995ea6182`  
		Last Modified: Fri, 12 Jun 2020 18:27:01 GMT  
		Size: 86.9 MB (86868588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10938405ff505cbefc2abf93e72607642d6d13d611bf1df914c7ccc62f2010fa`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 4.9 KB (4851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3656315d96d9326a97929d688679e34d594759499e9f6e6652ce44a70d285c64`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:8c7b8ef0282a747aa0e686f5c2d3b68f050f8d5aebc51884681057f3d6bab5af
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121139407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227094abd47e39aba82a11a0d4aff3492e3733207529c4fb90f4d1fa8299d10c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 00:18:16 GMT
ADD file:e9947aff2dfa8f220d4b25dc0770aff8d9ffc08482e52f54833f39e1c3ec08bf in / 
# Fri, 24 Apr 2020 00:18:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 00:18:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:18:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:18:29 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:53:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:53:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:53:46 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:54:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:54:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:54:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:54:14 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:54:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:55:26 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:55:26 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:55:28 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:56:18 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:56:20 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:56:21 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:56:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:56:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:56:24 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:56:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c2d76ba33f8d52087147ce28d8f03c08f69677591e3e10db810bf76a6e09427`  
		Last Modified: Fri, 24 Apr 2020 00:22:00 GMT  
		Size: 27.2 MB (27158644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92d4cfc71d3821474946021fdbf241a74992a84c6269c3e9a052ce7fc56cece`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 32.3 KB (32326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63063bfe137200b3c8d1ee8d819124352c20ee8c189a0388f461ec66bb759310`  
		Last Modified: Fri, 24 Apr 2020 00:21:53 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38385900086ffa7d7cb9c3bbeabaf2176d7d7958ebf0736d2a01773a830201ee`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0959e86d4d132b0e91456f1d1ecc3b1d6518d720b7ee82926559fd34800d7b53`  
		Last Modified: Fri, 12 Jun 2020 18:58:18 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f37953089cdddf8b409b61f0f30de595d96483dd0ce38463384dd5d201b70f`  
		Last Modified: Fri, 12 Jun 2020 18:58:19 GMT  
		Size: 5.5 MB (5456917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab7a5713dbb2830a805d0b68dae96ce4dd827b086473a3d785f76b37d885fe1`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 1.3 MB (1258973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0614221a0d602714b38672c572d4071df43a41223dab9b1c81ab45ea5bc9c9`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e232435757d992d57a40890acb9528958726ef62b7f400e4ef7c3b7d97c234c`  
		Last Modified: Fri, 12 Jun 2020 18:58:16 GMT  
		Size: 1.3 MB (1263367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb430a3947464ff3d178d412e9047e4b67e2cc3a09923dd4b84596fa57403d66`  
		Last Modified: Fri, 12 Jun 2020 18:58:15 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c366377b87f5bd2fac450a70e60f1eb72d08d295b001fe3744ab2ce6aba51c50`  
		Last Modified: Fri, 12 Jun 2020 18:58:52 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2724d7dec4121bbe85b94aa2443356afd739e9b04e6adfc6f42b6b6e905a95f7`  
		Last Modified: Fri, 12 Jun 2020 18:59:19 GMT  
		Size: 86.0 MB (85958453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c46e43e925893ef88759184e58a70d17f45392e6524dfddf0d68becb6077b9`  
		Last Modified: Fri, 12 Jun 2020 18:58:52 GMT  
		Size: 4.9 KB (4851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d77187f1fde12afc91b5b14093343ab71bc1d97ed7e79c60e4722d5c39ea0ca`  
		Last Modified: Fri, 12 Jun 2020 18:58:53 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a1705f7fecaefda698c2cf024327bca91cb8f66f2103614ae4d050f3ae194a4e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133498155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d3057995bde70b21d4b3cf61e8df037115877ab7f95cdf5326e78e3c2020c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:56:35 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:56:46 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:57:04 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 19:02:53 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 19:03:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 19:03:18 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 19:03:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 19:03:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 19:04:08 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 19:04:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03b359a03f81831c2fd57d9416ebc819388fd8574d85ad8898645d72f66c3c7`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09607cc66ed45e59b9ecfd2ed2dde55ce5b8e9b80729c7e1e9afa3c8d8e417ec`  
		Last Modified: Fri, 12 Jun 2020 19:14:23 GMT  
		Size: 91.0 MB (90987667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4bd398a89880ad4c07dbeb3afa3e02a724fbc012f4713549758f5ea6f58a11`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dfb689374ca4c43f6019d271c2cd0aa592a343710516129428cebb3c3cb9e3`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.13`

```console
$ docker pull mariadb@sha256:3ce8368efbf25059a1b7d2ff1df9f1cdb52fcd272eb2b906599e8613971379bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.13` - linux; amd64

```console
$ docker pull mariadb@sha256:b0fe725e9008b651ee0577383887728879986580d1e0a809dc263a04d1c40907
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123544564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41c9d63e23e3408f9615c5519ef1a540874e867460268af29993862155376a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:25:03 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:25:22 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:25:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:25:23 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:25:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:25:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:25:24 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:25:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d075a6a30ab84cd85dbfe7ff6b7ff4b1da51420bb6502fbbcd165a6362314d89`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d12c1b8c73e8aaa38978b59b62c4a6d88faaf072f8dd8170cc20c995ea6182`  
		Last Modified: Fri, 12 Jun 2020 18:27:01 GMT  
		Size: 86.9 MB (86868588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10938405ff505cbefc2abf93e72607642d6d13d611bf1df914c7ccc62f2010fa`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 4.9 KB (4851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3656315d96d9326a97929d688679e34d594759499e9f6e6652ce44a70d285c64`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.13` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:8c7b8ef0282a747aa0e686f5c2d3b68f050f8d5aebc51884681057f3d6bab5af
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121139407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227094abd47e39aba82a11a0d4aff3492e3733207529c4fb90f4d1fa8299d10c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 00:18:16 GMT
ADD file:e9947aff2dfa8f220d4b25dc0770aff8d9ffc08482e52f54833f39e1c3ec08bf in / 
# Fri, 24 Apr 2020 00:18:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 00:18:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:18:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:18:29 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:53:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:53:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:53:46 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:54:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:54:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:54:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:54:14 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:54:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:55:26 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:55:26 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:55:28 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:56:18 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:56:20 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:56:21 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:56:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:56:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:56:24 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:56:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c2d76ba33f8d52087147ce28d8f03c08f69677591e3e10db810bf76a6e09427`  
		Last Modified: Fri, 24 Apr 2020 00:22:00 GMT  
		Size: 27.2 MB (27158644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92d4cfc71d3821474946021fdbf241a74992a84c6269c3e9a052ce7fc56cece`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 32.3 KB (32326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63063bfe137200b3c8d1ee8d819124352c20ee8c189a0388f461ec66bb759310`  
		Last Modified: Fri, 24 Apr 2020 00:21:53 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38385900086ffa7d7cb9c3bbeabaf2176d7d7958ebf0736d2a01773a830201ee`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0959e86d4d132b0e91456f1d1ecc3b1d6518d720b7ee82926559fd34800d7b53`  
		Last Modified: Fri, 12 Jun 2020 18:58:18 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f37953089cdddf8b409b61f0f30de595d96483dd0ce38463384dd5d201b70f`  
		Last Modified: Fri, 12 Jun 2020 18:58:19 GMT  
		Size: 5.5 MB (5456917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab7a5713dbb2830a805d0b68dae96ce4dd827b086473a3d785f76b37d885fe1`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 1.3 MB (1258973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0614221a0d602714b38672c572d4071df43a41223dab9b1c81ab45ea5bc9c9`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e232435757d992d57a40890acb9528958726ef62b7f400e4ef7c3b7d97c234c`  
		Last Modified: Fri, 12 Jun 2020 18:58:16 GMT  
		Size: 1.3 MB (1263367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb430a3947464ff3d178d412e9047e4b67e2cc3a09923dd4b84596fa57403d66`  
		Last Modified: Fri, 12 Jun 2020 18:58:15 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c366377b87f5bd2fac450a70e60f1eb72d08d295b001fe3744ab2ce6aba51c50`  
		Last Modified: Fri, 12 Jun 2020 18:58:52 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2724d7dec4121bbe85b94aa2443356afd739e9b04e6adfc6f42b6b6e905a95f7`  
		Last Modified: Fri, 12 Jun 2020 18:59:19 GMT  
		Size: 86.0 MB (85958453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c46e43e925893ef88759184e58a70d17f45392e6524dfddf0d68becb6077b9`  
		Last Modified: Fri, 12 Jun 2020 18:58:52 GMT  
		Size: 4.9 KB (4851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d77187f1fde12afc91b5b14093343ab71bc1d97ed7e79c60e4722d5c39ea0ca`  
		Last Modified: Fri, 12 Jun 2020 18:58:53 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.13` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a1705f7fecaefda698c2cf024327bca91cb8f66f2103614ae4d050f3ae194a4e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133498155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d3057995bde70b21d4b3cf61e8df037115877ab7f95cdf5326e78e3c2020c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:56:35 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:56:46 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:57:04 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 19:02:53 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 19:03:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 19:03:18 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 19:03:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 19:03:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 19:04:08 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 19:04:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03b359a03f81831c2fd57d9416ebc819388fd8574d85ad8898645d72f66c3c7`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09607cc66ed45e59b9ecfd2ed2dde55ce5b8e9b80729c7e1e9afa3c8d8e417ec`  
		Last Modified: Fri, 12 Jun 2020 19:14:23 GMT  
		Size: 91.0 MB (90987667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4bd398a89880ad4c07dbeb3afa3e02a724fbc012f4713549758f5ea6f58a11`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dfb689374ca4c43f6019d271c2cd0aa592a343710516129428cebb3c3cb9e3`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.13-focal`

```console
$ docker pull mariadb@sha256:3ce8368efbf25059a1b7d2ff1df9f1cdb52fcd272eb2b906599e8613971379bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.13-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:b0fe725e9008b651ee0577383887728879986580d1e0a809dc263a04d1c40907
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123544564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41c9d63e23e3408f9615c5519ef1a540874e867460268af29993862155376a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:25:03 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:25:22 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:25:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:25:23 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:25:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:25:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:25:24 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:25:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d075a6a30ab84cd85dbfe7ff6b7ff4b1da51420bb6502fbbcd165a6362314d89`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d12c1b8c73e8aaa38978b59b62c4a6d88faaf072f8dd8170cc20c995ea6182`  
		Last Modified: Fri, 12 Jun 2020 18:27:01 GMT  
		Size: 86.9 MB (86868588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10938405ff505cbefc2abf93e72607642d6d13d611bf1df914c7ccc62f2010fa`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 4.9 KB (4851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3656315d96d9326a97929d688679e34d594759499e9f6e6652ce44a70d285c64`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.13-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:8c7b8ef0282a747aa0e686f5c2d3b68f050f8d5aebc51884681057f3d6bab5af
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121139407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227094abd47e39aba82a11a0d4aff3492e3733207529c4fb90f4d1fa8299d10c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 00:18:16 GMT
ADD file:e9947aff2dfa8f220d4b25dc0770aff8d9ffc08482e52f54833f39e1c3ec08bf in / 
# Fri, 24 Apr 2020 00:18:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 00:18:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:18:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:18:29 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:53:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:53:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:53:46 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:54:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:54:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:54:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:54:14 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:54:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:55:26 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:55:26 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:55:28 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:56:18 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:56:20 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:56:21 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:56:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:56:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:56:24 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:56:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c2d76ba33f8d52087147ce28d8f03c08f69677591e3e10db810bf76a6e09427`  
		Last Modified: Fri, 24 Apr 2020 00:22:00 GMT  
		Size: 27.2 MB (27158644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92d4cfc71d3821474946021fdbf241a74992a84c6269c3e9a052ce7fc56cece`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 32.3 KB (32326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63063bfe137200b3c8d1ee8d819124352c20ee8c189a0388f461ec66bb759310`  
		Last Modified: Fri, 24 Apr 2020 00:21:53 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38385900086ffa7d7cb9c3bbeabaf2176d7d7958ebf0736d2a01773a830201ee`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0959e86d4d132b0e91456f1d1ecc3b1d6518d720b7ee82926559fd34800d7b53`  
		Last Modified: Fri, 12 Jun 2020 18:58:18 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f37953089cdddf8b409b61f0f30de595d96483dd0ce38463384dd5d201b70f`  
		Last Modified: Fri, 12 Jun 2020 18:58:19 GMT  
		Size: 5.5 MB (5456917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab7a5713dbb2830a805d0b68dae96ce4dd827b086473a3d785f76b37d885fe1`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 1.3 MB (1258973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0614221a0d602714b38672c572d4071df43a41223dab9b1c81ab45ea5bc9c9`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e232435757d992d57a40890acb9528958726ef62b7f400e4ef7c3b7d97c234c`  
		Last Modified: Fri, 12 Jun 2020 18:58:16 GMT  
		Size: 1.3 MB (1263367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb430a3947464ff3d178d412e9047e4b67e2cc3a09923dd4b84596fa57403d66`  
		Last Modified: Fri, 12 Jun 2020 18:58:15 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c366377b87f5bd2fac450a70e60f1eb72d08d295b001fe3744ab2ce6aba51c50`  
		Last Modified: Fri, 12 Jun 2020 18:58:52 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2724d7dec4121bbe85b94aa2443356afd739e9b04e6adfc6f42b6b6e905a95f7`  
		Last Modified: Fri, 12 Jun 2020 18:59:19 GMT  
		Size: 86.0 MB (85958453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c46e43e925893ef88759184e58a70d17f45392e6524dfddf0d68becb6077b9`  
		Last Modified: Fri, 12 Jun 2020 18:58:52 GMT  
		Size: 4.9 KB (4851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d77187f1fde12afc91b5b14093343ab71bc1d97ed7e79c60e4722d5c39ea0ca`  
		Last Modified: Fri, 12 Jun 2020 18:58:53 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.13-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a1705f7fecaefda698c2cf024327bca91cb8f66f2103614ae4d050f3ae194a4e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133498155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d3057995bde70b21d4b3cf61e8df037115877ab7f95cdf5326e78e3c2020c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:56:35 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:56:46 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:57:04 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 19:02:53 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 19:03:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 19:03:18 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 19:03:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 19:03:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 19:04:08 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 19:04:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03b359a03f81831c2fd57d9416ebc819388fd8574d85ad8898645d72f66c3c7`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09607cc66ed45e59b9ecfd2ed2dde55ce5b8e9b80729c7e1e9afa3c8d8e417ec`  
		Last Modified: Fri, 12 Jun 2020 19:14:23 GMT  
		Size: 91.0 MB (90987667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4bd398a89880ad4c07dbeb3afa3e02a724fbc012f4713549758f5ea6f58a11`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dfb689374ca4c43f6019d271c2cd0aa592a343710516129428cebb3c3cb9e3`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4-focal`

```console
$ docker pull mariadb@sha256:3ce8368efbf25059a1b7d2ff1df9f1cdb52fcd272eb2b906599e8613971379bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:b0fe725e9008b651ee0577383887728879986580d1e0a809dc263a04d1c40907
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123544564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41c9d63e23e3408f9615c5519ef1a540874e867460268af29993862155376a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:25:03 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:25:22 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:25:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:25:23 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:25:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:25:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:25:24 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:25:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d075a6a30ab84cd85dbfe7ff6b7ff4b1da51420bb6502fbbcd165a6362314d89`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d12c1b8c73e8aaa38978b59b62c4a6d88faaf072f8dd8170cc20c995ea6182`  
		Last Modified: Fri, 12 Jun 2020 18:27:01 GMT  
		Size: 86.9 MB (86868588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10938405ff505cbefc2abf93e72607642d6d13d611bf1df914c7ccc62f2010fa`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 4.9 KB (4851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3656315d96d9326a97929d688679e34d594759499e9f6e6652ce44a70d285c64`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:8c7b8ef0282a747aa0e686f5c2d3b68f050f8d5aebc51884681057f3d6bab5af
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121139407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227094abd47e39aba82a11a0d4aff3492e3733207529c4fb90f4d1fa8299d10c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 00:18:16 GMT
ADD file:e9947aff2dfa8f220d4b25dc0770aff8d9ffc08482e52f54833f39e1c3ec08bf in / 
# Fri, 24 Apr 2020 00:18:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 00:18:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:18:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:18:29 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:53:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:53:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:53:46 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:54:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:54:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:54:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:54:14 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:54:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:55:26 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:55:26 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:55:28 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:56:18 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:56:20 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:56:21 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:56:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:56:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:56:24 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:56:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c2d76ba33f8d52087147ce28d8f03c08f69677591e3e10db810bf76a6e09427`  
		Last Modified: Fri, 24 Apr 2020 00:22:00 GMT  
		Size: 27.2 MB (27158644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92d4cfc71d3821474946021fdbf241a74992a84c6269c3e9a052ce7fc56cece`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 32.3 KB (32326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63063bfe137200b3c8d1ee8d819124352c20ee8c189a0388f461ec66bb759310`  
		Last Modified: Fri, 24 Apr 2020 00:21:53 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38385900086ffa7d7cb9c3bbeabaf2176d7d7958ebf0736d2a01773a830201ee`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0959e86d4d132b0e91456f1d1ecc3b1d6518d720b7ee82926559fd34800d7b53`  
		Last Modified: Fri, 12 Jun 2020 18:58:18 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f37953089cdddf8b409b61f0f30de595d96483dd0ce38463384dd5d201b70f`  
		Last Modified: Fri, 12 Jun 2020 18:58:19 GMT  
		Size: 5.5 MB (5456917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab7a5713dbb2830a805d0b68dae96ce4dd827b086473a3d785f76b37d885fe1`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 1.3 MB (1258973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0614221a0d602714b38672c572d4071df43a41223dab9b1c81ab45ea5bc9c9`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e232435757d992d57a40890acb9528958726ef62b7f400e4ef7c3b7d97c234c`  
		Last Modified: Fri, 12 Jun 2020 18:58:16 GMT  
		Size: 1.3 MB (1263367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb430a3947464ff3d178d412e9047e4b67e2cc3a09923dd4b84596fa57403d66`  
		Last Modified: Fri, 12 Jun 2020 18:58:15 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c366377b87f5bd2fac450a70e60f1eb72d08d295b001fe3744ab2ce6aba51c50`  
		Last Modified: Fri, 12 Jun 2020 18:58:52 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2724d7dec4121bbe85b94aa2443356afd739e9b04e6adfc6f42b6b6e905a95f7`  
		Last Modified: Fri, 12 Jun 2020 18:59:19 GMT  
		Size: 86.0 MB (85958453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c46e43e925893ef88759184e58a70d17f45392e6524dfddf0d68becb6077b9`  
		Last Modified: Fri, 12 Jun 2020 18:58:52 GMT  
		Size: 4.9 KB (4851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d77187f1fde12afc91b5b14093343ab71bc1d97ed7e79c60e4722d5c39ea0ca`  
		Last Modified: Fri, 12 Jun 2020 18:58:53 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a1705f7fecaefda698c2cf024327bca91cb8f66f2103614ae4d050f3ae194a4e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133498155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d3057995bde70b21d4b3cf61e8df037115877ab7f95cdf5326e78e3c2020c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:56:35 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:56:46 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:57:04 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 19:02:53 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 19:03:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 19:03:18 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 19:03:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 19:03:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 19:04:08 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 19:04:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03b359a03f81831c2fd57d9416ebc819388fd8574d85ad8898645d72f66c3c7`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09607cc66ed45e59b9ecfd2ed2dde55ce5b8e9b80729c7e1e9afa3c8d8e417ec`  
		Last Modified: Fri, 12 Jun 2020 19:14:23 GMT  
		Size: 91.0 MB (90987667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4bd398a89880ad4c07dbeb3afa3e02a724fbc012f4713549758f5ea6f58a11`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dfb689374ca4c43f6019d271c2cd0aa592a343710516129428cebb3c3cb9e3`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5`

```console
$ docker pull mariadb@sha256:eec0568c86675b6d233f9e56b71e0a53306b7652df20b31e655e98cd55acdeb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5` - linux; amd64

```console
$ docker pull mariadb@sha256:1c43c2c9a9cbc8d6d917b3baccc746029611401140afacbc341f9e0543f693d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125468046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d666ead09d0cdb6b38628b20884b7a034975d73e0c72bf72af995bf25b32ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:24:12 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 12 Jun 2020 18:24:12 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Fri, 12 Jun 2020 18:24:13 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:24:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:24:45 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:24:45 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:24:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:24:46 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:24:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2a69879e3e44e2c33e196212dc1e1f81aa3f8a2f150e64ba2be5415cebf05f`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3434e5ff172ae3f9a2ebac367af66daecf7e55fb5d24d1202cc34d1a680d5a`  
		Last Modified: Fri, 12 Jun 2020 18:26:37 GMT  
		Size: 88.8 MB (88792188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9318b4b2608af288b8a860c61f31daa1e48322b0a4d0588a94e1ae7269bb89a9`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:a5634fa0b151ea9b814b46fa01c24e79020cc778431c75ca984b86128d07a336
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (122997696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc94523ed8e1f81f5c414f6b5f9e562d1ee6476c06c55e41d88dfecf0035ac55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 00:18:16 GMT
ADD file:e9947aff2dfa8f220d4b25dc0770aff8d9ffc08482e52f54833f39e1c3ec08bf in / 
# Fri, 24 Apr 2020 00:18:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 00:18:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:18:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:18:29 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:53:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:53:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:53:46 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:54:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:54:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:54:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:54:14 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:54:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:54:17 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 12 Jun 2020 18:54:18 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Fri, 12 Jun 2020 18:54:20 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:55:07 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:55:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:55:10 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:55:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:55:11 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:55:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c2d76ba33f8d52087147ce28d8f03c08f69677591e3e10db810bf76a6e09427`  
		Last Modified: Fri, 24 Apr 2020 00:22:00 GMT  
		Size: 27.2 MB (27158644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92d4cfc71d3821474946021fdbf241a74992a84c6269c3e9a052ce7fc56cece`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 32.3 KB (32326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63063bfe137200b3c8d1ee8d819124352c20ee8c189a0388f461ec66bb759310`  
		Last Modified: Fri, 24 Apr 2020 00:21:53 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38385900086ffa7d7cb9c3bbeabaf2176d7d7958ebf0736d2a01773a830201ee`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0959e86d4d132b0e91456f1d1ecc3b1d6518d720b7ee82926559fd34800d7b53`  
		Last Modified: Fri, 12 Jun 2020 18:58:18 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f37953089cdddf8b409b61f0f30de595d96483dd0ce38463384dd5d201b70f`  
		Last Modified: Fri, 12 Jun 2020 18:58:19 GMT  
		Size: 5.5 MB (5456917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab7a5713dbb2830a805d0b68dae96ce4dd827b086473a3d785f76b37d885fe1`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 1.3 MB (1258973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0614221a0d602714b38672c572d4071df43a41223dab9b1c81ab45ea5bc9c9`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e232435757d992d57a40890acb9528958726ef62b7f400e4ef7c3b7d97c234c`  
		Last Modified: Fri, 12 Jun 2020 18:58:16 GMT  
		Size: 1.3 MB (1263367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb430a3947464ff3d178d412e9047e4b67e2cc3a09923dd4b84596fa57403d66`  
		Last Modified: Fri, 12 Jun 2020 18:58:15 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f581713dad871dd1e951c6f9dae24eb128f99423677031f7b995e5d0e5afd2`  
		Last Modified: Fri, 12 Jun 2020 18:58:15 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e73fa8d9c1238f2fb5bdc8c15aa0f1f818cd4d08be1762d677bc650a6765903`  
		Last Modified: Fri, 12 Jun 2020 18:58:41 GMT  
		Size: 87.8 MB (87816861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e23804dfe7361c4d8bb4fdd1b89013bd168ba1669961992b16e8516bacccbd0`  
		Last Modified: Fri, 12 Jun 2020 18:58:16 GMT  
		Size: 4.9 KB (4853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; ppc64le

```console
$ docker pull mariadb@sha256:7f3c6e4fbe1d904fe0f1daf0b28dd7b6055906d0e4ef545e0f167305737edfb3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135491752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4482a6d35ab27dc6622588f472d707755fd0242ccf076f18f56b764f32d2f56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:49:25 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 12 Jun 2020 18:49:36 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Fri, 12 Jun 2020 18:50:14 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:55:32 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:55:52 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:55:58 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:56:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:56:12 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:56:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907c120bad3d45c4179d4a0c2dcde4937f90d39332c52fb866de70e4b7634460`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5768c1a14ad9b899134606bad0b1bf95337891f65101e352d91fe125d74a1e7`  
		Last Modified: Fri, 12 Jun 2020 19:13:37 GMT  
		Size: 93.0 MB (92981382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9e462c378a4b7787721cd8cb5720e89d8e9696d398174bb7b4d6d60bacfada`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 4.9 KB (4855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.3`

```console
$ docker pull mariadb@sha256:eec0568c86675b6d233f9e56b71e0a53306b7652df20b31e655e98cd55acdeb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5.3` - linux; amd64

```console
$ docker pull mariadb@sha256:1c43c2c9a9cbc8d6d917b3baccc746029611401140afacbc341f9e0543f693d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125468046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d666ead09d0cdb6b38628b20884b7a034975d73e0c72bf72af995bf25b32ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:24:12 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 12 Jun 2020 18:24:12 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Fri, 12 Jun 2020 18:24:13 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:24:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:24:45 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:24:45 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:24:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:24:46 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:24:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2a69879e3e44e2c33e196212dc1e1f81aa3f8a2f150e64ba2be5415cebf05f`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3434e5ff172ae3f9a2ebac367af66daecf7e55fb5d24d1202cc34d1a680d5a`  
		Last Modified: Fri, 12 Jun 2020 18:26:37 GMT  
		Size: 88.8 MB (88792188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9318b4b2608af288b8a860c61f31daa1e48322b0a4d0588a94e1ae7269bb89a9`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.3` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:a5634fa0b151ea9b814b46fa01c24e79020cc778431c75ca984b86128d07a336
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (122997696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc94523ed8e1f81f5c414f6b5f9e562d1ee6476c06c55e41d88dfecf0035ac55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 00:18:16 GMT
ADD file:e9947aff2dfa8f220d4b25dc0770aff8d9ffc08482e52f54833f39e1c3ec08bf in / 
# Fri, 24 Apr 2020 00:18:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 00:18:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:18:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:18:29 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:53:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:53:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:53:46 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:54:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:54:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:54:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:54:14 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:54:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:54:17 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 12 Jun 2020 18:54:18 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Fri, 12 Jun 2020 18:54:20 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:55:07 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:55:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:55:10 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:55:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:55:11 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:55:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c2d76ba33f8d52087147ce28d8f03c08f69677591e3e10db810bf76a6e09427`  
		Last Modified: Fri, 24 Apr 2020 00:22:00 GMT  
		Size: 27.2 MB (27158644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92d4cfc71d3821474946021fdbf241a74992a84c6269c3e9a052ce7fc56cece`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 32.3 KB (32326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63063bfe137200b3c8d1ee8d819124352c20ee8c189a0388f461ec66bb759310`  
		Last Modified: Fri, 24 Apr 2020 00:21:53 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38385900086ffa7d7cb9c3bbeabaf2176d7d7958ebf0736d2a01773a830201ee`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0959e86d4d132b0e91456f1d1ecc3b1d6518d720b7ee82926559fd34800d7b53`  
		Last Modified: Fri, 12 Jun 2020 18:58:18 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f37953089cdddf8b409b61f0f30de595d96483dd0ce38463384dd5d201b70f`  
		Last Modified: Fri, 12 Jun 2020 18:58:19 GMT  
		Size: 5.5 MB (5456917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab7a5713dbb2830a805d0b68dae96ce4dd827b086473a3d785f76b37d885fe1`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 1.3 MB (1258973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0614221a0d602714b38672c572d4071df43a41223dab9b1c81ab45ea5bc9c9`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e232435757d992d57a40890acb9528958726ef62b7f400e4ef7c3b7d97c234c`  
		Last Modified: Fri, 12 Jun 2020 18:58:16 GMT  
		Size: 1.3 MB (1263367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb430a3947464ff3d178d412e9047e4b67e2cc3a09923dd4b84596fa57403d66`  
		Last Modified: Fri, 12 Jun 2020 18:58:15 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f581713dad871dd1e951c6f9dae24eb128f99423677031f7b995e5d0e5afd2`  
		Last Modified: Fri, 12 Jun 2020 18:58:15 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e73fa8d9c1238f2fb5bdc8c15aa0f1f818cd4d08be1762d677bc650a6765903`  
		Last Modified: Fri, 12 Jun 2020 18:58:41 GMT  
		Size: 87.8 MB (87816861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e23804dfe7361c4d8bb4fdd1b89013bd168ba1669961992b16e8516bacccbd0`  
		Last Modified: Fri, 12 Jun 2020 18:58:16 GMT  
		Size: 4.9 KB (4853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.3` - linux; ppc64le

```console
$ docker pull mariadb@sha256:7f3c6e4fbe1d904fe0f1daf0b28dd7b6055906d0e4ef545e0f167305737edfb3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135491752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4482a6d35ab27dc6622588f472d707755fd0242ccf076f18f56b764f32d2f56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:49:25 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 12 Jun 2020 18:49:36 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Fri, 12 Jun 2020 18:50:14 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:55:32 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:55:52 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:55:58 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:56:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:56:12 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:56:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907c120bad3d45c4179d4a0c2dcde4937f90d39332c52fb866de70e4b7634460`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5768c1a14ad9b899134606bad0b1bf95337891f65101e352d91fe125d74a1e7`  
		Last Modified: Fri, 12 Jun 2020 19:13:37 GMT  
		Size: 93.0 MB (92981382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9e462c378a4b7787721cd8cb5720e89d8e9696d398174bb7b4d6d60bacfada`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 4.9 KB (4855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.3-focal`

```console
$ docker pull mariadb@sha256:eec0568c86675b6d233f9e56b71e0a53306b7652df20b31e655e98cd55acdeb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5.3-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:1c43c2c9a9cbc8d6d917b3baccc746029611401140afacbc341f9e0543f693d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125468046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d666ead09d0cdb6b38628b20884b7a034975d73e0c72bf72af995bf25b32ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:24:12 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 12 Jun 2020 18:24:12 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Fri, 12 Jun 2020 18:24:13 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:24:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:24:45 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:24:45 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:24:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:24:46 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:24:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2a69879e3e44e2c33e196212dc1e1f81aa3f8a2f150e64ba2be5415cebf05f`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3434e5ff172ae3f9a2ebac367af66daecf7e55fb5d24d1202cc34d1a680d5a`  
		Last Modified: Fri, 12 Jun 2020 18:26:37 GMT  
		Size: 88.8 MB (88792188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9318b4b2608af288b8a860c61f31daa1e48322b0a4d0588a94e1ae7269bb89a9`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.3-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:a5634fa0b151ea9b814b46fa01c24e79020cc778431c75ca984b86128d07a336
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (122997696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc94523ed8e1f81f5c414f6b5f9e562d1ee6476c06c55e41d88dfecf0035ac55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 00:18:16 GMT
ADD file:e9947aff2dfa8f220d4b25dc0770aff8d9ffc08482e52f54833f39e1c3ec08bf in / 
# Fri, 24 Apr 2020 00:18:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 00:18:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:18:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:18:29 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:53:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:53:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:53:46 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:54:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:54:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:54:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:54:14 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:54:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:54:17 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 12 Jun 2020 18:54:18 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Fri, 12 Jun 2020 18:54:20 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:55:07 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:55:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:55:10 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:55:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:55:11 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:55:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c2d76ba33f8d52087147ce28d8f03c08f69677591e3e10db810bf76a6e09427`  
		Last Modified: Fri, 24 Apr 2020 00:22:00 GMT  
		Size: 27.2 MB (27158644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92d4cfc71d3821474946021fdbf241a74992a84c6269c3e9a052ce7fc56cece`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 32.3 KB (32326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63063bfe137200b3c8d1ee8d819124352c20ee8c189a0388f461ec66bb759310`  
		Last Modified: Fri, 24 Apr 2020 00:21:53 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38385900086ffa7d7cb9c3bbeabaf2176d7d7958ebf0736d2a01773a830201ee`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0959e86d4d132b0e91456f1d1ecc3b1d6518d720b7ee82926559fd34800d7b53`  
		Last Modified: Fri, 12 Jun 2020 18:58:18 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f37953089cdddf8b409b61f0f30de595d96483dd0ce38463384dd5d201b70f`  
		Last Modified: Fri, 12 Jun 2020 18:58:19 GMT  
		Size: 5.5 MB (5456917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab7a5713dbb2830a805d0b68dae96ce4dd827b086473a3d785f76b37d885fe1`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 1.3 MB (1258973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0614221a0d602714b38672c572d4071df43a41223dab9b1c81ab45ea5bc9c9`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e232435757d992d57a40890acb9528958726ef62b7f400e4ef7c3b7d97c234c`  
		Last Modified: Fri, 12 Jun 2020 18:58:16 GMT  
		Size: 1.3 MB (1263367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb430a3947464ff3d178d412e9047e4b67e2cc3a09923dd4b84596fa57403d66`  
		Last Modified: Fri, 12 Jun 2020 18:58:15 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f581713dad871dd1e951c6f9dae24eb128f99423677031f7b995e5d0e5afd2`  
		Last Modified: Fri, 12 Jun 2020 18:58:15 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e73fa8d9c1238f2fb5bdc8c15aa0f1f818cd4d08be1762d677bc650a6765903`  
		Last Modified: Fri, 12 Jun 2020 18:58:41 GMT  
		Size: 87.8 MB (87816861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e23804dfe7361c4d8bb4fdd1b89013bd168ba1669961992b16e8516bacccbd0`  
		Last Modified: Fri, 12 Jun 2020 18:58:16 GMT  
		Size: 4.9 KB (4853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.3-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:7f3c6e4fbe1d904fe0f1daf0b28dd7b6055906d0e4ef545e0f167305737edfb3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135491752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4482a6d35ab27dc6622588f472d707755fd0242ccf076f18f56b764f32d2f56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:49:25 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 12 Jun 2020 18:49:36 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Fri, 12 Jun 2020 18:50:14 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:55:32 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:55:52 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:55:58 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:56:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:56:12 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:56:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907c120bad3d45c4179d4a0c2dcde4937f90d39332c52fb866de70e4b7634460`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5768c1a14ad9b899134606bad0b1bf95337891f65101e352d91fe125d74a1e7`  
		Last Modified: Fri, 12 Jun 2020 19:13:37 GMT  
		Size: 93.0 MB (92981382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9e462c378a4b7787721cd8cb5720e89d8e9696d398174bb7b4d6d60bacfada`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 4.9 KB (4855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5-focal`

```console
$ docker pull mariadb@sha256:eec0568c86675b6d233f9e56b71e0a53306b7652df20b31e655e98cd55acdeb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:1c43c2c9a9cbc8d6d917b3baccc746029611401140afacbc341f9e0543f693d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125468046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d666ead09d0cdb6b38628b20884b7a034975d73e0c72bf72af995bf25b32ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:24:12 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 12 Jun 2020 18:24:12 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Fri, 12 Jun 2020 18:24:13 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:24:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:24:45 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:24:45 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:24:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:24:46 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:24:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2a69879e3e44e2c33e196212dc1e1f81aa3f8a2f150e64ba2be5415cebf05f`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3434e5ff172ae3f9a2ebac367af66daecf7e55fb5d24d1202cc34d1a680d5a`  
		Last Modified: Fri, 12 Jun 2020 18:26:37 GMT  
		Size: 88.8 MB (88792188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9318b4b2608af288b8a860c61f31daa1e48322b0a4d0588a94e1ae7269bb89a9`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:a5634fa0b151ea9b814b46fa01c24e79020cc778431c75ca984b86128d07a336
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (122997696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc94523ed8e1f81f5c414f6b5f9e562d1ee6476c06c55e41d88dfecf0035ac55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 00:18:16 GMT
ADD file:e9947aff2dfa8f220d4b25dc0770aff8d9ffc08482e52f54833f39e1c3ec08bf in / 
# Fri, 24 Apr 2020 00:18:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 00:18:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:18:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:18:29 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:53:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:53:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:53:46 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:54:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:54:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:54:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:54:14 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:54:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:54:17 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 12 Jun 2020 18:54:18 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Fri, 12 Jun 2020 18:54:20 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:55:07 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:55:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:55:10 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:55:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:55:11 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:55:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c2d76ba33f8d52087147ce28d8f03c08f69677591e3e10db810bf76a6e09427`  
		Last Modified: Fri, 24 Apr 2020 00:22:00 GMT  
		Size: 27.2 MB (27158644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92d4cfc71d3821474946021fdbf241a74992a84c6269c3e9a052ce7fc56cece`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 32.3 KB (32326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63063bfe137200b3c8d1ee8d819124352c20ee8c189a0388f461ec66bb759310`  
		Last Modified: Fri, 24 Apr 2020 00:21:53 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38385900086ffa7d7cb9c3bbeabaf2176d7d7958ebf0736d2a01773a830201ee`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0959e86d4d132b0e91456f1d1ecc3b1d6518d720b7ee82926559fd34800d7b53`  
		Last Modified: Fri, 12 Jun 2020 18:58:18 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f37953089cdddf8b409b61f0f30de595d96483dd0ce38463384dd5d201b70f`  
		Last Modified: Fri, 12 Jun 2020 18:58:19 GMT  
		Size: 5.5 MB (5456917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab7a5713dbb2830a805d0b68dae96ce4dd827b086473a3d785f76b37d885fe1`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 1.3 MB (1258973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0614221a0d602714b38672c572d4071df43a41223dab9b1c81ab45ea5bc9c9`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e232435757d992d57a40890acb9528958726ef62b7f400e4ef7c3b7d97c234c`  
		Last Modified: Fri, 12 Jun 2020 18:58:16 GMT  
		Size: 1.3 MB (1263367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb430a3947464ff3d178d412e9047e4b67e2cc3a09923dd4b84596fa57403d66`  
		Last Modified: Fri, 12 Jun 2020 18:58:15 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f581713dad871dd1e951c6f9dae24eb128f99423677031f7b995e5d0e5afd2`  
		Last Modified: Fri, 12 Jun 2020 18:58:15 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e73fa8d9c1238f2fb5bdc8c15aa0f1f818cd4d08be1762d677bc650a6765903`  
		Last Modified: Fri, 12 Jun 2020 18:58:41 GMT  
		Size: 87.8 MB (87816861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e23804dfe7361c4d8bb4fdd1b89013bd168ba1669961992b16e8516bacccbd0`  
		Last Modified: Fri, 12 Jun 2020 18:58:16 GMT  
		Size: 4.9 KB (4853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:7f3c6e4fbe1d904fe0f1daf0b28dd7b6055906d0e4ef545e0f167305737edfb3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135491752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4482a6d35ab27dc6622588f472d707755fd0242ccf076f18f56b764f32d2f56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:49:25 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 12 Jun 2020 18:49:36 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Fri, 12 Jun 2020 18:50:14 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:55:32 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:55:52 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:55:58 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:56:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:56:12 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:56:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907c120bad3d45c4179d4a0c2dcde4937f90d39332c52fb866de70e4b7634460`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5768c1a14ad9b899134606bad0b1bf95337891f65101e352d91fe125d74a1e7`  
		Last Modified: Fri, 12 Jun 2020 19:13:37 GMT  
		Size: 93.0 MB (92981382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9e462c378a4b7787721cd8cb5720e89d8e9696d398174bb7b4d6d60bacfada`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 4.9 KB (4855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10-focal`

```console
$ docker pull mariadb@sha256:3ce8368efbf25059a1b7d2ff1df9f1cdb52fcd272eb2b906599e8613971379bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:b0fe725e9008b651ee0577383887728879986580d1e0a809dc263a04d1c40907
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123544564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41c9d63e23e3408f9615c5519ef1a540874e867460268af29993862155376a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:25:03 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:25:22 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:25:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:25:23 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:25:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:25:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:25:24 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:25:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d075a6a30ab84cd85dbfe7ff6b7ff4b1da51420bb6502fbbcd165a6362314d89`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d12c1b8c73e8aaa38978b59b62c4a6d88faaf072f8dd8170cc20c995ea6182`  
		Last Modified: Fri, 12 Jun 2020 18:27:01 GMT  
		Size: 86.9 MB (86868588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10938405ff505cbefc2abf93e72607642d6d13d611bf1df914c7ccc62f2010fa`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 4.9 KB (4851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3656315d96d9326a97929d688679e34d594759499e9f6e6652ce44a70d285c64`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:8c7b8ef0282a747aa0e686f5c2d3b68f050f8d5aebc51884681057f3d6bab5af
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121139407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227094abd47e39aba82a11a0d4aff3492e3733207529c4fb90f4d1fa8299d10c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 00:18:16 GMT
ADD file:e9947aff2dfa8f220d4b25dc0770aff8d9ffc08482e52f54833f39e1c3ec08bf in / 
# Fri, 24 Apr 2020 00:18:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 00:18:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:18:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:18:29 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:53:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:53:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:53:46 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:54:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:54:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:54:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:54:14 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:54:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:55:26 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:55:26 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:55:28 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:56:18 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:56:20 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:56:21 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:56:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:56:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:56:24 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:56:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c2d76ba33f8d52087147ce28d8f03c08f69677591e3e10db810bf76a6e09427`  
		Last Modified: Fri, 24 Apr 2020 00:22:00 GMT  
		Size: 27.2 MB (27158644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92d4cfc71d3821474946021fdbf241a74992a84c6269c3e9a052ce7fc56cece`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 32.3 KB (32326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63063bfe137200b3c8d1ee8d819124352c20ee8c189a0388f461ec66bb759310`  
		Last Modified: Fri, 24 Apr 2020 00:21:53 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38385900086ffa7d7cb9c3bbeabaf2176d7d7958ebf0736d2a01773a830201ee`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0959e86d4d132b0e91456f1d1ecc3b1d6518d720b7ee82926559fd34800d7b53`  
		Last Modified: Fri, 12 Jun 2020 18:58:18 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f37953089cdddf8b409b61f0f30de595d96483dd0ce38463384dd5d201b70f`  
		Last Modified: Fri, 12 Jun 2020 18:58:19 GMT  
		Size: 5.5 MB (5456917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab7a5713dbb2830a805d0b68dae96ce4dd827b086473a3d785f76b37d885fe1`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 1.3 MB (1258973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0614221a0d602714b38672c572d4071df43a41223dab9b1c81ab45ea5bc9c9`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e232435757d992d57a40890acb9528958726ef62b7f400e4ef7c3b7d97c234c`  
		Last Modified: Fri, 12 Jun 2020 18:58:16 GMT  
		Size: 1.3 MB (1263367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb430a3947464ff3d178d412e9047e4b67e2cc3a09923dd4b84596fa57403d66`  
		Last Modified: Fri, 12 Jun 2020 18:58:15 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c366377b87f5bd2fac450a70e60f1eb72d08d295b001fe3744ab2ce6aba51c50`  
		Last Modified: Fri, 12 Jun 2020 18:58:52 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2724d7dec4121bbe85b94aa2443356afd739e9b04e6adfc6f42b6b6e905a95f7`  
		Last Modified: Fri, 12 Jun 2020 18:59:19 GMT  
		Size: 86.0 MB (85958453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c46e43e925893ef88759184e58a70d17f45392e6524dfddf0d68becb6077b9`  
		Last Modified: Fri, 12 Jun 2020 18:58:52 GMT  
		Size: 4.9 KB (4851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d77187f1fde12afc91b5b14093343ab71bc1d97ed7e79c60e4722d5c39ea0ca`  
		Last Modified: Fri, 12 Jun 2020 18:58:53 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a1705f7fecaefda698c2cf024327bca91cb8f66f2103614ae4d050f3ae194a4e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133498155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d3057995bde70b21d4b3cf61e8df037115877ab7f95cdf5326e78e3c2020c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:56:35 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:56:46 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:57:04 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 19:02:53 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 19:03:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 19:03:18 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 19:03:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 19:03:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 19:04:08 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 19:04:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03b359a03f81831c2fd57d9416ebc819388fd8574d85ad8898645d72f66c3c7`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09607cc66ed45e59b9ecfd2ed2dde55ce5b8e9b80729c7e1e9afa3c8d8e417ec`  
		Last Modified: Fri, 12 Jun 2020 19:14:23 GMT  
		Size: 91.0 MB (90987667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4bd398a89880ad4c07dbeb3afa3e02a724fbc012f4713549758f5ea6f58a11`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dfb689374ca4c43f6019d271c2cd0aa592a343710516129428cebb3c3cb9e3`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:focal`

```console
$ docker pull mariadb@sha256:3ce8368efbf25059a1b7d2ff1df9f1cdb52fcd272eb2b906599e8613971379bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:focal` - linux; amd64

```console
$ docker pull mariadb@sha256:b0fe725e9008b651ee0577383887728879986580d1e0a809dc263a04d1c40907
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123544564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41c9d63e23e3408f9615c5519ef1a540874e867460268af29993862155376a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:25:03 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:25:22 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:25:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:25:23 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:25:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:25:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:25:24 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:25:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d075a6a30ab84cd85dbfe7ff6b7ff4b1da51420bb6502fbbcd165a6362314d89`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d12c1b8c73e8aaa38978b59b62c4a6d88faaf072f8dd8170cc20c995ea6182`  
		Last Modified: Fri, 12 Jun 2020 18:27:01 GMT  
		Size: 86.9 MB (86868588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10938405ff505cbefc2abf93e72607642d6d13d611bf1df914c7ccc62f2010fa`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 4.9 KB (4851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3656315d96d9326a97929d688679e34d594759499e9f6e6652ce44a70d285c64`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:8c7b8ef0282a747aa0e686f5c2d3b68f050f8d5aebc51884681057f3d6bab5af
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121139407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227094abd47e39aba82a11a0d4aff3492e3733207529c4fb90f4d1fa8299d10c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 00:18:16 GMT
ADD file:e9947aff2dfa8f220d4b25dc0770aff8d9ffc08482e52f54833f39e1c3ec08bf in / 
# Fri, 24 Apr 2020 00:18:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 00:18:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:18:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:18:29 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:53:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:53:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:53:46 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:54:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:54:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:54:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:54:14 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:54:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:55:26 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:55:26 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:55:28 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:56:18 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:56:20 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:56:21 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:56:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:56:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:56:24 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:56:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c2d76ba33f8d52087147ce28d8f03c08f69677591e3e10db810bf76a6e09427`  
		Last Modified: Fri, 24 Apr 2020 00:22:00 GMT  
		Size: 27.2 MB (27158644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92d4cfc71d3821474946021fdbf241a74992a84c6269c3e9a052ce7fc56cece`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 32.3 KB (32326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63063bfe137200b3c8d1ee8d819124352c20ee8c189a0388f461ec66bb759310`  
		Last Modified: Fri, 24 Apr 2020 00:21:53 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38385900086ffa7d7cb9c3bbeabaf2176d7d7958ebf0736d2a01773a830201ee`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0959e86d4d132b0e91456f1d1ecc3b1d6518d720b7ee82926559fd34800d7b53`  
		Last Modified: Fri, 12 Jun 2020 18:58:18 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f37953089cdddf8b409b61f0f30de595d96483dd0ce38463384dd5d201b70f`  
		Last Modified: Fri, 12 Jun 2020 18:58:19 GMT  
		Size: 5.5 MB (5456917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab7a5713dbb2830a805d0b68dae96ce4dd827b086473a3d785f76b37d885fe1`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 1.3 MB (1258973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0614221a0d602714b38672c572d4071df43a41223dab9b1c81ab45ea5bc9c9`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e232435757d992d57a40890acb9528958726ef62b7f400e4ef7c3b7d97c234c`  
		Last Modified: Fri, 12 Jun 2020 18:58:16 GMT  
		Size: 1.3 MB (1263367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb430a3947464ff3d178d412e9047e4b67e2cc3a09923dd4b84596fa57403d66`  
		Last Modified: Fri, 12 Jun 2020 18:58:15 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c366377b87f5bd2fac450a70e60f1eb72d08d295b001fe3744ab2ce6aba51c50`  
		Last Modified: Fri, 12 Jun 2020 18:58:52 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2724d7dec4121bbe85b94aa2443356afd739e9b04e6adfc6f42b6b6e905a95f7`  
		Last Modified: Fri, 12 Jun 2020 18:59:19 GMT  
		Size: 86.0 MB (85958453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c46e43e925893ef88759184e58a70d17f45392e6524dfddf0d68becb6077b9`  
		Last Modified: Fri, 12 Jun 2020 18:58:52 GMT  
		Size: 4.9 KB (4851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d77187f1fde12afc91b5b14093343ab71bc1d97ed7e79c60e4722d5c39ea0ca`  
		Last Modified: Fri, 12 Jun 2020 18:58:53 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a1705f7fecaefda698c2cf024327bca91cb8f66f2103614ae4d050f3ae194a4e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133498155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d3057995bde70b21d4b3cf61e8df037115877ab7f95cdf5326e78e3c2020c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:56:35 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:56:46 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:57:04 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 19:02:53 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 19:03:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 19:03:18 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 19:03:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 19:03:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 19:04:08 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 19:04:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03b359a03f81831c2fd57d9416ebc819388fd8574d85ad8898645d72f66c3c7`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09607cc66ed45e59b9ecfd2ed2dde55ce5b8e9b80729c7e1e9afa3c8d8e417ec`  
		Last Modified: Fri, 12 Jun 2020 19:14:23 GMT  
		Size: 91.0 MB (90987667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4bd398a89880ad4c07dbeb3afa3e02a724fbc012f4713549758f5ea6f58a11`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dfb689374ca4c43f6019d271c2cd0aa592a343710516129428cebb3c3cb9e3`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:latest`

```console
$ docker pull mariadb@sha256:3ce8368efbf25059a1b7d2ff1df9f1cdb52fcd272eb2b906599e8613971379bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:latest` - linux; amd64

```console
$ docker pull mariadb@sha256:b0fe725e9008b651ee0577383887728879986580d1e0a809dc263a04d1c40907
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123544564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41c9d63e23e3408f9615c5519ef1a540874e867460268af29993862155376a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:25:03 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:25:22 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:25:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:25:23 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:25:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:25:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:25:24 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:25:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d075a6a30ab84cd85dbfe7ff6b7ff4b1da51420bb6502fbbcd165a6362314d89`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d12c1b8c73e8aaa38978b59b62c4a6d88faaf072f8dd8170cc20c995ea6182`  
		Last Modified: Fri, 12 Jun 2020 18:27:01 GMT  
		Size: 86.9 MB (86868588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10938405ff505cbefc2abf93e72607642d6d13d611bf1df914c7ccc62f2010fa`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 4.9 KB (4851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3656315d96d9326a97929d688679e34d594759499e9f6e6652ce44a70d285c64`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:8c7b8ef0282a747aa0e686f5c2d3b68f050f8d5aebc51884681057f3d6bab5af
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121139407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227094abd47e39aba82a11a0d4aff3492e3733207529c4fb90f4d1fa8299d10c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 00:18:16 GMT
ADD file:e9947aff2dfa8f220d4b25dc0770aff8d9ffc08482e52f54833f39e1c3ec08bf in / 
# Fri, 24 Apr 2020 00:18:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 00:18:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:18:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:18:29 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:53:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:53:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:53:46 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:54:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:54:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:54:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:54:14 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:54:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:55:26 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:55:26 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:55:28 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:56:18 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:56:20 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:56:21 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:56:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:56:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:56:24 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:56:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c2d76ba33f8d52087147ce28d8f03c08f69677591e3e10db810bf76a6e09427`  
		Last Modified: Fri, 24 Apr 2020 00:22:00 GMT  
		Size: 27.2 MB (27158644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92d4cfc71d3821474946021fdbf241a74992a84c6269c3e9a052ce7fc56cece`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 32.3 KB (32326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63063bfe137200b3c8d1ee8d819124352c20ee8c189a0388f461ec66bb759310`  
		Last Modified: Fri, 24 Apr 2020 00:21:53 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38385900086ffa7d7cb9c3bbeabaf2176d7d7958ebf0736d2a01773a830201ee`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0959e86d4d132b0e91456f1d1ecc3b1d6518d720b7ee82926559fd34800d7b53`  
		Last Modified: Fri, 12 Jun 2020 18:58:18 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f37953089cdddf8b409b61f0f30de595d96483dd0ce38463384dd5d201b70f`  
		Last Modified: Fri, 12 Jun 2020 18:58:19 GMT  
		Size: 5.5 MB (5456917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab7a5713dbb2830a805d0b68dae96ce4dd827b086473a3d785f76b37d885fe1`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 1.3 MB (1258973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0614221a0d602714b38672c572d4071df43a41223dab9b1c81ab45ea5bc9c9`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e232435757d992d57a40890acb9528958726ef62b7f400e4ef7c3b7d97c234c`  
		Last Modified: Fri, 12 Jun 2020 18:58:16 GMT  
		Size: 1.3 MB (1263367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb430a3947464ff3d178d412e9047e4b67e2cc3a09923dd4b84596fa57403d66`  
		Last Modified: Fri, 12 Jun 2020 18:58:15 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c366377b87f5bd2fac450a70e60f1eb72d08d295b001fe3744ab2ce6aba51c50`  
		Last Modified: Fri, 12 Jun 2020 18:58:52 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2724d7dec4121bbe85b94aa2443356afd739e9b04e6adfc6f42b6b6e905a95f7`  
		Last Modified: Fri, 12 Jun 2020 18:59:19 GMT  
		Size: 86.0 MB (85958453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c46e43e925893ef88759184e58a70d17f45392e6524dfddf0d68becb6077b9`  
		Last Modified: Fri, 12 Jun 2020 18:58:52 GMT  
		Size: 4.9 KB (4851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d77187f1fde12afc91b5b14093343ab71bc1d97ed7e79c60e4722d5c39ea0ca`  
		Last Modified: Fri, 12 Jun 2020 18:58:53 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a1705f7fecaefda698c2cf024327bca91cb8f66f2103614ae4d050f3ae194a4e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133498155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d3057995bde70b21d4b3cf61e8df037115877ab7f95cdf5326e78e3c2020c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:56:35 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:56:46 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:57:04 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 19:02:53 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 19:03:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 19:03:18 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 19:03:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 19:03:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 19:04:08 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 19:04:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03b359a03f81831c2fd57d9416ebc819388fd8574d85ad8898645d72f66c3c7`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09607cc66ed45e59b9ecfd2ed2dde55ce5b8e9b80729c7e1e9afa3c8d8e417ec`  
		Last Modified: Fri, 12 Jun 2020 19:14:23 GMT  
		Size: 91.0 MB (90987667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4bd398a89880ad4c07dbeb3afa3e02a724fbc012f4713549758f5ea6f58a11`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dfb689374ca4c43f6019d271c2cd0aa592a343710516129428cebb3c3cb9e3`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:rc`

```console
$ docker pull mariadb@sha256:eec0568c86675b6d233f9e56b71e0a53306b7652df20b31e655e98cd55acdeb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:rc` - linux; amd64

```console
$ docker pull mariadb@sha256:1c43c2c9a9cbc8d6d917b3baccc746029611401140afacbc341f9e0543f693d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125468046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d666ead09d0cdb6b38628b20884b7a034975d73e0c72bf72af995bf25b32ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:24:12 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 12 Jun 2020 18:24:12 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Fri, 12 Jun 2020 18:24:13 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:24:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:24:45 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:24:45 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:24:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:24:46 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:24:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2a69879e3e44e2c33e196212dc1e1f81aa3f8a2f150e64ba2be5415cebf05f`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3434e5ff172ae3f9a2ebac367af66daecf7e55fb5d24d1202cc34d1a680d5a`  
		Last Modified: Fri, 12 Jun 2020 18:26:37 GMT  
		Size: 88.8 MB (88792188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9318b4b2608af288b8a860c61f31daa1e48322b0a4d0588a94e1ae7269bb89a9`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:rc` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:a5634fa0b151ea9b814b46fa01c24e79020cc778431c75ca984b86128d07a336
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (122997696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc94523ed8e1f81f5c414f6b5f9e562d1ee6476c06c55e41d88dfecf0035ac55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 00:18:16 GMT
ADD file:e9947aff2dfa8f220d4b25dc0770aff8d9ffc08482e52f54833f39e1c3ec08bf in / 
# Fri, 24 Apr 2020 00:18:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 00:18:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:18:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:18:29 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:53:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:53:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:53:46 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:54:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:54:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:54:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:54:14 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:54:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:54:17 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 12 Jun 2020 18:54:18 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Fri, 12 Jun 2020 18:54:20 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:55:07 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:55:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:55:10 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:55:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:55:11 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:55:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c2d76ba33f8d52087147ce28d8f03c08f69677591e3e10db810bf76a6e09427`  
		Last Modified: Fri, 24 Apr 2020 00:22:00 GMT  
		Size: 27.2 MB (27158644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92d4cfc71d3821474946021fdbf241a74992a84c6269c3e9a052ce7fc56cece`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 32.3 KB (32326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63063bfe137200b3c8d1ee8d819124352c20ee8c189a0388f461ec66bb759310`  
		Last Modified: Fri, 24 Apr 2020 00:21:53 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38385900086ffa7d7cb9c3bbeabaf2176d7d7958ebf0736d2a01773a830201ee`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0959e86d4d132b0e91456f1d1ecc3b1d6518d720b7ee82926559fd34800d7b53`  
		Last Modified: Fri, 12 Jun 2020 18:58:18 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f37953089cdddf8b409b61f0f30de595d96483dd0ce38463384dd5d201b70f`  
		Last Modified: Fri, 12 Jun 2020 18:58:19 GMT  
		Size: 5.5 MB (5456917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab7a5713dbb2830a805d0b68dae96ce4dd827b086473a3d785f76b37d885fe1`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 1.3 MB (1258973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0614221a0d602714b38672c572d4071df43a41223dab9b1c81ab45ea5bc9c9`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e232435757d992d57a40890acb9528958726ef62b7f400e4ef7c3b7d97c234c`  
		Last Modified: Fri, 12 Jun 2020 18:58:16 GMT  
		Size: 1.3 MB (1263367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb430a3947464ff3d178d412e9047e4b67e2cc3a09923dd4b84596fa57403d66`  
		Last Modified: Fri, 12 Jun 2020 18:58:15 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f581713dad871dd1e951c6f9dae24eb128f99423677031f7b995e5d0e5afd2`  
		Last Modified: Fri, 12 Jun 2020 18:58:15 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e73fa8d9c1238f2fb5bdc8c15aa0f1f818cd4d08be1762d677bc650a6765903`  
		Last Modified: Fri, 12 Jun 2020 18:58:41 GMT  
		Size: 87.8 MB (87816861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e23804dfe7361c4d8bb4fdd1b89013bd168ba1669961992b16e8516bacccbd0`  
		Last Modified: Fri, 12 Jun 2020 18:58:16 GMT  
		Size: 4.9 KB (4853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:rc` - linux; ppc64le

```console
$ docker pull mariadb@sha256:7f3c6e4fbe1d904fe0f1daf0b28dd7b6055906d0e4ef545e0f167305737edfb3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135491752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4482a6d35ab27dc6622588f472d707755fd0242ccf076f18f56b764f32d2f56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:49:25 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 12 Jun 2020 18:49:36 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Fri, 12 Jun 2020 18:50:14 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:55:32 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:55:52 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:55:58 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:56:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:56:12 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:56:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907c120bad3d45c4179d4a0c2dcde4937f90d39332c52fb866de70e4b7634460`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5768c1a14ad9b899134606bad0b1bf95337891f65101e352d91fe125d74a1e7`  
		Last Modified: Fri, 12 Jun 2020 19:13:37 GMT  
		Size: 93.0 MB (92981382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9e462c378a4b7787721cd8cb5720e89d8e9696d398174bb7b4d6d60bacfada`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 4.9 KB (4855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:rc-focal`

```console
$ docker pull mariadb@sha256:eec0568c86675b6d233f9e56b71e0a53306b7652df20b31e655e98cd55acdeb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:rc-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:1c43c2c9a9cbc8d6d917b3baccc746029611401140afacbc341f9e0543f693d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125468046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d666ead09d0cdb6b38628b20884b7a034975d73e0c72bf72af995bf25b32ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:24:12 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 12 Jun 2020 18:24:12 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Fri, 12 Jun 2020 18:24:13 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:24:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:24:45 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:24:45 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:24:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:24:46 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:24:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2a69879e3e44e2c33e196212dc1e1f81aa3f8a2f150e64ba2be5415cebf05f`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3434e5ff172ae3f9a2ebac367af66daecf7e55fb5d24d1202cc34d1a680d5a`  
		Last Modified: Fri, 12 Jun 2020 18:26:37 GMT  
		Size: 88.8 MB (88792188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9318b4b2608af288b8a860c61f31daa1e48322b0a4d0588a94e1ae7269bb89a9`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:rc-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:a5634fa0b151ea9b814b46fa01c24e79020cc778431c75ca984b86128d07a336
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (122997696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc94523ed8e1f81f5c414f6b5f9e562d1ee6476c06c55e41d88dfecf0035ac55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 00:18:16 GMT
ADD file:e9947aff2dfa8f220d4b25dc0770aff8d9ffc08482e52f54833f39e1c3ec08bf in / 
# Fri, 24 Apr 2020 00:18:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 00:18:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:18:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:18:29 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:53:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:53:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:53:46 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:54:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:54:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:54:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:54:14 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:54:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:54:17 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 12 Jun 2020 18:54:18 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Fri, 12 Jun 2020 18:54:20 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:55:07 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:55:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:55:10 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:55:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:55:11 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:55:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c2d76ba33f8d52087147ce28d8f03c08f69677591e3e10db810bf76a6e09427`  
		Last Modified: Fri, 24 Apr 2020 00:22:00 GMT  
		Size: 27.2 MB (27158644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92d4cfc71d3821474946021fdbf241a74992a84c6269c3e9a052ce7fc56cece`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 32.3 KB (32326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63063bfe137200b3c8d1ee8d819124352c20ee8c189a0388f461ec66bb759310`  
		Last Modified: Fri, 24 Apr 2020 00:21:53 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38385900086ffa7d7cb9c3bbeabaf2176d7d7958ebf0736d2a01773a830201ee`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0959e86d4d132b0e91456f1d1ecc3b1d6518d720b7ee82926559fd34800d7b53`  
		Last Modified: Fri, 12 Jun 2020 18:58:18 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f37953089cdddf8b409b61f0f30de595d96483dd0ce38463384dd5d201b70f`  
		Last Modified: Fri, 12 Jun 2020 18:58:19 GMT  
		Size: 5.5 MB (5456917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab7a5713dbb2830a805d0b68dae96ce4dd827b086473a3d785f76b37d885fe1`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 1.3 MB (1258973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0614221a0d602714b38672c572d4071df43a41223dab9b1c81ab45ea5bc9c9`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e232435757d992d57a40890acb9528958726ef62b7f400e4ef7c3b7d97c234c`  
		Last Modified: Fri, 12 Jun 2020 18:58:16 GMT  
		Size: 1.3 MB (1263367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb430a3947464ff3d178d412e9047e4b67e2cc3a09923dd4b84596fa57403d66`  
		Last Modified: Fri, 12 Jun 2020 18:58:15 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f581713dad871dd1e951c6f9dae24eb128f99423677031f7b995e5d0e5afd2`  
		Last Modified: Fri, 12 Jun 2020 18:58:15 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e73fa8d9c1238f2fb5bdc8c15aa0f1f818cd4d08be1762d677bc650a6765903`  
		Last Modified: Fri, 12 Jun 2020 18:58:41 GMT  
		Size: 87.8 MB (87816861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e23804dfe7361c4d8bb4fdd1b89013bd168ba1669961992b16e8516bacccbd0`  
		Last Modified: Fri, 12 Jun 2020 18:58:16 GMT  
		Size: 4.9 KB (4853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:rc-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:7f3c6e4fbe1d904fe0f1daf0b28dd7b6055906d0e4ef545e0f167305737edfb3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135491752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4482a6d35ab27dc6622588f472d707755fd0242ccf076f18f56b764f32d2f56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:49:25 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 12 Jun 2020 18:49:36 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Fri, 12 Jun 2020 18:50:14 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:55:32 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:55:52 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:55:58 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:56:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:56:12 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:56:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907c120bad3d45c4179d4a0c2dcde4937f90d39332c52fb866de70e4b7634460`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5768c1a14ad9b899134606bad0b1bf95337891f65101e352d91fe125d74a1e7`  
		Last Modified: Fri, 12 Jun 2020 19:13:37 GMT  
		Size: 93.0 MB (92981382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9e462c378a4b7787721cd8cb5720e89d8e9696d398174bb7b4d6d60bacfada`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 4.9 KB (4855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
