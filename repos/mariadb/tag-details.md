<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mariadb`

-	[`mariadb:10`](#mariadb10)
-	[`mariadb:10-focal`](#mariadb10-focal)
-	[`mariadb:10.2`](#mariadb102)
-	[`mariadb:10.2-bionic`](#mariadb102-bionic)
-	[`mariadb:10.2.40`](#mariadb10240)
-	[`mariadb:10.2.40-bionic`](#mariadb10240-bionic)
-	[`mariadb:10.3`](#mariadb103)
-	[`mariadb:10.3-focal`](#mariadb103-focal)
-	[`mariadb:10.3.31`](#mariadb10331)
-	[`mariadb:10.3.31-focal`](#mariadb10331-focal)
-	[`mariadb:10.4`](#mariadb104)
-	[`mariadb:10.4-focal`](#mariadb104-focal)
-	[`mariadb:10.4.21`](#mariadb10421)
-	[`mariadb:10.4.21-focal`](#mariadb10421-focal)
-	[`mariadb:10.5`](#mariadb105)
-	[`mariadb:10.5-focal`](#mariadb105-focal)
-	[`mariadb:10.5.12`](#mariadb10512)
-	[`mariadb:10.5.12-focal`](#mariadb10512-focal)
-	[`mariadb:10.6`](#mariadb106)
-	[`mariadb:10.6-focal`](#mariadb106-focal)
-	[`mariadb:10.6.4`](#mariadb1064)
-	[`mariadb:10.6.4-focal`](#mariadb1064-focal)
-	[`mariadb:focal`](#mariadbfocal)
-	[`mariadb:latest`](#mariadblatest)

## `mariadb:10`

```console
$ docker pull mariadb@sha256:68a9a3ef9ee7b13438ba135a36643c43b7ec0e6f6e4a0ebae07dfb6539cededb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10` - linux; amd64

```console
$ docker pull mariadb@sha256:a9b26cdb3cfb008f4373b93cfd350ec51e3fbf2cbc227fc4da0cb6338851de07
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127015901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7220a722ce2a763177738b8cb0b42b3602368100ee7cc7088fb0bcc96fea1c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:19:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 05:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:18 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 05:19:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 05:19:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 05:19:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:39 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 05:19:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 05:19:50 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 01 Oct 2021 05:19:50 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 01 Oct 2021 05:19:50 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Fri, 01 Oct 2021 05:19:50 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Fri, 01 Oct 2021 05:19:51 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 05:19:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 05:20:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 05:20:26 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 05:20:26 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 05:20:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 05:20:26 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 05:20:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6f45e0fb03b087254fb0750ec2bbfbc7ea10f3eaaa2c3381f2ef6b3cf2c32b`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a10760fd6ecff1db568c4df08e4add59ea3424ae8b2ed2ac557f5239fa74d`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 5.5 MB (5489340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0645d99211dd422dc4b2c52d1005a518b5d9c76409584ee75faf26c78de36b`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 3.6 MB (3582638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff899ddf1cc12eb3161fb924245c2cdb096fe9cadd0b73128f7d3e45e4a0e6c`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e10ba5def77eae105b1dfab52bd41d16cba2895929673658ec8fedc7d8408e`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.3 MB (2274765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef565721758b7adafc1e282adeddbe68df6d6631699124a860c60f5c507840b4`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373c21a041dec3d49d5ab23634ca8c0141b8ec8504dfe832900a48a48baa5d10`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1a9ce482ccd35a23b4f61715fd76783510d6fb7832e6db07a37f77a2d31f36`  
		Last Modified: Fri, 01 Oct 2021 05:24:29 GMT  
		Size: 87.1 MB (87089918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecedf97e512c4f6e245cac1ca1aa143939b0cda2428ac65a108fc40470870576`  
		Last Modified: Fri, 01 Oct 2021 05:24:15 GMT  
		Size: 5.6 KB (5608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d7c05c4a4da3313b71382230d55dfdb154f05dde2637cb5abd717516cc29c90e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124307877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06bb3c39ebf3550feb4449c7f08243564fad0a09635993f85486e2305d3a395d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:38:47 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 03:38:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:38:56 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 03:39:11 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 03:39:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 03:39:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:39:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 03:39:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 03:39:29 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 01 Oct 2021 03:39:29 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 01 Oct 2021 03:39:29 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Fri, 01 Oct 2021 03:39:29 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Fri, 01 Oct 2021 03:39:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 03:39:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 03:39:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 03:39:54 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 03:39:55 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 03:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 03:39:55 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 03:39:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d5ae241c1f10925c65b1658513761cd873e86632ea54cd491a17314c717db9`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1337b7de0aecaa84469be03f6aca5f4716813a7f70d6df52ada4f37e67dce98`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 5.5 MB (5455225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720ecfb64bf9977e96130e89f4d49759a1b9577aabaa5c864b0f7a3c0473f778`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 3.4 MB (3368539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba0c987cf142da7e613c8eb5506412f33e85d62e8b737d82ae8a86dad1a3dd1`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1cd2ca1d8beab7fe86d456206b59ee252c55fd199373f2caae49c71ec65a2a`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.2 MB (2203545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9328b4fc02fb1261cd4016d0e4d31dd6528b268e170d8278afbd062e3a96fa1`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba1c8ccb51c846dc0a9271404c54d1917897030f09c2df37204078c31ffae94`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c825ac5e690d987bb7c9e20ac4d482d0b3d6d45e43e686f5494169516ea6380`  
		Last Modified: Fri, 01 Oct 2021 03:44:14 GMT  
		Size: 86.1 MB (86097833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2376eebe2a30870028a6b6ab6b9cf1b96551befdbee8ed82a18e56a125c83397`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; ppc64le

```console
$ docker pull mariadb@sha256:aa3c316f88dd9537eeaa7201d6d3c5f8d8732196ee6c9cd5ce553816c7a060d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137539722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a66b6be1b40e577fe733ec92528cf73ee97a8536e1fcddc9fe638aa9132f8173`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:34:53 GMT
ENV GOSU_VERSION=1.13
# Sat, 16 Oct 2021 01:35:28 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 01:35:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 01:36:02 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:36:03 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 16 Oct 2021 01:36:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 01:36:18 GMT
ARG MARIADB_MAJOR=10.6
# Sat, 16 Oct 2021 01:36:19 GMT
ENV MARIADB_MAJOR=10.6
# Sat, 16 Oct 2021 01:36:22 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Sat, 16 Oct 2021 01:36:24 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Sat, 16 Oct 2021 01:36:29 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Sat, 16 Oct 2021 01:36:39 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 16 Oct 2021 01:38:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 16 Oct 2021 01:39:01 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Oct 2021 01:39:03 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:39:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Oct 2021 01:39:08 GMT
EXPOSE 3306
# Sat, 16 Oct 2021 01:39:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bdbddf0ed762c90ab4fcfe1f42007a96e4f90ca4f0765dfcec52213a3f5c12`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 3.7 MB (3670760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cc95e86fb5ab1bda9839a1ecbd3c2d607bc6cfc5155f33bf32c9d7827ec98b`  
		Last Modified: Sat, 16 Oct 2021 01:49:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe2cefdba07cb9fc803227a545d4fcc196038c1020de7698bf4e333d9056cbd`  
		Last Modified: Sat, 16 Oct 2021 01:49:28 GMT  
		Size: 2.6 MB (2573066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab77c7b0e7b171541e9f7f813ef81190ef39151aea54bfe2b64f8c191ce672c`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d188c1c418692bd6c05728f7b542eab7acbdf502f48eaf84c762ba6b27718c`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288c0769408956c537d6b5b649bc2b69ffe5036157a0aa58dce6c17312680a33`  
		Last Modified: Sat, 16 Oct 2021 01:49:45 GMT  
		Size: 91.3 MB (91330343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4c9a0a37f40daaa1c904e99bb499d11db46dd87bd94236295d1ad90603ba74`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 5.6 KB (5613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; s390x

```console
$ docker pull mariadb@sha256:90bc202cc092060b6e454b7f2d06cbe792ffd3d7a2edefe42e30964c55d24dab
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (126014128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b71468a7107bd097e1852fade221839dfd4b89ee873666b6f7beda44310b7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:02:36 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:02:41 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:02:42 GMT
ENV GOSU_VERSION=1.13
# Sat, 16 Oct 2021 01:02:50 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 01:02:51 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 01:02:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:02:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 16 Oct 2021 01:03:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 01:03:03 GMT
ARG MARIADB_MAJOR=10.6
# Sat, 16 Oct 2021 01:03:03 GMT
ENV MARIADB_MAJOR=10.6
# Sat, 16 Oct 2021 01:03:03 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Sat, 16 Oct 2021 01:03:04 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Sat, 16 Oct 2021 01:03:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Sat, 16 Oct 2021 01:03:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 16 Oct 2021 01:03:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 16 Oct 2021 01:03:26 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Oct 2021 01:03:26 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:03:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Oct 2021 01:03:26 GMT
EXPOSE 3306
# Sat, 16 Oct 2021 01:03:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc30a1fd200d10ce23e934b30e72d36ea131fb670d30afe697304591986fe1`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228a3fc0a9531bf3e9e08d9800daffbe33729ba8a16fb427b07a1a36fb047e02`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 5.4 MB (5380980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e511a129710d7aa78451eebec778e60a256b2a9e60db59a9f6d09641bd4f96`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 3.2 MB (3239822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a9cf411b6c206dca4cd2f493440c36781e332782682bb40969b6640e8e98e9`  
		Last Modified: Sat, 16 Oct 2021 01:04:31 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cac3f3cdb186c64fce6e0a7efc39abe96d0e6ab755d9193c981cc44c801cc51`  
		Last Modified: Sat, 16 Oct 2021 01:04:31 GMT  
		Size: 2.2 MB (2188905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd5f55dd4f1666fe90f4ca1b3b0cc36a9092c44ae19033a4d2b7b0e2ff3dddb`  
		Last Modified: Sat, 16 Oct 2021 01:04:30 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0ae06775bbebbdaaf444830172bb614071d5d08004722e2ac0acc7dc0106c3`  
		Last Modified: Sat, 16 Oct 2021 01:04:30 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362403b21b44d69858c7a816e3ddbbd7cb67dac62386727c8ce11d44891fc990`  
		Last Modified: Sat, 16 Oct 2021 01:04:48 GMT  
		Size: 88.1 MB (88073232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48196c9046fbbce7d43754945286d36794d5f7eb923e2501d8a9a4ddc88b3dd3`  
		Last Modified: Sat, 16 Oct 2021 01:04:30 GMT  
		Size: 5.6 KB (5614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10-focal`

```console
$ docker pull mariadb@sha256:68a9a3ef9ee7b13438ba135a36643c43b7ec0e6f6e4a0ebae07dfb6539cededb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:a9b26cdb3cfb008f4373b93cfd350ec51e3fbf2cbc227fc4da0cb6338851de07
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127015901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7220a722ce2a763177738b8cb0b42b3602368100ee7cc7088fb0bcc96fea1c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:19:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 05:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:18 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 05:19:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 05:19:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 05:19:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:39 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 05:19:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 05:19:50 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 01 Oct 2021 05:19:50 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 01 Oct 2021 05:19:50 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Fri, 01 Oct 2021 05:19:50 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Fri, 01 Oct 2021 05:19:51 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 05:19:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 05:20:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 05:20:26 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 05:20:26 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 05:20:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 05:20:26 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 05:20:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6f45e0fb03b087254fb0750ec2bbfbc7ea10f3eaaa2c3381f2ef6b3cf2c32b`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a10760fd6ecff1db568c4df08e4add59ea3424ae8b2ed2ac557f5239fa74d`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 5.5 MB (5489340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0645d99211dd422dc4b2c52d1005a518b5d9c76409584ee75faf26c78de36b`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 3.6 MB (3582638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff899ddf1cc12eb3161fb924245c2cdb096fe9cadd0b73128f7d3e45e4a0e6c`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e10ba5def77eae105b1dfab52bd41d16cba2895929673658ec8fedc7d8408e`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.3 MB (2274765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef565721758b7adafc1e282adeddbe68df6d6631699124a860c60f5c507840b4`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373c21a041dec3d49d5ab23634ca8c0141b8ec8504dfe832900a48a48baa5d10`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1a9ce482ccd35a23b4f61715fd76783510d6fb7832e6db07a37f77a2d31f36`  
		Last Modified: Fri, 01 Oct 2021 05:24:29 GMT  
		Size: 87.1 MB (87089918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecedf97e512c4f6e245cac1ca1aa143939b0cda2428ac65a108fc40470870576`  
		Last Modified: Fri, 01 Oct 2021 05:24:15 GMT  
		Size: 5.6 KB (5608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d7c05c4a4da3313b71382230d55dfdb154f05dde2637cb5abd717516cc29c90e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124307877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06bb3c39ebf3550feb4449c7f08243564fad0a09635993f85486e2305d3a395d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:38:47 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 03:38:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:38:56 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 03:39:11 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 03:39:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 03:39:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:39:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 03:39:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 03:39:29 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 01 Oct 2021 03:39:29 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 01 Oct 2021 03:39:29 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Fri, 01 Oct 2021 03:39:29 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Fri, 01 Oct 2021 03:39:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 03:39:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 03:39:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 03:39:54 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 03:39:55 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 03:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 03:39:55 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 03:39:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d5ae241c1f10925c65b1658513761cd873e86632ea54cd491a17314c717db9`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1337b7de0aecaa84469be03f6aca5f4716813a7f70d6df52ada4f37e67dce98`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 5.5 MB (5455225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720ecfb64bf9977e96130e89f4d49759a1b9577aabaa5c864b0f7a3c0473f778`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 3.4 MB (3368539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba0c987cf142da7e613c8eb5506412f33e85d62e8b737d82ae8a86dad1a3dd1`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1cd2ca1d8beab7fe86d456206b59ee252c55fd199373f2caae49c71ec65a2a`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.2 MB (2203545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9328b4fc02fb1261cd4016d0e4d31dd6528b268e170d8278afbd062e3a96fa1`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba1c8ccb51c846dc0a9271404c54d1917897030f09c2df37204078c31ffae94`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c825ac5e690d987bb7c9e20ac4d482d0b3d6d45e43e686f5494169516ea6380`  
		Last Modified: Fri, 01 Oct 2021 03:44:14 GMT  
		Size: 86.1 MB (86097833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2376eebe2a30870028a6b6ab6b9cf1b96551befdbee8ed82a18e56a125c83397`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:aa3c316f88dd9537eeaa7201d6d3c5f8d8732196ee6c9cd5ce553816c7a060d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137539722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a66b6be1b40e577fe733ec92528cf73ee97a8536e1fcddc9fe638aa9132f8173`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:34:53 GMT
ENV GOSU_VERSION=1.13
# Sat, 16 Oct 2021 01:35:28 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 01:35:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 01:36:02 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:36:03 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 16 Oct 2021 01:36:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 01:36:18 GMT
ARG MARIADB_MAJOR=10.6
# Sat, 16 Oct 2021 01:36:19 GMT
ENV MARIADB_MAJOR=10.6
# Sat, 16 Oct 2021 01:36:22 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Sat, 16 Oct 2021 01:36:24 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Sat, 16 Oct 2021 01:36:29 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Sat, 16 Oct 2021 01:36:39 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 16 Oct 2021 01:38:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 16 Oct 2021 01:39:01 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Oct 2021 01:39:03 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:39:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Oct 2021 01:39:08 GMT
EXPOSE 3306
# Sat, 16 Oct 2021 01:39:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bdbddf0ed762c90ab4fcfe1f42007a96e4f90ca4f0765dfcec52213a3f5c12`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 3.7 MB (3670760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cc95e86fb5ab1bda9839a1ecbd3c2d607bc6cfc5155f33bf32c9d7827ec98b`  
		Last Modified: Sat, 16 Oct 2021 01:49:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe2cefdba07cb9fc803227a545d4fcc196038c1020de7698bf4e333d9056cbd`  
		Last Modified: Sat, 16 Oct 2021 01:49:28 GMT  
		Size: 2.6 MB (2573066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab77c7b0e7b171541e9f7f813ef81190ef39151aea54bfe2b64f8c191ce672c`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d188c1c418692bd6c05728f7b542eab7acbdf502f48eaf84c762ba6b27718c`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288c0769408956c537d6b5b649bc2b69ffe5036157a0aa58dce6c17312680a33`  
		Last Modified: Sat, 16 Oct 2021 01:49:45 GMT  
		Size: 91.3 MB (91330343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4c9a0a37f40daaa1c904e99bb499d11db46dd87bd94236295d1ad90603ba74`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 5.6 KB (5613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:90bc202cc092060b6e454b7f2d06cbe792ffd3d7a2edefe42e30964c55d24dab
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (126014128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b71468a7107bd097e1852fade221839dfd4b89ee873666b6f7beda44310b7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:02:36 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:02:41 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:02:42 GMT
ENV GOSU_VERSION=1.13
# Sat, 16 Oct 2021 01:02:50 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 01:02:51 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 01:02:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:02:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 16 Oct 2021 01:03:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 01:03:03 GMT
ARG MARIADB_MAJOR=10.6
# Sat, 16 Oct 2021 01:03:03 GMT
ENV MARIADB_MAJOR=10.6
# Sat, 16 Oct 2021 01:03:03 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Sat, 16 Oct 2021 01:03:04 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Sat, 16 Oct 2021 01:03:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Sat, 16 Oct 2021 01:03:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 16 Oct 2021 01:03:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 16 Oct 2021 01:03:26 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Oct 2021 01:03:26 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:03:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Oct 2021 01:03:26 GMT
EXPOSE 3306
# Sat, 16 Oct 2021 01:03:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc30a1fd200d10ce23e934b30e72d36ea131fb670d30afe697304591986fe1`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228a3fc0a9531bf3e9e08d9800daffbe33729ba8a16fb427b07a1a36fb047e02`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 5.4 MB (5380980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e511a129710d7aa78451eebec778e60a256b2a9e60db59a9f6d09641bd4f96`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 3.2 MB (3239822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a9cf411b6c206dca4cd2f493440c36781e332782682bb40969b6640e8e98e9`  
		Last Modified: Sat, 16 Oct 2021 01:04:31 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cac3f3cdb186c64fce6e0a7efc39abe96d0e6ab755d9193c981cc44c801cc51`  
		Last Modified: Sat, 16 Oct 2021 01:04:31 GMT  
		Size: 2.2 MB (2188905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd5f55dd4f1666fe90f4ca1b3b0cc36a9092c44ae19033a4d2b7b0e2ff3dddb`  
		Last Modified: Sat, 16 Oct 2021 01:04:30 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0ae06775bbebbdaaf444830172bb614071d5d08004722e2ac0acc7dc0106c3`  
		Last Modified: Sat, 16 Oct 2021 01:04:30 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362403b21b44d69858c7a816e3ddbbd7cb67dac62386727c8ce11d44891fc990`  
		Last Modified: Sat, 16 Oct 2021 01:04:48 GMT  
		Size: 88.1 MB (88073232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48196c9046fbbce7d43754945286d36794d5f7eb923e2501d8a9a4ddc88b3dd3`  
		Last Modified: Sat, 16 Oct 2021 01:04:30 GMT  
		Size: 5.6 KB (5614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2`

```console
$ docker pull mariadb@sha256:82594695e7daacb7e59c2400b503073c8a79514e9b1e56b57f01986cbdf34bdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2` - linux; amd64

```console
$ docker pull mariadb@sha256:a528fb0b369f7dc138106ac7ff2d3500577d1be6cbee3a7261509bdbb7ee62d6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109274501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354c935e3d016be16ddc8baaebc97205b8c78a89230b00f06333a2ce62c0f0d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:23 GMT
ADD file:0d82cd095966e8ee78b593cb47a352eec842edb7bd9d9468e8a70154522447d1 in / 
# Fri, 01 Oct 2021 02:23:24 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:22:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 05:22:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:22:25 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 05:22:39 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 05:22:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 05:22:48 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:22:49 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 05:22:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 05:22:57 GMT
ARG MARIADB_MAJOR=10.2
# Fri, 01 Oct 2021 05:22:57 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 01 Oct 2021 05:22:57 GMT
ARG MARIADB_VERSION=1:10.2.40+maria~bionic
# Fri, 01 Oct 2021 05:22:58 GMT
ENV MARIADB_VERSION=1:10.2.40+maria~bionic
# Fri, 01 Oct 2021 05:22:58 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
# Fri, 01 Oct 2021 05:22:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 05:23:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 05:23:36 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 05:23:36 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 05:23:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Oct 2021 05:23:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 05:23:38 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 05:23:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:284055322776031bac33723839acb0db2d063a525ba4fa1fd268a831c7553b26`  
		Last Modified: Fri, 01 Oct 2021 02:25:02 GMT  
		Size: 26.7 MB (26705075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c939c6256f1f0a750da3d02b63d4aa63b9ac6f085a5b904ede35065e2f9074ad`  
		Last Modified: Fri, 01 Oct 2021 05:26:25 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b11a4bc2affe5918649c7ac2245c1ba21dc9f4ea8a536f01188e6e7a32bf30`  
		Last Modified: Fri, 01 Oct 2021 05:26:24 GMT  
		Size: 4.8 MB (4813381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec46f26e2520dcdcb3b1337a6f1d0324de5ca746cf496c2f58d1b3a999b0b3ee`  
		Last Modified: Fri, 01 Oct 2021 05:26:23 GMT  
		Size: 3.5 MB (3547363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c10147eb944f79d9fbf87b70609cf920a464f53924f34d5e0e221a7a301474`  
		Last Modified: Fri, 01 Oct 2021 05:26:22 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c518dbe68aa8249927d923eb729c649959ac6346fc141829fb1631d88a918d`  
		Last Modified: Fri, 01 Oct 2021 05:26:23 GMT  
		Size: 1.6 MB (1585830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2389b8a7dd566761cba6e2dc15b3fc69c13543880fc93dbf19d15619c461dad2`  
		Last Modified: Fri, 01 Oct 2021 05:26:20 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4107cbdbc866a69764051c7aae57edbfaa8754f1ab814924f894fb24795bf0d2`  
		Last Modified: Fri, 01 Oct 2021 05:26:20 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1abc07c11569f5fdfc3bd41ab8584879a293c570c6d10e80240ba609fbe5918`  
		Last Modified: Fri, 01 Oct 2021 05:26:31 GMT  
		Size: 72.6 MB (72609605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b160c6de4e1da109323527158924e3ed20ee08ffbc35fa30f621da4e1842a63`  
		Last Modified: Fri, 01 Oct 2021 05:26:20 GMT  
		Size: 5.6 KB (5609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0543f573ce8402a676c92fe1ae461f34d772ae08698e463551812b0a2879babc`  
		Last Modified: Fri, 01 Oct 2021 05:26:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d9b65ff8471c9f99c8c527e184a634a5fd9fe7c055219c6126842bd9307aa2ae
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104362815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea90b5b91095548619940d86462e72eeb25d738e12ebd464a616ad703541175f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:40 GMT
ADD file:35e2504756850fc1add00516fa89b0499b59c348457a96708eedb61313e7b25e in / 
# Fri, 01 Oct 2021 02:43:41 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:41:45 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 03:41:55 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:41:55 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 03:42:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 03:42:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 03:42:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:42:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 03:42:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 03:42:29 GMT
ARG MARIADB_MAJOR=10.2
# Fri, 01 Oct 2021 03:42:29 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 01 Oct 2021 03:42:29 GMT
ARG MARIADB_VERSION=1:10.2.40+maria~bionic
# Fri, 01 Oct 2021 03:42:29 GMT
ENV MARIADB_VERSION=1:10.2.40+maria~bionic
# Fri, 01 Oct 2021 03:42:29 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
# Fri, 01 Oct 2021 03:42:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 03:42:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 03:42:56 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 03:42:56 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 03:42:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Oct 2021 03:42:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 03:42:57 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 03:42:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f46992f278c2dd50c481ff60ce8528b6eb59016ac6243e1a7fb385c79c5944b9`  
		Last Modified: Fri, 01 Oct 2021 02:45:30 GMT  
		Size: 23.7 MB (23727476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2f5eee07061665f2228abc3a2728edd1e4154d6df13108b774b783e80f0e66`  
		Last Modified: Fri, 01 Oct 2021 03:46:30 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d367371c2390bcbc842695eaf3f40cce09f04619642c4b24f3c44ed3d52b6c`  
		Last Modified: Fri, 01 Oct 2021 03:46:29 GMT  
		Size: 4.4 MB (4395696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7506380fa349a5c0c64aefa19caa23a14d4a2c0fba39e1e33c9fbee85ed857`  
		Last Modified: Fri, 01 Oct 2021 03:46:28 GMT  
		Size: 3.2 MB (3204622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6538e9a7bc49ebcf8e6535bdc0738d136053609e8f3c5c9a5ecabd9f552b18`  
		Last Modified: Fri, 01 Oct 2021 03:46:28 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da46f0ea77b03886259bd98657e5307c555223078466fdffbcb8683f430c070`  
		Last Modified: Fri, 01 Oct 2021 03:46:28 GMT  
		Size: 1.5 MB (1532555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d09dd4e711e507d8a254bfa5b5e9c1607f64e647b7cd492c79d5d87a488218`  
		Last Modified: Fri, 01 Oct 2021 03:46:25 GMT  
		Size: 5.2 KB (5170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d53ed47ee11ab96617578a59a8e36273abda3d74c34b4779262b643895ae4be`  
		Last Modified: Fri, 01 Oct 2021 03:46:25 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d01f94244806aa25dd55875bc8b3215476ae8d2f3eb11860d5f876752c11a23`  
		Last Modified: Fri, 01 Oct 2021 03:46:37 GMT  
		Size: 71.5 MB (71489216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b4fa26ada886c1a4e2f56d8afa9e6ecfb72f646136b03161e7921341117749`  
		Last Modified: Fri, 01 Oct 2021 03:46:25 GMT  
		Size: 5.6 KB (5608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a845960e2ac4fc04dc156629e63af0cdb83d58f30547bc9a86f553caa4d24f9`  
		Last Modified: Fri, 01 Oct 2021 03:46:26 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a87355bbfcd8c4d277b81f614a424ae07e75c61cd4f907771fafd75c95734f6d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117673902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8c855f600de1dcf745c21fc2bad2a8c78a04b1b30e81059ceb8015b6831b98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Oct 2021 11:07:29 GMT
ADD file:fd96554dfb72307c3cf9292c343050a8b9f0848735b7555820f0068914ebd758 in / 
# Tue, 05 Oct 2021 11:07:35 GMT
CMD ["bash"]
# Wed, 06 Oct 2021 18:27:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Oct 2021 18:28:04 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 18:28:07 GMT
ENV GOSU_VERSION=1.13
# Wed, 06 Oct 2021 18:28:50 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Oct 2021 18:28:56 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Oct 2021 18:30:32 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 18:30:36 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Oct 2021 18:30:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Oct 2021 18:30:51 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 06 Oct 2021 18:30:54 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 06 Oct 2021 18:30:56 GMT
ARG MARIADB_VERSION=1:10.2.40+maria~bionic
# Wed, 06 Oct 2021 18:30:58 GMT
ENV MARIADB_VERSION=1:10.2.40+maria~bionic
# Wed, 06 Oct 2021 18:31:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
# Wed, 06 Oct 2021 18:31:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Oct 2021 18:32:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Oct 2021 18:32:58 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Oct 2021 18:33:01 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Wed, 06 Oct 2021 18:33:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 06 Oct 2021 18:33:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Oct 2021 18:33:40 GMT
EXPOSE 3306
# Wed, 06 Oct 2021 18:33:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:db28fc1e594e5598e665c54ac1b7fd602d86dddaf8bb237a72303cec22a9185c`  
		Last Modified: Tue, 05 Oct 2021 11:10:31 GMT  
		Size: 30.4 MB (30432921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508be09c006b6365ae7c5fc9b0593010a2d284d9b02e4f9ad77ee4f4209c8c0a`  
		Last Modified: Wed, 06 Oct 2021 18:37:35 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57bc7004e2371a404c5ff023b89e2ade70ef3581e3c7156807ac620fad13dbaf`  
		Last Modified: Wed, 06 Oct 2021 18:37:32 GMT  
		Size: 5.6 MB (5630476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0247b3a43e1d7479a934dd7064273de0a582a7b29cbbe3930976de3cdea14165`  
		Last Modified: Wed, 06 Oct 2021 18:37:32 GMT  
		Size: 3.5 MB (3529458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36f80bf4a4eb1f224d050821b3697d447a6684a83bd5474d805d269be98738a`  
		Last Modified: Wed, 06 Oct 2021 18:37:31 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c8e01754107b9697fb72ecd295ce381ffdbf045d9af0e8434896bbdfb99589`  
		Last Modified: Wed, 06 Oct 2021 18:37:32 GMT  
		Size: 1.9 MB (1938899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68c6f8634752aa2fad0a3bb47ecd3db12661c09a627f009b659af43d8b50693`  
		Last Modified: Wed, 06 Oct 2021 18:37:28 GMT  
		Size: 5.2 KB (5172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05753e4613d3ea1d36cd939dcb1df72b40d033867d856378e3bb83f4ab74f77e`  
		Last Modified: Wed, 06 Oct 2021 18:37:27 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b48f20163eab27b9baf9ec26b3653fc71506f35970677fcab2ed9a46cf41ef`  
		Last Modified: Wed, 06 Oct 2021 18:37:42 GMT  
		Size: 76.1 MB (76128891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9e3e320fa8bc28bbfe5b93681ab8640f37280697cd105ce8b6687c1b48b9edc`  
		Last Modified: Wed, 06 Oct 2021 18:37:28 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf75adc1fe0afd7e3946ed2ab76579aaa00cb5961dd57eb02fe88a7151ff240`  
		Last Modified: Wed, 06 Oct 2021 18:37:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2-bionic`

```console
$ docker pull mariadb@sha256:82594695e7daacb7e59c2400b503073c8a79514e9b1e56b57f01986cbdf34bdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:a528fb0b369f7dc138106ac7ff2d3500577d1be6cbee3a7261509bdbb7ee62d6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109274501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354c935e3d016be16ddc8baaebc97205b8c78a89230b00f06333a2ce62c0f0d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:23 GMT
ADD file:0d82cd095966e8ee78b593cb47a352eec842edb7bd9d9468e8a70154522447d1 in / 
# Fri, 01 Oct 2021 02:23:24 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:22:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 05:22:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:22:25 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 05:22:39 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 05:22:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 05:22:48 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:22:49 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 05:22:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 05:22:57 GMT
ARG MARIADB_MAJOR=10.2
# Fri, 01 Oct 2021 05:22:57 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 01 Oct 2021 05:22:57 GMT
ARG MARIADB_VERSION=1:10.2.40+maria~bionic
# Fri, 01 Oct 2021 05:22:58 GMT
ENV MARIADB_VERSION=1:10.2.40+maria~bionic
# Fri, 01 Oct 2021 05:22:58 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
# Fri, 01 Oct 2021 05:22:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 05:23:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 05:23:36 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 05:23:36 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 05:23:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Oct 2021 05:23:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 05:23:38 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 05:23:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:284055322776031bac33723839acb0db2d063a525ba4fa1fd268a831c7553b26`  
		Last Modified: Fri, 01 Oct 2021 02:25:02 GMT  
		Size: 26.7 MB (26705075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c939c6256f1f0a750da3d02b63d4aa63b9ac6f085a5b904ede35065e2f9074ad`  
		Last Modified: Fri, 01 Oct 2021 05:26:25 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b11a4bc2affe5918649c7ac2245c1ba21dc9f4ea8a536f01188e6e7a32bf30`  
		Last Modified: Fri, 01 Oct 2021 05:26:24 GMT  
		Size: 4.8 MB (4813381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec46f26e2520dcdcb3b1337a6f1d0324de5ca746cf496c2f58d1b3a999b0b3ee`  
		Last Modified: Fri, 01 Oct 2021 05:26:23 GMT  
		Size: 3.5 MB (3547363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c10147eb944f79d9fbf87b70609cf920a464f53924f34d5e0e221a7a301474`  
		Last Modified: Fri, 01 Oct 2021 05:26:22 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c518dbe68aa8249927d923eb729c649959ac6346fc141829fb1631d88a918d`  
		Last Modified: Fri, 01 Oct 2021 05:26:23 GMT  
		Size: 1.6 MB (1585830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2389b8a7dd566761cba6e2dc15b3fc69c13543880fc93dbf19d15619c461dad2`  
		Last Modified: Fri, 01 Oct 2021 05:26:20 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4107cbdbc866a69764051c7aae57edbfaa8754f1ab814924f894fb24795bf0d2`  
		Last Modified: Fri, 01 Oct 2021 05:26:20 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1abc07c11569f5fdfc3bd41ab8584879a293c570c6d10e80240ba609fbe5918`  
		Last Modified: Fri, 01 Oct 2021 05:26:31 GMT  
		Size: 72.6 MB (72609605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b160c6de4e1da109323527158924e3ed20ee08ffbc35fa30f621da4e1842a63`  
		Last Modified: Fri, 01 Oct 2021 05:26:20 GMT  
		Size: 5.6 KB (5609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0543f573ce8402a676c92fe1ae461f34d772ae08698e463551812b0a2879babc`  
		Last Modified: Fri, 01 Oct 2021 05:26:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d9b65ff8471c9f99c8c527e184a634a5fd9fe7c055219c6126842bd9307aa2ae
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104362815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea90b5b91095548619940d86462e72eeb25d738e12ebd464a616ad703541175f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:40 GMT
ADD file:35e2504756850fc1add00516fa89b0499b59c348457a96708eedb61313e7b25e in / 
# Fri, 01 Oct 2021 02:43:41 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:41:45 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 03:41:55 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:41:55 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 03:42:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 03:42:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 03:42:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:42:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 03:42:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 03:42:29 GMT
ARG MARIADB_MAJOR=10.2
# Fri, 01 Oct 2021 03:42:29 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 01 Oct 2021 03:42:29 GMT
ARG MARIADB_VERSION=1:10.2.40+maria~bionic
# Fri, 01 Oct 2021 03:42:29 GMT
ENV MARIADB_VERSION=1:10.2.40+maria~bionic
# Fri, 01 Oct 2021 03:42:29 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
# Fri, 01 Oct 2021 03:42:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 03:42:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 03:42:56 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 03:42:56 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 03:42:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Oct 2021 03:42:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 03:42:57 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 03:42:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f46992f278c2dd50c481ff60ce8528b6eb59016ac6243e1a7fb385c79c5944b9`  
		Last Modified: Fri, 01 Oct 2021 02:45:30 GMT  
		Size: 23.7 MB (23727476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2f5eee07061665f2228abc3a2728edd1e4154d6df13108b774b783e80f0e66`  
		Last Modified: Fri, 01 Oct 2021 03:46:30 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d367371c2390bcbc842695eaf3f40cce09f04619642c4b24f3c44ed3d52b6c`  
		Last Modified: Fri, 01 Oct 2021 03:46:29 GMT  
		Size: 4.4 MB (4395696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7506380fa349a5c0c64aefa19caa23a14d4a2c0fba39e1e33c9fbee85ed857`  
		Last Modified: Fri, 01 Oct 2021 03:46:28 GMT  
		Size: 3.2 MB (3204622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6538e9a7bc49ebcf8e6535bdc0738d136053609e8f3c5c9a5ecabd9f552b18`  
		Last Modified: Fri, 01 Oct 2021 03:46:28 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da46f0ea77b03886259bd98657e5307c555223078466fdffbcb8683f430c070`  
		Last Modified: Fri, 01 Oct 2021 03:46:28 GMT  
		Size: 1.5 MB (1532555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d09dd4e711e507d8a254bfa5b5e9c1607f64e647b7cd492c79d5d87a488218`  
		Last Modified: Fri, 01 Oct 2021 03:46:25 GMT  
		Size: 5.2 KB (5170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d53ed47ee11ab96617578a59a8e36273abda3d74c34b4779262b643895ae4be`  
		Last Modified: Fri, 01 Oct 2021 03:46:25 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d01f94244806aa25dd55875bc8b3215476ae8d2f3eb11860d5f876752c11a23`  
		Last Modified: Fri, 01 Oct 2021 03:46:37 GMT  
		Size: 71.5 MB (71489216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b4fa26ada886c1a4e2f56d8afa9e6ecfb72f646136b03161e7921341117749`  
		Last Modified: Fri, 01 Oct 2021 03:46:25 GMT  
		Size: 5.6 KB (5608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a845960e2ac4fc04dc156629e63af0cdb83d58f30547bc9a86f553caa4d24f9`  
		Last Modified: Fri, 01 Oct 2021 03:46:26 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a87355bbfcd8c4d277b81f614a424ae07e75c61cd4f907771fafd75c95734f6d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117673902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8c855f600de1dcf745c21fc2bad2a8c78a04b1b30e81059ceb8015b6831b98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Oct 2021 11:07:29 GMT
ADD file:fd96554dfb72307c3cf9292c343050a8b9f0848735b7555820f0068914ebd758 in / 
# Tue, 05 Oct 2021 11:07:35 GMT
CMD ["bash"]
# Wed, 06 Oct 2021 18:27:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Oct 2021 18:28:04 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 18:28:07 GMT
ENV GOSU_VERSION=1.13
# Wed, 06 Oct 2021 18:28:50 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Oct 2021 18:28:56 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Oct 2021 18:30:32 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 18:30:36 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Oct 2021 18:30:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Oct 2021 18:30:51 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 06 Oct 2021 18:30:54 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 06 Oct 2021 18:30:56 GMT
ARG MARIADB_VERSION=1:10.2.40+maria~bionic
# Wed, 06 Oct 2021 18:30:58 GMT
ENV MARIADB_VERSION=1:10.2.40+maria~bionic
# Wed, 06 Oct 2021 18:31:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
# Wed, 06 Oct 2021 18:31:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Oct 2021 18:32:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Oct 2021 18:32:58 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Oct 2021 18:33:01 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Wed, 06 Oct 2021 18:33:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 06 Oct 2021 18:33:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Oct 2021 18:33:40 GMT
EXPOSE 3306
# Wed, 06 Oct 2021 18:33:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:db28fc1e594e5598e665c54ac1b7fd602d86dddaf8bb237a72303cec22a9185c`  
		Last Modified: Tue, 05 Oct 2021 11:10:31 GMT  
		Size: 30.4 MB (30432921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508be09c006b6365ae7c5fc9b0593010a2d284d9b02e4f9ad77ee4f4209c8c0a`  
		Last Modified: Wed, 06 Oct 2021 18:37:35 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57bc7004e2371a404c5ff023b89e2ade70ef3581e3c7156807ac620fad13dbaf`  
		Last Modified: Wed, 06 Oct 2021 18:37:32 GMT  
		Size: 5.6 MB (5630476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0247b3a43e1d7479a934dd7064273de0a582a7b29cbbe3930976de3cdea14165`  
		Last Modified: Wed, 06 Oct 2021 18:37:32 GMT  
		Size: 3.5 MB (3529458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36f80bf4a4eb1f224d050821b3697d447a6684a83bd5474d805d269be98738a`  
		Last Modified: Wed, 06 Oct 2021 18:37:31 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c8e01754107b9697fb72ecd295ce381ffdbf045d9af0e8434896bbdfb99589`  
		Last Modified: Wed, 06 Oct 2021 18:37:32 GMT  
		Size: 1.9 MB (1938899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68c6f8634752aa2fad0a3bb47ecd3db12661c09a627f009b659af43d8b50693`  
		Last Modified: Wed, 06 Oct 2021 18:37:28 GMT  
		Size: 5.2 KB (5172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05753e4613d3ea1d36cd939dcb1df72b40d033867d856378e3bb83f4ab74f77e`  
		Last Modified: Wed, 06 Oct 2021 18:37:27 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b48f20163eab27b9baf9ec26b3653fc71506f35970677fcab2ed9a46cf41ef`  
		Last Modified: Wed, 06 Oct 2021 18:37:42 GMT  
		Size: 76.1 MB (76128891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9e3e320fa8bc28bbfe5b93681ab8640f37280697cd105ce8b6687c1b48b9edc`  
		Last Modified: Wed, 06 Oct 2021 18:37:28 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf75adc1fe0afd7e3946ed2ab76579aaa00cb5961dd57eb02fe88a7151ff240`  
		Last Modified: Wed, 06 Oct 2021 18:37:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.40`

```console
$ docker pull mariadb@sha256:82594695e7daacb7e59c2400b503073c8a79514e9b1e56b57f01986cbdf34bdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2.40` - linux; amd64

```console
$ docker pull mariadb@sha256:a528fb0b369f7dc138106ac7ff2d3500577d1be6cbee3a7261509bdbb7ee62d6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109274501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354c935e3d016be16ddc8baaebc97205b8c78a89230b00f06333a2ce62c0f0d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:23 GMT
ADD file:0d82cd095966e8ee78b593cb47a352eec842edb7bd9d9468e8a70154522447d1 in / 
# Fri, 01 Oct 2021 02:23:24 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:22:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 05:22:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:22:25 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 05:22:39 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 05:22:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 05:22:48 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:22:49 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 05:22:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 05:22:57 GMT
ARG MARIADB_MAJOR=10.2
# Fri, 01 Oct 2021 05:22:57 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 01 Oct 2021 05:22:57 GMT
ARG MARIADB_VERSION=1:10.2.40+maria~bionic
# Fri, 01 Oct 2021 05:22:58 GMT
ENV MARIADB_VERSION=1:10.2.40+maria~bionic
# Fri, 01 Oct 2021 05:22:58 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
# Fri, 01 Oct 2021 05:22:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 05:23:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 05:23:36 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 05:23:36 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 05:23:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Oct 2021 05:23:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 05:23:38 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 05:23:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:284055322776031bac33723839acb0db2d063a525ba4fa1fd268a831c7553b26`  
		Last Modified: Fri, 01 Oct 2021 02:25:02 GMT  
		Size: 26.7 MB (26705075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c939c6256f1f0a750da3d02b63d4aa63b9ac6f085a5b904ede35065e2f9074ad`  
		Last Modified: Fri, 01 Oct 2021 05:26:25 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b11a4bc2affe5918649c7ac2245c1ba21dc9f4ea8a536f01188e6e7a32bf30`  
		Last Modified: Fri, 01 Oct 2021 05:26:24 GMT  
		Size: 4.8 MB (4813381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec46f26e2520dcdcb3b1337a6f1d0324de5ca746cf496c2f58d1b3a999b0b3ee`  
		Last Modified: Fri, 01 Oct 2021 05:26:23 GMT  
		Size: 3.5 MB (3547363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c10147eb944f79d9fbf87b70609cf920a464f53924f34d5e0e221a7a301474`  
		Last Modified: Fri, 01 Oct 2021 05:26:22 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c518dbe68aa8249927d923eb729c649959ac6346fc141829fb1631d88a918d`  
		Last Modified: Fri, 01 Oct 2021 05:26:23 GMT  
		Size: 1.6 MB (1585830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2389b8a7dd566761cba6e2dc15b3fc69c13543880fc93dbf19d15619c461dad2`  
		Last Modified: Fri, 01 Oct 2021 05:26:20 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4107cbdbc866a69764051c7aae57edbfaa8754f1ab814924f894fb24795bf0d2`  
		Last Modified: Fri, 01 Oct 2021 05:26:20 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1abc07c11569f5fdfc3bd41ab8584879a293c570c6d10e80240ba609fbe5918`  
		Last Modified: Fri, 01 Oct 2021 05:26:31 GMT  
		Size: 72.6 MB (72609605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b160c6de4e1da109323527158924e3ed20ee08ffbc35fa30f621da4e1842a63`  
		Last Modified: Fri, 01 Oct 2021 05:26:20 GMT  
		Size: 5.6 KB (5609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0543f573ce8402a676c92fe1ae461f34d772ae08698e463551812b0a2879babc`  
		Last Modified: Fri, 01 Oct 2021 05:26:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.40` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d9b65ff8471c9f99c8c527e184a634a5fd9fe7c055219c6126842bd9307aa2ae
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104362815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea90b5b91095548619940d86462e72eeb25d738e12ebd464a616ad703541175f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:40 GMT
ADD file:35e2504756850fc1add00516fa89b0499b59c348457a96708eedb61313e7b25e in / 
# Fri, 01 Oct 2021 02:43:41 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:41:45 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 03:41:55 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:41:55 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 03:42:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 03:42:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 03:42:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:42:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 03:42:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 03:42:29 GMT
ARG MARIADB_MAJOR=10.2
# Fri, 01 Oct 2021 03:42:29 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 01 Oct 2021 03:42:29 GMT
ARG MARIADB_VERSION=1:10.2.40+maria~bionic
# Fri, 01 Oct 2021 03:42:29 GMT
ENV MARIADB_VERSION=1:10.2.40+maria~bionic
# Fri, 01 Oct 2021 03:42:29 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
# Fri, 01 Oct 2021 03:42:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 03:42:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 03:42:56 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 03:42:56 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 03:42:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Oct 2021 03:42:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 03:42:57 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 03:42:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f46992f278c2dd50c481ff60ce8528b6eb59016ac6243e1a7fb385c79c5944b9`  
		Last Modified: Fri, 01 Oct 2021 02:45:30 GMT  
		Size: 23.7 MB (23727476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2f5eee07061665f2228abc3a2728edd1e4154d6df13108b774b783e80f0e66`  
		Last Modified: Fri, 01 Oct 2021 03:46:30 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d367371c2390bcbc842695eaf3f40cce09f04619642c4b24f3c44ed3d52b6c`  
		Last Modified: Fri, 01 Oct 2021 03:46:29 GMT  
		Size: 4.4 MB (4395696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7506380fa349a5c0c64aefa19caa23a14d4a2c0fba39e1e33c9fbee85ed857`  
		Last Modified: Fri, 01 Oct 2021 03:46:28 GMT  
		Size: 3.2 MB (3204622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6538e9a7bc49ebcf8e6535bdc0738d136053609e8f3c5c9a5ecabd9f552b18`  
		Last Modified: Fri, 01 Oct 2021 03:46:28 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da46f0ea77b03886259bd98657e5307c555223078466fdffbcb8683f430c070`  
		Last Modified: Fri, 01 Oct 2021 03:46:28 GMT  
		Size: 1.5 MB (1532555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d09dd4e711e507d8a254bfa5b5e9c1607f64e647b7cd492c79d5d87a488218`  
		Last Modified: Fri, 01 Oct 2021 03:46:25 GMT  
		Size: 5.2 KB (5170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d53ed47ee11ab96617578a59a8e36273abda3d74c34b4779262b643895ae4be`  
		Last Modified: Fri, 01 Oct 2021 03:46:25 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d01f94244806aa25dd55875bc8b3215476ae8d2f3eb11860d5f876752c11a23`  
		Last Modified: Fri, 01 Oct 2021 03:46:37 GMT  
		Size: 71.5 MB (71489216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b4fa26ada886c1a4e2f56d8afa9e6ecfb72f646136b03161e7921341117749`  
		Last Modified: Fri, 01 Oct 2021 03:46:25 GMT  
		Size: 5.6 KB (5608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a845960e2ac4fc04dc156629e63af0cdb83d58f30547bc9a86f553caa4d24f9`  
		Last Modified: Fri, 01 Oct 2021 03:46:26 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.40` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a87355bbfcd8c4d277b81f614a424ae07e75c61cd4f907771fafd75c95734f6d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117673902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8c855f600de1dcf745c21fc2bad2a8c78a04b1b30e81059ceb8015b6831b98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Oct 2021 11:07:29 GMT
ADD file:fd96554dfb72307c3cf9292c343050a8b9f0848735b7555820f0068914ebd758 in / 
# Tue, 05 Oct 2021 11:07:35 GMT
CMD ["bash"]
# Wed, 06 Oct 2021 18:27:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Oct 2021 18:28:04 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 18:28:07 GMT
ENV GOSU_VERSION=1.13
# Wed, 06 Oct 2021 18:28:50 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Oct 2021 18:28:56 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Oct 2021 18:30:32 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 18:30:36 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Oct 2021 18:30:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Oct 2021 18:30:51 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 06 Oct 2021 18:30:54 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 06 Oct 2021 18:30:56 GMT
ARG MARIADB_VERSION=1:10.2.40+maria~bionic
# Wed, 06 Oct 2021 18:30:58 GMT
ENV MARIADB_VERSION=1:10.2.40+maria~bionic
# Wed, 06 Oct 2021 18:31:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
# Wed, 06 Oct 2021 18:31:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Oct 2021 18:32:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Oct 2021 18:32:58 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Oct 2021 18:33:01 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Wed, 06 Oct 2021 18:33:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 06 Oct 2021 18:33:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Oct 2021 18:33:40 GMT
EXPOSE 3306
# Wed, 06 Oct 2021 18:33:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:db28fc1e594e5598e665c54ac1b7fd602d86dddaf8bb237a72303cec22a9185c`  
		Last Modified: Tue, 05 Oct 2021 11:10:31 GMT  
		Size: 30.4 MB (30432921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508be09c006b6365ae7c5fc9b0593010a2d284d9b02e4f9ad77ee4f4209c8c0a`  
		Last Modified: Wed, 06 Oct 2021 18:37:35 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57bc7004e2371a404c5ff023b89e2ade70ef3581e3c7156807ac620fad13dbaf`  
		Last Modified: Wed, 06 Oct 2021 18:37:32 GMT  
		Size: 5.6 MB (5630476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0247b3a43e1d7479a934dd7064273de0a582a7b29cbbe3930976de3cdea14165`  
		Last Modified: Wed, 06 Oct 2021 18:37:32 GMT  
		Size: 3.5 MB (3529458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36f80bf4a4eb1f224d050821b3697d447a6684a83bd5474d805d269be98738a`  
		Last Modified: Wed, 06 Oct 2021 18:37:31 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c8e01754107b9697fb72ecd295ce381ffdbf045d9af0e8434896bbdfb99589`  
		Last Modified: Wed, 06 Oct 2021 18:37:32 GMT  
		Size: 1.9 MB (1938899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68c6f8634752aa2fad0a3bb47ecd3db12661c09a627f009b659af43d8b50693`  
		Last Modified: Wed, 06 Oct 2021 18:37:28 GMT  
		Size: 5.2 KB (5172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05753e4613d3ea1d36cd939dcb1df72b40d033867d856378e3bb83f4ab74f77e`  
		Last Modified: Wed, 06 Oct 2021 18:37:27 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b48f20163eab27b9baf9ec26b3653fc71506f35970677fcab2ed9a46cf41ef`  
		Last Modified: Wed, 06 Oct 2021 18:37:42 GMT  
		Size: 76.1 MB (76128891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9e3e320fa8bc28bbfe5b93681ab8640f37280697cd105ce8b6687c1b48b9edc`  
		Last Modified: Wed, 06 Oct 2021 18:37:28 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf75adc1fe0afd7e3946ed2ab76579aaa00cb5961dd57eb02fe88a7151ff240`  
		Last Modified: Wed, 06 Oct 2021 18:37:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.40-bionic`

```console
$ docker pull mariadb@sha256:82594695e7daacb7e59c2400b503073c8a79514e9b1e56b57f01986cbdf34bdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2.40-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:a528fb0b369f7dc138106ac7ff2d3500577d1be6cbee3a7261509bdbb7ee62d6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109274501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354c935e3d016be16ddc8baaebc97205b8c78a89230b00f06333a2ce62c0f0d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:23 GMT
ADD file:0d82cd095966e8ee78b593cb47a352eec842edb7bd9d9468e8a70154522447d1 in / 
# Fri, 01 Oct 2021 02:23:24 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:22:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 05:22:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:22:25 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 05:22:39 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 05:22:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 05:22:48 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:22:49 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 05:22:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 05:22:57 GMT
ARG MARIADB_MAJOR=10.2
# Fri, 01 Oct 2021 05:22:57 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 01 Oct 2021 05:22:57 GMT
ARG MARIADB_VERSION=1:10.2.40+maria~bionic
# Fri, 01 Oct 2021 05:22:58 GMT
ENV MARIADB_VERSION=1:10.2.40+maria~bionic
# Fri, 01 Oct 2021 05:22:58 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
# Fri, 01 Oct 2021 05:22:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 05:23:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 05:23:36 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 05:23:36 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 05:23:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Oct 2021 05:23:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 05:23:38 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 05:23:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:284055322776031bac33723839acb0db2d063a525ba4fa1fd268a831c7553b26`  
		Last Modified: Fri, 01 Oct 2021 02:25:02 GMT  
		Size: 26.7 MB (26705075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c939c6256f1f0a750da3d02b63d4aa63b9ac6f085a5b904ede35065e2f9074ad`  
		Last Modified: Fri, 01 Oct 2021 05:26:25 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b11a4bc2affe5918649c7ac2245c1ba21dc9f4ea8a536f01188e6e7a32bf30`  
		Last Modified: Fri, 01 Oct 2021 05:26:24 GMT  
		Size: 4.8 MB (4813381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec46f26e2520dcdcb3b1337a6f1d0324de5ca746cf496c2f58d1b3a999b0b3ee`  
		Last Modified: Fri, 01 Oct 2021 05:26:23 GMT  
		Size: 3.5 MB (3547363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c10147eb944f79d9fbf87b70609cf920a464f53924f34d5e0e221a7a301474`  
		Last Modified: Fri, 01 Oct 2021 05:26:22 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c518dbe68aa8249927d923eb729c649959ac6346fc141829fb1631d88a918d`  
		Last Modified: Fri, 01 Oct 2021 05:26:23 GMT  
		Size: 1.6 MB (1585830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2389b8a7dd566761cba6e2dc15b3fc69c13543880fc93dbf19d15619c461dad2`  
		Last Modified: Fri, 01 Oct 2021 05:26:20 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4107cbdbc866a69764051c7aae57edbfaa8754f1ab814924f894fb24795bf0d2`  
		Last Modified: Fri, 01 Oct 2021 05:26:20 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1abc07c11569f5fdfc3bd41ab8584879a293c570c6d10e80240ba609fbe5918`  
		Last Modified: Fri, 01 Oct 2021 05:26:31 GMT  
		Size: 72.6 MB (72609605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b160c6de4e1da109323527158924e3ed20ee08ffbc35fa30f621da4e1842a63`  
		Last Modified: Fri, 01 Oct 2021 05:26:20 GMT  
		Size: 5.6 KB (5609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0543f573ce8402a676c92fe1ae461f34d772ae08698e463551812b0a2879babc`  
		Last Modified: Fri, 01 Oct 2021 05:26:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.40-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d9b65ff8471c9f99c8c527e184a634a5fd9fe7c055219c6126842bd9307aa2ae
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104362815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea90b5b91095548619940d86462e72eeb25d738e12ebd464a616ad703541175f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:40 GMT
ADD file:35e2504756850fc1add00516fa89b0499b59c348457a96708eedb61313e7b25e in / 
# Fri, 01 Oct 2021 02:43:41 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:41:45 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 03:41:55 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:41:55 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 03:42:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 03:42:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 03:42:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:42:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 03:42:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 03:42:29 GMT
ARG MARIADB_MAJOR=10.2
# Fri, 01 Oct 2021 03:42:29 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 01 Oct 2021 03:42:29 GMT
ARG MARIADB_VERSION=1:10.2.40+maria~bionic
# Fri, 01 Oct 2021 03:42:29 GMT
ENV MARIADB_VERSION=1:10.2.40+maria~bionic
# Fri, 01 Oct 2021 03:42:29 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
# Fri, 01 Oct 2021 03:42:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 03:42:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 03:42:56 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 03:42:56 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 03:42:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Oct 2021 03:42:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 03:42:57 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 03:42:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f46992f278c2dd50c481ff60ce8528b6eb59016ac6243e1a7fb385c79c5944b9`  
		Last Modified: Fri, 01 Oct 2021 02:45:30 GMT  
		Size: 23.7 MB (23727476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2f5eee07061665f2228abc3a2728edd1e4154d6df13108b774b783e80f0e66`  
		Last Modified: Fri, 01 Oct 2021 03:46:30 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d367371c2390bcbc842695eaf3f40cce09f04619642c4b24f3c44ed3d52b6c`  
		Last Modified: Fri, 01 Oct 2021 03:46:29 GMT  
		Size: 4.4 MB (4395696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7506380fa349a5c0c64aefa19caa23a14d4a2c0fba39e1e33c9fbee85ed857`  
		Last Modified: Fri, 01 Oct 2021 03:46:28 GMT  
		Size: 3.2 MB (3204622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6538e9a7bc49ebcf8e6535bdc0738d136053609e8f3c5c9a5ecabd9f552b18`  
		Last Modified: Fri, 01 Oct 2021 03:46:28 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da46f0ea77b03886259bd98657e5307c555223078466fdffbcb8683f430c070`  
		Last Modified: Fri, 01 Oct 2021 03:46:28 GMT  
		Size: 1.5 MB (1532555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d09dd4e711e507d8a254bfa5b5e9c1607f64e647b7cd492c79d5d87a488218`  
		Last Modified: Fri, 01 Oct 2021 03:46:25 GMT  
		Size: 5.2 KB (5170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d53ed47ee11ab96617578a59a8e36273abda3d74c34b4779262b643895ae4be`  
		Last Modified: Fri, 01 Oct 2021 03:46:25 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d01f94244806aa25dd55875bc8b3215476ae8d2f3eb11860d5f876752c11a23`  
		Last Modified: Fri, 01 Oct 2021 03:46:37 GMT  
		Size: 71.5 MB (71489216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b4fa26ada886c1a4e2f56d8afa9e6ecfb72f646136b03161e7921341117749`  
		Last Modified: Fri, 01 Oct 2021 03:46:25 GMT  
		Size: 5.6 KB (5608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a845960e2ac4fc04dc156629e63af0cdb83d58f30547bc9a86f553caa4d24f9`  
		Last Modified: Fri, 01 Oct 2021 03:46:26 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.40-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a87355bbfcd8c4d277b81f614a424ae07e75c61cd4f907771fafd75c95734f6d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117673902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8c855f600de1dcf745c21fc2bad2a8c78a04b1b30e81059ceb8015b6831b98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Oct 2021 11:07:29 GMT
ADD file:fd96554dfb72307c3cf9292c343050a8b9f0848735b7555820f0068914ebd758 in / 
# Tue, 05 Oct 2021 11:07:35 GMT
CMD ["bash"]
# Wed, 06 Oct 2021 18:27:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Oct 2021 18:28:04 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 18:28:07 GMT
ENV GOSU_VERSION=1.13
# Wed, 06 Oct 2021 18:28:50 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Oct 2021 18:28:56 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Oct 2021 18:30:32 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 18:30:36 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Oct 2021 18:30:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Oct 2021 18:30:51 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 06 Oct 2021 18:30:54 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 06 Oct 2021 18:30:56 GMT
ARG MARIADB_VERSION=1:10.2.40+maria~bionic
# Wed, 06 Oct 2021 18:30:58 GMT
ENV MARIADB_VERSION=1:10.2.40+maria~bionic
# Wed, 06 Oct 2021 18:31:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
# Wed, 06 Oct 2021 18:31:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Oct 2021 18:32:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Oct 2021 18:32:58 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Oct 2021 18:33:01 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Wed, 06 Oct 2021 18:33:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 06 Oct 2021 18:33:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Oct 2021 18:33:40 GMT
EXPOSE 3306
# Wed, 06 Oct 2021 18:33:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:db28fc1e594e5598e665c54ac1b7fd602d86dddaf8bb237a72303cec22a9185c`  
		Last Modified: Tue, 05 Oct 2021 11:10:31 GMT  
		Size: 30.4 MB (30432921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508be09c006b6365ae7c5fc9b0593010a2d284d9b02e4f9ad77ee4f4209c8c0a`  
		Last Modified: Wed, 06 Oct 2021 18:37:35 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57bc7004e2371a404c5ff023b89e2ade70ef3581e3c7156807ac620fad13dbaf`  
		Last Modified: Wed, 06 Oct 2021 18:37:32 GMT  
		Size: 5.6 MB (5630476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0247b3a43e1d7479a934dd7064273de0a582a7b29cbbe3930976de3cdea14165`  
		Last Modified: Wed, 06 Oct 2021 18:37:32 GMT  
		Size: 3.5 MB (3529458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36f80bf4a4eb1f224d050821b3697d447a6684a83bd5474d805d269be98738a`  
		Last Modified: Wed, 06 Oct 2021 18:37:31 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c8e01754107b9697fb72ecd295ce381ffdbf045d9af0e8434896bbdfb99589`  
		Last Modified: Wed, 06 Oct 2021 18:37:32 GMT  
		Size: 1.9 MB (1938899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68c6f8634752aa2fad0a3bb47ecd3db12661c09a627f009b659af43d8b50693`  
		Last Modified: Wed, 06 Oct 2021 18:37:28 GMT  
		Size: 5.2 KB (5172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05753e4613d3ea1d36cd939dcb1df72b40d033867d856378e3bb83f4ab74f77e`  
		Last Modified: Wed, 06 Oct 2021 18:37:27 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b48f20163eab27b9baf9ec26b3653fc71506f35970677fcab2ed9a46cf41ef`  
		Last Modified: Wed, 06 Oct 2021 18:37:42 GMT  
		Size: 76.1 MB (76128891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9e3e320fa8bc28bbfe5b93681ab8640f37280697cd105ce8b6687c1b48b9edc`  
		Last Modified: Wed, 06 Oct 2021 18:37:28 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf75adc1fe0afd7e3946ed2ab76579aaa00cb5961dd57eb02fe88a7151ff240`  
		Last Modified: Wed, 06 Oct 2021 18:37:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3`

```console
$ docker pull mariadb@sha256:f0845fe533e3be271f22dfba9ee99f641979aae888add4b4ac6664cbde674379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3` - linux; amd64

```console
$ docker pull mariadb@sha256:40b58c630b688f2af308adf249a24dba177e5fafa236b63443f16a2c829c35c2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120017318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f9ac3252e08082db47429140ef6907f8b887f6600b729f151f6f14a73e0a08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:19:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 05:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:18 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 05:19:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 05:19:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 05:19:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:39 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 05:19:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 05:21:33 GMT
ARG MARIADB_MAJOR=10.3
# Fri, 01 Oct 2021 05:21:33 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 01 Oct 2021 05:21:33 GMT
ARG MARIADB_VERSION=1:10.3.31+maria~focal
# Fri, 01 Oct 2021 05:21:33 GMT
ENV MARIADB_VERSION=1:10.3.31+maria~focal
# Fri, 01 Oct 2021 05:21:33 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 05:21:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 05:22:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 05:22:03 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 05:22:03 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 05:22:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Oct 2021 05:22:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 05:22:04 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 05:22:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6f45e0fb03b087254fb0750ec2bbfbc7ea10f3eaaa2c3381f2ef6b3cf2c32b`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a10760fd6ecff1db568c4df08e4add59ea3424ae8b2ed2ac557f5239fa74d`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 5.5 MB (5489340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0645d99211dd422dc4b2c52d1005a518b5d9c76409584ee75faf26c78de36b`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 3.6 MB (3582638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff899ddf1cc12eb3161fb924245c2cdb096fe9cadd0b73128f7d3e45e4a0e6c`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e10ba5def77eae105b1dfab52bd41d16cba2895929673658ec8fedc7d8408e`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.3 MB (2274765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef565721758b7adafc1e282adeddbe68df6d6631699124a860c60f5c507840b4`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3c670c6f24cc3e29abf3af268073c6ce8dbbf9f684d40af076e3549e763252`  
		Last Modified: Fri, 01 Oct 2021 05:25:52 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7d08c7f33a237d041cc7644173cf3c895b5fdcfa2e1e2c1f8e1ed4a57c724f`  
		Last Modified: Fri, 01 Oct 2021 05:26:04 GMT  
		Size: 80.1 MB (80091210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc356da8c13b498fc481a453aaf0c3b3222c3993f398414949ec468bdb6f891`  
		Last Modified: Fri, 01 Oct 2021 05:25:52 GMT  
		Size: 5.6 KB (5611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37cb59f9aa1ae9c3f71acc88d526794713ad3d5f93f37e61280241369278c1ae`  
		Last Modified: Fri, 01 Oct 2021 05:25:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:bbd3a3cf613358fbb05108dd7dc9ac6e902e1ef8617e7ec5928ec759f6dc4d17
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117623997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77c013d6bf7007d3d94c458ab3918e9c68ead56a2fdc71efb870a3d229ef5f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:38:47 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 03:38:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:38:56 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 03:39:11 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 03:39:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 03:39:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:39:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 03:39:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 03:41:07 GMT
ARG MARIADB_MAJOR=10.3
# Fri, 01 Oct 2021 03:41:08 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 01 Oct 2021 03:41:08 GMT
ARG MARIADB_VERSION=1:10.3.31+maria~focal
# Fri, 01 Oct 2021 03:41:08 GMT
ENV MARIADB_VERSION=1:10.3.31+maria~focal
# Fri, 01 Oct 2021 03:41:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 03:41:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 03:41:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 03:41:36 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 03:41:37 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 03:41:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Oct 2021 03:41:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 03:41:38 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 03:41:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d5ae241c1f10925c65b1658513761cd873e86632ea54cd491a17314c717db9`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1337b7de0aecaa84469be03f6aca5f4716813a7f70d6df52ada4f37e67dce98`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 5.5 MB (5455225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720ecfb64bf9977e96130e89f4d49759a1b9577aabaa5c864b0f7a3c0473f778`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 3.4 MB (3368539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba0c987cf142da7e613c8eb5506412f33e85d62e8b737d82ae8a86dad1a3dd1`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1cd2ca1d8beab7fe86d456206b59ee252c55fd199373f2caae49c71ec65a2a`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.2 MB (2203545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9328b4fc02fb1261cd4016d0e4d31dd6528b268e170d8278afbd062e3a96fa1`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c4a4c53fccbe5fcacb1204de248af27df80039edf6f327fb2a1c3bbe4f3e55`  
		Last Modified: Fri, 01 Oct 2021 03:45:52 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003e43ca6fa30ba8ffed812ee011dfa91fd4dc750ba1be39c62d8f55de817c18`  
		Last Modified: Fri, 01 Oct 2021 03:46:06 GMT  
		Size: 79.4 MB (79413829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0aaf0a90cfbb05c1065e5881d45812b427c0561302274e66bc5bf5170a44ece`  
		Last Modified: Fri, 01 Oct 2021 03:45:52 GMT  
		Size: 5.6 KB (5611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da02843ac443d5f1f0505e68cef6d9cfcd7107a9fbb28d065d4efa119a25c9b`  
		Last Modified: Fri, 01 Oct 2021 03:45:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; ppc64le

```console
$ docker pull mariadb@sha256:eabb2e81a20381ca05c1eef2015ba97f7ad63de9a30d74add3c07174ceb70ab7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130878512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b14c8cd50591ce95eaff04590dcce413136bcdf53a1d7e29f4664791de54dfd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:34:53 GMT
ENV GOSU_VERSION=1.13
# Sat, 16 Oct 2021 01:35:28 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 01:35:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 01:36:02 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:36:03 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 16 Oct 2021 01:36:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 01:45:24 GMT
ARG MARIADB_MAJOR=10.3
# Sat, 16 Oct 2021 01:45:26 GMT
ENV MARIADB_MAJOR=10.3
# Sat, 16 Oct 2021 01:45:30 GMT
ARG MARIADB_VERSION=1:10.3.31+maria~focal
# Sat, 16 Oct 2021 01:45:31 GMT
ENV MARIADB_VERSION=1:10.3.31+maria~focal
# Sat, 16 Oct 2021 01:45:34 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
# Sat, 16 Oct 2021 01:45:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 16 Oct 2021 01:47:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 16 Oct 2021 01:48:00 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Oct 2021 01:48:01 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:48:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 16 Oct 2021 01:48:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Oct 2021 01:48:17 GMT
EXPOSE 3306
# Sat, 16 Oct 2021 01:48:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bdbddf0ed762c90ab4fcfe1f42007a96e4f90ca4f0765dfcec52213a3f5c12`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 3.7 MB (3670760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cc95e86fb5ab1bda9839a1ecbd3c2d607bc6cfc5155f33bf32c9d7827ec98b`  
		Last Modified: Sat, 16 Oct 2021 01:49:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe2cefdba07cb9fc803227a545d4fcc196038c1020de7698bf4e333d9056cbd`  
		Last Modified: Sat, 16 Oct 2021 01:49:28 GMT  
		Size: 2.6 MB (2573066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab77c7b0e7b171541e9f7f813ef81190ef39151aea54bfe2b64f8c191ce672c`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94aeb2fd007f06d10435736a0bd9fae69670ff9c01bc11e62f75e5fea4653129`  
		Last Modified: Sat, 16 Oct 2021 01:51:28 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e393cff902c3ca290ce3dbad73eceaf35a4548496b5944e1fcd51253e5fcf022`  
		Last Modified: Sat, 16 Oct 2021 01:51:45 GMT  
		Size: 84.7 MB (84669015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9afc7f203a71d7290d7ab97ce69fc1691c8ef75f8582f449060a77a9ca89d1`  
		Last Modified: Sat, 16 Oct 2021 01:51:29 GMT  
		Size: 5.6 KB (5610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc4f496ad3cc84a892fb9157e7341f3c85c2fd8d8a0251e3578987bc804d6a9`  
		Last Modified: Sat, 16 Oct 2021 01:51:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3-focal`

```console
$ docker pull mariadb@sha256:f0845fe533e3be271f22dfba9ee99f641979aae888add4b4ac6664cbde674379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:40b58c630b688f2af308adf249a24dba177e5fafa236b63443f16a2c829c35c2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120017318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f9ac3252e08082db47429140ef6907f8b887f6600b729f151f6f14a73e0a08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:19:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 05:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:18 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 05:19:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 05:19:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 05:19:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:39 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 05:19:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 05:21:33 GMT
ARG MARIADB_MAJOR=10.3
# Fri, 01 Oct 2021 05:21:33 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 01 Oct 2021 05:21:33 GMT
ARG MARIADB_VERSION=1:10.3.31+maria~focal
# Fri, 01 Oct 2021 05:21:33 GMT
ENV MARIADB_VERSION=1:10.3.31+maria~focal
# Fri, 01 Oct 2021 05:21:33 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 05:21:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 05:22:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 05:22:03 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 05:22:03 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 05:22:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Oct 2021 05:22:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 05:22:04 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 05:22:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6f45e0fb03b087254fb0750ec2bbfbc7ea10f3eaaa2c3381f2ef6b3cf2c32b`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a10760fd6ecff1db568c4df08e4add59ea3424ae8b2ed2ac557f5239fa74d`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 5.5 MB (5489340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0645d99211dd422dc4b2c52d1005a518b5d9c76409584ee75faf26c78de36b`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 3.6 MB (3582638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff899ddf1cc12eb3161fb924245c2cdb096fe9cadd0b73128f7d3e45e4a0e6c`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e10ba5def77eae105b1dfab52bd41d16cba2895929673658ec8fedc7d8408e`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.3 MB (2274765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef565721758b7adafc1e282adeddbe68df6d6631699124a860c60f5c507840b4`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3c670c6f24cc3e29abf3af268073c6ce8dbbf9f684d40af076e3549e763252`  
		Last Modified: Fri, 01 Oct 2021 05:25:52 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7d08c7f33a237d041cc7644173cf3c895b5fdcfa2e1e2c1f8e1ed4a57c724f`  
		Last Modified: Fri, 01 Oct 2021 05:26:04 GMT  
		Size: 80.1 MB (80091210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc356da8c13b498fc481a453aaf0c3b3222c3993f398414949ec468bdb6f891`  
		Last Modified: Fri, 01 Oct 2021 05:25:52 GMT  
		Size: 5.6 KB (5611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37cb59f9aa1ae9c3f71acc88d526794713ad3d5f93f37e61280241369278c1ae`  
		Last Modified: Fri, 01 Oct 2021 05:25:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:bbd3a3cf613358fbb05108dd7dc9ac6e902e1ef8617e7ec5928ec759f6dc4d17
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117623997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77c013d6bf7007d3d94c458ab3918e9c68ead56a2fdc71efb870a3d229ef5f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:38:47 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 03:38:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:38:56 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 03:39:11 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 03:39:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 03:39:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:39:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 03:39:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 03:41:07 GMT
ARG MARIADB_MAJOR=10.3
# Fri, 01 Oct 2021 03:41:08 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 01 Oct 2021 03:41:08 GMT
ARG MARIADB_VERSION=1:10.3.31+maria~focal
# Fri, 01 Oct 2021 03:41:08 GMT
ENV MARIADB_VERSION=1:10.3.31+maria~focal
# Fri, 01 Oct 2021 03:41:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 03:41:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 03:41:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 03:41:36 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 03:41:37 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 03:41:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Oct 2021 03:41:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 03:41:38 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 03:41:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d5ae241c1f10925c65b1658513761cd873e86632ea54cd491a17314c717db9`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1337b7de0aecaa84469be03f6aca5f4716813a7f70d6df52ada4f37e67dce98`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 5.5 MB (5455225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720ecfb64bf9977e96130e89f4d49759a1b9577aabaa5c864b0f7a3c0473f778`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 3.4 MB (3368539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba0c987cf142da7e613c8eb5506412f33e85d62e8b737d82ae8a86dad1a3dd1`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1cd2ca1d8beab7fe86d456206b59ee252c55fd199373f2caae49c71ec65a2a`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.2 MB (2203545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9328b4fc02fb1261cd4016d0e4d31dd6528b268e170d8278afbd062e3a96fa1`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c4a4c53fccbe5fcacb1204de248af27df80039edf6f327fb2a1c3bbe4f3e55`  
		Last Modified: Fri, 01 Oct 2021 03:45:52 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003e43ca6fa30ba8ffed812ee011dfa91fd4dc750ba1be39c62d8f55de817c18`  
		Last Modified: Fri, 01 Oct 2021 03:46:06 GMT  
		Size: 79.4 MB (79413829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0aaf0a90cfbb05c1065e5881d45812b427c0561302274e66bc5bf5170a44ece`  
		Last Modified: Fri, 01 Oct 2021 03:45:52 GMT  
		Size: 5.6 KB (5611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da02843ac443d5f1f0505e68cef6d9cfcd7107a9fbb28d065d4efa119a25c9b`  
		Last Modified: Fri, 01 Oct 2021 03:45:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:eabb2e81a20381ca05c1eef2015ba97f7ad63de9a30d74add3c07174ceb70ab7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130878512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b14c8cd50591ce95eaff04590dcce413136bcdf53a1d7e29f4664791de54dfd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:34:53 GMT
ENV GOSU_VERSION=1.13
# Sat, 16 Oct 2021 01:35:28 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 01:35:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 01:36:02 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:36:03 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 16 Oct 2021 01:36:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 01:45:24 GMT
ARG MARIADB_MAJOR=10.3
# Sat, 16 Oct 2021 01:45:26 GMT
ENV MARIADB_MAJOR=10.3
# Sat, 16 Oct 2021 01:45:30 GMT
ARG MARIADB_VERSION=1:10.3.31+maria~focal
# Sat, 16 Oct 2021 01:45:31 GMT
ENV MARIADB_VERSION=1:10.3.31+maria~focal
# Sat, 16 Oct 2021 01:45:34 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
# Sat, 16 Oct 2021 01:45:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 16 Oct 2021 01:47:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 16 Oct 2021 01:48:00 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Oct 2021 01:48:01 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:48:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 16 Oct 2021 01:48:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Oct 2021 01:48:17 GMT
EXPOSE 3306
# Sat, 16 Oct 2021 01:48:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bdbddf0ed762c90ab4fcfe1f42007a96e4f90ca4f0765dfcec52213a3f5c12`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 3.7 MB (3670760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cc95e86fb5ab1bda9839a1ecbd3c2d607bc6cfc5155f33bf32c9d7827ec98b`  
		Last Modified: Sat, 16 Oct 2021 01:49:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe2cefdba07cb9fc803227a545d4fcc196038c1020de7698bf4e333d9056cbd`  
		Last Modified: Sat, 16 Oct 2021 01:49:28 GMT  
		Size: 2.6 MB (2573066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab77c7b0e7b171541e9f7f813ef81190ef39151aea54bfe2b64f8c191ce672c`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94aeb2fd007f06d10435736a0bd9fae69670ff9c01bc11e62f75e5fea4653129`  
		Last Modified: Sat, 16 Oct 2021 01:51:28 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e393cff902c3ca290ce3dbad73eceaf35a4548496b5944e1fcd51253e5fcf022`  
		Last Modified: Sat, 16 Oct 2021 01:51:45 GMT  
		Size: 84.7 MB (84669015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9afc7f203a71d7290d7ab97ce69fc1691c8ef75f8582f449060a77a9ca89d1`  
		Last Modified: Sat, 16 Oct 2021 01:51:29 GMT  
		Size: 5.6 KB (5610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc4f496ad3cc84a892fb9157e7341f3c85c2fd8d8a0251e3578987bc804d6a9`  
		Last Modified: Sat, 16 Oct 2021 01:51:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.31`

```console
$ docker pull mariadb@sha256:f0845fe533e3be271f22dfba9ee99f641979aae888add4b4ac6664cbde674379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.31` - linux; amd64

```console
$ docker pull mariadb@sha256:40b58c630b688f2af308adf249a24dba177e5fafa236b63443f16a2c829c35c2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120017318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f9ac3252e08082db47429140ef6907f8b887f6600b729f151f6f14a73e0a08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:19:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 05:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:18 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 05:19:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 05:19:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 05:19:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:39 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 05:19:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 05:21:33 GMT
ARG MARIADB_MAJOR=10.3
# Fri, 01 Oct 2021 05:21:33 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 01 Oct 2021 05:21:33 GMT
ARG MARIADB_VERSION=1:10.3.31+maria~focal
# Fri, 01 Oct 2021 05:21:33 GMT
ENV MARIADB_VERSION=1:10.3.31+maria~focal
# Fri, 01 Oct 2021 05:21:33 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 05:21:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 05:22:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 05:22:03 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 05:22:03 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 05:22:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Oct 2021 05:22:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 05:22:04 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 05:22:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6f45e0fb03b087254fb0750ec2bbfbc7ea10f3eaaa2c3381f2ef6b3cf2c32b`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a10760fd6ecff1db568c4df08e4add59ea3424ae8b2ed2ac557f5239fa74d`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 5.5 MB (5489340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0645d99211dd422dc4b2c52d1005a518b5d9c76409584ee75faf26c78de36b`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 3.6 MB (3582638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff899ddf1cc12eb3161fb924245c2cdb096fe9cadd0b73128f7d3e45e4a0e6c`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e10ba5def77eae105b1dfab52bd41d16cba2895929673658ec8fedc7d8408e`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.3 MB (2274765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef565721758b7adafc1e282adeddbe68df6d6631699124a860c60f5c507840b4`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3c670c6f24cc3e29abf3af268073c6ce8dbbf9f684d40af076e3549e763252`  
		Last Modified: Fri, 01 Oct 2021 05:25:52 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7d08c7f33a237d041cc7644173cf3c895b5fdcfa2e1e2c1f8e1ed4a57c724f`  
		Last Modified: Fri, 01 Oct 2021 05:26:04 GMT  
		Size: 80.1 MB (80091210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc356da8c13b498fc481a453aaf0c3b3222c3993f398414949ec468bdb6f891`  
		Last Modified: Fri, 01 Oct 2021 05:25:52 GMT  
		Size: 5.6 KB (5611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37cb59f9aa1ae9c3f71acc88d526794713ad3d5f93f37e61280241369278c1ae`  
		Last Modified: Fri, 01 Oct 2021 05:25:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.31` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:bbd3a3cf613358fbb05108dd7dc9ac6e902e1ef8617e7ec5928ec759f6dc4d17
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117623997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77c013d6bf7007d3d94c458ab3918e9c68ead56a2fdc71efb870a3d229ef5f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:38:47 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 03:38:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:38:56 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 03:39:11 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 03:39:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 03:39:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:39:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 03:39:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 03:41:07 GMT
ARG MARIADB_MAJOR=10.3
# Fri, 01 Oct 2021 03:41:08 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 01 Oct 2021 03:41:08 GMT
ARG MARIADB_VERSION=1:10.3.31+maria~focal
# Fri, 01 Oct 2021 03:41:08 GMT
ENV MARIADB_VERSION=1:10.3.31+maria~focal
# Fri, 01 Oct 2021 03:41:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 03:41:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 03:41:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 03:41:36 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 03:41:37 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 03:41:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Oct 2021 03:41:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 03:41:38 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 03:41:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d5ae241c1f10925c65b1658513761cd873e86632ea54cd491a17314c717db9`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1337b7de0aecaa84469be03f6aca5f4716813a7f70d6df52ada4f37e67dce98`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 5.5 MB (5455225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720ecfb64bf9977e96130e89f4d49759a1b9577aabaa5c864b0f7a3c0473f778`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 3.4 MB (3368539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba0c987cf142da7e613c8eb5506412f33e85d62e8b737d82ae8a86dad1a3dd1`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1cd2ca1d8beab7fe86d456206b59ee252c55fd199373f2caae49c71ec65a2a`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.2 MB (2203545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9328b4fc02fb1261cd4016d0e4d31dd6528b268e170d8278afbd062e3a96fa1`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c4a4c53fccbe5fcacb1204de248af27df80039edf6f327fb2a1c3bbe4f3e55`  
		Last Modified: Fri, 01 Oct 2021 03:45:52 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003e43ca6fa30ba8ffed812ee011dfa91fd4dc750ba1be39c62d8f55de817c18`  
		Last Modified: Fri, 01 Oct 2021 03:46:06 GMT  
		Size: 79.4 MB (79413829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0aaf0a90cfbb05c1065e5881d45812b427c0561302274e66bc5bf5170a44ece`  
		Last Modified: Fri, 01 Oct 2021 03:45:52 GMT  
		Size: 5.6 KB (5611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da02843ac443d5f1f0505e68cef6d9cfcd7107a9fbb28d065d4efa119a25c9b`  
		Last Modified: Fri, 01 Oct 2021 03:45:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.31` - linux; ppc64le

```console
$ docker pull mariadb@sha256:eabb2e81a20381ca05c1eef2015ba97f7ad63de9a30d74add3c07174ceb70ab7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130878512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b14c8cd50591ce95eaff04590dcce413136bcdf53a1d7e29f4664791de54dfd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:34:53 GMT
ENV GOSU_VERSION=1.13
# Sat, 16 Oct 2021 01:35:28 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 01:35:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 01:36:02 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:36:03 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 16 Oct 2021 01:36:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 01:45:24 GMT
ARG MARIADB_MAJOR=10.3
# Sat, 16 Oct 2021 01:45:26 GMT
ENV MARIADB_MAJOR=10.3
# Sat, 16 Oct 2021 01:45:30 GMT
ARG MARIADB_VERSION=1:10.3.31+maria~focal
# Sat, 16 Oct 2021 01:45:31 GMT
ENV MARIADB_VERSION=1:10.3.31+maria~focal
# Sat, 16 Oct 2021 01:45:34 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
# Sat, 16 Oct 2021 01:45:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 16 Oct 2021 01:47:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 16 Oct 2021 01:48:00 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Oct 2021 01:48:01 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:48:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 16 Oct 2021 01:48:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Oct 2021 01:48:17 GMT
EXPOSE 3306
# Sat, 16 Oct 2021 01:48:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bdbddf0ed762c90ab4fcfe1f42007a96e4f90ca4f0765dfcec52213a3f5c12`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 3.7 MB (3670760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cc95e86fb5ab1bda9839a1ecbd3c2d607bc6cfc5155f33bf32c9d7827ec98b`  
		Last Modified: Sat, 16 Oct 2021 01:49:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe2cefdba07cb9fc803227a545d4fcc196038c1020de7698bf4e333d9056cbd`  
		Last Modified: Sat, 16 Oct 2021 01:49:28 GMT  
		Size: 2.6 MB (2573066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab77c7b0e7b171541e9f7f813ef81190ef39151aea54bfe2b64f8c191ce672c`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94aeb2fd007f06d10435736a0bd9fae69670ff9c01bc11e62f75e5fea4653129`  
		Last Modified: Sat, 16 Oct 2021 01:51:28 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e393cff902c3ca290ce3dbad73eceaf35a4548496b5944e1fcd51253e5fcf022`  
		Last Modified: Sat, 16 Oct 2021 01:51:45 GMT  
		Size: 84.7 MB (84669015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9afc7f203a71d7290d7ab97ce69fc1691c8ef75f8582f449060a77a9ca89d1`  
		Last Modified: Sat, 16 Oct 2021 01:51:29 GMT  
		Size: 5.6 KB (5610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc4f496ad3cc84a892fb9157e7341f3c85c2fd8d8a0251e3578987bc804d6a9`  
		Last Modified: Sat, 16 Oct 2021 01:51:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.31-focal`

```console
$ docker pull mariadb@sha256:f0845fe533e3be271f22dfba9ee99f641979aae888add4b4ac6664cbde674379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.31-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:40b58c630b688f2af308adf249a24dba177e5fafa236b63443f16a2c829c35c2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120017318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f9ac3252e08082db47429140ef6907f8b887f6600b729f151f6f14a73e0a08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:19:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 05:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:18 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 05:19:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 05:19:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 05:19:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:39 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 05:19:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 05:21:33 GMT
ARG MARIADB_MAJOR=10.3
# Fri, 01 Oct 2021 05:21:33 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 01 Oct 2021 05:21:33 GMT
ARG MARIADB_VERSION=1:10.3.31+maria~focal
# Fri, 01 Oct 2021 05:21:33 GMT
ENV MARIADB_VERSION=1:10.3.31+maria~focal
# Fri, 01 Oct 2021 05:21:33 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 05:21:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 05:22:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 05:22:03 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 05:22:03 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 05:22:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Oct 2021 05:22:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 05:22:04 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 05:22:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6f45e0fb03b087254fb0750ec2bbfbc7ea10f3eaaa2c3381f2ef6b3cf2c32b`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a10760fd6ecff1db568c4df08e4add59ea3424ae8b2ed2ac557f5239fa74d`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 5.5 MB (5489340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0645d99211dd422dc4b2c52d1005a518b5d9c76409584ee75faf26c78de36b`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 3.6 MB (3582638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff899ddf1cc12eb3161fb924245c2cdb096fe9cadd0b73128f7d3e45e4a0e6c`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e10ba5def77eae105b1dfab52bd41d16cba2895929673658ec8fedc7d8408e`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.3 MB (2274765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef565721758b7adafc1e282adeddbe68df6d6631699124a860c60f5c507840b4`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3c670c6f24cc3e29abf3af268073c6ce8dbbf9f684d40af076e3549e763252`  
		Last Modified: Fri, 01 Oct 2021 05:25:52 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7d08c7f33a237d041cc7644173cf3c895b5fdcfa2e1e2c1f8e1ed4a57c724f`  
		Last Modified: Fri, 01 Oct 2021 05:26:04 GMT  
		Size: 80.1 MB (80091210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc356da8c13b498fc481a453aaf0c3b3222c3993f398414949ec468bdb6f891`  
		Last Modified: Fri, 01 Oct 2021 05:25:52 GMT  
		Size: 5.6 KB (5611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37cb59f9aa1ae9c3f71acc88d526794713ad3d5f93f37e61280241369278c1ae`  
		Last Modified: Fri, 01 Oct 2021 05:25:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.31-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:bbd3a3cf613358fbb05108dd7dc9ac6e902e1ef8617e7ec5928ec759f6dc4d17
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117623997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77c013d6bf7007d3d94c458ab3918e9c68ead56a2fdc71efb870a3d229ef5f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:38:47 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 03:38:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:38:56 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 03:39:11 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 03:39:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 03:39:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:39:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 03:39:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 03:41:07 GMT
ARG MARIADB_MAJOR=10.3
# Fri, 01 Oct 2021 03:41:08 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 01 Oct 2021 03:41:08 GMT
ARG MARIADB_VERSION=1:10.3.31+maria~focal
# Fri, 01 Oct 2021 03:41:08 GMT
ENV MARIADB_VERSION=1:10.3.31+maria~focal
# Fri, 01 Oct 2021 03:41:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 03:41:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 03:41:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 03:41:36 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 03:41:37 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 03:41:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Oct 2021 03:41:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 03:41:38 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 03:41:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d5ae241c1f10925c65b1658513761cd873e86632ea54cd491a17314c717db9`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1337b7de0aecaa84469be03f6aca5f4716813a7f70d6df52ada4f37e67dce98`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 5.5 MB (5455225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720ecfb64bf9977e96130e89f4d49759a1b9577aabaa5c864b0f7a3c0473f778`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 3.4 MB (3368539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba0c987cf142da7e613c8eb5506412f33e85d62e8b737d82ae8a86dad1a3dd1`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1cd2ca1d8beab7fe86d456206b59ee252c55fd199373f2caae49c71ec65a2a`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.2 MB (2203545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9328b4fc02fb1261cd4016d0e4d31dd6528b268e170d8278afbd062e3a96fa1`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c4a4c53fccbe5fcacb1204de248af27df80039edf6f327fb2a1c3bbe4f3e55`  
		Last Modified: Fri, 01 Oct 2021 03:45:52 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003e43ca6fa30ba8ffed812ee011dfa91fd4dc750ba1be39c62d8f55de817c18`  
		Last Modified: Fri, 01 Oct 2021 03:46:06 GMT  
		Size: 79.4 MB (79413829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0aaf0a90cfbb05c1065e5881d45812b427c0561302274e66bc5bf5170a44ece`  
		Last Modified: Fri, 01 Oct 2021 03:45:52 GMT  
		Size: 5.6 KB (5611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da02843ac443d5f1f0505e68cef6d9cfcd7107a9fbb28d065d4efa119a25c9b`  
		Last Modified: Fri, 01 Oct 2021 03:45:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.31-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:eabb2e81a20381ca05c1eef2015ba97f7ad63de9a30d74add3c07174ceb70ab7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130878512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b14c8cd50591ce95eaff04590dcce413136bcdf53a1d7e29f4664791de54dfd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:34:53 GMT
ENV GOSU_VERSION=1.13
# Sat, 16 Oct 2021 01:35:28 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 01:35:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 01:36:02 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:36:03 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 16 Oct 2021 01:36:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 01:45:24 GMT
ARG MARIADB_MAJOR=10.3
# Sat, 16 Oct 2021 01:45:26 GMT
ENV MARIADB_MAJOR=10.3
# Sat, 16 Oct 2021 01:45:30 GMT
ARG MARIADB_VERSION=1:10.3.31+maria~focal
# Sat, 16 Oct 2021 01:45:31 GMT
ENV MARIADB_VERSION=1:10.3.31+maria~focal
# Sat, 16 Oct 2021 01:45:34 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
# Sat, 16 Oct 2021 01:45:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 16 Oct 2021 01:47:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 16 Oct 2021 01:48:00 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Oct 2021 01:48:01 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:48:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 16 Oct 2021 01:48:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Oct 2021 01:48:17 GMT
EXPOSE 3306
# Sat, 16 Oct 2021 01:48:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bdbddf0ed762c90ab4fcfe1f42007a96e4f90ca4f0765dfcec52213a3f5c12`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 3.7 MB (3670760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cc95e86fb5ab1bda9839a1ecbd3c2d607bc6cfc5155f33bf32c9d7827ec98b`  
		Last Modified: Sat, 16 Oct 2021 01:49:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe2cefdba07cb9fc803227a545d4fcc196038c1020de7698bf4e333d9056cbd`  
		Last Modified: Sat, 16 Oct 2021 01:49:28 GMT  
		Size: 2.6 MB (2573066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab77c7b0e7b171541e9f7f813ef81190ef39151aea54bfe2b64f8c191ce672c`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94aeb2fd007f06d10435736a0bd9fae69670ff9c01bc11e62f75e5fea4653129`  
		Last Modified: Sat, 16 Oct 2021 01:51:28 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e393cff902c3ca290ce3dbad73eceaf35a4548496b5944e1fcd51253e5fcf022`  
		Last Modified: Sat, 16 Oct 2021 01:51:45 GMT  
		Size: 84.7 MB (84669015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9afc7f203a71d7290d7ab97ce69fc1691c8ef75f8582f449060a77a9ca89d1`  
		Last Modified: Sat, 16 Oct 2021 01:51:29 GMT  
		Size: 5.6 KB (5610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc4f496ad3cc84a892fb9157e7341f3c85c2fd8d8a0251e3578987bc804d6a9`  
		Last Modified: Sat, 16 Oct 2021 01:51:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4`

```console
$ docker pull mariadb@sha256:47afeb1fb58eef19fa48e363aa47d038601b96e8ddebc8b4f2083a01ea835c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4` - linux; amd64

```console
$ docker pull mariadb@sha256:f020b9478d19d646a2ccca8fea5926fb72e4b4004a92d1fec7f704775b95a52f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124740237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1282b9953779374fdfca748be97f06e8c04906130cb43c183e4975dcf6505ffe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:19:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 05:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:18 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 05:19:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 05:19:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 05:19:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:39 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 05:19:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 05:21:02 GMT
ARG MARIADB_MAJOR=10.4
# Fri, 01 Oct 2021 05:21:02 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 01 Oct 2021 05:21:02 GMT
ARG MARIADB_VERSION=1:10.4.21+maria~focal
# Fri, 01 Oct 2021 05:21:02 GMT
ENV MARIADB_VERSION=1:10.4.21+maria~focal
# Fri, 01 Oct 2021 05:21:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 05:21:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 05:21:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 05:21:28 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 05:21:28 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 05:21:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Oct 2021 05:21:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 05:21:29 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 05:21:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6f45e0fb03b087254fb0750ec2bbfbc7ea10f3eaaa2c3381f2ef6b3cf2c32b`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a10760fd6ecff1db568c4df08e4add59ea3424ae8b2ed2ac557f5239fa74d`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 5.5 MB (5489340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0645d99211dd422dc4b2c52d1005a518b5d9c76409584ee75faf26c78de36b`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 3.6 MB (3582638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff899ddf1cc12eb3161fb924245c2cdb096fe9cadd0b73128f7d3e45e4a0e6c`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e10ba5def77eae105b1dfab52bd41d16cba2895929673658ec8fedc7d8408e`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.3 MB (2274765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef565721758b7adafc1e282adeddbe68df6d6631699124a860c60f5c507840b4`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fc84e43c4b5ddfa68c6ff7d94b15bfd0c1a2c2a3086a538bd4cc1af33b7c43`  
		Last Modified: Fri, 01 Oct 2021 05:25:23 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78df6670f106bd0e5909e2021f673fbac2ae0bb77eb73c04d9fa263f0696411c`  
		Last Modified: Fri, 01 Oct 2021 05:25:35 GMT  
		Size: 84.8 MB (84814133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c50c795ffaab7dde36197d25796eca44f80020657b0f3220a59d7eb8c9ea3b`  
		Last Modified: Fri, 01 Oct 2021 05:25:23 GMT  
		Size: 5.6 KB (5608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf5ef64431a25f537dc908fc9564255a8eb16f68c071f45078d7a72809ac55e`  
		Last Modified: Fri, 01 Oct 2021 05:25:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:fd42b3a79249b06ac5ffaf8d6154b4468e66149e9b0012d6793b98c8f66e3a2b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122257682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07640aa9a427948f5fb3725fd8807a5547f1956e4b94370998f664540327d913`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:38:47 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 03:38:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:38:56 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 03:39:11 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 03:39:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 03:39:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:39:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 03:39:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 03:40:35 GMT
ARG MARIADB_MAJOR=10.4
# Fri, 01 Oct 2021 03:40:35 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 01 Oct 2021 03:40:36 GMT
ARG MARIADB_VERSION=1:10.4.21+maria~focal
# Fri, 01 Oct 2021 03:40:36 GMT
ENV MARIADB_VERSION=1:10.4.21+maria~focal
# Fri, 01 Oct 2021 03:40:36 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 03:40:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 03:40:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 03:41:00 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 03:41:00 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 03:41:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Oct 2021 03:41:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 03:41:01 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 03:41:01 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d5ae241c1f10925c65b1658513761cd873e86632ea54cd491a17314c717db9`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1337b7de0aecaa84469be03f6aca5f4716813a7f70d6df52ada4f37e67dce98`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 5.5 MB (5455225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720ecfb64bf9977e96130e89f4d49759a1b9577aabaa5c864b0f7a3c0473f778`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 3.4 MB (3368539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba0c987cf142da7e613c8eb5506412f33e85d62e8b737d82ae8a86dad1a3dd1`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1cd2ca1d8beab7fe86d456206b59ee252c55fd199373f2caae49c71ec65a2a`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.2 MB (2203545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9328b4fc02fb1261cd4016d0e4d31dd6528b268e170d8278afbd062e3a96fa1`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57c614f2f695b34d80b99cab9b355f51a9195d57275f0c6c68ec8a39d3b27dd`  
		Last Modified: Fri, 01 Oct 2021 03:45:19 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8c19e76c9e478242d95b697af4081371e9158a01037cb61c72c74dfcc6ab0e`  
		Last Modified: Fri, 01 Oct 2021 03:45:34 GMT  
		Size: 84.0 MB (84047515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb818408546e9d89412235e284f3be786f01a59a79128a41ed866c7993fbbd1e`  
		Last Modified: Fri, 01 Oct 2021 03:45:19 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6dd39f8c938029c683d1fedbc6d0cd2f4c24f306a7a19188a66b8496b8a3744`  
		Last Modified: Fri, 01 Oct 2021 03:45:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; ppc64le

```console
$ docker pull mariadb@sha256:db23ae4a8dc88c4e06fcd477bd8ec87388a4acd0562e8f1baeb9c16cd2e3d3a2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135463544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3acf37940c7d117f6000c53a107c6013f52d57d70afb7a47a667ea880124344b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:34:53 GMT
ENV GOSU_VERSION=1.13
# Sat, 16 Oct 2021 01:35:28 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 01:35:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 01:36:02 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:36:03 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 16 Oct 2021 01:36:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 01:42:17 GMT
ARG MARIADB_MAJOR=10.4
# Sat, 16 Oct 2021 01:42:19 GMT
ENV MARIADB_MAJOR=10.4
# Sat, 16 Oct 2021 01:42:22 GMT
ARG MARIADB_VERSION=1:10.4.21+maria~focal
# Sat, 16 Oct 2021 01:42:25 GMT
ENV MARIADB_VERSION=1:10.4.21+maria~focal
# Sat, 16 Oct 2021 01:42:27 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
# Sat, 16 Oct 2021 01:42:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 16 Oct 2021 01:44:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 16 Oct 2021 01:44:36 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Oct 2021 01:44:42 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:44:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 16 Oct 2021 01:44:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Oct 2021 01:45:02 GMT
EXPOSE 3306
# Sat, 16 Oct 2021 01:45:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bdbddf0ed762c90ab4fcfe1f42007a96e4f90ca4f0765dfcec52213a3f5c12`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 3.7 MB (3670760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cc95e86fb5ab1bda9839a1ecbd3c2d607bc6cfc5155f33bf32c9d7827ec98b`  
		Last Modified: Sat, 16 Oct 2021 01:49:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe2cefdba07cb9fc803227a545d4fcc196038c1020de7698bf4e333d9056cbd`  
		Last Modified: Sat, 16 Oct 2021 01:49:28 GMT  
		Size: 2.6 MB (2573066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab77c7b0e7b171541e9f7f813ef81190ef39151aea54bfe2b64f8c191ce672c`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e32cfb63425b3d801b33babc5bccf0ef736e4a9c7dd5e04fe577798daedc1634`  
		Last Modified: Sat, 16 Oct 2021 01:50:51 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5c5072f86749780a8a81ebfe4aa7ca737f4f74bb3f6a69febc5eb2924e89cf`  
		Last Modified: Sat, 16 Oct 2021 01:51:09 GMT  
		Size: 89.3 MB (89254045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45b7223486b0ec48518eefd709259162497aa7fa00c4ffd87b23d69b694143e`  
		Last Modified: Sat, 16 Oct 2021 01:50:51 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d460edc3fbc58f5e1daccef6ff69244bbed3674513cc88cc95a9b7ea0e4421`  
		Last Modified: Sat, 16 Oct 2021 01:50:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4-focal`

```console
$ docker pull mariadb@sha256:47afeb1fb58eef19fa48e363aa47d038601b96e8ddebc8b4f2083a01ea835c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:f020b9478d19d646a2ccca8fea5926fb72e4b4004a92d1fec7f704775b95a52f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124740237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1282b9953779374fdfca748be97f06e8c04906130cb43c183e4975dcf6505ffe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:19:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 05:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:18 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 05:19:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 05:19:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 05:19:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:39 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 05:19:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 05:21:02 GMT
ARG MARIADB_MAJOR=10.4
# Fri, 01 Oct 2021 05:21:02 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 01 Oct 2021 05:21:02 GMT
ARG MARIADB_VERSION=1:10.4.21+maria~focal
# Fri, 01 Oct 2021 05:21:02 GMT
ENV MARIADB_VERSION=1:10.4.21+maria~focal
# Fri, 01 Oct 2021 05:21:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 05:21:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 05:21:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 05:21:28 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 05:21:28 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 05:21:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Oct 2021 05:21:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 05:21:29 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 05:21:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6f45e0fb03b087254fb0750ec2bbfbc7ea10f3eaaa2c3381f2ef6b3cf2c32b`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a10760fd6ecff1db568c4df08e4add59ea3424ae8b2ed2ac557f5239fa74d`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 5.5 MB (5489340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0645d99211dd422dc4b2c52d1005a518b5d9c76409584ee75faf26c78de36b`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 3.6 MB (3582638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff899ddf1cc12eb3161fb924245c2cdb096fe9cadd0b73128f7d3e45e4a0e6c`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e10ba5def77eae105b1dfab52bd41d16cba2895929673658ec8fedc7d8408e`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.3 MB (2274765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef565721758b7adafc1e282adeddbe68df6d6631699124a860c60f5c507840b4`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fc84e43c4b5ddfa68c6ff7d94b15bfd0c1a2c2a3086a538bd4cc1af33b7c43`  
		Last Modified: Fri, 01 Oct 2021 05:25:23 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78df6670f106bd0e5909e2021f673fbac2ae0bb77eb73c04d9fa263f0696411c`  
		Last Modified: Fri, 01 Oct 2021 05:25:35 GMT  
		Size: 84.8 MB (84814133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c50c795ffaab7dde36197d25796eca44f80020657b0f3220a59d7eb8c9ea3b`  
		Last Modified: Fri, 01 Oct 2021 05:25:23 GMT  
		Size: 5.6 KB (5608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf5ef64431a25f537dc908fc9564255a8eb16f68c071f45078d7a72809ac55e`  
		Last Modified: Fri, 01 Oct 2021 05:25:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:fd42b3a79249b06ac5ffaf8d6154b4468e66149e9b0012d6793b98c8f66e3a2b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122257682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07640aa9a427948f5fb3725fd8807a5547f1956e4b94370998f664540327d913`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:38:47 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 03:38:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:38:56 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 03:39:11 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 03:39:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 03:39:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:39:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 03:39:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 03:40:35 GMT
ARG MARIADB_MAJOR=10.4
# Fri, 01 Oct 2021 03:40:35 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 01 Oct 2021 03:40:36 GMT
ARG MARIADB_VERSION=1:10.4.21+maria~focal
# Fri, 01 Oct 2021 03:40:36 GMT
ENV MARIADB_VERSION=1:10.4.21+maria~focal
# Fri, 01 Oct 2021 03:40:36 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 03:40:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 03:40:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 03:41:00 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 03:41:00 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 03:41:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Oct 2021 03:41:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 03:41:01 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 03:41:01 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d5ae241c1f10925c65b1658513761cd873e86632ea54cd491a17314c717db9`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1337b7de0aecaa84469be03f6aca5f4716813a7f70d6df52ada4f37e67dce98`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 5.5 MB (5455225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720ecfb64bf9977e96130e89f4d49759a1b9577aabaa5c864b0f7a3c0473f778`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 3.4 MB (3368539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba0c987cf142da7e613c8eb5506412f33e85d62e8b737d82ae8a86dad1a3dd1`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1cd2ca1d8beab7fe86d456206b59ee252c55fd199373f2caae49c71ec65a2a`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.2 MB (2203545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9328b4fc02fb1261cd4016d0e4d31dd6528b268e170d8278afbd062e3a96fa1`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57c614f2f695b34d80b99cab9b355f51a9195d57275f0c6c68ec8a39d3b27dd`  
		Last Modified: Fri, 01 Oct 2021 03:45:19 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8c19e76c9e478242d95b697af4081371e9158a01037cb61c72c74dfcc6ab0e`  
		Last Modified: Fri, 01 Oct 2021 03:45:34 GMT  
		Size: 84.0 MB (84047515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb818408546e9d89412235e284f3be786f01a59a79128a41ed866c7993fbbd1e`  
		Last Modified: Fri, 01 Oct 2021 03:45:19 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6dd39f8c938029c683d1fedbc6d0cd2f4c24f306a7a19188a66b8496b8a3744`  
		Last Modified: Fri, 01 Oct 2021 03:45:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:db23ae4a8dc88c4e06fcd477bd8ec87388a4acd0562e8f1baeb9c16cd2e3d3a2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135463544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3acf37940c7d117f6000c53a107c6013f52d57d70afb7a47a667ea880124344b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:34:53 GMT
ENV GOSU_VERSION=1.13
# Sat, 16 Oct 2021 01:35:28 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 01:35:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 01:36:02 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:36:03 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 16 Oct 2021 01:36:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 01:42:17 GMT
ARG MARIADB_MAJOR=10.4
# Sat, 16 Oct 2021 01:42:19 GMT
ENV MARIADB_MAJOR=10.4
# Sat, 16 Oct 2021 01:42:22 GMT
ARG MARIADB_VERSION=1:10.4.21+maria~focal
# Sat, 16 Oct 2021 01:42:25 GMT
ENV MARIADB_VERSION=1:10.4.21+maria~focal
# Sat, 16 Oct 2021 01:42:27 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
# Sat, 16 Oct 2021 01:42:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 16 Oct 2021 01:44:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 16 Oct 2021 01:44:36 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Oct 2021 01:44:42 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:44:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 16 Oct 2021 01:44:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Oct 2021 01:45:02 GMT
EXPOSE 3306
# Sat, 16 Oct 2021 01:45:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bdbddf0ed762c90ab4fcfe1f42007a96e4f90ca4f0765dfcec52213a3f5c12`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 3.7 MB (3670760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cc95e86fb5ab1bda9839a1ecbd3c2d607bc6cfc5155f33bf32c9d7827ec98b`  
		Last Modified: Sat, 16 Oct 2021 01:49:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe2cefdba07cb9fc803227a545d4fcc196038c1020de7698bf4e333d9056cbd`  
		Last Modified: Sat, 16 Oct 2021 01:49:28 GMT  
		Size: 2.6 MB (2573066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab77c7b0e7b171541e9f7f813ef81190ef39151aea54bfe2b64f8c191ce672c`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e32cfb63425b3d801b33babc5bccf0ef736e4a9c7dd5e04fe577798daedc1634`  
		Last Modified: Sat, 16 Oct 2021 01:50:51 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5c5072f86749780a8a81ebfe4aa7ca737f4f74bb3f6a69febc5eb2924e89cf`  
		Last Modified: Sat, 16 Oct 2021 01:51:09 GMT  
		Size: 89.3 MB (89254045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45b7223486b0ec48518eefd709259162497aa7fa00c4ffd87b23d69b694143e`  
		Last Modified: Sat, 16 Oct 2021 01:50:51 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d460edc3fbc58f5e1daccef6ff69244bbed3674513cc88cc95a9b7ea0e4421`  
		Last Modified: Sat, 16 Oct 2021 01:50:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.21`

```console
$ docker pull mariadb@sha256:47afeb1fb58eef19fa48e363aa47d038601b96e8ddebc8b4f2083a01ea835c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.21` - linux; amd64

```console
$ docker pull mariadb@sha256:f020b9478d19d646a2ccca8fea5926fb72e4b4004a92d1fec7f704775b95a52f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124740237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1282b9953779374fdfca748be97f06e8c04906130cb43c183e4975dcf6505ffe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:19:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 05:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:18 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 05:19:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 05:19:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 05:19:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:39 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 05:19:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 05:21:02 GMT
ARG MARIADB_MAJOR=10.4
# Fri, 01 Oct 2021 05:21:02 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 01 Oct 2021 05:21:02 GMT
ARG MARIADB_VERSION=1:10.4.21+maria~focal
# Fri, 01 Oct 2021 05:21:02 GMT
ENV MARIADB_VERSION=1:10.4.21+maria~focal
# Fri, 01 Oct 2021 05:21:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 05:21:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 05:21:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 05:21:28 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 05:21:28 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 05:21:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Oct 2021 05:21:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 05:21:29 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 05:21:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6f45e0fb03b087254fb0750ec2bbfbc7ea10f3eaaa2c3381f2ef6b3cf2c32b`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a10760fd6ecff1db568c4df08e4add59ea3424ae8b2ed2ac557f5239fa74d`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 5.5 MB (5489340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0645d99211dd422dc4b2c52d1005a518b5d9c76409584ee75faf26c78de36b`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 3.6 MB (3582638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff899ddf1cc12eb3161fb924245c2cdb096fe9cadd0b73128f7d3e45e4a0e6c`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e10ba5def77eae105b1dfab52bd41d16cba2895929673658ec8fedc7d8408e`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.3 MB (2274765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef565721758b7adafc1e282adeddbe68df6d6631699124a860c60f5c507840b4`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fc84e43c4b5ddfa68c6ff7d94b15bfd0c1a2c2a3086a538bd4cc1af33b7c43`  
		Last Modified: Fri, 01 Oct 2021 05:25:23 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78df6670f106bd0e5909e2021f673fbac2ae0bb77eb73c04d9fa263f0696411c`  
		Last Modified: Fri, 01 Oct 2021 05:25:35 GMT  
		Size: 84.8 MB (84814133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c50c795ffaab7dde36197d25796eca44f80020657b0f3220a59d7eb8c9ea3b`  
		Last Modified: Fri, 01 Oct 2021 05:25:23 GMT  
		Size: 5.6 KB (5608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf5ef64431a25f537dc908fc9564255a8eb16f68c071f45078d7a72809ac55e`  
		Last Modified: Fri, 01 Oct 2021 05:25:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.21` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:fd42b3a79249b06ac5ffaf8d6154b4468e66149e9b0012d6793b98c8f66e3a2b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122257682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07640aa9a427948f5fb3725fd8807a5547f1956e4b94370998f664540327d913`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:38:47 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 03:38:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:38:56 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 03:39:11 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 03:39:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 03:39:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:39:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 03:39:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 03:40:35 GMT
ARG MARIADB_MAJOR=10.4
# Fri, 01 Oct 2021 03:40:35 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 01 Oct 2021 03:40:36 GMT
ARG MARIADB_VERSION=1:10.4.21+maria~focal
# Fri, 01 Oct 2021 03:40:36 GMT
ENV MARIADB_VERSION=1:10.4.21+maria~focal
# Fri, 01 Oct 2021 03:40:36 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 03:40:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 03:40:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 03:41:00 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 03:41:00 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 03:41:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Oct 2021 03:41:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 03:41:01 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 03:41:01 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d5ae241c1f10925c65b1658513761cd873e86632ea54cd491a17314c717db9`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1337b7de0aecaa84469be03f6aca5f4716813a7f70d6df52ada4f37e67dce98`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 5.5 MB (5455225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720ecfb64bf9977e96130e89f4d49759a1b9577aabaa5c864b0f7a3c0473f778`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 3.4 MB (3368539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba0c987cf142da7e613c8eb5506412f33e85d62e8b737d82ae8a86dad1a3dd1`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1cd2ca1d8beab7fe86d456206b59ee252c55fd199373f2caae49c71ec65a2a`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.2 MB (2203545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9328b4fc02fb1261cd4016d0e4d31dd6528b268e170d8278afbd062e3a96fa1`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57c614f2f695b34d80b99cab9b355f51a9195d57275f0c6c68ec8a39d3b27dd`  
		Last Modified: Fri, 01 Oct 2021 03:45:19 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8c19e76c9e478242d95b697af4081371e9158a01037cb61c72c74dfcc6ab0e`  
		Last Modified: Fri, 01 Oct 2021 03:45:34 GMT  
		Size: 84.0 MB (84047515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb818408546e9d89412235e284f3be786f01a59a79128a41ed866c7993fbbd1e`  
		Last Modified: Fri, 01 Oct 2021 03:45:19 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6dd39f8c938029c683d1fedbc6d0cd2f4c24f306a7a19188a66b8496b8a3744`  
		Last Modified: Fri, 01 Oct 2021 03:45:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.21` - linux; ppc64le

```console
$ docker pull mariadb@sha256:db23ae4a8dc88c4e06fcd477bd8ec87388a4acd0562e8f1baeb9c16cd2e3d3a2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135463544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3acf37940c7d117f6000c53a107c6013f52d57d70afb7a47a667ea880124344b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:34:53 GMT
ENV GOSU_VERSION=1.13
# Sat, 16 Oct 2021 01:35:28 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 01:35:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 01:36:02 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:36:03 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 16 Oct 2021 01:36:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 01:42:17 GMT
ARG MARIADB_MAJOR=10.4
# Sat, 16 Oct 2021 01:42:19 GMT
ENV MARIADB_MAJOR=10.4
# Sat, 16 Oct 2021 01:42:22 GMT
ARG MARIADB_VERSION=1:10.4.21+maria~focal
# Sat, 16 Oct 2021 01:42:25 GMT
ENV MARIADB_VERSION=1:10.4.21+maria~focal
# Sat, 16 Oct 2021 01:42:27 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
# Sat, 16 Oct 2021 01:42:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 16 Oct 2021 01:44:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 16 Oct 2021 01:44:36 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Oct 2021 01:44:42 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:44:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 16 Oct 2021 01:44:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Oct 2021 01:45:02 GMT
EXPOSE 3306
# Sat, 16 Oct 2021 01:45:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bdbddf0ed762c90ab4fcfe1f42007a96e4f90ca4f0765dfcec52213a3f5c12`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 3.7 MB (3670760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cc95e86fb5ab1bda9839a1ecbd3c2d607bc6cfc5155f33bf32c9d7827ec98b`  
		Last Modified: Sat, 16 Oct 2021 01:49:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe2cefdba07cb9fc803227a545d4fcc196038c1020de7698bf4e333d9056cbd`  
		Last Modified: Sat, 16 Oct 2021 01:49:28 GMT  
		Size: 2.6 MB (2573066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab77c7b0e7b171541e9f7f813ef81190ef39151aea54bfe2b64f8c191ce672c`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e32cfb63425b3d801b33babc5bccf0ef736e4a9c7dd5e04fe577798daedc1634`  
		Last Modified: Sat, 16 Oct 2021 01:50:51 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5c5072f86749780a8a81ebfe4aa7ca737f4f74bb3f6a69febc5eb2924e89cf`  
		Last Modified: Sat, 16 Oct 2021 01:51:09 GMT  
		Size: 89.3 MB (89254045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45b7223486b0ec48518eefd709259162497aa7fa00c4ffd87b23d69b694143e`  
		Last Modified: Sat, 16 Oct 2021 01:50:51 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d460edc3fbc58f5e1daccef6ff69244bbed3674513cc88cc95a9b7ea0e4421`  
		Last Modified: Sat, 16 Oct 2021 01:50:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.21-focal`

```console
$ docker pull mariadb@sha256:47afeb1fb58eef19fa48e363aa47d038601b96e8ddebc8b4f2083a01ea835c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.21-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:f020b9478d19d646a2ccca8fea5926fb72e4b4004a92d1fec7f704775b95a52f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124740237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1282b9953779374fdfca748be97f06e8c04906130cb43c183e4975dcf6505ffe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:19:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 05:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:18 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 05:19:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 05:19:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 05:19:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:39 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 05:19:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 05:21:02 GMT
ARG MARIADB_MAJOR=10.4
# Fri, 01 Oct 2021 05:21:02 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 01 Oct 2021 05:21:02 GMT
ARG MARIADB_VERSION=1:10.4.21+maria~focal
# Fri, 01 Oct 2021 05:21:02 GMT
ENV MARIADB_VERSION=1:10.4.21+maria~focal
# Fri, 01 Oct 2021 05:21:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 05:21:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 05:21:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 05:21:28 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 05:21:28 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 05:21:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Oct 2021 05:21:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 05:21:29 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 05:21:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6f45e0fb03b087254fb0750ec2bbfbc7ea10f3eaaa2c3381f2ef6b3cf2c32b`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a10760fd6ecff1db568c4df08e4add59ea3424ae8b2ed2ac557f5239fa74d`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 5.5 MB (5489340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0645d99211dd422dc4b2c52d1005a518b5d9c76409584ee75faf26c78de36b`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 3.6 MB (3582638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff899ddf1cc12eb3161fb924245c2cdb096fe9cadd0b73128f7d3e45e4a0e6c`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e10ba5def77eae105b1dfab52bd41d16cba2895929673658ec8fedc7d8408e`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.3 MB (2274765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef565721758b7adafc1e282adeddbe68df6d6631699124a860c60f5c507840b4`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fc84e43c4b5ddfa68c6ff7d94b15bfd0c1a2c2a3086a538bd4cc1af33b7c43`  
		Last Modified: Fri, 01 Oct 2021 05:25:23 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78df6670f106bd0e5909e2021f673fbac2ae0bb77eb73c04d9fa263f0696411c`  
		Last Modified: Fri, 01 Oct 2021 05:25:35 GMT  
		Size: 84.8 MB (84814133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c50c795ffaab7dde36197d25796eca44f80020657b0f3220a59d7eb8c9ea3b`  
		Last Modified: Fri, 01 Oct 2021 05:25:23 GMT  
		Size: 5.6 KB (5608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf5ef64431a25f537dc908fc9564255a8eb16f68c071f45078d7a72809ac55e`  
		Last Modified: Fri, 01 Oct 2021 05:25:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.21-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:fd42b3a79249b06ac5ffaf8d6154b4468e66149e9b0012d6793b98c8f66e3a2b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122257682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07640aa9a427948f5fb3725fd8807a5547f1956e4b94370998f664540327d913`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:38:47 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 03:38:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:38:56 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 03:39:11 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 03:39:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 03:39:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:39:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 03:39:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 03:40:35 GMT
ARG MARIADB_MAJOR=10.4
# Fri, 01 Oct 2021 03:40:35 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 01 Oct 2021 03:40:36 GMT
ARG MARIADB_VERSION=1:10.4.21+maria~focal
# Fri, 01 Oct 2021 03:40:36 GMT
ENV MARIADB_VERSION=1:10.4.21+maria~focal
# Fri, 01 Oct 2021 03:40:36 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 03:40:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 03:40:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 03:41:00 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 03:41:00 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 03:41:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Oct 2021 03:41:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 03:41:01 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 03:41:01 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d5ae241c1f10925c65b1658513761cd873e86632ea54cd491a17314c717db9`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1337b7de0aecaa84469be03f6aca5f4716813a7f70d6df52ada4f37e67dce98`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 5.5 MB (5455225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720ecfb64bf9977e96130e89f4d49759a1b9577aabaa5c864b0f7a3c0473f778`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 3.4 MB (3368539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba0c987cf142da7e613c8eb5506412f33e85d62e8b737d82ae8a86dad1a3dd1`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1cd2ca1d8beab7fe86d456206b59ee252c55fd199373f2caae49c71ec65a2a`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.2 MB (2203545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9328b4fc02fb1261cd4016d0e4d31dd6528b268e170d8278afbd062e3a96fa1`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57c614f2f695b34d80b99cab9b355f51a9195d57275f0c6c68ec8a39d3b27dd`  
		Last Modified: Fri, 01 Oct 2021 03:45:19 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8c19e76c9e478242d95b697af4081371e9158a01037cb61c72c74dfcc6ab0e`  
		Last Modified: Fri, 01 Oct 2021 03:45:34 GMT  
		Size: 84.0 MB (84047515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb818408546e9d89412235e284f3be786f01a59a79128a41ed866c7993fbbd1e`  
		Last Modified: Fri, 01 Oct 2021 03:45:19 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6dd39f8c938029c683d1fedbc6d0cd2f4c24f306a7a19188a66b8496b8a3744`  
		Last Modified: Fri, 01 Oct 2021 03:45:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.21-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:db23ae4a8dc88c4e06fcd477bd8ec87388a4acd0562e8f1baeb9c16cd2e3d3a2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135463544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3acf37940c7d117f6000c53a107c6013f52d57d70afb7a47a667ea880124344b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:34:53 GMT
ENV GOSU_VERSION=1.13
# Sat, 16 Oct 2021 01:35:28 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 01:35:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 01:36:02 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:36:03 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 16 Oct 2021 01:36:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 01:42:17 GMT
ARG MARIADB_MAJOR=10.4
# Sat, 16 Oct 2021 01:42:19 GMT
ENV MARIADB_MAJOR=10.4
# Sat, 16 Oct 2021 01:42:22 GMT
ARG MARIADB_VERSION=1:10.4.21+maria~focal
# Sat, 16 Oct 2021 01:42:25 GMT
ENV MARIADB_VERSION=1:10.4.21+maria~focal
# Sat, 16 Oct 2021 01:42:27 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
# Sat, 16 Oct 2021 01:42:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 16 Oct 2021 01:44:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 16 Oct 2021 01:44:36 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Oct 2021 01:44:42 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:44:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 16 Oct 2021 01:44:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Oct 2021 01:45:02 GMT
EXPOSE 3306
# Sat, 16 Oct 2021 01:45:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bdbddf0ed762c90ab4fcfe1f42007a96e4f90ca4f0765dfcec52213a3f5c12`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 3.7 MB (3670760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cc95e86fb5ab1bda9839a1ecbd3c2d607bc6cfc5155f33bf32c9d7827ec98b`  
		Last Modified: Sat, 16 Oct 2021 01:49:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe2cefdba07cb9fc803227a545d4fcc196038c1020de7698bf4e333d9056cbd`  
		Last Modified: Sat, 16 Oct 2021 01:49:28 GMT  
		Size: 2.6 MB (2573066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab77c7b0e7b171541e9f7f813ef81190ef39151aea54bfe2b64f8c191ce672c`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e32cfb63425b3d801b33babc5bccf0ef736e4a9c7dd5e04fe577798daedc1634`  
		Last Modified: Sat, 16 Oct 2021 01:50:51 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5c5072f86749780a8a81ebfe4aa7ca737f4f74bb3f6a69febc5eb2924e89cf`  
		Last Modified: Sat, 16 Oct 2021 01:51:09 GMT  
		Size: 89.3 MB (89254045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45b7223486b0ec48518eefd709259162497aa7fa00c4ffd87b23d69b694143e`  
		Last Modified: Sat, 16 Oct 2021 01:50:51 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d460edc3fbc58f5e1daccef6ff69244bbed3674513cc88cc95a9b7ea0e4421`  
		Last Modified: Sat, 16 Oct 2021 01:50:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5`

```console
$ docker pull mariadb@sha256:b125a538789176c1a428f89f3ce7bf3018821c10d6cf2719a6ff055f13810708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5` - linux; amd64

```console
$ docker pull mariadb@sha256:15994bfb5fd4700cc6180c92752550488d2cfcaeca45a921fe28657b67da5df4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126863664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02241ea3e9b943595157787d6ad7737572ff7670070d6abf32e2bc446f3a235c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:19:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 05:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:18 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 05:19:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 05:19:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 05:19:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:39 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 05:19:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 05:20:32 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 01 Oct 2021 05:20:32 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 01 Oct 2021 05:20:32 GMT
ARG MARIADB_VERSION=1:10.5.12+maria~focal
# Fri, 01 Oct 2021 05:20:32 GMT
ENV MARIADB_VERSION=1:10.5.12+maria~focal
# Fri, 01 Oct 2021 05:20:32 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 05:20:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 05:20:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 05:20:57 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 05:20:57 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 05:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 05:20:57 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 05:20:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6f45e0fb03b087254fb0750ec2bbfbc7ea10f3eaaa2c3381f2ef6b3cf2c32b`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a10760fd6ecff1db568c4df08e4add59ea3424ae8b2ed2ac557f5239fa74d`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 5.5 MB (5489340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0645d99211dd422dc4b2c52d1005a518b5d9c76409584ee75faf26c78de36b`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 3.6 MB (3582638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff899ddf1cc12eb3161fb924245c2cdb096fe9cadd0b73128f7d3e45e4a0e6c`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e10ba5def77eae105b1dfab52bd41d16cba2895929673658ec8fedc7d8408e`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.3 MB (2274765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef565721758b7adafc1e282adeddbe68df6d6631699124a860c60f5c507840b4`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827d88322c0fbf9af8d3af5b2a11e87dac976d5cdcd466a49564fedcc0d979f8`  
		Last Modified: Fri, 01 Oct 2021 05:24:55 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73de2e05944a2f6723efe83f89f004960c463f7754ed1a0045ad484845f8545`  
		Last Modified: Fri, 01 Oct 2021 05:25:08 GMT  
		Size: 86.9 MB (86937676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb6b36ede734262ad3b61f725fb5918b4b90621d55ef9608ec95d6b9ceaca4c`  
		Last Modified: Fri, 01 Oct 2021 05:24:55 GMT  
		Size: 5.6 KB (5610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:693dc7438e76753b2268f6c4493ef6844e31e3c71f504e9c0f52e3428dad6cb9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124311951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4569802db431aa0e364a1dc990bbc1bd13a9e689a30b1b8930a6f872bea628`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:38:47 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 03:38:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:38:56 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 03:39:11 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 03:39:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 03:39:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:39:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 03:39:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 03:40:04 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 01 Oct 2021 03:40:04 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 01 Oct 2021 03:40:04 GMT
ARG MARIADB_VERSION=1:10.5.12+maria~focal
# Fri, 01 Oct 2021 03:40:04 GMT
ENV MARIADB_VERSION=1:10.5.12+maria~focal
# Fri, 01 Oct 2021 03:40:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 03:40:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 03:40:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 03:40:26 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 03:40:27 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 03:40:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 03:40:27 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 03:40:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d5ae241c1f10925c65b1658513761cd873e86632ea54cd491a17314c717db9`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1337b7de0aecaa84469be03f6aca5f4716813a7f70d6df52ada4f37e67dce98`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 5.5 MB (5455225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720ecfb64bf9977e96130e89f4d49759a1b9577aabaa5c864b0f7a3c0473f778`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 3.4 MB (3368539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba0c987cf142da7e613c8eb5506412f33e85d62e8b737d82ae8a86dad1a3dd1`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1cd2ca1d8beab7fe86d456206b59ee252c55fd199373f2caae49c71ec65a2a`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.2 MB (2203545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9328b4fc02fb1261cd4016d0e4d31dd6528b268e170d8278afbd062e3a96fa1`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e83551fceb22ef951d01f5c7b3c731ef65a3ce5134cff79beaf9a7ddab84d0`  
		Last Modified: Fri, 01 Oct 2021 03:44:46 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c055bdbde0df919694eedcd426329a549f55f8f44af11815a2681df052cbb7a9`  
		Last Modified: Fri, 01 Oct 2021 03:45:01 GMT  
		Size: 86.1 MB (86101907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d24b32215f5f5d263e7c68bbfdfe19229efa899099bac6d5eebfb02057f009dc`  
		Last Modified: Fri, 01 Oct 2021 03:44:47 GMT  
		Size: 5.6 KB (5611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; ppc64le

```console
$ docker pull mariadb@sha256:4f8d9dd96a6dbef3deb6138d39cfc38f8d0277a783db2e39a34d7a054b674684
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137580279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea3573cf742f38dedaa04d69169803bfa123f2c4d59e9b3c0c592ab22381be5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:34:53 GMT
ENV GOSU_VERSION=1.13
# Sat, 16 Oct 2021 01:35:28 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 01:35:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 01:36:02 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:36:03 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 16 Oct 2021 01:36:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 01:39:39 GMT
ARG MARIADB_MAJOR=10.5
# Sat, 16 Oct 2021 01:39:42 GMT
ENV MARIADB_MAJOR=10.5
# Sat, 16 Oct 2021 01:39:45 GMT
ARG MARIADB_VERSION=1:10.5.12+maria~focal
# Sat, 16 Oct 2021 01:39:47 GMT
ENV MARIADB_VERSION=1:10.5.12+maria~focal
# Sat, 16 Oct 2021 01:39:49 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
# Sat, 16 Oct 2021 01:39:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 16 Oct 2021 01:41:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 16 Oct 2021 01:41:52 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Oct 2021 01:41:54 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:41:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Oct 2021 01:42:00 GMT
EXPOSE 3306
# Sat, 16 Oct 2021 01:42:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bdbddf0ed762c90ab4fcfe1f42007a96e4f90ca4f0765dfcec52213a3f5c12`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 3.7 MB (3670760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cc95e86fb5ab1bda9839a1ecbd3c2d607bc6cfc5155f33bf32c9d7827ec98b`  
		Last Modified: Sat, 16 Oct 2021 01:49:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe2cefdba07cb9fc803227a545d4fcc196038c1020de7698bf4e333d9056cbd`  
		Last Modified: Sat, 16 Oct 2021 01:49:28 GMT  
		Size: 2.6 MB (2573066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab77c7b0e7b171541e9f7f813ef81190ef39151aea54bfe2b64f8c191ce672c`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec67cba87144a745f61e6d90badf06dd6518c512a3b7a067623cdeb4b9cec79`  
		Last Modified: Sat, 16 Oct 2021 01:50:16 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def963c9f47e8420d77e6cd15e6dc91a13dd6a6505af461e51c341d383391007`  
		Last Modified: Sat, 16 Oct 2021 01:50:34 GMT  
		Size: 91.4 MB (91370902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec1682d32f1d61eec73e062f876c8ea7b60b2bbd1ca6c8517026f735a72bf88`  
		Last Modified: Sat, 16 Oct 2021 01:50:16 GMT  
		Size: 5.6 KB (5611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; s390x

```console
$ docker pull mariadb@sha256:7f7a7b0832e1b134a141c55274c96532dd995cc1ae0e963b6a928dc890847d2b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (126048014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f672fd796e85e5a330f1f56ebd53ff3b67f962c269decf39128ae22f9ab408f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:02:36 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:02:41 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:02:42 GMT
ENV GOSU_VERSION=1.13
# Sat, 16 Oct 2021 01:02:50 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 01:02:51 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 01:02:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:02:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 16 Oct 2021 01:03:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 01:03:35 GMT
ARG MARIADB_MAJOR=10.5
# Sat, 16 Oct 2021 01:03:35 GMT
ENV MARIADB_MAJOR=10.5
# Sat, 16 Oct 2021 01:03:35 GMT
ARG MARIADB_VERSION=1:10.5.12+maria~focal
# Sat, 16 Oct 2021 01:03:35 GMT
ENV MARIADB_VERSION=1:10.5.12+maria~focal
# Sat, 16 Oct 2021 01:03:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
# Sat, 16 Oct 2021 01:03:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 16 Oct 2021 01:03:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 16 Oct 2021 01:03:58 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Oct 2021 01:03:58 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:03:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Oct 2021 01:03:58 GMT
EXPOSE 3306
# Sat, 16 Oct 2021 01:03:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc30a1fd200d10ce23e934b30e72d36ea131fb670d30afe697304591986fe1`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228a3fc0a9531bf3e9e08d9800daffbe33729ba8a16fb427b07a1a36fb047e02`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 5.4 MB (5380980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e511a129710d7aa78451eebec778e60a256b2a9e60db59a9f6d09641bd4f96`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 3.2 MB (3239822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a9cf411b6c206dca4cd2f493440c36781e332782682bb40969b6640e8e98e9`  
		Last Modified: Sat, 16 Oct 2021 01:04:31 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cac3f3cdb186c64fce6e0a7efc39abe96d0e6ab755d9193c981cc44c801cc51`  
		Last Modified: Sat, 16 Oct 2021 01:04:31 GMT  
		Size: 2.2 MB (2188905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd5f55dd4f1666fe90f4ca1b3b0cc36a9092c44ae19033a4d2b7b0e2ff3dddb`  
		Last Modified: Sat, 16 Oct 2021 01:04:30 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba27885bcb0e790f7990ad6b69669737ee44b5902deec85e48298b05b09835c`  
		Last Modified: Sat, 16 Oct 2021 01:05:06 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4814429007deb3858bf50326ba8c969e2a7b313c61ad7c5c387ed893d9d1f743`  
		Last Modified: Sat, 16 Oct 2021 01:05:18 GMT  
		Size: 88.1 MB (88107119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0aac5e8a79c251782a156851ac4e82652f50218e26b06c096f762d33782377c`  
		Last Modified: Sat, 16 Oct 2021 01:05:06 GMT  
		Size: 5.6 KB (5610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5-focal`

```console
$ docker pull mariadb@sha256:b125a538789176c1a428f89f3ce7bf3018821c10d6cf2719a6ff055f13810708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:15994bfb5fd4700cc6180c92752550488d2cfcaeca45a921fe28657b67da5df4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126863664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02241ea3e9b943595157787d6ad7737572ff7670070d6abf32e2bc446f3a235c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:19:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 05:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:18 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 05:19:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 05:19:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 05:19:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:39 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 05:19:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 05:20:32 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 01 Oct 2021 05:20:32 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 01 Oct 2021 05:20:32 GMT
ARG MARIADB_VERSION=1:10.5.12+maria~focal
# Fri, 01 Oct 2021 05:20:32 GMT
ENV MARIADB_VERSION=1:10.5.12+maria~focal
# Fri, 01 Oct 2021 05:20:32 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 05:20:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 05:20:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 05:20:57 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 05:20:57 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 05:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 05:20:57 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 05:20:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6f45e0fb03b087254fb0750ec2bbfbc7ea10f3eaaa2c3381f2ef6b3cf2c32b`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a10760fd6ecff1db568c4df08e4add59ea3424ae8b2ed2ac557f5239fa74d`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 5.5 MB (5489340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0645d99211dd422dc4b2c52d1005a518b5d9c76409584ee75faf26c78de36b`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 3.6 MB (3582638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff899ddf1cc12eb3161fb924245c2cdb096fe9cadd0b73128f7d3e45e4a0e6c`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e10ba5def77eae105b1dfab52bd41d16cba2895929673658ec8fedc7d8408e`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.3 MB (2274765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef565721758b7adafc1e282adeddbe68df6d6631699124a860c60f5c507840b4`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827d88322c0fbf9af8d3af5b2a11e87dac976d5cdcd466a49564fedcc0d979f8`  
		Last Modified: Fri, 01 Oct 2021 05:24:55 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73de2e05944a2f6723efe83f89f004960c463f7754ed1a0045ad484845f8545`  
		Last Modified: Fri, 01 Oct 2021 05:25:08 GMT  
		Size: 86.9 MB (86937676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb6b36ede734262ad3b61f725fb5918b4b90621d55ef9608ec95d6b9ceaca4c`  
		Last Modified: Fri, 01 Oct 2021 05:24:55 GMT  
		Size: 5.6 KB (5610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:693dc7438e76753b2268f6c4493ef6844e31e3c71f504e9c0f52e3428dad6cb9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124311951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4569802db431aa0e364a1dc990bbc1bd13a9e689a30b1b8930a6f872bea628`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:38:47 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 03:38:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:38:56 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 03:39:11 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 03:39:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 03:39:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:39:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 03:39:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 03:40:04 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 01 Oct 2021 03:40:04 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 01 Oct 2021 03:40:04 GMT
ARG MARIADB_VERSION=1:10.5.12+maria~focal
# Fri, 01 Oct 2021 03:40:04 GMT
ENV MARIADB_VERSION=1:10.5.12+maria~focal
# Fri, 01 Oct 2021 03:40:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 03:40:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 03:40:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 03:40:26 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 03:40:27 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 03:40:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 03:40:27 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 03:40:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d5ae241c1f10925c65b1658513761cd873e86632ea54cd491a17314c717db9`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1337b7de0aecaa84469be03f6aca5f4716813a7f70d6df52ada4f37e67dce98`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 5.5 MB (5455225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720ecfb64bf9977e96130e89f4d49759a1b9577aabaa5c864b0f7a3c0473f778`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 3.4 MB (3368539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba0c987cf142da7e613c8eb5506412f33e85d62e8b737d82ae8a86dad1a3dd1`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1cd2ca1d8beab7fe86d456206b59ee252c55fd199373f2caae49c71ec65a2a`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.2 MB (2203545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9328b4fc02fb1261cd4016d0e4d31dd6528b268e170d8278afbd062e3a96fa1`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e83551fceb22ef951d01f5c7b3c731ef65a3ce5134cff79beaf9a7ddab84d0`  
		Last Modified: Fri, 01 Oct 2021 03:44:46 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c055bdbde0df919694eedcd426329a549f55f8f44af11815a2681df052cbb7a9`  
		Last Modified: Fri, 01 Oct 2021 03:45:01 GMT  
		Size: 86.1 MB (86101907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d24b32215f5f5d263e7c68bbfdfe19229efa899099bac6d5eebfb02057f009dc`  
		Last Modified: Fri, 01 Oct 2021 03:44:47 GMT  
		Size: 5.6 KB (5611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:4f8d9dd96a6dbef3deb6138d39cfc38f8d0277a783db2e39a34d7a054b674684
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137580279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea3573cf742f38dedaa04d69169803bfa123f2c4d59e9b3c0c592ab22381be5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:34:53 GMT
ENV GOSU_VERSION=1.13
# Sat, 16 Oct 2021 01:35:28 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 01:35:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 01:36:02 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:36:03 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 16 Oct 2021 01:36:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 01:39:39 GMT
ARG MARIADB_MAJOR=10.5
# Sat, 16 Oct 2021 01:39:42 GMT
ENV MARIADB_MAJOR=10.5
# Sat, 16 Oct 2021 01:39:45 GMT
ARG MARIADB_VERSION=1:10.5.12+maria~focal
# Sat, 16 Oct 2021 01:39:47 GMT
ENV MARIADB_VERSION=1:10.5.12+maria~focal
# Sat, 16 Oct 2021 01:39:49 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
# Sat, 16 Oct 2021 01:39:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 16 Oct 2021 01:41:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 16 Oct 2021 01:41:52 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Oct 2021 01:41:54 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:41:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Oct 2021 01:42:00 GMT
EXPOSE 3306
# Sat, 16 Oct 2021 01:42:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bdbddf0ed762c90ab4fcfe1f42007a96e4f90ca4f0765dfcec52213a3f5c12`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 3.7 MB (3670760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cc95e86fb5ab1bda9839a1ecbd3c2d607bc6cfc5155f33bf32c9d7827ec98b`  
		Last Modified: Sat, 16 Oct 2021 01:49:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe2cefdba07cb9fc803227a545d4fcc196038c1020de7698bf4e333d9056cbd`  
		Last Modified: Sat, 16 Oct 2021 01:49:28 GMT  
		Size: 2.6 MB (2573066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab77c7b0e7b171541e9f7f813ef81190ef39151aea54bfe2b64f8c191ce672c`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec67cba87144a745f61e6d90badf06dd6518c512a3b7a067623cdeb4b9cec79`  
		Last Modified: Sat, 16 Oct 2021 01:50:16 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def963c9f47e8420d77e6cd15e6dc91a13dd6a6505af461e51c341d383391007`  
		Last Modified: Sat, 16 Oct 2021 01:50:34 GMT  
		Size: 91.4 MB (91370902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec1682d32f1d61eec73e062f876c8ea7b60b2bbd1ca6c8517026f735a72bf88`  
		Last Modified: Sat, 16 Oct 2021 01:50:16 GMT  
		Size: 5.6 KB (5611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:7f7a7b0832e1b134a141c55274c96532dd995cc1ae0e963b6a928dc890847d2b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (126048014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f672fd796e85e5a330f1f56ebd53ff3b67f962c269decf39128ae22f9ab408f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:02:36 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:02:41 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:02:42 GMT
ENV GOSU_VERSION=1.13
# Sat, 16 Oct 2021 01:02:50 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 01:02:51 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 01:02:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:02:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 16 Oct 2021 01:03:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 01:03:35 GMT
ARG MARIADB_MAJOR=10.5
# Sat, 16 Oct 2021 01:03:35 GMT
ENV MARIADB_MAJOR=10.5
# Sat, 16 Oct 2021 01:03:35 GMT
ARG MARIADB_VERSION=1:10.5.12+maria~focal
# Sat, 16 Oct 2021 01:03:35 GMT
ENV MARIADB_VERSION=1:10.5.12+maria~focal
# Sat, 16 Oct 2021 01:03:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
# Sat, 16 Oct 2021 01:03:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 16 Oct 2021 01:03:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 16 Oct 2021 01:03:58 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Oct 2021 01:03:58 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:03:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Oct 2021 01:03:58 GMT
EXPOSE 3306
# Sat, 16 Oct 2021 01:03:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc30a1fd200d10ce23e934b30e72d36ea131fb670d30afe697304591986fe1`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228a3fc0a9531bf3e9e08d9800daffbe33729ba8a16fb427b07a1a36fb047e02`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 5.4 MB (5380980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e511a129710d7aa78451eebec778e60a256b2a9e60db59a9f6d09641bd4f96`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 3.2 MB (3239822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a9cf411b6c206dca4cd2f493440c36781e332782682bb40969b6640e8e98e9`  
		Last Modified: Sat, 16 Oct 2021 01:04:31 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cac3f3cdb186c64fce6e0a7efc39abe96d0e6ab755d9193c981cc44c801cc51`  
		Last Modified: Sat, 16 Oct 2021 01:04:31 GMT  
		Size: 2.2 MB (2188905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd5f55dd4f1666fe90f4ca1b3b0cc36a9092c44ae19033a4d2b7b0e2ff3dddb`  
		Last Modified: Sat, 16 Oct 2021 01:04:30 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba27885bcb0e790f7990ad6b69669737ee44b5902deec85e48298b05b09835c`  
		Last Modified: Sat, 16 Oct 2021 01:05:06 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4814429007deb3858bf50326ba8c969e2a7b313c61ad7c5c387ed893d9d1f743`  
		Last Modified: Sat, 16 Oct 2021 01:05:18 GMT  
		Size: 88.1 MB (88107119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0aac5e8a79c251782a156851ac4e82652f50218e26b06c096f762d33782377c`  
		Last Modified: Sat, 16 Oct 2021 01:05:06 GMT  
		Size: 5.6 KB (5610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.12`

```console
$ docker pull mariadb@sha256:b125a538789176c1a428f89f3ce7bf3018821c10d6cf2719a6ff055f13810708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5.12` - linux; amd64

```console
$ docker pull mariadb@sha256:15994bfb5fd4700cc6180c92752550488d2cfcaeca45a921fe28657b67da5df4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126863664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02241ea3e9b943595157787d6ad7737572ff7670070d6abf32e2bc446f3a235c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:19:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 05:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:18 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 05:19:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 05:19:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 05:19:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:39 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 05:19:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 05:20:32 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 01 Oct 2021 05:20:32 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 01 Oct 2021 05:20:32 GMT
ARG MARIADB_VERSION=1:10.5.12+maria~focal
# Fri, 01 Oct 2021 05:20:32 GMT
ENV MARIADB_VERSION=1:10.5.12+maria~focal
# Fri, 01 Oct 2021 05:20:32 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 05:20:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 05:20:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 05:20:57 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 05:20:57 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 05:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 05:20:57 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 05:20:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6f45e0fb03b087254fb0750ec2bbfbc7ea10f3eaaa2c3381f2ef6b3cf2c32b`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a10760fd6ecff1db568c4df08e4add59ea3424ae8b2ed2ac557f5239fa74d`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 5.5 MB (5489340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0645d99211dd422dc4b2c52d1005a518b5d9c76409584ee75faf26c78de36b`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 3.6 MB (3582638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff899ddf1cc12eb3161fb924245c2cdb096fe9cadd0b73128f7d3e45e4a0e6c`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e10ba5def77eae105b1dfab52bd41d16cba2895929673658ec8fedc7d8408e`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.3 MB (2274765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef565721758b7adafc1e282adeddbe68df6d6631699124a860c60f5c507840b4`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827d88322c0fbf9af8d3af5b2a11e87dac976d5cdcd466a49564fedcc0d979f8`  
		Last Modified: Fri, 01 Oct 2021 05:24:55 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73de2e05944a2f6723efe83f89f004960c463f7754ed1a0045ad484845f8545`  
		Last Modified: Fri, 01 Oct 2021 05:25:08 GMT  
		Size: 86.9 MB (86937676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb6b36ede734262ad3b61f725fb5918b4b90621d55ef9608ec95d6b9ceaca4c`  
		Last Modified: Fri, 01 Oct 2021 05:24:55 GMT  
		Size: 5.6 KB (5610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.12` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:693dc7438e76753b2268f6c4493ef6844e31e3c71f504e9c0f52e3428dad6cb9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124311951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4569802db431aa0e364a1dc990bbc1bd13a9e689a30b1b8930a6f872bea628`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:38:47 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 03:38:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:38:56 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 03:39:11 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 03:39:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 03:39:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:39:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 03:39:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 03:40:04 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 01 Oct 2021 03:40:04 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 01 Oct 2021 03:40:04 GMT
ARG MARIADB_VERSION=1:10.5.12+maria~focal
# Fri, 01 Oct 2021 03:40:04 GMT
ENV MARIADB_VERSION=1:10.5.12+maria~focal
# Fri, 01 Oct 2021 03:40:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 03:40:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 03:40:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 03:40:26 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 03:40:27 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 03:40:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 03:40:27 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 03:40:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d5ae241c1f10925c65b1658513761cd873e86632ea54cd491a17314c717db9`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1337b7de0aecaa84469be03f6aca5f4716813a7f70d6df52ada4f37e67dce98`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 5.5 MB (5455225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720ecfb64bf9977e96130e89f4d49759a1b9577aabaa5c864b0f7a3c0473f778`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 3.4 MB (3368539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba0c987cf142da7e613c8eb5506412f33e85d62e8b737d82ae8a86dad1a3dd1`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1cd2ca1d8beab7fe86d456206b59ee252c55fd199373f2caae49c71ec65a2a`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.2 MB (2203545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9328b4fc02fb1261cd4016d0e4d31dd6528b268e170d8278afbd062e3a96fa1`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e83551fceb22ef951d01f5c7b3c731ef65a3ce5134cff79beaf9a7ddab84d0`  
		Last Modified: Fri, 01 Oct 2021 03:44:46 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c055bdbde0df919694eedcd426329a549f55f8f44af11815a2681df052cbb7a9`  
		Last Modified: Fri, 01 Oct 2021 03:45:01 GMT  
		Size: 86.1 MB (86101907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d24b32215f5f5d263e7c68bbfdfe19229efa899099bac6d5eebfb02057f009dc`  
		Last Modified: Fri, 01 Oct 2021 03:44:47 GMT  
		Size: 5.6 KB (5611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.12` - linux; ppc64le

```console
$ docker pull mariadb@sha256:4f8d9dd96a6dbef3deb6138d39cfc38f8d0277a783db2e39a34d7a054b674684
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137580279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea3573cf742f38dedaa04d69169803bfa123f2c4d59e9b3c0c592ab22381be5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:34:53 GMT
ENV GOSU_VERSION=1.13
# Sat, 16 Oct 2021 01:35:28 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 01:35:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 01:36:02 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:36:03 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 16 Oct 2021 01:36:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 01:39:39 GMT
ARG MARIADB_MAJOR=10.5
# Sat, 16 Oct 2021 01:39:42 GMT
ENV MARIADB_MAJOR=10.5
# Sat, 16 Oct 2021 01:39:45 GMT
ARG MARIADB_VERSION=1:10.5.12+maria~focal
# Sat, 16 Oct 2021 01:39:47 GMT
ENV MARIADB_VERSION=1:10.5.12+maria~focal
# Sat, 16 Oct 2021 01:39:49 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
# Sat, 16 Oct 2021 01:39:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 16 Oct 2021 01:41:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 16 Oct 2021 01:41:52 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Oct 2021 01:41:54 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:41:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Oct 2021 01:42:00 GMT
EXPOSE 3306
# Sat, 16 Oct 2021 01:42:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bdbddf0ed762c90ab4fcfe1f42007a96e4f90ca4f0765dfcec52213a3f5c12`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 3.7 MB (3670760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cc95e86fb5ab1bda9839a1ecbd3c2d607bc6cfc5155f33bf32c9d7827ec98b`  
		Last Modified: Sat, 16 Oct 2021 01:49:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe2cefdba07cb9fc803227a545d4fcc196038c1020de7698bf4e333d9056cbd`  
		Last Modified: Sat, 16 Oct 2021 01:49:28 GMT  
		Size: 2.6 MB (2573066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab77c7b0e7b171541e9f7f813ef81190ef39151aea54bfe2b64f8c191ce672c`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec67cba87144a745f61e6d90badf06dd6518c512a3b7a067623cdeb4b9cec79`  
		Last Modified: Sat, 16 Oct 2021 01:50:16 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def963c9f47e8420d77e6cd15e6dc91a13dd6a6505af461e51c341d383391007`  
		Last Modified: Sat, 16 Oct 2021 01:50:34 GMT  
		Size: 91.4 MB (91370902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec1682d32f1d61eec73e062f876c8ea7b60b2bbd1ca6c8517026f735a72bf88`  
		Last Modified: Sat, 16 Oct 2021 01:50:16 GMT  
		Size: 5.6 KB (5611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.12` - linux; s390x

```console
$ docker pull mariadb@sha256:7f7a7b0832e1b134a141c55274c96532dd995cc1ae0e963b6a928dc890847d2b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (126048014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f672fd796e85e5a330f1f56ebd53ff3b67f962c269decf39128ae22f9ab408f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:02:36 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:02:41 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:02:42 GMT
ENV GOSU_VERSION=1.13
# Sat, 16 Oct 2021 01:02:50 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 01:02:51 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 01:02:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:02:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 16 Oct 2021 01:03:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 01:03:35 GMT
ARG MARIADB_MAJOR=10.5
# Sat, 16 Oct 2021 01:03:35 GMT
ENV MARIADB_MAJOR=10.5
# Sat, 16 Oct 2021 01:03:35 GMT
ARG MARIADB_VERSION=1:10.5.12+maria~focal
# Sat, 16 Oct 2021 01:03:35 GMT
ENV MARIADB_VERSION=1:10.5.12+maria~focal
# Sat, 16 Oct 2021 01:03:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
# Sat, 16 Oct 2021 01:03:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 16 Oct 2021 01:03:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 16 Oct 2021 01:03:58 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Oct 2021 01:03:58 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:03:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Oct 2021 01:03:58 GMT
EXPOSE 3306
# Sat, 16 Oct 2021 01:03:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc30a1fd200d10ce23e934b30e72d36ea131fb670d30afe697304591986fe1`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228a3fc0a9531bf3e9e08d9800daffbe33729ba8a16fb427b07a1a36fb047e02`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 5.4 MB (5380980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e511a129710d7aa78451eebec778e60a256b2a9e60db59a9f6d09641bd4f96`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 3.2 MB (3239822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a9cf411b6c206dca4cd2f493440c36781e332782682bb40969b6640e8e98e9`  
		Last Modified: Sat, 16 Oct 2021 01:04:31 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cac3f3cdb186c64fce6e0a7efc39abe96d0e6ab755d9193c981cc44c801cc51`  
		Last Modified: Sat, 16 Oct 2021 01:04:31 GMT  
		Size: 2.2 MB (2188905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd5f55dd4f1666fe90f4ca1b3b0cc36a9092c44ae19033a4d2b7b0e2ff3dddb`  
		Last Modified: Sat, 16 Oct 2021 01:04:30 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba27885bcb0e790f7990ad6b69669737ee44b5902deec85e48298b05b09835c`  
		Last Modified: Sat, 16 Oct 2021 01:05:06 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4814429007deb3858bf50326ba8c969e2a7b313c61ad7c5c387ed893d9d1f743`  
		Last Modified: Sat, 16 Oct 2021 01:05:18 GMT  
		Size: 88.1 MB (88107119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0aac5e8a79c251782a156851ac4e82652f50218e26b06c096f762d33782377c`  
		Last Modified: Sat, 16 Oct 2021 01:05:06 GMT  
		Size: 5.6 KB (5610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.12-focal`

```console
$ docker pull mariadb@sha256:b125a538789176c1a428f89f3ce7bf3018821c10d6cf2719a6ff055f13810708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5.12-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:15994bfb5fd4700cc6180c92752550488d2cfcaeca45a921fe28657b67da5df4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126863664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02241ea3e9b943595157787d6ad7737572ff7670070d6abf32e2bc446f3a235c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:19:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 05:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:18 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 05:19:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 05:19:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 05:19:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:39 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 05:19:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 05:20:32 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 01 Oct 2021 05:20:32 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 01 Oct 2021 05:20:32 GMT
ARG MARIADB_VERSION=1:10.5.12+maria~focal
# Fri, 01 Oct 2021 05:20:32 GMT
ENV MARIADB_VERSION=1:10.5.12+maria~focal
# Fri, 01 Oct 2021 05:20:32 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 05:20:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 05:20:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 05:20:57 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 05:20:57 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 05:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 05:20:57 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 05:20:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6f45e0fb03b087254fb0750ec2bbfbc7ea10f3eaaa2c3381f2ef6b3cf2c32b`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a10760fd6ecff1db568c4df08e4add59ea3424ae8b2ed2ac557f5239fa74d`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 5.5 MB (5489340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0645d99211dd422dc4b2c52d1005a518b5d9c76409584ee75faf26c78de36b`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 3.6 MB (3582638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff899ddf1cc12eb3161fb924245c2cdb096fe9cadd0b73128f7d3e45e4a0e6c`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e10ba5def77eae105b1dfab52bd41d16cba2895929673658ec8fedc7d8408e`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.3 MB (2274765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef565721758b7adafc1e282adeddbe68df6d6631699124a860c60f5c507840b4`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827d88322c0fbf9af8d3af5b2a11e87dac976d5cdcd466a49564fedcc0d979f8`  
		Last Modified: Fri, 01 Oct 2021 05:24:55 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73de2e05944a2f6723efe83f89f004960c463f7754ed1a0045ad484845f8545`  
		Last Modified: Fri, 01 Oct 2021 05:25:08 GMT  
		Size: 86.9 MB (86937676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb6b36ede734262ad3b61f725fb5918b4b90621d55ef9608ec95d6b9ceaca4c`  
		Last Modified: Fri, 01 Oct 2021 05:24:55 GMT  
		Size: 5.6 KB (5610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.12-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:693dc7438e76753b2268f6c4493ef6844e31e3c71f504e9c0f52e3428dad6cb9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124311951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4569802db431aa0e364a1dc990bbc1bd13a9e689a30b1b8930a6f872bea628`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:38:47 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 03:38:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:38:56 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 03:39:11 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 03:39:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 03:39:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:39:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 03:39:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 03:40:04 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 01 Oct 2021 03:40:04 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 01 Oct 2021 03:40:04 GMT
ARG MARIADB_VERSION=1:10.5.12+maria~focal
# Fri, 01 Oct 2021 03:40:04 GMT
ENV MARIADB_VERSION=1:10.5.12+maria~focal
# Fri, 01 Oct 2021 03:40:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 03:40:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 03:40:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 03:40:26 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 03:40:27 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 03:40:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 03:40:27 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 03:40:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d5ae241c1f10925c65b1658513761cd873e86632ea54cd491a17314c717db9`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1337b7de0aecaa84469be03f6aca5f4716813a7f70d6df52ada4f37e67dce98`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 5.5 MB (5455225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720ecfb64bf9977e96130e89f4d49759a1b9577aabaa5c864b0f7a3c0473f778`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 3.4 MB (3368539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba0c987cf142da7e613c8eb5506412f33e85d62e8b737d82ae8a86dad1a3dd1`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1cd2ca1d8beab7fe86d456206b59ee252c55fd199373f2caae49c71ec65a2a`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.2 MB (2203545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9328b4fc02fb1261cd4016d0e4d31dd6528b268e170d8278afbd062e3a96fa1`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e83551fceb22ef951d01f5c7b3c731ef65a3ce5134cff79beaf9a7ddab84d0`  
		Last Modified: Fri, 01 Oct 2021 03:44:46 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c055bdbde0df919694eedcd426329a549f55f8f44af11815a2681df052cbb7a9`  
		Last Modified: Fri, 01 Oct 2021 03:45:01 GMT  
		Size: 86.1 MB (86101907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d24b32215f5f5d263e7c68bbfdfe19229efa899099bac6d5eebfb02057f009dc`  
		Last Modified: Fri, 01 Oct 2021 03:44:47 GMT  
		Size: 5.6 KB (5611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.12-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:4f8d9dd96a6dbef3deb6138d39cfc38f8d0277a783db2e39a34d7a054b674684
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137580279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea3573cf742f38dedaa04d69169803bfa123f2c4d59e9b3c0c592ab22381be5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:34:53 GMT
ENV GOSU_VERSION=1.13
# Sat, 16 Oct 2021 01:35:28 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 01:35:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 01:36:02 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:36:03 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 16 Oct 2021 01:36:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 01:39:39 GMT
ARG MARIADB_MAJOR=10.5
# Sat, 16 Oct 2021 01:39:42 GMT
ENV MARIADB_MAJOR=10.5
# Sat, 16 Oct 2021 01:39:45 GMT
ARG MARIADB_VERSION=1:10.5.12+maria~focal
# Sat, 16 Oct 2021 01:39:47 GMT
ENV MARIADB_VERSION=1:10.5.12+maria~focal
# Sat, 16 Oct 2021 01:39:49 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
# Sat, 16 Oct 2021 01:39:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 16 Oct 2021 01:41:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 16 Oct 2021 01:41:52 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Oct 2021 01:41:54 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:41:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Oct 2021 01:42:00 GMT
EXPOSE 3306
# Sat, 16 Oct 2021 01:42:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bdbddf0ed762c90ab4fcfe1f42007a96e4f90ca4f0765dfcec52213a3f5c12`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 3.7 MB (3670760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cc95e86fb5ab1bda9839a1ecbd3c2d607bc6cfc5155f33bf32c9d7827ec98b`  
		Last Modified: Sat, 16 Oct 2021 01:49:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe2cefdba07cb9fc803227a545d4fcc196038c1020de7698bf4e333d9056cbd`  
		Last Modified: Sat, 16 Oct 2021 01:49:28 GMT  
		Size: 2.6 MB (2573066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab77c7b0e7b171541e9f7f813ef81190ef39151aea54bfe2b64f8c191ce672c`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec67cba87144a745f61e6d90badf06dd6518c512a3b7a067623cdeb4b9cec79`  
		Last Modified: Sat, 16 Oct 2021 01:50:16 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def963c9f47e8420d77e6cd15e6dc91a13dd6a6505af461e51c341d383391007`  
		Last Modified: Sat, 16 Oct 2021 01:50:34 GMT  
		Size: 91.4 MB (91370902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec1682d32f1d61eec73e062f876c8ea7b60b2bbd1ca6c8517026f735a72bf88`  
		Last Modified: Sat, 16 Oct 2021 01:50:16 GMT  
		Size: 5.6 KB (5611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.12-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:7f7a7b0832e1b134a141c55274c96532dd995cc1ae0e963b6a928dc890847d2b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (126048014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f672fd796e85e5a330f1f56ebd53ff3b67f962c269decf39128ae22f9ab408f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:02:36 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:02:41 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:02:42 GMT
ENV GOSU_VERSION=1.13
# Sat, 16 Oct 2021 01:02:50 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 01:02:51 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 01:02:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:02:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 16 Oct 2021 01:03:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 01:03:35 GMT
ARG MARIADB_MAJOR=10.5
# Sat, 16 Oct 2021 01:03:35 GMT
ENV MARIADB_MAJOR=10.5
# Sat, 16 Oct 2021 01:03:35 GMT
ARG MARIADB_VERSION=1:10.5.12+maria~focal
# Sat, 16 Oct 2021 01:03:35 GMT
ENV MARIADB_VERSION=1:10.5.12+maria~focal
# Sat, 16 Oct 2021 01:03:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
# Sat, 16 Oct 2021 01:03:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 16 Oct 2021 01:03:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 16 Oct 2021 01:03:58 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Oct 2021 01:03:58 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:03:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Oct 2021 01:03:58 GMT
EXPOSE 3306
# Sat, 16 Oct 2021 01:03:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc30a1fd200d10ce23e934b30e72d36ea131fb670d30afe697304591986fe1`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228a3fc0a9531bf3e9e08d9800daffbe33729ba8a16fb427b07a1a36fb047e02`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 5.4 MB (5380980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e511a129710d7aa78451eebec778e60a256b2a9e60db59a9f6d09641bd4f96`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 3.2 MB (3239822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a9cf411b6c206dca4cd2f493440c36781e332782682bb40969b6640e8e98e9`  
		Last Modified: Sat, 16 Oct 2021 01:04:31 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cac3f3cdb186c64fce6e0a7efc39abe96d0e6ab755d9193c981cc44c801cc51`  
		Last Modified: Sat, 16 Oct 2021 01:04:31 GMT  
		Size: 2.2 MB (2188905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd5f55dd4f1666fe90f4ca1b3b0cc36a9092c44ae19033a4d2b7b0e2ff3dddb`  
		Last Modified: Sat, 16 Oct 2021 01:04:30 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba27885bcb0e790f7990ad6b69669737ee44b5902deec85e48298b05b09835c`  
		Last Modified: Sat, 16 Oct 2021 01:05:06 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4814429007deb3858bf50326ba8c969e2a7b313c61ad7c5c387ed893d9d1f743`  
		Last Modified: Sat, 16 Oct 2021 01:05:18 GMT  
		Size: 88.1 MB (88107119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0aac5e8a79c251782a156851ac4e82652f50218e26b06c096f762d33782377c`  
		Last Modified: Sat, 16 Oct 2021 01:05:06 GMT  
		Size: 5.6 KB (5610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6`

```console
$ docker pull mariadb@sha256:68a9a3ef9ee7b13438ba135a36643c43b7ec0e6f6e4a0ebae07dfb6539cededb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6` - linux; amd64

```console
$ docker pull mariadb@sha256:a9b26cdb3cfb008f4373b93cfd350ec51e3fbf2cbc227fc4da0cb6338851de07
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127015901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7220a722ce2a763177738b8cb0b42b3602368100ee7cc7088fb0bcc96fea1c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:19:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 05:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:18 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 05:19:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 05:19:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 05:19:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:39 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 05:19:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 05:19:50 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 01 Oct 2021 05:19:50 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 01 Oct 2021 05:19:50 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Fri, 01 Oct 2021 05:19:50 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Fri, 01 Oct 2021 05:19:51 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 05:19:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 05:20:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 05:20:26 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 05:20:26 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 05:20:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 05:20:26 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 05:20:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6f45e0fb03b087254fb0750ec2bbfbc7ea10f3eaaa2c3381f2ef6b3cf2c32b`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a10760fd6ecff1db568c4df08e4add59ea3424ae8b2ed2ac557f5239fa74d`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 5.5 MB (5489340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0645d99211dd422dc4b2c52d1005a518b5d9c76409584ee75faf26c78de36b`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 3.6 MB (3582638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff899ddf1cc12eb3161fb924245c2cdb096fe9cadd0b73128f7d3e45e4a0e6c`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e10ba5def77eae105b1dfab52bd41d16cba2895929673658ec8fedc7d8408e`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.3 MB (2274765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef565721758b7adafc1e282adeddbe68df6d6631699124a860c60f5c507840b4`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373c21a041dec3d49d5ab23634ca8c0141b8ec8504dfe832900a48a48baa5d10`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1a9ce482ccd35a23b4f61715fd76783510d6fb7832e6db07a37f77a2d31f36`  
		Last Modified: Fri, 01 Oct 2021 05:24:29 GMT  
		Size: 87.1 MB (87089918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecedf97e512c4f6e245cac1ca1aa143939b0cda2428ac65a108fc40470870576`  
		Last Modified: Fri, 01 Oct 2021 05:24:15 GMT  
		Size: 5.6 KB (5608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d7c05c4a4da3313b71382230d55dfdb154f05dde2637cb5abd717516cc29c90e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124307877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06bb3c39ebf3550feb4449c7f08243564fad0a09635993f85486e2305d3a395d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:38:47 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 03:38:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:38:56 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 03:39:11 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 03:39:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 03:39:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:39:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 03:39:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 03:39:29 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 01 Oct 2021 03:39:29 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 01 Oct 2021 03:39:29 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Fri, 01 Oct 2021 03:39:29 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Fri, 01 Oct 2021 03:39:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 03:39:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 03:39:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 03:39:54 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 03:39:55 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 03:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 03:39:55 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 03:39:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d5ae241c1f10925c65b1658513761cd873e86632ea54cd491a17314c717db9`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1337b7de0aecaa84469be03f6aca5f4716813a7f70d6df52ada4f37e67dce98`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 5.5 MB (5455225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720ecfb64bf9977e96130e89f4d49759a1b9577aabaa5c864b0f7a3c0473f778`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 3.4 MB (3368539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba0c987cf142da7e613c8eb5506412f33e85d62e8b737d82ae8a86dad1a3dd1`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1cd2ca1d8beab7fe86d456206b59ee252c55fd199373f2caae49c71ec65a2a`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.2 MB (2203545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9328b4fc02fb1261cd4016d0e4d31dd6528b268e170d8278afbd062e3a96fa1`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba1c8ccb51c846dc0a9271404c54d1917897030f09c2df37204078c31ffae94`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c825ac5e690d987bb7c9e20ac4d482d0b3d6d45e43e686f5494169516ea6380`  
		Last Modified: Fri, 01 Oct 2021 03:44:14 GMT  
		Size: 86.1 MB (86097833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2376eebe2a30870028a6b6ab6b9cf1b96551befdbee8ed82a18e56a125c83397`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; ppc64le

```console
$ docker pull mariadb@sha256:aa3c316f88dd9537eeaa7201d6d3c5f8d8732196ee6c9cd5ce553816c7a060d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137539722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a66b6be1b40e577fe733ec92528cf73ee97a8536e1fcddc9fe638aa9132f8173`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:34:53 GMT
ENV GOSU_VERSION=1.13
# Sat, 16 Oct 2021 01:35:28 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 01:35:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 01:36:02 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:36:03 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 16 Oct 2021 01:36:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 01:36:18 GMT
ARG MARIADB_MAJOR=10.6
# Sat, 16 Oct 2021 01:36:19 GMT
ENV MARIADB_MAJOR=10.6
# Sat, 16 Oct 2021 01:36:22 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Sat, 16 Oct 2021 01:36:24 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Sat, 16 Oct 2021 01:36:29 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Sat, 16 Oct 2021 01:36:39 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 16 Oct 2021 01:38:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 16 Oct 2021 01:39:01 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Oct 2021 01:39:03 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:39:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Oct 2021 01:39:08 GMT
EXPOSE 3306
# Sat, 16 Oct 2021 01:39:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bdbddf0ed762c90ab4fcfe1f42007a96e4f90ca4f0765dfcec52213a3f5c12`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 3.7 MB (3670760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cc95e86fb5ab1bda9839a1ecbd3c2d607bc6cfc5155f33bf32c9d7827ec98b`  
		Last Modified: Sat, 16 Oct 2021 01:49:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe2cefdba07cb9fc803227a545d4fcc196038c1020de7698bf4e333d9056cbd`  
		Last Modified: Sat, 16 Oct 2021 01:49:28 GMT  
		Size: 2.6 MB (2573066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab77c7b0e7b171541e9f7f813ef81190ef39151aea54bfe2b64f8c191ce672c`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d188c1c418692bd6c05728f7b542eab7acbdf502f48eaf84c762ba6b27718c`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288c0769408956c537d6b5b649bc2b69ffe5036157a0aa58dce6c17312680a33`  
		Last Modified: Sat, 16 Oct 2021 01:49:45 GMT  
		Size: 91.3 MB (91330343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4c9a0a37f40daaa1c904e99bb499d11db46dd87bd94236295d1ad90603ba74`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 5.6 KB (5613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; s390x

```console
$ docker pull mariadb@sha256:90bc202cc092060b6e454b7f2d06cbe792ffd3d7a2edefe42e30964c55d24dab
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (126014128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b71468a7107bd097e1852fade221839dfd4b89ee873666b6f7beda44310b7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:02:36 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:02:41 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:02:42 GMT
ENV GOSU_VERSION=1.13
# Sat, 16 Oct 2021 01:02:50 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 01:02:51 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 01:02:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:02:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 16 Oct 2021 01:03:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 01:03:03 GMT
ARG MARIADB_MAJOR=10.6
# Sat, 16 Oct 2021 01:03:03 GMT
ENV MARIADB_MAJOR=10.6
# Sat, 16 Oct 2021 01:03:03 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Sat, 16 Oct 2021 01:03:04 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Sat, 16 Oct 2021 01:03:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Sat, 16 Oct 2021 01:03:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 16 Oct 2021 01:03:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 16 Oct 2021 01:03:26 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Oct 2021 01:03:26 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:03:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Oct 2021 01:03:26 GMT
EXPOSE 3306
# Sat, 16 Oct 2021 01:03:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc30a1fd200d10ce23e934b30e72d36ea131fb670d30afe697304591986fe1`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228a3fc0a9531bf3e9e08d9800daffbe33729ba8a16fb427b07a1a36fb047e02`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 5.4 MB (5380980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e511a129710d7aa78451eebec778e60a256b2a9e60db59a9f6d09641bd4f96`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 3.2 MB (3239822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a9cf411b6c206dca4cd2f493440c36781e332782682bb40969b6640e8e98e9`  
		Last Modified: Sat, 16 Oct 2021 01:04:31 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cac3f3cdb186c64fce6e0a7efc39abe96d0e6ab755d9193c981cc44c801cc51`  
		Last Modified: Sat, 16 Oct 2021 01:04:31 GMT  
		Size: 2.2 MB (2188905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd5f55dd4f1666fe90f4ca1b3b0cc36a9092c44ae19033a4d2b7b0e2ff3dddb`  
		Last Modified: Sat, 16 Oct 2021 01:04:30 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0ae06775bbebbdaaf444830172bb614071d5d08004722e2ac0acc7dc0106c3`  
		Last Modified: Sat, 16 Oct 2021 01:04:30 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362403b21b44d69858c7a816e3ddbbd7cb67dac62386727c8ce11d44891fc990`  
		Last Modified: Sat, 16 Oct 2021 01:04:48 GMT  
		Size: 88.1 MB (88073232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48196c9046fbbce7d43754945286d36794d5f7eb923e2501d8a9a4ddc88b3dd3`  
		Last Modified: Sat, 16 Oct 2021 01:04:30 GMT  
		Size: 5.6 KB (5614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6-focal`

```console
$ docker pull mariadb@sha256:68a9a3ef9ee7b13438ba135a36643c43b7ec0e6f6e4a0ebae07dfb6539cededb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:a9b26cdb3cfb008f4373b93cfd350ec51e3fbf2cbc227fc4da0cb6338851de07
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127015901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7220a722ce2a763177738b8cb0b42b3602368100ee7cc7088fb0bcc96fea1c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:19:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 05:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:18 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 05:19:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 05:19:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 05:19:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:39 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 05:19:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 05:19:50 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 01 Oct 2021 05:19:50 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 01 Oct 2021 05:19:50 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Fri, 01 Oct 2021 05:19:50 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Fri, 01 Oct 2021 05:19:51 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 05:19:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 05:20:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 05:20:26 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 05:20:26 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 05:20:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 05:20:26 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 05:20:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6f45e0fb03b087254fb0750ec2bbfbc7ea10f3eaaa2c3381f2ef6b3cf2c32b`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a10760fd6ecff1db568c4df08e4add59ea3424ae8b2ed2ac557f5239fa74d`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 5.5 MB (5489340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0645d99211dd422dc4b2c52d1005a518b5d9c76409584ee75faf26c78de36b`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 3.6 MB (3582638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff899ddf1cc12eb3161fb924245c2cdb096fe9cadd0b73128f7d3e45e4a0e6c`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e10ba5def77eae105b1dfab52bd41d16cba2895929673658ec8fedc7d8408e`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.3 MB (2274765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef565721758b7adafc1e282adeddbe68df6d6631699124a860c60f5c507840b4`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373c21a041dec3d49d5ab23634ca8c0141b8ec8504dfe832900a48a48baa5d10`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1a9ce482ccd35a23b4f61715fd76783510d6fb7832e6db07a37f77a2d31f36`  
		Last Modified: Fri, 01 Oct 2021 05:24:29 GMT  
		Size: 87.1 MB (87089918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecedf97e512c4f6e245cac1ca1aa143939b0cda2428ac65a108fc40470870576`  
		Last Modified: Fri, 01 Oct 2021 05:24:15 GMT  
		Size: 5.6 KB (5608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d7c05c4a4da3313b71382230d55dfdb154f05dde2637cb5abd717516cc29c90e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124307877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06bb3c39ebf3550feb4449c7f08243564fad0a09635993f85486e2305d3a395d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:38:47 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 03:38:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:38:56 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 03:39:11 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 03:39:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 03:39:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:39:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 03:39:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 03:39:29 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 01 Oct 2021 03:39:29 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 01 Oct 2021 03:39:29 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Fri, 01 Oct 2021 03:39:29 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Fri, 01 Oct 2021 03:39:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 03:39:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 03:39:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 03:39:54 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 03:39:55 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 03:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 03:39:55 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 03:39:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d5ae241c1f10925c65b1658513761cd873e86632ea54cd491a17314c717db9`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1337b7de0aecaa84469be03f6aca5f4716813a7f70d6df52ada4f37e67dce98`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 5.5 MB (5455225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720ecfb64bf9977e96130e89f4d49759a1b9577aabaa5c864b0f7a3c0473f778`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 3.4 MB (3368539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba0c987cf142da7e613c8eb5506412f33e85d62e8b737d82ae8a86dad1a3dd1`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1cd2ca1d8beab7fe86d456206b59ee252c55fd199373f2caae49c71ec65a2a`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.2 MB (2203545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9328b4fc02fb1261cd4016d0e4d31dd6528b268e170d8278afbd062e3a96fa1`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba1c8ccb51c846dc0a9271404c54d1917897030f09c2df37204078c31ffae94`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c825ac5e690d987bb7c9e20ac4d482d0b3d6d45e43e686f5494169516ea6380`  
		Last Modified: Fri, 01 Oct 2021 03:44:14 GMT  
		Size: 86.1 MB (86097833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2376eebe2a30870028a6b6ab6b9cf1b96551befdbee8ed82a18e56a125c83397`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:aa3c316f88dd9537eeaa7201d6d3c5f8d8732196ee6c9cd5ce553816c7a060d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137539722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a66b6be1b40e577fe733ec92528cf73ee97a8536e1fcddc9fe638aa9132f8173`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:34:53 GMT
ENV GOSU_VERSION=1.13
# Sat, 16 Oct 2021 01:35:28 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 01:35:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 01:36:02 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:36:03 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 16 Oct 2021 01:36:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 01:36:18 GMT
ARG MARIADB_MAJOR=10.6
# Sat, 16 Oct 2021 01:36:19 GMT
ENV MARIADB_MAJOR=10.6
# Sat, 16 Oct 2021 01:36:22 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Sat, 16 Oct 2021 01:36:24 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Sat, 16 Oct 2021 01:36:29 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Sat, 16 Oct 2021 01:36:39 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 16 Oct 2021 01:38:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 16 Oct 2021 01:39:01 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Oct 2021 01:39:03 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:39:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Oct 2021 01:39:08 GMT
EXPOSE 3306
# Sat, 16 Oct 2021 01:39:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bdbddf0ed762c90ab4fcfe1f42007a96e4f90ca4f0765dfcec52213a3f5c12`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 3.7 MB (3670760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cc95e86fb5ab1bda9839a1ecbd3c2d607bc6cfc5155f33bf32c9d7827ec98b`  
		Last Modified: Sat, 16 Oct 2021 01:49:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe2cefdba07cb9fc803227a545d4fcc196038c1020de7698bf4e333d9056cbd`  
		Last Modified: Sat, 16 Oct 2021 01:49:28 GMT  
		Size: 2.6 MB (2573066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab77c7b0e7b171541e9f7f813ef81190ef39151aea54bfe2b64f8c191ce672c`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d188c1c418692bd6c05728f7b542eab7acbdf502f48eaf84c762ba6b27718c`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288c0769408956c537d6b5b649bc2b69ffe5036157a0aa58dce6c17312680a33`  
		Last Modified: Sat, 16 Oct 2021 01:49:45 GMT  
		Size: 91.3 MB (91330343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4c9a0a37f40daaa1c904e99bb499d11db46dd87bd94236295d1ad90603ba74`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 5.6 KB (5613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:90bc202cc092060b6e454b7f2d06cbe792ffd3d7a2edefe42e30964c55d24dab
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (126014128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b71468a7107bd097e1852fade221839dfd4b89ee873666b6f7beda44310b7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:02:36 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:02:41 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:02:42 GMT
ENV GOSU_VERSION=1.13
# Sat, 16 Oct 2021 01:02:50 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 01:02:51 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 01:02:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:02:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 16 Oct 2021 01:03:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 01:03:03 GMT
ARG MARIADB_MAJOR=10.6
# Sat, 16 Oct 2021 01:03:03 GMT
ENV MARIADB_MAJOR=10.6
# Sat, 16 Oct 2021 01:03:03 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Sat, 16 Oct 2021 01:03:04 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Sat, 16 Oct 2021 01:03:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Sat, 16 Oct 2021 01:03:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 16 Oct 2021 01:03:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 16 Oct 2021 01:03:26 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Oct 2021 01:03:26 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:03:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Oct 2021 01:03:26 GMT
EXPOSE 3306
# Sat, 16 Oct 2021 01:03:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc30a1fd200d10ce23e934b30e72d36ea131fb670d30afe697304591986fe1`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228a3fc0a9531bf3e9e08d9800daffbe33729ba8a16fb427b07a1a36fb047e02`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 5.4 MB (5380980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e511a129710d7aa78451eebec778e60a256b2a9e60db59a9f6d09641bd4f96`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 3.2 MB (3239822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a9cf411b6c206dca4cd2f493440c36781e332782682bb40969b6640e8e98e9`  
		Last Modified: Sat, 16 Oct 2021 01:04:31 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cac3f3cdb186c64fce6e0a7efc39abe96d0e6ab755d9193c981cc44c801cc51`  
		Last Modified: Sat, 16 Oct 2021 01:04:31 GMT  
		Size: 2.2 MB (2188905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd5f55dd4f1666fe90f4ca1b3b0cc36a9092c44ae19033a4d2b7b0e2ff3dddb`  
		Last Modified: Sat, 16 Oct 2021 01:04:30 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0ae06775bbebbdaaf444830172bb614071d5d08004722e2ac0acc7dc0106c3`  
		Last Modified: Sat, 16 Oct 2021 01:04:30 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362403b21b44d69858c7a816e3ddbbd7cb67dac62386727c8ce11d44891fc990`  
		Last Modified: Sat, 16 Oct 2021 01:04:48 GMT  
		Size: 88.1 MB (88073232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48196c9046fbbce7d43754945286d36794d5f7eb923e2501d8a9a4ddc88b3dd3`  
		Last Modified: Sat, 16 Oct 2021 01:04:30 GMT  
		Size: 5.6 KB (5614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6.4`

```console
$ docker pull mariadb@sha256:68a9a3ef9ee7b13438ba135a36643c43b7ec0e6f6e4a0ebae07dfb6539cededb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6.4` - linux; amd64

```console
$ docker pull mariadb@sha256:a9b26cdb3cfb008f4373b93cfd350ec51e3fbf2cbc227fc4da0cb6338851de07
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127015901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7220a722ce2a763177738b8cb0b42b3602368100ee7cc7088fb0bcc96fea1c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:19:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 05:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:18 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 05:19:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 05:19:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 05:19:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:39 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 05:19:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 05:19:50 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 01 Oct 2021 05:19:50 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 01 Oct 2021 05:19:50 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Fri, 01 Oct 2021 05:19:50 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Fri, 01 Oct 2021 05:19:51 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 05:19:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 05:20:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 05:20:26 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 05:20:26 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 05:20:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 05:20:26 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 05:20:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6f45e0fb03b087254fb0750ec2bbfbc7ea10f3eaaa2c3381f2ef6b3cf2c32b`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a10760fd6ecff1db568c4df08e4add59ea3424ae8b2ed2ac557f5239fa74d`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 5.5 MB (5489340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0645d99211dd422dc4b2c52d1005a518b5d9c76409584ee75faf26c78de36b`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 3.6 MB (3582638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff899ddf1cc12eb3161fb924245c2cdb096fe9cadd0b73128f7d3e45e4a0e6c`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e10ba5def77eae105b1dfab52bd41d16cba2895929673658ec8fedc7d8408e`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.3 MB (2274765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef565721758b7adafc1e282adeddbe68df6d6631699124a860c60f5c507840b4`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373c21a041dec3d49d5ab23634ca8c0141b8ec8504dfe832900a48a48baa5d10`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1a9ce482ccd35a23b4f61715fd76783510d6fb7832e6db07a37f77a2d31f36`  
		Last Modified: Fri, 01 Oct 2021 05:24:29 GMT  
		Size: 87.1 MB (87089918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecedf97e512c4f6e245cac1ca1aa143939b0cda2428ac65a108fc40470870576`  
		Last Modified: Fri, 01 Oct 2021 05:24:15 GMT  
		Size: 5.6 KB (5608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.4` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d7c05c4a4da3313b71382230d55dfdb154f05dde2637cb5abd717516cc29c90e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124307877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06bb3c39ebf3550feb4449c7f08243564fad0a09635993f85486e2305d3a395d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:38:47 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 03:38:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:38:56 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 03:39:11 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 03:39:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 03:39:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:39:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 03:39:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 03:39:29 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 01 Oct 2021 03:39:29 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 01 Oct 2021 03:39:29 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Fri, 01 Oct 2021 03:39:29 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Fri, 01 Oct 2021 03:39:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 03:39:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 03:39:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 03:39:54 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 03:39:55 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 03:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 03:39:55 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 03:39:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d5ae241c1f10925c65b1658513761cd873e86632ea54cd491a17314c717db9`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1337b7de0aecaa84469be03f6aca5f4716813a7f70d6df52ada4f37e67dce98`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 5.5 MB (5455225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720ecfb64bf9977e96130e89f4d49759a1b9577aabaa5c864b0f7a3c0473f778`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 3.4 MB (3368539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba0c987cf142da7e613c8eb5506412f33e85d62e8b737d82ae8a86dad1a3dd1`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1cd2ca1d8beab7fe86d456206b59ee252c55fd199373f2caae49c71ec65a2a`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.2 MB (2203545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9328b4fc02fb1261cd4016d0e4d31dd6528b268e170d8278afbd062e3a96fa1`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba1c8ccb51c846dc0a9271404c54d1917897030f09c2df37204078c31ffae94`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c825ac5e690d987bb7c9e20ac4d482d0b3d6d45e43e686f5494169516ea6380`  
		Last Modified: Fri, 01 Oct 2021 03:44:14 GMT  
		Size: 86.1 MB (86097833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2376eebe2a30870028a6b6ab6b9cf1b96551befdbee8ed82a18e56a125c83397`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.4` - linux; ppc64le

```console
$ docker pull mariadb@sha256:aa3c316f88dd9537eeaa7201d6d3c5f8d8732196ee6c9cd5ce553816c7a060d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137539722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a66b6be1b40e577fe733ec92528cf73ee97a8536e1fcddc9fe638aa9132f8173`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:34:53 GMT
ENV GOSU_VERSION=1.13
# Sat, 16 Oct 2021 01:35:28 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 01:35:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 01:36:02 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:36:03 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 16 Oct 2021 01:36:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 01:36:18 GMT
ARG MARIADB_MAJOR=10.6
# Sat, 16 Oct 2021 01:36:19 GMT
ENV MARIADB_MAJOR=10.6
# Sat, 16 Oct 2021 01:36:22 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Sat, 16 Oct 2021 01:36:24 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Sat, 16 Oct 2021 01:36:29 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Sat, 16 Oct 2021 01:36:39 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 16 Oct 2021 01:38:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 16 Oct 2021 01:39:01 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Oct 2021 01:39:03 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:39:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Oct 2021 01:39:08 GMT
EXPOSE 3306
# Sat, 16 Oct 2021 01:39:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bdbddf0ed762c90ab4fcfe1f42007a96e4f90ca4f0765dfcec52213a3f5c12`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 3.7 MB (3670760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cc95e86fb5ab1bda9839a1ecbd3c2d607bc6cfc5155f33bf32c9d7827ec98b`  
		Last Modified: Sat, 16 Oct 2021 01:49:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe2cefdba07cb9fc803227a545d4fcc196038c1020de7698bf4e333d9056cbd`  
		Last Modified: Sat, 16 Oct 2021 01:49:28 GMT  
		Size: 2.6 MB (2573066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab77c7b0e7b171541e9f7f813ef81190ef39151aea54bfe2b64f8c191ce672c`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d188c1c418692bd6c05728f7b542eab7acbdf502f48eaf84c762ba6b27718c`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288c0769408956c537d6b5b649bc2b69ffe5036157a0aa58dce6c17312680a33`  
		Last Modified: Sat, 16 Oct 2021 01:49:45 GMT  
		Size: 91.3 MB (91330343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4c9a0a37f40daaa1c904e99bb499d11db46dd87bd94236295d1ad90603ba74`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 5.6 KB (5613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.4` - linux; s390x

```console
$ docker pull mariadb@sha256:90bc202cc092060b6e454b7f2d06cbe792ffd3d7a2edefe42e30964c55d24dab
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (126014128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b71468a7107bd097e1852fade221839dfd4b89ee873666b6f7beda44310b7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:02:36 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:02:41 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:02:42 GMT
ENV GOSU_VERSION=1.13
# Sat, 16 Oct 2021 01:02:50 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 01:02:51 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 01:02:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:02:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 16 Oct 2021 01:03:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 01:03:03 GMT
ARG MARIADB_MAJOR=10.6
# Sat, 16 Oct 2021 01:03:03 GMT
ENV MARIADB_MAJOR=10.6
# Sat, 16 Oct 2021 01:03:03 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Sat, 16 Oct 2021 01:03:04 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Sat, 16 Oct 2021 01:03:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Sat, 16 Oct 2021 01:03:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 16 Oct 2021 01:03:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 16 Oct 2021 01:03:26 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Oct 2021 01:03:26 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:03:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Oct 2021 01:03:26 GMT
EXPOSE 3306
# Sat, 16 Oct 2021 01:03:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc30a1fd200d10ce23e934b30e72d36ea131fb670d30afe697304591986fe1`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228a3fc0a9531bf3e9e08d9800daffbe33729ba8a16fb427b07a1a36fb047e02`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 5.4 MB (5380980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e511a129710d7aa78451eebec778e60a256b2a9e60db59a9f6d09641bd4f96`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 3.2 MB (3239822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a9cf411b6c206dca4cd2f493440c36781e332782682bb40969b6640e8e98e9`  
		Last Modified: Sat, 16 Oct 2021 01:04:31 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cac3f3cdb186c64fce6e0a7efc39abe96d0e6ab755d9193c981cc44c801cc51`  
		Last Modified: Sat, 16 Oct 2021 01:04:31 GMT  
		Size: 2.2 MB (2188905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd5f55dd4f1666fe90f4ca1b3b0cc36a9092c44ae19033a4d2b7b0e2ff3dddb`  
		Last Modified: Sat, 16 Oct 2021 01:04:30 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0ae06775bbebbdaaf444830172bb614071d5d08004722e2ac0acc7dc0106c3`  
		Last Modified: Sat, 16 Oct 2021 01:04:30 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362403b21b44d69858c7a816e3ddbbd7cb67dac62386727c8ce11d44891fc990`  
		Last Modified: Sat, 16 Oct 2021 01:04:48 GMT  
		Size: 88.1 MB (88073232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48196c9046fbbce7d43754945286d36794d5f7eb923e2501d8a9a4ddc88b3dd3`  
		Last Modified: Sat, 16 Oct 2021 01:04:30 GMT  
		Size: 5.6 KB (5614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6.4-focal`

```console
$ docker pull mariadb@sha256:68a9a3ef9ee7b13438ba135a36643c43b7ec0e6f6e4a0ebae07dfb6539cededb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6.4-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:a9b26cdb3cfb008f4373b93cfd350ec51e3fbf2cbc227fc4da0cb6338851de07
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127015901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7220a722ce2a763177738b8cb0b42b3602368100ee7cc7088fb0bcc96fea1c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:19:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 05:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:18 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 05:19:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 05:19:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 05:19:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:39 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 05:19:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 05:19:50 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 01 Oct 2021 05:19:50 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 01 Oct 2021 05:19:50 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Fri, 01 Oct 2021 05:19:50 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Fri, 01 Oct 2021 05:19:51 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 05:19:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 05:20:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 05:20:26 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 05:20:26 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 05:20:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 05:20:26 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 05:20:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6f45e0fb03b087254fb0750ec2bbfbc7ea10f3eaaa2c3381f2ef6b3cf2c32b`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a10760fd6ecff1db568c4df08e4add59ea3424ae8b2ed2ac557f5239fa74d`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 5.5 MB (5489340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0645d99211dd422dc4b2c52d1005a518b5d9c76409584ee75faf26c78de36b`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 3.6 MB (3582638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff899ddf1cc12eb3161fb924245c2cdb096fe9cadd0b73128f7d3e45e4a0e6c`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e10ba5def77eae105b1dfab52bd41d16cba2895929673658ec8fedc7d8408e`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.3 MB (2274765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef565721758b7adafc1e282adeddbe68df6d6631699124a860c60f5c507840b4`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373c21a041dec3d49d5ab23634ca8c0141b8ec8504dfe832900a48a48baa5d10`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1a9ce482ccd35a23b4f61715fd76783510d6fb7832e6db07a37f77a2d31f36`  
		Last Modified: Fri, 01 Oct 2021 05:24:29 GMT  
		Size: 87.1 MB (87089918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecedf97e512c4f6e245cac1ca1aa143939b0cda2428ac65a108fc40470870576`  
		Last Modified: Fri, 01 Oct 2021 05:24:15 GMT  
		Size: 5.6 KB (5608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.4-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d7c05c4a4da3313b71382230d55dfdb154f05dde2637cb5abd717516cc29c90e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124307877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06bb3c39ebf3550feb4449c7f08243564fad0a09635993f85486e2305d3a395d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:38:47 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 03:38:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:38:56 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 03:39:11 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 03:39:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 03:39:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:39:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 03:39:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 03:39:29 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 01 Oct 2021 03:39:29 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 01 Oct 2021 03:39:29 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Fri, 01 Oct 2021 03:39:29 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Fri, 01 Oct 2021 03:39:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 03:39:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 03:39:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 03:39:54 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 03:39:55 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 03:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 03:39:55 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 03:39:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d5ae241c1f10925c65b1658513761cd873e86632ea54cd491a17314c717db9`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1337b7de0aecaa84469be03f6aca5f4716813a7f70d6df52ada4f37e67dce98`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 5.5 MB (5455225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720ecfb64bf9977e96130e89f4d49759a1b9577aabaa5c864b0f7a3c0473f778`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 3.4 MB (3368539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba0c987cf142da7e613c8eb5506412f33e85d62e8b737d82ae8a86dad1a3dd1`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1cd2ca1d8beab7fe86d456206b59ee252c55fd199373f2caae49c71ec65a2a`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.2 MB (2203545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9328b4fc02fb1261cd4016d0e4d31dd6528b268e170d8278afbd062e3a96fa1`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba1c8ccb51c846dc0a9271404c54d1917897030f09c2df37204078c31ffae94`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c825ac5e690d987bb7c9e20ac4d482d0b3d6d45e43e686f5494169516ea6380`  
		Last Modified: Fri, 01 Oct 2021 03:44:14 GMT  
		Size: 86.1 MB (86097833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2376eebe2a30870028a6b6ab6b9cf1b96551befdbee8ed82a18e56a125c83397`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.4-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:aa3c316f88dd9537eeaa7201d6d3c5f8d8732196ee6c9cd5ce553816c7a060d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137539722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a66b6be1b40e577fe733ec92528cf73ee97a8536e1fcddc9fe638aa9132f8173`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:34:53 GMT
ENV GOSU_VERSION=1.13
# Sat, 16 Oct 2021 01:35:28 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 01:35:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 01:36:02 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:36:03 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 16 Oct 2021 01:36:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 01:36:18 GMT
ARG MARIADB_MAJOR=10.6
# Sat, 16 Oct 2021 01:36:19 GMT
ENV MARIADB_MAJOR=10.6
# Sat, 16 Oct 2021 01:36:22 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Sat, 16 Oct 2021 01:36:24 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Sat, 16 Oct 2021 01:36:29 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Sat, 16 Oct 2021 01:36:39 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 16 Oct 2021 01:38:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 16 Oct 2021 01:39:01 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Oct 2021 01:39:03 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:39:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Oct 2021 01:39:08 GMT
EXPOSE 3306
# Sat, 16 Oct 2021 01:39:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bdbddf0ed762c90ab4fcfe1f42007a96e4f90ca4f0765dfcec52213a3f5c12`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 3.7 MB (3670760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cc95e86fb5ab1bda9839a1ecbd3c2d607bc6cfc5155f33bf32c9d7827ec98b`  
		Last Modified: Sat, 16 Oct 2021 01:49:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe2cefdba07cb9fc803227a545d4fcc196038c1020de7698bf4e333d9056cbd`  
		Last Modified: Sat, 16 Oct 2021 01:49:28 GMT  
		Size: 2.6 MB (2573066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab77c7b0e7b171541e9f7f813ef81190ef39151aea54bfe2b64f8c191ce672c`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d188c1c418692bd6c05728f7b542eab7acbdf502f48eaf84c762ba6b27718c`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288c0769408956c537d6b5b649bc2b69ffe5036157a0aa58dce6c17312680a33`  
		Last Modified: Sat, 16 Oct 2021 01:49:45 GMT  
		Size: 91.3 MB (91330343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4c9a0a37f40daaa1c904e99bb499d11db46dd87bd94236295d1ad90603ba74`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 5.6 KB (5613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.4-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:90bc202cc092060b6e454b7f2d06cbe792ffd3d7a2edefe42e30964c55d24dab
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (126014128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b71468a7107bd097e1852fade221839dfd4b89ee873666b6f7beda44310b7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:02:36 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:02:41 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:02:42 GMT
ENV GOSU_VERSION=1.13
# Sat, 16 Oct 2021 01:02:50 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 01:02:51 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 01:02:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:02:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 16 Oct 2021 01:03:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 01:03:03 GMT
ARG MARIADB_MAJOR=10.6
# Sat, 16 Oct 2021 01:03:03 GMT
ENV MARIADB_MAJOR=10.6
# Sat, 16 Oct 2021 01:03:03 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Sat, 16 Oct 2021 01:03:04 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Sat, 16 Oct 2021 01:03:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Sat, 16 Oct 2021 01:03:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 16 Oct 2021 01:03:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 16 Oct 2021 01:03:26 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Oct 2021 01:03:26 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:03:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Oct 2021 01:03:26 GMT
EXPOSE 3306
# Sat, 16 Oct 2021 01:03:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc30a1fd200d10ce23e934b30e72d36ea131fb670d30afe697304591986fe1`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228a3fc0a9531bf3e9e08d9800daffbe33729ba8a16fb427b07a1a36fb047e02`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 5.4 MB (5380980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e511a129710d7aa78451eebec778e60a256b2a9e60db59a9f6d09641bd4f96`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 3.2 MB (3239822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a9cf411b6c206dca4cd2f493440c36781e332782682bb40969b6640e8e98e9`  
		Last Modified: Sat, 16 Oct 2021 01:04:31 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cac3f3cdb186c64fce6e0a7efc39abe96d0e6ab755d9193c981cc44c801cc51`  
		Last Modified: Sat, 16 Oct 2021 01:04:31 GMT  
		Size: 2.2 MB (2188905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd5f55dd4f1666fe90f4ca1b3b0cc36a9092c44ae19033a4d2b7b0e2ff3dddb`  
		Last Modified: Sat, 16 Oct 2021 01:04:30 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0ae06775bbebbdaaf444830172bb614071d5d08004722e2ac0acc7dc0106c3`  
		Last Modified: Sat, 16 Oct 2021 01:04:30 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362403b21b44d69858c7a816e3ddbbd7cb67dac62386727c8ce11d44891fc990`  
		Last Modified: Sat, 16 Oct 2021 01:04:48 GMT  
		Size: 88.1 MB (88073232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48196c9046fbbce7d43754945286d36794d5f7eb923e2501d8a9a4ddc88b3dd3`  
		Last Modified: Sat, 16 Oct 2021 01:04:30 GMT  
		Size: 5.6 KB (5614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:focal`

```console
$ docker pull mariadb@sha256:68a9a3ef9ee7b13438ba135a36643c43b7ec0e6f6e4a0ebae07dfb6539cededb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:focal` - linux; amd64

```console
$ docker pull mariadb@sha256:a9b26cdb3cfb008f4373b93cfd350ec51e3fbf2cbc227fc4da0cb6338851de07
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127015901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7220a722ce2a763177738b8cb0b42b3602368100ee7cc7088fb0bcc96fea1c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:19:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 05:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:18 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 05:19:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 05:19:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 05:19:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:39 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 05:19:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 05:19:50 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 01 Oct 2021 05:19:50 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 01 Oct 2021 05:19:50 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Fri, 01 Oct 2021 05:19:50 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Fri, 01 Oct 2021 05:19:51 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 05:19:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 05:20:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 05:20:26 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 05:20:26 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 05:20:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 05:20:26 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 05:20:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6f45e0fb03b087254fb0750ec2bbfbc7ea10f3eaaa2c3381f2ef6b3cf2c32b`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a10760fd6ecff1db568c4df08e4add59ea3424ae8b2ed2ac557f5239fa74d`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 5.5 MB (5489340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0645d99211dd422dc4b2c52d1005a518b5d9c76409584ee75faf26c78de36b`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 3.6 MB (3582638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff899ddf1cc12eb3161fb924245c2cdb096fe9cadd0b73128f7d3e45e4a0e6c`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e10ba5def77eae105b1dfab52bd41d16cba2895929673658ec8fedc7d8408e`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.3 MB (2274765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef565721758b7adafc1e282adeddbe68df6d6631699124a860c60f5c507840b4`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373c21a041dec3d49d5ab23634ca8c0141b8ec8504dfe832900a48a48baa5d10`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1a9ce482ccd35a23b4f61715fd76783510d6fb7832e6db07a37f77a2d31f36`  
		Last Modified: Fri, 01 Oct 2021 05:24:29 GMT  
		Size: 87.1 MB (87089918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecedf97e512c4f6e245cac1ca1aa143939b0cda2428ac65a108fc40470870576`  
		Last Modified: Fri, 01 Oct 2021 05:24:15 GMT  
		Size: 5.6 KB (5608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d7c05c4a4da3313b71382230d55dfdb154f05dde2637cb5abd717516cc29c90e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124307877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06bb3c39ebf3550feb4449c7f08243564fad0a09635993f85486e2305d3a395d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:38:47 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 03:38:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:38:56 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 03:39:11 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 03:39:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 03:39:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:39:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 03:39:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 03:39:29 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 01 Oct 2021 03:39:29 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 01 Oct 2021 03:39:29 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Fri, 01 Oct 2021 03:39:29 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Fri, 01 Oct 2021 03:39:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 03:39:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 03:39:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 03:39:54 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 03:39:55 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 03:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 03:39:55 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 03:39:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d5ae241c1f10925c65b1658513761cd873e86632ea54cd491a17314c717db9`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1337b7de0aecaa84469be03f6aca5f4716813a7f70d6df52ada4f37e67dce98`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 5.5 MB (5455225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720ecfb64bf9977e96130e89f4d49759a1b9577aabaa5c864b0f7a3c0473f778`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 3.4 MB (3368539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba0c987cf142da7e613c8eb5506412f33e85d62e8b737d82ae8a86dad1a3dd1`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1cd2ca1d8beab7fe86d456206b59ee252c55fd199373f2caae49c71ec65a2a`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.2 MB (2203545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9328b4fc02fb1261cd4016d0e4d31dd6528b268e170d8278afbd062e3a96fa1`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba1c8ccb51c846dc0a9271404c54d1917897030f09c2df37204078c31ffae94`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c825ac5e690d987bb7c9e20ac4d482d0b3d6d45e43e686f5494169516ea6380`  
		Last Modified: Fri, 01 Oct 2021 03:44:14 GMT  
		Size: 86.1 MB (86097833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2376eebe2a30870028a6b6ab6b9cf1b96551befdbee8ed82a18e56a125c83397`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:aa3c316f88dd9537eeaa7201d6d3c5f8d8732196ee6c9cd5ce553816c7a060d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137539722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a66b6be1b40e577fe733ec92528cf73ee97a8536e1fcddc9fe638aa9132f8173`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:34:53 GMT
ENV GOSU_VERSION=1.13
# Sat, 16 Oct 2021 01:35:28 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 01:35:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 01:36:02 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:36:03 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 16 Oct 2021 01:36:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 01:36:18 GMT
ARG MARIADB_MAJOR=10.6
# Sat, 16 Oct 2021 01:36:19 GMT
ENV MARIADB_MAJOR=10.6
# Sat, 16 Oct 2021 01:36:22 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Sat, 16 Oct 2021 01:36:24 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Sat, 16 Oct 2021 01:36:29 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Sat, 16 Oct 2021 01:36:39 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 16 Oct 2021 01:38:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 16 Oct 2021 01:39:01 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Oct 2021 01:39:03 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:39:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Oct 2021 01:39:08 GMT
EXPOSE 3306
# Sat, 16 Oct 2021 01:39:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bdbddf0ed762c90ab4fcfe1f42007a96e4f90ca4f0765dfcec52213a3f5c12`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 3.7 MB (3670760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cc95e86fb5ab1bda9839a1ecbd3c2d607bc6cfc5155f33bf32c9d7827ec98b`  
		Last Modified: Sat, 16 Oct 2021 01:49:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe2cefdba07cb9fc803227a545d4fcc196038c1020de7698bf4e333d9056cbd`  
		Last Modified: Sat, 16 Oct 2021 01:49:28 GMT  
		Size: 2.6 MB (2573066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab77c7b0e7b171541e9f7f813ef81190ef39151aea54bfe2b64f8c191ce672c`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d188c1c418692bd6c05728f7b542eab7acbdf502f48eaf84c762ba6b27718c`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288c0769408956c537d6b5b649bc2b69ffe5036157a0aa58dce6c17312680a33`  
		Last Modified: Sat, 16 Oct 2021 01:49:45 GMT  
		Size: 91.3 MB (91330343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4c9a0a37f40daaa1c904e99bb499d11db46dd87bd94236295d1ad90603ba74`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 5.6 KB (5613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; s390x

```console
$ docker pull mariadb@sha256:90bc202cc092060b6e454b7f2d06cbe792ffd3d7a2edefe42e30964c55d24dab
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (126014128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b71468a7107bd097e1852fade221839dfd4b89ee873666b6f7beda44310b7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:02:36 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:02:41 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:02:42 GMT
ENV GOSU_VERSION=1.13
# Sat, 16 Oct 2021 01:02:50 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 01:02:51 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 01:02:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:02:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 16 Oct 2021 01:03:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 01:03:03 GMT
ARG MARIADB_MAJOR=10.6
# Sat, 16 Oct 2021 01:03:03 GMT
ENV MARIADB_MAJOR=10.6
# Sat, 16 Oct 2021 01:03:03 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Sat, 16 Oct 2021 01:03:04 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Sat, 16 Oct 2021 01:03:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Sat, 16 Oct 2021 01:03:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 16 Oct 2021 01:03:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 16 Oct 2021 01:03:26 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Oct 2021 01:03:26 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:03:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Oct 2021 01:03:26 GMT
EXPOSE 3306
# Sat, 16 Oct 2021 01:03:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc30a1fd200d10ce23e934b30e72d36ea131fb670d30afe697304591986fe1`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228a3fc0a9531bf3e9e08d9800daffbe33729ba8a16fb427b07a1a36fb047e02`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 5.4 MB (5380980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e511a129710d7aa78451eebec778e60a256b2a9e60db59a9f6d09641bd4f96`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 3.2 MB (3239822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a9cf411b6c206dca4cd2f493440c36781e332782682bb40969b6640e8e98e9`  
		Last Modified: Sat, 16 Oct 2021 01:04:31 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cac3f3cdb186c64fce6e0a7efc39abe96d0e6ab755d9193c981cc44c801cc51`  
		Last Modified: Sat, 16 Oct 2021 01:04:31 GMT  
		Size: 2.2 MB (2188905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd5f55dd4f1666fe90f4ca1b3b0cc36a9092c44ae19033a4d2b7b0e2ff3dddb`  
		Last Modified: Sat, 16 Oct 2021 01:04:30 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0ae06775bbebbdaaf444830172bb614071d5d08004722e2ac0acc7dc0106c3`  
		Last Modified: Sat, 16 Oct 2021 01:04:30 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362403b21b44d69858c7a816e3ddbbd7cb67dac62386727c8ce11d44891fc990`  
		Last Modified: Sat, 16 Oct 2021 01:04:48 GMT  
		Size: 88.1 MB (88073232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48196c9046fbbce7d43754945286d36794d5f7eb923e2501d8a9a4ddc88b3dd3`  
		Last Modified: Sat, 16 Oct 2021 01:04:30 GMT  
		Size: 5.6 KB (5614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:latest`

```console
$ docker pull mariadb@sha256:68a9a3ef9ee7b13438ba135a36643c43b7ec0e6f6e4a0ebae07dfb6539cededb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:latest` - linux; amd64

```console
$ docker pull mariadb@sha256:a9b26cdb3cfb008f4373b93cfd350ec51e3fbf2cbc227fc4da0cb6338851de07
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127015901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7220a722ce2a763177738b8cb0b42b3602368100ee7cc7088fb0bcc96fea1c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:19:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 05:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:18 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 05:19:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 05:19:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 05:19:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:19:39 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 05:19:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 05:19:50 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 01 Oct 2021 05:19:50 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 01 Oct 2021 05:19:50 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Fri, 01 Oct 2021 05:19:50 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Fri, 01 Oct 2021 05:19:51 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 05:19:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 05:20:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 05:20:26 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 05:20:26 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 05:20:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 05:20:26 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 05:20:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6f45e0fb03b087254fb0750ec2bbfbc7ea10f3eaaa2c3381f2ef6b3cf2c32b`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a10760fd6ecff1db568c4df08e4add59ea3424ae8b2ed2ac557f5239fa74d`  
		Last Modified: Fri, 01 Oct 2021 05:24:19 GMT  
		Size: 5.5 MB (5489340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0645d99211dd422dc4b2c52d1005a518b5d9c76409584ee75faf26c78de36b`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 3.6 MB (3582638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff899ddf1cc12eb3161fb924245c2cdb096fe9cadd0b73128f7d3e45e4a0e6c`  
		Last Modified: Fri, 01 Oct 2021 05:24:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e10ba5def77eae105b1dfab52bd41d16cba2895929673658ec8fedc7d8408e`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.3 MB (2274765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef565721758b7adafc1e282adeddbe68df6d6631699124a860c60f5c507840b4`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373c21a041dec3d49d5ab23634ca8c0141b8ec8504dfe832900a48a48baa5d10`  
		Last Modified: Fri, 01 Oct 2021 05:24:16 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1a9ce482ccd35a23b4f61715fd76783510d6fb7832e6db07a37f77a2d31f36`  
		Last Modified: Fri, 01 Oct 2021 05:24:29 GMT  
		Size: 87.1 MB (87089918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecedf97e512c4f6e245cac1ca1aa143939b0cda2428ac65a108fc40470870576`  
		Last Modified: Fri, 01 Oct 2021 05:24:15 GMT  
		Size: 5.6 KB (5608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d7c05c4a4da3313b71382230d55dfdb154f05dde2637cb5abd717516cc29c90e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124307877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06bb3c39ebf3550feb4449c7f08243564fad0a09635993f85486e2305d3a395d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:38:47 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 03:38:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:38:56 GMT
ENV GOSU_VERSION=1.13
# Fri, 01 Oct 2021 03:39:11 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 03:39:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 03:39:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:39:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Oct 2021 03:39:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 03:39:29 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 01 Oct 2021 03:39:29 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 01 Oct 2021 03:39:29 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Fri, 01 Oct 2021 03:39:29 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Fri, 01 Oct 2021 03:39:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Fri, 01 Oct 2021 03:39:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Oct 2021 03:39:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 01 Oct 2021 03:39:54 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Oct 2021 03:39:55 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Fri, 01 Oct 2021 03:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 03:39:55 GMT
EXPOSE 3306
# Fri, 01 Oct 2021 03:39:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d5ae241c1f10925c65b1658513761cd873e86632ea54cd491a17314c717db9`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1337b7de0aecaa84469be03f6aca5f4716813a7f70d6df52ada4f37e67dce98`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 5.5 MB (5455225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720ecfb64bf9977e96130e89f4d49759a1b9577aabaa5c864b0f7a3c0473f778`  
		Last Modified: Fri, 01 Oct 2021 03:44:03 GMT  
		Size: 3.4 MB (3368539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba0c987cf142da7e613c8eb5506412f33e85d62e8b737d82ae8a86dad1a3dd1`  
		Last Modified: Fri, 01 Oct 2021 03:44:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1cd2ca1d8beab7fe86d456206b59ee252c55fd199373f2caae49c71ec65a2a`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.2 MB (2203545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9328b4fc02fb1261cd4016d0e4d31dd6528b268e170d8278afbd062e3a96fa1`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba1c8ccb51c846dc0a9271404c54d1917897030f09c2df37204078c31ffae94`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c825ac5e690d987bb7c9e20ac4d482d0b3d6d45e43e686f5494169516ea6380`  
		Last Modified: Fri, 01 Oct 2021 03:44:14 GMT  
		Size: 86.1 MB (86097833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2376eebe2a30870028a6b6ab6b9cf1b96551befdbee8ed82a18e56a125c83397`  
		Last Modified: Fri, 01 Oct 2021 03:44:00 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; ppc64le

```console
$ docker pull mariadb@sha256:aa3c316f88dd9537eeaa7201d6d3c5f8d8732196ee6c9cd5ce553816c7a060d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137539722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a66b6be1b40e577fe733ec92528cf73ee97a8536e1fcddc9fe638aa9132f8173`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:34:53 GMT
ENV GOSU_VERSION=1.13
# Sat, 16 Oct 2021 01:35:28 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 01:35:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 01:36:02 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:36:03 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 16 Oct 2021 01:36:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 01:36:18 GMT
ARG MARIADB_MAJOR=10.6
# Sat, 16 Oct 2021 01:36:19 GMT
ENV MARIADB_MAJOR=10.6
# Sat, 16 Oct 2021 01:36:22 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Sat, 16 Oct 2021 01:36:24 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Sat, 16 Oct 2021 01:36:29 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Sat, 16 Oct 2021 01:36:39 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 16 Oct 2021 01:38:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 16 Oct 2021 01:39:01 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Oct 2021 01:39:03 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:39:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Oct 2021 01:39:08 GMT
EXPOSE 3306
# Sat, 16 Oct 2021 01:39:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bdbddf0ed762c90ab4fcfe1f42007a96e4f90ca4f0765dfcec52213a3f5c12`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 3.7 MB (3670760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cc95e86fb5ab1bda9839a1ecbd3c2d607bc6cfc5155f33bf32c9d7827ec98b`  
		Last Modified: Sat, 16 Oct 2021 01:49:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe2cefdba07cb9fc803227a545d4fcc196038c1020de7698bf4e333d9056cbd`  
		Last Modified: Sat, 16 Oct 2021 01:49:28 GMT  
		Size: 2.6 MB (2573066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab77c7b0e7b171541e9f7f813ef81190ef39151aea54bfe2b64f8c191ce672c`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d188c1c418692bd6c05728f7b542eab7acbdf502f48eaf84c762ba6b27718c`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288c0769408956c537d6b5b649bc2b69ffe5036157a0aa58dce6c17312680a33`  
		Last Modified: Sat, 16 Oct 2021 01:49:45 GMT  
		Size: 91.3 MB (91330343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4c9a0a37f40daaa1c904e99bb499d11db46dd87bd94236295d1ad90603ba74`  
		Last Modified: Sat, 16 Oct 2021 01:49:27 GMT  
		Size: 5.6 KB (5613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; s390x

```console
$ docker pull mariadb@sha256:90bc202cc092060b6e454b7f2d06cbe792ffd3d7a2edefe42e30964c55d24dab
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (126014128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b71468a7107bd097e1852fade221839dfd4b89ee873666b6f7beda44310b7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:02:36 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:02:41 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:02:42 GMT
ENV GOSU_VERSION=1.13
# Sat, 16 Oct 2021 01:02:50 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 01:02:51 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 01:02:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:02:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 16 Oct 2021 01:03:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 01:03:03 GMT
ARG MARIADB_MAJOR=10.6
# Sat, 16 Oct 2021 01:03:03 GMT
ENV MARIADB_MAJOR=10.6
# Sat, 16 Oct 2021 01:03:03 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Sat, 16 Oct 2021 01:03:04 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Sat, 16 Oct 2021 01:03:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Sat, 16 Oct 2021 01:03:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 16 Oct 2021 01:03:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 16 Oct 2021 01:03:26 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Oct 2021 01:03:26 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:03:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Oct 2021 01:03:26 GMT
EXPOSE 3306
# Sat, 16 Oct 2021 01:03:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc30a1fd200d10ce23e934b30e72d36ea131fb670d30afe697304591986fe1`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228a3fc0a9531bf3e9e08d9800daffbe33729ba8a16fb427b07a1a36fb047e02`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 5.4 MB (5380980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e511a129710d7aa78451eebec778e60a256b2a9e60db59a9f6d09641bd4f96`  
		Last Modified: Sat, 16 Oct 2021 01:04:32 GMT  
		Size: 3.2 MB (3239822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a9cf411b6c206dca4cd2f493440c36781e332782682bb40969b6640e8e98e9`  
		Last Modified: Sat, 16 Oct 2021 01:04:31 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cac3f3cdb186c64fce6e0a7efc39abe96d0e6ab755d9193c981cc44c801cc51`  
		Last Modified: Sat, 16 Oct 2021 01:04:31 GMT  
		Size: 2.2 MB (2188905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd5f55dd4f1666fe90f4ca1b3b0cc36a9092c44ae19033a4d2b7b0e2ff3dddb`  
		Last Modified: Sat, 16 Oct 2021 01:04:30 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0ae06775bbebbdaaf444830172bb614071d5d08004722e2ac0acc7dc0106c3`  
		Last Modified: Sat, 16 Oct 2021 01:04:30 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362403b21b44d69858c7a816e3ddbbd7cb67dac62386727c8ce11d44891fc990`  
		Last Modified: Sat, 16 Oct 2021 01:04:48 GMT  
		Size: 88.1 MB (88073232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48196c9046fbbce7d43754945286d36794d5f7eb923e2501d8a9a4ddc88b3dd3`  
		Last Modified: Sat, 16 Oct 2021 01:04:30 GMT  
		Size: 5.6 KB (5614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
